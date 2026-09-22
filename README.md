## Project Overview

Zomato Business Intelligence & Delivery Analytics is a data analytics and machine learning project focused on understanding restaurant orders, revenue, delivery performance, customer ratings, and order cancellations.

The project follows a business intelligence workflow from data cleaning and exploratory data analysis to cancellation prediction and business insights.

## Objectives

- Analyze Zomato order and restaurant data.
- Clean and prepare the dataset for analysis.
- Identify revenue, restaurant, city, rating, and delivery patterns.
- Analyze order cancellation patterns.
- Build a machine learning model to predict order cancellation risk.
- Generate actionable business insights from the analysis.

## Dataset

The project uses a Zomato food delivery dataset containing order, restaurant, delivery, rating, payment, and location-related information.


The dataset used in this project was obtained from Kaggle.

**Dataset Link:**  
https://www.kaggle.com/datasets/nairahul/zometo-dataset

- **Original Records:** 12,079
- **Columns:** 33
- **Records After Cleaning:** 11,867

The dataset contains 12,079 records and 33 columns before cleaning.

## Data Cleaning

The following data cleaning steps were performed:

- Removed duplicate records.
- Standardized column names by removing extra spaces.
- Converted the Order Date column into datetime format.
- Checked missing values.
- Checked invalid numerical values.
- Checked rating values outside the valid 1–5 range.
- Filled missing categorical/text values with "Unknown".

After cleaning, the dataset contained 11,867 records and 33 columns.

## Exploratory Data Analysis (EDA)

Exploratory Data Analysis was performed to understand:

- Revenue trends.
- Top-performing restaurants by revenue.
- City-wise revenue.
- Order status distribution.
- Payment method usage.
- Restaurant and customer ratings.
- Delivery time patterns.
- Cancellation patterns.
- Promo code and free delivery analysis.
- Relationships between order amount, delivery distance, delivery time, ratings, and number of items.

## Machine Learning

A Logistic Regression model was used to predict whether an order would be cancelled.

The target variable was:

- 0 — Not Cancelled
- 1 — Cancelled

Two model versions were evaluated. The second version used pre-order features to reduce the possibility of outcome-related data leakage.

### Final Model Performance

| Metric | V2 Model |
|---|---:|
| Accuracy | 50.63% |
| Precision | 32.65% |
| Recall | 49.48% |
| F1-Score | 39.34% |

The model also generated cancellation probabilities that were grouped into Low Risk, Medium Risk, and High Risk categories using predefined probability ranges.

## Key Business Insights

- Total revenue generated was ₹18,743,281 across 11,867 records.
- The average order value was ₹1,579.45.
- The overall cancellation rate was 32.34%.
- Domino's Pizza generated the highest revenue among the top restaurants analyzed, with ₹102,833.
- Chennai generated the highest revenue among the top cities analyzed, with ₹1,198,459.
- Shimla had the highest cancellation rate among the listed top cancellation-rate cities, at 44.90%.
- The correlation between delivery time and rating was approximately -0.004, indicating almost no linear relationship in this dataset.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- Excel

## Project Structure

Zomato_Business_Intelligence_Analytics/
│
├── Zomato_Business_Intelligence_Analytics.ipynb
├── data/
│   └── zomato_data.xlsx
├── outputs/
│   ├── charts/
│   └── cleaned_data/
├── README.md
├── requirements.txt
└── Zomato_ProjectReport.docx

## How to Run

1. Install Python.
2. Install the required libraries using:

   pip install -r requirements.txt

3. Open Jupyter Notebook.
4. Open `Zomato_Business_Intelligence_Analytics.ipynb`.
5. Make sure the dataset is available inside the `data` folder.
6. Run the notebook cells from top to bottom.
