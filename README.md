# 🧮 Project 11 - FastAPI Calculator

This project adds a `Calculation` model to a FastAPI app using **SQLAlchemy** and **Pydantic**. It supports basic arithmetic operations (Add, Subtract, Multiply, Divide) and includes robust validation, optional use of the factory design pattern, and a full CI/CD pipeline using GitHub Actions and Docker Hub.

---

## 🚀 How to Run Tests Locally

# Step 1: Install requirements
pip install -r requirements.txt

# Step 2: Start PostgreSQL container
docker compose up -d

# Step 3: Run tests
python3 -m pytest

## ✅ Features

- **SQLAlchemy model**: `id`, `a`, `b`, `type`, `result`
- **Pydantic schemas with validation**:
  - `CalculationCreate` – accepts input
  - `CalculationRead` – returns full result
- **Optional Factory Pattern** for clean operation logic
- **Unit tests** for validation and logic
- **Integration tests** using PostgreSQL container
- **CI/CD with GitHub Actions**:
  - Run tests
  - Vulnerability scan with Trivy
  - Push Docker image to Docker Hub

## 🐳 Docker Hub

Docker image is available at:  
👉 [**https://hub.docker.com/repository/docker/fattylipid/project11**](https://hub.docker.com/repository/docker/fattylipid/project11)

To run the app locally with Docker:

```bash
docker compose up --build