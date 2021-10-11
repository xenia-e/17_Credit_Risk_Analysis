# 17_Credit_Risk_Analysis
 apply machine learning  techniques to assess credit card risk

# Purpouse

The pourpose of current project is to employ different techniques to train and evaluate models with unbalanced classes to asses credit card risks.


## Methods

Oversample the data using the *RandomOverSampler* and *SMOTE* algorithms, and undersample the data using the *ClusterCentroids* algorithm. Use a combinatorial approach of over- and undersampling using the *SMOTEENN* algorithm. 

Next, compare two new machine learning models that reduce bias, *BalancedRandomForestClassifier* and *EasyEnsembleClassifier*, to predict credit risk.

## Deliverables

__*Deliverable 1:*__ Use Resampling Models to Predict Credit Risk [credit_risk_resampling.ipynb](https://github.com/xenia-e/17_Credit_Risk_Analysis/blob/main/credit_risk_resampling.ipynb)

__*Deliverable 2:*__  Use the SMOTEENN Algorithm to Predict Credit Risk ([credit_risk_resampling.ipynb](https://github.com/xenia-e/17_Credit_Risk_Analysis/blob/main/credit_risk_resampling.ipynb))

__*Deliverable 3:*__  Use Ensemble Classifiers to Predict Credit Risk ([credit_risk_ensemble.ipynb](https://github.com/xenia-e/17_Credit_Risk_Analysis/blob/main/credit_risk_ensemble.ipynb))

__*Deliverable 4:*__  A Written Report on the Credit Risk Analysis ([README.md](https://github.com/xenia-e/17_Credit_Risk_Analysis/blob/main/README.md))

# Results

- Naive Random Oversampling model: 

The balanced accuracy score equals to 64%.
The high_risk precision is about 1% only with 66% sensitivity which results a F1 Score of 0.02 only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 62% and F1 score of 0.76.

![Naive Random Oversampling results](https://github.com/xenia-e/17_Credit_Risk_Analysis/blob/main/Analysis/naive_random_sampling.png)

>Figure 1 - Naive Random Oversampling results

- SMOTE model

The balanced accuracy score equals to 65%.
The high_risk precision is about 1%  with 61% sensitivity and F1 Score of 0.02 .
Precision for the low_risk population is 100% with recall 69% and F1 Score of 0.81

![SMOTE Oversampling results](https://github.com/xenia-e/17_Credit_Risk_Analysis/blob/main/Analysis/smote_oversampling.png)

>Figure 2 - SMOTE Oversampling Results

- ClusterCentroids resampler model

The balanced accuracy score is 54%.
The high_risk precision is about 1%  with 69% sensitivity and F1 Score of 0.01 .
Precision for the low_risk population is 100%, sensitivity 40%, and F1 Score of 0.57

![Undersampling model Results](https://github.com/xenia-e/17_Credit_Risk_Analysis/blob/main/Analysis/undersampling.png)

>Figure 3 - Undersampling model Results

- Combination (Over and Under) Sampling

The balanced accuracy score is 64%.
The high_risk precision is about 1%  with 72% sensitivity and F1 Score of 0.02 .
Precision for the low_risk population is 100%, sensitivity 578%, and F1 Score of 0.72

![Combination (Over and Under) Sampling Results](https://github.com/xenia-e/17_Credit_Risk_Analysis/blob/main/Analysis/combination.png)

>Figure 4 - Combination (Over and Under) Sampling Results

- Balanced Random Forest Classifier

The balanced accuracy score is 79%.
The high_risk precision is about 3%  with 70% sensitivity and F1 Score of 0.06 .
Precision for the low_risk population is 100%, sensitivity 87%, and F1 Score of 0.93

![Balanced Random Forest Classifier model Results](https://github.com/xenia-e/17_Credit_Risk_Analysis/blob/main/Analysis/brf.png)

>Figure 5 - Balanced Random Forest Classifier model Results

- Easy Ensemble AdaBoost Classifier

The balanced accuracy score is  93.5%.
The high_risk precision is about 10%  with 92% sensitivity and F1 Score of 0.18.
Precision for the low_risk population is 100%, sensitivity 95%, and F1 Score of 0.97

![Easy Ensemble AdaBoost Classifier model Results](https://github.com/xenia-e/17_Credit_Risk_Analysis/blob/main/Analysis/eea.png)

>Figure 6 - Easy Ensemble AdaBoost Classifier model Results


# Summary 

All the models used to perform the credit risk analysis show weak precision in determining high risk loans and are not save to use for this purpose.

Even though the Ensemble models showed more accurate results specially on the sensitivity of the high risk credits the F1 Scores are not high enough to relay on them.

The EasyEnsembleClassifier model shows a recall of 92% so it detects almost all high risk credit. On another hand, with a low precision and F1 Score, there are a lot credits that falsely marked as high risk, which would penalize the bank's credit strategy.

For those reasons I would not recommend the bank to use any of these models to predict credit risk without further improvements.