# 🏥 Healthcare Management System

A production-ready fullstack web application to manage healthcare records — built using React, Spring Boot, PostgreSQL, Docker, GitHub Actions CI/CD, and cloud deployments via Render & Railway.

---

## ⚙️ Tech Stack

| Layer       | Technology                  |
|------------|-----------------------------|
| Frontend    | React (CRA)                 |
| Backend     | Spring Boot (Java 21)       |
| Database    | PostgreSQL                  |
| Container   | Docker + Docker Compose     |
| CI/CD       | GitHub Actions              |
| Backend Host| Render                      |
| DB Host     | Railway                     |

---

## 📁 Project Structure
healthcare-management-system/

├── backend/ # Spring Boot backend

│ ├── Dockerfile # Container definition for backend

│ └── src/ # Java source files

├── frontend/ # React frontend (CRA)

│ ├── Dockerfile # Container definition for frontend

│ ├── .env # Contains REACT_APP_API_URL

│ └── src/ # React source files

├── docker-compose.yml # Compose file to run all services locally

└── .github/

└── workflows/

└── ci-cd-backend.yml # GitHub Actions: CI/CD to Render backend



---

## 🌐 Deployment URLs

| Service   | URL |
|-----------|-----|
| Frontend  | `https://cicd-healthcare-management-system.vercel.app/` |
| Backend   | `https://cicd-healthcaremanagementsystem.onrender.com/` |
| API Test  | `https://cicd-healthcaremanagementsystem.onrender.com/api/patients` |
| DB        | Railway (persistent Postgres) |

---

## 🔐 Environment Configuration

### 🔹 Backend (`application.yml`)

Use environment variables, not hardcoded values:

```yaml
spring:
  datasource:
    url: ${SPRING_DATASOURCE_URL}
    username: ${SPRING_DATASOURCE_USERNAME}
    password: ${SPRING_DATASOURCE_PASSWORD}


