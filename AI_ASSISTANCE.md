# AI Assistance on This Project

## What was used
This project was built with help from **Claude** (Anthropic's AI assistant), used as a data-analysis and document-generation tool within a chat session. No IBM Bob AI or other AI coding agent was used.

## What Claude actually did

### 1. Data extraction & cleaning
- The source data arrived as a PDF export of a 500-row supermarket transaction table, with formatting issues from the PDF-to-text conversion (fields like category and quantity, or payment method and rating, were sometimes merged together with no space, e.g. `Snacks8`, `Card5`).
- Claude wrote a regex-based parser to correctly split these merged fields back into their own columns, then validated the result: 500/500 rows parsed successfully, and `Sales = Quantity × Unit Price` was cross-checked for every row with zero discrepancies.
- Checked the cleaned dataset for missing values and duplicate rows/invoice IDs (none found).

### 2. Exploratory data analysis
- Computed aggregations for product performance, branch profitability, category sales, payment method popularity, customer-type spend comparison, and rating distribution.
- Extended the analysis beyond the original brief with day-of-week trends, gender comparison, a correlation heatmap, a branch × category breakdown, and a unit-price-vs-sales scatter plot.
- Verified all computed figures matched the reference answers provided in the project brief (e.g. Cheese ₹27,906.30, Branch C Mumbai ₹72,469.45, UPI 127 transactions).

### 3. Chart generation
- Generated all 12 charts in this repo (`charts/`) using Matplotlib, styled consistently and exported at print quality.

### 4. Deliverable creation
- **`notebooks/Supermarket_Sales_Analysis.ipynb`** — wrote and executed the full analysis notebook (65 cells), including markdown commentary on each insight.
- **`reports/Supermarket_Sales_Report.docx`** — generated the business-facing Word report (executive summary, KPI table, findings with embedded charts, recommendations), then rendered it to PDF and visually reviewed it page-by-page to catch and fix a chart-embedding sizing bug before final delivery.
- **`dashboard/Supermarket_Sales_Dashboard.xlsx`** — built the Excel workbook with a KPI dashboard tab (native Excel charts), per-topic data tabs, and embedded heatmap images.
- **`data/supermarket_sales_clean.csv`** — the cleaned, validated dataset.

### 5. Business recommendations
- Drafted the six recommendations in the report, tied directly to the data findings (e.g. flagging that Branch A has both the lowest sales *and* the lowest rating, which wasn't explicitly asked for but stood out from the analysis).

## What Claude did not do
- Did not use any tool called "Bob AI" — that name refers to an IBM product this project did not use.
- Did not fix pre-existing code, since there was no pre-existing codebase — everything in `notebooks/`, `reports/`, and `dashboard/` was generated from scratch in this session.

## Verification
The notebook was executed end-to-end with zero errors before being included in this repo. The Word report was rendered to PDF and checked page-by-page. The Excel workbook was reopened and validated after each edit. The full zip archive was integrity-tested before delivery.
