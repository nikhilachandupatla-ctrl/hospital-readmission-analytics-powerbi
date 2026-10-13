# Hospital Readmission Analytics Dashboard | Power BI

## Project Overview

This project analyzes hospital encounter data using Microsoft Power BI to explore readmission patterns, patient demographics, length of hospital stay, and hospital admission and discharge characteristics.

The objective is to transform healthcare data into an interactive dashboard that helps users understand key metrics and explore patterns across different patient and encounter groups.

## Business Problem

Hospital readmissions are an important area of healthcare analytics. Understanding encounter patterns and differences across patient groups can help identify areas for further investigation.

This project explores the following business questions:

- How many hospital encounters and unique patients are represented in the dataset?
- What proportion of encounters is classified as readmitted?
- How do readmission patterns vary across length-of-stay groups?
- How do readmission patterns differ by age, gender, and admission type?
- What insights can be explored from admission sources and discharge dispositions?

## Tools and Technologies

- **Microsoft Power BI Desktop** – Dashboard development and interactive visualizations
- **Power Query** – Data cleaning, profiling, and transformation
- **DAX** – KPI calculations and analytical measures
- **Data Modeling** – Organizing data and supporting lookup tables
- **GitHub** – Project documentation and portfolio presentation

## Project Workflow

1. Explored the dataset structure and reviewed column quality.
2. Examined missing values and important categorical variables.
3. Cleaned and transformed data using Power Query.
4. Prepared mapping tables for admission type, admission source, and discharge disposition.
5. Created DAX measures for encounter counts, unique patients, and readmission metrics.
6. Developed interactive dashboard pages with charts, KPI cards, and slicers.
7. Reviewed report navigation, formatting, and analytical calculations.

## Dashboard Pages

### 1. Executive Overview
Summarizes total encounters, unique patients, readmitted encounters, non-readmitted encounters, and the recorded readmission rate.

### 2. Readmission Analysis
Explores readmission patterns by length of stay and admission type, including the analysis of 30-day readmission where supported by the measure definition.

### 3. Demographics
Explores encounter patterns across demographic groups, including age and gender.

### 4. Hospital Operations
Examines operational characteristics, including length of stay, admission information, and discharge disposition.

## Key Performance Indicators

The following are the currently recorded results from the project. They should be confirmed against the final report before publication.

| Metric | Recorded Value |
|---|---:|
| Total Encounters | 101,766 |
| Unique Patients | 71,518 |
| Readmitted Encounters | 46,902 |
| Not-Readmitted Encounters | 54,864 |
| Recorded Readmission Rate | 46.09% |

The readmission rate depends on the classification and denominator used in the Power BI measure. It should not automatically be interpreted as a 30-day readmission rate.

## Dashboard Screenshots

Screenshots of the completed dashboard pages will be added here after final report validation.

## Data Quality and Limitations

- Some variables contain substantial missing data, including weight and diagnosis fields.
- The analysis depends on the quality and definitions of the available dataset fields.
- The original dataset distinguishes between readmission categories, including `NO`, `>30`, and `<30`. These categories must be interpreted correctly when defining readmission measures.
- The analysis is descriptive and does not establish causal relationships.
- The dashboard is intended for learning and portfolio demonstration, not clinical decision-making.

## Key Learnings

- Data profiling and transformation using Power Query.
- Creating and validating DAX measures.
- Distinguishing encounter counts from unique patient counts.
- Developing interactive Power BI dashboards.
- Presenting healthcare data through business-focused visualizations.

## Future Improvements

- Complete and document additional validation checks.
- Refine readmission definitions and calculation documentation.
- Enhance dashboard accessibility and usability.
- Explore additional trends supported by the dataset.

## How to View the Project

1. Review the dashboard screenshots in this repository.
2. Download the Power BI `.pbix` file.
3. Open it using Microsoft Power BI Desktop.
4. Explore the dashboard pages and interact with the available slicers.

## Author

**Nikhila Chandupatla**

Aspiring Data Analyst | Healthcare Analytics | Power BI | SQL | SAS | Python

GitHub: [nikhilachandupatla-ctrl](https://github.com/nikhilachandupatla-ctrl)
