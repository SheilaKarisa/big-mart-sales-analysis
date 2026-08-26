# BigMart Sales Analysis Pipeline & Interactive Dashboard

An end-to-end data analysis project exploring BigMart retail sales. This repository contains an integrated pipeline using R and SQLite to clean raw sales records, evaluate item- and outlet-level performance, and render a interactive web report.
## Live Dashboard
View the interactive report: **[BigMart Sales Analysis Dashboard](https://sheilakarisa.github.io/big-mart-sales-analysis/)**

### Tech Stack
* **Language:** R (RStudio)
* **Database Management:** RSQLite, SQL (Views, Aggregations, Data Transformations)
* **Visualization & Reporting:** ggplot2, R Markdown (`flatly` theme, floating TOC)
* **Deployment & Hosting:** GitHub Pages

#### Key Analytical Insights
* **Fat Content Standardizations:** Consolidated inconsistent entry formats (`LF`, `low fat`, `reg`) into clean categories via SQLite views before aggregation. Analysis revealed Low Fat products drive 64% of total revenue ($11.9M) versus 36% for Regular ($6.7M), with the revenue gap primarily driven by catalog composition volume rather than per-item sales outperformance.
* **Outlet Performance:** Evaluated revenue distribution across 8,523 records, identifying Medium-sized outlets as top performers ($7.49M total revenue; $2,682 average revenue per item). While Supermarket Type 1 generated the highest overall revenue ($12.9M / 69.5%), Supermarket Type 3 demonstrated superior per-item efficiency ($3,694 avg/item vs. $2,316 for Type 1). Accounted for data quality constraints by identifying and isolating 2,410 missing Outlet Size entries (28.3%) as a distinct "Unknown" category prior to evaluation.
* **Pricing vs. Sales Volume:** Analyzed price elasticity and revenue relationships across item categories. Identified a moderate positive relationship ($r = 0.57$, R^2 approximately 0.32$) between Item Price (Item MRP) and sales revenue (Item Outlet Sales). While higher-priced items drive larger sales totals, pricing accounts for roughly one-third of overall sales variance. Cross-segment analysis confirmed this relationship remains virtually identical regardless of product fat content (Low Fat: 0.563 vs. Regular: 0.576).

##### Repository Structure
.
├── Project.Rmd       # Source R Markdown code with SQLite queries & visualizations
├── index.html        # Rendered HTML report hosted on GitHub Pages
├── Train.csv         # Raw dataset
└── outputs/          # Generated output assets
