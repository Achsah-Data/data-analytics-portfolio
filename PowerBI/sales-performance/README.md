# Sales Performance Dashboard (Power BI)

**Author:** Pasula Achsah Hadassah  
**Tools:** Power BI Desktop, DAX, Power Query  
**Dataset:** Superstore dataset (Kaggle)

## Overview
Interactive sales & profitability dashboard built with the Superstore dataset.  
Includes 3 pages: Overview, Product Analysis, Time & Trend.

## Files
- `superstore.pdf` — exported report (PDF)
- `assets/overview.png` — screenshot of Overview page
- `assets/product.png` — screenshot of Product Analysis
- `assets/time.png` — screenshot of Time & Trend
- `superstore_sales.pbix` — Power BI file (if included)

## Key Insights
- Total Sales ≈ 2.3M; Profit Margin ≈ 12%.  
- West & East regions drive most revenue.  
- Technology is top-selling and profitable; Furniture has lower margins.  
- Some high-sales items (e.g., Tables) show poor profitability → review pricing.

## Key Measures
```DAX
Total Sales = SUM('Superstore Dataset'[Sales])
Total Profit = SUM('Superstore Dataset'[Profit])
Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)
Orders Count = DISTINCTCOUNT('Superstore Dataset'[Order ID])
AOV = DIVIDE([Total Sales], [Orders Count], 0)



