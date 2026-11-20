# Indian Banking Transactions — Excel Data Analysis Project

An Excel-based banking transaction analysis project completed as part of training at **Innomatics**. The workbook demonstrates data preparation, data-quality checks, formula-based feature creation, pivot-table summaries, and a dashboard.

> **Dataset provenance:** This is a training/practice dataset believed to have been sourced from Kaggle. The exact original Kaggle URL has not been verified. This project does not claim to represent real Indian bank operational data.
>
> **Privacy:** The workbook intended for publication is a sanitized copy. Customer names, customer IDs, and account numbers are replaced with synthetic placeholders. Do not publish the unsanitized original workbook.

## Project objective

Explore a sample banking transactions dataset and summarize transaction activity across regions, branches, account types, transaction types, payment modes, dates, statuses, and fraud labels.

## Workbook contents

The Excel workbook contains five worksheets:

1. **Raw Data** — the source transaction table used in the exercise.
2. **Cleaned data** — the analysis table with additional calculated fields.
3. **Data_Quality_Check** — checks for missing values, negative transaction/balance values, date range, and customer segmentation.
4. **Pivot_Tables** — summary tables used to compare transaction counts by region and month and fraud labels by branch.
5. **Dashboard** — a visual summary with four charts.

## Analysis techniques and Excel skills

- Data review and cleaning workflow
- Excel structured tables and calculated columns
- `TEXT` for year-month grouping
- `IF` and nested `IF` / `OR` logic for net change, fraud flag, and transaction category
- `COUNTIF` for customer segmentation and quality checks
- Pivot-table summaries
- Dashboard charts and visual reporting

## Calculated fields in the cleaned worksheet

| Field | Purpose |
|---|---|
| `year_month` | Groups transaction dates into a `YYYY-MM` month key |
| `Net Change` | Treats withdrawals as negative and other transaction types as positive |
| `Fraud Flag` | Converts the Yes/No fraud label to a numeric 1/0 flag |
| `Transaction Category` | Groups Cash as Cash-Based and supported electronic payment modes as Digital; other values are marked Review |
| `Customer Type` | Labels customers as Frequent Transactor or One-Time User based on the count of Customer ID values |

## Dataset snapshot

The supplied workbook contains **500 transaction rows** and **16 source columns**. Transaction dates range from **11 July 2023 to 6 July 2025**.

Descriptive figures from the supplied cleaned worksheet:

- Total transaction amount: **₹93,933,780.49**
- Average transaction amount: **₹187,867.56**
- Completed transactions: **434**
- Fraud-labelled transactions: **13**
- Digital category: **402**; Cash-Based category: **98**

These are descriptive summaries of this sample workbook only, not claims about a real bank or the banking sector.

## Repository files

- `Indian_Banking_Transactions_Sanitized.xlsx` — sanitized workbook with all five worksheets.
- `WORKBOOK_CONTENTS.md` — column and worksheet notes.

## How to use

1. Download the Excel workbook from this repository.
2. Open it in Microsoft Excel (recommended for formula recalculation and dashboard rendering).
3. Review the Raw Data and Cleaned data sheets.
4. Explore the Data_Quality_Check and Pivot_Tables sheets.
5. Open Dashboard to view the charts.

## Limitations and notes

- The exact original Kaggle listing has not been confirmed.
- The workbook is a learning exercise based on sample data; it is not an official Indian Bank dataset.
- All 500 rows in the supplied cleaned sheet are currently classified as One-Time User by its customer-count formula. This is a property of the supplied sample, not a general customer-behaviour conclusion.
- Excel may recalculate formula-driven cells when the workbook is first opened.

## Acknowledgement

Completed as an Excel data-analysis training project at **Innomatics**. Dataset source attribution should be updated if the original Kaggle URL becomes available.
