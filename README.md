# MachineLearning_Classification-Project

# Risky Business

![Credit Risk](Images/credit-risk.jpg)

## Background

Mortgages, student and auto loans, and debt consolidation are just a few examples of credit and loans that people seek online. Peer-to-peer lending services such as Loans Canada and Mogo let investors loan people money without using a bank. However, because investors always want to mitigate risk, this project deals with predicting credit risk with machine learning techniques.

This involves building and evaluating several machine learning models to predict credit risk using data one would typically see from peer-to-peer lending services. Credit risk is an inherently imbalanced classification problem (the number of good loans is much larger than the number of at-risk loans), so one needs to employ different techniques for training and evaluating models with imbalanced classes. This involves using the imbalanced-learn and Scikit-learn libraries to build and evaluate models using the two following techniques:

1. [Resampling](#Resampling)
2. [Ensemble Learning](#Ensemble-Learning)

- - -

### Files

[Resampling Starter Notebook](Starter_Code/credit_risk_resampling.ipynb)

[Ensemble Starter Notebook](Starter_Code/credit_risk_ensemble.ipynb)

[Lending Club Loans Data](Instructions/Resources/LoanStats_2019Q1.csv.zip)

- - -

### Instructions

#### Resampling

The [imbalanced learn](https://imbalanced-learn.readthedocs.io) library was used to resample the LendingClub data and build and evaluate logistic regression classifiers using the resampled data.

It was required to:

1. Oversample the data using the `Naive Random Oversampler` and `SMOTE` algorithms.

2. Undersample the data using the `Cluster Centroids` algorithm.

3. Over- and undersample using a combination `SMOTEENN` algorithm.


For each of the above, it was required to:

1. Train a `logistic regression classifier` from `sklearn.linear_model` using the resampled data.

2. Calculate the `balanced accuracy score` from `sklearn.metrics`.

3. Calculate the `confusion matrix` from `sklearn.metrics`.

4. Print the `imbalanced classification report` from `imblearn.metrics`.


Using the above, the following observations were made:

* Logistic Regression model with SMOTE oversmapling had the best balanced accuracy score, very closely followed by Random Oversampling and Combination (SMOTEEN) Sampling.
>
* It was a tie between Random oversampling, SMOTE Oversampling and Combination(SMOTEEN) Sampling for best recall score.
>
* It was also a tie between Random oversampling, SMOTE Oversampling and Combination(SMOTEEN) Sampling for the best geometric mean score.

#### Ensemble Learning

In this section,  two different ensemble classifiers were trained and compared to predict loan risk and each model was evaluated. The use of `balanced random forest classifier` and the `easy ensemble AdaBoost classifier` was made.

The following steps were completed for each model:

1. Train the model using the quarterly data from LendingClub provided in the `Resource` folder.

2. Calculate the balanced accuracy score from `sklearn.metrics`.

3. Print the confusion matrix from `sklearn.metrics`.

4. Generate a classification report using the `imbalanced_classification_report` from imbalanced learn.

5. For the balanced random forest classifier only, print the feature importance sorted in descending order (most important feature to least important) along with the feature score.


Using the above information, the following observations were made:

* The Easy Ensemble Classifier model had the better balanced accuracy score.

* It was a tie between Random Forest Classifier and Easy Ensemble Classifier for the best recall score.

* It was also a tie between Random Forest Classifier and Easy Ensemble Classifier for the best geometric mean score.

* The top three features to be included in our model are "Borrower's Income", "Interest Rate" and "Debt to Income Ratio". Other features which may be look at are "Total Debt" and "Loan Size".



