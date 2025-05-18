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

## Key Findings

- **Top Crime Areas:**  
  The five most crime-prone areas in Los Angeles are **Central**, **77th Street**, **Pacific**, **Southwest**, and **Hollywood**, with Central reporting over 60,000 incidents.

- **Yearly Crime Distribution:**  
  Most areas experienced a peak in crime during **2022**, with gradual changes observed in 2023. Distribution varies slightly across districts, but general trends remain consistent.

- **Victim Racial Group Analysis:**  
  - **Hispanic** individuals accounted for **34.8%** of reported incidents.  
  - **White** individuals made up **23.3%**, followed by **Black** individuals at **16%**.  
  - Other groups showed smaller but significant presence depending on the district.

- **Gender-Based Victimization Trends (2020–2024):**  
  - **Male** victims consistently had the highest counts each year.  
  - **Female** victimization followed similar patterns but in slightly lower volumes.  
  - **Non-Binary** individuals were also represented, particularly in Central and Wilshire.

- **Most Affected Group and Area:**  
  The most affected group was **Hispanic descent in Central Los Angeles**, based on incident concentration.

- **Victim Age Statistics:**  
  The **average age** for victims in the most affected descent and area is **approximately 31.5 years**, with most incidents occurring in the **19–29** and **30–44** age ranges.

- **Bonus Insight – Common Crime Types by Descent:**  
  - **Hispanic:**  
    - Battery – Simple Assault: 37,460  
    - Assault with a Deadly Weapon / Aggravated Assault: 26,495  
    - Intimate Partner Assault: 24,650  
  - **White:**  
    - Burglary from Vehicle: 19,321  
    - Burglary: 17,634
    - Theft of Identity: 16,881 
  - **Black:**  
    - Battery – Simple Assault: 14,631
    - Aggravated Assault: 14,387  
    - Theft of Identity: 13,481

