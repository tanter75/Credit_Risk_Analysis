# Credit Risk Analysis

## Overview of Analysis:
###
As stated in the beginning of Challenge 17, credit risk is an inherently unbalanced classification problem, as good loans easily outnumber bad ones.  The purpose of this analysis is to use machine learning technics of RandomOverSampling, UnderSampling, SMOTE and SMOTEENN algorithms, BalancedRandomForestClassifier, EasyEnsembleClassifier and imbalanced-learn and scikit-learn libraries to build and evaluate models to measure credit risk for credit card application.s

## Results of Analysis:
###

**Credit Risk Resampling:**

**Native Random OverSampling:****
- Balanced accuracy score: 0.6502
- High risk loans: Precision: 0.01  Recall: 0.69
- Low risk loans:  Precision: 1.00  Recall: 0.61
- Average precision: 0.99  Recall:  0.61
![image](https://user-images.githubusercontent.com/86161212/138574845-fb4c3658-15eb-494d-86cf-c44a3093bb8d.png)

**SMOTE OverSampling:**
- Balanced accuracy score: 0.6623
- High risk loans: Precision: 0.01  Recall: 0.63
- Low risk loans:  Precision: 1.00  Recall: 0.69
- Average precision: 0.99  Recall:  0.69
![image](https://user-images.githubusercontent.com/86161212/138574973-4c07f7c5-f6ae-4038-b7bb-e8b504c08acd.png)

**UnderSampling using ClusterCentroids resampler:**
- Balanced accuarcy score: 0.5443
- High risk loans: Precision: 0.01  Recall: 0.69
- Low risk loans:  Precision: 1.00  Recall: 0.40
- Average precision: 0.99  Recall:  0.40
![image](https://user-images.githubusercontent.com/86161212/138574993-0adc2716-3183-452d-83b3-055c6ba35c31.png)

**Combination (Over and Under) Sampling (SMOTEENN):**
- Balanced accuracy rate: 0.6514
- High risk loans: Precision: 0.01  Recall: 0.72
- Low risk loans:  Precision: 1.00  Recall: 0.58
- Average precision: 0.99  Recall:  0.58
![image](https://user-images.githubusercontent.com/86161212/138575018-a787c61b-4475-4c88-8e37-d5cfacb1cf7c.png)

**Balanced Random Forest Classifier:**
- Balanced accuracy rate: 0.7885
- High risk loans: Precision: 0.03  Recall: 0.70
- Low risk loans:  Precision: 1.00  Recall: 0.87
- Average precision: 0.99  Recall:  0.87
![image](https://user-images.githubusercontent.com/86161212/138575039-7d2c6a6d-8e06-4304-8b83-7063777b4032.png)

**Easy Ensemble AdaBoost Classifier:**
- Balanced accuracy score: 0.9155
- High risk loans: Precision: 0.05  Recall: 0.93
- Low risk loans:  Precision: 1.00  Recall: 0.90
- Average precision: 0.99  Recall:  0.90
![image](https://user-images.githubusercontent.com/86161212/138575090-631ceb53-07e1-4669-949b-d81a1d2d88a6.png)

## Summary of Analysis:
###
Of all the machine learning methods applied to the data, the Easy Ensemble AdaBoost Classifier performed best with 0.9155 balanced accuracy score, 0.05 precision, 0.93 score for precision, 0.10 f1 score for high risk loans.  For low risk loans the results were 1.00 score for precision, 0.90 for recall and f1 score of 0.95.  
All 6 of the models performed sub-optimally with regards to precision of high risk loans, however a marked improvement in recall was present when the Easy Ensemble AdaBoost Classifier was used (0.93).  Here are the recommendations for using machine learning to assess credit card application risk based pn analysis:
1) If one of the 6 machine learning models tested needs to be implemented, it is recommended that the Easy Ensemble AddaBoost Classifier be used with several stipulations:
    i)  Recommendations for low risk applications may be followed, however high risk applications should have a secondary manual adjudication completed due to the poor precision         rate, which would otherwise result in many false declines which could result in a loss of profit, consumer confidence and company reputation
2) The machine learning protocols be re-run and consider better credit decisioning factors such as total debt service ratio, revolving credit utilization ("all_util") and client's repayment history ('Late (31-120 days)'), ('Late (16-30 days)') which are better indications of the client's ability and likelihood to repay borrowed funds.
It should be noted that the second recommendation is the preferred method and factors should be retested until results can be found that produce an acceptable threshold of precision, recall and balance accuracy for both low and high risk applications.
