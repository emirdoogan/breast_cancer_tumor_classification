# Breast Cancer Classification

In this project the main goal is to classify tumors with less predictors (without losing significant accuracy) and choose the best model between Logistic Regression and Gaussian Naive Bayes.

## Code and Resources Used 

- **Python Version**: 3.10.9
- **Packages**: pandas, numpy, seaborn, matplotlib, sklearn
- **Dataset**: [Kaggle](https://www.kaggle.com/datasets/yasserh/breast-cancer-dataset)

## Data Exploration
- Some basic data exploration to understand the dataset better. For example count the total numbers of benign and malignant tumors:


  ![countplot](https://github.com/emirdoogan/breast_cancer_tumor_classification/blob/608aeefdcbbb5c02a0f6f7a8981496b01416d14d/countplot.png)

- Also looked for the correlations between features before creating the model.
- Checking for the missing data.

## Feature Selection
- Features that are not as significant as others have been removed and only the most important features kept. These are: 'concavity_mean', 'concave points_mean', 'perimeter_worst',
       'area_worst', 'concave points_worst'.

## Choosing The Best Model
- First cross validation performed for each model(Logistic Regression and Gaussian Naive Bayes). And then ROC AUC scores calculated for each model's cross validation.

<img width="372" alt="crossvalidationrocauc" src="https://github.com/emirdoogan/breast_cancer_tumor_classification/blob/608aeefdcbbb5c02a0f6f7a8981496b01416d14d/crossvalrocauc.png">

- Compare the performance metrics(ROC AUC, Precision, Recall, F1 Score) after splitting the dataset into a test and training data.
<img width="453" alt="Screen Shot 2023-09-20 at 7 23 13 PM" src="https://github.com/emirdoogan/breast_cancer_tumor_classification/blob/608aeefdcbbb5c02a0f6f7a8981496b01416d14d/gnbmetrics.png">
<img width="457" alt="Screen Shot 2023-09-20 at 7 23 04 PM" src="https://github.com/emirdoogan/breast_cancer_tumor_classification/blob/608aeefdcbbb5c02a0f6f7a8981496b01416d14d/lrmetrics.png">

- Visualize the ROC curves for both models.
  
![ROC](https://github.com/emirdoogan/breast_cancer_tumor_classification/blob/608aeefdcbbb5c02a0f6f7a8981496b01416d14d/roc.png)

## Conclusion
- Naive Bayes works better and superior based on performance metrics. However Logistic Regression is slightly better on ROC AUC scores for **cross-validation**. 
