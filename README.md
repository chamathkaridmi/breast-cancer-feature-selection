# 🎗️ Does Feature Selection Improve Model Performance?

> A comparative study of feature selection techniques applied to the  
> Breast Cancer Wisconsin Diagnostic Dataset

---

## 🧠 Overview

Medical diagnostic datasets are often **wide, noisy, and redundant**.  
This project investigates whether systematically reducing features from **30 → 8**  
using statistical filtering can build a **leaner, more accurate** breast cancer classifier.

**Hypothesis:** Feature selection improves model performance compared to using all available features.

---

## 📊 Key Results

| Metric | Baseline (30 feat.) | ✅ Selected (8 feat.) | Improvement |
|--------|--------------------|-----------------------|-------------|
| Accuracy | 95.26% | **97.36%** | +2.10% |
| Precision | 92.33% | **96.31%** | +3.98% |
| Sensitivity | 95.27% | **96.69%** | +1.42% |
| Specificity | 95.24% | **97.75%** | +2.51% |
| AUC | 96.30% | **99.15%** | +2.85% |

> 🔬 A paired t-test (p = 0.013) confirmed the improvement is **statistically significant** — not due to chance.

---

## 🔍 Methodology

    30 Features (Raw)
          ↓
    🧹 ANOVA Filter → removed 5 noise features (p ≥ 0.05)
          ↓
    🔗 Correlation Filter → removed 17 multicollinear duplicates (|r| > 0.8)
          ↓
    ✅ 8 Final Features — balanced predictive power + interpretability

### 🏆 The 8 Selected Features

1. `concave.points_worst` — strongest predictor (r = 0.79)
2. `perimeter_worst` — best size-related feature
3. `concave.points_mean` — complementary shape signal
4. `radius_mean` — baseline size indicator
5. `texture_worst` — surface variation
6. `smoothness_worst` — local radius variation
7. `symmetry_worst` — malignant tumors are less symmetric
8. `concave.points_se` — shape irregularity variability

---

## 🛠️ Tools Used

![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)

- **R** — glm, caret, ggplot2
- **Python** — rpy2 (Python-R bridge)
- **Platform** — Google Colab

---

## 📁 Dataset

[🔗 Breast Cancer Wisconsin Dataset — Kaggle](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data)

- 569 patient records
- 30 numerical features
- 2 target classes: Benign (63%) · Malignant (37%)

---

## 💡 Key Takeaway

> *"A carefully selected 8-feature model outperforms the 30-feature baseline  
> on every metric — while being 4× simpler and fully interpretable."*
