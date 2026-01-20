# Mercado Libre: User Journey & Retention Analysis 📦

### Project Overview
This project simulates a real-world task for a Product Analyst within the Growth & Retention team at Mercado Libre. The objective is to analyze user behavior to understand where users drop off in the purchasing process and how retention evolves over time.

Using **SQL**, I mapped the complete conversion funnel and calculated user retention rates by cohorts to propose actionable improvements based on data.

### Business Problem
The product director posed the following key questions:
1.  **Funnel Analysis:** At which stage of the process do we lose the most users? What is the conversion rate between each key step?
2.  **Retention Analysis:** How well do we retain users over time (D7, D14, D21, D28)?
3.  **Segmentation:** How do these metrics vary by country (`country`) and device (`device_category`)?

### Technical Stack
* **Language:** SQL (Standard/BigQuery dialect)
* **Key Concepts:**
    * **CTEs (Common Table Expressions):** To structure the funnel stages logically.
    * **Aggregate Functions:** To calculate conversion rates and drop-offs.
    * **Window Functions:** For complex user segmentation.
    * **Cohort Analysis:** Grouping users by signup date to track retention.

### Dataset Structure
The analysis utilizes two main datasets covering the period from **Jan 2025 to Aug 2025**:

#### 1. `mercadolibre_funnel`
Tracks user events during the shopping process.
* **Key Stages:** `first_visit` ➔ `select_item` ➔ `add_to_cart` ➔ `begin_checkout` ➔ `add_shipping_info` ➔ `add_payment_info` ➔ `purchase`.
* **Key Dimensions:** `user_id`, `session_id`, `event_name`, `country`, `device_category`, `referral_source`.

#### 2. `mercadolibre_retention`
Tracks recurring user activity and registration dates.
* **Key Metrics:** `signup_date`, `activity_date`, `day_after_signup` (D7, D14, etc.), `active` (binary indicator).

### Methodology
1.  **Funnel Mapping:** Defined a **7-stage macro journey** from "Discovery" to "Conversion".
2.  **Conversion Rates:** Calculated the percentage of users moving from one stage to the next to identify the steepest "drop-off" points.
3.  **Cohort Grid:** Built a retention matrix to analyze user engagement on days 7, 14, 21, and 28 post-signup.

### Key Insights (Example Placeholders)
* *Funnel:* The largest drop-off occurs between **Add to Cart** and **Begin Checkout**, indicating potential friction in the login or cart review process.
* *Retention:* Users acquired through "Paid Search" show a **15% higher retention** rate at D7 compared to organic traffic.
* *Seasonality:* A spike in conversion was observed during promotion periods in specific countries.

---
*This project is part of the Data Analysis Bootcamp at TripleTen.*
