# Heart Disease Risk (Practice) — Classic ML
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)

![scikit-learn](https://img.shields.io/badge/scikit--learn-1.x-informational.svg)
![Pandas](https://img.shields.io/badge/Pandas-2.x-informational.svg)
![NumPy](https://img.shields.io/badge/NumPy-1.x-informational.svg)
![XGBoost](https://img.shields.io/badge/XGBoost-2.x-informational.svg)
![CatBoost](https://img.shields.io/badge/CatBoost-1.x-informational.svg)
![LightAutoML](https://img.shields.io/badge/LightAutoML-LAMA-informational.svg)

> ⚠️ **Disclaimer**: This is a practice/portfolio project based on a small, noisy dataset. Results are **not** for medical use.

## What's inside
- `Practice_classic_ML.ipynb` — single Jupyter notebook with EDA → preprocessing → modeling (classic ML classifiers).
- `requirements_from_notebook.txt` — quick list of Python deps auto-extracted from the notebook.

## Reproduce
```bash
python -m venv .venv && . .venv/bin/activate  # (or on Windows: .venv\Scripts\activate)
pip install -r requirements_from_notebook.txt
jupyter lab
```

Open the notebook and run cells top-to-bottom. Set `RANDOM_STATE` for reproducibility.

## Data
- **Not included** by default. Either:
  1. Use a public dataset (e.g., UCI Heart Disease) and set `DATA_PATH` accordingly; **or**
  2. Place your own CSV under `data/raw/heart.csv` and do **not** commit it if it has sensitive info.

If you use public data, add a link in this README and a short **Data Card**: source, size, license, known issues.

## Model Card (Short)
- **Task**: binary classification (heart disease risk proxy).
- **Models**: LogisticRegression, RandomForest, XGBoost/CatBoost (depending on availability).
- **Metrics**: ROC-AUC, PR-AUC, F1 (macro), recall@k (if applicable) via CV.
- **Limitations**: tiny sample → high variance; potential label noise; not for clinical decisions.

## License
- Code: MIT (suggested).
- Data: follow upstream license; **do not commit private/PHI data**.
