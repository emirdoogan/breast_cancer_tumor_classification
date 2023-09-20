
# Breast Cancer Classification

In this project the main goal is to classify tumors with less predictors (without losing significant accuracy) and choose the best model between Logistic Regression and Gaussian Naive Bayes.

## Code and Resources Used 

- **Python Version**: 3.10.9
- **Packages**: pandas, numpy, seaborn, matplotlib, sklearn
- **Dataset**: [Kaggle](https://www.kaggle.com/datasets/yasserh/breast-cancer-dataset)

## Data Exploration
- Some basic data exploration to understand the dataset better. For example count the total numbers of benign and malignant tumors:
 ![countplot](https://github.com/emirdoogan/breast_cancer_tumor_classification/assets/55497482/7d1fb3dc-2613-47c1-821f-d30515243cfa)
- Also looked for the correlations between features before creating the model.
- Checking for the missing data.

## Feature Selection
- Features that are not as significant as others have been removed and only the most important features kept. These are: 'perimeter_mean', 'area_mean', 'area_se', 'perimeter_worst', 'area_worst'.

## Choosing The Best Model
- First cross validation performed for each model(Logistic Regression and Gaussian Naive Bayes). And then ROC AUC scores calculated for each model's cross validation.
<img width="372" alt="crossvalidationrocauc" src="https://github.com/emirdoogan/breast_cancer_tumor_classification/assets/55497482/38be7e43-4afe-43e2-ae47-1a4373f66734">
- Compare the performance metrics(ROC AUC, Precision, Recall, F1 Score) after splitting the dataset into a test and training data.
      


