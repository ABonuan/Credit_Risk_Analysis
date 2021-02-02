# Credit_Risk_Analysis

## Overview of the Analysis
The purpose of this analysis is to use different techniques and create, train & evaluate different models to predict credit risk.

## Results
**Oversampling using RandomOverSampler**
- Balanced Accuracy Score: 0.626
- Precision Score
    - High Risk: 0.01
    - Low Risk: 1.00
- Recall Score
    - High Risk: 0.59
    - Low Risk: 0.67\
![alt text](https://github.com/ABonuan/Credit_Risk_Analysis/blob/main/Resources/Random_Oversampling_rep.png?raw=True)

**Oversampling using SMOTE**
- Balanced Accuracy Score: 0.630
- Precision Score
    - High Risk: 0.01
    - Low Risk: 1.00
- Recall Score
    - High Risk: 0.62
    - Low Risk: 0.64\
![alt text](https://github.com/ABonuan/Credit_Risk_Analysis/blob/main/Resources/SMOTE_Oversampling_rep.png?raw=True)

**Undersampling using ClusterCentroids**
- Balanced Accuracy Score: 0.523
- Precision Score
    - High Risk: 0.01
    - Low Risk: 1.00
- Recall Score
    - High Risk: 0.64
    - Low Risk: 0.40\
![alt text](https://github.com/ABonuan/Credit_Risk_Analysis/blob/main/Resources/ClusterCentroids_Undersampling_rep.png?raw=True)

**Combination of Over\- and Undersampling using SMOTEENN**
- Balanced Accuracy Score: 0.622
- Precision Score
    - High Risk: 0.01
    - Low Risk: 1.00
- Recall Score
    - High Risk: 0.71
    - Low Risk: 0.53\
![alt text](https://github.com/ABonuan/Credit_Risk_Analysis/blob/main/Resources/SMOTEEN_Combo_rep.png?raw=True)

**Ensemble Learning using BalancedRandomForestClassifier**
- Balanced Accuracy Score: 0.788
- Precision Score
    - High Risk: 0.04
    - Low Risk: 1.00
- Recall Score
    - High Risk: 0.67
    - Low Risk: 0.91\
![alt text](https://github.com/ABonuan/Credit_Risk_Analysis/blob/main/Resources/Ensemble_BalancedRandomForestClassifier_rep.png?raw=True)

**Ensemble Learning using EasyEnsembleClassifier**
- Balanced Accuracy Score: 0.925
- Precision Score
    - High Risk: 0.07
    - Low Risk: 1.00
- Recall Score
    - High Risk: 0.91
    - Low Risk: 0.94\
![alt text](https://github.com/ABonuan/Credit_Risk_Analysis/blob/main/Resources/Ensemble_EasyEnsembleClassifier_rep.png?raw=True)

## Summary
The oversampling models achieved about a 60% accuracy score, the undersampling model achieved only about 50%, and a combination of over- & undersampling achieved 60%.  Ensemble learning models scored higher in accuracy with the BalancedRandomClassifier at about 80% and the EasyEnsembleClassifier at a high 90%.  The EasyEnsembleClassifier model has the highest percentage in which it predicts outcomes correctly from the test dataset.

Every model recognized low risk loans pretty well with a perfect precision score of 1.0, but missed the target with high risk loans with precision scores ranging from 0.01 to 0.07.

Only the EasyEnsembleClassifier scored high on sensitivity\/recall.  Of the total number of actual high risk loans, this model confirmed those applications as high risk 90% of the time.  All other models only confirm high risk applications at 60% or 70%.

I would recommend using the EasyEnsembleClassifier model to predict credit risk.  Although the precision score is low, meaning there may be many false positives, the sensitivity scores high.  Having a high recall score tells us that the model confirms actual high risk application at a high rate.