# Credit Risk Classification

### Purpose of the analysis:
 
 The purpose of this analysis was to use historical lending activity from a peer-to-peer lending services company to build a model that can predict whether a loan will be healthy or high-risk.

### Explain what financial information the data was on, and what you needed to predict:
The data used to make the model included over 77,000 data points containing the following 7 features:
- Loan size
- Interest rate
- Borrower's yearly income
- Borrower's debt to income Ratio
- Borrower's number of accounts
- Borrower's derogatory marks
- Borrower's total debt

Using these features, the model can predict if a loan will be healthy or high-risk. The model would help the lender adjust the loan size and interest rate offered with the goal of predicting a healthy loan. For example, if a potential borrower wanted a $15,000 loan but the model always predicted this to be high-risk, then the lender would deny that loan. If lowering the amount to $10,000 resulted in a prediction of healthy, then the lender could instead offer a $10,000 loan, rather than completely denying the loan service. A good model will lower the amount of defaulted loans the lender gets.

### Describe the stages of the machine learning process you went through as part of this analysis:
First, the dataset was randomly split into training and testing datasets. The training dataset contained 75% of the original data, the testing dataset contained the remaining 75% of the original data.

Then, a Logistic Regression model was treated using the training data and the LogisticRegression function from sklear.linear_model.

The testing data was then applied to this model to make predictions on the loan's status.

The model's performace was evaluated using three functions from skliearn.metrics: calculating its balanced accuracy score, generating a confusion matrix, and printing a classification report.


### Results:
- Accurracy: The balanced accuracy score was 95% when using the balanced_accuracy_score function from the sklearn.metrics library. The balanced accuracy score is lower than the accurracy score of 99% because the dataset is imbalanced, meaning the dataset contains far more healthy loans than unhealthy loans. Since the model performs so much better at predicting healthy loans, the accurracy score is higher than the balanced accuracy score. Both of these are very good and shows that overall, the you can be confident that the model is correct 95% of the time. 

- Precision: The classification report shows that the precision of a healthy loan predictions is 1.00, meaning that when the model predicts a loan is healthy, it is correct essentially every time. The classification report shows that the precision of a high-risk loan is 0.85, meaning that when the model predicts a loan is high-risk, it is only correct 85% of the time. This means that the lender has a significant chance of denying a good loan if making their decision based on this model alone.

- Recall: The classification report shows that the recall of a healthy loan prediction is 0.99, meaning that when a loan is healthy, the model will have predicted it is healthy 99% of the time. The classification report shows that the recall of a high-risk loan prediction is 0.91, meaning that when a loan is high-risk, the model will have predicted that 91% of the time.

### Summary:
Ultimately, if the decision is "should I ALWAYS go with the precictions of this model?" the lender has to ask themselves this question: Is erroneously denying 15% of healthy loans worth correctly identifying and denying 91% of high-risk loans. They'd have to look at their current track-record of loan decisions to determine if that's better or worse than their current performance.

Overall, the lender can be more confident in the model's prediction when it predicts the loan is healthy. Therefore I would recommend that they absolutely go with the model's prediction when approving a loan. When denying a loan, they might first want to look at other contributing factors outside of the model's features.
