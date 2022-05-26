# Risky Business
## Background

Mortgages, student and auto loans, and debt consolidation are just a few examples of credit and loans that people seek online. Peer-to-peer lending services such as Loans Canada and Mogo let investors loan people money without using a bank. However, because investors always want to mitigate risk, a client has asked that you help them predict credit risk with machine learning techniques.

In this project I will build and evaluate several machine learning models to predict credit risk using data you'd typically see from peer-to-peer lending services. Credit risk is an inherently imbalanced classification problem so I used the imbalanced-learn and Scikit-learn libraries to build and evaluate models using the two following techniques:

1) Resampling
2) Ensemble Learning

### Resampling

To begin:

1. Read the CSV into a DataFrame.

2. Split the data into Training and Testing sets.

3. Scale the training and testing data using the `StandardScaler` from `sklearn.preprocessing`.

4. Use the provided code to run a Simple Logistic Regression:
    * Fit the `logistic regression classifier`.
    * Calculate the `balanced accuracy score`.
    * Display the `confusion matrix`.
    * Print the `imbalanced classification report`.

#### Next:

1. Oversample the data using the `Naive Random Oversampler` and `SMOTE` algorithms.

2. Undersample the data using the `Cluster Centroids` algorithm.

3. Over- and undersample using a combination `SMOTEENN` algorithm.

#### Use the above to answer the following questions:

### Which model had the best balanced accuracy score?
> Oversampling, SMOTE, and under had equal 99.48% accuracy score
> 
### Which model had the best recall score?
> High risk Oversampling, High risk SMOTE, High risk Combination all had perfect recall
>
### Which model had the best geometric mean score?
> Smote, over, under, and combination all had geo scores of .99

### Ensemble Learning

In this section, I trained and compared two different ensemble classifiers to predict loan risk and then evaluated each model. I used Balanced Random Forest and Easy Ensemble Classifier.

To begin:

1. Read the data into a DataFrame using the provided starter code.

2. Split the data into training and testing sets.

3. Scale the training and testing data using the `StandardScaler` from `sklearn.preprocessing`.

4. Calculate the balanced accuracy score from `sklearn.metrics`.

5. Display the confusion matrix from `sklearn.metrics`.

6. Generate a classification report using the `imbalanced_classification_report` from imbalanced learn.

7. For the balanced random forest classifier only, print the feature importance sorted in descending order (most important feature to least important) along with the feature score.

Use the above to answer the following questions:

### Which model had the best balanced accuracy score?
> Easy Ensemble Classifier

### Which model had the best recall score?
> All but high risk in Easy Ensemble had perfect recall

### Which model had the best geometric mean score?
> Random Forest

### What are the top three features?
> loan_status_low_risk', loan_status_high_risk, total_rec_int
