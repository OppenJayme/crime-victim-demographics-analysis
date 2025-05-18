# Crime Incident Analysis in Los Angeles  
**Data Mining & Data Warehousing Project – IT 3107**

## Overview

This project explores crime incident data in Los Angeles by implementing a full ETL (Extract, Transform, Load) pipeline and generating insights through structured data analysis and visualizations. The goal is to answer key analytical questions related to area-based crime patterns, victim demographics, and trends from 2020 to 2024.

---

## Technologies Used

- **Python (Pandas)** – For data extraction, cleaning, transformation, and normalization  
- **SSIS (SQL Server Integration Services)** – For loading data into the data warehouse  
- **Microsoft SQL Server** – As the central data repository  
- **Plotly Express** – For statistical and comparative visualizations  
- **Folium** – For creating geospatial heatmaps  
- **Canvas** – For compiling dashboards and reports

---

## ETL Process

### Extract
Raw crime data was collected and ingested using Python.

### Transform
The data was cleaned, standardized, and normalized, including conversions for area names, gender, racial descent, and timestamps.

### Load
Transformed datasets were imported into SQL Server using SSIS workflows and properly indexed for efficient querying.

---

## Guide Questions and Analytical Approach

### Question 1  
**What are the top 5 crime-prone areas in Los Angeles?**  
We identified high-crime areas using frequency counts grouped by neighborhood and visualized the results with Folium heatmaps and bar charts.

### Question 2  
**For all areas, what is their crime distribution throughout the years?**  
We aggregated incident counts per area per year and visualized the trends using multi-line graphs to highlight annual fluctuations from 2020 to 2024.

### Question 3  
**In Los Angeles, which racial groups are most likely to be victims of reported crimes?**  
The data was grouped by racial descent and filtered per area. The resulting frequencies were presented using bar charts to highlight disparities.

### Question 4  
**What is the yearly trend in crime victimization by gender across various areas of Los Angeles from 2020 to 2024?**  
Gender-based victim data was analyzed across all years, with results plotted as time series comparisons across districts.

### Question 5  
**Which victim descent is the most affected in these 5 areas?**  
Using the top 5 areas from Question 1, we filtered records to identify the most frequently reported victim descent per area.

### Question 6  
**What is the average age for all age categories of victims belonging to the most affected descent in the most dangerous area?**  
Average age statistics were computed from the dataset after filtering by both area and descent to assess vulnerability among specific age groups.

---

## Sample Visualizations

- Folium heatmaps highlighting crime density across Los Angeles  
- Time series graphs of crime incidents by year, gender, and area  
- Comparative bar charts for racial and descent-based victim statistics  
- Aggregated averages for victim age in high-risk areas
