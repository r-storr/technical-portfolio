
cat > "/Users/z/Projects/technical-portfolio/03-data-analysis/supply-chain-analysis/README.md" <<'EOF'
# Supply Chain Performance Analysis

## Project Overview

This project examines supplier delivery reliability, purchase-order quantity fulfillment, and warehouse receipt activity using synthetic supply chain data covering 2023–2025.

The analysis was conducted using Microsoft Excel, Power Query, and PivotTables. The project includes data cleaning, transformation, validation, KPI development, and a performance dashboard designed to communicate findings in an easily digestible format.

## Business Objectives

The analysis sought to answer four realistic business questions:

1. How reliably do suppliers meet expected delivery dates?
2. How completely are purchase-order quantities fulfilled?
3. Which suppliers generate the most late deliveries?
4. How are recorded inbound inventory receipts distributed across warehouses?

## Tools and Skills Demonstrated

- **Microsoft Excel:** Data analysis, formulas, PivotTables, and dashboard development
- **Power Query:** Data cleaning, table merging, filtering, and aggregation
- **Data Validation:** Missing-value checks, relationship validation, and KPI reconciliation
- **Data Visualization:** Supplier performance comparisons, warehouse receipt charts, and KPI cards
- **Business Analysis:** Interpreting operational performance and developing recommendations

## Dataset

**Source:** [Inventory & Supply Chain Dataset — Data Cleaning Challenge](https://www.analyticsengineering.com/datasets/inventory-supply-chain)

**Period:** 2023–2025

The dataset contains seven interconnected tables:

- Purchase Orders
- Purchase Order Lines
- Suppliers
- Products
- Warehouses
- Inventory Movements
- Inventory Opening Balances

The original data was imported into a consolidated Excel workbook while retaining the separate tables for cleaning, transformation, and analysis.

## Methodology

### 1. Data Preparation and Cleaning

The source tables were examined for missing values, inconsistent quantities, invalid dates, and missing relationships between records.

Power Query was used to prepare and transform the data. Identified data-quality issues were investigated and documented rather than automatically replacing missing information.

### 2. Data Transformation

Related tables were joined using purchase-order, supplier, product, and warehouse identifiers.

Additional calculations and aggregated tables were created to support supplier delivery analysis, quantity fulfillment analysis, and warehouse receipt reporting.

### 3. KPI Development

The analysis included:

- Orders evaluated
- On-time and late orders
- On-time and late delivery rates
- Average and maximum recorded delivery delays
- Overall order fill rate
- Outstanding units
- Supplier-level delivery and fulfillment rates
- Warehouse receipt volumes and shares

Delivery reliability calculations used completed purchase orders with valid delivery dates. Quantity fulfillment calculations included eligible received and partially received orders.

The overall fill rate was calculated using total units received divided by total units ordered, rather than averaging individual order-line percentages.

### 4. Dashboard Development

An Excel dashboard was developed to summarize the results through KPI cards, supplier comparisons, and warehouse receipt visualizations.

## Key Findings

| KPI | Result |
|---|---:|
| Late Delivery Rate | 78.22% |
| Overall Fill Rate | 94.28% |
| Average Late Delivery | 7.40 days |
| Outstanding Units | 4,567 |
| Suppliers With No On-Time Deliveries | 47 |
| Top Three Warehouses' Share of Receipts | 29.47% |

### Delivery Reliability

78.22% of completed purchase orders were delivered late, with an average delay of 7.40 days among late completed orders.

Additionally, 47 suppliers recorded no on-time deliveries among their eligible orders.

Frequent lateness may reduce scheduling predictability and increase replenishment risk.

### Quantity Fulfillment

The overall fill rate was 94.28%, with 4,567 units remaining unfulfilled across the evaluated orders.

Quantity fulfillment was comparatively stronger than delivery punctuality, although unfulfilled quantities still warrant monitoring.

### Warehouse Receipt Distribution

The three highest-volume warehouses were:

| Warehouse | Recorded Receipt Units |
|---|---:|
| W002 | 60,283 |
| W004 | 59,364 |
| W001 | 58,101 |
| **Combined** | **177,748** |

Together, these warehouses accounted for approximately 29.47% of recorded inbound receipts.

## Business Recommendations

Based on the findings, the following actions could be considered:

1. **Monitor supplier delivery reliability:** Establish regular supplier performance reviews and investigate recurring late deliveries.
2. **Prioritize underperforming suppliers:** Evaluate suppliers with consistently low on-time delivery rates and determine whether corrective action is needed.
3. **Track outstanding quantities:** Monitor incomplete purchase-order fulfillment to support replenishment planning.
4. **Review warehouse receipt patterns:** Compare inbound receipt volumes with warehouse capacity and demand data when available.
5. **Improve data quality:** Strengthen record validation and completeness to support more reliable inventory reporting.

## Data Limitations

The analysis uses synthetic data and is subject to limitations in the source records.

Missing relationships between inventory opening balances and recorded receipts prevented reliable calculation of actual ending inventory, inventory turnover, and stockout rates.

Warehouse findings therefore describe recorded inbound receipt activity rather than actual inventory availability or warehouse efficiency.

Outstanding units represent unfulfilled quantities within the evaluated purchase orders and should not automatically be interpreted as the current operational backlog.

## Project Deliverables

- [Excel Analysis Workbook](analysis/supply_chain_analysis.xlsx)
- [Supply Chain Performance Analysis Report (PDF)](reports/supply%20chain%20performance%20analysis.pdf)

The Excel workbook contains the analytical worksheets, Power Query transformations, PivotTables, and performance dashboard.

The PDF report provides additional methodology, findings, business implications, and recommendations.

## Conclusion

The analysis identified delivery reliability as a significant area of concern, while quantity fulfillment showed comparatively stronger performance.

The project demonstrates how data cleaning, transformation, validation, and visualization can be combined to investigate operational business questions and support data-driven decision-making.
EOF
