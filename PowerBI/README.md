# Power BI: Performance Driver Analysis

*Part of the [Square POS Business Analytics](https://github.com/monikemyles-sys/Square-POS-Business-Analytics) project. Companion workstream: see the [Excel Financial Health Assessment](https://github.com/monikemyles-sys/Square-POS-Business-Analytics/tree/main/Excel) for whether the business is healthy — this dashboard looks at what is driving that performance.*

## Objective
Interactive Power BI business intelligence dashboard identifying the factors driving YumYum BBQ's business performance and profitability — tracking revenue performance, net operating profit, profit margin, fee burden, category revenue, sales volume, and expense distribution using Power Query and DAX.

## Key Metrics

| Metric | Value |
|---|---|
| Total Revenue | $581,640 |
| Net Operating Profit | $18,850 |
| Profit Margin | 3.24% |
| Fee Burden Ratio | 1.16% |

*These figures match the Excel Financial Health Assessment exactly, confirming the two data corrections below carried through consistently to both tools.*

## Dashboard Screenshots
<img width="1912" height="851" alt="Main screen" src="https://github.com/user-attachments/assets/925b72f6-9663-40b0-8fb4-6f2049b8d903" />
<img width="1912" height="832" alt="Monthly Rev Trend" src="https://github.com/user-attachments/assets/e1420038-c362-4c04-9ac1-cd277cd6dc0b" />
<img width="1912" height="827" alt="2022 filter" src="https://github.com/user-attachments/assets/643f8d9b-021a-4733-8025-e9ab75c59f03" />

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

## Key Findings
- Lunch Plates is the leading revenue category at $327,849.97, substantially ahead of Catering at $48,361.01 — the business's core brick-and-mortar lunch service remains its primary revenue engine.
- The Two Piece Chicken is the single highest-revenue item at $73,633.96, followed by Ribs at $36,112.58 and Rib Tips at $23,741.01 — these three items are the clearest candidates for featured promotion or bundling.
- Walmart inventory (~26%) and general business expenses (~19%) are the two largest expense drivers, together making up nearly half of total costs — the clearest lever for improving the current 3.24% margin.
- Catering and the Clinton Marketplace Festival move in opposite directions across the year: Catering peaks in May and drops to its lowest point in October, the same month the festival peaks — suggesting the festival circuit may help offset Catering's seasonal dip.
- Lunch Plates (brick-and-mortar) peaks in March, declines gradually through the year, and reaches its lowest point in November and December — a seasonal pattern worth planning staffing and inventory around.
- At a verified 3.24% profit margin and 1.16% fee burden ratio, the business is profitable but thin-margined; processing fees are well-controlled, and expense management is the clearer opportunity for growth.

## Business Questions Answered

**What factors have the greatest impact on profitability?**
At a verified 3.24% profit margin and a low 1.16% fee burden ratio, processing fees are not a meaningful drag on profitability — payment fees of this size are well below typical industry card-processing rates of 2.5–3.5%. The larger lever is operating expenses: Walmart inventory (~26% of costs) and general business expenses (~19%) together account for nearly half of all spending, making cost management the clearest path to growing the thin margin further.

**Which categories drive revenue growth?**
Lunch Plates is the dominant category at $327,849.97, with Catering a distant second at $48,361.01. At the item level, the Two Piece Chicken ($73,633.96), Ribs ($36,112.58), and Rib Tips ($23,741.01) are the top three individual revenue drivers, unchanged by the data correction since item-level totals were never affected by the double-counting issue.

**How much revenue is being absorbed by fees and expenses?**
Processing fees are minimal at a 1.16% fee burden ratio. Operating expenses are the larger factor, with Walmart inventory and general business expenses together making up nearly half of total costs.

**Where can operational efficiencies be improved?**
The clearest opportunity remains on the cost side, particularly a vendor cost review of Walmart inventory and business expense spending. On the revenue side, the monthly trend data shows real seasonal structure worth planning around: Catering peaks in May and bottoms out in October, Lunch Plates (brick-and-mortar) peaks in March and declines steadily into a November/December low, and the Clinton Marketplace Festival peaks in October — right as Catering is at its weakest point, partially offsetting the dip. Whether Catering also offsets the brick-and-mortar's winter slowdown specifically is still an open question pending November/December Catering figures, and a deeper split of events versus brick-and-mortar profitability is planned as a follow-up analysis.

## Next Steps
- Split revenue and cost performance by Events/Catering versus Brick-and-Mortar to evaluate whether continuing event and catering work is net beneficial to profitability, or whether that time could be better spent on the core lunch service.

