# Project Methodology

## 1. Project Approach

The Hospital Readmission Analytics Dashboard was developed using a structured approach, starting with raw healthcare encounter data and progressing through data preparation, modelling, DAX calculations, and interactive reporting.

The objective was to organize the data into meaningful categories and present readmission patterns through an interactive Power BI report.

## 2. Data Sources

The project uses two CSV files:

- `diabetic_data.csv`: Contains hospital encounter information, patient demographics, diagnoses, treatments, length of stay, and readmission outcomes.
- `IDS_mapping.csv`: Provides descriptions for coded admission and discharge-related fields.

## 3. Data Preparation

Data preparation was performed in Power Query.

The main activities included:

- Reviewing the source tables and their structures.
- Checking column names and data types.
- Reviewing missing and unmapped values.
- Using the mapping dataset to translate coded admission and discharge categories into readable descriptions.
- Creating grouped categories for admission type and admission source.
- Creating length-of-stay groups for easier comparison.
- Reviewing diagnosis-field completeness.
- Organizing the data for reporting and analysis.

Missing and unmapped categories were retained where appropriate rather than being automatically treated as meaningful business categories.

## 4. Data Modelling

The prepared encounter data was used as the main reporting table.

The mapping information was incorporated to provide readable descriptions for coded fields. The model was organized to support the dashboard's measures, visualizations, and report-level filtering.

## 5. DAX Calculations

DAX measures were developed to calculate:

- Total encounters.
- Unique patients.
- Any readmission encounters.
- Not-readmitted encounters.
- Any readmission rate.
- Eligible encounters.
- Eligible 30-day readmissions.
- Eligible 30-day readmission rate.

Calculated categories were also used to support analysis by length of stay, admission type, and admission source.

## 6. Dashboard Development

The report was organized into seven pages:

1. Hospital Readmission Dashboard
2. Executive Overview
3. Readmission Analysis
4. Demographic Analysis
5. Admission Source Analysis
6. Discharge Disposition Analysis
7. Discharge Disposition Summary

The visuals were selected to communicate encounter volumes, readmission patterns, demographic comparisons, and operational characteristics.

Gender and age-group slicers were synchronized across the report pages to support consistent filtering.

## 7. Validation and Review

The dashboard was reviewed by checking KPI results, comparing calculated results against the source categories, testing slicer interactions, and reviewing visual labels and formatting.

The baseline KPI values were checked with report filters reset.

Additional attention was given to missing and unmapped categories to avoid misleading interpretations.

## 8. Final Output

The completed project includes an interactive Power BI report, a project README, dashboard screenshots, and supporting documentation.

The report is designed to help users explore hospital encounter and readmission patterns through clearly defined measures and interactive visuals.
