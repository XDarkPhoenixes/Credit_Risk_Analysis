# Credit_Risk_Analysis

## Overview of the analysis
Employ different techniques to train and evaluate models with unbalanced classes, in this case, credit card's credit risk. RandomOverSampler (Random Oversampling) and SMOTE (Synthetic Minority Oversampling Technique) algorithms were first used to oversample the credit card credit dataset from LendingClub, and then ClusterCentroids (Cluster Centroid Undersampling) algorithm was used to undersample the data. A combinatorial approach of over- and undersampling called SMOTEENN (SMOTE and Edited Nearest Neighbors (ENN)) algorithm was also implemented. Finally two ensemble models BalancedRandomForestClassifier and EasyEnsembleClassifier were used to predict credit risk. The performances of these models were evaluated. 

## Results

- Using Naive Random Oversampling, the balanced accuracy score is 65%, the precision for the high risk is extremely low only at 1%, and the sensitivity at 73%.

![RanOver](https://user-images.githubusercontent.com/84931545/137801542-542848a2-ac41-49e7-bbc6-fe0099f6562d.PNG)


- Using SMOTE oversampling, the balanced accuracy score is 66%, the precision for the high risk is again at 1% with recall at 63%.

![SMOTE](https://user-images.githubusercontent.com/84931545/137801556-c7417c36-abe9-4419-89e9-a859c484f88f.PNG)

- Using the Cluster Centroid Undersampling model, the balanced accuracy score is 54%, with recall at 69% and precision at 1%.

![UnderS](https://user-images.githubusercontent.com/84931545/137801573-89bbbb32-094c-40fe-a585-005ae1c61280.PNG)

- Using the combinatorial approach SMOTEENN, the balanced accuracy score is 62%, the precision for the high risk is also at 1% with sensitivity at 68%. 

![SMOTEENN](https://user-images.githubusercontent.com/84931545/137802049-434a0efa-3dba-4deb-99ab-8e4170776185.PNG)

- Using the Balanced Random Forest Classifier, the balanced accuracy score is 79%, the precision for the high risk is at 3%, and the sensitivity is at 70%.

![BlaEn](https://user-images.githubusercontent.com/84931545/137802068-726b988f-f596-41df-902f-46ba5f3d64f4.PNG)


- Using the Easy Ensemble AdaBoost Classifier, the balanced accuracy score is 93%, the precision for the high risk is at 9%, and the recall is at 92%.

![easyens](https://user-images.githubusercontent.com/84931545/137802110-8e08fdd5-87ae-4050-94c2-7f4c6687e7fa.PNG)



## Summary 
The precision from all 6 models is extremely low for high risk. The undersampling model has the lowest accuracy score while the Easy Ensemble model has the highest accuracy score. Easy Ensemble model also has the highest recall while SMOTE oversampling model has the lowest sensitivity. 

Considering while determining credit risk, it is very important to reduce False Negative which could have dangerous consequences in the future. False positives can be ruled out by future testing to rule out high risks. Therefore sensitivity is more important than precision in this case. Easy Ensemble AdaBoost Classifier model is most recommended here since it has the highest sensitivity with also a high accuracy score of 93%. 

