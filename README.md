# Bank Loan Portfolio & Credit Risk Analytics

**Microsoft Excel | Business Intelligence | Financial Analytics | Independent Portfolio Project**

## Executive summary

This Excel project explores lending volume, portfolio composition, loan status, interest rates, and debt-to-income ratios. It combines a cleaned loan-level dataset, formula-driven KPI analysis, pivot tables, and a dashboard to help users explore where portfolio monitoring may be warranted. This is an independent analytical exercise, **not an assessment of a real lender's current risk or financial performance**.

## Business questions

1. What is the volume and funded value of the loan portfolio?
2. How do good/bad loan classifications compare across the portfolio?
3. How do interest rates and debt-to-income ratios differ by grade?
4. Which loan purposes and borrower segments account for application volume?
5. What additional evidence would be required before making lending-policy recommendations?

## Workbook structure

| Sheet | Role |
|---|---|
| `raw_data` | Source loan-level records |
| `cleaned_data` | Prepared loan records and derived `Loan_Category` |
| `Analysis` | Formula-based KPIs and pivot summaries |
| `Dashboard` | Visual reporting and interactive analysis |
| `Sheet1` | Additional loan-level data present in the original workbook; its relationship to the main source needs clarification |

## KPIs recorded in the workbook

| Measure | Value |
|---|---:|
| Applications | 19,323 |
| Total funded amount | $529,626,471 |
| Total payments recorded | $245,079,990.72 |
| Average interest rate | 12.04% |
| Average debt-to-income ratio | 17.38% |
| Good-loan applications | 9,689 (50.14%) |
| Bad-loan applications | 9,634 (49.86%) |
| Good-loan funded amount | $264,848,614 |
| Bad-loan funded amount | $264,777,857 |

These values are read from the workbook's cached KPI and pivot outputs; they should be recalculated in Excel after any changes to data or filters. The `Loan_Category` is a workbook-derived classification, not an independently validated probability of default.

## Findings

- **Portfolio classification is nearly evenly split:** 9,689 loans are classified as good and 9,634 as bad. This calls for careful review of the classification definition before making any real-world risk claims.
- **Grade B has the most applications:** 5,839, compared with 4,837 in Grade A and 4,009 in Grade C.
- **Interest rates increase across the reported grade spectrum:** average rates are approximately 7.36% in Grade A and 21.49% in Grade G. These are descriptive averages, not evidence of causal effects.
- **Debt-to-income ratios also differ by grade:** approximately 13.36% in Grade A versus 30.77% in Grade G.
- **Recorded payments are not profit:** total payments and funded amounts should not be compared as if they represent completed lifetime returns; loan vintages, timing, outstanding balances, fees, and write-offs are not resolved here.

## Analytical workflow

1. Inspect loan-level fields, date representations, and category definitions.
2. Review the prepared `cleaned_data` sheet and its derived loan classification.
3. Use Excel formulas and pivot tables to aggregate application counts, funded amounts, payments, interest rates, and debt-to-income ratios.
4. Explore segment differences using the dashboard and pivot summaries.
5. Translate descriptive findings into questions for credit-risk and operations teams, with explicit limitations.

### Data Preparation and Analysis Workflow

The Excel workbook follows a structured analytical workflow designed to preserve the original data while supporting exploration, preparation, and reporting.

1. **Raw Data (`raw_data`):** Contains the original loan records, retained as a reference dataset.
2. **Exploratory Analysis (`Sheet1`):** A duplicate of the original dataset used for applying filters, examining variables, and conducting preliminary analysis without modifying the source data.
3. **Cleaned Data (`cleaned_data`):** Contains the prepared data used for subsequent analysis and reporting.
4. **Analysis (`Analysis`):** Contains calculated performance indicators and supporting analytical summaries.
5. **Dashboard (`Dashboard`):** Presents loan performance, financial indicators, and portfolio characteristics through interactive Excel visualizations.

This approach separates the original dataset from analytical operations and helps maintain data integrity throughout the project.

## Tools and techniques

- Microsoft Excel, PivotTables, PivotCharts, KPI formulas, and dashboard reporting
- `COUNTIF`, `SUMIFS`, `AVERAGEIFS`, and `GETPIVOTDATA` formulas visible in the analysis sheet
- Portfolio segmentation by loan status, grade, purpose, credit score, and other fields

## Suggested business actions

See [`docs/business-recommendations.md`](docs/business-recommendations.md). These are **proposed investigations**, not implemented outcomes.

## Data quality, ethics, and limitations

- **Privacy:** the original workbook includes fields such as identifiers, employer names, gender, race, income, and credit score. Do not publish raw borrower-level records until the dataset's origin, redistribution rights, and privacy status are confirmed. If necessary, publish an anonymized sample and screenshots instead.
- **Fair lending:** demographic attributes should be used only for carefully governed fairness assessment, not as unreviewed decision criteria.
- **Date formats:** some loan dates appear as Excel serial values while others appear as text. Normalize and validate before drawing time-based conclusions.
- **Unresolved extra sheet:** `Sheet1` contains additional records. Confirm whether these belong to the analysis population before combining them with `cleaned_data`.
- **No validated model:** this project provides descriptive portfolio reporting, not a calibrated credit-scoring or default-prediction model.
- **No source license established:** verify that the dataset and workbook may be shared publicly before committing them.

## How to explore

Open the original Excel workbook locally, review the `Analysis` and `Dashboard` sheets, and refresh pivots where appropriate. Excel desktop is recommended for the full interactive experience. Dashboard screenshots may be added to `screenshots/` for visitors without Excel.

## Portfolio context

Independent project demonstrating how financial datasets can be converted into interpretable portfolio KPIs, interactive reports, and evidence-aware recommendations.
