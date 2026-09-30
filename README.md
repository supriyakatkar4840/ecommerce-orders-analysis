# E-commerce Orders Analysis

Exploratory data analysis of 100 e-commerce orders (Apr–Jul 2024) using **NumPy, Pandas, Matplotlib and Seaborn**.

## Objective
Answer 22 analysis questions across three areas:
- **NumPy:** descriptive stats, revenue arrays, min-max normalization
- **Pandas:** grouping, filtering, sorting, missing-value handling, de-duplication, data cleaning
- **Visualization:** trends, regional comparisons, product mix, distributions

## Dataset
`data/ecommerce_orders.csv` – 100 rows, 9 columns:

| Column | Description |
|---|---|
| OrderID | Unique order identifier |
| CustomerID | Customer code (20 customers) |
| Product | Laptop, Mobile, Tablet, Camera, Smartwatch, Headphone |
| Quantity | Units ordered (1–4) |
| Price | Unit price (₹) |
| OrderDate | Date in DD-MM-YYYY format |
| Region | East, West, North, South |
| PaymentMode | Cash, Credit Card, Debit Card, UPI |
| TotalAmount | Quantity × Price |

## Key findings
- Total revenue **₹65.7 L**; average order value **≈ ₹65,745**
- **South** has the highest total sales; **North** has the highest average order value (fewer, larger orders)
- **Laptop** is the top product by revenue (~22%), **Smartwatch** the lowest (~13%)
- Exactly one order per day for 100 days, so daily order count is flat; sales *value* is what varies
- No missing values, duplicates or negative values in the raw data

## Charts
| | |
|---|---|
| ![Sales over time](images/01_sales_over_time.png) | ![Sales by region](images/02_sales_by_region.png) |
| ![Product pie](images/03_product_sales_pie.png) | ![Orders per day](images/04_orders_per_day.png) |
| ![Boxplot](images/05_boxplot_region.png) | |

## Project structure
```
ecommerce-orders-analysis/
├── data/ecommerce_orders.csv
├── notebooks/case_study_analysis.ipynb   # full solution, Q1–Q22
├── images/                                # exported charts
├── requirements.txt
└── README.md
```

## How to run
```bash
git clone https://github.com/<your-username>/ecommerce-orders-analysis.git
cd ecommerce-orders-analysis
pip install -r requirements.txt
jupyter notebook notebooks/case_study_analysis.ipynb
```

## Notes
- Dates are parsed with `format="%d-%m-%Y"` to avoid day/month confusion.
- Because the data is already clean, the cleaning steps (Q13–Q17) leave it unchanged; each prints a before/after count so this is verifiable.

## Author
Supriya Katkar
