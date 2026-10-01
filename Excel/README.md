# Excel Dashboard Analysis

## Objective

Analyze category Interactive Excel and Power Pivot business intelligence dashboard analyzing multi-year Square POS sales, processing fees, and net operating profit margins using Power Query and DAX.

## Key Metrics

| Metric | Value |
|---|---|
| Total Revenue | $582,044.42 |
| Total Operating Expenses | $556,051.21 |
| Net Operating Profit | $19,257.21 |
| Profit Margin | 3.31% |
| Average Selling Price (ASP) | $6.63 |
| Items Sold | 87,855 |

## Dashboard Screenshots
<img width="1887" height="737" alt="image" src="https://github.com/user-attachments/assets/51faaa25-2064-4d30-9948-bd5d146a21e9" />

<img width="1902" height="776" alt="image" src="https://github.com/user-attachments/assets/f54bda97-2e11-478c-8bc3-66c82b586f53" />

<img width="1906" height="762" alt="image" src="https://github.com/user-attachments/assets/b5a2c2f3-bd9e-4093-b487-4400710e94de" />


## Project Background

This dashboard was developed using seven years of real operational and financial data from a family-owned restaurant that utilizes Square POS. The objective was to automate reporting, improve business visibility, and support data-driven decision-making.

## Tools Used

- Microsoft Excel
- Power Query
- Power Pivot
- DAX

## How I Built It

### 1. Data Ingestion & Transformation (Power Query)

Automated Data Pipeline:

- Cleaned, transformed, and consolidated seven years (2019–2026) of messy wide-format Square POS exports (Item Sales, Modifiers, Processing Fees, and Operational Expenses).
- Date Standardization
- Unpivoted daily wide-column transaction

### Data Modeling

- Built Star Schema (Power Pivot)
- Created relationships between tables
- Authored DAX calculations

### Dashboard Architecture

- Designed KPI scorecards
- Built interactive slicers
- Created profitability and sales analysis views

## Data Quality & Validation

Before finalizing the metrics above, two data quality issues were identified, investigated, and corrected. Documenting the process here, because catching these errors was as much a part of this project as the dashboard itself.

### Issue 1: Revenue was double-counted
**The problem:** The original Total Revenue measure added two numbers together that should never have been combined — the full Item Sales total (which already includes the price of every side or modifier added to a plate) plus the Modifier Sales total (a separate report breaking out how much of that same revenue came specifically from sides). Since Square bakes a modifier's price directly into the parent item's own sale total, adding Modifier Sales on top counted every side twice.

**How it was confirmed:** Tracing a single item (a chicken leg plate) through Square's own itemized sales report showed each line's total was literally the base price plus every modifier's listed price added together in one sale, proving modifiers are not a separate transaction.

**The fix:** Total Revenue was redefined to equal the Item Sales total alone. Modifier Sales is kept as an informational breakdown of which sides are most popular, not as additional revenue.

**Impact:** Total Revenue corrected from $727,429.45 to $582,070.64 lifetime (2019–2026), a reduction of about 20%.

### Issue 2: A data entry typo inflated expenses by $23,367
**The problem:** One cell in the underlying expense-tracking workbook (October 2020, Sam's Club) was entered as "233,67" using a comma instead of a decimal point. Depending on which tool read it, this single typo was interpreted two different ways: Excel treated it as text and excluded it from its own total (undercounting by $233.67), while Power Query's type conversion read the comma as a thousands separator and parsed it as $23,367.00 (overcounting by more than $23,000).

**How it was found:** Reconciling the dashboard's Total Operating Expenses against an independent, manually-kept bookkeeping ledger surfaced a $23,367 gap. Filtering the expense data down to the specific category and comparing it month by month pinpointed the exact cell responsible.

**The fix:** Corrected the cell to 233.67 and refreshed the data model.

**Impact:** Total Operating Expenses corrected from $579,184.54 to $556,051.21 lifetime.

### Why this matters
Together, these two fixes moved Net Operating Profit from an artificially distorted figure to a true, verified lifetime profit of $26,019.43 — a 4.47% margin, independently cross-checked against a separate, manually-kept financial ledger for the business. A dashboard is only as trustworthy as the logic feeding it, and reconciling against an independent source turned out to be the single most valuable check in this project.

## Key Findings

- Revenue increased significantly between 2019 and 2023.
- The business shifted from high-volume/low-ticket sales to higher-value transactions.
- Menu diversification contributed additional revenue streams.
- Profitability remained positive across the reporting period.



