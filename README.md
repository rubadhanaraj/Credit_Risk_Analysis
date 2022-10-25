# Credit_Risk_Analysis
## Overview of the analysis
The purpose of this project is to analyze large amounts of data using Python to build and evaluate several machine learning models to predict credit risk. Being able to predict credit risk with machine learning algorithms can help banks and financial institutions predict anomalies, reduce risk cases, monitor portfolios, and provide recommendations on what to do in cases of fraud. The main objectives of this project were to
* Explain how a machine learning algorithm is used in data analytics.
* Create training and test groups from a given data set.
* Implement the logistic regression, decision tree, random forest, and support vector machine algorithms.
* Interpret the results of the logistic regression, decision tree, random forest, and support vector machine algorithms.
* Compare the advantages and disadvantages of each supervised learning algorithm.
* Determine which supervised learning algorithm is best used for a given data set or scenario.
* Use ensemble and resampling techniques to improve model performance.

Using the credit card credit dataset from LendingClub, oversample and undersample machine learning techniques have been incorporated using the RandomOverSampler,SMOTE algorithms and ClusterCentroids algorithm. Then, a combinatorial approach of over- and undersampling using the SMOTEENN algorithm was used.BalancedRandomForestClassifier and EasyEnsembleClassifier were compared that reduce bias, to predict credit risk.

## Results
The Lending Club dataset has been loaded into pandas dataframe and null values has been dropped. Interest rate was converted into numerical. Features and targets were created. TRain,test,split model was imported and the dataset has been splitted into X_train, X_test, y_train, y_test. The balanced accuracy score, confusion matrix and imbalanced classification report were created for six machine learning models.

### RandomOversampler

![Randam_oversampler](https://user-images.githubusercontent.com/108298416/197601059-ff92970c-00b7-4868-b81c-562a66612af4.PNG)

* The balance accuracy score for RandomOversampler model is 64%
* The precision and recall values for high risk applications are 1% and 60% respectively.
* The precision and recall values for low risk applications are 100% and 68% respectively, as the number of the low_risk applications were higher.

### SMOTE 

![SMOTE](https://user-images.githubusercontent.com/108298416/197677812-5c8dfa52-6f83-4ec6-acdb-f351ddbaaf3d.PNG)

* The balance accuracy score for SMOTE  model is 64% as same as RandomOverSampler machine learning model
* The precision and recall values for high and low risk applications were also as same as RandomOverSampler machine leraning model

### ClusterCentroids

![ClusterCentroids ](https://user-images.githubusercontent.com/108298416/197678151-e78d5294-28f3-4bd3-90d2-ec00015f5360.PNG)

* The balance accuracy score for ClusterCentroids model is 53%
* The precision and recall values for high risk applications are 1% and 61% respectively
* The precision and recall values for low risk applications are 100% and 45% respectively

### SMOTEENN

![SMOTEENN](https://user-images.githubusercontent.com/108298416/197678416-939c5ce1-be68-461d-b408-91d09bcf047c.PNG)

* The balance accuracy score for SMOTEENN model is 64%
* The precision and recall values for high risk applications are 1% and 70% respectively
* The precision and recall values for low risk applications are 100% and 57% respectively

### Balanced_Random_Forest_Classifier

![BalancedRandomForestClassifier](https://user-images.githubusercontent.com/108298416/197678749-b845257e-617f-4381-8168-01f7f27af133.PNG)

* The balance accuracy score for Balanced_Random_Forest_Classifier model is 79%
* The precision and recall values for high risk applications are 4% and 67% respectively
* The precision and recall values for low risk applications are 100% and 91% respectively

### Easy_Ensemble_AdaBoost_Classifier

![EasyEnsembleAdaBoostClassifier](https://user-images.githubusercontent.com/108298416/197679037-3d9465d1-f655-42f2-b7e9-21eb3585b866.PNG)

* The balance accuracy score for Easy_Ensemble_AdaBoost_Classifier model is 92%
* The precision and recall values for high risk applications are 7% and 90% respectively
* The precision and recall values for low risk applications are 100% and 94% respectively

## Summary
* All the six machine learning models used to perform credit risk analysis shows almost same precision values while determining whether the credit risk is high and the precision values were weak. 
* The Easy Ensemble Adaboost clasiifier yields the better results than other machine learning models with the balanced accuracy rate of 92%. The precision value when predicting high risk is 7%. As far as the sensitivity(recall) values are concerned, Easy Ensemble Adaboost Classifier model shows a decent improvement 90% in determining high risk and the sensitivity results when predicting low risk was also the highest with the sensitivity rate at 94%.
* If a model is to be recommended to perform the credit risk analysis, Easy Ensemble Adaboost Classifier model would be helpful in analysing credit risk
* However, with the low precision rate results from all the machine learning models, low risk applications would be falsely predicted as high risk, which would affect bank's credit approval process and it's customers. Thus, None of this machine learning models can be recommended.
