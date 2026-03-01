Bank Transaction Analysis & Customer Segmentation 💳📊

Project Overview

This project performs an end-to-end Exploratory Data Analysis (EDA) and Customer Segmentation on a dataset of over 1 million bank transactions in India from 2016. The goal is to derive actionable insights into customer spending behavior and classify users into distinct segments using the RFM (Recency, Frequency, Monetary) framework.
📂 Dataset Features

The dataset contains transaction-level data with the following attributes:

    Customer Demographics: Gender (CustGender), Location (CustLocation), and Date of Birth (CustomerDOB).

    Financial Data: Account Balance (CustAccountBalance) and Transaction Amount (TransactionAmount (INR)).

    Temporal Data: Transaction Date and Time.

🛠️ Tech Stack

    Language: Python

    Data Manipulation: Pandas, NumPy

    Visualization: Matplotlib, Seaborn, Plotly, Squarify (for Treemaps)

🔍 Key Analysis Phases
1. Data Cleaning & Preprocessing

    Sampling: Utilized a 10% stratified sample for computational efficiency.

    Datetime Correction: Handled legacy date formats (pre-1970) and corrected year-of-birth anomalies.

    Binning: Categorized customers into age groups: Under35, Adults, and Over65.

2. Exploratory Data Analysis (EDA)

    Gender & Age Insights: Analyzed average account balances across demographics, revealing that the Over65 male segment holds the highest average balance.

    Time Series Analysis: Identified a massive transaction spike in August 2016, suggesting a seasonal or external economic event.

    Balance vs. Spending: Discovered a correlation where customers in higher balance quartiles tend to perform larger average transactions.

3. RFM Segmentation (The Core)

We implemented an RFM Model to score customers on a scale of 1–4 across three dimensions:

    Recency: Days since last transaction (calculated from a 2016-12-10 snapshot).

    Frequency: Total number of transactions per customer.

    Monetary: Total transaction value.

Customers were then grouped into 7 behavioral segments:
| Segment | Description |
| :--- | :--- |
| Elite Customers | High value, high frequency, and recent activity. |
| Very Good/Good | Reliable customers with consistent engagement. |
| Average | The standard user base. |
| Inactive | At-risk customers who haven't transacted in a long time. |
📈 Visualizations

The project includes:

    RFM Treemaps: Using squarify to visualize the proportion of each customer segment.

    Pivot Tables: Aggregated views of account balances by age and gender.

    Monthly Distributions: Bar charts showing transaction volume per month.

🚀 How to Run

    Clone the repo.

    Ensure you have the CSV file in the root directory.

    Install dependencies:
    Bash

    pip install pandas matplotlib seaborn plotly squarify

    Execute Bank_Transactions-Final(1).ipynb.
