# Business Recommendations and Next Analyses

These recommendations are hypotheses for further investigation based on descriptive workbook summaries, **not actions implemented at a lender**.

## 1. Validate loan outcome definitions

The workbook divides 19,323 applications into 9,689 good and 9,634 bad loans. Inspect the underlying `loan_status` to `Loan_Category` mapping and assess whether active, charged-off, defaulted, and fully paid loans are categorized consistently. Document the observation period and maturity of each loan before interpreting the bad-loan share as a default metric.

## 2. Investigate risk differences by grade

The workbook reports higher average interest rates and debt-to-income ratios in lower credit grades. Calculate grade-specific outcome shares and confidence intervals, and compare by loan vintage, term, and purpose before suggesting pricing or underwriting changes. Descriptive correlations do not establish causation.

## 3. Build a reliable collections and repayment view

The dashboard records $245.08 million in payments against $529.63 million in funded amounts. These aggregates alone cannot determine recovery rate or profitability. Add outstanding principal, loan age, payment schedule, delinquency status, write-offs, and fees to produce valid cohort-based collections metrics.

## 4. Prioritize data quality checks

Standardize mixed text/serial dates, confirm unique loan IDs, check missing values and outliers, and reconcile the additional `Sheet1` records against the 19,323-row analysis population. Refresh formulas and pivot caches after corrections.

## 5. Apply responsible analytics to borrower demographics

If analyzing outcomes by gender or race, use the results for appropriately governed fairness monitoring and potential disparate-impact review. Do not infer borrower creditworthiness from protected characteristics or recommend using them as automated approval features.

## Suggested next KPIs

- Vintage-adjusted delinquency and charge-off rates
- Outcome rates by loan grade, term, and purpose
- Time to resolution and payment performance by cohort
- Data quality completeness and date-format validation
- Fairness monitoring with documented governance

## Limits of interpretation

The workbook provides a historical dataset and descriptive analyses. It does not establish real business impact, current portfolio health, actual net profitability, or the effectiveness of any recommended intervention.
