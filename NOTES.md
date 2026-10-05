# Copilot Development Notes

## 1. Star Schema Suggestion

### Prompt
I am building a Power BI business intelligence project for Brewmetrics Coffee Co. The source is a coffee sales CSV containing date, city, store format, category, item, quantity, unit price, and sales amount. Suggest a star schema with one fact table and at least three dimension tables. Explain the purpose of each table briefly.

### Copilot Suggestion
Copilot suggested a star schema consisting of:
- FactCoffeeSales
- DimDate
- DimStore
- DimProduct

It also recommended using surrogate keys such as DateKey, StoreKey, and ProductKey.

### Implementation
I created the four tables and established relationships between the fact table and the three dimensions.

---

## 2. Month-over-Month Sales Growth

### Prompt
I am building a Power BI business intelligence project for Brewmetrics Coffee Co. My semantic model has a FactCoffeeSales table and DimDate, DimStore, and DimProduct dimensions. I need a DAX measure for month-over-month sales growth. The measure should compare the current month's total sales with the previous month's sales using the DimDate table. Please suggest the DAX formula and briefly explain it.

### Copilot Suggestion

```DAX
Total Sales =
SUM ( FactCoffeeSales[SalesAmount] )

Previous Month Sales =
CALCULATE (
    [Total Sales],
    DATEADD ( DimDate[Date], -1, MONTH )
)

Month-over-Month Sales Growth % =
DIVIDE (
    [Total Sales] - [Previous Month Sales],
    [Previous Month Sales]
)