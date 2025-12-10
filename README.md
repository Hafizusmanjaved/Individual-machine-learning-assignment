# Gaussian Mixture Models vs K-Means Clustering on Penguin Morphometrics

This repository contains a complete clustering analysis performed on the Palmer Penguins dataset, focusing on the comparison between Gaussian Mixture Models (GMM) and K-Means. The goal is to demonstrate how different clustering assumptions influence the grouping of multivariate biological measurements.

The project includes data preprocessing, exploratory analysis, Bayesian Information Criterion (BIC) for model selection, full GMM clustering with responsibilities, and a comparison with K-Means using standardised features.

---

## Repository Structure

.
│
├── README.md  
├── requirements.txt  
├── LICENSE  
│
├── notebooks/  
│   └── clustering_penguins.ipynb  
│
├── figures/  
│   ├── pairplot.png  
│   ├── bic_curve.png  
│   ├── gmm_clusters.png  
│   ├── responsibilities_hist.png  
│   ├── kmeans_clusters.png  
│   └── projection_gmm.png  
│
└── report/  
    ├── full_report.docx  
    └── full_report.pdf  

---

## Project Overview

The notebook compares two clustering techniques:

1. Gaussian Mixture Models (GMM)  
   - Learns ellipsoidal clusters.  
   - Supports different variances and orientations.  
   - Provides soft assignments through cluster responsibilities.

2. K-Means  
   - Produces spherical clusters with equal variance.  
   - Assigns each point to the nearest centroid.  
   - Computationally simple and widely used.

The project demonstrates how model assumptions affect clustering outcomes, particularly when natural group structure is complex and non-spherical.

---

## Dataset

The analysis uses a subset of the Palmer Penguins dataset containing four numeric features:

- bill_length_mm  
- bill_depth_mm  
- flipper_length_mm  
- body_mass_g  

Rows with missing values were removed for clean clustering.  
The dataset is loaded directly from seaborn, so no local CSV file is required.

---

## Installation

Install all required dependencies using:

pip install -r requirements.txt

A Python environment of version 3.9+ is recommended.

---

## Running the Notebook

Launch Jupyter Notebook:

jupyter notebook

Then open:

notebooks/clustering_penguins.ipynb

All outputs are already included for reproducibility.  
To regenerate, simply run all cells.

---

## Figures and Visualisations

All generated figures are stored in the figures/ directory, including:

- Pairplot of standardised features  
- BIC curve for GMM component selection  
- GMM cluster visualisation  
- Responsibility histogram to assess confidence  
- K-Means cluster comparison  

Each figure is accompanied by descriptive text inside the notebook and report for accessibility.

---

## Reproducibility Notes

- All feature standardisation uses StandardScaler.  
- GMM was fitted using full covariance matrices.  
- BIC selection identified 3 components as optimal.  
- Random seeds were fixed where applicable to ensure consistent results.  

---

## Accessibility Notes

- All images include descriptive captions.  
- Colourblind-safe palettes are used.  
- Figures include axis labels and readable fonts.  
- The report version of this project is screen-reader friendly.

---

## License

This project is released under the MIT License.  
See the LICENSE file for details.
