# Does Feature Selection Improve Model Performance?

A comparative study of feature selection techniques applied to the 
Breast Cancer Wisconsin Diagnostic dataset.

## Overview
This project investigates whether reducing features from 30 to 8 
using ANOVA and Pearson correlation filtering improves logistic 
regression performance for breast cancer classification.

## Key Results
| Metric | Baseline (30 feat.) | Selected (8 feat.) |
|--------|--------------------|--------------------|
| Accuracy | 95.26% | 97.36% |
| Precision | 92.33% | 96.31% |
| AUC | 96.30% | 99.15% |

A paired t-test (p = 0.013) confirmed the improvement is 
statistically significant.

## Tools Used
- R (glm, caret, ggplot2)
- Python / Google Colab
- rpy2 (Python-R bridge)

## Dataset
[Breast Cancer Wisconsin Dataset - Kaggle](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data)
