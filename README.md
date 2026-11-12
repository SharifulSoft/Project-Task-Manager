# 📋 Project Task Manager

A full-stack **collaborative task manager** where you can create tasks, register team members, and assign each task to a user. It's built with **React + Vite** on the front end and **Node.js, Express and MongoDB** on the back end.

![React](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?logo=mongodb&logoColor=white)

---

## ✨ Features

- **Create tasks** with a title and description
- **View all tasks** in one list
- **Assign tasks** to registered users (with a user search by first name)
- **Edit and delete** tasks
- **User sign-up** with first name, last name, email, password and role, plus form validation (valid email, password of 8+ characters)
- REST API backed by MongoDB Atlas

## 🛠 Tech Stack

| Layer    | Technology                                   |
|----------|----------------------------------------------|
| Frontend | React, React Router, Vite, CSS               |
| Backend  | Node.js, Express, CORS, dotenv               |
| Database | MongoDB (official `mongodb` driver)          |

## 📁 Project Structure

```
project-task-manager/
├── server-side/          # Express REST API
│   ├── index.js
│   └── .env.example
└── task-side/            # React + Vite client
    └── src/
        ├── App.jsx
        ├── component/    # TaskCreate, Tasks, AssignUser, SignIn, Login, NavBer
        └── utlis/        # Form validation helpers
```

## 🚀 Getting Started

### Prerequisites
- Node.js 18 or newer
- A MongoDB connection string (for example, from [MongoDB Atlas](https://www.mongodb.com/atlas))

### 1. Clone the repository
```bash
git clone https://github.com/SharifulSoft/Project-Task-Manager.git
cd Project-Task-Manager
```

### 2. Start the backend
```bash
cd server-side
npm install
cp .env.example .env      # then set MONGODB_URI to your own connection string
npx nodemon index.js      # or: node index.js
```
The API runs at **http://localhost:5000**.

### 3. Start the frontend
```bash
cd ../task-side
npm install
npm run dev
```
Open the URL Vite prints, usually **http://localhost:5173**.

## 🔐 Environment Variables (`server-side/.env`)

| Variable      | Description                          |
|---------------|--------------------------------------|
| `MONGODB_URI` | Your MongoDB connection string       |
| `PORT`        | API port (default `5000`)            |

## 📡 API Endpoints

| Method | Endpoint             | Description                               |
|--------|----------------------|-------------------------------------------|
| GET    | `/tasks`             | Get all tasks                             |
| POST   | `/tasks`             | Create a task                             |
| PUT    | `/tasks/:id`         | Update a task (title, description, user)  |
| DELETE | `/tasks/:id`         | Delete a task                             |
| GET    | `/assign/:id`        | Get a single task to assign               |
| GET    | `/users`             | Get users (`?firstName=` to search)       |
| POST   | `/users`             | Register a user                           |

## 👤 Author

**SharifulSoft**: [github.com/SharifulSoft](https://github.com/SharifulSoft)

⭐ If you find this project useful, please give it a star!
