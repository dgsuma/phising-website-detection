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
