# Defne Erencan DSA210 Term Project
Seasonal Spending Analysis using Akbank Card Data.

## Introduction
I am **Defne Erencan**, and this project analyzes my **seasonal spending patterns** based on my **Akbank card transaction data**.  
The main purpose is to understand how my financial habits change between **summer break** and the **school term**.  
I also study how my spending behavior changes when I stay at my **family home**, where my costs are usually lower.

## Motivation
As a university student, my spending habits and priorities vary during the year.  
This project focuses on several key differences:

- **Higher expenses during school time** because of transportation and academic needs.  
- **More social spending in summer** since I have more free time.  
- **Different types of personal expenses**, such as spending more on self-care or leisure in summer and on essentials during school.  
- **Study workload effects** on flexible spending like coffee, snacks, or entertainment.  
- **Less spending at home**, since many daily expenses (food, bills, etc.) are paid by my family.

## Data Source
The data comes from **Akbank card transaction records**, exported as an **Excel file**.
Data was exported **manually** from **Akbank mobile banking**.
Main columns include:

- **Date & Time** – When the transaction happened.  
- **Transaction Amount** – How much was spent.  
- **Category** – Type of expense (food, transportation, entertainment, etc.).  
- **Merchant Name** – Where the purchase was made.  
- **Remaining Balance** – Card balance after the transaction.  

## Exploratory Data Analysis (EDA)
Several visualizations were created to explore spending behavior across different time periods and categories.

- **Total spending over time** shows clear differences between school and summer periods, indicating seasonal variation in expenses.
- **Category-based plots** reveal that essential spending dominates during the school term, while discretionary and social spending increase in summer.
- **Coffee and snack-related plots** suggest higher frequency and spending during exam weeks.
- **Home vs. university comparisons** show lower overall spending when staying at the family home.

**Interpretation:**  
These visual patterns suggest meaningful differences in spending behavior across seasons and living conditions, motivating formal hypothesis testing.

## Hypothesis Testing

### Spending Difference Test
- **H₀ (Null Hypothesis):** There is **no difference** in total spending between school and summer periods.  
- **H₁ (Alternative Hypothesis):** Total spending is **significantly different** between school and summer periods.  
- **Method:** Independent t-test.  
- **Interpretation:** If *p-value < 0.05*, the difference in spending is statistically significant.

### Coffee Consumption Test
- **H₀ (Null Hypothesis):** Exam weeks **do not affect** coffee purchases.  
- **H₁ (Alternative Hypothesis):** Coffee spending **increases during exam weeks**.  
- **Method:** t-test comparing exam and non-exam periods.  
- **Interpretation:** If *p-value < 0.05*, exam periods have a significant effect on coffee spending.

### Family Home Spending Test
- **H₀ (Null Hypothesis):** Spending is **the same** at university and at the family home.  
- **H₁ (Alternative Hypothesis):** Spending **decreases** when staying at the family home.  
- **Method:** t-test.  
- **Interpretation:** If *p-value < 0.05*, spending at home is significantly lower.

## Tools & Technologies
- **Python**
  - `pandas` – Data cleaning and organization  
  - `numpy` – Numerical operations  
  - `matplotlib` & `seaborn` – Data visualization  
  - `scipy.stats` – Hypothesis testing  
- **Jupyter Notebook** – Analysis and visualization  
- **Excel** – Data collection and categorization  

## Data Processing
- **Cleaning Data:** Removed unnecessary columns and handled missing values.  
- **Categorizing Transactions:**  
  - **Essential spending:** Food, transportation, school items  
  - **Discretionary spending:** Entertainment, self-care, shopping  
  - **Social spending:** Restaurants, outings, events  
- **Time Period Definitions:**  
  - **Summer Vacation:** June – September  
  - **School Term:** October – May  
  - **Family Home Periods:** Winter and summer breaks  

## Data Analysis & Visualizations
- **Total Spending Over Time:** Line and area charts comparing school and summer spending.  
- **Spending by Category:** Bar and stacked bar plots.  
- **Social vs. Academic Spending:** Grouped bar and violin plots.  
- **Coffee Spending Trends:** Line plots and histograms during exam periods.  
- **Balance Tracking:** Scatter and cumulative balance plots.  
- **Home vs. University Spending:** Box plots and heatmaps.

## Machine Learning

To extend the analysis beyond descriptive statistics and hypothesis testing,
a **machine learning classification model** was developed to predict
expense categories based on transaction-level features.

### Problem Definition
- **Task:** Expense category prediction  
- **Type:** Supervised multiclass classification  
- **Target Variable:** Expense category  

### Features Used
- **Transaction Amount**  
- **Month**  
- **Weekday**  
- **Weekend Indicator**  

These features capture temporal and behavioral spending patterns without
relying on merchant-level information.

### Models Implemented
- **Logistic Regression** (baseline model)  
- **Random Forest Classifier** (non-linear model)  

Logistic Regression was used as a simple baseline, while Random Forest was
chosen to better capture non-linear relationships in spending behavior.

### Model Evaluation
- **Evaluation Metrics:** Accuracy, Precision, Recall, F1-score  
- **Confusion Matrices** were used to analyze class-level performance.  

The Random Forest model achieved higher overall performance compared to
Logistic Regression, particularly for frequent categories such as
**Restaurant** and **Bank Transfer**.

### Interpretation
- Transaction amount was identified as the **most important feature**
  for predicting spending categories.
- Temporal features such as **month** and **weekday** contributed
  additional predictive power.
- Lower performance on rare categories highlights the effect of
  **class imbalance** in personal spending data.

### Use Case
This machine learning approach demonstrates how future card transactions
can be **automatically categorized**, reducing the need for manual labeling
and enabling scalable personal finance analysis.


## Limitations & Future Work
- **Personal Data:** Analysis is based on a single individual and is not generalizable.  
- **Limited Time Range:** Additional years of data could improve trend reliability.  
- **Automation Idea:** Applying machine learning to automatically classify transactions.  
- **Future Improvements:** Developing an interactive dashboard for real-time spending tracking.
