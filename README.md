# Credit Risk Analysis - Supervised Machine Learning
## Overview
Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we’ll compare two machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Finally, we'll evaluate the performance of these models and make recommendation on whether they should be used to predict credit risk.

## Resources
* Data Source: LoanStats_2019Q1.csv
* Software & Tools: Machine Learning Models, Python, Jupyter Lab 

## Results 

Please note that the results shown below show the balanced accuracy scores, the confusion matrixes, and the imbalanced classification reports of each specific credit risk resampling technique. As a result, we are able to analyze the ways in which each algorithm differs in providing accurate predictions of credit risk for each user in the dataset provided. 

## OverSampling

### Naive Random OverSampling Algorithm
<p align="center">
<img width="666" alt="Screen Shot 2022-03-24 at 3 33 45 PM" src="https://user-images.githubusercontent.com/94571150/160021088-a539ce5e-d0ed-490e-8b08-10e896734022.png">
</p>

* Accuracy score: 65%
* High_risk Precision: 1%
* High_risk Sensitivity: 62%
* F1: 2%
* Low_risk Precision: 100%
* Low_risk Sensitivity: 68%

<br><br>

### SMOTE Algorithm
<p align="center">
  <img width="678" alt="Screen Shot 2022-03-24 at 3 40 47 PM" src="https://user-images.githubusercontent.com/94571150/160021803-7bf64d7b-70e6-416f-b800-b9215f541a36.png">
</p>

* Accuracy score: 64%
* High_risk Precision: 1%
* High_risk Sensitivity: 63%
* F1: 2%
* Low_risk Precision: 100%
* Low_risk Sensitivity: 66%
<br><br>

## UnderSampling

### ClusterCentroids Algorithm
<p align="center">
<img width="670" alt="Screen Shot 2022-03-24 at 3 49 42 PM" src="https://user-images.githubusercontent.com/94571150/160022710-b8619810-c63c-4e1e-a4f1-552c4cbb5f8e.png">
</p>

* Accuracy score: 53%
* High_risk Precision: 1%
* High_risk Sensitivity: 61%
* F1: 1%
* Low_risk Precision: 100%
* Low_risk Sensitivity: 45%

<br><br>

## Combination (Over and Under) Sampling 

### SMOTEENN Algorithm
<p align="center">
 <img width="664" alt="Screen Shot 2022-03-24 at 3 44 17 PM" src="https://user-images.githubusercontent.com/94571150/160022178-e5a13fc5-6fa6-4b02-8bac-2d953c043bc1.png">
</p>

* Accuracy score: 62%
* High_risk Precision: 1%
* High_risk Sensitivity: 68%
* F1: 2%
* Low_risk Precision: 100%
* Low_risk Sensitivity: 57%

<br><br>

## Ensemble Learners

### BalancedRandomForestClassifier Algorithm
<p align="center">
  <img width="673" alt="Screen Shot 2022-03-24 at 3 45 15 PM" src="https://user-images.githubusercontent.com/94571150/160022274-e1ba5b60-c8df-43be-a252-86d9ff42871d.png">
</p>

* Accuracy score: 79%
* High_risk Precision: 4%
* High_risk Sensitivity: 67%
* F1: 7%
* Low_risk Precision: 100%
* Low_risk Sensitivity: 91%

<br><br>

### EasyEnsembleClassifier Algorithm
<p align="center">
<img width="671" alt="Screen Shot 2022-03-24 at 3 46 09 PM" src="https://user-images.githubusercontent.com/94571150/160022373-4cf7cd99-77ad-49d9-a416-f66d73d99d1e.png">
</p>

* Accuracy score: 93%
* High_risk Precision: 7%
* High_risk Sensitivity: 91%
* F1: 14%
* Low_risk Precision: 100%
* Low_risk Sensitivity: 94%

<br><br>

## Summary

Unfortunately, all of the alogrithms used to perform a credit risk analysis did not provide strong precision in determining high credit risk. However, the Ensemble Learns proved to be much stronger in accuracy and sensitivity when predicting high credit risk. The EasyEnsembleClassifier algorithm, more specifically, showed an improvement from previous algorithms with a 93% accuracy score and a 91% high_risk sensitivity score. That being said, similarly to all of the other algorithms, the EasyEnsembleClassifier algorithm still gives a low precision score. As a result, it is possible that user credits who would normally be considered low risk, are being flagged as high risk credits. It is my recommendation that these algorithms be worked on further, because as is, none of the alogrithms are providing accurate predictions of credit risk that are strong enough to implement in LendingClub's business model. 

