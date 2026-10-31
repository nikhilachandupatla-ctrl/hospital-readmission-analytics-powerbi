# DAX Measures

## 1. Overview

This document describes the key DAX measures used in the Hospital Readmission Analytics Dashboard.

The measures support encounter analysis, patient counts, readmission reporting, and eligible 30-day readmission analysis.

## 2. Encounter and Patient Measures

### Total Encounters

Counts the total number of hospital encounters.

```dax
Total Encounters =
COUNTROWS(diabetic_data)
```

### Unique Patients

Counts distinct patients using the patient identifier.

```dax
Unique Patients =
DISTINCTCOUNT(diabetic_data[patient_nbr])
```

### Any Readmission Encounters

Counts encounters with a recorded readmission either within or after 30 days.

```dax
Any Readmission Encounters =
CALCULATE(
    COUNTROWS(diabetic_data),
    diabetic_data[readmitted] IN {"<30", ">30"}
)
```

### Not Readmitted Encounters

Counts encounters with no recorded readmission.

```dax
Not Readmitted Encounters =
CALCULATE(
    COUNTROWS(diabetic_data),
    diabetic_data[readmitted] = "NO"
)
```

## 3. Readmission Measures

### Any Readmission Rate

Calculates the percentage of encounters with a recorded readmission, including both within-30-day and after-30-day outcomes.

```dax
Any Readmission Rate =
DIVIDE(
    [Any Readmission Encounters],
    [Total Encounters],
    0
)
```

### Readmitted Within 30 Days

Counts encounters with a recorded readmission within 30 days.

```dax
Readmitted Within 30 Days =
CALCULATE(
    COUNTROWS(diabetic_data),
    diabetic_data[readmitted] = "<30"
)
```

## 4. Eligible 30-Day Readmission Measures

For this project, selected discharge disposition categories are excluded from the eligible encounter population.

### Readmission Eligible

Calculated column:

```dax
Readmission Eligible =
IF(
    diabetic_data[discharge_disposition_id]
        IN {"11", "13", "14", "19", "20", "21"},
    "Excluded",
    "Eligible"
)
```

### Eligible Encounters

Counts encounters classified as eligible.

```dax
Eligible Encounters =
CALCULATE(
    [Total Encounters],
    diabetic_data[Readmission Eligible] = "Eligible"
)
```

### Eligible 30 Day Readmissions

Counts eligible encounters with a readmission within 30 days.

```dax
Eligible 30 Day Readmissions =
CALCULATE(
    [Readmitted Within 30 Days],
    diabetic_data[Readmission Eligible] = "Eligible"
)
```

### 30 Day Readmission Rate (Eligible)

Calculates the percentage of eligible encounters with a recorded readmission within 30 days.

```dax
30 Day Readmission Rate (Eligible) =
DIVIDE(
    [Eligible 30 Day Readmissions],
    [Eligible Encounters],
    BLANK()
)

## 5. Baseline Results

With report filters reset, the dashboard displays the following baseline results:

| Measure | Result |
|---|---:|
| Total Encounters | 101,766 |
| Unique Patients | 71,518 |
| Any Readmission Encounters | 46,902 |
| Not Readmitted Encounters | 54,864 |
| Any Readmission Rate | 46.09% |
| Eligible Encounters | 99,343 |
| Eligible 30 Day Readmissions | 11,314 |
| 30 Day Readmission Rate (Eligible) | 11.39% |

These figures represent the dataset-level results with no report slicer filters applied.

## 6. Calculation Notes

- Any Readmission Rate includes both `<30` and `>30` outcomes.
- The eligible 30-day readmission rate uses only `<30` outcomes in its numerator.
- The eligible encounter population excludes the specified discharge disposition IDs.
- `DIVIDE` is used to handle division safely.
- The eligible 30-day rate returns BLANK when there are no eligible encounters in the current filter context.
- Dashboard measures respond to report filters and slicers.
