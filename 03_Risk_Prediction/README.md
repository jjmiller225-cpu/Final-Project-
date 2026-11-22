# 03 | Predicting the Next Adverse Inspection

**Purpose:** Assess whether previous inspections and facility context can help prioritize follow-up visits.

## Workbook
- `Logistic Regression.xlsx` — the team's Excel-based regression and classification work.

## Outcome and predictors
The analysis models an adverse inspection result and examines indicators including previous adverse result, restaurant category, reinspection, and complaint visits.

| Factor | Reported odds ratio | Reading |
|---|---:|---|
| Previous adverse inspection | 2.41 | Higher odds of another adverse outcome |
| Restaurant category | 1.77 | Higher odds relative to the reference group |
| Reinspection | 0.30 | Lower odds relative to the reference inspection type |

## The critical distinction
**About 70% accuracy** at a `0.50` threshold sounds promising; however, the report describes an **82.4% false-negative rate** for adverse outcomes. In a safety setting, sensitivity matters. The team's proposed `0.30` threshold is a **candidate for evaluation**, not a validated operational guarantee.

## Reproduce
Open the Excel file and review fitted coefficients, classification probabilities, and the confusion matrix. Re-estimating the model may require the Excel analytics add-in used in the original course project.

[Return to project overview](../README.md)
