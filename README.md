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

- Accurracy:
- Precision:
- Recall

### Summary:

Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

Summarize the results from the machine learning model. Include your justification for recommending the model for use by the company. If you don’t recommend the model, justify your reasoning. (10 points)
