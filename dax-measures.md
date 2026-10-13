# DAX Measures and Business Definitions

## Overview

This document describes the key measures used in the Hospital Readmission Analytics dashboard.

The final DAX formulas must be copied from the actual Power BI model before publication.

## 1. Total Encounters

**Purpose:** Counts hospital encounter records in the current filter context.

**Recorded result:** 101,766

**Formula:** Add the exact DAX measure from Power BI Desktop.

## 2. Unique Patients

**Purpose:** Counts distinct patient identifiers.

**Recorded result:** 71,518

**Formula:** Add the exact DAX measure from Power BI Desktop.

## 3. Readmitted Encounters

**Purpose:** Counts encounters classified as readmitted under the project's current definition.

**Recorded result:** 46,902

**Formula:** Add the exact DAX measure from Power BI Desktop.

## 4. Not-Readmitted Encounters

**Purpose:** Counts encounters classified as not readmitted under the project's current definition.

**Recorded result:** 54,864

**Formula:** Add the exact DAX measure from Power BI Desktop.

## 5. Readmission Rate

**Purpose:** Reports the proportion of encounters classified as readmitted under the measure's definition.

**Recorded result:** 46.09%

**Formula:** Add the exact DAX measure from Power BI Desktop.

Document the numerator, denominator, filters, and readmission classification.

## 6. Readmission by Length of Stay

**Purpose:** Compares the readmission measure across the `1-3 Days`, `4-7 Days`, and `8+ Days` categories.

**Formula:** Add the final measure used by the visual.

## 7. 30-Day Readmission Analysis

**Purpose:** Analyzes readmission within 30 days only if the final measure explicitly implements that definition.

**Formula:** Add the exact final 30-day measure from the Power BI model.

Document its numerator, denominator, and classification logic.

## DAX Concepts

- Measures are evaluated in the current filter context.
- Slicers can change measure results.
- Distinct counts are used when counting unique patient identifiers.
- Percentage measures require a clearly defined numerator and denominator.
- The documented formula must match the formula used in the final report.
