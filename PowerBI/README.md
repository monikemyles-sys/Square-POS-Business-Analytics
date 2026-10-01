# Power BI: Performance Driver Analysis

*Part of the [Square POS Business Analytics](https://github.com/monikemyles-sys/Square-POS-Business-Analytics) project. Companion workstream: see the [Excel Financial Health Assessment](https://github.com/monikemyles-sys/Square-POS-Business-Analytics/tree/main/Excel) for whether the business is healthy — this dashboard looks at what is driving that performance.*

## Objective
Interactive Power BI business intelligence dashboard identifying the factors driving YumYum BBQ's business performance and profitability — tracking revenue performance, net operating profit, profit margin, fee burden, category revenue, sales volume, and expense distribution using Power Query and DAX.

## Key Metrics

| Metric | Value |
|---|---|
| Total Revenue | $727,043 |
| Net Operating Profit | $141,051 |
| Profit Margin | 19.45% |
| Fee Burden Ratio | 0.93% |

## Dashboard Screenshots
*(Add screenshots of your Power BI report pages here — export each page as an image from Power BI Desktop with File > Export > Export report pages as image, then drag them into this section on GitHub. Do this before publishing: a dashboard project with no screenshot is the fastest way to lose a recruiter's attention.)*

## Project Background
This dashboard is the Power BI workstream of the Square POS Business Analytics project, focused on performance driver analysis — identifying what is driving YumYum BBQ's revenue, profitability, and cost structure. It uses the same underlying Square POS sales, processing fee, and expense data as the Excel workstream, but is built to investigate a different set of business questions rather than duplicate that dashboard.

## Tools Used
- Power BI Desktop
- Power Query
- Power Pivot / Data Modeling
- DAX

## How I Built It

### 1. Data Ingestion & Transformation (Power Query)
- Loaded and shaped the Item Sales Summary, Expense Summary, Service Fees, and Date Table data for the reporting period.
- Standardized dates and cleaned category, item, and expense-type fields ahead of modeling.

### Data Modeling
- Built relationships between the sales, expense, fee, and date tables.
- Authored DAX measures for Total Revenue, Net Operating Profit, Profit Margin, Category Revenue, and Fee Burden Ratio.

### Dashboard Architecture
- Designed KPI cards for the four headline metrics.
- Built clustered bar charts for category- and item-level revenue comparisons.
- Added a donut chart for the expense-type breakdown and a line chart for the monthly revenue trend.
- Included year and category slicers for interactive filtering.

## Business Questions Answered

**What factors have the greatest impact on profitability?**
Expense structure is the biggest lever available. The business already holds a healthy 19.45% profit margin and a low 0.93% fee burden ratio, but Walmart inventory and general business expenses together account for nearly 45% of total costs — making cost management, not fees, the main profitability driver to watch.

**Which categories drive revenue growth?**
Lunch Plates is the clear driver, generating $473,235 in revenue — roughly 144% higher than the next-closest category, Catering, at $193,746.04. At the item level, the Two Piece Chicken ($73,633), Ribs ($36,112), and Rib Tips ($23,741) are the top three individual contributors.

**How much revenue is being absorbed by fees and expenses?**
Processing fees are minimal, at a 0.93% fee burden ratio. Operating expenses are more significant: Walmart inventory alone accounts for 25.39% of total costs, with general business expenses adding another 18.9%.

**Where can operational efficiencies be improved?**
The clearest opportunity is on the cost side — specifically a vendor cost review of Walmart inventory and business expense spending — since revenue is already strong and consistent year over year, aside from a seasonal uptick around October worth planning around.



