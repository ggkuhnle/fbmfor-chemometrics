# FBMFOR — Chemometric Analysis for Food Fraud Detection

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOURUSERNAME/FBMFOR-chemometrics/blob/main/FBMFOR_Chemometrics_Analysis.ipynb)
[![GitHub Pages](https://img.shields.io/badge/docs-GitHub%20Pages-blue)](https://YOURUSERNAME.github.io/FBMFOR-chemometrics/)

Interactive chemometric analysis notebook for the **MSc Food Technology and Quality Assurance** module on food fraud analysis at the University of Reading.

## Overview

This notebook provides a complete pipeline for multivariate analysis of spectroscopic data (NMR, FTIR) in food authentication:

| Method | Type | Purpose |
|--------|------|---------|
| **PCA** | Unsupervised | Exploratory analysis, outlier detection, variance structure |
| **HCA** | Unsupervised | Hierarchical clustering, dendrogram visualisation |
| **PLS-DA** | Supervised | Classification with cross-validation, VIP scores |
| **OPLS-DA** | Supervised | Orthogonal signal correction, S-plot biomarker identification |

Preprocessing options include baseline correction (ALS), normalisation (SNV, area, min-max), and Savitzky-Golay derivatives.

## Quick Start

1. Click the **Open in Colab** badge above (or [this link](https://colab.research.google.com/github/YOURUSERNAME/FBMFOR-chemometrics/blob/main/FBMFOR_Chemometrics_Analysis.ipynb))
2. Run the cells sequentially — the demo dataset (simulated olive oil FTIR) loads automatically
3. To use your own data, uncomment the upload cells in Section 3

## Data Format

The notebook expects **two CSV files**:

**Spectral data** (`spectra.csv`):

| Sample_ID | 4000.0 | 3997.8 | ... | 400.0 |
|-----------|--------|--------|-----|-------|
| EVOO_01   | 0.032  | 0.028  | ... | 0.015 |
| ROO_01    | 0.041  | 0.035  | ... | 0.018 |

**Metadata** (`metadata.csv`):

| Sample_ID | Class |
|-----------|-------|
| EVOO_01   | EVOO  |
| ROO_01    | ROO   |

## Repository Structure

```
├── noebooks
│   └── FBMFOR_Chemometrics_Analysis.ipynb   # Main analysis notebook
├── index.qmd                                # Quarto landing page (→ GitHub Pages)
├── _quarto.yml                              # Quarto project configuration
├── styles.css                               # Custom styling for the site
├── .github/
│   └── workflows/
│       └── publish.yml                      # GitHub Actions workflow for Pages
├── .nojekyll                                # Bypass Jekyll on GitHub Pages
└── README.md                                # This file
```

## GitHub Pages Site

The documentation site is built with [Quarto](https://quarto.org) and deployed automatically via GitHub Actions. It provides an overview of the notebook, links to Colab, and guidance for students.

### Setup (one-time, for the repository owner)

1. Push this repository to GitHub
2. Go to **Settings → Pages → Source** and select **GitHub Actions**
3. The site will build and deploy automatically on each push to `main`

> **Note:** Replace `YOURUSERNAME` with your GitHub username and `FBMFOR-chemometrics` with your repository name in the badge URLs above and in `_quarto.yml`.

## Dependencies

All dependencies are available in Google Colab by default:

- numpy, pandas, scipy
- scikit-learn
- plotly
- matplotlib

## References

- Trygg, J. & Wold, S. (2002). Orthogonal projections to latent structures (O-PLS). *J. Chemometrics*, 16(3), 119–128.
- Barker, M. & Rayens, W. (2003). Partial least squares for discrimination. *J. Chemometrics*, 17(3), 166–173.
- Eilers, P.H.C. & Boelens, H.F.M. (2005). Baseline correction with asymmetric least squares smoothing.

## Licence

This material is provided for educational use within the University of Reading MSc programme. 

## Contact

**Gunter Kuhnle**
Department of Food and Nutritional Sciences, University of Reading
g.g.kuhnle@reading.ac.uk
