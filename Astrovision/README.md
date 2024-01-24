Astrovision

#### 4.1 Introduction
In the pursuit of constructing a machine learning model for a redshift regressor and galaxy classifier, a systematic procedure is outlined through the following modules, each presented in a step-by-step format.

### The Regression Model:

#### 4.2 Library Importation
In this step, we import essential libraries from Python packages, enabling the utilization of functions such as numpy, DecisionTreeRegressor, KFold, pyplot, etc., within the code.

#### 4.3 Dataset Loading and Feature-Target Generation
To train the model, we require a dataset. The Sloan Digital Sky Survey (SDSS) dataset is employed, providing measured flux for each object through optical and infrared filters. Feature targets are generated using magnitudes from five Sloan filters (U, G, R, I, Z) by subtracting magnitudes measured in neighboring filters.

#### 4.4 Implementation of the `median_diff` Function
The `median_diff` function calculates the median residual error of the model, representing the median difference between predicted and actual redshifts. It takes two arguments – the predicted and actual/target values, which will correspond to predicted redshifts from the decision tree and their measured/target values.

#### 4.5 Data Splitting & Decision Tree Model Validation
The dataset undergoes splitting into training and testing sets. The training set is utilized to train the model, while the testing set assesses the model's predictions. The `median_diff` function from the previous step is employed to validate the decision tree model.

#### 4.6 Decision Tree Plotting
The decision tree model is visualized using the `export_graphviz` function. This graphical representation aids in understanding the structure and decision-making processes of the trained model.

### The Classifier Model:

#### 4.8 Library Importation
This task involves importing essential libraries from Python packages to utilize functions such as numpy, DecisionTreeClassifier, confusion_matrix, pyplot, cross_val_predict, and RandomForestClassifier implemented in the code.

#### 4.9 Data Splitting
The dataset is divided into a 70% training dataset and a 30% testing dataset.

#### 4.10 Feature Target Generation
Feature variables are generated, contributing to the model-building process.

#### 4.11 Decision Tree Classifier Training
The classifier is trained using the decision tree algorithm with train features and train targets. Predictions for test features are obtained, providing information about predicted and actual class values.

#### 4.12 Decision Tree Classifier Analysis
A function is created to plot the confusion matrix, offering insights into the classifier's performance on a set of test datasets with known true values. Additionally, an accuracy calculation function is implemented.

#### 4.13 Random Forest Classifier
A function predicting actual values using 10-fold validation and cross_val_predict is introduced. Random forest classifiers are instantiated, and accuracy scores are calculated. The confusion matrix is plotted based on the obtained accuracy score.

#### 4.14 Summary
To construct the model, a robust dataset is derived from five Sloan filters for each galaxy, subsequently split into training and testing datasets. The decision tree algorithm is applied initially, but to address overfitting and optimize the entire dataset, the Random Forest Classifier and 10-fold validation are introduced. This enhances accuracy and mitigates overfitting issues. The model's output is visualized through a confusion matrix, providing a comprehensive assessment of classification performance.
