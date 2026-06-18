🚢 Titanic Survival Prediction Portfolio Project


📌 Project Overview

The Titanic disaster is one of the most well-known events in history and has become a classic machine learning classification problem.

This project develops an end-to-end Machine Learning pipeline that predicts whether a passenger would survive the Titanic disaster based on passenger demographics and travel information.

The project goes beyond a simple assignment by incorporating:

Data Cleaning & Preprocessing
Exploratory Data Analysis (EDA)
Categorical Encoding
Feature Scaling & Standardization
Dimensionality Reduction (PCA)
Multiple Model Comparison
Stratified K-Fold Cross Validation
Hyperparameter Tuning (GridSearchCV)
Performance Evaluation
Feature Importance Analysis
Automated Survival Prediction for New Passengers

🎯 Problem Statement

Predict whether a Titanic passenger survived or not.

Target Variable:

Value	Meaning
1	Survived
0	Did Not Survive

This is a Binary Classification problem.

📂 Dataset

Titanic Passenger Dataset

Features include:

Passenger Class (Pclass)
Sex
Age
Fare
Number of Siblings/Spouses (SibSp)
Number of Parents/Children (Parch)
Embarkation Port
Ticket Information
Cabin Information

Target:

Survived


🔍 Exploratory Data Analysis


Key visualizations included:

Survival Distribution
Survival Rate by Gender
Survival Rate by Passenger Class
Survival Rate by Passenger Class and Gender
Age Distribution
Age Distribution by Survival
Fare Distribution
Survival Rate by Embarkation Port
Correlation Heatmap
Fare Distribution by Survival

Key Findings

✔ Female passengers had significantly higher survival rates.
✔ First-class passengers were more likely to survive.
✔ Higher ticket fares were associated with higher survival probability.
✔ Several features contained missing values requiring preprocessing.

⚙️ Data Preprocessing
Missing Value Handling
Feature	Strategy
Age	Median Imputation
Fare	Median Imputation
Embarked	Most Frequent Value
Cabin	Removed
Feature Engineering

Removed:

PassengerId
Name
Ticket
Cabin

These features either contained excessive missing values or required advanced feature engineering beyond the baseline model.

Encoding

Categorical variables were transformed using: OneHotEncoder()

Applied to:
Sex
Embarked
Passenger Class
Standardization

Numerical variables were standardized using: StandardScaler()

Applied to:
Age
Fare
SibSp
Parch
📉 Dimensionality Reduction

Principal Component Analysis (PCA) was used to reduce dimensionality while preserving 95% of the information.

PCA(n_components=0.95)

Benefits:
Reduced noise
Faster training
Better generalization
🤖 Machine Learning Models Evaluated

The following algorithms were compared:
Logistic Regression
K-Nearest Neighbors (KNN)
Support Vector Machine (SVM)
Decision Tree
Random Forest
Gradient Boosting
AdaBoost


🔄 Cross Validation

Stratified K-Fold Cross Validation was used.

StratifiedKFold(
    n_splits=5,
    shuffle=True,
    random_state=42
)

Evaluation Metrics:
Accuracy
Precision
Recall
F1-Score
ROC-AUC


🎛 Hyperparameter Tuning

The best-performing model was selected based on validation performance.

GridSearchCV was used to identify optimal hyperparameters.

GridSearchCV()

This ensured the final model achieved the best balance between bias and variance.



📊 Model Evaluation

Performance metrics include:
Accuracy Score
Precision
Recall
F1-Score
ROC-AUC Score
Confusion Matrix
Classification Report

Visualizations:
Confusion Matrix
ROC Curve
Model Comparison Chart
Feature Importance Chart


📈 Feature Importance Analysis
The project identifies which features contribute most to survival prediction.

Examples:
Sex
Passenger Class
Fare
Age

Feature importance was analyzed using: permutation_importance()



🚀 Final Prediction System

One of the portfolio enhancements in this project is a prediction system for new passengers.

Users can input passenger information:

Passenger Class
Sex
Age
Fare
SibSp
Parch
Embarked

The system automatically:

Cleans the input
Applies encoding
Applies scaling
Applies PCA transformation
Generates survival prediction

Output:

Prediction: Survived
or
Prediction: Did Not Survive


🛠 Technologies Used

Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-Learn
Google Colab
Jupyter Notebook

    ├── model_comparison.xlsx
    ├── classification_report.txt
    └── prediction_results.xlsx
