# Overview
This is a Python project of mine created with the goal of analyzing sales trends for an e-commerce business and visualizing them. The project consisted of importing data through BigQuery using SQL, analyzing sales trends by region, traffic channel and devices and analyzing user registration trends through the same verticals. Throughout the code you can find business recommendations for this e-commerce business based on the data discovered.

# Tech Stack
- Python (Google Colab) for writing the code
- Numpy, Pandas, SciPy libraries for data cleanup and analytics
- Matplotlib, Seaborn and Tableau Public for visualizations

# Conclusions based on the data

This analysis of 349,545 ecommerce sessions from November 2020 to January 2021 reveals several key insights into business performance and customer behavior:

- **Geographic & Market Dynamics:**
The Americas dominate revenue (17.7M USD, 55%) and order volume (18,553 orders), with the United States alone accounting for ≈44% of global sales. Asia and Europe represent secondary markets at 24% and 19% of revenue respectively. Cross-continental correlation analysis shows that Americas, Asia, and Europe exhibit moderate positive correlations (r=0.67-0.69), suggesting synchronized purchasing patterns driven by shared seasonal trends like holiday shopping. Africa and Oceania operate largely independently with minimal market share.

- **Product Performance:**
Sofas & armchairs lead in revenue (26.24%, 8.4M USD) but rank third in order volume, indicating high-value, low-frequency purchases. Conversely, Bookcases & shelving units dominate order count (22.75%) but contribute less revenue (11.39%), reflecting affordable, frequent purchases. This revenue-vs-volume discrepancy highlights two distinct customer behaviors: occasional big-ticket purchases versus regular smaller transactions. Category sales show moderate correlations (r=0.48-0.67), suggesting promotional periods and traffic spikes lift all categories simultaneously.

- **Traffic & Acquisition:**
Organic search drives 34% of revenue, establishing it as the primary acquisition channel, followed by direct traffic (23%) and referral (18%). Paid CPC accounts for only 4% of revenue, indicating heavy reliance on non-paid channels. All traffic sources exhibit moderate to strong correlations with each other (r=0.43-0.72), confirming that high-traffic days generate increases across all channels simultaneously rather than isolated spikes in individual sources.

- **Device & User Behavior:**
Desktop dominates with 59% of sales, while mobile represents 39% and tablet is negligible at 2%. Average order values remain consistent across devices (≈950 USD mean, ≈440 USD median), indicating no device-specific spending patterns. The mean-median gap reveals significant outlier orders pulling averages upward across all segments.

- **Registration & Conversion:**
Only 7.99% of sessions come from registered users, with ≈20% of orders placed by guest users consistently across all continents. Subscription status shows no meaningful impact on average order value (921 USD vs 965 USD), suggesting email engagement does not correlate with purchase value. This represents a significant growth opportunity for improving user registration and email capture strategies.

- **Temporal Patterns:**
Sales peaked dramatically in early December (≈680K daily) corresponding to Black Friday/Cyber Monday, with this spike primarily driven by Americas and organic traffic. Daily order count exhibits an exceptionally strong correlation with total sales (r=0.96, p < 0.001), indicating stable average order values and predictable revenue patterns based on order volume alone.

- **Data Quality Considerations:**
The mobile_model_name field mixes browsers and device models, limiting device-level analysis. Approximately 6.4% of revenue has deleted attribution data, likely reflecting GDPR compliance. The 'unknown' and '(not set)' categories across various dimensions suggest data collection inconsistencies worth addressing in future implementations.

# Visualization
You can find the Tableau Public dashboard for this project here: [Tableau Public](https://public.tableau.com/app/profile/mykhailo.nedozhdii/viz/E-commerceDashboard_17714170715700/E-commerceDashboard)
