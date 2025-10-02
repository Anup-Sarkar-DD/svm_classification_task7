<div style="text-align: center; margin-bottom: 20px;">
  <h1>Breast Cancer Classification using SVM & Feature Selection</h1>
</div>

- Loaded the Breast Cancer dataset (569 samples with 32 features), containing numeric data including mean, standard error, and worst values of cell nucleus characteristics such as radius, texture, perimeter, area, smoothness, compactness, concavity, concave points, symmetry, and fractal dimension.

- Performed initial exploratory data analysis (EDA):
  - Checked data structure and null/missing values.
  - Statistical summary with `.describe()` of features.
  - Visualized class distribution of diagnosis (Benign vs Malignant).

- Feature selection was done using a Random Forest Classifier to rank the importance of variables.
  - Top features selected include `concave points worst`, `concave points mean`, `concavity mean`, `radius mean`, `concavity worst`, among others.
  - Selected these top features for downstream modeling.

- Data preprocessing involved scaling features using `StandardScaler` to normalize the feature ranges.

- Splitting data:
  - The dataset was split into 80% training and 20% test sets maintaining the diagnosis ratio for stratification.

- Implemented Support Vector Machine (SVM) classification:
  - Trained baseline Linear SVM and RBF Kernel SVM.
  - Evaluated models on test set using classification reports and confusion matrices.

- Hyperparameter tuning for RBF SVM was performed using GridSearchCV with different values of `C` and `gamma` to optimize model performance.
  - Best parameters found were approximately `C=10` and `gamma=0.01`.
  - The tuned RBF SVM showed improved metrics with accuracy around 97%.

- Employed 5-fold cross-validation to confirm model robustness with mean accuracy near 96.8%.

- Visualized SVM decision boundaries on the first two principal components for interpretability.

- Optional PCA was applied to visualize the data distribution and class separability in 2D space.

- Overall, SVM with tuned RBF kernel effectively classifies breast cancer data, demonstrating high precision, recall, and F1-scores in distinguishing benign and malignant diagnoses.

- Key metrics:
  - Accuracy: ~97%
  - High precision and recall for both classes
  - Confusion matrices show low misclassification

This notebook consolidates data preprocessing, feature selection, model training, tuning, and evaluation for breast cancer classification using SVM, showcasing strong predictive performance on benchmark medical data.

