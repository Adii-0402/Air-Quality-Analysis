# Air Quality Analysis Dashboard | Power BI

An interactive Power BI dashboard exploring daily air-quality measurements across Indian cities. The report compares city-level Average AQI, visualizes AQI trends over time, summarizes selected pollutant measurements, and provides a map-based view.

## Dashboard Preview

### All Cities View

![Air Quality Dashboard - All Cities](Screenshots/dashboard-all-cities.png)

### Bhopal Filtered View

![Air Quality Dashboard - Bhopal](Screenshots/dashboard-bhopal-filter.png)

## Project Objectives

- Explore air-quality measurements across Indian cities.
- Compare Average AQI between cities.
- Examine how Average AQI changes over time.
- View selected pollutant averages and filter the report by city.
- Present city-level information through a map visualization.

## Dashboard Features

The Power BI report is a single-page dashboard containing 11 visual elements:

| Visual | Purpose |
|---|---|
| AQI Trend Overview (line chart) | Displays Average AQI over time using the date hierarchy. |
| City dropdown slicer | Filters the dashboard for a selected city. |
| Top 3 Cities by Average AQI (bar chart) | Compares the three highest cities by Average AQI. |
| Bottom 3 Cities by Average AQI (bar chart) | Compares the three lowest cities by Average AQI. |
| Average CO card | Displays the average CO value for the current filter selection. |
| Average NO card | Displays the average NO value for the current filter selection. |
| Average SO2 card | Displays the average SO2 value for the current filter selection. |
| Average PM2.5 card | Displays the average PM2.5 value for the current filter selection. |
| Area-wise AQI overview map | Shows city-level AQI information geographically. |
| Maximum Date card | Displays the maximum date in the report's current data context. |
| Report heading | Displays the report title. |

> **Dashboard label note:** The supplied screenshots still show the original chart titles “TOP 3 POLLUTANT CITY” and “LEAST POLLUTANT CITY”. The bar charts use **Average of AQI**, so the clearer titles recommended above are “Top 3 Cities by Average AQI” and “Bottom 3 Cities by Average AQI”. Update the titles in Power BI Desktop to match this documentation.

## Dataset

- **Dataset:** Air Quality Data in India — `city_day.csv`
- **Kaggle publisher:** Rohan Rao
- **Kaggle source:** [Air Quality Data in India — city_day.csv](https://www.kaggle.com/datasets/rohanrao/air-quality-data-in-india?select=city_day.csv)
- **Rows in the supplied CSV:** 29,531
- **Columns:** 16
- **Cities:** 26
- **Date coverage in the supplied CSV:** 1 January 2015 to 1 July 2020

The CSV contains daily city-level readings and AQI information. Its columns are:

`City`, `Date`, `PM2.5`, `PM10`, `NO`, `NO2`, `NOx`, `NH3`, `CO`, `SO2`, `O3`, `Benzene`, `Toluene`, `Xylene`, `AQI`, and `AQI_Bucket`.

The dataset is distributed through Kaggle. Please review the dataset's current licence and terms before committing a copy of the CSV to a public repository. If you do not include the CSV, keep the Kaggle link above and download `city_day.csv` from that page when setting up the report.

## Selected Dashboard Observations

The values below are transcribed from the supplied Power BI screenshots. They describe the displayed report and have not been independently recalculated from the underlying model.

### All Cities View

| Metric | Displayed value |
|---|---:|
| Average CO | 2.25 |
| Average NO | 17.57 |
| Average SO2 | 14.53 |
| Average PM2.5 | 67.45 |

**Three highest displayed Average AQI values:**

| City | Average AQI |
|---|---:|
| Ahmedabad | 452.12 |
| Delhi | 259.49 |
| Patna | 240.78 |

**Three lowest displayed Average AQI values:**

| City | Average AQI |
|---|---:|
| Aizawl | 34.77 |
| Coimbatore | 73.02 |
| Shillong | 53.80 |

*Note: The lower-chart values above are copied from the screenshot. The chart's displayed ordering is not a ranking order, so compare the numeric values rather than the row order.*

### Bhopal Filtered View

| Metric | Displayed value |
|---|---:|
| Average AQI | 132.83 |
| Average CO | 0.88 |
| Average NO | 7.04 |
| Average SO2 | 13.06 |
| Average PM2.5 | 50.06 |

The Bhopal-filtered line chart shows Average AQI declining from approximately 162 in 2019 to approximately 115 in 2020, based on the plotted points in the screenshot.

## Tools and Technologies

- Microsoft Power BI Desktop
- Power BI visualizations, slicers, and filters
- CSV dataset

## Repository Structure

```text
Air-Quality-Analysis/
├── AIR QUALITY TEST.pbix
├── README.md
├── .gitignore
├── city_day.csv                 # Optional; include only if licence permits
└── Screenshots/
    ├── dashboard-all-cities.png
    └── dashboard-bhopal-filter.png
```

## How to Open the Project

1. Download or clone this repository.
2. Open `AIR QUALITY TEST.pbix` in Microsoft Power BI Desktop.
3. If Power BI reports that the CSV source path cannot be found, use **Transform data** or **Data source settings** to point the query to your local `city_day.csv` file.
4. Apply the changes and select **Refresh** if required.
5. Use the City slicer to explore the report for individual cities, including Bhopal.

If the CSV is not included in the repository, download `city_day.csv` from the Kaggle source linked above before reconnecting the report.

## Notes and Limitations

- This project is a descriptive dashboard; it does not forecast future AQI.
- The displayed pollutant cards report averages for the current filter context.
- The screenshots are visual evidence of the report at the time they were captured. Values may differ if the data, filters, or Power BI calculations are changed.
- Missing values exist in the supplied dataset. This README does not claim that missing values were imputed or that the dataset was independently cleaned.
- AQI and pollutant measurements are presented for data exploration. This dashboard alone should not be treated as a health assessment or proof of the cause of pollution.

## Author

**Aditya Rathore**
