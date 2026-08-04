# Stellar Luminosity Regression Refresher

## Purpose

This project explores the relationship between stellar mass and luminosity by implementing linear and polynomial regression from first principles (prediction, mean squared error, gradients, and gradient descent, all hand-written with NumPy). The goal is to understand how a regression model learns from data, compare a linear and a polynomial representation on the same small dataset, and reason about where each model's predictions can and cannot be trusted.

## Required libraries

- Python 3
- NumPy
- Matplotlib

## How to run

1. Create and activate a virtual environment (optional but recommended):
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```
2. Install the dependencies:
   ```bash
   pip install numpy matplotlib
   ```
3. Open `stellar_luminosity_hands_on.ipynb` in Jupyter (or VS Code) and run all cells from top to bottom.

## Main result

The polynomial model (`mass`, `mass²`) reaches a training cost about 8x lower than the linear model and tracks the curvature of the data much better within the observed mass range (0.6-2.4 solar masses). However, both models diverge sharply when extrapolated to a mass far outside that range (5.0 solar masses) — a reminder that a lower training cost does not, by itself, justify trusting a model's predictions outside the data it was trained on.