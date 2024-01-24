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
