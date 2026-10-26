# Power BI DAX Measures

This document contains the DAX calculations used in the Superstore Sales Performance Dashboard.

## 1. Total Sales

Calculates total revenue generated from sales.

```dax
Total Sales = SUM('Sample - Superstore 3'[Sales])
```

## 2. Total Profit

Calculates the total profit earned.

```dax
Total Profit = SUM('Sample - Superstore 3'[Profit])
```

## 3. Total Orders

Counts unique customer orders.

```dax
Total Orders = DISTINCTCOUNT('Sample - Superstore 3'[Order ID])
```

## 4. Profit Margin

Calculates the percentage of sales retained as profit.

```dax
Profit Margin = DIVIDE([Total Profit], [Total Sales], 0)
```

## 5. Average Order Value

Calculates the average revenue generated per order.

```dax
Average Order Value = DIVIDE([Total Sales], [Total Orders], 0)
```

## How the Measures Work

These measures automatically recalculate when users interact with the Year, Region, and Category slicers.

This allows users to compare sales performance across different periods, geographic regions, and product categories.
