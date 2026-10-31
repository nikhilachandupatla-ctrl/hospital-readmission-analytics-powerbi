# Validation and Limitations

## 1. Purpose

This document describes the validation checks performed during dashboard development and the limitations that should be considered when interpreting the results.

The purpose is to improve transparency and help users understand how the reported figures should be interpreted.

## 2. Validation Checks

The following checks were performed during the development of the dashboard.

### KPI Validation

The main KPI measures were reviewed with report filters reset.

| KPI | Validated Result |
|---|---:|
| Total Encounters | 101,766 |
| Unique Patients | 71,518 |
| Any Readmission Encounters | 46,902 |
| Not Readmitted Encounters | 54,864 |
| Any Readmission Rate | 46.09% |
| Eligible Encounters | 99,343 |
| Eligible 30 Day Readmissions | 11,314 |
| 30 Day Readmission Rate (Eligible) | 11.39% |

### Readmission Definition Checks

- The `<30` category was used to identify recorded readmissions within 30 days.
- The `>30` category was included in the Any Readmission calculation.
- The `NO` category was used to identify encounters without a recorded readmission.
- The eligible 30-day calculation was restricted to encounters classified as eligible.

### Filter and Interaction Checks

- Gender and age-group slicers were tested.
- Slicer synchronization across report pages was checked.
- KPI cards and charts were reviewed under different filter selections.
- Page navigation was tested to confirm that users could move between report pages.

### Visual Validation

- Chart titles and labels were reviewed for clarity.
- Number formatting and percentage displays were checked.
- Encounter volumes and readmission rates were presented as separate measures where appropriate.
- Categories with missing or unmapped values were reviewed to avoid misleading comparisons.

## 3. Data Quality Considerations

The dataset contains categories that require careful interpretation.

### Missing Admission Type Values

Some encounters have missing admission-type information. These records are retained as a separate category and should not be interpreted as a specific admission type.

### Unmapped Admission Sources

Some admission-source records are classified as Not Mapped. These values are treated as a data-quality observation rather than a meaningful named admission source.

### Diagnosis Field Completeness

The diagnosis fields have varying levels of completeness. The presence of missing diagnosis values should be considered when interpreting diagnosis-related analysis.

### Discharge Disposition Categories

Certain discharge disposition categories are excluded from the eligible 30-day readmission calculation according to the project's eligibility rule.

Their encounter volumes should not be confused with the eligible population used to calculate the rate.

## 4. Project Limitations

The following limitations should be considered:

1. **Historical dataset:** The analysis reflects the records available in the supplied dataset and does not represent current hospital performance.

2. **Encounter-level analysis:** Patients may have multiple encounters. Encounter counts should not be interpreted as unique patient counts.

3. **Recorded readmission outcomes:** The analysis relies on the readmission values provided in the dataset.

4. **Eligibility definition:** The eligible 30-day readmission rate depends on the discharge disposition exclusions defined for this project.

5. **Missing and unmapped values:** Incomplete or unmapped categories may affect comparisons across groups.

6. **Descriptive analysis:** The dashboard identifies patterns and associations within the available data. It does not establish that a particular demographic, admission type, or length of stay causes readmission.

7. **Limited external context:** The dataset does not provide all the clinical and operational information that may influence readmission outcomes.

## 5. Future Improvements

Potential improvements include:

- Adding additional validation against independent reference results.
- Exploring diagnosis-related readmission patterns after reviewing data completeness.
- Investigating patient-level readmission sequences.
- Adding time-based analysis if reliable date fields and suitable data become available.
- Incorporating additional hospital or clinical information to provide broader context.

## 6. Conclusion

The dashboard provides a structured view of hospital encounter and readmission patterns. Its results should be interpreted using the documented metric definitions, eligibility rules, and data limitations.

Clear definitions and validation checks are important for producing reliable and understandable reporting.
