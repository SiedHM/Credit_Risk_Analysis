# Challenge 17
Sied H Mohamed

# Overview of the project

This project deals on credit card analysis using a supervised machine learning analysis method using a data from LendingClub, a P2P lending service company to evaluate and predict credit risk. Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. In order to balance out such classifications and improve the accuracy and prediction of the model I used RandomOverSampler, SMOTE, ClusterCentroids, SMOTEENN, BalancedRandomForestClassifier, and EasyEnsembleClassifier. Supervised Machine learning algorithm  is used because the data includes labeled outcome(target) variable.

# Results
## Deliverable 1:  Resampling Models 

###  Unbalanced data
A python library  scikit-learn and imbalanced-learn  are used to resample and evaluate the results. The status of credit risk is represented by “loan status” and  classifies as “low risk” and “ high risk”. Before balancing these two classes, there are about 
-	68470 low risk
-	347 high risk   loan applicants
From this, it can be seen that it is highly unbalanced. About 99.5% of the loan applicants were “low risk” loan applicants.

### Naive Random Oversampling
As its name implies, this method oversamples the high risk(with small sample)  by repeated sampling until it is equal to sample size of the class with higher sample size. With the nave random oversampling method, the distribution of the loan applicants become,
-	51366 low risk
-	51366 high risk   loan applicants
Applying and training logistic regression with the resampled data, it resulted in
-	64.4% balanced accuracy score
-	The imbalanced classification report is
![Ove_sampling ](https://github.com/SiedHM/Credit_Risk_Analysis/blob/main/images/oversampling.png)


###  SMOTE Oversampling
The SMOTE oversampling resulted in the same balanced the classes of loan applicants
-	51366 low risk
-	51366 high risk   loan applicant
The logistic regression results shows some improvement with the SMOTE Oversampling
-	66.3% balanced accuracy score
-	The imbalanced classification report is
![Smote ](https://github.com/SiedHM/Credit_Risk_Analysis/blob/main/images/SMOTE.png)

### Under sampling

In this method, we under sample the class with higher sample size. With this method, the balanced sample size is

-	246 low risk
-	246 high risk   loan applicants

The logistic regression results shown low performance compared to SMOTE and Random Oversampling methods
-	58.9% balanced accuracy score
-	The imbalanced classification report is
![under ](https://github.com/SiedHM/Credit_Risk_Analysis/blob/main/images/under.png)

# Deliverable 2:  SMOTEENN  METHOD

### Combination (Over and Under) Sampling

With the combination of the over and under sampling method,
The resampled sample size , not exactly balanced, but close to each other
-	62011 low risk
-	68460 high risk   loan applicants

The logistic regression results shown lower than the  SMOTE but almost same as Random Oversampling methods and better than under sampling
-	64.5% balanced accuracy score
-	The imbalanced classification report is
![combined ](https://github.com/SiedHM/Credit_Risk_Analysis/blob/main/images/combined.png)

# Deliverable 3: Ensemble Models

### Balanced Random Forest Classifier

Compared to the logistic regression with balanced resampling, the balanced random forest classifier results in better performance.

-	78.8% balanced accuracy score
-	The imbalanced classification report is
![balanced randomF ](https://github.com/SiedHM/Credit_Risk_Analysis/blob/main/images/balanced.png)

#### Importance of feasures
![](https://github.com/SiedHM/Credit_Risk_Analysis/blob/main/images/list%20of%20features.png)

### Easy Ensemble Classifier
Compared to all models, the easy ensemble model results in best preformances in ters of balanced accuracy report
![easy](https://github.com/SiedHM/Credit_Risk_Analysis/blob/main/images/easy.png))

# Conclusion
From the above results, the SMOTE random sampling performs better and the results of the ensemble models are better than logistic regression results.  

 From the above models Easy Ensemble  Classifer model results in with an accuracy rate of 93%, 9% precision,92% sensitivity and16% f1 for the high credit risk.  I recommend banks to use this method to predict credit risk loan applications. 

