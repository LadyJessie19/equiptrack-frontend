# 🎨✨ EquipTrack-Lite Frontend
#### 👉 _[Ler em Português](./README.md)_

## Equipment Risk Management Interface

### A lightweight Single Page Application (SPA) built with **Vue.js** and **Vite**, consuming the **Quarkus** microservice to create, view, and manage equipment.

<img src="https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExaWdtMHNkczF5cTdsaW40bjA1ajhuZ3U3bmxxZTAyODA4bXpheWozZSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/adXwYTDvQNOMCggg8i/giphy.gif" alt="Vue and Quarkus Logos" width="500" />

---

## 📋 Project Information

| Field | Detail |
|--------|----------|
| **Project Name** | EquipTrack-Lite Frontend 🎨✨ |
| **Start Date** | 10/11/2025 ⏩ |
| **End Date** | 10/12/2025 🏁 |
| **Status** | ✔ Completed |

---

## 💻 Technologies Used

- 💚 **Vue.js 3**
- ⚡ **Vite**
- 🧪 **Composition API**
- 📡 **Axios**
- 💅 **Basic CSS**

🔗 **Quarkus Backend:** [EquipTrack-Lite Backend](https://github.com/LadyJessie19/equiptrack-backend)

---

## 📝 Project Description

The **EquipTrack-Lite Frontend** is the user interface of the system, responsible for interacting with the **Quarkus backend microservice**.  
This application demonstrates basic asset (equipment) management, serving as the foundation for the future **Equipment Risk Management** module.

The interface implements a full **CRUD** (Create, Read, Update, Delete) communicating through a **RESTful API**.  
The main goal is to demonstrate effective use of Vue's **Composition API** for **reactivity and form handling**.

---

## 🔧 Main Features

- ⚙️ **Reactive Display:** Equipment list updates automatically after CRUD operations.  
- 📝 **Simple Registration:** Form using `v-model` (Two-Way Data Binding) to add new equipment.  
- 🔗 **API Communication:** Uses **Axios** for `GET`, `POST`, and `DELETE` requests to the Quarkus backend.  
- ⚡ **Vue Reactivity:** State management with `ref()` and `onMounted()`, similar to React Hooks.

---

## 🔄 Installation & Execution

> ⚠️ **Prerequisite:** Ensure the [EquipTrack-Lite Backend (Quarkus)](https://github.com/LadyJessie19/equiptrack-backend) is running on port `8080`.

### 1️⃣ Clone the repository

```bash
git clone https://github.com/LadyJessie19/equiptrack-frontend.git
cd equiptrack-frontend
````

### 2️⃣ Install dependencies

```bash
npm install
# or
yarn
```

### 3️⃣ Run the application

```bash
npm run dev
# or
yarn dev
```

The application will be available at:
👉 **[http://localhost:5173/](http://localhost:5173/)**

---

## 👩‍💻 Developed by Jessie Moura

<img src="public/jessica.png" alt="Jessie" width="200" />

💡 **Jessie M. Bentes** — Fullstack Developer (focus on Backend Java with Spring Boot and Quarkus)

🎨 Enthusiast of clean interfaces, elegant integrations, and agile development.

📬 Contact: [LinkedIn](https://www.linkedin.com/in/jessiemoura) | [GitHub](https://github.com/LadyJessie19)

---

## 🚪 License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).
