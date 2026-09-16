Support Vector Machine (SVM) — Breast Cancer Classification

📌 Project Overview

This project demonstrates the implementation of a Support Vector Machine (SVM) algorithm for classifying breast tumors as malignant or benign.

The project uses the Breast Cancer Wisconsin (Diagnostic) Dataset and covers the complete machine learning workflow, including data preprocessing, feature scaling, model training, prediction, and evaluation.

🎯 Objective

The objective of this project is to build an SVM classification model that can predict whether a breast tumor is:

Malignant (M) → 1
Benign (B) → 0
📊 Dataset

Dataset: Breast Cancer Wisconsin (Diagnostic)

The dataset contains 569 samples and 30 numerical features describing characteristics of cell nuclei.

Examples of features:

Mean Radius
Mean Texture
Mean Perimeter
Mean Area
Mean Smoothness
Mean Compactness
Mean Concavity
Mean Concave Points
Worst Radius
Worst Texture
Worst Perimeter
Worst Area

The diagnosis column is used as the target variable.

🛠️ Technologies Used
Python
Pandas
NumPy
Scikit-learn
Matplotlib
Jupyter Notebook
🔄 Machine Learning Workflow
Load Dataset
     ↓
Data Exploration
     ↓
Data Cleaning
     ↓
Select Features & Target
     ↓
Train-Test Split
     ↓
Feature Scaling
     ↓
Train SVM Model
     ↓
Make Predictions
     ↓
Evaluate Model
     ↓
Visualize Decision Boundary
🧹 Data Preprocessing

The following preprocessing steps were performed:

Removed unnecessary columns such as id.
Converted the target variable:
M → 1
B → 0
Checked for missing values.
Split the data into training and testing sets.
Standardized the features using StandardScaler.

Feature scaling is particularly important for SVM because SVM relies on distances and margins between data points.

🤖 Model

The project uses SVC from Scikit-learn.

from sklearn.svm import SVC

model = SVC(kernel="linear")
model.fit(X_train_scaled, y_train)
Why SVM?

SVM attempts to find a decision boundary that separates different classes while maximizing the margin between them.

For a linear SVM, the decision boundary can be represented as:

w₁x₁ + w₂x₂ + ... + wₙxₙ + b = 0

The data points closest to the decision boundary are called support vectors. These points play an important role in determining the position of the boundary.

🔬 SVM Concepts Covered

This project explores the following SVM concepts:

Hyperplane
Decision boundary
Margin
Support vectors
Linear kernel
Feature scaling
C parameter
Kernel functions
Model evaluation
📈 Evaluation

The trained model is evaluated using:

Accuracy
Confusion Matrix
Precision
Recall
F1-Score
Classification Report

Example:

from sklearn.metrics import accuracy_score, confusion_matrix, classification_report

print("Accuracy:", accuracy_score(y_test, y_pred))
print(confusion_matrix(y_test, y_pred))
print(classification_report(y_test, y_pred))
📊 Visualization

For understanding how SVM works geometrically, two features can be selected and plotted in 2D.

The visualization can show:

Data points
Decision boundary
Support vectors

Note that the original dataset contains 30 features, so a 2D visualization is only an educational representation and does not represent the complete 30-dimensional decision boundary.

📚 Key Learnings

Through this project, I learned:

  How SVM performs binary classification.
  Why feature scaling is important for SVM.
  How support vectors determine the decision boundary.
  How the C parameter affects model complexity.
  How different kernels can handle different types of decision boundaries.
  How to evaluate a classification model using multiple metrics.
  How to visualize a linear SVM using two features.
  🔮 Future Improvements
  Compare Linear, RBF, and Polynomial kernels.
  Perform hyperparameter tuning using GridSearchCV.
  Compare SVM performance with Logistic Regression and Random Forest.
  Analyze precision and recall more deeply.
  Build a simple prediction interface.
📜 License

This project is created for educational and learning purposes.
