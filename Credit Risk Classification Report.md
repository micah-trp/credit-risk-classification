# Credit risk classification 

## Overview of the Analysis

The purpose of this analysis was to use a dataset of historical lending activity from a peer-to-peer lending service company and build a model that can identify the creditworthiness of borrowers by predicting if they are healthy loan or a high-risk loans.

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
We were required to use the information of the data to build a model and `predict whether a loan was (0) "Healthy" or (1) "High Risk"` in this context.
   
In the provided data there were `77,536` with `2,500 observations / 3.22%` as High Risk and the remaining `75,036 observationsor 76.78%` as Healthy.
Therefore it is noted that the model may include some form of class imbalance- as there a many more instances of class (0) than class (1).

## Stages of Building the model.

1. Data Collection: Data was provided in csv format.

2. Data Preprocessing: Data was taken at import value in this case.

3. Data Partitioning: Split the preprocessed data into two or three subsets: a training set and a test set. 

4. Model Training: Feed the training data into the logistic regression algorithm to estimate the model's coefficients or weights.

5. Model Evaluation: Assess the performance of the trained model using evaluation metrics such as the confusion matrix,  accuracy, precision, recall, F1 score.


## Methods Used

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


## Summary

Overall, the logistic regression model demonstrates excellent performance in predicting loan statuses.  
It achieves high accuracy and shows good precision, recall, and f1-scores for both classes. 
However, due to the class imbalance, it's important to consider additional techniques like oversampling or undersampling to handle the imbalance effectively and ensure the model's performance on both classes.  
  
- If the sponsor of the application has a higher risk appetite then this model may not be best optimised yet as it predicts a higher proportion of "False Negatives" and fails to identify "High Risk" loans.
Further adjustment to the model would be required to take into account the class imbalance.  

- If the sponsor of the application has a lower risk appetitite then the model is recommended as it performs with high accuracy.  