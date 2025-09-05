# Task Manager API – Backend (Node.js + MySQL)

A simple and extensible backend API built with **Node.js**, **Express**, and **MySQL**, designed for managing tasks with full CRUD operations and user authentication.

<p align="center">
  <img alt="Node.js" src="https://img.shields.io/badge/Node.js-18+-339933?logo=node.js&logoColor=white">
  <img alt="Express.js" src="https://img.shields.io/badge/Express.js-4.x-black?logo=express&logoColor=white">
  <img alt="MySQL" src="https://img.shields.io/badge/MySQL-8.x-4479A1?logo=mysql&logoColor=white">
  <img alt="License" src="https://img.shields.io/badge/License-MIT-blue">
</p>

---

## ✨ Features
- RESTful API for task management
- CRUD endpoints (Create, Read, Update, Delete)
- Authentication and login flow
- MySQL database integration
- Modular code structure for easy extension

---

## 📂 Project Structure
.
├─ authentication.js      # Middleware for token verification
├─ db_connection.js       # Database connection logic
├─ db_properties.js       # Database configuration
├─ server.js              # App entry point (Express server)
├─ login.js               # User login handler
├─ task.js                # Task model
├─ get.js                 # Endpoint: get all tasks
├─ getbyid.js             # Endpoint: get task by id
├─ insert.js              # Endpoint: insert new task
├─ update.js              # Endpoint: update task
└─ delete.js              # Endpoint: delete task
---

## 🚀 Getting Started

### 1. Prerequisites
- Node.js 18+  
- MySQL 8+  
- npm  

### 2. Setup Database
```sql
CREATE DATABASE task_manager;

USE task_manager;

CREATE TABLE tasks (
  id INT AUTO_INCREMENT PRIMARY KEY,
  title VARCHAR(255) NOT NULL,
  status ENUM('open','in_progress','done') DEFAULT 'open',
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);


3. Configure Environment

Update db_properties.js (or add .env if you refactor) with your database credentials:

module.exports = {
  host: "localhost",
  user: "your_mysql_user",
  password: "your_mysql_password",
  database: "task_manager",
};

4. Install & Run
npm install
node server.js

🔌 API Endpoints

Tasks
	•	GET /tasks → Get all tasks
	•	GET /tasks/:id → Get task by ID
	•	POST /tasks → Insert a new task
	•	PUT /tasks/:id → Update task by ID
	•	DELETE /tasks/:id → Delete task by ID

Authentication
	•	POST /auth/login → User login (returns token)
	•	Protected routes require header:

Authorization: Bearer <JWT_TOKEN>

📜 License

MIT License © 2022 Gunapu Bhargava
---

This version is **ready to paste** directly into your project.  
Do you also want me to generate a **banner/logo image** (ASCII or Shields-style) for the very top so it looks extra eye-catchy on GitHub?
