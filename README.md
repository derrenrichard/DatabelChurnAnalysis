# Databel Telecom: Customer Churn Analysis in Excel

This project is a comprehensive analysis of the Databel Telecom customer churn dataset. Using only Microsoft Excel, this analysis dives into the key drivers of customer attrition. The final output is a single, interactive dashboard that visualizes *who* is churning, *why* they are leaving, and *where* the problems are most severe.

## 📈 Final Dashboard

<img width="1494" height="746" alt="Image" src="https://github.com/user-attachments/assets/c25e4882-2ec7-43be-83d5-8d1bc85cd848" />

## 💡 Key Insights from the Analysis

This dashboard uncovers several critical, actionable insights:

1.  **Seniors are the Highest-Risk Group:** Customers aged 60+ are the most vulnerable demographic, churning at a rate of **38%**, far higher than any other group.
2.  **Losing to the Competition:** The **#1 reason** customers leave is for a "competitor's better offer," followed by "competitor's better devices."
3.  **The "Unlimited Plan" is Failing:** The Unlimited Plan has a *higher* churn rate than limited plans, suggesting a significant problem with its price or perceived value.
4.  **"International Plan" is a Major Problem:** Customers with the International Plan churn at extremely high rates (e.g., **75% in California**), indicating it's a major source of dissatisfaction.
5.  **Geographic Hotspots:** Churn is not evenly distributed. States like **California (34.8%)** and **Pennsylvania (33.3%)** are major problem areas that require targeted action.

## 🛠️ Tools & Methodology

This entire project was conducted in **Microsoft Excel**, leveraging its powerful data analysis features.

* **Tool:** Microsoft Excel
* **Core Features:**
    * **Data Preparation:** New columns were created using `IF` formulas to segment data (e.g., `Demographics`, `Grouped Consumption`).
    * **PivotTables:** Used extensively to aggregate and slice data across multiple dimensions (e.g., State, Age, Plan).
    * **Calculated Fields:** The `Churn Rate %` field was created directly within the PivotTable to perform analysis.
    * **PivotCharts:** All visuals (Bar, Doughnut, Line, and Combo charts) are PivotCharts driven by the data.
    * **Dashboarding:** The final dashboard is a collection of charts and slicers on a single, clean worksheet.

### Key Formulas Used (Excel)

* **Demographics Column:**
    ```excel
    =IF([@[Under 30]]="Yes", "Under 30", IF([@Senior]="Yes", "Senior", "Other"))
    ```
* **Consumption Grouping Column:**
    ```excel
    =IF([@[Avg Monthly GB Download]]<5, "Less than 5 GB", IF([@[Avg Monthly GB Download]]<10, "Between 5 and 10 GB", "10 or more GB"))
    ```
* **Churn Rate % (Calculated Field):**
    ```excel
    ='Churned Customers' / 'Total Customers'
    ```

## 📊 Data Source

* **Dataset:** [Databel Telecom Customer Churn Dataset on Kaggle](https://www.kaggle.com/datasets/yichienchong/databel-telecom-customer-churn-dataset)
* **Metadata:** [Databel Metadata Sheet (PDF)](https://assets.datacamp.com/production/repositories/6386/datasets/0d84b751e28911f4a2c51b1a38c0100a55d8037e/Metadata%20Sheet%20-%20Customer%20Churn.pdf)

## 🚀 Recommended Action Plan

Based on the data, the following strategic actions are recommended:

1.  **Create a Retention Plan Specifically for Seniors.**
2.  **Analyze Competitors' Pricing and Device Offers** to understand why we are losing.
3.  **Fix Customer Support Attitude** (the #2 reason for churn) and **Re-evaluate the "Unlimited Plan" Pricing.**
