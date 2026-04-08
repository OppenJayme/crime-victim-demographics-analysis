# Crime Victim Demographics Analysis

An end-to-end crime analysis project built from Los Angeles crime incident data, focused on victim demographics, area-level crime concentration, and heatmap-based geographic exploration.

This cleaned project package was reconstructed from the original `crimeincidents` workspace. The main analysis notebook is [fact.ipynb](./notebooks/fact.ipynb), and the supporting dimension workbooks were selected from the exact files that notebook uses.

## Project Overview

This project combines data preparation, dimensional modeling, and exploratory analysis to answer questions about:

- which Los Angeles areas report the highest concentration of crime incidents
- how crime patterns vary across years
- which victim descent groups are most affected
- how victim demographics vary by area
- where unresolved incidents cluster geographically

The original work was done as an early data analysis and warehousing project using Pandas, SSIS, SQL Server, and map-based visualization tooling. This folder is the cleaned, portfolio-ready version of that work.

## Tech Stack

- Python
- Pandas
- Jupyter Notebook
- Folium
- Plotly
- Seaborn / Matplotlib
- SSIS
- Microsoft SQL Server

## Main Analysis

The canonical notebook is:

- [fact.ipynb](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\notebooks\fact.ipynb)

This notebook:

- loads the raw LAPD crime dataset
- joins the cleaned dimension workbooks
- constructs a fact table
- explores area-level and demographic trends
- exports HTML-based visualizations for geographic and comparative analysis

## Repository Structure

```text
crime-victim-demographics-analysis/
  data/
    raw/
      crimeData.csv
    dimensions/
      Area_Dim_with_Lat_Long.xlsx
      Crime_Type_Dim.xlsx
      Investigation_Stat_Dim.xlsx
      date_Final.xlsx
      location_dimrevised.xlsx
      premiseData.xlsx
      time_finalnajd.xlsx
      victimDimFinal.xlsx
  notebooks/
    fact.ipynb
  outputs/
    fact-table/
      fact_tableV3.xlsx
    visualizations/
      heatmaps/
      age-analysis/
  docs/
    selection-notes.md
```

## Data Assets

### Raw dataset

- `crimeData.csv` is used by the notebook but is not committed to the repository because the file exceeds GitHub's 100 MB limit.
- Place the dataset at `data/raw/crimeData.csv` before running the notebook.
- The original workspace source file was the LAPD crime incident dataset covering 2020 to present.

### Dimension workbooks used by the notebook

- [Area_Dim_with_Lat_Long.xlsx](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\data\dimensions\Area_Dim_with_Lat_Long.xlsx)
- [Crime_Type_Dim.xlsx](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\data\dimensions\Crime_Type_Dim.xlsx)
- [Investigation_Stat_Dim.xlsx](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\data\dimensions\Investigation_Stat_Dim.xlsx)
- [date_Final.xlsx](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\data\dimensions\date_Final.xlsx)
- [location_dimrevised.xlsx](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\data\dimensions\location_dimrevised.xlsx)
- [premiseData.xlsx](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\data\dimensions\premiseData.xlsx)
- [time_finalnajd.xlsx](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\data\dimensions\time_finalnajd.xlsx)
- [victimDimFinal.xlsx](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\data\dimensions\victimDimFinal.xlsx)

These were chosen from the versions referenced directly inside `fact.ipynb`. Where duplicates existed elsewhere in the original workspace, the copies under `fact table/` were treated as canonical because they matched the final notebook context.

## Fact Table Output

The latest final exported fact table found in the workspace is:

- [fact_tableV3.xlsx](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\outputs\fact-table\fact_tableV3.xlsx)

This workbook is preserved as the primary final tabular output of the project.

## Included Visual Outputs

### Core heatmaps

- [interactive_crime_heatmap.html](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\outputs\visualizations\heatmaps\interactive_crime_heatmap.html)
- [victim_descent_H_heatmap.html](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\outputs\visualizations\heatmaps\victim_descent_H_heatmap.html)
- [victim_descent_W_heatmap.html](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\outputs\visualizations\heatmaps\victim_descent_W_heatmap.html)
- [victim_descent_B_heatmap.html](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\outputs\visualizations\heatmaps\victim_descent_B_heatmap.html)
- [victim_descent_F_heatmap.html](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\outputs\visualizations\heatmaps\victim_descent_F_heatmap.html)

### Unresolved case heatmaps by year

- [unresolved_cases_heatmap_2020.html](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\outputs\visualizations\heatmaps\unresolved_cases_heatmap_2020.html)
- [unresolved_cases_heatmap_2021.html](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\outputs\visualizations\heatmaps\unresolved_cases_heatmap_2021.html)
- [unresolved_cases_heatmap_2022.html](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\outputs\visualizations\heatmaps\unresolved_cases_heatmap_2022.html)
- [unresolved_cases_heatmap_2023.html](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\outputs\visualizations\heatmaps\unresolved_cases_heatmap_2023.html)
- [unresolved_cases_heatmap_2024.html](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\outputs\visualizations\heatmaps\unresolved_cases_heatmap_2024.html)

### Age analysis exports

- [average_age_by_the_mostdangerous_area_descent_H.html](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\outputs\visualizations\age-analysis\average_age_by_the_mostdangerous_area_descent_H.html)
- [average_age_by_the_mostdangerous_area_descent_B.html](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\outputs\visualizations\age-analysis\average_age_by_the_mostdangerous_area_descent_B.html)

These were selected as the stable final exports and exclude obvious scratch or duplicate variants such as `Gwapo.html`, `interactiv_crime_heatmap.html`, and intermediate `V2` to `V7` files.

## Analytical Focus

The notebook and exported outputs support questions such as:

- What are the top crime-prone areas in Los Angeles?
- How does crime distribution change from 2020 to 2024?
- Which victim descent groups are most affected?
- How do gender and descent relate to spatial crime concentration?
- Where are unresolved incidents concentrated geographically?

## Notes On Cleanup

- The original workspace was highly iterative and contained many duplicate or partial files.
- This cleaned version keeps the final notebook, its required dimensions, the raw dataset, the latest fact table export, and the most meaningful final HTML outputs.
- Notebook file paths were updated so the project works with the new directory structure.

For file-selection details, see [selection-notes.md](d:\IVAN USC\Vs Code\Python\crimeincidents\crime-victim-demographics-analysis\docs\selection-notes.md).
