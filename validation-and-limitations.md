# Data Validation and Project Limitations

## 1. Purpose

This document records the validation checks and limitations associated with the Hospital Readmission Analytics Power BI project.

## 2. Validation Checklist

| Check | What to Verify | Status |
|---|---|---|
| Total encounters | Confirm the final encounter count | To confirm |
| Unique patients | Confirm the distinct patient count | To confirm |
| Readmission classification | Verify source categories and transformation logic | To confirm |
| Readmission rate | Validate the numerator and denominator | To confirm |
| Length-of-stay groups | Check category boundaries and assignments | To confirm |
| Mapping tables | Verify admission and discharge mappings | To confirm |
| Slicer interactions | Check the intended visual interactions | To confirm |
| Page navigation | Test navigation across all report pages | To confirm |

Update each status after completing the relevant check.

## 3. KPI Reconciliation

The current recorded results are:

- Total encounters: 101,766
- Unique patients: 71,518
- Readmitted encounters: 46,902
- Not-readmitted encounters: 54,864
- Recorded readmission rate: 46.09%

Confirm these results against the final Power BI model and the filters applied.

The readmitted and not-readmitted categories should be reconciled with the relevant encounter population. Do not assume they cover all records without checking the classification logic.

## 4. Readmission Definition

The original dataset distinguishes `NO`, `>30`, and `<30`.

The binary status used in the report must be reviewed before making claims about 30-day readmission. A general readmission classification is not automatically equivalent to a 30-day readmission rate.

## 5. Limitations

- Some variables contain substantial missing information.
- Results depend on the quality and definitions of the source data.
- A patient may have multiple encounters.
- Descriptive comparisons do not establish causation.
- The report is for educational and portfolio purposes, not clinical decision-making.

## 6. Privacy and Data Sharing

Before sharing the repository publicly, confirm that the source dataset can be used and referenced under its applicable terms.

Do not publish confidential records, patient-identifiable information, or sensitive data in the report, screenshots, or supporting files.

## 7. Final Review

Record completed checks accurately. Document unresolved issues and update this file when the report is validated.
