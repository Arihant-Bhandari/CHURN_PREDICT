# Customer Churn Prediction

Dataset link: https://www.kaggle.com/datasets/blastchar/telco-customer-churn

* Problem Statement: For any service-based industry, it is always paramount to focus on **Customer Retention**. The **loss of customers** is known as **Customer Churn**. Utilizing ML models, we aim to predict whether a given customer will leave their service based on certain features or "parameters".

* Task type: **Classification**

* Features: 

| Column Name      | Description |
|------------------|-------------|
| customerID       | Unique identifier for each customer |
| gender           | Customer's gender |
| SeniorCitizen    | Whether the customer is a senior citizen (1) or not (0) |
| Partner          | Whether the customer has a partner (Yes/No) |
| Dependents       | Whether the customer has dependents (Yes/No) |
| tenure           | Number of months the customer has been with the company |
| PhoneService     | Whether the customer has phone service (Yes/No) |
| MultipleLines    | Whether the customer has multiple lines (Yes/No/No phone service) |
| InternetService  | Type of internet service (DSL/Fiber optic/No) |
| OnlineSecurity   | Whether the customer has online security (Yes/No/No internet service) |
| OnlineBackup     | Whether the customer has online backup (Yes/No/No internet service) |
| DeviceProtection | Whether the customer has device protection (Yes/No/No internet service) |
| TechSupport      | Whether the customer has tech support (Yes/No/No internet service) |
| StreamingTV      | Whether the customer has streaming TV (Yes/No/No internet service) |
| StreamingMovies  | Whether the customer has streaming movies (Yes/No/No internet service) |
| Contract         | Type of contract (Month-to-month/One year/Two year) |
| PaperlessBilling | Whether the customer has paperless billing (Yes/No) |
| PaymentMethod    | Customer's payment method |
| MonthlyCharges   | Amount charged to the customer monthly |
| TotalCharges     | Total amount charged to the customer |
| Churn            | Whether the customer has churned (Yes/No) |

## Pipeline:

1. Data Loading: loading the data, basic look on top 5 and bottom 5 values

2. Data Description: basic dataset description like information about columns (datatype and non-null count of columns), statistics for numerical columns (max, min, std dev, quantiles, etc.), number null values in columns

3. Data Imputation and Data Encoding: cleaning data, by imputing missing values and encoding categorical values

4. Model Creation and Evaluation: creating models and testing them based on metrics

## Models used as of version 1.0:

* Logistic Regression

* Xtreme Gradient Boosting (XGB) Classifier

* Histogram-based Gradient Boosting Classifier 

* Categorical Boosting (CatBoost) Classifier

* Random Forrest Classifier

Max Accuracy obtained (VERS 1.0): 79.9%

---

## Website integration

The ML model can be "pickled" using Python's pickle library for object serialization into a byte-file, which can be stored as a web resource to be called at runtime.

By building a website which takes in necessary details, running it through similar encoding procedures to be turned into numerical values and deserializing our model's byte-file, we can predict and return our prediction with the help of a flask application file over APIs.

1. Building a web interface to collect user input
2. Processing the input (including encoding categorical variables)
3. Loading the serialized model
4. Making predictions
5. Returning results via an API