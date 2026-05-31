 Microservices-Docker-Project

# 🚀 Containerizing & Orchestrating Microservices with Docker Compose

## 📌 Project Overview

This project demonstrates how to containerize and orchestrate a multi-service application using Docker and Docker Compose.

The application consists of:

- Frontend (React.js)
- Backend API (Node.js + Express.js)
- Database (MongoDB)

All services run in separate Docker containers and communicate through Docker Compose networking.

---

## 🏗️ Architecture

```text
                +-------------+
                |  Frontend   |
                |  React.js   |
                +------+------+
                       |
                       |
                       v
                +-------------+
                |   Backend   |
                | Express API |
                +------+------+
                       |
                       |
                       v
                +-------------+
                |   MongoDB   |
                |  Database   |
                +-------------+
```

---

## 🛠️ Technologies Used

- Docker
- Docker Compose
- React.js
- Node.js
- Express.js
- MongoDB
- AWS EC2
- Linux (Ubuntu)

---

## 📂 Project Structure

```text
Microservices-Docker-Project/
│
├── frontend/
│   ├── Dockerfile
│   ├── package.json
│   └── src/
│
├── backend/
│   ├── Dockerfile
│   ├── package.json
│   └── server.js
│
├── docker-compose.yml
├── .env.example
├── README.md
│
└── screenshots/
    ├── docker-ps.png
    ├── frontend-output.png
    └── backend-output.png
```

---

## ⚙️ Prerequisites

Before running the project, ensure the following are installed:

- Docker
- Docker Compose
- Git

Verify installation:

```bash
docker --version
docker compose version
git --version
```

---

## 🚀 Setup & Installation

### 1️⃣ Clone Repository

```bash
git clone https://github.com/YOUR_USERNAME/Microservices-Docker-Project.git

cd Microservices-Docker-Project
```

### 2️⃣ Create Environment File

Create `.env` file:

```env
MONGO_URI=mongodb://database:27017/microdb
```

### 3️⃣ Build Containers

```bash
docker compose build
```

### 4️⃣ Run Application

```bash
docker compose up --build
```

Run in background:

```bash
docker compose up -d
```

---

## 🐳 Docker Services

| Service | Technology | Port |
|----------|------------|------|
| Frontend | React.js | 3000 |
| Backend | Node.js + Express | 5000 |
| Database | MongoDB | 27017 |

---

## 🔍 Verify Running Containers

```bash
docker ps
```

Expected Output:

```text
frontend
backend
mongodb
```

---

## 🌐 Application Access

### Frontend

```text
http://54.179.33.203:3000
```

### Backend API

```text
http://<54.179.33.203>:5000
```

Expected Response:

```json
{
  "message": "Backend Running Successfully"
}
```

---

## 📊 Docker Compose Features

✅ Multi-container architecture

✅ Service-to-service communication

✅ Environment variable configuration

✅ MongoDB persistent storage using Docker Volumes

✅ Container orchestration using Docker Compose

✅ Backend service scaling support

---

## 📈 Scaling Backend Service

Scale backend containers:

```bash
docker compose up --scale backend=3
```

Verify:

```bash
docker ps
```

## 🧹 Useful Commands

### Stop Containers

```bash
docker compose down
```

### Restart Containers

```bash
docker compose up -d
```

### View Logs

```bash
docker compose logs
```

### Rebuild Project

```bash
docker compose up --build -d
```

---

## 🎯 Learning Outcomes

Through this project I learned:

- Docker Fundamentals
- Containerization of Applications
- Docker Compose Orchestration
- Multi-Container Deployments
- Environment Variable Management
- Volume Management
- Microservices Communication
- AWS EC2 Deployment

---

## 👨‍💻 Author

**Ashu Chamle**

Cloud & DevOps Enthusiast

- AWS
- Docker
- Linux
- CI/CD
- Terraform

---
