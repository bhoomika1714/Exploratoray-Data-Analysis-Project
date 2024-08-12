# Exploratoray-Data-Analysis-Project
**The WiDS  Datathon  2024 focuses on predicting the metastatic diagnosis period for patients who have been diagnosed with metastatic triple-negative breast cancer (TNBC). The goal is to develop predictive models to estimate the period (in days) between the diagnosis of breast cancer and the diagnosis of metastatic cancer.**

## Objectives
Understand and preprocess the data to handle missing values, encode categorical         variables, and normalize features appropriately.
Perform exploratory data analysis (EDA) to uncover patterns, relationships, and feature importance related to the target variable.
Develop and evaluate multiple machine learning models to predict the probability of the Diagnosis Period being less than 90 days, using performance metrics for optimization. 

## Data description
The WiDS Datathon 2024 focuses on a prediction task using a roughly 19k record dataset (split into training and test sets).
 The objective of the test is to predict the patients Metastatic Diagnosis period in the test dataset based on the provided charateristics and information about the patient.

## Data Pre-processing
No duplicates were present in the dataset
DROPPING THE COLUMNS 
Imputing The rest of the columns with mean values and dropping those columns with more than 20% of null           values.
['metastatic_first_novel_treatment', 'metastatic_first_novel_treatment_type', 'patient_gender’] dropped columns.
Filling the columns with null value with mean of each column for numerical data and mode of each column for categorical data.
Aggregating Temperature DataAveraged monthly temperature data and dropped original columns

## Target Encoding
Target Encoding is a technique used to convert categorical variables into numerical values by replacing each category with the mean of the target variable for that category. 
This encoding technique uses the relationship between the categorical feature and the target variable to create the numerical representation.
By using Target Encoding, we effectively encode categorical variables into meaningful numerical representations that preserve their relationship with the target variable. 
This process helps improve the predictive power of the models and handles high-cardinality features efficiently.payer_type', 'patient_state', 'Region', 'Division', 'patient_gender', 'breast_cancer_diagnosis_code', 'metastatic_cancer_diagnosis_code' these are our target columns.

# Feature Selection
While developing the machine learning model, only a few variables in the dataset are useful for building the model, and the rest features are either redundant or irrelevant. 
If we input the dataset with all these redundant and irrelevant features, it may negatively impact and reduce the overall performance and accuracy of the model.
 Hence, it is very important to identify and select the most appropriate features from the data and remove the irrelevant or less important features, which is done with the help of feature selection in machine learning. 
We used an 80-20 split ratio with the train_test_split function from sklearn.   - This means 80% of the data was used for training and 20% for testing.  
 random_state=100 was set to ensure the split is reproducible.
selected_features ->'patient_id','payer_type', 'patient_age', 'metastatic_cancer_diagnosis_code’.

# Hyperparameter Tuning!
We have used GridSearchCV to perform hyperparameter tuning for a CatBoost Regressor, evaluating different combinations of depth, learning_rate, and iterations to find the best model. 
Hyperparameter tuning is crucial as it helps in enhancing model performance, preventing overfitting, and ensuring the model is efficient and well-suited for the given dataset.





# RMSE SCORE USING DIFFERENT MACHINE LEARNING MODELS

![Screenshot 2024-08-13 001550](https://github.com/user-attachments/assets/8fd4db0d-94dd-4466-b163-9d70beff51b2)

# Port-Folio Link:
https://sites.google.com/view/portfolio-bhoomika/home


