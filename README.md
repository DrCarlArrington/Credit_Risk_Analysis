# Credit_Risk_Analysis
Machine Learning Module 1 Challenge - Dr. Carl Arrington, Jr.

# Summary and Analysis of Results - Resampling: Oversampling, Undersampling, and Combination Sampling Models

**Oversampling** - For this dataset, using oversampling with both the 'Naive Random' and the 'SMOTE' methods did **not produce a model that would be useful** for the prediction of risky loans. 

  According to the classification report generated, Naive Random oversampling resulted in a precision score of 0.01 for high risk loans and a recall score of 0.60 for all high and low risk loans. The low precision score was reflected in the f1 score of 0.02 for high risk loans.

  According to the classification report generated, SMOTE oversampling resulted in a precision score similar to Naive Random oversampling. SMOTE produced a precision score of 0.01 for high risk loans and a recall score of 0.67 for all high and low risk loans. SMOTE also produced an f1 score of 0.02 for high risk loans.

**Undersampling** - For this dataset, using undersampling with Cluster Centroids produced similar results as the Oversampling methods, with a precision score of 0.01 for high risk loans, a recall of 0.43 for both high and low risk loans, and an f1 score of 0.01 for high risk loans.

**Combination Sampling** - For this dataset, using combination sampling with SMOTEENN resulted in a precision score of 0.01 for high risk loans and recall of 0.58 for all high risk and low risk loans, and a f1 score of 0.02 for high risk loans. The overall performance of the model is still poor.

Overall, the Oversampling, Undersampling, and Combination Sampling Models are inadequate at predictions for this dataset and are not recommended. 

# Summary and Analysis of Results - Ensemble Classification Models

**Balanced Random Forest** - Although the instructions recommended using the Balanced Random Forest method, results were unable to be produced due to an 'ValueError: object of too small depth for desired array' error when using the suggested method with 100 estimators and a random state of 1. The researcher even attempted to increase the number of estimators to as many as 1,000,000 as well as a random state of 78 based on documentation, only resulting in lengthy compilation times ( > 10 minutes) and the same 'ValueError: object of too small depth for desired array'. Therefore, in order to still approach the analysis, the researcher used a basic Random Forest Classifier to analyze this dataset. 

**Random Forest** - 
