# Databel Telecom: Customer Churn Analysis in Excel

This project is a comprehensive analysis of the Databel Telecom customer churn dataset. Using only Microsoft Excel, this analysis dives into the key drivers of customer attrition. The final output is a single, interactive dashboard that visualizes *who* is churning, *why* they are leaving, and *where* the problems are most severe.

## 📈 Final Dashboard

<img width="1494" height="746" alt="Image" src="https://github.com/user-attachments/assets/c25e4882-2ec7-43be-83d5-8d1bc85cd848" />

## 💡 Key Findings

### Overall Summary
Our overall churn rate is a high **26.86%**. The problem is being driven by **Seniors (60+)**, who churn at a rate of **38%**. The primary reason they're leaving is for **competitors who offer better devices and prices**. This problem is most severe in **California**.

### Key Problems
* **Seniors are the highest-risk group.** Customers aged 60+ are churning at a much higher rate (38%) than any other group.
* **Losing to competitors.** The #1 reason people leave is for a "**competitor's better offer**," followed by "**better devices**."
* **"Unlimited Plan" is failing.** It has a *higher* churn rate than your limited plans, which suggests customers don't find it valuable.
* **Bad Support:** "Attitude of support person" is the **#2 biggest** single reason for churn.

### Deeper Insights
* More than 1 out of every 4 customers has left.
* "Unlimited Plan" customers are churning **more** than our other customers, suggesting the plan is not perceived as a good value.
* "International Plan" **is a huge churn signal**. The churn rates for customers with the plan are extremely high and significantly worse than the churn rates for customers without the plan.

## 🚀 Recommended Action Plan

1.  Create a retention plan specifically for **Seniors**.
2.  Analyze your **competitors' pricing and device offers** to see why you are losing.
3.  Fix your **customer support attitude** and re-evaluate your "**Unlimited Plan**" and "**International Plan**" pricing.

---

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
