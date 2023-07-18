# Bank_Customer_Prediction
This project aims to develop a machine learning model for a top European bank to predict customer churn. By analyzing customer data, the model identifies patterns causing churn and achieves an accuracy of up to 86.36%.
Bank Customer Churn Prediction
This project aims to develop a machine learning model to predict whether a customer of one of the topmost banks in Europe is likely to churn (i.e., discontinue their relationship with the bank) in the near future. By analyzing customer data and identifying patterns that contribute to customer churn, the bank can take proactive measures to retain customers.
Dataset
The dataset used for this project is stored in the file "BankCustomerChurn.csv". It contains information about both churned and active customers, including the following variables:
•	RowNumber: Row number in the dataset
•	CustomerId: Unique identifier for each customer
•	Surname: Customer's surname
•	CreditScore: Customer's credit score
•	Geography: Customer's country (France, Spain, Germany)
•	Gender: Customer's gender (Female, Male)
•	Age: Customer's age
•	Tenure: Number of years the customer has been with the bank
•	Balance: Customer's account balance
•	NumOfProducts: Number of bank products/services used by the customer
•	HasCrCard: Whether the customer has a credit card (0 = No, 1 = Yes)
•	IsActiveMember: Whether the customer is an active member (0 = No, 1 = Yes)
•	EstimatedSalary: Estimated salary of the customer
•	Exited: Whether the customer has churned (0 = No, 1 = Yes)
Preprocessing of the Data
The first step is to preprocess the data before building the machine learning model. The following steps are performed:
1.	Import necessary libraries and load the dataset into a pandas DataFrame.
2.	Check the dimensions of the dataset using the shape attribute.
3.	Explore the column names using the columns attribute.
4.	Check the data types of the columns using the dtypes attribute.
5.	Identify categorical variables in the dataset with less than 10 unique values.
6.	Convert the identified categorical variables into the 'category' data type.
7.	Remove duplicate rows from the dataset using the drop_duplicates method.
8.	Check for missing values in the dataset using the isna().sum() method.
9.	Create the feature matrix x by dropping the target variable ('Exited') and irrelevant columns ('RowNumber', 'CustomerId', 'Surname').
10.	Create the target variable vector y by selecting only the 'Exited' column from the dataset.
11.	Perform dummification of the categorical attributes using the get_dummies function.
Model Building
The next step involves building the machine learning model for churn prediction. The following steps are performed:
1.	Split the preprocessed data into training and testing sets using the train_test_split function.
2.	Check the dimensions of the training and testing sets.
3.	Create an instance of the DecisionTreeClassifier class with the desired parameters.
4.	Fit the model to the training data using the fit method.
5.	Generate predictions for both the training and testing data using the predict method.
6.	Calculate the accuracy of the model on the training and testing data using the accuracy_score function.
7.	Compute the confusion matrix for both the training and testing data using the confusion_matrix function.
8.	Generate a classification report for both the training and testing data using the classification_report function.
Results
The project considers three decision tree models with different maximum depths: 3, 9, and 6. The evaluation metrics for each model are as follows:
Decision Tree with Depth 3:
•	Training Accuracy: 0.8406
•	Testing Accuracy: 0.8518
Decision Tree with Depth 9:
•	Training Accuracy: 0.8888
•	Testing Accuracy: 0.8539
Decision Tree with Depth 6:
•	Training Accuracy: 0.8579
•	Testing Accuracy: 0.8636
The classification reports provide precision, recall, and F1-score values for each class, as well as the overall accuracy and support.
Conclusion
In conclusion, this project developed machine learning models using decision trees to predict customer churn for a top European bank. The models achieved reasonable accuracy in predicting churn based on the given customer data. The decision tree with a depth of 6 performed slightly better than the other models, with a testing accuracy of 86.36%. These models can assist the bank in identifying customers who are more likely to churn and enable them to take proactive measures to retain those customers.
Note: The code provided is a series of code snippets. To run the code, ensure that the necessary libraries are imported and the dataset file "BankCustomerChurn.csv" is available in the working directory.

![image](https://github.com/Kartheekbandi/Bank_Customer_Prediction/assets/123476304/207faa80-e442-4c50-ab06-7c5d77651853)
