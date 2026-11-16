# Exploratory Data Analysis of St. Petersburg Real Estate Market

## Project Description
Exploratory data analysis of Yandex Real Estate listings — an archive of apartment sale listings in St. Petersburg and Leningrad Oblast (~23,700 listings).

Goal — identify key factors affecting property prices and determine parameters for building an automated anomaly detection system for listings.

## Data
- **Source:** Yandex Real Estate
- **Coverage:** St. Petersburg and Leningrad Oblast, multiple years
- **Size:** ~23,700 listings, 22 features
- **Data types:** user input + automated geodata

## Workflow
- Initial data analysis: missing values, types, anomalies
- Preprocessing: filling missing values, type conversion, duplicate removal
- Feature engineering: price per m², floor type, time-based features
- Distribution analysis and outlier detection with threshold justification
- Correlation analysis (Pearson coefficient)
- Analysis of 7 factors affecting price: area, floor, number of rooms, listing date, location
- Price per m² comparison across 10 largest localities in the dataset
- Price dependency on distance from St. Petersburg city center

## Key Findings
- **Area** — the strongest price predictor: total_area (r=0.67), living_area (r=0.59), kitchen_area (r=0.50)
- **Floor:** ground floor is consistently cheaper than average, top floor — mid-range
- **Location:** price per m² in St. Petersburg is the highest in the dataset; clear negative correlation with distance from city center
- **Time to sell:** median listing duration — 95 days; listings significantly exceeding the median are candidates for review
- **Priority features for modeling:** `total_area`, `living_area`, `rooms`, `cityCenters_nearest`, `floor_type`

## Tech Stack
![Python](https://img.shields.io/badge/Python-3.x-blue)
![Pandas](https://img.shields.io/badge/Pandas-grey)
![Matplotlib](https://img.shields.io/badge/Matplotlib-grey)

## Repository Structure
```
├── spb_real_estate_eda.ipynb   # main notebook
└── README.md
```
