# Regional Sales Analysis

A data analytics project focused on evaluating sales performance, profitability, and regional trends using Python, pandas, and data visualization. The project aims to turn sales-order data into actionable insights that can support business planning and resource allocation. A Power BI dashboard will complement the Python analysis with interactive reporting.

## Business Problem

Sales teams often lack a clear, data-driven understanding of regional performance, making it difficult to identify growth opportunities and optimize resources. This project analyzes sales and cost data across regions, products, customers, and sales channels to uncover performance trends, evaluate profitability, and support strategic decision-making.

## Project Objectives

- Measure sales performance across delivery regions and sales channels.
- Compare revenue, costs, and profitability to identify strong and weak performers.
- Analyze sales trends over time.
- Identify products and customer segments that contribute to sales performance.
- Prepare a business-focused Power BI dashboard for interactive exploration.
- Translate analytical findings into practical recommendations.

## Tools and Technologies

- **Python** — analysis and data preparation
- **Jupyter Notebook** — exploratory data analysis (EDA)
- **pandas and NumPy** — data manipulation and calculations
- **Matplotlib and Seaborn** — visualizations
- **Power BI** — interactive dashboard (planned / in progress)

## Dataset Overview

The workbook shown in the source data contains multiple sheets:

- **Sales Orders** — order-level sales and cost information
- **Customers** — customer lookup information
- **Regions** — region lookup information
- **State Regions** — state-to-region mapping
- **Products** — product lookup information
- **2017 Budgets** — budget information for comparison with actual performance

The Sales Orders sheet includes fields such as:

| Column                      | Description                                              |
| --------------------------- | -------------------------------------------------------- |
| `OrderDate`                 | Date of the order                                        |
| `Customer Name Index`       | Customer identifier linked to customer lookup data       |
| `Channel`                   | Sales channel, such as Wholesale, Distributor, or Export |
| `Currency Code`             | Currency used for the order                              |
| `Warehouse Code`            | Warehouse identifier                                     |
| `Delivery Region Index`     | Region identifier linked to region lookup data           |
| `Product Description Index` | Product identifier linked to product lookup data         |
| `Order Quantity`            | Quantity ordered                                         |
| `Unit Price`                | Price per unit                                           |
| `Line Total`                | Total sales value for the order line                     |
| `Total Unit Cost`           | Total cost recorded for the order line                   |

The workbook also appears to include reference tables and 2017 budget data, which may support geographic analysis and actual-versus-budget comparisons.

**Data note:** Confirm the dataset's source, license, date coverage, row count, currency conventions, and definitions of the financial fields before publishing the repository. Do not publish proprietary or confidential data.

## Repository Structure

```text
regional-sales-analysis/
├── README.md
├── requirements.txt
├── .gitignore
├── data/
│   └── Regional Sales Dataset.xlsx
├── notebooks/
│   └── regional_sales_analysis.ipynb
├── reports/
│   └── figures/
└── powerbi/
    ├── screenshots/
    └── documentation.md
```

## Analysis Workflow

1. **Data loading and inspection** — load the workbook and inspect sheet names, dimensions, column types, and sample records.
2. **Data quality assessment** — check missing values, duplicates, inconsistent data types, and unexpected values.
3. **Data preparation** — parse order dates, validate numeric fields, and connect lookup tables using the relevant identifiers.
4. **Exploratory data analysis** — summarize sales, costs, quantities, and performance over time and across business dimensions.
5. **Profitability analysis** — calculate profit and profit margin only after validating the definitions and units of the source fields.
6. **Visualization** — use charts and summary tables to communicate patterns and exceptions.
7. **Power BI reporting** — build an interactive report with documented KPIs, filters, and drill-downs.
8. **Recommendations** — connect the findings to potential business actions and state any limitations.

## Business Questions

The analysis is designed to investigate questions such as:

- Which delivery regions generate the highest and lowest sales?
- Which regions contribute most to profit, and do high-sales regions also have strong margins?
- How do revenue and profitability change over time?
- Which sales channels contribute most to revenue and profit?
- Which products and customers are the largest contributors to sales?
- Are there regions or products with high sales but comparatively low profitability?
- How does actual performance compare with the 2017 budget, where the data supports a valid comparison?

These questions may be refined based on the available data and the results of the analysis.

## Key Findings

- **Regional performance:** [Insert the key regional comparison, supported by figures.]
- **Profitability:** [Insert a finding about profit or margin.]
- **Sales trends:** [Insert a time-based finding.]
- **Products or channels:** [Insert a finding about product or channel contribution.]

## Power BI Dashboard

**Status:** Planned / in progress.

The planned dashboard will provide an interactive view of regional sales performance.

Potential report components:

- **KPI cards:** total sales, total cost, profit, profit margin, and order quantity, subject to validation of the source fields.
- **Regional performance:** sales and profit by delivery region or state.
- **Sales trends:** monthly or yearly sales and profit.
- **Channel analysis:** performance by Wholesale, Distributor, Export, and other available channels.
- **Product and customer analysis:** leading contributors and underperforming segments.
- **Budget comparison:** actual versus budget, if the budget data can be aligned correctly with the sales data.

Potential slicers include order date, delivery region, state, sales channel, product, and customer.

## How to Run the Python Analysis

1. Clone or download this repository.
2. Install the dependencies listed in `requirements.txt`.
3. Obtain the dataset using the source and access instructions documented in `data/Regional Sales Datset.xlsx`.
4. Open `notebooks/regional_sales_analysis.ipynb` in Jupyter Notebook or JupyterLab.
5. Run the notebook cells in order.

Install dependencies with:

```bash
pip install -r requirements.txt
```

Example `requirements.txt` for a notebook using the libraries listed above:

```text
pandas
numpy
matplotlib
seaborn
openpyxl
jupyter
ipykernel
```

Adjust the dependency list to match the packages the notebook actually imports.

## Recommendations

Recommendations will be added after the analysis has established the relevant regional, product, channel, and profitability patterns. Possible areas to investigate include:

- Reviewing low-performing regions to understand whether the gap relates to sales volume, product mix, or costs.
- Studying high-revenue regions with low margins before allocating additional resources.
- Examining product and channel performance to identify potential growth opportunities.
- Using actual-versus-budget comparisons to prioritize follow-up, where the underlying measures are comparable.

These are investigation areas, not confirmed conclusions or recommendations from completed results.

## Limitations and Future Improvements

- Validate source definitions and units before comparing sales, cost, profit, and budget values.
- Document how missing or duplicate records are handled.
- Confirm that lookup keys uniquely identify customers, products, and regions before joining tables.
- Add a reproducible data-cleaning pipeline if the workflow grows beyond a notebook.
- Extend the Power BI report with validated measures, drill-through pages, and documented filters.
- Consider automated data-quality checks for future refreshes.

## Project Status

- [x] Business problem and analysis scope defined
- [x] Data cleaning and validation documented
- [x] Exploratory analysis finalized
- [ ] Key findings and recommendations added
- [ ] Power BI dashboard completed
- [ ] Dashboard screenshots and documentation added

---

_This project is intended as a portfolio case study. Dataset attribution, licensing, and any applicable usage restrictions should be documented before public release._
