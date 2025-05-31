# US Accidents Insights

## Project Overview
This project analyzes a large-scale dataset of **7.7 million** traffic accidents across the United States to extract meaningful insights about accident patterns, contributing factors, and severity. It aims to demonstrate practical skills in handling big data, data cleaning, imputation, and geospatial visualization, providing a solid foundation for data-driven traffic safety analysis.

## Dataset
The dataset is sourced from Kaggle’s [US Accidents (March 2023)](https://www.kaggle.com/datasets/sobhanmoosavi/us-accidents), containing detailed records of road accidents from 2016 till 2023. It includes timestamps, location data, weather and visibility conditions, road features, and severity ratings.

## Data Cleaning and Preprocessing
Given the dataset’s size and complexity, intensive data cleaning was crucial:

* **Chunk-wise loading** to efficiently handle large data without memory overload.
* **Dropping irrelevant columns** to reduce noise.
* **Datetime conversion** for time-based analysis.
* **Handling missing values:**
  * Imputed missing timestamps by using weather timestamp proxies and statistical averages grouped by city and weather condition.
  * Cleaned and standardized categorical variables like weather conditions and wind directions by mapping multiple variants to consistent categories.
  * Corrected inconsistent city names using regex and title-casing for uniformity.
  * Geocoded missing zip codes using latitude and longitude information, respecting API rate limits.
* **Boolean conversion** for compatibility with ML models and easier analysis.
* **Feature engineering:** Extracted accident duration, date, and hour features.
* **Imputed numerical weather-related features** (temperature, humidity, visibility) with group-wise and overall means to handle missing data effectively.
* **Standardized twilight phase indicators** by computing missing values based on sunrise/sunset times and converting them to binary for analysis.

## Key Analyses and Visualizations
* Examined accident frequency and severity by weather conditions and visibility.
* Identified how road features like traffic signals, junctions, crossings, etc influence accident severity.
* Compared accident durations across different times of day and twilight phases, revealing longer durations during nighttime and adverse weather.
* Created city- and state-level geospatial visualizations to identify accident hotspots and duration trends.
* Developed a choropleth map showing year-wise accident counts by state for temporal-spatial trend analysis.

## Skills Demonstrated
* Large-scale data processing with chunking and efficient memory management.
* Advanced data cleaning and imputation strategies tailored to domain-specific data.
* Categorical standardization to improve data quality.
* Integration of geospatial data processing and visualization techniques.
* Insightful exploratory data analysis highlighting real-world traffic safety issues.

## Conclusion
This project showcases the importance of thorough data cleaning and domain-aware preprocessing to derive reliable and actionable insights from complex, large-scale datasets. It also highlights how data science can support traffic safety improvement initiatives through informed analysis and visualization.


