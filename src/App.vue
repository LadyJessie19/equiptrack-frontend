<script setup>
/* FIND ALL */

import { ref, onMounted } from "vue";
import axios from "axios";

// 1. URL base da sua API Quarkus
const API_URL = "http://localhost:8080/equipamentos";

// 2. Variável reativa para o estado da lista (Similar ao useState do React)
const equipamentos = ref([]);

// 3. Função para buscar os dados
const carregarEquipamentos = async () => {
  try {
    const response = await axios.get(API_URL);
    // .value é como você acessa/muda o valor de uma variável 'ref'
    equipamentos.value = response.data;
  } catch (error) {
    console.error("Erro ao carregar equipamentos:", error);
  }
};

// 4. Hook de ciclo de vida (Similar ao useEffect([], quando monta))
onMounted(async () => {
  await carregarEquipamentos();
});

/* CREATE */

// 5. Estado do formulário
const novoEquipamento = ref({
  nome: "",
  serialNumber: "",
  localizacao: "",
  riscoPontuacao: 1,
});

// 6. Função para submissão (POST)
const enviarFormulario = async () => {
  try {
    // 1. Envia os dados para a API
    await axios.post(API_URL, novoEquipamento.value);

    // 2. Atualiza a lista para mostrar o novo item
    await carregarEquipamentos();

    // 3. Limpa o formulário
    novoEquipamento.value = {
      nome: "",
      serialNumber: "",
      localizacao: "",
      riscoPontuacao: 1,
    };

    alert("Equipamento cadastrado com sucesso!");
  } catch (error) {
    console.error("Erro ao cadastrar equipamento:", error);
    alert("Falha ao cadastrar equipamento.");
  }
};

/* REMOVE */

// 7. Função para deletar
const deletarEquipamento = async (id) => {
  if (!confirm(`Tem certeza que deseja deletar o equipamento ID ${id}?`)) {
    return;
  }

  try {
    // 1. Chamada DELETE para a API
    await axios.delete(`${API_URL}/${id}`);

    // 2. Atualiza a lista (otimizado: remove o item localmente)
    equipamentos.value = equipamentos.value.filter((e) => e.id !== id);

    alert(`Equipamento ID ${id} deletado com sucesso!`);
  } catch (error) {
    console.error(`Erro ao deletar equipamento ID ${id}:`, error);
    alert("Falha ao deletar equipamento.");
  }
};
</script>

<template>
  <div class="container">
    <h1>EquipTrack-Lite 🛠️ | Gerenciamento de Equipamentos</h1>

    <form @submit.prevent="enviarFormulario" class="form-cadastro">
      <h2>+ Novo Cadastro</h2>
      <div>
        <label>Nome:</label>
        <input type="text" v-model="novoEquipamento.nome" required />
      </div>
      <div>
        <label>Serial:</label>
        <input type="text" v-model="novoEquipamento.serialNumber" required />
      </div>
      <div>
        <label>Localização:</label>
        <input type="text" v-model="novoEquipamento.localizacao" required />
      </div>
      <div>
        <label>Risco (1-5):</label>
        <input
          type="number"
          v-model.number="novoEquipamento.riscoPontuacao"
          min="1"
          max="5"
          required />
      </div>
      <button type="submit">Cadastrar Equipamento</button>
    </form>

    <hr />

    <p v-if="!equipamentos.length">
      Carregando ou nenhum equipamento cadastrado.
    </p>

    <table v-else>
      <thead>
        <tr>
          <th>ID</th>
          <th>Nome</th>
          <th>Serial</th>
          <th>Localização</th>
          <th>Risco</th>
          <th>Ações</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="equipamento in equipamentos" :key="equipamento.id">
          <td>{{ equipamento.id }}</td>
          <td>{{ equipamento.nome }}</td>
          <td>{{ equipamento.serialNumber }}</td>
          <td>{{ equipamento.localizacao }}</td>
          <td>{{ equipamento.riscoPontuacao }}</td>
          <td>
            <button @click="deletarEquipamento(equipamento.id)">
              🗑️ Deletar
            </button>
          </td>
        </tr>
      </tbody>
    </table>
  </div>

  <hr />
</template>

<style scoped>
/* Estilos básicos para a visualização */
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}
table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 20px;
}
th,
td {
  border: 1px solid #ccc;
  padding: 8px;
  text-align: left;
}
</style>
