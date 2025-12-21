## command for initilizing the project
uv init
git branch -m master main
uv --version
uv python list
uv venv env --python cpython-3.11.13-windows-x86_64-none

Activate the env with : env\Scripts\activate
Then install requirements : uv pip install -r requirements.txt

## command for executing the training pipeline
python -m run_pipeline


## command for running the ml application
uvicorn api.main:app --reload

## command for configuring the mlflow in ml project
uv pip install  mlflow
mlflow --version
mlflow ui
After this mlflow ui will automatically popped up onto this url:
127.0.0.1:5000
Mlflow document: https://mlflow.org/docs/3.2.0/
