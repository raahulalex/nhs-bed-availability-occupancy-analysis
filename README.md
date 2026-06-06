# NHS Bed Availability and Occupancy Analysis (2025–2026)

## Project Overview

This project analyses NHS England overnight bed availability and occupancy data for the 2025–2026 financial year.

The project explores hospital capacity pressure across:

- NHS providers
- NHS regions
- bed sectors
- clinical specialties

It builds on my earlier NHS A&E Patient Flow Analysis project by examining wider inpatient capacity pressures that may contribute to patient-flow challenges across urgent and emergency care services.

## Tableau Dashboard

View the interactive Tableau story here:

**[NHS Bed Availability & Occupancy Analysis 2025–26](https://public.tableau.com/views/NHSBedAvailabilityOccupancyAnalysis202526/NHSBedAvailabilityOccupancyAnalysis?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)**

## Project Objectives

The objectives of this project were to:

1. Analyse national overnight bed availability and occupancy trends across 2025–26.
2. Compare regional variation in bed occupancy across NHS England regions.
3. Identify NHS providers with consistently high overnight bed occupancy.
4. Compare occupancy across key bed sectors including General & Acute, Mental Illness, Maternity and Learning Disabilities.
5. Analyse occupied bed use by clinical specialty.
6. Prepare clean, validated Tableau-ready datasets for interactive dashboarding.

## Dataset

The analysis uses publicly available NHS England KH03 Bed Availability and Occupancy data.

The project uses four quarterly overnight bed files for 2025–26:

- Q1: April to June 2025
- Q2: July to September 2025
- Q3: October to December 2025
- Q4: January to March 2026

The main sheets used were:

- NHS Trust by Sector
- Region by Sector
- Occupied by Specialty

## Tools Used

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook
- Tableau Public
- GitHub

## Data Cleaning and Validation

The original NHS Excel files required cleaning before analysis because they contained:

- metadata rows
- grouped column headers
- blank separator columns
- repeated header rows
- national summary rows mixed with provider-level data
- specialty data stored in wide format

Cleaning steps included:

- extracting the correct data rows from each quarterly file
- selecting the relevant available, occupied and occupancy columns
- standardising column names
- converting occupancy rates into percentage format
- removing repeated header rows
- separating England national summary rows from provider-level rows
- reshaping specialty data from wide to long format
- creating high occupancy flags and occupancy bands
- exporting clean CSV files for Tableau

Validation checks were performed by comparing cleaned values against the original Excel files. Available beds, occupied beds and occupancy rates were checked row by row to ensure that the cleaned provider-level data matched the raw NHS source data.

## Key Metrics

Key metrics analysed included:

- available overnight beds
- occupied overnight beds
- occupancy rate
- providers above 92% occupancy
- providers above 95% occupancy
- average occupancy by region
- average occupancy by bed sector
- total occupied beds by clinical specialty

## Key Findings

### 1. National occupancy remained high

At national level, overnight bed occupancy remained consistently high across 2025–26. Occupancy ranged from 88.9% in Q2 to 90.1% in Q4.

General & Acute occupancy was higher than total occupancy and reached 92.5% in Q4.

### 2. Capacity pressure varied by region

Regional analysis showed that bed occupancy pressure was not evenly distributed across NHS England.

The South West had the highest average total overnight occupancy and the highest General & Acute occupancy during 2025–26.

### 3. Provider-level pressure increased in Q4

The number of providers above 92% occupancy increased in Q4.

Providers above 92% occupancy by quarter:

- Q1: 53
- Q2: 50
- Q3: 48
- Q4: 59

Providers above 95% occupancy by quarter:

- Q1: 15
- Q2: 9
- Q3: 15
- Q4: 27

This suggests that high occupancy became more visible toward the end of the financial year.

### 4. Some providers had persistently high occupancy

A group of NHS providers were above 92% occupancy in all four quarters of 2025–26.

This indicates that some organisations had consistently limited spare overnight bed capacity across the year.

### 5. General & Acute beds showed the highest sector-level occupancy

General & Acute beds had the highest average occupancy among the bed sectors analysed.

This is important because General & Acute beds are most closely linked to urgent and emergency care admissions and wider hospital patient flow.

### 6. Occupied bed use was concentrated in key specialties

Specialty-level analysis showed that General Medicine and Geriatric Medicine accounted for the largest occupied overnight bed use.

This provides clinical context because these specialties are closely linked to acute inpatient demand, older adult care, emergency admissions and complex discharge planning.

## Tableau Dashboard Structure

The Tableau Public story includes four dashboard sections:

1. Provider Occupancy Overview
2. Regional Bed Occupancy Analysis
3. Sector Occupancy Analysis
4. Specialty-Level Occupied Bed Analysis

## Limitations

This analysis uses aggregated quarterly NHS provider-level data rather than patient-level data.

As a result:

- it cannot determine individual patient pathways
- it cannot prove a direct causal relationship between bed occupancy and A&E delays
- provider comparisons may be affected by hospital size, case mix, specialty mix and local service configuration
- occupancy does not fully capture staffing constraints, infection control restrictions, discharge delays or patient acuity
- specialty-level analysis focuses on occupied beds only and does not include available specialty-level bed capacity

## Conclusion

This project shows that NHS overnight bed occupancy remained high across 2025–26, with pressure varying across providers, regions, sectors and clinical specialties.

The findings suggest that capacity pressure was particularly visible in General & Acute beds and in specialties linked to acute and older adult inpatient care.

While the analysis does not prove a direct causal relationship with A&E delays, it provides important context for understanding wider patient-flow pressures across the hospital system.

## Future Work

Future work could extend this analysis by linking bed occupancy data with:

- discharge delay data
- urgent and emergency care SitRep data
- ambulance handover delays
- A&E waiting time performance
- workforce and staffing pressure indicators

This would allow a more complete analysis of patient-flow pressures across the urgent and emergency care system.
