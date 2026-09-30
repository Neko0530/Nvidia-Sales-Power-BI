# Nvidia GPU Sales Dashboard

A Power BI dashboard analyzing synthetic Nvidia GPU sales data for 2026 — built to answer the kind of questions a sales or product team would actually ask: which GPU models are moving, which regions are driving revenue, how customer satisfaction tracks against price, and how sales trend over time.

Dataset

The report is built on a single table, nvidia_gpu_sales_synthetic_2026, containing GPU sales transactions with fields covering:

Product details — gpu_model, gpu_family
Sales metrics — revenue, units sold, price
Customer context — customer_segment, satisfaction scores
Geography — region
Inventory status — stock_status
Time — sale_date, broken into a full Year → Quarter → Month → Day hierarchy for trend analysis

(Note: this is a synthetic dataset built for portfolio/practice purposes, not real Nvidia sales data.)

Report Pages
Page 1 — Sales Overview

This is the main dashboard, titled "Nvidia GPU Sales" at the top, and it's built around four key numbers you can see at a glance:

Total Revenue
Total Units (sold)
Average Price
Average Satisfaction (customer satisfaction score)

Below those headline cards, the page breaks the story down from several angles:

A donut chart splitting total units by stock_status — a quick read on how much of what's been sold is in stock, backordered, or discontinued.
A clustered column chart of total revenue by region, showing which markets are contributing the most.
A clustered bar chart of total revenue by gpu_model, ranking individual GPU models against each other.
A 100% stacked column chart of total units by gpu_family, showing how the unit mix shifts across product families.
A line chart of total revenue over time, using the full date hierarchy (Year/Quarter/Month/Day), so you can drill from a yearly trend all the way down to daily sales.

Three slicers sit alongside the visuals, letting you filter the whole page by region, GPU model, and customer segment — so you can isolate, say, just the enterprise segment in one region and watch every chart update together.

Page 2 — Model Detail (in progress)

The second page currently holds a single gpu_model slicer and appears to be a work-in-progress detail view — likely intended as a drill-down page for exploring an individual GPU model's performance once fully built out.

Tools & Format

Built in Power BI Desktop using the newer PBIR (Power BI Enhanced Report) project format, where each page and visual is stored as its own readable JSON file rather than one packed binary blob — this makes the report easier to diff and version-control alongside the rest of a portfolio project.

To open: load the .pbix file directly in Power BI Desktop.
