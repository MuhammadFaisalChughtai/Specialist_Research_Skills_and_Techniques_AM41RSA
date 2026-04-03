# Specialist Research Skills and Techniques (AM41RSA)

## Overview

This repository contains the research proposal source files for an MSc dissertation project titled:

**"Forecasting GB System Inertia: An Explainable Deep Learning Analysis of Renewable Generation Impacts"**

The proposal investigates how explainable AI (XAI), specifically SHAP, can be integrated with forecasting models to improve both prediction quality and operator trust in Great Britain's low-inertia power system context.

## Research Focus

The work addresses the operational challenge created by increasing renewable penetration (especially wind and solar), which reduces synchronous inertia and increases frequency stability risk.

Key objectives in the proposal:

- Forecast GB system inertia from historical generation mix and inertia data.
- Compare Bi-LSTM against ARIMA and XGBoost baselines.
- Apply SHAP-based interpretation to explain model predictions.
- Evaluate trade-offs between predictive performance and interpretability for safety-critical energy operations.

## Repository Structure

- `Research_Proposal_Latex/proposal_template.tex`: Main proposal manuscript in LaTeX.
- `Research_Proposal_Latex/references.bib`: Bibliography database used by the proposal.

## Method Summary (from proposal)

- **Data**: NESO system inertia and generation mix data (30-minute settlement interval).
- **Pipeline**: Time alignment, cleaning, interpolation, normalization, and feature engineering for synchronous vs asynchronous generation.
- **Models**: ARIMA, XGBoost, and Bi-LSTM.
- **Evaluation**: RMSE and MAE.
- **Interpretability**: SHAP analysis (including time-windowed interpretation strategy for time-series context).

## Requirements Mentioned in Proposal

- Python-based data pipeline for merging and preprocessing inertia + generation datasets.
- Forecasting framework covering ARIMA, XGBoost, and Bi-LSTM.
- SHAP visual outputs (summary and force-style explanations).
- Reproducible workflow suitable for standard Google Colab T4 usage.

## Compile the Proposal

From the `Research_Proposal_Latex` directory, compile with a LaTeX + Biber workflow:

```bash
pdflatex proposal_template.tex
biber proposal_template
pdflatex proposal_template.tex
pdflatex proposal_template.tex
```

If `latexmk` is available:

```bash
latexmk -pdf -bibtex proposal_template.tex
```

## Notes

- This repository currently contains proposal source files and references only.
- The README reflects the current LaTeX proposal content and cited literature in `references.bib`.
