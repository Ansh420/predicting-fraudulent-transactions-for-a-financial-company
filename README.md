# predicting-fraudulent-transactions-for-a-financial-company
We developed a robust fraud detection model for a financial company using XGBoost, leveraging its superior accuracy and ability to handle imbalanced datasets, to predict fraudulent transactions and enhance the company's security measures.
## Data cleaning including missing values, outliers and multi-collinearity.
 - There is **no null values** in any columns
 - Most of the datapoints are **not correlated**
 - Oldbalance is correlated with newbalance of person who intitiated transaction
 - newbalanceDest and oldbalanceDest is also correlated.

## Describe your fraud detection model in elaboration.
**Fraud Detection Model contains following steps**:

- Loading of dataset and Explore it
- Checking the Distribution of transaction datatype
- Checking for the need of data cleaning
- **statistical Analysis of Data**
- Deal with the skewed data with boxcox tranformation and log transformation
- Taking features to train the data
- **Train test split with 80-20 rule**
- use Sampling to balance the dataset.
- Fit the model to RandomForestClassifier and Logistic Regression
- **Analyse the results**
## What are the key factors that predict fraudulent customer?
'isFlaggedFraud', 'oldbalanceOrg', 'type_CASH_OUT', 'type_TRANSFER' are fraud causing/predicting features.
## Do these factors make sense? If yes, How? If not, How not?
**Yes, these factors absolutely makes sense**.

- **'isFlaggedFraud'** - column which marks transaction as a fraud or not

- **'oldbalanceOrg'** - indicates that customer/individual with more balance in his account is prone to fraud transaction

- **'Cash-Out'** - it refers to convert non-cash asset into Cash. Thus online selling of large goods etc is more prone to frauds.

- **'Transfer'** - Uninformed transfers mode have found to be modes through which fraud takes place.
## What kind of prevention should be adopted while company update its infrastructure?
- Can implement multiple account to distribute the huge balance.
- Sperate account for online transactions.
- Special mode for cash out transactions.
- Special regestering of account users for transfer modes.
## Demonstrate the performance of the model by using best set of tools

- **Accuracy** is used for measuring accuracy.

- Only accuracy cannot be relied as in Fraud detection problem, recall and precision is more important than other metrics.

- We Get **highest Precision** in Logistic Regression

- **highest Accuracy** in Random Forest Classifier

- **highest Recall** in Random Forest Classifier

- **highest F1 Score** in Random Forest Classifier

- By this I concludes **Random Forest Classifier is best model** for this fraud transaction detection
