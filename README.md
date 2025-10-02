# Breast Cancer Classification with SVM

## Project Overview
This project performs binary classification of breast cancer tumors (malignant vs benign) using Support Vector Machines (SVM). It uses the Breast Cancer Wisconsin dataset from Kaggle and covers comprehensive data science steps from exploratory data analysis to model tuning and evaluation.

## Dataset
The Breast Cancer Wisconsin (Diagnostic) dataset consists of 569 samples described by 30 numeric features computed from digitized images of fine needle aspirate (FNA) of breast masses.

## Project Steps

1. **Data Loading and Inspection**
   - Imported dataset and inspected structure, missing values, and statistics.
   
2. **Exploratory Data Analysis (EDA)**
   - Visualized diagnosis distribution and tumor feature distributions.
   - Detected outliers using boxplots.
   
3. **Data Cleaning**
   - Handled outliers by clipping extreme values using the IQR method.
   - Removed highly correlated features to reduce multicollinearity.
   
4. **Feature Engineering**
   - Encoded target diagnosis column into binary format (M=1, B=0).
   - Evaluated feature importance with Random Forest and selected the top features.
   - Performed dimensionality reduction with PCA for visualization.
   
5. **Preprocessing**
   - Applied feature scaling (StandardScaler) to numeric features.
   - Split the data into training and testing sets in a stratified manner.
   
6. **Model Building and Evaluation**
   - Trained SVM classifiers with linear and RBF kernels.
   - Evaluated classification performance using accuracy, precision, recall, F1-score, and confusion matrices.
   - Tuned hyperparameters (C and gamma) via grid search and cross-validation.
   - Visualized SVM decision boundaries on 2D projections.
   
7. **Cross-Validation**
   - Performed 5-fold cross-validation to estimate the model’s generalization performance.

## Technologies and Libraries
- Python 3.x
- Pandas, NumPy for data manipulation
- Matplotlib, Seaborn for visualization
- Scikit-learn for modeling and evaluation

## Usage
- Clone repository.
- Install required dependencies.
- Follow the notebooks or scripts to run the analysis and model training steps.

## Author
- [Your Name or GitHub handle]

---

This project demonstrates a practical data science workflow for medical data classification problems using SVMs with end-to-end processing, visualization, and tuning.
