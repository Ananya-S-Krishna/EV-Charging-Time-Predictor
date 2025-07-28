# EV Charging Time Predictor

This project predicts how long an electric vehicle (EV) will take to charge based on key battery and charging parameters. Built using real-world Level-3 fast-charging session data from EPFL-DESL, the model uses regression to learn relationships between state of charge, power input, and battery size.

## Problem Statement

Estimate EV charging time (in minutes) using:
- State of Charge (SOC) at arrival and departure
- Battery energy capacity (Wh)
- Max requested charging power (W)

## Tools & Technologies

- Python, Pandas, NumPy
- Scikit-learn (Random Forest Regressor)
- Matplotlib (for visualization)

## Workflow Summary

- Loaded real EV charging data from `Session_data.xlsx`
- Engineered SOC delta and selected key input features
- Trained a Random Forest Regressor to predict charging time
- Evaluated performance: R² ≈ 0.75, MAE ≈ 6 minutes
- Visualized predictions and feature importance

## Feature Importance Insight

Feature importance analysis showed that **SOC delta** is the dominant factor influencing charging time. This aligns with engineering intuition — higher SOC change means more energy is transferred, leading to longer charging duration.

## Outcome

A lightweight, interpretable model that connects data-driven prediction with real-world EV charging behavior - valuable for mechanical system design, battery management, and energy planning.
