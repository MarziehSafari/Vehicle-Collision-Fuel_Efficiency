# NYC Traffic Safety & Fuel Efficiency Analysis
This repository contains a two-part data science study focused on urban mobility in New York City. The first part investigates **Motor Vehicle Collisions** to identify high-risk areas and demographics, while the second part focuses on **Fuel Efficiency** and **Predictive Modeling**.

### 🚦 Part 1: NYC Collision Analysis (2021)
This project analyzes traffic accident patterns across NYC to pinpoint high-risk zones and contributing factors using geospatial and statistical tools.

#### Objectives
**Data Integration:** Retrieve real-time data from NYC OpenData via API calls.  
**Preprocessing:** Clean and structure raw JSON/CSV data for spatial analysis.  
**Geospatial Visualization:** Map crash locations using Folium to identify hotspots.  
**Statistical Profiling:** Identify correlations between vehicle makes, driver demographics, and crash frequency.

#### Tech Stack & Libraries
**Languages/Tools:** Python, SQL, SQLite3, Jupyter Notebook  
**Libraries:** matplotlib, seaborn, folium, geopy, pandas

#### Key Findings
**High-Risk Zones:** Brooklyn and Queens emerged as the areas with the highest collision frequency, likely influenced by the high traffic volume surrounding JFK and LaGuardia airports.  
**Demographics:** Analysis revealed that male drivers were involved in a significantly higher proportion of crashes.  
**Vehicle Makes:** The most frequent makes involved in collisions were Toyota, Honda, Nissan, and Ford.

### ⛽ Part 2: Fuel Efficiency & Model Development
Using real-world fuel consumption data, this study evaluates the accuracy of EPA ratings compared to actual performance and builds predictive models for fuel economy.

#### Objectives
**Feature Engineering:** Calculate percent_difference_actual to compare EPA ratings against real-world Geotab data.  
**Statistical Testing:** Use Chi-square tests to find significant associations between vehicle specs (Make, Hybrid status) and efficiency.  
**Predictive Modeling:** Develop and refine Regression models to predict expected fuel consumption.

### Analysis & Results
*1. Statistical Insights (Chi-Square Test)*  
Actual Fuel Economy is significantly associated with Vehicle Make, Hybrid/Non-Hybrid status, and Standard Type.  
Winner: The data indicates that Toyota Hybrids (Sedans) are the most efficient choices in the NYC fleet.  
*2. Model Evaluation*  
I compared two approaches to predict epa_expected_fuel:  
Simple Linear Regression: Used total_actual_fuel as a single predictor.  
Multiple Linear Regression: Combined total_actual_miles, total_actual_fuel, and actual_fuel_economy_geotab.

#### Result: 
The Multiple Linear Regression model performed significantly better, showing a higher $R^2$ and lower standard deviation, indicating a more robust fit.

#### 📈 Future Work
**Temporal Analysis:** Investigate how weather patterns and time of year impact collision rates.  
**Infrastructure Study:** Analyze how specific city infrastructure (bike lanes, roundabouts) correlates with safety data.
