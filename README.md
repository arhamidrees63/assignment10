# 🧩 Module 10 – Secure User Model, Validation, and Docker CI/CD  
**Author:** Muhammad Arham  
 
---

## 🚀 Overview
This project implements a secure FastAPI application with:
- A **User model** using **SQLAlchemy** and **Pydantic** schemas  
- **Password hashing** and verification for authentication security  
- **Unit**, **integration**, and **end-to-end** tests with `pytest`  
- Full **CI/CD pipeline** via **GitHub Actions** and **Docker Hub**  
- A **PostgreSQL** backend running in a Docker container  

---

## 🧱 Features
✅ Secure user registration and login  
✅ Unique username and email constraints  
✅ Password hashing with verification  
✅ Automated testing and coverage reporting  
✅ Dockerized environment for development and deployment  
✅ CI/CD pipeline to build and push Docker images  

---

## ⚙️ Local Setup Instructions

### 1️⃣ Clone the Repository
```bash
git clone git@github.com:arhamidrees63/assignment10.git
cd assignment10
2️⃣ Create and Activate Virtual Environment
bash
Copy code
python3 -m venv venv
source venv/bin/activate
3️⃣ Install Dependencies
bash
Copy code
pip install -r requirements.txt
4️⃣ Start Docker Containers
bash
Copy code
docker compose up -d --build
This spins up:

fastapi_calculator → your FastAPI web app

postgres_db_module10 → PostgreSQL instance

pgadmin → optional web interface at http://localhost:5050

🧪 Run Tests
bash
Copy code
pytest -v
Unit tests: validate logic, password hashing, and schema correctness

Integration tests: verify database operations and API routes

E2E tests: confirm UI calculator operations via Playwright

Expected result:
✅ 74 passed, 1 skipped
✅ ~98% coverage

🐳 Docker Commands
Build and run manually:

bash
Copy code
docker build -t howdynutz/module10_is601 .
docker run -p 8000:8000 howdynutz/module10_is601
Access the app at:
👉 http://localhost:8000

⚡ CI/CD Pipeline (GitHub Actions)
Located in .github/workflows/.

Pipeline Tasks:

Run tests with pytest

Build Docker image

Push image to Docker Hub (after successful test run)

You can check your workflow runs here:
🔗 GitHub Actions Tab

🐋 Docker Hub Repository
Once pushed, your image will be available here (example):
🔗 https://hub.docker.com/r/arhamidrees63/module10_is601

(replace with your actual Docker Hub link once image is pushed)

🧠 Reflection
During this module, I learned how to:

Structure a secure FastAPI project with proper database models and schemas

Use Pydantic for input validation and data serialization

Implement password hashing and verification for user security

Integrate PostgreSQL with SQLAlchemy

Run and automate tests using pytest and GitHub Actions

Build and deploy Docker containers in a CI/CD pipeline

The biggest challenge was debugging Docker-Postgres compatibility and ensuring tests used a clean database state. Resolving that improved my understanding of container orchestration and environment isolation.

