# SmartKart Customer Churn Analytics

> **End-to-end machine learning pipeline for identifying customers at risk of churn and supporting data-driven customer retention decisions.**

## Overview

Customer churn is a critical business problem for customer-centric organizations. Losing existing customers can impact revenue, customer lifetime value, and long-term business growth.

This project develops an end-to-end **Customer Churn Analytics and Prediction Pipeline** for SmartKart. The workflow transforms raw customer data into actionable churn predictions using data preprocessing, exploratory analysis, feature selection, feature standardisation, and **Logistic Regression**.

The dataset intentionally contains real-world data-quality challenges, including duplicate records, missing values, invalid entries, and outliers, allowing the pipeline to demonstrate practical machine learning preprocessing rather than working with an already-clean dataset.

---

## Business Problem

SmartKart needs to proactively identify customers who are likely to leave the platform.

The objective is to answer:

> **"Which customers are most likely to churn, and how can predictive analytics help the business take preventive action?"**

The resulting predictions can support customer retention teams in prioritising customers for targeted engagement and retention initiatives.

---

## Project Objectives

* Analyze customer-level behavioral data
* Identify and handle data-quality issues
* Detect and treat outliers
* Select relevant predictive features
* Prepare data for machine learning
* Build a binary classification model
* Predict customer churn
* Evaluate model performance
* Interpret model results from a business perspective

---

## Machine Learning Workflow

The project follows a structured **15-stage ML pipeline**:

```text
Raw Customer Data
       ↓
Data Collection
       ↓
Data Understanding
       ↓
Data Cleaning
       ↓
Outlier Detection & Treatment
       ↓
Feature Selection
       ↓
Target Definition
       ↓
Target Encoding
       ↓
Train-Test Split
       ↓
Feature Standardisation
       ↓
Model Building
       ↓
Model Training
       ↓
Churn Prediction
       ↓
Model Evaluation
       ↓
Model Interpretation
       ↓
Business Output
```

This structure follows the workflow implemented in the notebook.

---

## Dataset

The project uses a deliberately messy SmartKart customer dataset containing **100 customer records**.

### Key Features

| Feature         | Description                               |
| --------------- | ----------------------------------------- |
| `Customer_ID`   | Unique customer identifier                |
| `Age`           | Customer age                              |
| `Monthly_Spend` | Customer's monthly spending               |
| `Complaints`    | Number of complaints raised               |
| `Churn`         | Target variable indicating customer churn |

The target variable is binary:

```text
0 → Customer did not churn
1 → Customer churned
```

The notebook output also shows that duplicate customer IDs and extreme values are present in the raw data, requiring preprocessing before modeling.

---

## Data Preprocessing

A major focus of the project is preparing imperfect business data for machine learning.

The pipeline addresses:

* Duplicate records
* Missing values
* Invalid values
* Outliers
* Data-type inconsistencies
* Feature selection
* Feature standardisation

This reflects a practical ML workflow where **data preparation is an important part of model development**.

---

## Model

### Logistic Regression

The project uses **Logistic Regression** as the primary classification algorithm.

It is suitable for this use case because churn is represented as a binary classification problem.

### Prediction

The model estimates the probability that a customer belongs to the churn class.

```text
Customer Data
     ↓
Preprocessed Features
     ↓
Logistic Regression
     ↓
Churn Probability
     ↓
Predicted Class
     ↓
0 = Retained
1 = Churned
```

---

## Model Evaluation

The notebook evaluates the classification model using appropriate performance metrics.

The evaluation stage is designed to assess how effectively the model distinguishes between customers who churn and customers who remain.

Typical classification evaluation includes:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

The project also includes model interpretation to connect the technical results with the underlying business problem.

---

## Business Impact

A churn prediction system can help SmartKart move from **reactive customer management to proactive retention**.

### Potential Business Applications

**Risk Identification**

Identify customers with a higher likelihood of leaving.

**Retention Prioritisation**

Focus retention resources on customers who require attention.

**Customer Segmentation**

Understand differences between retained and churned customers.

**Data-Driven Decisions**

Use predictive insights to support customer engagement strategies.

**Revenue Protection**

Early identification of potential churn can help reduce preventable customer losses.

---

## Technology Stack

| Category                | Technology                      |
| ----------------------- | ------------------------------- |
| Programming             | Python                          |
| Data Processing         | Pandas, NumPy                   |
| Data Visualization      | Matplotlib, Seaborn             |
| Machine Learning        | Scikit-learn                    |
| Model                   | Logistic Regression             |
| Development Environment | Google Colab / Jupyter Notebook |
| Data Format             | CSV                             |

The notebook imports Pandas, NumPy, Matplotlib and Seaborn and uses a Colab-based data-upload workflow.

---

## Project Structure

```text
smartkart-customer-churn-analytics/
│
├── SmartKart_Churn_Prediction_ML_Pipeline.ipynb
├── SmartKart_dirty_100_rows.csv
├── README.md
└── LICENSE
```

---

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/smartkart-customer-churn-analytics.git
cd smartkart-customer-churn-analytics
```

### 2. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
SmartKart_Churn_Prediction_ML_Pipeline.ipynb
```

### Google Colab

The notebook can also be executed in Google Colab. Upload the required CSV dataset and run the cells sequentially from beginning to end.

---

## Key Learning Outcomes

This project demonstrates practical understanding of:

* Data collection
* Data inspection
* Data cleaning
* Exploratory data analysis
* Outlier treatment
* Feature selection
* Target encoding
* Train-test splitting
* Feature standardisation
* Classification
* Logistic Regression
* Model evaluation
* Model interpretation
* Business-oriented ML application

---

## Future Improvements

The current project provides a strong baseline churn prediction workflow. It can be further enhanced by:

* Comparing Logistic Regression with Random Forest, XGBoost, and other classifiers
* Hyperparameter tuning
* Cross-validation
* Feature engineering
* Probability-based customer risk scoring
* Model explainability using SHAP
* Churn-risk dashboards
* Automated model deployment
* Monitoring model performance over time

---

## Project Outcome

The project demonstrates how an organization can transform **raw customer data into predictive insights** through a structured machine learning pipeline.

The ultimate goal is not simply to predict churn, but to provide information that can support **proactive customer retention and business decision-making**.

---

## Author

**Ayushi**

BBA FinTech & AI / AI & ML

---

## License

This project is intended for **educational and portfolio purposes**.

---

⭐ **If you found this project useful, consider starring the repository.**
