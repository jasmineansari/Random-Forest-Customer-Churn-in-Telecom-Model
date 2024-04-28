# Random-Forest-Customer-Churn-in-Telecom-Model
Oversaw a meticulous data refinement and outlier remediation process. Crafted an advanced random forest model, meticulously fine tuned through hyperparameter adjustments.

## Overview
The project aims to build a predictive model to identify customers who are likely to churn (cancel their subscription) from a telecom company. The dataset used in this project contains various customer-related features, such as gender, age, contract type, monthly charges, and more.

## Data Preprocessing
1. The dataset is loaded and the target variable "Churn" is extracted into separate variables `y_train` and `y_test`.
2. The remaining features are stored in `x_train` and `x_test` for the training and testing datasets, respectively.

## Model Building
1. A Random Forest Classifier model is created with 50 estimators (decision trees) and a random state of 23.
2. The model is trained on the `x_train` and `y_train` data using the `fit()` method.
3. The trained model is used to make predictions on the `x_test` data, and the predicted values are stored in the `rf_pred` variable.

## Model Evaluation
1. The accuracy score of the Random Forest model is calculated using the `accuracy_score()` function, which compares the predicted values (`rf_pred`) with the actual target values (`y_test`). The accuracy score is 77.75%.
2. A confusion matrix is generated using the `confusion_matrix()` function, which provides a breakdown of the true positive, true negative, false positive, and false negative predictions.
3. The confusion matrix is then visualized using the `sns.heatmap()` function from the Seaborn library.

## Hyperparameter Tuning
1. The code then explores the impact of varying the number of estimators (decision trees) in the Random Forest model.
2. A list of different values for the number of estimators (100 to 700) is defined.
3. The model is trained and evaluated for each value of the number of estimators, and the corresponding accuracy scores are printed.
4. The highest accuracy of 77.82% is achieved with 450 estimators.

## Grid Search Optimization
1. The code then uses the `GridSearchCV` function from the Scikit-learn library to perform further hyperparameter tuning.
2. The grid search is configured to explore different values for the `criterion` (gini or entropy) and `max_depth` (None, 5, or 10) hyperparameters.
3. The grid search is performed using 2-fold cross-validation, and the best hyperparameters are stored in the `best_params_` attribute of the `grid_search` object.

Overall, this Jupyter Notebook demonstrates the process of building a customer churn prediction model using the Random Forest algorithm. It includes data preprocessing, model training, evaluation, and hyperparameter tuning steps to optimize the model's performance. The code provides a solid foundation for understanding the application of machine learning techniques in a telecom customer churn prediction scenario.
