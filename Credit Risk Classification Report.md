# Credit risk classification 

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.  
The purpose of this analysis was to use a dataset of historical lending activity from a peer-to-peer lending service company and build a model that can identify the creditworthiness of borrowers by predicting if they are healthy loan or a high-risk loans.


* Explain what financial information the data was on, and what you needed to predict.

The model was built using a dataset of `77,536` observations of historical lending data with the following variables: 
  
* 1   loan_size          
* 2   interest_rate       
* 3   borrower_income     
* 4   debt_to_income      
* 5   num_of_accounts     
* 6   derogatory_marks      
* 7   total_debt           
* 8   loan_status 

Variable 1 - 7 were our independent variables in the model.
Variable 8: "loan_status" was our dependent variable in the model - with classification of (0)healthy Loan or (1)High-Risk loan. 
We were required to use the information of the data to build a model and predict whether a customer was (0) or (1) in this context.
   
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).

In the provided data there were `77,536` with `2,500 observations / 3.22%` as High Risk and the remaining `75,036 observationsor 76.78%` as Healthy.
Therefore it is noted that the model may include some form of class imbalance- as there a many more instances of class (0) than class (1).

* Describe the stages of the machine learning process you went through as part of this analysis.

The stages of machine learning for logistic regression typically involve the following steps:

1. Data Collection: Gather the relevant data for your problem domain. This may involve acquiring data from various sources, such as databases, APIs, or manual data entry.

2. Data Preprocessing: Clean and preprocess the collected data to ensure its quality and compatibility with the logistic regression model. This step may involve handling missing values, removing duplicates, transforming variables, and normalizing or standardizing the data.

3. Data Partitioning: Split the preprocessed data into two or three subsets: a training set, a validation set (optional), and a test set. The training set is used to train the logistic regression model, the validation set is used for model selection or hyperparameter tuning, and the test set is used to evaluate the final model's performance.

4. Model Training: Feed the training data into the logistic regression algorithm to estimate the model's coefficients or weights. The algorithm adjusts these weights iteratively to minimize the difference between predicted probabilities and actual outcomes in the training set.

5. Model Evaluation: Assess the performance of the trained model using evaluation metrics such as accuracy, precision, recall, F1 score, or area under the ROC curve (AUC-ROC). This evaluation is typically done on the validation set, and the model's hyperparameters can be tuned based on these results.

6. Model Optimization: Fine-tune the logistic regression model by adjusting its hyperparameters, such as learning rate, regularization strength, or convergence criteria. This step aims to improve the model's performance by finding the optimal configuration of these parameters.

7. Model Testing: Once the model is trained and optimized, evaluate its performance on the independent test set. This step provides an unbiased assessment of the model's ability to generalize to unseen data. The test set results can guide decisions regarding the model's deployment and its effectiveness for making predictions on new instances.

8. Deployment: Deploy the logistic regression model into a production environment, where it can be used to predict outcomes for new data instances. This may involve integrating the model into an application, system, or workflow, depending on the specific use case.

9. Monitoring and Maintenance: Continuously monitor the performance of the deployed logistic regression model in the real-world setting. Retrain or update the model periodically to ensure its accuracy and relevance as new data becomes available or as the problem domain evolves.

These stages provide a general framework for applying logistic regression in a machine learning context. However, the exact steps and their order may vary depending on the specific problem, dataset, and requirements of the application.



* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

Logisitic regression was used for predicting the binary outcomes (0 - 1). This type of model calculates the probabliity of a positiv outcome based on a linear combination of independent variables.  
By applying this function, the linear combination is transformed into a range between 0 and 1 representing the probabiolity.   
The model estimates the coefficients that maximise thelikliehood of observed outcomes in the training data. Predictions are made by comparing the probability to a threshold (usually 0.5).

## Results

Based on the provided information, here's a summary analysis:

1. Dataset Information:
   - The dataset contains 77,536 entries and 8 columns.
   - The columns represent features such as loan_size, interest_rate, borrower_income, debt_to_income, num_of_accounts, derogatory_marks, total_debt, and loan_status.
   - The dataset has a mix of float and integer data types.

2. Logistic Regression Model:
   - The logistic regression model has been trained and tested on the given dataset.
   - The model achieved a high accuracy score of 99.24% on the testing data.
   - The model's performance on the training data is also impressive, with an accuracy score of 99.15%.
   - The model's predictions were compared with the actual values for both the training and testing data.

3. Confusion Matrix (Test):
   - The confusion matrix for the testing data is presented as a 2x2 array.
   - True negatives (TN) are 18,679, false negatives (FN) are 80, false positives (FP) are 67, and true positives (TP) are 558.

4. Class Report (Test):
   - The class report provides precision, recall, and f1-score for each class (0 and 1) in the testing data.
   - Class 0 (healthy) has a precision of 99.64%, recall of 99.57%, and f1-score of 99.61%.
   - Class 1 (high risk) has a precision of 87.46%, recall of 89.28%, and f1-score of 88.36%.
   - The weighted average of precision, recall, and f1-score is also provided, along with support (the number of instances) for each class.
   - The accuracy of the model on the testing data is 99.24%.

5. Class Report (Train):
   - The class report provides precision, recall, and f1-score for each class (0 and 1) in the training data.
   - Class 0 (healthy) has a precision of 99.64%, recall of 99.57%, and f1-score of 99.61%.
   - Class 1 (high risk) has a precision of 85.46%, recall of 89.89%, and f1-score of 87.78%.
   - The weighted average of precision, recall, and f1-score is also provided, along with support (the number of instances) for each class.
   - The accuracy of the model on the training data is 99.15%.

6. Dataset Distribution:
   - The loan_status column shows that there are 75,036 healthy (0) observations and 2,500 high-risk (1) observations.
   - This indicates an imbalance in the dataset, with the majority class being healthy loans.

7. Additional Information:
   - The classification report is provided as a dictionary format, showing precision, recall, f1-score, and support for each class.

Overall, the logistic regression model demonstrates excellent performance in predicting loan statuses. It achieves high accuracy and shows good precision, recall, and f1-scores for both classes. However, due to the class imbalance, it's important to consider additional techniques like oversampling or undersampling to handle the imbalance effectively and ensure the model's performance on both classes.


## Summary

Summarise the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
