# Balancing the Scales: Optimizing Churn Prediction with different Machine Learning Models
## Project Overview and Objectives
- The project outlines a comprehensive approach to predicting customer churn using a Telco dataset.
- The project investigates how imbalanced datasets affect machine learning models and explores various resampling techniques (like oversampling, SMOTE, and undersampling) to address this imbalance.
- The primary goal is to improve churn prediction by preprocessing the data, performing exploratory data analysis (EDA), balancing the classes, and comparing several classification models.

## Data Preprocessing and EDA
- The process began with an initial review of the dataset, cleaning, and handling missing values.
- Additional steps included outlier detection, binning of the 'tenure' feature into groups (TenureGroup), and standardizing binary/categorical columns for consistency.
- Exploratory Data Analysis provided insights into customer demographics, service usage, and contract/payment methods, setting the stage for modeling.

## Model Training and Comparison
- A Random Forest Classifier (RFC) was trained on a balanced version of the dataset—balanced using SMOTE, which increased the proportion of the minority class (churn).
- The model’s performance was evaluated on a split of the data with balanced class weights. It was compared against other models, such as Support Vector Classifier (SVC) and K-Nearest Neighbors (KNN).
- The RFC outperformed the other models, delivering strong results across key metrics (accuracy, precision, recall, and F1-score). A stacking classifier was also tested and showed slightly better F1 performance but at the cost of added complexity.

## Evaluation Strategy
- Cross-validation was employed to ensure robust performance estimation and to mitigate overfitting.
- Evaluation metrics were focused particularly on the minority class (churning customers), with RFC demonstrating an optimal balance.

## Resampling Methods and Their Impact
Three main resampling techniques reviewed include:
- Oversampling: Increases minority class samples by duplication but risks overfitting.
- SMOTE: Generates synthetic samples and is shown to improve minority class predictions with lower overfitting risk.
- Undersampling: Reduces majority class samples but may lose important information.

Comparative metric scores illustrated that SMOTE provided a better balance without the high overfitting risk associated with simple oversampling.

## Conclusions
- The combination of SMOTE and the Random Forest Classifier proved to be the most effective approach for handling imbalanced data and predicting customer churn.
- The project concludes that while alternative models and methods exist, the robustness and balanced performance of the RFC make it the preferred choice for this dataset.

This summary encapsulates the methodology, key analyses, model comparisons, and conclusions drawn.

