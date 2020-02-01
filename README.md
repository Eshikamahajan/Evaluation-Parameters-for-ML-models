# Evaluation-Parameters-for-ML-models
Collection of Basic Parameters like accuaracy etc for evaluating the models 

# Model Evaluation

Model evaluation aims to estimate the generalization accuracy of a model on future (unseen/out-of-sample) data. Where we have different techniques to predict the data, its accuracy and other evaluation parameters helps in selecting the best ML Algorithm to be used.

# About Eval_param.py

This code is used for model evaluation that uses "2 class" confusion matrix as a criteria (in classification) and basic parameters like accuracy,rmse etc for the regression problems.




# Installation

You can either use the code file
or
Use the package manager pip to install Eval-param-EM.

```bash
pip install Eval-param-EM
```
# Usage

for using this package,

```bash
import Eval-param-EM as E
```
## Evaluation using Confusion Matrix 

Create an instance of the class 'Classification_Eval_Param' and pass the confusion matrix obtained as its parameter.


You can further access the following function with the help of this instance

|Functi             |Parameter |Description                                                          |
|-------------------|----------|---------------------------------------------------------------------|
|accura             | NONE     |measures the accuracy of the model using confusion matrix            |
|recall             | NONE     |measures the recall of the model using confusion matrix              |
|precision          | NONE     |measures the precision of the model using confusion matrix           |
|F_score            | NONE     |measures the F1_score of the model using confusion matrix            |
|specificity        | NONE     |measures the specificity of the model using confusion matrix         |
|negative_prediction| NONE     |measures the negative prediction of the model using confusion matrix |

To find the accuracy of the confusion matrix , following code snippet will be required.
Let 'cm' be the 'confusion matrix' for evaluation

```bash
classifier=E.Classification_Eval_Param(cm)
classifier.accuracy()
```
You can also store the result in a variable like

```bash
accuracy=classifier.accuracy()
```
Similarly all the other Functions from this class can be accessed.


## Evaluating the Regression Models 

Create an instance of the class 'Regression_Eval_Param' and pass the dataframe as its parameter.


You can further access the following function with the help of this instance

|Function    |Parameter | Description |     
|------------|---------|---------------|
|accuracy    |(actual,predicted)|measures the accuracy of the actual and predicted values passed as a parameter.|
|correlation|NONE|prints the pearson corrleation of dataframe columns|
|r_square    |NONE|measures the coefficient of determination of the dataframe.|
|rmse |(actual,predicted)   |measures the root mean square error between the actual and predicted datacolumns.|
|mse           |(actual,predicted)    |measures the mean square error between the actual and predicted datacolumns.|
|abs_accuarcy|(actual,predicted,perm_error)|measures the absolute accuracy such that if the actual-predicted value lies within the permissible error (perm_error) then it results in 1 else 0.|

# Note
actual and predicted can be either datacolumns or list.
perm_error needs to be an integer.

To find the accuracy of the confusion matrix , following code snippet will be required.
Let 'cm' be the 'confusion matrix' for evaluation

```bash
Regressor=E.Regression_Eval_Param(cm)
Regressor.accuracy(df['actual'],y_predcited)
```
You can also store the result in a variable like

```bash
accuracy=Regressor.accuracy(df['actual'],df['predicted'])
```
Similarly all the other Functions from this class can be accessed.


# Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
Please make sure to update tests as appropriate.


# License
[MIT](https://choosealicense.com/licenses/mit/)
