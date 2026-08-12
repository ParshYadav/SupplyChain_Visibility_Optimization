# Milestone 4 – Warehouse Efficiency & Executive Dashboard

## Project Overview

Milestone 4 extends the existing Supply Chain Visibility & Optimization Power BI report from Milestone 3. The objective is to analyze warehouse performance and provide an executive-level overview using KPIs, DAX measures, interactive visuals, drill-through, and forecasting.

## Deliverables

- `Milestone 4.pbix` – Power BI report
- `Warehouse_Efficiency_Dashboard.png` – Warehouse dashboard screenshot
- `Executive_Dashboard.png` – Executive dashboard screenshot
- `README.md` – Project documentation

---

# 1. Warehouse Efficiency Dashboard

The Warehouse Efficiency Dashboard monitors:

- Warehouse utilization
- Warehouse throughput
- Inventory storage efficiency
- Warehouse productivity
- Performance by warehouse
- Performance by region
- Performance by product category

### Key KPIs

- Total Warehouses
- Average Utilization %
- Maximum Utilization %
- Minimum Utilization %
- Total Inventory
- Total Throughput
- Average Throughput
- Storage Efficiency
- Warehouse Productivity

---

# 2. Calculation Methodology

### Warehouse Utilization

**Utilization % = Used Storage Capacity / Total Storage Capacity × 100**

Example DAX:

```DAX
Average Utilization % =
AVERAGE ( Fact_table[utilization_%] )
```

Warehouse-level maximum and minimum utilization are calculated using `MAXX` and `MINX` over individual warehouses.

### Throughput

**Total Throughput = Sum of Processed Units**

```DAX
Total Throughput =
SUM ( Fact_table[throughput] )
```

Throughput is analyzed by warehouse, region, product category, and time.

### Warehouse Productivity

**Productivity = Throughput / Resource Input**

Where resource input may be labor hours, operating hours, or another suitable operational measure available in the dataset.

### Storage Efficiency

Storage efficiency evaluates how effectively available warehouse capacity is being used and is analyzed together with inventory and throughput.

---

# 3. Executive Dashboard

The Executive Dashboard provides a consolidated view of important supply-chain KPIs.

It includes:

- KPI cards
- Performance trends
- Warehouse and regional comparisons
- Product-category analysis
- Interactive filters
- Drill-through analysis
- Forecasting where applicable

The dashboard follows a top-down design: **KPI Summary → Trends → Comparisons → Detailed Analysis**.

---

# 4. Forecasting Approach

Power BI forecasting is applied to suitable time-series data such as throughput or inventory.

The process includes:

1. Using a continuous date field.
2. Displaying the KPI as a time-series chart.
3. Adding a forecast through the Analytics pane.
4. Reviewing forecast trends and confidence intervals.
5. Using the forecast for capacity and inventory planning.

Forecast values are treated as estimates.

---

# 5. Dashboard Optimization

The report is optimized by:

- Using DAX measures instead of unnecessary calculated columns.
- Removing unused fields.
- Maintaining appropriate relationships.
- Avoiding unnecessary visuals.
- Optimizing complex DAX calculations.
- Limiting high-cardinality fields.
- Optimizing visual interactions.
- Using Performance Analyzer where required.

These techniques improve report performance and user experience.

---

# 6. Key Insights & Business Recommendations

The dashboards help identify:

- Over-utilized and under-utilized warehouses.
- High-throughput warehouses.
- Warehouses with high inventory but low throughput.
- Regional performance differences.
- Product categories requiring significant storage capacity.
- Productivity improvement opportunities.

### Recommendations

- Monitor warehouses approaching maximum capacity.
- Redistribute inventory where possible.
- Investigate slow-moving inventory.
- Improve productivity in low-performing warehouses.
- Use forecasting for future capacity and inventory planning.
- Replicate best practices from high-performing warehouses.

---

# 7. Conclusion

Milestone 4 provides an interactive Power BI solution for monitoring warehouse efficiency and executive-level supply-chain performance. The dashboards combine DAX KPIs, utilization, throughput, productivity, storage efficiency, trends, forecasting, filters, and drill-through analysis to support data-driven business decisions.

## Technology Used

- Power BI Desktop
- DAX
- Power Query
- Data Modeling
- Power BI Visualizations
- Power BI Forecasting
- GitHub
