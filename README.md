# Lead-Scoring-Case-Study-


Summary of Lead Scoring
X Education has appointed us to help them select the most promising leads, i.e. the leads that
are most likely to convert into paying customers. The company requires us to build a model
wherein we need to assign a lead score to each of the leads such that the customers with higher
lead score have a higher conversion chance and the customers with lower lead score have a
lower conversion chance.
The CEO, in particular, has given a ballpark of the target lead conversion rate to be around
80%.
Data
We have been provided with a leads dataset from the past with around 9000 data points. This
dataset consists of various attributes such as Lead Source, Total Time Spent on Website, Total
Visits, Last Activity, etc. which may or may not be useful in ultimately deciding whether a
lead will be converted or not. The target variable, in this case, is the column ‘Converted’
which tells whether a past lead was converted or not wherein 1 means it was converted and 0
means it wasn’t converted.
Approach
1. Cleaning Data
The data was cleaned as it contained lot of unrelated columns and column which
contained NULL values. We also cautiously dropped a few columns after
understanding the meaning from the Data Dictionary.
2. Dummy Variables
The dummy variables were created for the categorical variables and the NULL
equivalent rows were removed from the data before doing the model building exercise.
3. Train-Test Split
The split between the test and train data was kept at 70:30.
4. Model Building
A RFE model was created with number of features as 15. Later a few variables were
removed the model depending on the Variance Inflation Factor ( lesser than 5) and p
value threshold lower than 0.05.
5. Model Evaluation
We also identified the optimum threshold using ROC curve. All parameters like the
specificity, sensitivity and accuracy were also calculated. Confusion Matrix was
created for model evaluation.
6. Prediction and Precision/Recall
Prediction threshold was kept at 45% with Precision and Recall close to 79%
