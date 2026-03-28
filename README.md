# Titanic Survival Analysis

Overview
Predicting passenger survival on the Titanic using machine learning (Logistic Regression). Built on pre-processed dataset with 100 passenger records and 17 engineered features.
Dataset

Total Records: 100 passengers
Total Features: 17 (pre-processed & encoded)
Target Variable: Survived (0 = Did Not Survive, 1 = Survived)
Overall Survival Rate: 36%

Analysis Performed
1. Exploratory Data Analysis (EDA)

Distribution analysis of survival by demographics
Survival rates by gender, passenger class, age, and fare
Visualization of key patterns

2. Statistical Analysis

Correlation analysis with survival outcomes
Significance testing (point-biserial correlation)
Key finding: Sex and Fare showed statistically significant relationships (p < 0.05)

3. Predictive Modeling

Algorithm: Logistic Regression
Train-Test Split: 80-20
Features Used: All 16 features (excluding PassengerId and Unnamed column)

4. Model Evaluation

Confusion matrix analysis
Classification report (precision, recall, F1-score)
Feature importance ranking

Key Findings
Survival Distribution

Did Not Survive: 64 passengers (64%)
Survived: 36 passengers (36%)

Survival Rates by Demographics
By Gender:

Female survival: 68.57%
Male survival: 18.46%
Gender was the strongest predictor (correlation: -0.498)

By Passenger Class:

1st Class survival: 73.91%
2nd Class survival: 35.00%
3rd Class survival: 21.05%

By Fare:

Average fare of survivors: $0.08
Average fare of non-survivors: $0.03
Higher fare strongly correlated with survival (correlation: 0.380)

By Age:

Age was NOT a significant predictor (p-value: 0.761)

Statistical Significance
VariableCorrelationP-ValueSignificantSex-0.49790.000000✓ YESFare0.37970.000098✓ YESAge0.03080.761079✗ NO
Model Performance
Accuracy

Training Accuracy: 87.50%
Test Accuracy: 95.00%
Model Status: EXCELLENT ✓

Classification Report (Test Set)
ClassPrecisionRecallF1-ScoreSupportDid Not Survive0.921.000.9612Survived1.000.880.938Overall0.950.950.9520
Confusion Matrix
                Predicted: No    Predicted: Yes
Actual: No           12              0
Actual: Yes           1              7
Breakdown:

True Negatives: 12 (correctly identified non-survivors)
False Positives: 0 (no false alarms)
False Negatives: 1 (missed 1 survivor)
True Positives: 7 (correctly identified survivors)

Feature Importance
Top 5 Survival Predictors
Positive Impact (Increase Survival):

Title_3: +1.1095
Pclass_1 (1st Class): +1.0820
Emb_1 (Embarked Port 1): +0.2722

Negative Impact (Decrease Survival):

Sex (Male): -1.8310 (strongest negative predictor)
Pclass_3 (3rd Class): -0.8997
Title_4: -0.7998

Tools & Technologies Used

Language: Python 3
Data Processing: Pandas, NumPy
Machine Learning: Scikit-learn
Visualization: Matplotlib, Seaborn
Environment: Jupyter Notebook

Project Deliverables

titanic_analysis.ipynb - Complete analysis notebook with all code
titanic_cleaned.csv - Processed dataset ready for analysis
visualizations/ folder containing:

survival_overview.png - Survival distribution charts
correlation_matrix.png - Feature correlation heatmap
confusion_matrix.png - Model performance visualization
feature_importance.png - Feature importance ranking chart
