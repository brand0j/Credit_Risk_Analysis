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

### Random Over Sample

![cm_RandomOverSample](https://github.com/brand0j/Credit_Risk_Analysis/blob/main/Resources/cm_RandomOverSample.PNG)
![class_report_RandomOverSample](https://github.com/brand0j/Credit_Risk_Analysis/blob/main/Resources/class_report_RandomOverSample.PNG)

**Balanced Accuracy Score**: *0.6571*

### SMOTE Oversampling

![cm_SMOTE](https://github.com/brand0j/Credit_Risk_Analysis/blob/main/Resources/cm_SMOTE.PNG)
![class_report_SMOTE](https://github.com/brand0j/Credit_Risk_Analysis/blob/main/Resources/class_report_SMOTE.PNG)

**Balanced Accuracy Score**: *0.6536*

## Undersampling

### Cluster-Centroids

![cm_ClusterCentroids](https://github.com/brand0j/Credit_Risk_Analysis/blob/main/Resources/cm_ClusterCentroids.PNG)
![class_report_ClusterCentroids](https://github.com/brand0j/Credit_Risk_Analysis/blob/main/Resources/class_report_ClusterCentroids.PNG)

**Balanced Accuracy Score**: *0.5442*

## Combined (Over & Under) Sampling

### SMOTEENN
![cm_SMOTEENN](https://github.com/brand0j/Credit_Risk_Analysis/blob/main/Resources/cm_SMOTEENN.PNG)
![class_report_SMOTEENN](https://github.com/brand0j/Credit_Risk_Analysis/blob/main/Resources/class_report_SMOTEENN.PNG)

**Balanced Accuracy Score**: *0.6786*

## Ensemble Classifiers

### Balanced Random Forest Classifier

![cm_BalancedRandomForestClassifier](https://github.com/brand0j/Credit_Risk_Analysis/blob/main/Resources/cm_BalancedRandomForestClassifier.PNG)
![class_report_BalancedRandomForestClassifier](https://github.com/brand0j/Credit_Risk_Analysis/blob/main/Resources/class_report_BalancedRandomForestClassifier.PNG)

**Balanced Accuracy Score**: *0.7878*

### Easy Ensemble Classifier (AdaBoost)

![cm_EasyEnsembleAdaBoostClassifier](https://github.com/brand0j/Credit_Risk_Analysis/blob/main/Resources/cm_EasyEnsembleAdaBoostClassifier.PNG)
![class_report_EasyEnsembleAdaBoostClassifier](https://github.com/brand0j/Credit_Risk_Analysis/blob/main/Resources/class_report_EasyEnsembleAdaBoostClassifier.PNG)

**Balanced Accuracy Score**: *0.9254*
