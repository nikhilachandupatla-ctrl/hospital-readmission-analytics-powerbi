# Project Methodology

## 1. Project Objective

The objective of this project is to analyze hospital encounter data and build an interactive Power BI dashboard exploring readmission patterns, patient demographics, length of stay, and hospital admission and discharge characteristics.

## 2. Data Understanding

The project uses the `diabetic_data` table. The initial analysis focuses on understanding the data structure, field definitions, data types, category values, and missing information.

The analysis distinguishes hospital encounters from unique patients because one patient may have multiple encounters.

## 3. Data Profiling and Cleaning

Power Query was used to examine column quality, completeness, and categorical values and to prepare the data for analysis.

Initial profiling identified substantial missingness in some fields, including weight and diagnosis variables. Missing values must be interpreted according to the meaning of each field.

## 4. Data Transformation

The data preparation process included mapping admission type, admission source, and discharge disposition categories for reporting.

Length of stay is grouped into the following categories:

- 1-3 Days
- 4-7 Days
- 8+ Days

These categories support comparisons across different hospital stay durations.

## 5. DAX and KPI Development

DAX measures were created for encounter counts, unique patients, readmitted encounters, non-readmitted encounters, and the recorded readmission rate.

The final formulas and business definitions are documented in `dax-measures.md`.

## 6. Dashboard Development

The report contains four pages:

1. Executive Overview
2. Readmission Analysis
3. Demographics
4. Hospital Operations

The report uses KPI cards, charts, slicers, and page navigation to support interactive exploration.

## 7. Validation

The final review should verify KPI calculations, patient and encounter counts, length-of-stay categories, mapping tables, slicer interactions, and navigation.

The readmission classification and denominator must be checked before interpreting a result as a 30-day readmission rate.

## 8. Limitations

This is a descriptive portfolio project. Observed patterns do not establish causal relationships and should not be used for clinical decision-making.

The findings depend on the source data, available variables, data-quality limitations, and the definitions used in the report.
