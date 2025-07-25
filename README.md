# Wildfires, Air Quality & CO₂ Analysis (2020–2024)

## Project overview

This project investigates whether years with more wildfires in the United States correspond to worse ambient air quality and positions the findings within the broader context of increasing atmospheric carbon dioxide.  It showcases a data‑driven workflow that integrates multiple public data sources, cleans and summarizes them, visualizes trends and computes simple correlations.  The aim is to produce a job‑ready portfolio piece demonstrating skills in data acquisition, cleaning, analysis and communication.

## Data sources

| Source | Description | Citation |
|---|---|---|
| **National Interagency Fire Center (NIFC)** | Annual counts of wildland fires and acres burned were taken from the NIFC’s historical statistics table. The table lists, for each year since 1983, the number of fires and total acres burned【127707258858993†L308-L317】. | NIFC Table【127707258858993†L308-L317】 |
| **EPA AirData (pre‑generated files)** | The U.S. Environmental Protection Agency provides pre‑generated datasets of daily and annual air quality summaries. Annual AQI by county files for 2020–2024 were downloaded; each file contains the number of days in AQI categories (Good, Moderate, Unhealthy for Sensitive Groups, Unhealthy, Very Unhealthy and Hazardous) and pollutant counts for each county【295235041241295†L28-L66】【295235041241295†L114-L170】. | EPA AirData【295235041241295†L28-L66】【295235041241295†L114-L170】 |
| **NOAA Global Monitoring Laboratory** | Monthly mean atmospheric carbon dioxide concentrations at Mauna Loa were retrieved. The NOAA page offers the complete record and data files for the Mauna Loa CO₂ measurements【602935728654264†L137-L146】. Annual averages were computed for 2020–2024. | NOAA CO₂ Data【602935728654264†L137-L146】 |

## Repository structure

```
.
├── wildfire_air_quality_analysis.ipynb  # Main Jupyter notebook with narrative, code and embedded charts
├── README.md                            # Project summary and instructions (this file)
├── annual_aqi_by_county_2020.zip        # Raw air quality data (EPA)
├── annual_aqi_by_county_2021.zip        # "
├── annual_aqi_by_county_2022.zip        # "
├── annual_aqi_by_county_2023.zip        # "
├── annual_aqi_by_county_2024.zip        # "
├── co2_mm_mlo.csv                       # Atmospheric CO₂ monthly mean data (NOAA)
├── chart_wildfires.png                  # Generated plot showing wildfires (notebook attachment)
├── chart_air_quality.png                # Generated plot showing air quality metrics (attachment)
├── chart_co2.png                        # Generated plot showing CO₂ trend (attachment)
└── chart_correlation.png                # Generated scatter plot of AQI vs acres burned
```

## Getting started

1. **Clone or download the repository.**  Ensure that the ZIP files and CSV file listed above remain in the project directory.
2. **Install dependencies.**  You will need Python ≥3.8 with `pandas` and `matplotlib` installed.  If you wish to execute the notebook, other dependencies (e.g., `zipfile`, `nbformat`) are part of Python’s standard library or preinstalled.

   ```bash
   pip install pandas matplotlib
   ```

3. **Run the notebook.**  Open `wildfire_air_quality_analysis.ipynb` in Jupyter Notebook or JupyterLab.  Execute the cells sequentially to reproduce the analysis.  The charts are already embedded as attachments, but running the plotting code will regenerate them.

4. **Explore the data.**  The code demonstrates how to load each year’s air quality data from a ZIP archive, aggregate metrics, merge with wildfire statistics and compute correlations.

## Key results

* **Wildfires:** 2020 had the highest acreage burned (~10 million acres) and 2022 had the highest number of fires, while 2023 experienced a sharp decline in acreage burned.
* **Air quality:** The weighted median AQI was highest in 2023 (~42), despite relatively low wildfire acreage.  The number of unhealthy days declined from 2020 to 2022, then increased again in 2023.
* **Correlation:** With only five data points, correlations are exploratory.  Acres burned show a negative correlation with the weighted median AQI, suggesting that years with larger fires did not necessarily have worse national‑scale air quality.  Other factors—such as meteorological conditions, smoke dispersion and non‑wildfire emissions—likely influence the results.
* **CO₂ trend:** The Mauna Loa record shows a steady rise in atmospheric CO₂ from ~414 ppm in 2020 to >424 ppm in 2024, contextualizing wildfire activity within a warming climate.

## Discussion

The project demonstrates how to combine diverse environmental datasets to address a real‑world question.  While simple correlations suggest that years with more acres burned do not necessarily coincide with worse national air quality, the small sample size and aggregated nature of the data limit causal interpretations.  Additional analyses at regional scales, incorporating meteorological variables and smoke dispersion models, would provide deeper insights.  The persistent upward trend in atmospheric CO₂ reminds us that wildfires are occurring in a climate system that is continually warming, underscoring the importance of both mitigation and adaptation strategies.

## License

This project is released under the [MIT License](https://opensource.org/licenses/MIT).  You are free to reuse the code and materials with attribution.

## Skip to wildfire_air_quality-analysis.ipynb for the analysis in one section
