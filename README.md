# credit-risk-classification
##This repository uses a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.
  
Please read through report "Credit Risk Classification Report" for the finalised model report.  
Jupyter file can be found under folder Credit_Risk > "credit_risk_classification.ipnb"  
 

1. Dataset Information:
   - The dataset contains 77,536 entries and 8 columns.
   - The columns represent features such as loan_size, interest_rate, borrower_income, debt_to_income, num_of_accounts, derogatory_marks, total_debt, and loan_status.
   - The dataset has a mix of float and integer data types.

2. Logistic Regression Model:
   - The logistic regression model has been trained and tested on the given dataset.
   - The model achieved a high accuracy score of 99.24% on the testing data.
   - The model's performance on the training data is also impressive, with an accuracy score of 99.15%.
   - The model's predictions were compared with the actual values for both the training and testing data.

   ## Summary

Overall, the logistic regression model demonstrates excellent performance in predicting loan statuses.  
It achieves high accuracy and shows good precision, recall, and f1-scores for both classes. 
However, due to the class imbalance, it's important to consider additional techniques like oversampling or undersampling to handle the imbalance effectively and ensure the model's performance on both classes.  
If the sponsor of the application has a higher risk appetite
If the sponsor of the application has alower risk appetitite then 