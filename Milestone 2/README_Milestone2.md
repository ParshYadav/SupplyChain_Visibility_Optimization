# Supply Chain Visibility & Optimization – Milestone 2

> **Inventory Analytics** and **Delivery Performance** dashboards built in **Power BI** using DAX measures, KPIs, interactive visuals, and drill-down analysis.

---


# Inventory Analytics Dashboard

## Objective

The Inventory Analytics Dashboard monitors inventory performance across warehouses, regions, categories, and products to improve stock utilization, reduce carrying costs, and support inventory optimization.

### Inventory Turnover Calculation

**Formula**

```text
Inventory Turnover Ratio = Total Sales / Average Inventory Value
```

**DAX**

```DAX
Avg Inventory Value = AVERAGE(Fact_table[inventory_value])

Inventory Turnover Ratio =
DIVIDE([Total Sales],[Avg Inventory Value],0)
```

### Unit-Based Inventory Turnover

```text
Inventory Turnover Ratio = Units Sold / Average Stock Quantity
```

```DAX
Units Sold = SUM(Fact_table[order_item_quantity])

Inventory Turnover Ratio (Units) =
DIVIDE([Units Sold],AVERAGE(Fact_table[stock_qty]),0)
```

A higher turnover ratio indicates efficient inventory movement, while a lower ratio indicates excess inventory or weak product demand.

---

## Slow-Moving and Fast-Moving Inventory Logic

Inventory movement is classified using **Days Since Last Sale**.

| Days Since Last Sale | Stock Quantity | Status |
|----------------------|---------------:|--------|
| Any | 0 | Out of Stock |
| More than 90 | > 0 | Dead Stock |
| 31–90 | > 0 | Slow-Moving |
| 0–30 | > 0 | Active (Fast-Moving) |

This approach helps identify products requiring liquidation, replenishment, or promotional strategies.

---

## Inventory KPIs

| KPI | Purpose |
|------|---------|
| Total Inventory Value | Current inventory valuation |
| Total Stock Quantity | Available stock |
| Inventory Turnover Ratio | Inventory efficiency |
| Inventory Turnover Ratio (Units) | Unit movement efficiency |
| Dead Stock Count | Non-moving products |
| Dead Stock Value | Capital blocked in dead inventory |
| Slow Moving Quantity | Slow-moving stock |
| Warehouse Capacity Used % | Storage utilization |
| Products to Reorder | Immediate replenishment |
| Products Below Safety Stock | Critical inventory |
| Stock Optimization Gap | Replenishment requirement |
| Reorder Quantity Suggested | Recommended procurement |
| MoM Inventory Value Change | Monthly inventory trend |

---

## Inventory Analysis

The dashboard supports analysis by:

- Warehouse
- Region
- Product Category
- Product
- Month and Year

Interactive slicers and drill-downs enable detailed exploration.

---

## Stock Monitoring

Products are automatically categorized as:

- OK
- Reorder Now
- Critical – Below Safety Stock

This enables proactive replenishment planning.

---

# Delivery Performance Dashboard

## Objective

The Delivery Performance Dashboard evaluates shipping efficiency, fulfillment performance, delivery delays, and logistics performance across different business dimensions.

---

## Delivery Performance Analysis Methodology

Key performance indicators include:

- Total Orders
- On-Time Delivery %
- Late Delivery %
- Advance Shipping %
- Average Scheduled Shipping Days
- Average Actual Shipping Days
- Lead Time Variance
- Fulfillment Rate
- Cancelled Orders
- Regional Late Rate
- Total Risk Flagged Orders
- Late Delivery Risk %
- Risk vs Actual Accuracy

### Lead Time Variance

```text
Actual Shipping Days − Scheduled Shipping Days
```

A positive value indicates delayed delivery, while a negative value indicates early delivery.

---

## Delivery Analysis

Delivery performance is analyzed by:

- Region
- Shipping Mode
- Product Category
- Product
- Time

Drill-down functionality allows detailed regional and product-level analysis.

---

## Trend Analysis

The dashboard tracks:

- Monthly delivery performance
- Monthly late delivery trend
- Regional delivery trend
- Shipping mode comparison
- Delivery status distribution

---

# Interactive Dashboard Features

- Interactive slicers
- Cross-filtering visuals
- KPI cards
- Line and bar charts
- Drill-down capability
- Regional analysis
- Warehouse analysis
- Product-level analysis
- Time-series trends

---

# Key Insights

## Inventory

- Low turnover products indicate overstocking.
- Dead stock increases holding costs.
- Slow-moving inventory highlights products requiring promotion.
- Safety stock monitoring prevents stock-outs.
- Warehouse utilization identifies storage bottlenecks.

## Delivery

- Late delivery percentage highlights logistics inefficiencies.
- Regional analysis identifies high-delay locations.
- Lead time variance measures delivery consistency.
- Fulfillment rate reflects operational efficiency.
- Delivery risk analysis supports proactive planning.

---

# Business Recommendations

## Inventory

1. Replenish products below safety stock.
2. Reduce dead stock through liquidation or promotions.
3. Monitor slow-moving products regularly.
4. Optimize warehouse utilization.
5. Use inventory trends for demand forecasting.

## Delivery

1. Improve shipping performance in high-delay regions.
2. Select efficient shipping modes based on historical performance.
3. Reduce lead time variance.
4. Improve fulfillment planning to minimize cancellations.
5. Use delivery risk indicators for proactive logistics decisions.

---

# Technologies Used

- Microsoft Power BI
- DAX
- Power Query
- Supply Chain Dataset

---

# Deliverables

- Milestone2_PowerBI.pbix
- Inventory Analytics Dashboard
- Delivery Performance Dashboard
- Dashboard Screenshots
- README.md

---

# Conclusion

This milestone extends the Supply Chain Visibility & Optimization project by delivering comprehensive inventory and delivery analytics dashboards. Interactive reports, DAX-based KPIs, trend analysis, and drill-down capabilities provide actionable insights that support inventory optimization, improve logistics performance, and enable informed business decisions.
