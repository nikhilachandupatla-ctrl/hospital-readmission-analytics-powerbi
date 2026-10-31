# Data Dictionary

## 1. Overview

This project uses a hospital encounter dataset containing information about patient demographics, hospital admissions, diagnoses, treatments, length of stay, and readmission outcomes.

The dataset is analyzed at the encounter level. Each row represents a hospital encounter, rather than necessarily representing a unique patient.

## 2. Dataset Information

| Item | Description |
|---|---|
| Primary dataset | `diabetic_data.csv` |
| Mapping dataset | `IDS_mapping.csv` |
| Number of encounters | 101,766 |
| Unique patients | 71,518 |
| Number of original columns | 50 |
| Analysis tool | Microsoft Power BI |

## 3. Important Fields

| Field | Description |
|---|---|
| `encounter_id` | Unique identifier for a hospital encounter |
| `patient_nbr` | Patient identifier used to distinguish patients |
| `race` | Recorded patient race category |
| `gender` | Recorded patient gender |
| `age` | Patient age range |
| `admission_type_id` | Coded hospital admission type |
| `discharge_disposition_id` | Coded discharge destination or disposition |
| `admission_source_id` | Coded source of hospital admission |
| `time_in_hospital` | Number of days spent in the hospital |
| `diag_1` | Primary diagnosis code |
| `diag_2` | Secondary diagnosis code |
| `diag_3` | Additional diagnosis code |
| `readmitted` | Readmission outcome: `<30`, `>30`, or `NO` |

## 4. Derived Fields Used in the Dashboard

| Derived field | Description |
|---|---|
| `Readmission Status` | Groups encounters into Readmitted and Not Readmitted |
| `Length of Stay Group` | Groups hospital stays into 1–3 Days, 4–7 Days, and 8+ Days |
| `Admission Type Group` | Groups admission types into reporting categories |
| `Admission Source Group` | Groups admission sources into reporting categories |
| `Readmission Eligible` | Identifies encounters included or excluded from the eligible 30-day readmission calculation |

## 5. Readmission Outcome Definitions

| Original value | Interpretation |
|---|---|
| `<30` | Readmitted within 30 days |
| `>30` | Readmitted after 30 days |
| `NO` | No recorded readmission |

**Any Readmission** includes both `<30` and `>30`.

**30-Day Readmission** includes only encounters with the `<30` outcome, subject to the project's eligibility classification.

## 6. Data Interpretation Notes

- An encounter is not the same as a unique patient. One patient may have multiple encounters.
- Coded admission and discharge fields require mapping to meaningful descriptions.
- Missing or unmapped categories are retained and interpreted separately.
- Diagnosis fields are available in the dataset but are not necessarily used in every dashboard visual.
- The data dictionary describes the fields relevant to this project and is not intended to document every original dataset column.
