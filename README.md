# Credit-Risk Analysis

## Description
Our objective in this project was to utilize multiple machine-learning algorithms paired with Logistic Regression to resample, fit and make predictions on a dataset containing Loan Statistics for Q1 of 2019. The following were used and the documentation is provided for further reading:
- Oversampling using [Random Over Sampler](https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.RandomOverSampler.html) and [SMOTE](https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.SMOTE.html) algorithms
- Undersampling using [Cluster Centroids](https://imbalanced-learn.org/stable/references/generated/imblearn.under_sampling.ClusterCentroids.html)
- Combination (Over & Under) sampling using SMOTE and Edited Nearest Neighbours [SMOTEENN](https://imbalanced-learn.org/stable/references/generated/imblearn.combine.SMOTEENN.html)
- Two machine learning models to help reduce bias when resampling, [BalancedRandomForestClassifier](https://imbalanced-learn.org/stable/references/generated/imblearn.ensemble.BalancedRandomForestClassifier.html) and [EasyEnsembleClassifier](https://imbalanced-learn.org/stable/references/generated/imblearn.ensemble.EasyEnsembleClassifier.html)

## Resources
For a better understanding concerning the measurements we will be looking at, it might be helpful to familiarize yourself with [Precision & Recall](https://en.wikipedia.org/wiki/Precision_and_recall). We will be using these measurements along with F1-measure to gauge which model performs the best overall.

## Results

## Oversampling
### RandomOverSample
balanced_accuracy_score: 0.6571

### SMOTE Oversampling
balanced_accuracy_score: 0.6536

## Undersampling

### ClusterCentroids
balanced_accuracy_score: 0.5442

### SMOTEENN
balanced_accuracy_score: 0.6786

## BalancedRandomForestClassifier
balanced_accuracy_score: 0.7878

## EasyEnsembleClassifier
balance_accuracy_score: 0.9254
