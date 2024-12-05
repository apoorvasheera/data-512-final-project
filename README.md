# Wildfire Smoke and Respiratory Mortality Analysis

This repository provides tools and analysis code to examine the impact of wildfires on air quality and respiratory health outcomes. The project focuses on Birmingham, Alabama, exploring historical wildfire and air quality data, as well as its correlation with respiratory disease mortality. The analysis includes forecasting future smoke exposure and its associated health risks.

## Table of Contents
- [Wildfire Smoke and Respiratory Mortality Analysis](#wildfire-smoke-and-respiratory-mortality-analysis)
  - [Table of Contents](#table-of-contents)
  - [Project Overview](#project-overview)
  - [Folder Structure](#folder-structure)
    - [common-analysis](#common-analysis)
    - [respiratory-diseases](#respiratory-diseases)
  - [Data Sources](#data-sources)
  - [Adopted Models](#adopted-models)
  - [Intermediate Data Files](#intermediate-data-files)
  - [License](#license)
  - [Acknowledgements](#acknowledgements)

## Project Overview

This project aims to:

- Process and clean historical wildfire and air quality data to estimate smoke impacts on Birmingham.
- Develop a Smoke Index to quantify the impact of nearby wildfires.
- Perform a mortality analysis, linking smoke exposure to respiratory disease mortality using CDC data.
- Forecast future trends in smoke exposure and respiratory mortality using Meta's Prophet model.
- Investigate demographic disparities, identifying gender-specific impacts of smoke on mortality.

## Folder Structure

### common-analysis
This folder contains the foundational wildfire and air quality analysis.

- **aqi_data_request.ipynb**: Retrieves and processes historical AQI data.
- **common-analysis.ipynb**: Main notebook for calculating the Smoke Index and validating it against AQI data.

### respiratory-diseases
This folder contains the mortality analysis linking smoke exposure to respiratory health.

- **data-request**: Contains screenshots of query used to download CDC data
- **smoke-mortality-analysis.ipynb**: Examines the relationship between wildfire smoke and respiratory mortality. It includes:
  - Forecasting respiratory mortality trends using the projected Smoke Index.
  -  Development of a gender-specific analysis for mortality.

## Data Sources

- **Wildfire Dataset**: Published by the U.S. Geological Survey, this dataset includes wildfire data from the 1800s to the present, used to calculate the Smoke Index.  
  *Citation*: Welty, J.L., and Jeffries, M.I., 2021, Combined wildland fire datasets for the United States and certain territories, 1800s-Present: U.S. Geological Survey data release, [https://doi.org/10.5066/P9ZXGFY3](https://doi.org/10.5066/P9ZXGFY3).

- **Air Quality Data**: Historical AQI data from the EPA for validating the Smoke Index.  
  *Link*: [EPA Air Quality Data](https://www.epa.gov/outdoor-air-quality-data)

- **CDC Compressed Mortality File (CMF)**: Respiratory mortality data from Jefferson County, Alabama, used for health impact analysis.  
  *Link*: [CDC WONDER Mortality Data](https://wonder.cdc.gov/)

## Adopted Models

- **Meta’s Prophet Model**: Used for time-series forecasting of the Smoke Index and respiratory mortality. Prophet was chosen for its flexibility in handling missing data and incorporating external regressors.  
  *Citation*: Taylor, S.J., & Letham, B. (2018). Forecasting at scale. The American Statistician, 72(1), 37-45. [Link](https://doi.org/10.1080/00031305.2018.1461947)

## Intermediate Data Files

- **gdf_analysis.geojson**: Processed wildfire data is a geo data frame 
- **particulate_aqi_data.csv**: Particulate AQI data from USGS API
- **yearly_smoke_index.csv**: Contains annual Smoke Index values for Birmingham, derived from wildfire data.
- **year_smoke_index_forecast.csv**: Projected Smoke Index for Birmingham through 2050.


## License

This project is licensed under the MIT License. See the LICENSE file for more details.

## Acknowledgements

This project was developed with the guidance and support of:

- Dr. David W. McDonald and the DATA 512 course at the University of Washington.
- Open data providers, including the USGS, EPA, and CDC, whose datasets form the backbone of this analysis.

