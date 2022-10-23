# Neural_Network_Charity_Analysis

## Overview
The goal of this project is to develop a binary classifier that can determine whether applications will be sponsored by a hypothetical firm called "Alphabet Soup" or not. The preprocessing of the data is followed by the creation, training, and evaluation of a neural network model. Last but not least, an effort is made to improve the model by raising accuracy to 75% or greater.

## Results

### Data Preprocessing
The "EIN" and "NAME" columns were removed from the dataset once the file was read into a Pandas DataFrame. There was nothing of value in these identifying columns.

The uncommon categorical variables in columns with more than 10 distinct values, such as the "CLASSIFICATION" and "APPLICATION TYPE" columns, have been binned into a new "other" column. OneHotEncoder is then used to encode a list of categorical variables. A brand-new dataframe is expanded with these encoded variable names. The original features are lost after combining the one-hot encoded features.

"IS SUCCESSFUL" is the variable that this model considers to be its objective; all other variables in the dataframe are thought of as features. The StandardScaler module from Scikit-Learn is used to normalize the numerical variables.

### Compiling, Training, and Evaluating the Model

A deep learning model is created to predict whether a "Alphabet Soup" sponsored organization will be successful based on the characteristics in the dataset after the data has been preprocessed.

The activation function for the first and second hidden layers is Rectified Linear Unit (ReLU). A sigmoid activation function is employed for the output layer. Every five training epochs, a callback stores the model's weights. The model's accuracy and loss values are assessed after training. The model's output is shown in the image below.

Although an accuracy of 72.67% is somewhat high, it is decided to optimize the model to 75% or higher. 

## Summary 
There may be a variety of explanations for why this model was unable to achieve the desired prediction accuracy level of 75%. It could be necessary to modify the amount of neurons in the buried layers. During training, the number of epochs may need to be raised. There might be anomalies or factors in the input data that throw the model off.

In this binary classification job, a Random Forest Classifier may be preferred than a Deep Learning model. Random Forest Classifiers are far easier to set up and can be trained in a matter of seconds, in contrast to Deep Learning models, which need extensive setup and lengthy training. Furthermore, these two models' levels of prediction accuracy would probably be comparable.

For its ease of implementation and applicability to this situation, it is recommended to use a Random Forest Classifier for future development on this project.

None of the optimization attempts in this analysis were able to produce a model with a predictive accuracy level of 75% or higher. The following methods were attempted: 
- Adding an additional hidden layer.
- Adding more neurons to a hidden layer.
- Using different activation functions.
- Decreasing the number of epochs in the training.
