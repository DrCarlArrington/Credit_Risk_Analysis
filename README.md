# Module 01 Challenge - Credit Risk Analysis
Researcher: Dr. Carl Arrington, Jr.

# Overview

During this module, the reseacher (re)developed skills in data preparation, statistical reasoning, and machine learning. In the following submission, the researcher applied machine learning to solve a real-world challenge: credit card risk.

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, the researcher needed to employ different techniques of Machine Learning to train and evaluate models with unbalanced classes. The researcher was asked to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, the researcher oversampled the data using the RandomOverSampler and SMOTE algorithms, and undersampled the data using the ClusterCentroids algorithm. Then the researcher used combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Finally the researcher compared two new machine learning models that reduced bias, BalancedRandomForestClassifier (attempted then used a regular RandomForestClassifier) and EasyEnsembleClassifier, to predict credit risk. 

# Summary and Analysis of Results - Resampling: Oversampling, Undersampling, and Combination Sampling Models

**Oversampling** - For this dataset, using oversampling with both the 'Naive Random' and the 'SMOTE' methods did **not produce a model that would be useful** for the prediction of risky loans. 

  According to the classification report generated, Naive Random oversampling resulted in a precision score of 0.01 for high risk loans and a recall score of 0.60 for all high and low risk loans. The low precision score was reflected in the f1 score of 0.02 for high risk loans.

  According to the classification report generated, SMOTE oversampling resulted in a precision score similar to Naive Random oversampling. SMOTE produced a precision score of 0.01 for high risk loans and a recall score of 0.67 for all high and low risk loans. SMOTE also produced an f1 score of 0.02 for high risk loans.

**Undersampling** - For this dataset, using undersampling with Cluster Centroids produced similar results as the Oversampling methods, with a precision score of 0.01 for high risk loans, a recall of 0.43 for both high and low risk loans, and an f1 score of 0.01 for high risk loans.

**Combination Sampling** - For this dataset, using combination sampling with SMOTEENN resulted in a precision score of 0.01 for high risk loans and recall of 0.58 for all high risk and low risk loans, and a f1 score of 0.02 for high risk loans. The overall performance of the model is still poor.

Overall, the Oversampling, Undersampling, and Combination Sampling Models are inadequate at predictions for this dataset and are not recommended. 

# Summary and Analysis of Results - Ensemble Classification Models

**Balanced Random Forest** - Although the instructions recommended using the Balanced Random Forest method, results were unable to be produced due to an 'ValueError: object of too small depth for desired array' error when using the suggested method with 100 estimators and a random state of 1. The researcher even attempted to increase the number of estimators to as many as 1,000,000 as well as a random state of 78 based on documentation, only resulting in lengthy compilation times ( > 10 minutes) and the same 'ValueError: object of too small depth for desired array'. Therefore, in order to still approach the analysis, the researcher used a basic Random Forest Classifier to analyze this dataset. 

**Random Forest** - Upon using the Random Forest classifier, the precision for high risk loans was 0.88 and 1.00 for low risk loans. The recall, was 0.37 for high risk loans, meaning that it only found 37% of the bad loan applications. The F1 score for high risk loans was the highes of all of the models at 0.52, but that value may not be the best representation of the dataset, as the Random Forest was not balanced. If functional, a Balanced Random Forest model may have lent some diversity of data to learn and not focus on a portion of the majority class which was the Low Risk data.

**Easy Ensemble With AdaBoost** - There were different, yet more expected results from using the random forest classifier with AdaBoost. The Easy Ensemble with AdaBoost still suffered from inadequate predictive power. Its precision score was 0.09 and its recall was 0.92 for high risk loans. The F1 score, scored low at 0.16 for predicting high risk loans.

Overall, the Ensemble Classification Models are inadequate at predictions for this dataset and are not recommended. 

