 Income Classification Project
This project involves building a machine learning model to predict whether an individual's income exceeds $50K per year based on census data. The dataset used is the well-known UCI Adult Income dataset, also known as the "Census Income" dataset.

Dataset Overview
The dataset contains demographic and employment-related attributes such as:

Age

Education

Occupation

Hours-per-week

Capital gain/loss

Native country

... and more

Target Variable:

<=50K — Low income

>50K — High income

Objective
To build a classification pipeline that predicts income category (<=50K or >50K) based on available features, and evaluate the model performance using precision, recall, F1-score, and accuracy.

 Exploratory Data Analysis (EDA)
EDA was performed to understand:

Class imbalance in the income column

Distributions of features like age and hours-per-week

Correlation between features and income

Categorical feature value counts

Visualizations used:

Count plots

Box plots


Preprocessing Steps:
Replaced missing values (?) with np.nan

Dropped rows with missing values (can be replaced with imputation)

Label-encoded the target variable

Applied One-Hot Encoding to categorical features

Used Pipelines and a ColumnTransformer to process numerical and categorical features separately

Model
Algorithm used:

RandomForestClassifier from sklearn.ensemble

Performance (on test set):

Metric	<=50K	>50K
Precision	0.88	0.72
Recall	0.92	0.62
F1-score	0.90	0.66

Overall Accuracy: 85%
Macro Avg F1-score: 78%

The model performs well overall, especially for the majority class. However, it struggles more with correctly identifying high-income individuals.

 Future Improvements
Apply SMOTE or class weighting to improve recall for the >50K class

Try other models like XGBoost or Logistic Regression
