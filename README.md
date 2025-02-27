# Decision Trees, LASSO, and Boosting for Regression

## Overview

This project explores **interpretable models and regression techniques**, focusing on **Decision Trees, LASSO, Principal Component Regression (PCR), and Gradient Boosting**. The tasks involve handling missing data, feature selection, and optimizing models for better generalization.

## Key Objectives

- **Decision Trees for Interpretability:**
  - Build and visualize decision trees for classification.
  - Convert decision trees into **IF-THEN rules**.
  - Apply **cost-complexity pruning** for a more interpretable model.

- **Regression Methods:**
  - Train **Linear Regression, Ridge Regression, LASSO, and PCR**.
  - Use **cross-validation** to optimize hyperparameters.
  - Analyze feature selection using **Coefficient of Variation (CV)**.

- **Boosting with XGBoost:**
  - Train a **Gradient Boosting Tree** for regression.
  - Use **ℓ1-penalized regression at decision nodes**.
  - Optimize **regularization parameter (α) using cross-validation**.

## Datasets

### **1️⃣ Acute Inflammations Dataset (Decision Trees)**
- **Source**: [UCI Repository](https://archive.ics.uci.edu/ml/datasets/Acute+Inflammations)
- **Description**: Multi-class classification dataset used for interpretable tree models.

### **2️⃣ Communities and Crime Dataset (Regression)**
- **Source**: [UCI Repository](https://archive.ics.uci.edu/ml/datasets/Communities+and+Crime)
- **Description**: Predicting violent crime rates based on demographic, economic, and law enforcement attributes.
- **Preprocessing**:
  - Handle **missing values** using imputation.
  - Perform **feature selection using variance and scatter plots**.

## Methodology

### **1️⃣ Decision Trees for Interpretability**
- Train a **decision tree** and visualize it.
- Convert the tree into **IF-THEN rules** for interpretability.
- Apply **cost-complexity pruning** to simplify the tree while retaining accuracy.

---

### **2️⃣ Feature Selection & Data Preprocessing**
- Compute the **Coefficient of Variation (CV)** for all features.
- Select **top √128 features** for analysis.
- Generate **scatter plots and box plots** for selected features.

---

### **3️⃣ Regression Models**
#### **A. Linear & Ridge Regression**
- Train a **Least Squares Linear Regression model**.
- Train a **Ridge Regression model**, tuning **λ (regularization parameter)** via **cross-validation**.
- Report **test error** for both models.

#### **B. LASSO Regression**
- Train **LASSO Regression**, selecting **λ via cross-validation**.
- Compare **standardized vs. non-standardized features**.
- Report **test error and selected features**.

#### **C. Principal Component Regression (PCR)**
- Train **PCR**, selecting the number of **principal components (M)** via **cross-validation**.
- Compare test error with other regression models.

---

### **4️⃣ Boosting with XGBoost**
- Train an **XGBoost model** for regression.
- Implement **ℓ1-penalized regression at each node** for feature selection.
- Tune **α (regularization term) via cross-validation**.
- Compare results with other regression models.

---

## Results & Insights

- **Pruned Decision Trees** improved interpretability while maintaining accuracy.
- **LASSO Regression selected key predictive features**, reducing overfitting.
- **PCR performed well in reducing dimensionality** while maintaining performance.
- **Gradient Boosting with ℓ1-penalization outperformed other models**, particularly in high-dimensional settings.

---

## Technologies Used

- **Python** (NumPy, Pandas, Matplotlib, Scikit-Learn)
- **Machine Learning Models**:
  - **Decision Trees** (with Cost-Complexity Pruning)
  - **Linear Regression, Ridge, LASSO, PCR**
  - **Gradient Boosting (XGBoost)**
- **Feature Selection**:
  - **Coefficient of Variation (CV)**
  - **Scatter Plots & Box Plots**
- **Hyperparameter Tuning**:
  - **Cross-validation for λ (regularization)**
  - **Principal Component Selection (PCR)**
  - **ℓ1-Regularization for Boosting Trees**

---

## Future Improvements

- **Experiment with other feature selection techniques** (e.g., mutual information).
- **Try advanced boosting frameworks** (e.g., LightGBM, CatBoost).
- **Analyze model robustness** under different missing data imputation methods.

