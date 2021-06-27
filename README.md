# Credit_Risk_Analysis

<p align="center">
  <img src="images/Loan-Free-PNG-Image.png" width="300">
  <br/><br/>
  <a href="#">Resampling Models to Predict Credit Risk</a>
</p>



## Table of Contents
* [Overview](https://github.com/rkaysen63/Credit_Risk_Analysis/blob/master/README.md#overview)
* [Resources](https://github.com/rkaysen63/Credit_Risk_Analysis/blob/master/README.md#resources)
* [Results](https://github.com/rkaysen63/Credit_Risk_Analysis/blob/master/README.md#results)
* [Summary](https://github.com/rkaysen63/Credit_Risk_Analysis/blob/master/README.md#summary)

## Resources:    
* Data: 
  *  LendingClub data:  LoanStats_2019Q1.csv
* Tools: 
  * Python (Libraries: pandas, matplotlib, imblearn, sklearn)
  * Jupyter Notebook
* "Loan Approved" image is courtesy of: http://www.pngall.com/wp-content/uploads/2017/11/Loan-Free-PNG-Image.png
* Lesson Plan: UTA-VIRT-DATA-PT-02-2021-U-B-TTH, Module 17 Challenge

## Overview:
The purpose of this analysis is evaluate five supervised learning models for their ability to predict high risk loans.  The models will be trained using an unbalanced dataset from LendingClub lending services. (The ratio of low risk loans to high risk loans in the dataset used for this analysis is nearly 200:1.)

## Results:

  <h3>Resampling Models to Predict Credit Risk</h3>
<p align="center">
  <img src="images/metrics_random_oversampling.png" width="700">
  <a href="#">*****************************************************************************************************************************************</a>
  <br/><br/> 
  <img src="images/metrics_SMOTE.png" width="700">
  <a href="#">*****************************************************************************************************************************************</a>
  <br/><br/> 
  <img src="images/metrics_ClusterCentroids_Und_Smpl.png" width="700">
  <a href="#">*****************************************************************************************************************************************</a>
  <br/><br/> 
  <img src="images/metrics_SMOTEENN.png" width="700">
  <a href="#">*****************************************************************************************************************************************</a>
  <br/><br/> 
  <img src="images/metrics_BalancedRFC.png" width="700">
  <a href="#">*****************************************************************************************************************************************</a>
  <br/><br/> 
  <img src="images/metrics_EasyEnsemble.png" width="700">
</p>

## Summary:
  * There is a summary of the results (2 pt)
  * There is a recommendation on which model to use, or there is no recommendation with a justification (3 pt)
The data used to train the models:
* low-risk:  68,470
* high-risk: 347

The confusion matrix below explains how to interpret the six confusion matrices shown in the results above.
 * TP is the number of customers that the model correctly predicts to default.  
 * FP is the number of customers that the model predicts will default but they did not.
 * FN is the number of customers that default but the model predicts that they do not default.
 * TN is the number of customers that do not default and the model correctly predicts that they do not default.

CONFUSION MATRIX | HIGH RISK PREDICTED TRUE | HIGH RISK PREDICTED FALSE |
-----------------|----------------|-----------------|
HIGH RISK ACTUAL TRUE | TP | FN |
HIGH RISK ACTUAL FALSE | FP | TN |

* Precision<br/><br/> 
Precision is a ratio of true positive predictions to total positive predictions.   As precision approaches 1.00, false positives diminish. <br/><br/> 
`TP/(TP + FP) = 375/(375 +0) = 1.00`<br/><br/> 
<br/><br/> 
* Recall (AKA Sensitivity)<br/><br/> 
`TP/(TP + FN) = 375(375 + 0) = 1.00`<br/><br/> 
Sensitivity is a ratio true positive predictions to total actual values.  As sensitivity approaches 1.00, false negatives diminish.<br/><br/> 
<br/><br/> 

MODEL | BALANCED ACCURACY | HIGH RISK PRECISION | HIGH RISK RECALL |
--------------------|--------------------|--------------------|--------------------|
Formula | (TP + TN)/(TP + FP + TN + FN) | TP/(TP + FP) | TP/(TP + FN) | 
RandomOverSampler | 0.65 | 0.01 | 0.69 | 
SMOTE | 0.66 | 0.01 | 0.63 | 
ClusterCentroids | 0.54 | 0.01 | 0.69 |
SMOTEENN | 0.66 | 0.01 | 0.75 |  
BalancedRandomForestClassifier | 0.79 | 0.03 | 0.70   |
EasyEnsembleClassifier |0.93 | 0.09 | 0.92|
<p/>
<br/><br/> 




[Back to the Table of Contents](https://github.com/rkaysen63/Credit_Risk_Analysis/blob/master/README.md#table-of-contents)
