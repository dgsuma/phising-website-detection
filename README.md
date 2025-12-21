# Phishing Website Detection

## 📋 Table of Contents
- [Project Initialization](#project-initialization)
- [Virtual Environment Setup](#virtual-environment-setup)
- [ML Pipeline Execution](#ml-pipeline-execution)
- [ML Application](#ml-application)
- [MLFlow Configuration](#mlflow-configuration)
- [Docker Commands](#docker-commands)
- [AWS Configuration](#aws-configuration)

## 🚀 Project Initialization

Initialize the project with uv:

```bash
# Initialize project
uv init

# Rename default branch to main (recommended)
git branch -m master main

# Check uv version
uv --version

# List available Python versions
uv python list
```

## 🐍 Virtual Environment Setup

### Create Virtual Environment

```bash
# Create virtual environment with specific Python version
uv venv env --python cpython-3.11.13-windows-x86_64-none
```

### Activate Virtual Environment

**Windows:**
```bash
env\Scripts\activate
```

### Install Dependencies

```bash
uv pip install -r requirements.txt
```

## 🤖 ML Pipeline Execution

Run the training pipeline:

```bash
python -m run_pipeline
```

## 🌐 ML Application

Start the FastAPI application:

```bash
uvicorn api.main:app --reload
```

## 📊 MLFlow Configuration

### Installation

```bash
uv pip install mlflow
```

### Verify Installation

```bash
mlflow --version
```

### Start MLFlow UI

```bash
mlflow ui
```

After running the MLFlow UI, the dashboard will be available at: **http://127.0.0.1:5000**

📖 **Documentation:** [MLFlow Docs](https://mlflow.org/docs/3.2.0/)

## 🐳 Docker Commands

### Build Image

```bash
docker build -t test .
```

### Run Container

```bash
docker run --rm -p 8000:8005 test
```

**Note:** Access the application at **http://localhost:8000/**

### Manage Images and Containers

```bash
# List all Docker images
docker images

# Remove Docker image
docker rmi test

# List all containers
docker ps -a
```

## ☁️ AWS Configuration

### 🔐 Required Environment Variables

For CI/CD and cloud deployment, configure the following repository secrets:

- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`
- `AWS_REGION`
- `ECR_REPO`

### AWS Setup Instructions

#### 1. Create ECR Repository

1. Create an ECR repository in AWS Console
2. Copy the repository URI
3. Use this URI as the value for `ECR_REPO`

#### 2. Create IAM User

1. Create an IAM user in AWS Console
2. Attach the `AdministratorAccess` policy
3. Generate access keys for the user
4. Use these keys for `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY`
