# Credit Risk Analysis

## Overview of Analysis:
###
As stated in the beginning of Challenge 17, credit risk is an inherently unbalanced classification problem, as good loans easily outnumber bad ones.  The purpose of this analysis is to use machine learning technics of RandomOverSampling, UnderSampling, SMOTE and SMOTEENN algorithms, BalancedRandomForestClassifier, EasyEnsembleClassifier and imbalanced-learn and scikit-learn libraries to build and evaluate models to measure credit risk.

## Results of Analysis:
###
As 
**Credit Risk Resampling:**

**Native Random OverSampling:****
- Balanced accuracy score: 65.01%
- F1 high risk loans: 0.02
- F1 low risk loans:  0.75
![image](https://user-images.githubusercontent.com/86161212/138574845-fb4c3658-15eb-494d-86cf-c44a3093bb8d.png)
**SMOTE OverSampling:**
- Balanced accuracy score: 66.23%
- F1 high risk loans: 0.02
- F1 low risk loans:  0.82
![image](https://user-images.githubusercontent.com/86161212/138574973-4c07f7c5-f6ae-4038-b7bb-e8b504c08acd.png)
**UnderSampling using ClusterCentroids resampler:**
- Balanced accuarcy score: 54.43%
- F1 high risk loans: 0.01
- F1 low risk loans:  0.57
![image](https://user-images.githubusercontent.com/86161212/138574993-0adc2716-3183-452d-83b3-055c6ba35c31.png)
**Combination (Over and Under) Sampling (SMOTEENN):**
- Balanced accuracy rate: 65.14%
- F1 high risk loans: 0.02
- F1 low risk loans:  0.73
![image](https://user-images.githubusercontent.com/86161212/138575018-a787c61b-4475-4c88-8e37-d5cfacb1cf7c.png)
**Balanced Random Forest Classifier:**
- Balanced accuracy rate: 78.85%
- F1 high risk loans: 0.06
- F1 low risk loans:  0.93
![image](https://user-images.githubusercontent.com/86161212/138575039-7d2c6a6d-8e06-4304-8b83-7063777b4032.png)
**Easy Ensemble AdaBoost Classifier:**
- Balanced accuracy score: 91.55%
- F1 high risk loans: 0.10
- F1 low risk loans:  0.95
![image](https://user-images.githubusercontent.com/86161212/138575090-631ceb53-07e1-4669-949b-d81a1d2d88a6.png)

## Summary of Analysis:
###
Of all the machine learning methods applied to the data, the Easy Ensemble AdaBoost Classifier had the highest balanced accuracy rate of 91.55%, 
