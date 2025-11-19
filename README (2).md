
# Time Series Forecasting with LSTM / GRU + Hyperparameter Optimization

## Project Overview
This repository contains a reproducible project for time series forecasting using RNN architectures (LSTM and GRU). It demonstrates:
- Synthetic multivariate time series generation
- Preprocessing: scaling and windowing
- Baseline naive model comparison
- Simple LSTM and GRU models (quick mode)
- (Optional) hyperparameter tuning with Keras Tuner (longer run)

## Files
- `project_script.py` - Main runnable script with code and explanation in-block.
- `README.md` - This file.
- Output folder created when running: `/mnt/data/ts_project_output` containing `results.json`.

## Requirements
Install the following (example):
```bash
pip install numpy pandas scikit-learn matplotlib tensorflow keras-tuner
```

If `keras-tuner` import fails, try:
```bash
pip install keras-tuner
```

## How to run
1. Open a terminal in the directory containing `project_script.py`.
2. Run:
```bash
python project_script.py
```
This will run in "quick" mode (short training). To run full hyperparameter tuning, edit the `main` call in the script and set `quick=False`.

## Deliverables to prepare (suggested)
- Executable Python script / Jupyter notebook (this repo contains the script)
- A short report (text) describing:
  - Data source (synthetic), preprocessing steps, optimization strategy
  - Comparative metrics (Baseline vs LSTM vs GRU)
  - Final model choice justification
- Save model weights and results (script creates `results.json`)

## Notes & Next steps
- Replace synthetic data generator with a real dataset (e.g., `sklearn.datasets.fetch_openml`, or your CSV).
- For multi-step forecasting, adapt the target construction and model output layer.
- Add SHAP or other explainability for local/global insights (for LSTM/GRU consider model-agnostic explainers).
