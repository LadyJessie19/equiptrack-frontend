# 🎨✨ EquipTrack-Lite Frontend

## Interface de Gerenciamento de Riscos de Equipamentos

### Uma SPA (*Single Page Application*) leve, desenvolvida com **Vue.js** e **Vite**, que consome o microserviço **Quarkus** para criar, visualizar e gerenciar equipamentos.

<img src="https://i.imgur.com/8QzXy2A.png" alt="Vue and Quarkus Logos" width="500" />

---

## 📋 Informações do Projeto

| Campo | Detalhe |
|--------|----------|
| **Nome do Projeto** | EquipTrack-Lite Frontend 🎨✨ |
| **Data de Início** | 11/10/2025 ⏩ |
| **Data de Término** | 12/10/2025 🏁 |
| **Status** | 🔨 Em Desenvolvimento (Foco no CRUD) |

---

## 💻 Tecnologias Utilizadas

- 💚 **Vue.js 3**
- ⚡ **Vite**
- 🧪 **Composition API**
- 📡 **Axios**
- 💅 **CSS Básico**

🔗 **Backend Quarkus:** [EquipTrack-Lite Backend](https://github.com/jessiemoura/equiptrack-lite-backend)

---

## 📝 Descrição do Projeto

O **EquipTrack-Lite Frontend** é a interface de usuário do sistema, responsável por interagir com o **microserviço backend Quarkus**.  
Esta aplicação demonstra o gerenciamento básico de ativos (equipamentos), representando a futura base para o **Gerenciamento de Riscos de Equipamentos**.

A interface implementa um **CRUD completo** (*Create, Read, Update, Delete*) comunicando-se via **RESTful API**.  
O foco principal é demonstrar o uso eficiente do **Composition API** do Vue para **reatividade e manipulação de formulários**.

---

## 🔧 Funcionalidades Principais

- ⚙️ **Visualização Reativa:** Lista de equipamentos atualizada em tempo real após operações CRUD.  
- 📝 **Cadastro Simples:** Formulário utilizando `v-model` (*Two-Way Data Binding*) para adicionar novos equipamentos.  
- 🔗 **Comunicação API:** Uso do **Axios** para chamadas `GET`, `POST` e `DELETE` com o backend Quarkus.  
- ⚡ **Reatividade Vue:** Gerenciamento de estado com `ref()` e `onMounted()`, similar aos *React Hooks*.

---

## 🔄 Instalação e Execução

> ⚠️ **Pré-requisito:** Certifique-se de que o [EquipTrack-Lite Backend (Quarkus)](https://github.com/jessiemoura/equiptrack-lite-backend) está rodando na porta `8080`.

### 1️⃣ Clone o repositório

```bash
git clone <link-do-seu-repo-frontend>
cd equiptrack-lite-frontend
````

### 2️⃣ Instale as dependências

```bash
npm install
# ou
yarn
```

### 3️⃣ Execute a aplicação

```bash
npm run dev
# ou
yarn dev
```

A aplicação estará disponível em:
👉 **[http://localhost:5173/](http://localhost:5173/)**

---

## 👩‍💻 Desenvolvido por Jessie Moura

<img src="assets/jessie-dev.jpg" alt="Jessie" width="200" />

💡 **Jessie M. Bentes** — *Fullstack Developer (foco em Backend Java com Spring Boot e Quarkus)*
🎨 Entusiasta de interfaces limpas, integrações elegantes e desenvolvimento ágil.
📬 Contato: [LinkedIn](https://www.linkedin.com/in/jessiemoura) | [GitHub](https://github.com/jessiemoura)

---

## 🪪 Licença

Este projeto é licenciado sob a [Licença MIT](https://opensource.org/licenses/MIT).