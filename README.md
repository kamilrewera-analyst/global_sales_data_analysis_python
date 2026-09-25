# Global E-Commerce Sales & Supply Chain Analytics

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1_w7f5-IXysiUrWDf7bTL411eAQ4PT_0L)

An end-to-end Python data analytics project exploring global sales operations across online and physical retail channels. The study covers data cleaning, data integration, KPI reporting, fulfillment lead-time analysis, time-series dynamics, and day-of-week seasonality trends.

---

## 📌 Project Overview & Objectives

The goal of this project is to clean, transform, aggregate, and visualize multi-year transactional data to uncover key business insights and logistics performance patterns.

### Core Business Questions Addressed:
1. **Financial KPIs & Channel Performance:** What are the total revenue, profit, order volume, and geographic reach across online vs. physical retail channels?
2. **Geographic & Product Metrics:** Which regions, countries, and product categories generate the highest margins and demand?
3. **Supply Chain & Logistics Lead Time:** How long does fulfillment take (order-to-shipment duration), how does it vary by country/category, and does fulfillment speed impact profitability?
4. **Sales Dynamics & Seasonality:** What are the multi-year sales trends and day-of-week demand patterns across product categories?

---

## 🛠️ Data Pipeline & Project Workflow

The project follows a standard Data Analytics Lifecycle:

### 1. Data Ingestion & Schema Exploration
* Source datasets merged:
  * `events.csv`: Transaction logs across multiple years.
  * `products.csv`: Product taxonomy and catalog metadata.
  * `countries.csv`: Regional hierarchy and country codes.

### 2. Data Cleaning & Preprocessing
* **Missing Value Analysis:** Evaluated null proportion and handled missing records with business logic justification.
* **Type Conversion & Normalization:** Corrected date formatting, numeric casting, and string whitespace/casing inconsistencies.
* **Deduplication:** Identified and eliminated duplicate entries caused by encoding variances or extra whitespace.
* **Anomaly & Outlier Detection:** Screened for invalid order dates, negative prices, and unrealistic lead times.

### 3. Exploratory Data Analysis (EDA) & Feature Engineering
* Calculated key metrics: Revenue, Cost, Profit, and Fulfillment Lead Time (`shipping_date - order_date`).
* Extracted temporal attributes such as year, month, and day of week (`day_name()`).

### 4. Logistics & Seasonality Deep Dive
* Evaluated average fulfillment delays by product category and country.
* Analyzed correlation between shipping duration and overall profitability.
* Uncovered seasonality trends across weekdays to assist in demand forecasting.

---

## 🧰 Tech Stack & Python Libraries

* **Environment:** Google Colab / Jupyter Notebook
* **Data Wrangling:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Temporal Analysis:** `datetime`

---

## 📊 Business Key Takeaways & Findings

* **Sales Channels:** Clear breakdown of physical store performance vs. online sales distribution.
* **Logistics Efficiency:** Identified bottleneck countries/regions with above-average fulfillment delays.
* **Seasonality:** Revealed distinct day-of-week purchasing patterns informing target promotional schedules.

---

## 🔗 Notebook Access

You can view the full Google Colab report, code implementation, and interactive visualizations here:
👉 [Open Google Colab Notebook](https://colab.research.google.com/drive/1_w7f5-IXysiUrWDf7bTL411eAQ4PT_0L)
