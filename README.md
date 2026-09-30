# Nvidia GPU Sales Dashboard

A Power BI dashboard analyzing synthetic Nvidia GPU sales data for 2026, designed to answer core commercial questions: which products are selling, which regions are driving revenue, how price relates to customer satisfaction, and how sales are trending over time.

*Note: this is a synthetic dataset built for portfolio purposes, not real Nvidia sales data.*

---

## Dataset

| Category | Fields |
|---|---|
| Product | `gpu_model`, `gpu_family` |
| Sales | Revenue, units sold, price |
| Customer | `customer_segment`, satisfaction score |
| Geography | `region` |
| Inventory | `stock_status` |
| Time | `sale_date` (Year → Quarter → Month → Day hierarchy) |

All fields come from a single table: `nvidia_gpu_sales_synthetic_2026`.

---

## Report Pages

### Page 1 — Sales Overview

The primary dashboard page, titled **"Nvidia GPU Sales."**

**KPI Cards**
| Metric | What it shows |
|---|---|
| Total Revenue | Overall sales revenue |
| Total Units | Overall units sold |
| Average Price | Mean selling price per unit |
| Average Satisfaction | Mean customer satisfaction score |

**Visuals**
| Visual | Breakdown | Purpose |
|---|---|---|
| Donut chart | Total units by `stock_status` | Read on stock health — in stock vs. backordered vs. discontinued |
| Clustered column chart | Total revenue by `region` | Compares regional sales performance |
| Clustered bar chart | Total revenue by `gpu_model` | Ranks individual GPU models by revenue |
| 100% stacked column chart | Total units by `gpu_family` | Shows the shifting unit mix across product families |
| Line chart | Total revenue over time | Trend view using the full date hierarchy, drillable from year down to day |

**Filters**
Three slicers — **region**, **GPU model**, and **customer segment** — filter every visual on the page simultaneously, so a single selection (e.g. one region and one segment) updates the entire view at once.

### Page 2 — Model Detail (In Progress)

Currently contains a single `gpu_model` slicer. This appears to be a planned drill-down page for individual GPU model performance, not yet built out with supporting visuals.

---

## Tools & Format

Built in Power BI Desktop using the PBIR (Power BI Enhanced Report) project format, which stores each page and visual as its own readable JSON file rather than a single packed binary. This makes the report easier to diff and version-control alongside the rest of a portfolio project.

**To open:** load the `.pbix` file directly in Power BI Desktop.
