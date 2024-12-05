# Data Schemas

## CDC Compressed Mortality File (CMF)

| Column Name         | Data Type           | Description                                                                                   |
|---------------------|---------------------|-----------------------------------------------------------------------------------------------|
| Notes               | string (nullable)   | Additional notes or comments on the data entry (may include flags for reliability or missing data). |
| Age Group           | string              | The age group of individuals (e.g., < 1 year, 85+ years).                                      |
| Age Group Code      | string              | A code representing the age group (e.g., 1 for < 1 year, 85+ for 85+ years).                   |
| Race                | string              | The racial category of the individual (e.g., Black or African American, White).                |
| Race Code           | string              | A standardized race code (e.g., 2054-5 for Black or African American).                         |
| Gender              | string              | The gender of the individual (e.g., Male, Female).                                             |
| Gender Code         | string              | A code representing gender (e.g., F for Female, M for Male).                                   |
| Cause of Death      | string              | The specific cause of death (e.g., Pneumonia, organism unspecified).                           |
| Cause of Death Code | string              | A standardized code for the cause of death (e.g., ICD codes).                                  |
| Year                | integer             | The year in which the death occurred.                                                          |
| Deaths              | integer             | The total number of deaths recorded for the category.                                          |
| Population          | integer             | The total population corresponding to the category (age, race, gender).                        |
| Crude Rate          | string              | The crude mortality rate per 100,000 population (may include notes such as Unreliable).        |
| Standard Error      | float (nullable)    | The standard error for the crude rate, indicating variability in the rate calculation.         |
| Percent of Total    | string              | The percentage of total deaths attributed to the cause within the dataset (e.g., 0.0%).        |
