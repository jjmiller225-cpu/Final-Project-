# Montgomery County Food Safety | Risk Intelligence

**From inspection records to better inspection priorities.**  
*A BUS 446 business analytics case study · November 2026*

> **The central finding:** A model can be about **70% accurate** and still miss **82.4% of adverse inspections** at a 0.50 decision threshold. For food safety, the cost of a missed hazard matters more than headline accuracy.

## At a glance

| Inspection records | Establishments | Adverse outcomes | Model accuracy (reported) |
|---:|---:|---:|---:|
| 11,854 | 4,160 | ~31% | ~70% |

**Geography:** Montgomery County, Maryland  
**Period:** October 5, 2022 – October 3, 2024  
**Tools:** Microsoft Excel, Tableau, Excel logistic regression add-in (named *XLMinner* in the team report)

## The question behind the charts

With limited inspection resources, how can public health teams focus attention on establishments and food safety practices that warrant the closest monitoring? This project connects three lines of inquiry:

1. **Where are adverse inspection outcomes concentrated?** Compare establishment categories while accounting for inspection type.
2. **Which compliance failures recur?** Explore cold holding, pests, and seasonal patterns.
3. **Can inspection history improve risk prioritization?** Evaluate logistic regression, including the consequences of false negatives.

## What the team found

| Signal | Finding reported in the final report | Why it matters |
|---|---|---|
| Facility type | Public middle schools **40.5%**, restaurants **36.2%**, carry out **33.2%** adverse outcome rates | Risk varies by facility category |
| Cold holding | **19.9%** of visits recorded noncompliance | Refrigeration deserves targeted prevention |
| Pest control | **15.5%** of visits recorded rodent/insect noncompliance | Pest prevention is a priority |
| Seasonality | Cold holding: **18.5% winter** vs **21.8% summer** | Pre-summer equipment checks may help |
| Prior adverse result | Odds ratio **2.41** | Past inspection performance is a strong risk signal |
| Restaurant indicator | Odds ratio **1.77** | Higher estimated odds than reference group |
| Reinspection indicator | Odds ratio **0.30** | Lower estimated odds |
| Classification at 0.50 | **82.4% false-negative rate** | Accuracy can conceal poor detection |

*These are team-reported inspection-level findings, not independently verified figures. Associations do not establish causality.*

## Visual evidence

The original charts are embedded in the team's report and extracted to the `visualizations/` folder in the accompanying [project package](https://github.com/jjmiller225-cpu/Final-Project-). The editable Tableau workbooks are included in the downloadable project package until uploaded to this repository.

## Data and method

**Source:** [Montgomery County Food Inspection dataset (Data.gov)](https://catalog.data.gov/dataset/food-inspection). The project documents 31 fields and 11,854 inspection records.

1. Clean inspection data; group **No Critical Violations Noted** separately from **Critical Violations Corrected / Facility Closed**.
2. Compare outcome rates across facility categories and inspection types in Tableau.
3. Analyze compliance checks by category and season.
4. Build prior-inspection indicators and estimate a logistic regression in Excel.
5. Assess false negatives and classification threshold trade-offs.

**Interpretation note:** “Adverse outcome” is a project-defined grouping, not an official county pass/fail designation.

## Decisions supported by the analysis

- **Prioritize repeat adverse outcomes** with earlier follow-up visits.
- **Target refrigeration and pest-control hazards** in prevention efforts.
- **Test a lower model cutoff:** The team proposes reducing 0.50 to 0.30, but this requires validation of sensitivity, precision, and inspection workload before operational use.

## Project files

| Folder | Material |
|---|---|
| `data/` | Cleaned inspection workbook |
| `analysis/` | Logistic regression workbook |
| `tableau/` | Tableau analysis workbooks |
| `visualizations/` | Figures from the final report |
| `report/` | Full business case report |
| `documentation/` | Project overview and task plan |

**Reproducibility:** The original Tableau workbooks reference a teammate's local Windows file path and may require reconnecting to the cleaned Excel dataset. Reproducing the regression may require the original Excel add-in.

## Limitations

The study covers one county and approximately two years. Different inspection types, repeated establishment visits, missing values, and potential duplicates limit interpretation. The project does not measure actual foodborne illness. Predictive performance should be validated on held-out data before making enforcement decisions.

## Team and attribution

**Maxwell Blanc · Jace Miller · Ryan Winkler · Mikey Vang**  
BUS 446 · November 20, 2026

Source: Montgomery County of Maryland, *Food Inspection*, Data.gov (as cited in the team's final report). All analyses and interpretations are from the student team.
