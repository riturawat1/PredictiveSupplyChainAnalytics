# Predictive Supply Chain Analytics
 Predictive analytics dashboard using Machine Learning (XGBoost) & Power BI to identify and reduce late supply chain deliveries.
**📥 Live Dashboard:** [Click here to download the interactive Power BI (.pbix) file](https://drive.google.com/file/d/1WZKutVWML5awUBgIZt-1zG2s4c7nNfxU/view?usp=sharing)

## Project Overview
Supply chain inefficiencies and late deliveries lead to significant profit erosion and loss of customer trust. This project is an end-to-end data analytics and machine learning pipeline built to solve real-world fulfillment bottlenecks. 
Instead of just visualizing past delays, this project integrates a predictive Machine Learning model to identify which pending orders are at the highest risk of being late, allowing warehouse and operations teams to take proactive action before the SLA is breached.

## Tools & Technologies
* **Data Processing & EDA:** Python (Pandas, NumPy)
* **Machine Learning:** Scikit-Learn, XGBoost (Classification)
* **Data Visualization:** Power BI, Matplotlib, Seaborn
* **Environment:** Jupyter Notebook

## Machine Learning Integration (Predictive Action)
To move from descriptive to predictive analytics, an XGBoost classification model was trained on historical data to predict late deliveries.
* **Strictly Avoided Data Leakage:** Excluded 'actual shipping days' and 'shipping gap' from the training features to ensure the model reflects real-world predictive environments.
* **Actionable Probabilities:** Utilized `.predict_proba()` to generate a 'Late Probability %' for each order rather than a simple binary output.
* **The Action Center:** Fed the ML predictions directly into the Power BI dashboard, isolating 17.7K pending orders with a >90% probability of being late. This serves as a daily action list for warehouse managers to fast-track high-risk shipments.

## Key Business Insights
1. **Overall System Risk:** 57.28% of all orders are delivered late. When an order misses its deadline, the average delay is 2 days past the scheduled delivery date.
2. **Fulfillment Bottlenecks:** Standard Class shipping is the primary driver of delays, averaging 2.4 days over the SLA. This indicates a strong need to renegotiate current logistics contracts.
3. **Regional Risk:** LATAM and Africa face a 60%+ late rate. Transitioning to localized distribution hubs is critical to stop profit leakage in these regions.
4. **Financial Impact:** Delays in high-volume categories like Fishing & Camping correlate directly with negative profit margins. Reducing the shipping gap by even one day would significantly recover lost margins.

## Repository Structure
* `/Scripts`: Contains Jupyter Notebooks for Data Cleaning, Feature Engineering, Exploratory Data Analysis (EDA), and Machine Learning.
* `/Dashboard_Screenshots`: Contains high-quality previews of the final Power BI dashboard.

## Dashboard Previews

### 1. Executive Overview
*(Provides a high-level summary of total revenue, average delays, and historical late delivery trends.)*
![Executive Overview](<img width="1327" height="744" alt="Screenshot 2026-05-19 111801" src="https://github.com/user-attachments/assets/a6fcae57-e242-4022-bb9d-fff56e76c085" />
)

### 2. Operational Analysis
*(Breaks down bottlenecks by shipping class, region, and product category to identify root causes.)*
![Operational Analysis](<img width="1330" height="743" alt="Screenshot 2026-05-19 111823" src="https://github.com/user-attachments/assets/b1216c50-d203-4598-a172-eb96cca4ee8c" />
)

### 3. Predictive Risk & Action Center
*(The ML-driven interface showing real-time system risk and a prioritized list of high-risk orders for the operations team.)*
![Predictive Risk](<img width="1328" height="745" alt="Screenshot 2026-05-19 111842" src="https://github.com/user-attachments/assets/e8a4093a-01fe-4f4f-988e-c33655e6797d" />
)
