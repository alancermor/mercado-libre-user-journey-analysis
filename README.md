# Mercado Libre: User Journey & Retention Analysis 📦

### Project Overview
This project simulates a real-world task for a Product Analyst within the Growth & Retention team at Mercado Libre. The objective is to analyze user behavior to understand where users drop off in the purchasing process and how retention evolves over time.

Using **SQL**, I mapped the complete conversion funnel and calculated user retention rates by cohorts to propose actionable improvements based on data.

### Business Problem
The product director posed the following key questions:
1.  **Funnel Analysis:** At which stage of the process do we lose the most users? What is the conversion rate between each key step?
2.  **Retention Analysis:** How well do we retain users over time (D7, D14, D21, D28)?
3.  **Segmentation:** How do these metrics vary by country (`country`)?

### Technical Stack
* **Language:** SQL (Standard/BigQuery dialect)
* **Key Concepts:**
    * **CTEs (Common Table Expressions):** To structure the funnel stages logically.
    * **Aggregate Functions:** To calculate conversion rates and drop-offs.
    * **Window Functions:** For complex user segmentation.
    * **Cohort Analysis:** Grouping users by signup date to track retention.

### Key Insights 💡
Based on the analysis of data from Jan 2025 to Aug 2025:

* **Critical Drop-off:** There is a significant loss of approximately **65 percentage points** between the *First Visit* and the *Select Item* stages. This suggests a need to optimize the homepage or search relevance.
* **Top Performer:** **Uruguay** displays the highest conversion rates across the funnel, whereas Paraguay shows the lowest efficiency.
* **Retention Trends:** Retention is strong at **Day 7 (~86%)** across most cohorts but drops aggressively by **Day 28 (~2-3%)**. This indicates that while acquisition is effective, long-term engagement strategies (like loyalty programs) are needed to sustain user activity.

### Repository Structure
1.  `mercadolibre_analysis.sql`: The complete SQL script containing data exploration, funnel construction (CTEs), and cohort logic.
2.  `Executive_Summary.xlsx`: A detailed report containing the quantitative results, visualizations tables, and strategic recommendations.

---
*This project is part of the Data Analysis Bootcamp at TripleTen.*
