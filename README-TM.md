curl -LsSf https://astral.sh/uv/install.sh | sh
source $HOME/.cargo/env
source $HOME/.cargo/env
which uv
conda env create -n py-3.12 python=3.12
uv pip install --system --python 3.12 --no-cache -r requirements.txt

export UVICORN_HOST=0.0.0.0
export UVICORN_PORT=8000
uvicorn faster_whisper_server.server:app
