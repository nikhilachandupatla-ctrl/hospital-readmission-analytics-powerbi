# Hospital Readmission Analytics Dashboard | Power BI

## Project Overview

This project uses Microsoft Power BI to analyze hospital encounter data and explore readmission patterns, patient demographics, length of hospital stay, admission sources, and discharge dispositions.

The dashboard transforms hospital encounter data into interactive visual reports, helping users understand patterns in hospital utilization and readmissions.

## Business Objective

Hospital readmissions are an important metric in healthcare analytics. This project explores encounter-level data to:

- Understand overall hospital encounter volumes and readmission patterns.
- Analyze readmissions across admission types and admission sources.
- Explore demographic patterns by age group and gender.
- Examine length of stay and discharge disposition.
- Compare overall readmission rates with eligible 30-day readmission rates.

The analysis is descriptive and is intended for data exploration and reporting, not clinical decision-making.

## Dashboard Pages

The Power BI report contains seven interactive pages:

1. **Hospital Readmission Dashboard** – Provides an overall view of hospital encounters and key performance indicators, with interactive filters and charts covering age groups, gender, admission type, and length-of-stay groups. It includes encounter volumes, overall readmission rates, and eligible 30-day readmission rates.

2. **Executive Overview** – Presents the main KPIs and high-level summaries of encounter volumes and readmissions.

3. **Readmission Analysis** – Examines readmission patterns across admission types.

4. **Demographic Analysis** – Explores encounter volumes and readmission rates by age group and gender.

5. **Admission Source Analysis** – Analyzes hospital encounters and readmission rates by admission source.

6. **Discharge Disposition Analysis** – Examines encounter volumes and readmission patterns across discharge dispositions.

7. **Discharge Disposition Summary** – Provides a tabular summary of encounter volumes and readmission measures by discharge disposition.

## Key Performance Indicators

The following figures represent the overall dashboard totals with the report slicers cleared.

| KPI | Value |
|---|---:|
| Total Encounters | 101,766 |
| Unique Patients | 71,518 |
| Any Readmission Encounters | 46,902 |
| Not Readmitted Encounters | 54,864 |
| Any Readmission Rate | 46.1% |
| Eligible Encounters | 99,343 |
| Eligible 30-Day Readmissions | 11,314 |
| 30-Day Readmission Rate (Eligible) | 11.4% |

### Understanding the Readmission Measures

**Any Readmission Rate**

Measures the percentage of encounters with a recorded readmission, including both readmissions within 30 days (`<30`) and readmissions after 30 days (`>30`).

**30-Day Readmission Rate (Eligible)**

Measures readmissions within 30 days (`<30`) among encounters classified as eligible based on discharge disposition.

These measures use different definitions and denominators, so they should be interpreted separately.

**Important note:** Any Readmission Rate includes all encounters. The 30-Day Readmission Rate (Eligible) excludes encounters classified as ineligible based on discharge disposition.

## Business Insights

The dashboard provides the following observations from the hospital encounter data:

1. **Overall Readmissions:** Approximately 46.1% of recorded encounters had a readmission, including readmissions within and after 30 days.

2. **30-Day Readmissions:** The eligible 30-day readmission rate was approximately 11.4%, calculated using eligible encounters as the denominator.

3. **Length of Stay:** The dashboard compares encounter volumes and readmission rates across three length-of-stay groups: 1–3 days, 4–7 days, and 8+ days.

4. **Patient Demographics:** Users can compare encounter volumes and readmission rates across age groups and gender.

5. **Admission Patterns:** The report explores differences in encounter volumes and readmission rates across admission types and admission sources.

6. **Discharge Patterns:** Discharge disposition analysis provides a breakdown of encounter volumes and readmission measures across discharge categories.

These findings are descriptive observations from the available dataset. They do not establish causal relationships or explain why readmissions occur.

## Data Preparation and Transformation

Data preparation was performed using Power Query and Power BI.

Key activities included:

- Reviewing the source data and identifying data quality considerations.
- Cleaning and preparing columns for analysis.
- Using mapping tables to create readable admission source, admission type, and discharge disposition categories.
- Creating age categories and length-of-stay groups.
- Classifying encounters as eligible or ineligible for the eligible 30-day readmission analysis.
- Organizing fields and measures for reporting and visualization.

## Tools and Technologies

- **Microsoft Power BI Desktop** – Dashboard development and data visualization.
- **Power Query** – Data cleaning and transformation.
- **DAX** – Calculated columns and measures.
- **CSV files** – Source data and mapping information.
- **GitHub** – Project version control and portfolio presentation.

## Interactive Features

- Gender and Age Group slicers are available on the main dashboard page.
- Slicer selections are synchronized across the report pages.
- Charts and tables respond to the selected filters.
- KPI cards and visual summaries update dynamically based on filter selections.

## Data Interpretation and Reporting Considerations

- Encounters with no recorded readmissions are displayed with zero for the relevant overall readmission count and rate.
- The eligible 30-day readmission rate remains blank when there are no eligible encounters in the selected category, because a rate cannot be calculated with a zero denominator.
- Readmission rates are descriptive measures and should be interpreted within the definitions and limitations of the dataset.

## Limitations

- The analysis is based on the available hospital encounter dataset and its recorded variables.
- Results describe patterns in the data and do not establish causal relationships.
- The dashboard is intended for learning, portfolio demonstration, and exploratory analysis.
- It is not a clinical decision-support tool and should not be used to make patient-care decisions.

## Future Improvements

Potential enhancements include:

- Adding more detailed time-based analysis if suitable date information is available.
- Exploring additional patient and encounter characteristics.
- Incorporating further data quality checks and validation.
- Extending the analysis with SQL or Python.

## Repository Structure

The repository is organized to make the project files easy to locate.

```text
hospital-readmission-powerbi/
│
├── README.md
├── Hospital_Readmission_Analytics_Dashboard.pbix
│
├── 01_Raw_Data/
│   ├── diabetic_data.csv
│   └── IDS_mapping.csv
│
└── 02_Screenshots/
    ├── 01_Hospital_Readmission_Dashboard.png
    ├── 02_Executive_Overview.png
    ├── 03_Readmission_Analysis.png
    ├── 04_Demographic_Analysis.png
    ├── 05_Admission_Source_Analysis.png
    ├── 06_Discharge_Disposition_Analysis.png
    └── 07_Discharge_Disposition_Summary.png
```

*Note: Adjust the folder and file names above to match the actual names in your GitHub repository. Before publishing source data, check that you have permission to redistribute it.*

## How to Explore the Dashboard

1. Clone or download this repository.
2. Open `Hospital_Readmission_Analytics_Dashboard.pbix` using Power BI Desktop.
3. Navigate through the seven report pages.
4. Use the Gender and Age Group slicers on the main dashboard page to explore different segments.
5. Select charts and categories to explore the interactive report.

## Author

**Nikhila Chandupatla**

Aspiring Data Analyst | Healthcare Analytics | Power BI | SQL | SAS | Python

[GitHub Profile](https://github.com/nikhilachandupatla-ctrl)
