<h1 style="text-align: center;">Analysis of 911 Calls for Detroit and New York City</h1>

This project presents a detailed analysis of 911 emergency call data from two major U.S. cities: Detroit and New York City. The purpose of this analysis is to utilize advanced data mining and machine learning techniques to gain insights that can enhance public safety and emergency response strategies.

Detroit, known for its high crime rates, and New York City, with its dense population, provide two distinct urban landscapes that pose unique challenges for emergency response. By exploring patterns in the frequency, distribution, and nature of 911 calls, this project aims to help city departments such as police, fire departments, hospitals, and emergency services allocate resources more effectively. The analysis also identifies high-demand areas, common emergencies, and peak times for calls, which will contribute to improved crisis management and quicker response times.

## Goals
- Identify trends in call volumes by time and location to enable faster, more efficient deployment of emergency services.
- Provide recommendations for the strategic deployment of emergency units based on high-call areas and peak times.
- Identify common emergencies and geographic hotspots to help city departments implement targeted interventions.
- Use predictive analytics to forecast future emergency call trends, improving readiness and crisis response.

## Methodology

### 1. Data Collection and Preprocessing
The analysis was based on two datasets:
- **Detroit 911 Calls Dataset**: Contains timestamps, locations, call types, response times, and descriptions.
- **New York City NYPD Calls Dataset**: Includes incident location, type, response times, and more.

**Preprocessing Steps**:
- **Handling Missing Values**: Filled missing time values using mean or forward-fill methods to maintain data integrity.
- **Date/Time Parsing**: Separated timestamp columns into date and time components to analyze daily, monthly, and seasonal trends.
- **Outlier Handling**: Corrected or removed extreme outliers (e.g., unusually long response times) to ensure consistency.
- **Categorization**: Grouped call types into broader categories (e.g., medical emergencies, crimes) for simplified trend analysis.

### 2. Exploratory Data Analysis (EDA)
We conducted EDA to gain insights into the structure and trends of the data:
- **Temporal Analysis**: Charts were used to analyze call distributions by hour, day, and month, identifying peak times.
- **Spatial Analysis**: Heatmaps revealed geographic hotspots of emergency calls.
- **Call Types and Response Times**: Visualizations highlighted the most common emergencies and average response times.

### 3. Predictive Modeling
Two models were used to forecast emergency call volumes:
- **SARIMAX**: A time-series model trained on hourly data to predict future call volumes by identifying seasonal patterns. Performance was evaluated using Mean Absolute Error (MAE).
- **XGBoost**: A regression model used to predict hourly call distribution based on features like call time, location, and type. The model was evaluated using Mean Squared Error (MSE).

### 4. Clustering
Clustering techniques were applied to identify patterns in incident types and locations:
- **K-Means Clustering**: Grouped incidents based on call type, location, and response time. The quality of clusters was measured using the Calinski-Harabasz Index.
- **DBSCAN**: Identified high-density clusters and separated them from outliers. This technique highlighted specific hotspots that traditional methods might miss.

## Key Findings

#### Peak Call Times:
- **Detroit**: The highest volume of 911 calls occurred between 4 PM and 7 PM, with significant spikes in winter months (January and February).
- **New York City**: The call volume peaked at 4 PM, with another increase around midnight, especially in high-density boroughs like Manhattan and Brooklyn.

#### High-Demand Areas:
- **Detroit**: Midtown, Wayne State, and Warrendale reported the highest number of 911 calls.
- **New York City**: Manhattan and Brooklyn consistently showed the highest call volumes, particularly in areas with a high concentration of nightlife and public events.

#### Response Times:
- **Detroit**: Longer response times were observed in low-priority incidents, while high-priority calls (e.g., violent crimes) received faster responses.
- **New York City**: Response times varied by borough, with faster responses in high-risk areas but slower times for non-emergency calls.

#### Seasonal Trends:
Both cities showed a significant increase in emergency calls during the winter months, likely due to weather-related incidents and holidays.
