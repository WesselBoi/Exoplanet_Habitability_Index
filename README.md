# Exoplanet Habitability Index (Kepler)

Classifies NASA Kepler exoplanets into three habitability levels:
**0 – non‑habitable**, **1 – partially habitable**, **2 – strictly habitable**.

## Overview

- Uses Kepler/Kaggle exoplanet catalog (planetary + stellar features).
- Habitability labels are defined from physical criteria (radius, Teq, insolation, stellar Teff).
- Handles extreme class imbalance with a **two‑stage model**:
  - Stage 1: detect candidate planets (0 vs 1+2).
  - Stage 2: distinguish partial vs strict habitability (1 vs 2).
- Outputs final 3‑class predictions and a ranking of top‑N most habitable planets.

## Tech stack

- **Python**, **NumPy**, **Pandas**
- **scikit‑learn** (preprocessing, metrics)
- **imbalanced‑learn** (SMOTE)
- **XGBoost** (hierarchical boosting models)
- **Matplotlib / Seaborn** (evaluation plots)
