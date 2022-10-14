# Credit_Risk_Analysis

## Overview
The purpose of this project is to use supervized machine learning in order to analyze credit risk. Credit risk analysis poses a potential difficulty due to unbalanced classification (as good loans outnumber risky loans). Six models are trained and tested with credit risk information and their performance evaluated. These approaches include RandomOverSampler, SMOTE, ClusterCentroids, SMOTEENN, BalancedRandomForestClassifier and EasyEnsembleClassifier of the Scikit-learn library.  

## Results
These results can also be found in the results folder which includes accuracy scores, confusion matrices, and imbalanced classification reports for all 6 models. 

### Balanced Accuracy Scores 
- The balanced accuracy score for the easy ensemble classifier model was .93.
- The balanced accuracy score for the balanced random forest classifier model was .68.
- The balanced accuracy score for the naive random oversampling model was .66.
- The balanced accuracy score for the SMOTE oversampling model was .66.
- The balanced accuracy score for the cluster centroids undersampling model was .66.
- The balanced accuracy score for the SMOTEENN combination sampling model was .54.

### Precision Scores
- The precision score for the easy ensemble classifier model was .09 for high risk loans and 1 for low risk loans.
- The precision score for the balanced random forest classifier model was .88 for high risk loans and 1 for low risk loans.
- The precision score for the naive random oversampling model was .01 for high risk loans and 1 for low risk loans.
- The precision score for the SMOTE oversampling model was .01 for high risk loans and 1 for low risk loans.
- The precision score for the cluster centroids undersampling model was .01 for high risk loans and 1 for low risk loans.
- The precision score for the SMOTEENN combination sampling model was .01 for high risk loans and 1 for low risk loans. 

### Recall Scores
- The recall score for the easy ensemble classifier model was .92 for high risk loans and .94 for low risk loans. 
- The recall score for the balanced random forest classifier model was .37 for high risk loans and 1 for low risk loans.
- The recall score for the naive random oversampling model was .72 for high risk loans and .6 for low risk loans.
- The recall score for the SMOTE oversampling model was .62 for high risk loans and .69 for low risk loans. 
- The recall score for the cluster centroids undersampling model was .69 for high risk loans, and .4 for low risk loans.
- The recall score for the SMOTEENN combination sampling model was .77 for high risk loans and 1 for low risk loans. 

### Imbalanced Classification Reports
The following imbalanced classification reports support the preceding results, as well as showing the associated F1 scores which describe the balance between precision and recall in each model.

#### Easy Ensemble
<img width="675" alt="easy_ensemble_imbalanced" src="https://user-images.githubusercontent.com/107224097/195918603-f2451607-6b2e-4366-a40b-d181176fe757.PNG">

#### Balanced Random Forest
<img width="675" alt="randomforest_imbalanced" src="https://user-images.githubusercontent.com/107224097/195918719-d3992c70-f0fb-4263-a3fe-e3f327fdd57a.PNG">

#### Naive Random Oversampling
<img width="675" alt="naive_imbalanced" src="https://user-images.githubusercontent.com/107224097/195918678-8323ad5b-3a77-42ef-9e9d-bd16ddd15dbf.PNG">

#### SMOTE Oversampling
<img width="675" alt="smote_imbalanced" src="https://user-images.githubusercontent.com/107224097/195918747-9e78e849-f00c-4124-8452-684de5f7b594.PNG">

#### Cluster Centroids Undersampling
<img width="675" alt="cluster_centroids_imbalanced" src="https://user-images.githubusercontent.com/107224097/195918554-e2f4d1c2-b8d0-4de8-bfb1-f87c98e26d13.PNG">

#### SMOTEENN Combination Sampling
<img width="675" alt="smoteenn_imbalanced" src="https://user-images.githubusercontent.com/107224097/195918773-a51f6422-fc1b-493b-8b66-5ab731a4a361.PNG">

## Summary 
The easy ensemble classifier approach achieved the highest accuracy score, at .92, while the other models did not score higher that .7 accuracy. However, every model besides the balanced random forest achieved a poor score for precision regarding high risk loans. This indicated a high rate of false positives regarding high risk loans. The highest score achieved for precision regarding high risk loans was .88, achieved by the balanced random forest model. Overall, the easy ensemble classifier model was most effective. However, it would not be recommended to solely depend on this model, due to it's poor score for precision regarding high risk loans. A combination of the easy ensemble approach and balanced random forest model (to deal with high risk loans) could improve this, but a low sensitivity score (.37) for the balanced random forest model for high risk loans would indicate that there could be many false negatives.
