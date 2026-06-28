# M. A. Halim — standalone model repo

This repository is **Halim only** — no HANOON trading bot code.

## Clone + run

```bash
git clone https://github.com/sajibmdsaberahmad-create/M-A-Halim.git
cd M-A-Halim
git lfs pull
pip install -e ".[hf]"
export HALIM_REPO_ROOT="$PWD"
export HALIM_LM_BACKEND=hf
export HALIM_MODEL_PATH=data/checkpoints/latest
export HALIM_FORCE_LM=true
python halim/serve.py
```

Health: `curl http://127.0.0.1:8765/health`

## Contents

- `halim/` — Python package (serve, engine, inference)
- `data/checkpoints/toddler_v1/` — Colab-trained toddler LM (Git LFS)
- `scripts/` — train, register checkpoint, prepare SFT
- `colab/` — Google Colab training notebooks
