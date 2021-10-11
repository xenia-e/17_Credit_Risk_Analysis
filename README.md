# 17_Credit_Risk_Analysis

# Purpouse

The purpose of the current project is to employ different techniques to train and evaluate models with unbalanced classes to assess credit card risks.


## Methods

Oversample the data using the *RandomOverSampler* and *SMOTE* algorithms, and undersample the data using the *ClusterCentroids* algorithm. Use a combinatorial approach of over- and undersampling using the *SMOTEENN* algorithm. 

Next, compare two new machine learning models that reduce bias, *BalancedRandomForestClassifier* and *EasyEnsembleClassifier*, to predict credit risk.

## Deliverables

__*Deliverable 1:*__ Use Resampling Models to Predict Credit Risk [credit_risk_resampling.ipynb](https://github.com/xenia-e/17_Credit_Risk_Analysis/blob/main/credit_risk_resampling.ipynb)

__*Deliverable 2:*__ Use the SMOTEENN Algorithm to Predict Credit Risk ([credit_risk_resampling.ipynb](https://github.com/xenia-e/17_Credit_Risk_Analysis/blob/main/credit_risk_resampling.ipynb))

__*Deliverable 3:*__ Use Ensemble Classifiers to Predict Credit Risk ([credit_risk_ensemble.ipynb](https://github.com/xenia-e/17_Credit_Risk_Analysis/blob/main/credit_risk_ensemble.ipynb))

__*Deliverable 4:*__ A Written Report on the Credit Risk Analysis ([README.md](https://github.com/xenia-e/17_Credit_Risk_Analysis/blob/main/README.md))

# Results

### Naive Random Oversampling model: 

The balanced accuracy score equals 64%.
The high_risk precision is about 1% only with 66% sensitivity which results in an F1 Score of 0.02.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 62% and an F1 Score of 0.76.

![Naive Random Oversampling results](https://github.com/xenia-e/17_Credit_Risk_Analysis/blob/main/Analysis/naive_random_sampling.png)

>Figure 1 - Naive Random Oversampling results


### SMOTE model

The balanced accuracy score equals 65%.
The high_risk precision is about 1% with 61% sensitivity and an F1 Score of 0.02.
Precision for the low_risk population is 100% with recall 69% and an F1 Score of 0.81

![SMOTE Oversampling results](https://github.com/xenia-e/17_Credit_Risk_Analysis/blob/main/Analysis/smote_oversampling.png)

>Figure 2 - SMOTE Oversampling Results


### ClusterCentroids resampler model

The balanced accuracy score is 54%.
The high_risk precision is about 1% with 69% sensitivity and an F1 Score of 0.01.
Precision for the low_risk population is 100%, sensitivity 40%, and F1 Score of 0.57

![Undersampling model Results](https://github.com/xenia-e/17_Credit_Risk_Analysis/blob/main/Analysis/undersampling.png)

>Figure 3 - Undersampling model Results


### Combination (Over and Under) Sampling

The balanced accuracy score is 64%.
The high_risk precision is about 1% with 72% sensitivity and an F1 Score of 0.02.
Precision for the low_risk population is 100%, sensitivity 578%, and F1 Score of 0.72

![Combination (Over and Under) Sampling Results](https://github.com/xenia-e/17_Credit_Risk_Analysis/blob/main/Analysis/combination.png)

>Figure 4 - Combination (Over and Under) Sampling Results


### Balanced Random Forest Classifier

The balanced accuracy score is 79%.
The high_risk precision is about 3% with 70% sensitivity and an F1 Score of 0.06.
Precision for the low_risk population is 100%, sensitivity 87%, and F1 Score of 0.93

![Balanced Random Forest Classifier model Results](https://github.com/xenia-e/17_Credit_Risk_Analysis/blob/main/Analysis/brf.png)

>Figure 5 - Balanced Random Forest Classifier model Results


### Easy Ensemble AdaBoost Classifier

The balanced accuracy score is 93.5%.
The high_risk precision is about 10% with 92% sensitivity and an F1 Score of 0.18.
Precision for the low_risk population is 100%, sensitivity 95%, and F1 Score of 0.97

![Easy Ensemble AdaBoost Classifier model Results](https://github.com/xenia-e/17_Credit_Risk_Analysis/blob/main/Analysis/eea.png)

>Figure 6 - Easy Ensemble AdaBoost Classifier model Results


# Summary 

The precision for the bad loan applications is low in all used models, indicating a large number of false positives, which indicates an unreliable positive classification. So they are not safe to use for the purpose of detecting high-risk loans. The recall is also low for the high-risk loan applications, which is indicative of a large number of false negatives.

Even though the Ensemble models showed more accurate results specially on the sensitivity of the high-risk credits the F1 Scores are not high enough to rely on them.

The EasyEnsembleClassifier model shows a recall of 92% so it detects almost all high-risk credit. On another hand, with low precision and F1 Score, there are a lot of credits that are falsely marked as high-risk, which would penalize the bank's credit strategy.

In summary, all models are not good at classifying fraudulent loan applications. I would not recommend the bank to use any of these models to predict credit risk without further improvements. 
