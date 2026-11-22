# Data and method

**Source:** Montgomery County, Maryland food service inspection records, October 5, 2022–October 3, 2024, accessed through [Data.gov](https://catalog.data.gov/dataset/food-inspection).

The team documented 11,854 inspections of 4,160 establishments across 31 fields.

## Analysis workflow
1. Prepare inspection records and categorize inspection outcomes.
2. Compare adverse outcome rates by facility type and inspection type in Tableau.
3. Rank compliance checks and compare seasonal patterns.
4. Create previous-inspection indicators and other model variables.
5. Fit logistic regression in Excel and assess model accuracy and false negatives.

## Outcome definition
The team's binary analytical outcome codes **Critical Violations Corrected** and **Facility Closed** as adverse outcomes; **No Critical Violations Noted** is the other class. This is not an official county pass/fail label.

## Reproducing the work
Download the Excel and Tableau files from this repository after uploading the package. Open Tableau workbooks in Tableau Desktop and reconnect the local data source to `data/cleaned_inspection_data.xlsx`. The original workbooks contain local file paths. Reproducing the logistic regression may require the team's Excel add-in.

## Cautions
Inspection types differ; some records have missing values and possible duplicates. Model associations do not establish causality. Lowering the classification cutoff should be evaluated with a fresh confusion matrix before operational use.
