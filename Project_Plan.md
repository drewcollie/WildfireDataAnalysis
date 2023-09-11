---

# **PROJECT PLAN - WILDFIRE DATA ANALYSIS**

---

## **OBJECTIVE:**
The primary objective of this analysis is to understand the factors contributing to wildfires, their distribution, frequency, and the conditions under which they are most prevalent. By the end of this analysis, I hope to provide stakeholders with insights that can guide preventive measures, resource allocation, and public awareness campaigns.

## **PURPOSE OVERARCHING QUESTION, HYPOTHESIS OR PROBLEM STATEMENT:**

- **Purpose**: 
  - To analyze the characteristics of wildfires, discern patterns, and understand their primary causes.
- **Question**: 
  - What are the primary causes of wildfires in the given regions, and how do factors like time of year, geographical location, and land ownership influence their occurrence and magnitude?
- **Benefit to Business/Organization**: 
  - This analysis will aid forest management agencies, policymakers, and local communities in understanding wildfire trends, leading to better preparedness and prevention strategies.
- **Desired Outcomes**: 
  - To identify the top causes of wildfires, regions most affected, peak times of the year for wildfires, and the correlation between land ownership and fire incidence.

## **DATA PRIMARY AND SECONDARY SOURCES TO SUPPORT YOUR ANALYSIS:**

- **Primary Dataset**: 
  - Wildfire dataset.
- **Source**: 
  - "US Forest Service Database (URL: https://www.fs.usda.gov/rds/archive/catalog/RDS-2013-0009.6)"
- **Story of One Row's Value**: 
  - Each row provides comprehensive details on individual fire events, allowing for analysis from various perspectives - cause, location, time, magnitude, etc.
- **Key Columns for Analysis**: 
  - `FIRE_YEAR`, `STAT_CAUSE_DESCR`, `FIRE_SIZE`, `FIRE_SIZE_CLASS`, `LATITUDE`, `LONGITUDE`, `OWNER_DESCR`, `STATE`, `COUNTY`, `DISCOVERY_DATE`.
- **Dataset Attributes**:
  - **Size**: (2303566, 39)
  - **Range**: From 1992 to 2020
  - **Descriptive Statistics**: 
      - "Most Common Defined Cause Counts: Debris and open burning 535851, Natural 327319, Arson/incendiarism 320814", 
      - "Average Fire Size Grouped by Cause shows the largest fires are caused by: Natural 322.733929 ACRES, Firearms and explosives 237.010874 ACRES, Power generation/transmission/distribution 107.500738 ACRES"
      - "Most Common Cause: Missing data/not specified/undetermined 597933"
- **Secondary Data**: 
  - Weather patterns, population density, and land use changes can be sourced to add depth to the analysis.
- **Data Dictionary**: 

## Data Dictionary for "Fires" Table

| Column                        | Description                                                       | Dtype  |
|-------------------------------|-------------------------------------------------------------------|-------|
| OBJECTID                      | Unique identifier for each record                                 | int64 |
| Shape                         | Binary data for the shape of the fire incident on a map           | object|
| FOD_ID                        | Fire Occurrence Database Identifier                               | int64 |
| FPA_ID                        | Fire Program Analysis Identifier                                  | object|
| SOURCE_SYSTEM_TYPE            | Type of source system from which the data was sourced             | object|
| SOURCE_SYSTEM                 | Specific system from which the data originated                    | object|
| NWCG_REPORTING_AGENCY         | Reporting agency based on National Wildfire Coordinating Group    | object|
| NWCG_REPORTING_UNIT_ID        | ID for the reporting unit based on NWCG standards                 | object|
| NWCG_REPORTING_UNIT_NAME      | Name of the reporting unit based on NWCG standards                | object|
| SOURCE_REPORTING_UNIT         | Source's own ID for the reporting unit                            | object|
| SOURCE_REPORTING_UNIT_NAME    | Name given by the source for the reporting unit                   | object|
| LOCAL_FIRE_REPORT_ID          | Local ID for the fire report                                      | object|
| LOCAL_INCIDENT_ID             | Local ID for the fire incident                                    | object|
| FIRE_CODE                     | Code assigned to the fire incident                                | object|
| FIRE_NAME                     | Name assigned to the fire incident                                | object|
| ICS_209_PLUS_INCIDENT_JOIN_ID | ID for joining with ICS 209+ incident data                        | object|
| ICS_209_PLUS_COMPLEX_JOIN_ID  | ID for joining with ICS 209+ complex data                         | object|
| MTBS_ID                       | Monitoring Trends in Burn Severity ID                             | object|
| MTBS_FIRE_NAME                | Name assigned based on Monitoring Trends in Burn Severity         | object|
| COMPLEX_NAME                  | Name of the complex if fire is part of one                        | object|
| FIRE_YEAR                     | Year when the fire was reported                                   | int64 |
| DISCOVERY_DATE                | Date when the fire was discovered                                 | object|
| DISCOVERY_DOY                 | Day of year when the fire was discovered                          | int64 |
| DISCOVERY_TIME                | Time of day when the fire was discovered                          | object|
| NWCG_CAUSE_CLASSIFICATION     | Classification of the fire's cause based on NWCG                  | object|
| NWCG_GENERAL_CAUSE            | General cause of the fire based on NWCG                           | object|
| NWCG_CAUSE_AGE_CATEGORY       | Age category related to the cause based on NWCG                   | object|
| CONT_DATE                     | Date when the fire was contained                                  | object|
| CONT_DOY                      | Day of year when the fire was contained                           | int64 |
| CONT_TIME                     | Time of day when the fire was contained                           | object|
| FIRE_SIZE                     | Size of the fire in acres                                         | float64|
| FIRE_SIZE_CLASS               | Class category based on the fire size                             | object|
| LATITUDE                      | Latitude coordinate of the fire's location                        | float64|
| LONGITUDE                     | Longitude coordinate of the fire's location                       | float64|
| OWNER_DESCR                   | Description of the land's ownership                               | object|
| STATE                         | U.S. State where the fire occurred                                | object|
| COUNTY                        | County where the fire occurred                                    | object|
| FIPS_CODE                     | Federal Information Processing Standards code for the county      | object|
| FIPS_NAME                     | Name associated with the FIPS code                                | object|


## **ANALYSIS DATA DRIVEN INSIGHTS:**

- **KPIs**:
  - Total number of wildfires per year.
  - Distribution of fire causes.
  - Average fire size and its distribution.
  - Number of wildfires by land ownership type.
  - Geographical heatmap of fire occurrences.
- **Starting Questions**:
  - Which years had the highest number of wildfires?
  - What are the top causes of wildfires?
  - How does fire size vary with its cause?
  - Are certain land ownership types more prone to wildfires?
  - How does the frequency of wildfires vary across states and counties?
- **Observation Process**: 
  - Begin with a general overview, move to specific trends, and then derive correlations and potential causative factors.
- **Additional Calculations**: 
  - Seasonality index to determine peak fire months, correlation coefficients between fire size and other factors.
- **Models/Scenarios**: 
  - Regression models to predict fire sizes based on factors like cause, location, and time of year. "What if" scenarios to model potential changes in frequency or size under changing conditions.
- **Confirmation Methods**: 
  - Statistical tests to confirm significance, cross-validation for predictive models.
- **Limitations & Assumptions**: 
  - Data is limited to the range provided and may not represent future trends.
  - External factors like policy changes, global climate events, or major infrastructural developments aren't accounted for directly in the dataset.

---