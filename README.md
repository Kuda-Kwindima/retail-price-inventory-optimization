# Retail Price & Inventory Optimization

## Objective
Build a demand forecasting model to improve inventory and pricing decisions across Walmart stores.

This project combines:
- Time series feature engineering
- Machine learning (XGBoost regression)
- Baseline comparison (lag-based naive model)
- Time-aware validation split

---

## Dataset
Walmart Recruiting: Store Sales Forecasting (Kaggle)

Time range:
2010-02-05 → 2012-10-26

---

## Model Performance

Baseline (lag_1):
- MAE: ~1547
- RMSE: ~3442

XGBoost Model:
- MAE: ~1423
- RMSE: ~2872

Model outperforms naive baseline by ~8–17%.

---

## Feature Engineering

- Lag features (1, 4, 52 weeks)
- Rolling means (4, 12 weeks)
- Holiday indicator
- Promotional markdown handling
- Store type encoding

---

## Repository Structure

- `src/` → Modular pipeline (ingest, transform, feature, train, evaluate)
- `notebooks/` → EDA & experimentation
- `data_raw/` → Raw datasets (excluded from Git)

---

## Next Steps

- SHAP explainability (regression)
- Error segmentation (holiday vs non-holiday)
- Inventory optimization layer
- Docker containerization