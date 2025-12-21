Project Initialization
# Initialize project with uv
uv init
git branch -m master main

# Check uv version and Python installations
uv --version
uv python list

# Create virtual environment with specific Python version
uv venv env --python cpython-3.11.13-windows-x86_64-none

Virtual Environment Activation & Dependencies
# Activate virtual environment (Windows)
env\Scripts\activate

# Install requirements
uv pip install -r requirements.txt

ML Pipeline Execution
# Run training pipeline
python -m run_pipeline

ML Application
# Start FastAPI application
uvicorn api.main:app --reload

MLFlow Configuration
# Install MLFlow
uv pip install mlflow

# Check MLFlow version
mlflow --version

# Start MLFlow UI
mlflow ui

After running mlflow ui, the dashboard will be available at: http://127.0.0.1:5000

📖 MLFlow Documentation: https://mlflow.org/docs/3.2.0/

Docker Commands
# Build Docker image
docker build -t test .

# Run Docker container
docker run --rm -p 8000:8005 test

# List all Docker images
docker images

# Remove Docker image
docker rmi test

# List all containers
docker ps -a

Note: After running the container, access the application at: http://localhost:8000/

Required Secrets/Environment Variables
Repository Secrets (for CI/CD/Cloud deployment):
1. AWS_ACCESS_KEY_ID

2. AWS_SECRET_ACCESS_KEY

3. AWS_REGION

4. ECR_REPO