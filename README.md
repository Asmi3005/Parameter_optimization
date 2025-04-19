#  SVM Optimization on Letter Recognition Dataset

This project implements a hyperparameter tuning routine for Support Vector Machines (SVMs) on the **Letter Recognition dataset** using a small training sample size of only **50 instances** per run. The objective is to evaluate how well SVM can perform under extreme data constraints and observe convergence behavior of the optimization process.

---

## 📚 Dataset

- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/letter+recognition)
- **Dataset ID:** 59 (via `ucimlrepo`)
- **Classes:** 26 (A–Z uppercase letters)
- **Samples:** 20,000 instances with 16 numerical features per sample

---

## 🚀 Objective

To simulate a metaheuristic-style optimization for SVM hyperparameters:
- **Kernel**
- **C (regularization parameter)**
- **Gamma (kernel coefficient)**

The training is deliberately limited to only 50 rows to test the robustness of SVM under low-data conditions.

---

## ⚙️ Methodology

1. **Data Preprocessing**
   - Scaled features using `StandardScaler` (SVMs are sensitive to feature ranges)
   - Stratified split into train/test (70:30)

2. **Optimization Loop**
   - For 10 different random samples (with 50 training rows each)
   - Try 100 random combinations of SVM hyperparameters
   - Track and store the best configuration and its accuracy
   - Log progress every iteration

3. **Visualization**
   - Plotted convergence of best accuracy per iteration for the best-performing run


