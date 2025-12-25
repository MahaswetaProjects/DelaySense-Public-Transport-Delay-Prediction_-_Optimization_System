🚦 DelaySense - ML-Powered Public Transport Delay Prediction & Optimization System

## Project Overview

**DelaySense** is an end-to-end data analytics and machine learning project designed to analyze, predict, and optimize public transport delays across Indian transportation systems.
The project combines **Excel, Python, Power BI, and Machine Learning** to deliver actionable insights and real-time delay predictions through an interactive dashboard and deployed API.

## Problem Statement

Public transport delays negatively impact passenger satisfaction, fuel efficiency, and operational planning.
This project aims to:

* Identify delay patterns across routes, cities, and operators
* Understand the relationship between fuel usage, distance, and delays
* Predict delay categories using machine learning
* Provide data-driven insights for transport optimization


##  Datasets Used

APSRTC Public Transportation Dataset (Kaggle)

Key attributes:

* Route and depot details
* Distance traveled
* Passenger occupancy
* Fuel consumption
* Delay minutes

Indian Railways Train Delay Dataset (Kaggle)

Key attributes:

* Train and station details
* Average delay minutes
* On-time and delayed percentages

Both datasets were cleaned, standardized, and merged into a unified transport analytics dataset.

## Tech Stack

| Layer                         | Tools Used             |
| ----------------------------- | ---------------------- |
| Data Storage & Querying       | SQL                    |
| Data Cleaning & Preprocessing | Python (Pandas, NumPy) |
| Data Analysis & EDA           | Python, Excel          |
| Visualization                 | Power BI               |
| Machine Learning              | Scikit-learn           |
| Model Deployment              | Flask                  |
| Version Control               | Git & GitHub           |


## Data Preprocessing

* Removed duplicates and invalid records
* Handled missing values using logical imputation
* Converted data types (dates, numeric fields)
* Standardized column names
* Engineered new features:

  * `delay_category`
  * `fuel_delay_factor`
  * Aggregated delay metrics

  
## Exploratory Data Analysis (EDA)

Key insights explored:

* Delay distribution by city, route, and operator
* Peak delay periods (day-wise & monthly trends)
* Relationship between fuel consumption and delay minutes
* High-risk routes with consistent delays

## Machine Learning Model

### 🔹 Problem Type

Multi-class classification

### 🔹 Target Variable

`delay_category`
(On Time, Slight Delay, Moderate Delay, Severe Delay)

### 🔹 Model Selection

* Baseline: Logistic Regression
* Final Model: **Random Forest Classifier**

### 🔹 Why Random Forest?

* Handles non-linear relationships effectively
* Robust to noisy real-world transport data
* Supports mixed numerical and categorical features
* Provides feature importance for explainability

### 🔹 Model Optimization

* Hyperparameter tuning using **GridSearchCV**
* Evaluation using accuracy, precision, recall, and F1-score



## Model Deployment

The trained model was deployed using **Flask** as a REST API.

### API Features:

* Accepts transport details as JSON input
* Returns predicted delay category
* Ready for integration with dashboards or external applications


##  Power BI Dashboard

### Dashboard Highlights:

* KPI cards for average delay, maximum delay, on-time performance
* Delay intensity heatmap by day and time
* Fuel vs delay scatter analysis
* Actual vs predicted delay comparison
* Optimization recommendation table

### Dashboard Theme:

* Dark UI for better readability
* Conditional formatting for risk visualization
* Interactive slicers for dynamic analysis


## Key Insights

* Certain routes and operators consistently experience higher delays
* Fuel inefficiency strongly correlates with delay severity
* Peak delays are more frequent during specific weekdays and months
* ML predictions help identify potential delay risks before operations

## Future Enhancements

* Integrate real-time weather and traffic data
* Deploy API on cloud platforms (Render / AWS)
* Add confidence scores to predictions
* Extend dashboard with live prediction integration
* Implement advanced models like XGBoost

