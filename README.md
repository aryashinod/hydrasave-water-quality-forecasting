# HydraSave: River Water Quality Forecasting and Pollution Control System

🏆 **Best Paper Award — IEEE ICCPCT 2023**

An end-to-end AI-driven forecasting pipeline built for the Kerala State Pollution
Control Board (KSPCB), using real Periyar River monitoring data to forecast next-year
water quality and assign usability grades supporting pollution-control decisions.

## Pipeline

1. **Preprocessing** — mean imputation → z-score normalization
2. **WQI Generation** — weighted-arithmetic Water Quality Index computation
3. **Forecasting** — CNN + Bi-LSTM model predicts year-ahead WQI
4. **Grading** — LightGBM classifies forecasted WQI into 5 water-quality grades
5. **Delivery** — results served through a lightweight web app (Anvil)

Built using 5 water quality parameters (DO, pH, BOD, FC, TC) across 8 monitoring
stations on the Periyar River.

## Tech Stack
Python, TensorFlow, CNN, Bi-LSTM, LightGBM, pandas, NumPy, Anvil

## Repository Structure
```
├── src/
│   ├── forecasting/       # CNN + Bi-LSTM forecasting pipeline
│   ├── lgbm_grading.ipynb # LightGBM water-quality grading model
│   └── webapp/            # Anvil web app for results delivery
├── data/
│   └── predicted.csv      # sample model output
├── docs/
│   └── hydrasave_accepted_paper.pdf
├── references/
└── requirements.txt
```

## Publication
A. Thankachan, D. Damodaran, A. B. Abraham, A. Shinod, S. M. Kurian, "HydraSave: A
Unique River Water Quality Forecasting and Pollution Control System," *2023
International Conference on Circuit Power and Computing Technologies (ICCPCT)*,
Kollam, India. **Best Paper Award.**

## My Contribution
Contributed across the full pipeline — preprocessing, WQI generation, the
CNN+Bi-LSTM forecasting model, and the LightGBM grading stage — as part of a
5-member team for this KSPCB-supported research project.

## Setup
```bash
pip install -r requirements.txt
```
