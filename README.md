CREDIT RISK CLASSIFICATION

Overview of the Analysis

-	Purpose of the analysis.
Assessing borrower creditworthiness is crucial for the short-term and long-term success of lending institutions. 
Leveraging historical lending data to help identify borrower creditworthiness can provide significant advantages
Aiming to train and evaluate a model focused on loan risk

-	Data and prediction:
The dataset includes information on 77,536 unique loans, covering details such as loan amount, interest rate, borrower income, the ratio of loan size to income, total debt, loan status, and more. Complete details can be found in the "lending_data.csv" file located in the Credit Risk folder.
Determining whether a loan is high-risk or not will be crucial for the lender

-	Order of Operations and methods used
o	Read in the .csv file.
o	Create the label set (y) and develop the features (X)
o	Split the dataset into training and testing sets for y and X by using sklearn train_test_split.
o	Fit a logistic regression model using the training data (X_train and y_train) with methods sklearn logistic regression and its .fit
o	Generate predictions on the testing data labels using the testing feature data (X_test) and the fitted model with predict functions
o	Evaluate model performance with confusion matrix and classification report

Results
(a) The confusion matrix illustrates the model's performance based on known true values. The confusion matrix for this exercise is provided below and is also available in the Report folder:
Confusion Matrix:
•	True Positive (TP): 593
•	True Negative (TN): 18,673
•	False Positive (FP): 86
•	False Negative (FN): 32

(b) The classification report offers insights into the model's performance for each class of loan status. The classification report for this exercise is provided below and is also available in the Report folder:
Classification Report
The two classifications related to loans are Healthy and High Risk. The analysis yields the following scores:
(1) Precision measures the percentage of positive predictions (TP) out of the total positive predictions :
•	Healthy: 1.0
•	High Risk: 0.87
(2) Recall measures the percentage of correct positive predictions (TP) out of the total actual positives (TP + FN):
•	Healthy: 1.0
•	High Risk: 0.95
(3) F1 Score provides a balanced measure by comparing to 1.0, indicating how well the model predicts:
•	Healthy: 1.0
•	High Risk: 0.91
(4) Accuracy reflects the proportion of correct instances out of the total number of instances, which is 99%.
(5) Support denotes the number of actual occurrences of each class in the dataset:
•	Healthy: 18,759
•	High Risk: 625

Summary
In developing a methodology to assess borrower creditworthiness, the logistic regression model used in this exercise serves as a solid initial approach. It achieved high overall accuracy, with Precision, Recall, and F1 Score for High Risk loans all exceeding 87%. However, lenders generally seek even higher Accuracy, Precision, and Recall metrics, as their business relies on recovering the loan principal plus interest. Even minor issues with loan repayments or defaults can significantly affect their lending capacity.
Enhancing the model could be beneficial. Incorporating additional data about loans and borrowers—such as previous successful repayments or the number of open loans—might lead to more robust modeling and more accurate scores. It could be worthwhile to improve the model concurrently with using the current version or to slightly delay implementation to ensure the best possible model is available in the future.

Data source
Xpert Learning Assistant
