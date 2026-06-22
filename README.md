# TechyStore Sales Analytics Dashboard

A two-page Power BI dashboard built on 1,000 rows of tech product sales data (Sep 2023 – Sep 2024), with a focus on **DAX time-intelligence measures** — MTD, QTD, and YTD — to track revenue performance over time.

![Sales Overview](screenshots/page1_overview.png)
![Product & Channel Breakdown](screenshots/page2_breakdown.png)

---

## Business Questions Answered

- How much revenue did we generate this month, this quarter, and this year so far?
- Which products and sales channels are driving the most revenue?
- How does monthly sales trend look across the full 13-month period?
- How does each product perform across different sales channels and payment types?

---

## Dataset

**File:** `29-DAX_-_Tech_Products_Sales_Data.xlsx` → Sheet: `SalesData`

| Column | Description |
|---|---|
| Transaction ID | Unique order identifier |
| Product | One of 10 tech products (Laptop, Smartphone, Camera, etc.) |
| Quantity | Units sold per transaction |
| Unit Price (INR) | Price per unit |
| Date | Transaction date (Sep 2023 – Sep 2024) |
| Customer Name | Buyer name |
| State | Indian state where sale occurred |
| Country | India |
| Sales Channel | Online / Store / Direct |
| Payment Type | Cash / Credit Card / Debit Card / Net Banking / UPI |
| Sales | Total sale value (Quantity × Unit Price) |

**Key numbers at a glance:**
- 1,000 transactions across 13 months
- 10 product categories
- 3 sales channels, 5 payment types
- Total revenue: ₹5.12 Crore

---

## DAX Measures Built

This project demonstrates intermediate Power BI skills through custom time-intelligence measures. All measures are written from scratch in DAX:

| Measure | DAX Function Used | Purpose |
|---|---|---|
| Total Sales | `SUM` | Base revenue measure |
| Total Transactions | `COUNTROWS` | Order volume |
| Avg Sale per Transaction | `DIVIDE` | Revenue efficiency |
| Total Quantity Sold | `SUM` | Volume metric |
| MTD Sales | `TOTALMTD` | Month-to-date revenue |
| QTD Sales | `TOTALQTD` | Quarter-to-date revenue |
| YTD Sales | `TOTALYTD` | Year-to-date revenue |

The MTD / QTD / YTD measures are connected to a `DateTable` built using `CALENDARAUTO()` so time intelligence works correctly across all visuals and slicers.

---

## Dashboard Pages

### Page 1 — Sales Overview
The headline page. Four KPI cards at the top show Total Sales, MTD, QTD, and YTD side by side — making it immediately clear how current-period performance compares to longer time horizons.

- **4 KPI cards:** Total Sales · MTD Sales · QTD Sales · YTD Sales
- **Line chart:** Monthly sales trend across the full 13-month period
- **Bar chart:** Total sales by product (10 products, sorted by revenue)
- **Donut chart:** Revenue split by sales channel (Online / Store / Direct)
- **Slicers:** Product · Month

### Page 2 — Product & Channel Breakdown
A deeper drill-down into how products perform across channels and payment types, with a DAX-powered summary table.

- **3 KPI cards:** Avg Sale per Transaction · Total Quantity Sold · Top Product
- **Clustered bar chart:** Sales by product × sales channel (cross-breakdown)
- **Donut chart:** Order share by payment type
- **DAX table:** Product-wise Total Sales, MTD, QTD, YTD in one view
- **Slicers:** Sales Channel · Payment Type

---

## Tools Used

- **Power BI Desktop** — report building, DAX measures, data modelling
- **Power Query** — data loading and type formatting
- **Excel** — source data
- **DAX** — custom measures including time intelligence (MTD, QTD, YTD)

---

## Skills Demonstrated

- Writing DAX time-intelligence measures (`TOTALMTD`, `TOTALQTD`, `TOTALYTD`)
- Building a `DateTable` using `CALENDARAUTO()` for correct time-intelligence context
- Using `DIVIDE` for safe ratio calculations (no divide-by-zero errors)
- Combining KPI cards + trend lines + breakdowns into a coherent two-page narrative
- Cross-breakdown visuals (product × channel clustered bar)
- Interactive filtering with slicers that affect all visuals on the page

---

## How to Run

1. Download Power BI Desktop (free) from [powerbi.microsoft.com](https://powerbi.microsoft.com).
2. Open `TechyStore_Sales_Analytics_Dashboard.pbix`.
3. Data is embedded — no reconnection needed.
4. On Page 1, use the **Product** and **Month** slicers to filter all visuals including the MTD/QTD/YTD cards.
5. On Page 2, use the **Sales Channel** and **Payment Type** slicers to filter the clustered bar and DAX table.

---

## Repository Structure

```
TechyStore-Sales-Analytics-Dashboard/
├── README.md
├── TechyStore_Sales_Analytics_Dashboard.pbix
├── data/
│   └── Tech_Products_Sales_Data.xlsx
└── screenshots/
    ├── page1_overview.png
    └── page2_breakdown.png
```

---

## Author
[NAME -Harshit Panchal] | [LINKDIN - www.linkedin.com/in/harshit-panchal-955887205] | [Email- harshitpanchal2277@gmail.com]

Open to Data Analyst / Business Intelligence Analyst roles.
