# defneerencan-Defne-Erencan-DSA210
DSA210 Term Project – Seasonal Spending Analysis using Akbank Card Data.

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
Main columns include:

- **Date & Time** – When the transaction happened.  
- **Transaction Amount** – How much was spent.  
- **Category** – Type of expense (food, transportation, entertainment, etc.).  
- **Merchant Name** – Where the purchase was made.  
- **Remaining Balance** – Card balance after the transaction.  

## Hypothesis Testing
- **Spending Difference Test:**  
  - **H₀:** There is **no difference** in total spending between school and summer periods.  
  - **H₁:** Spending is **significantly different** between these two periods.  
  - **Method:** t-test for statistical comparison.  
  - **Interpretation:** If *p-value < 0.05*, the difference is statistically significant.

- **Coffee Consumption Test:**  
  - **H₀:** Exam weeks **do not affect** coffee purchases.  
  - **H₁:** Coffee spending **increases during exams**.  
  - **Interpretation:** *p-value < 0.05* means the change is significant.

- **Family Home Spending Test:**  
  - **H₀:** Spending is **the same** at university and at home.  
  - **H₁:** Spending **decreases** when staying at home.  
  - **Interpretation:** *p-value < 0.05* means spending is lower at home.

## Tools & Technologies
- **Python**
  - `pandas` – Organizing and cleaning data  
  - `numpy` – Math operations  
  - `matplotlib` & `seaborn` – Graphs and visualizations  
  - `scipy.stats` – Statistical analysis  
- **Jupyter Notebook** – For analysis and visualization  
- **Excel** – For collecting and categorizing data  

## Data Processing
- **Cleaning Data:** Removed columns that were not needed (e.g., receipt numbers).  
- **Categorizing Transactions:** Grouped transactions into:  
  - **Essential spending:** Food, transportation, school items  
  - **Discretionary spending:** Entertainment, self-care, shopping  
  - **Social spending:** Restaurants, outings, events  
- **Time Periods Defined:**  
  - **Summer Vacation (June – September)**  
  - **School Term (October – May)**  
  - **Family Home Periods (Winter & Summer Breaks)**  

## Data Analysis & Visualizations
- **Total Spending Over Time:** Compared spending in school and summer using **line and area charts**.  
- **Spending by Category:** Showed category totals with **bar and stacked bar plots**.  
- **Social vs. Academic Spending:** Compared these categories using **grouped bar** and **violin plots**.  
- **Coffee Spending Trends:** Checked **how often and how much** coffee was bought during exams using **line and histogram plots**.  
- **Balance Tracking:** Studied how the balance changed over time using **scatter** and **cumulative plots**.  
- **Home vs. University Spending:** Compared both situations using **box plots** and **heatmaps**.  

## Limitations & Future Work
- **Personal Data:** Based only on my own spending, so results are not general for everyone.  
- **Limited Time Range:** More years of data could show clearer patterns.  
- **Automation Idea:** Using machine learning to classify expenses automatically.  
- **Future Improvements:** Building an interactive dashboard to track spending in real time.  
