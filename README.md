# Renewable Energy Forecasting with Machine Learning

**Bachelor's Thesis – Smart and Sustainable City Management**  
**Universitat Autònoma de Barcelona (UAB) | 2025–26**  
**Author:** Arnau Ropero Garcia  
**Supervisor:** Juan Carlos Valle López

---

## Overview

This repository contains the code and models developed for the final degree project on renewable energy generation forecasting using Machine Learning. The project uses hourly solar and wind generation data from Spain (2023–2025) and evaluates three ML models: Prophet, XGBoost and LSTM.

The central case study is the **Iberian Peninsula blackout of April 28, 2025**. The models are used to detect anomalous deviations from meteorologically expected generation, evidencing the non-meteorological nature of the blackout.

---

## Models

| Model | Solar MAE (val) | Solar MAE (test) | Wind MAE (val) | Wind MAE (test) |
|-------|:-:|:-:|:-:|:-:|
| Prophet | 1,346 MW | 2,060 MW | 1,913 MW | 1,711 MW |
| XGBoost | 311 MW | 415 MW | 387 MW | 378 MW |
| LSTM | 405 MW | 580 MW | 375 MW | 350 MW |
| Naïve baseline | 1,071 MW | 1,297 MW | 406 MW | 443 MW |

---

## Repository Structure

```
├── notebooks/
│   ├── descarrega_entsoe.ipynb       # ENTSO-E data download
│   ├── fusio_preprocessament.ipynb   # Data fusion and preprocessing
│   ├── prophet_model.ipynb           # Prophet model
│   ├── xgboost_model.ipynb           # XGBoost model
│   └── lstm_model.ipynb              # LSTM model
├── models/
│   ├── prophet_solar.json
│   ├── prophet_eolic.json
│   ├── xgboost_solar.json
│   ├── xgboost_eolic.json
│   ├── lstm_solar.keras
│   └── lstm_eolic.keras
├── figures/                          # Generated plots
└── data/
    └── README.md                     # How to obtain the dataset
```

---

## Requirements

```
Python 3.12
tensorflow
xgboost
prophet
scikit-learn
pandas
numpy
matplotlib
entsoe-py
```

---

## Data

The dataset is not included in this repository. See `data/README.md` for instructions on how to reproduce it from public sources (ENTSO-E and Open-Meteo).

---

## License

MIT License
