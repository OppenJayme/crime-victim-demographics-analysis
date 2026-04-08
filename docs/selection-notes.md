# Selection Notes

`fact.ipynb` is treated as the canonical analysis notebook.

The following workbook names are loaded directly inside `fact.ipynb`:

- `victimDimFinal.xlsx`
- `date_Final.xlsx`
- `time_finalnajd.xlsx`
- `premiseData.xlsx`
- `Area_Dim_with_Lat_Long.xlsx`
- `Crime_Type_Dim.xlsx`
- `Investigation_Stat_Dim.xlsx`
- `location_dimrevised.xlsx`

Several of those files existed in multiple folders. The copied versions came from `fact table/` because that is where the final notebook lives and because some duplicates had different file hashes, which means they were not interchangeable.

## Output files kept

The cleaned folder also keeps the final exported artifacts that appear meaningful and non-duplicative:

- `fact_tableV3.xlsx` as the latest fact table export
- `interactive_crime_heatmap.html` as the final general crime heatmap
- `victim_descent_H_heatmap.html`
- `victim_descent_W_heatmap.html`
- `victim_descent_B_heatmap.html`
- `victim_descent_F_heatmap.html`
- yearly unresolved case heatmaps for 2020 to 2024
- final age-analysis HTML exports for descent `H` and `B`

The following were intentionally excluded from the cleaned package:

- obvious scratch or placeholder names such as `Gwapo.html`
- typo or near-duplicate variants such as `interactiv_crime_heatmap.html`
- iterative HTML versions such as `interactive_crime_heatmapV2` to `interactive_crime_heatmapV7`
- intermediate or superseded workbook variants not directly required by `fact.ipynb`
