# Supervised Machine Learning

## Project Overview
Using data from LendingClub, built and evaluated several machine learning models to assess credit risk.  Imlabanced-learn and Scikit-learn libraries are used to resample the models.

## Resources
1. Data:
- LoanStats_2019Q1.csv
- credit_risk_resampling.ipynb
- credit_risk_ensemble.ipynb

2. Software:
- Jupyter
- Python

## Analysis
### Oversampling
1. Naive Random Oversampling
Results:
 - Accuracy score(how correctly it classifies classes): 0.64
 - Confusion Matrix 
      - TP: 67    
      - FP: 6546  
      - FN: 34
      - TN: 10558
 - Precision(focused on low risk) has a low risk of 100% and there is a high risk of 1% for misclassification.
 - Recall(focused on high risk) returned results that high risk is predicted roughly 66% of the time correct.  There is a 62% low risk of misclassification, and is actually high risk.
 
 2. SMOTE Oversampling
 Results:
  - Accuracy score(how correctly it classifies classes): 0.65
  - Confusion Matrix 
      - TP: 62    
      - FP: 5317  
      - FN: 39
      - TN: 11787
  - Precision(focused on low risk) has a low risk of 100% and there is a high risk of 1% for misclassification.
  - Recall(focused on high risk) returned results that high risk is predicted roughly 61% of the time correct.  There is a 69% low risk of misclassification.

### Undersampling and Combination Sampling
1. Undersampling
Results:
 - Accuracy score(how correctly it classifies classes): 0.53
 - Confusion Matrix 
      - TP: 67    
      - FP: 10217  
      - FN: 34
      - TN: 6887
 - Precision(focused on low risk) has a low risk of 100% and there is a high risk of 1% for misclassification.
 - Recall(focused on high risk) returned results that high risk is predicted roughly 66% of the time correct.  There is a 40% low risk of misclassification.

2. Comination Sampling - SMOTEENN
Results:
 - Accuracy score(how correctly it classifies classes): 0.64
 - Confusion Matrix 
      - TP: 73    
      - FP: 7405 
      - FN: 28
      - TN: 9699
 - Precision(focused on low risk) has a low risk of 100% and there is a high risk of 1% for misclassification.
 - Recall(focused on high risk) returned results that high risk is predicted roughly 72% of the time correct.  There is a 57% low risk of misclassification.     

## Recommendation
Based on the four models, SMOTEENN would be the best model to use.  The reason is due to SMOTEEN's high risk percentage of 72% in recall.  It has the highest percentage from all four models and the only one that surpassess 70%, which can be considered acceptable. The low risk in recall is also the second lowest percentage of 57% from the four models.  In my opinion, being able to prevent False Negatives is more important, because that would prevent less risks for bad loans.

## Analysis 2
1. Balanced Random Forest Classifier
Results:
 - Accuracy score(how correctly it classifies classes): 0.79
 - Confusion Matrix 
      - TP: 68  
      - FP: 1749
      - FN: 33
      - TN: 15355
 - Precision(focused on low risk) has a low risk of 100% and there is a high risk of 4% for misclassification.
 - Recall(focused on high risk) returned results that high risk is predicted roughly 67% of the time correct.  There is a 90% low risk of misclassification.  

2. Easy Ensemble AdaBoost Classifier
Results:
 - Accuracy score(how correctly it classifies classes): 0.93
 - Confusion Matrix 
      - TP: 93  
      - FP: 983
      - FN: 8
      - TN: 16121
 - Precision(focused on low risk) has a low risk of 100% and there is a high risk of 9% for misclassification.
 - Recall(focused on high risk) returned results that high risk is predicted roughly 92% of the time correct.  There is a 94% low risk of misclassification.
 
## Recommendation
Based on the two models, Easy Ensemble AdaBoost would be the best model to use.  The reason is due to Easy Ensemble's high risk percentage of 92% in recall compared to Balanced Random Forest's 67%.  The low risk in recall is also 94% compared to Balanced Random Forest's of 90%.  Easy Ensemble results are substantially greater in providing a more accurate analysis of risky loans.
