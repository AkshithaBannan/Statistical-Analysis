# Statistical Analysis & Data Preprocessing Pipeline

Welcome to the **Statistical Analysis** repository. This project contains end-to-end Python implementations of core statistical workflows—bridging raw data exploration, mathematical feature transformation, and parametric interval estimation.

---

## Table of Contents
* [Overview](#-overview)
* [Notebooks & Module Architecture](#-notebooks--module-architecture)
  * [1. Exploratory Data Analysis & Feature Engineering](#1-exploratory-data-analysis--feature-engineering)
  * [2. Inferential Estimation & Confidence Intervals](#2-inferential-estimation--confidence-intervals)
* [Data Engineering & Modeling Strategy](#-data-engineering--modeling-strategy)
* [Technologies Used](#-technologies-used)
* [Getting Started](#-getting-started)

---

## Overview

This repository demonstrates the practical application of statistical theories to real-world datasets. The pipelines handle everything from diagnosing data skewness and outlier evaluation to executing geometric scaling and predictive interval modeling.

---

## Notebooks & Module Architecture

### 1. Exploratory Data Analysis & Feature Engineering (`statistics-1.ipynb`)
Focused on evaluating a multi-dimensional retail sales performance dataset containing metrics like volumes, margins, and applied pricing structures.
* **Descriptive Metrics:** Calculated mean, median, mode, and standard deviation distributions to interpret central tendencies.
* **Asymmetry Mapping:** Computed mathematical skewness values alongside `matplotlib` box plots to isolate features exceeding upper-whisker boundaries.
* **Categorical Feature Slicing:** Structured targeted `groupby` aggregations to map revenue vectors against dimensions like Business Units (`BU`), unique `Model` iterations, and temporal identifiers.

### 2. Inferential Estimation & Confidence Intervals (`Confidence Interval.ipynb`)
Focused on evaluating sample representatives to construct mathematical probability boundaries around unknown population targets.
* **Unknown Variance Modeling ($t$-distribution):** Built a 99% confidence interval loop tracking custom sample statistics using degrees of freedom ($df = n-1$).
* **Known Variance Projections ($Z$-distribution):** Generated a 99% standard normal estimation curve assuming specified historical population deviations.

---

## Data Engineering & Modeling Strategy

To ensure data readiness for modern downstream machine learning models, the following processing foundations were engineered:

* **Z-Score Normalization:** Handled feature scaling using `sklearn.preprocessing.StandardScaler` to map disparate financial matrices into bounded variance spaces centered cleanly between $[-3, +3]$.
* **One-Hot Encoding (Dummification):** Converted text arrays (`Brand`, `Model`, `SKU`) into machine-readable boolean vectors using `pd.get_dummies()` to completely mitigate implicit order biases during optimization.

---

## Technologies Used

* **Languages:** Python (Pandas, NumPy)
* **Mathematical Analytics:** SciPy, Statsmodels
* **Feature Processing:** Scikit-Learn (`StandardScaler`)
* **Visualization Engine:** Matplotlib, Seaborn

---

## Getting Started

To step through the notebook pipelines locally:

1. Clone this repository:
   ```bash
   git clone [https://github.com/AkshithaBannan/Statistical-Analysis.git](https://github.com/AkshithaBannan/Statistical-Analysis.git)
