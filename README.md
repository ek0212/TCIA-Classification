# The Cancer Imgaging Archive Low Grade Glioma vs Glioblastoma Classification

An XGBoost machine learning model was applied for dichotomized classification of glioblastomas versus low grade gliomas. For the development of this model, the “XGBoost” Python package was used. 

Stratified cross-validation was performed to minimize the risk of overfitting the data; a stratified approach ensured cortical lesions are present in the training and testing sets. Using stratified random sampling, 5-fold cross validation was performed, preserving the tumor type percentage in both training and validation samples. Each validation was performed on a random sample of 80% of the data and validated on the remaining 20%. The train set underwent training on 100 different XGBoost hyperparameter configurations before selecting the best fit and validating on the test set. The model was run on a different shuffle of the data 30 times to attain statistical significance. 

A rank of feature importance was performed at each validation, removing highly correlated features for accurate representation of importance. The model accuracy was determined by an average of the ROC area under the curve (AUC) for each validation step. 

The XGBoost model was useful for detecting cortical lesions (AUC of 0.95 ± 0.02). IDH status and 1 voxel imaging volume were the most powerful predictors, findings that are supported in brain tumor literature.
