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


### SMOTE Oversampling

![cm_SMOTE](https://github.com/brand0j/Credit_Risk_Analysis/blob/main/Resources/cm_SMOTE.PNG)
![class_report_SMOTE](https://github.com/brand0j/Credit_Risk_Analysis/blob/main/Resources/class_report_SMOTE.PNG)

**Balanced Accuracy Score (RandomOverSample)**: *0.6571*

**Balanced Accuracy Score(SMOTE)**: *0.6536*

In this comparison we are looking at the overall performance between using ```RandomOverSample()``` and ```SMOTE()``` in python. While both are oversampling techniques, they differ slightly in their application. The key difference of SMOTE() is how the minority class is increased (for an instance in the minority class, a number of it's closest neighbors are chosen and based on those values, new ones are created). When comparing the two models it's important to keep in mind what our objective is so we can determine which one performs better on the dataset we are working with. As you can see above, both models are comparible when looking at the balanced accuracy scores and their precision (low-risk & high-risk), but the main difference is their sensitivity to both of these classifications. Using ```RandomOverSample()``` results in a sensitivity of 71% (high-risk) & 60% (low-risk), compared to ```SMOTE()``` which yields a sensitivity of 61% (high-risk) & 69% (low-risk). In the context of our data, it is more valuable to correctly identify high-risk applications which is why ```RandomOverSample()``` would be preffered in this comparison.

## Undersampling

### Cluster-Centroids

![cm_ClusterCentroids](https://github.com/brand0j/Credit_Risk_Analysis/blob/main/Resources/cm_ClusterCentroids.PNG)
![class_report_ClusterCentroids](https://github.com/brand0j/Credit_Risk_Analysis/blob/main/Resources/class_report_ClusterCentroids.PNG)

**Balanced Accuracy Score**: *0.5442*

```ClusterCentroids()``` is similar to ```SMOTE()``` with how it chooses data points. It identifies clusters of the majority class, then generates synthetic data points (centroids) that are representative of the overall clusters. The majority class is then undersampled down to the size of the minority class. Using this technique we can see a degradation in the model's ability to accurately identify both high-risk & low-risk when compared to our results from ```RandomOverSample()```. It does a significantly worse job at identifying applicants who are low-risk (~40%) and shows in its balanced accuracy score. 

## Combined (Over & Under) Sampling

### SMOTE-ENN
![cm_SMOTEENN](https://github.com/brand0j/Credit_Risk_Analysis/blob/main/Resources/cm_SMOTEENN.PNG)
![class_report_SMOTEENN](https://github.com/brand0j/Credit_Risk_Analysis/blob/main/Resources/class_report_SMOTEENN.PNG)

**Balanced Accuracy Score**: *0.6786*

In this method we use a combination of sampling tactics. This first that is employed is one we have already covered, ```SMOTE()```, which is used to oversample the minority class, while using ENN(Edited Nearest Neighbors) to clean the resulting data. In this undersampling strategy, if the two nearest neighbors of a data poitn belong to two different classes, the data point is dropped altogether.

## Ensemble Classifiers

### Balanced Random Forest Classifier

![cm_BalancedRandomForestClassifier](https://github.com/brand0j/Credit_Risk_Analysis/blob/main/Resources/cm_BalancedRandomForestClassifier.PNG)
![class_report_BalancedRandomForestClassifier](https://github.com/brand0j/Credit_Risk_Analysis/blob/main/Resources/class_report_BalancedRandomForestClassifier.PNG)

**Balanced Accuracy Score**: *0.7878*

### Easy Ensemble Classifier (AdaBoost)

![cm_EasyEnsembleAdaBoostClassifier](https://github.com/brand0j/Credit_Risk_Analysis/blob/main/Resources/cm_EasyEnsembleAdaBoostClassifier.PNG)
![class_report_EasyEnsembleAdaBoostClassifier](https://github.com/brand0j/Credit_Risk_Analysis/blob/main/Resources/class_report_EasyEnsembleAdaBoostClassifier.PNG)

**Balanced Accuracy Score**: *0.9254*
