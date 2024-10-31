# Wildfire Analysis Project

This repository provides tools and analysis code to examine the impact of wildfires on air quality, focusing on historical data and projecting future smoke impacts on urban areas. The primary focus is on Birmingham, Alabama, analyzing its air quality in relation to nearby wildfires. The main analysis is within the `common-analysis` folder, which includes Jupyter notebooks and data processing scripts.

## Table of Contents

- [Wildfire Analysis Project](#wildfire-analysis-project)
  - [Table of Contents](#table-of-contents)
  - [Project Overview](#project-overview)
  - [Folder Structure](#folder-structure)
    - [common-analysis](#common-analysis)
  - [Data Sources](#data-sources)
  - [License](#license)
  - [Acknowledgements](#acknowledgements)

## Project Overview

The analysis in this repository:
1. Processes and cleans historical wildfire and air quality data.
2. Calculates a custom **Yearly Smoke Index** for Birmingham to estimate smoke impact.
3. Correlates the Smoke Index with actual Air Quality Index (AQI) data to validate the model.
4. Projects future wildfire smoke impact using time series forecasting.

The project demonstrates the integration of geospatial data with time-series air quality data, providing a reproducible workflow for wildfire smoke analysis.

## Folder Structure

### [common-analysis](common-analysis/)
The main analysis folder, containing Jupyter notebooks and log files.

- **[aqi_data_request.ipynb](common-analysis/aqi_data_request.ipynb)**: Requests air quality index (AQI) data from relevant sources.
- **[common-analysis.ipynb](common-analysis/common-analysis.ipynb)**: Main notebook for loading, processing, and analyzing wildfire data to estimate smoke impact.

## Data Sources

- **Combined Wildfire Dataset**: Published by the U.S. Geological Survey, this dataset contains wildfire data dating from the 1800s to the present, used to estimate smoke impact on Birmingham.
  - **Citation**: Welty, J.L., and Jeffries, M.I., 2021, Combined wildland fire datasets for the United States and certain territories, 1800s-Present: U.S. Geological Survey data release, https://doi.org/10.5066/P9ZXGFY3.

- **EPA Air Quality Data**: Used for correlating smoke impact with historical AQI data, enhancing model validation and accuracy https://aqs.epa.gov/aqsweb/documents/data_api.html#daily

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgements

This project was developed with data science code examples and guidance from:
- Dr. David W. McDonald: As part of DATA 512, a course in the UW MS Data Science degree program.