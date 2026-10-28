# Superstore Sales & Profitability Dashboard (Power BI)

Interactive Power BI dashboard analysing Superstore retail sales, profit, discounting, customers, and products across regions.

## Overview

| Item | Detail |
|---|---|
| Tool | Microsoft Power BI Desktop |
| Dataset | `Superstore.csv` (9,994 order lines) |
| Period | Jan 2011 – Dec 2014 |
| Orders / Customers | 5,009 / 793 |
| Total Sales / Profit | ~$2.30M / ~$286K |
| Geography | United States (Central, East, South, West) |
| Categories | Furniture, Office Supplies, Technology |

## Dashboard Pages

1. **Page 1**: KPI summary cards.
2. **Sales Overview**: sales trend over time, category/region breakdown, key sales KPIs.
3. **Sales Overview_1**: supporting sales view with additional KPI cards.
4. **Profitability Analysis**: sales vs profit scatter, profit by category/sub-category, profit-status split, discount impact.
5. **Customers & Product Insight**: customer and product rankings, segment breakdown, region and sub-category slicers, trend line, pivot table.
6. **Geo / Detail view**: map of sales and profit by location, plus detail tables.

> Page names match the `.pbix`. Rename sections here if you rename tabs in the report.

## Screenshots

Add images to `docs/screenshots/` and link them:

```md
![Sales Overview](docs/screenshots/sales-overview.png)
![Profitability Analysis](docs/screenshots/profitability.png)
![Customers & Product Insight](docs/screenshots/customers-products.png)
```

## Data Dictionary

| Column | Description |
|---|---|
| Row ID | Unique row identifier |
| Order ID / Order Date / Ship Date | Order identity and dates (`dd/mm/yy`) |
| Ship Mode | Standard, Second Class, First Class, Same Day |
| Customer ID / Customer Name / Segment | Customer identity and segment (Consumer, Corporate, Home Office) |
| Country / City / State / Postal Code / Region | Location |
| Product ID / Category / Sub-Category / Product Name | Product hierarchy |
| Sales | Revenue of the order line |
| Quantity | Units sold |
| Discount | Discount rate applied |
| Profit | Profit of the order line |
| Discount Status | Derived flag: discounted vs no discount |
| Profit Status | Derived flag: profit vs loss |
| Is Profitable | Derived boolean (`TRUE`/`FALSE`) |
| Sales Per Unit | Derived: Sales ÷ Quantity |

## Key Metrics

- Total Sales, Total Profit, Profit Margin %
- Total Orders, Total Customers, Total Quantity
- Average Discount, Average Sales per Unit
- Profitable vs loss-making orders

## Key Questions Answered

- Which regions, categories, and sub-categories drive sales and profit?
- Where do discounts hurt profitability?
- Which customers and segments contribute most?
- How do sales and profit trend over time?
- Which states and cities perform best or worst?

## Repository Structure

```
.
├── dashboard/
│   └── Super_store.pbix
├── data/
│   └── Superstore.csv
├── docs/
│   └── screenshots/
├── .gitignore
├── .gitattributes
└── README.md
```

## How to Use

1. Clone the repo:
   ```bash
   git clone <your-repo-url>
   cd <repo-name>
   ```
2. Open `dashboard/Super_store.pbix` in Power BI Desktop.
3. If data fails to load: **Home → Transform data → Data source settings → Change Source**, and point to `data/Superstore.csv`.
4. Click **Refresh**.

## Requirements

- Power BI Desktop (latest version recommended)
- No gateway or credentials needed (local CSV source)

## Notes

- Dates in the CSV are `dd/mm/yy`. Set locale to English (India/UK) when importing to avoid day/month swaps.
- `.pbix` is binary; Git cannot diff it. Describe changes in commit messages.

## Author

Ayushyaman Singh, Data Analyst
