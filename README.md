# Performance Dashboard (Power BI) — README

Short description
This repository contains a Power BI performance dashboard that shows monthly sales, targets, person-level metrics, trends, and highlights. The dashboard helps stakeholders get quick insights (a useful understanding) into sales performance and trends.

<img width="1257" height="713" alt="image" src="https://github.com/theravendrasahu/Performance-Dashboard/blob/89add227df509320770dda2d9d8b846a16f00dfd/Dashboard%20image.png" />

---

Table of contents

What is this

Key features

New words to learn

Folder structure (example)

Requirements

How to open / run

Data sources & refresh

Important notes & best practices

Contributing



---

## What is this

A Power BI report (.pbix) that visualizes sales vs target, trends across months, person-level KPIs, and a set of small multiples / charts for deeper analysis. The visuals help teams find which months met targets, who is over/under performing, and where to focus attention.


---

## Key features

Monthly Sales vs Target overview (high-level visualization — a visual representation)

Person / salesperson leaderboard and trends

Month-by-month target attainment heatmap

KPI cards (Total Sales Actual, Total Sales Target, Variance)

Drill-through filters and slicers for time, person, region, product (if available)

Notes section for commentary and action items



---

## New words to learn

Insight (a useful understanding)

Robust (strong and reliable)

Visualization (a visual representation)

Reconcile (to match and confirm)


I will try to add 1–2 new words in future chats to help you learn.


---

## Folder structure (example)

/performance-dashboard
├── data/
│   ├── sales.csv                # sample CSV (if used)
│   └── lookup_tables.xlsx
├── pbix/
│   └── Performance_Dashboard.pbix
├── docs/
│   └── data_dictionary.md
├── README.md


---

## Requirements

Power BI Desktop (latest stable version) — to open and edit the .pbix file

If using DirectQuery / database: access to the SQL Server / data source credentials

Optional: Power BI Service account (for publishing to cloud)



---

## How to open / run

1. Install Power BI Desktop: https://powerbi.microsoft.com/ (open Power BI Desktop).


2. Open the .pbix file from pbix/Performance_Dashboard.pbix.


3. If prompted, update data source credentials:

For files (CSV / Excel): browse to the data/ folder or the correct network path.

For databases: enter server name, database, and the correct authentication method.



4. Click Refresh to update visuals using current data.


5. Use slicers (on the report) to filter by month, person, product, or region.




---

## Data sources & refresh

Supported data sources: CSV, Excel, SQL Server, or other connectors supported by Power BI.

If the file uses imported data, update the local files then Refresh.

If using DirectQuery, visuals will query the source live (ensure permissions).

For scheduled refresh in Power BI Service: publish the report and configure gateway if needed.



---

## Important notes & best practices

Keep raw data files in the data/ folder or a secure database.

Use a consistent date table (calendar) for correct time intelligence and DAX measures.

Validate numbers by reconciling (matching) Power BI totals with source system totals — reconciliation ensures accuracy.

When sharing, export to PDF or publish to Power BI Service and give appropriate access.

Keep sensitive data out of the repository (do not commit credentials or PII).



---

## DAX / Measures (brief)

Examples of common measures used:

Total Sales = SUM(Sales[Amount])

Total Target = SUM(Targets[Amount])

Variance = [Total Sales] - [Total Target]

Percent of Target = DIVIDE([Total Sales], [Total Target], 0)


If you want, I can write actual DAX measures used in this report in simple language.


---

## Contributing

If you want to improve visuals, add measures, or fix data connections:

1. Create a new branch.


2. Edit the .pbix in Power BI Desktop.


3. Save changes, include a brief changelog in docs/changes.md.


4. Create a pull request with description of changes.



Keep changes small and document any new data sources or fields.


