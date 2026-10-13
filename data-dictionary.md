# Data Dictionary

## Overview

This document describes important fields used in the Hospital Readmission Analytics Power BI project.

## Source Fields

| Field | Description | Analytical Use |
|---|---|---|
| `encounter_id` | Hospital encounter identifier | Counting encounters |
| `patient_nbr` | Patient identifier | Counting unique patients |
| `readmitted` | Original readmission classification | Readmission analysis |
| `time_in_hospital` | Length of stay in days | Length-of-stay analysis |
| `admission_type_id` | Encoded admission type | Admission comparisons |
| `admission_source_id` | Encoded admission source | Admission-source analysis |
| `discharge_disposition_id` | Encoded discharge disposition | Discharge analysis |
| `gender` | Recorded gender category | Demographic analysis |
| `age` | Age category | Demographic analysis |
| `diag_1` | Primary diagnosis code | Diagnosis data exploration |
| `diag_2` | Secondary diagnosis code | Diagnosis data exploration |
| `diag_3` | Additional diagnosis code | Diagnosis data exploration |
| `weight` | Recorded weight information | Data completeness review |

Confirm the exact spelling of each field against the final Power BI model.

## Derived Categories

### Length of Stay Group

- `1-3 Days`
- `4-7 Days`
- `8+ Days`

These groups are used to compare encounter patterns across length-of-stay categories.

### Readmission Status

The Power BI report uses the labels `Readmitted` and `Not Readmitted`.

The original source field includes `NO`, `>30`, and `<30`. The report's classification logic must be reviewed before interpreting this binary status as a specific 30-day readmission measure.

## Data Quality Notes

Initial profiling indicated approximately:

- 97% missing values in weight.
- 1% missing values in `diag_1`.
- 5% missing values in `diag_2`.
- 10% missing values in `diag_3`.

These percentages should be rechecked against the final model before publication.

## Interpretation Notes

- One patient may have multiple hospital encounters.
- Encounter counts and unique patient counts represent different measures.
- Missing diagnosis information does not necessarily mean that a patient has no diagnosis.
- Mapping tables should be interpreted using the appropriate source codes and definitions.
