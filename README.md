# Intrusion-Detection-System-using-ML
## Dataset
The dataset used is the KDD Test and Train dataset taken from Kaggle. The reason behind choosing this dataset is it does not include redundant data in the training set, making the classifier more robust, and at the same time, it does not have duplicate records in the testing set.
It contains 42 columns, the last of which is the target column, where 1 defines an attack, and 0 represents no attack.


## Method 
Six models have been implemented, namely 
1. Decision Tree, 
2. Random Forest classifier,
3. Support Vector Machines,
4. Logistic Regression,
5. Gaussian Naive Bayes,
6. Multi-Layer perceptron.
 
The ROC-AUC curve is used to compare models. It illustrates the True Positive rates vs. False Positive rates for the model. The closer the area under the curve is to 1, the better the trained model is. The reference is a no-skill model that predicts only one class all the time and has an area under the curve of 0.5.

## Model Enhancement 
XGBoost has been used to enhance the model. It was chosen because it can handle large datasets and complex relationships. 

## Data Handling
Class imbalance is addressed using SMOTE(Synthetic Minority Oversampling Technique), which generates new data points to balance an imbalanced dataset and increase minority class samples. Instead of generating data points on the line segment connecting the two, SMOTE randomly selects a minority class point and one of its K-nearest neighbors to create a new data point. You can use this code before training other models.
For model evaluation purposes, we also used K-fold cross-validation for a better evaluation.

## Deployment
Built a pipeline for preprocessing and prediction and created a Flask Rest API for deployment.
