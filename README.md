# Supermarket Sales Analysis

**Data Analytics & AI Internship Project — Business Intelligence / EDA Track**

Analysis of 500 supermarket sales transactions (Jan–Jul 2026, branches in Jaipur, Delhi, Mumbai, and Bengaluru) to uncover customer purchasing behavior, product performance, branch profitability, and payment preferences, translated into actionable business recommendations.

## 📁 Repository Structure

```
├── data/
│   └── supermarket_sales_clean.csv       # Cleaned, validated dataset (500 rows)
├── notebooks/
│   └── Supermarket_Sales_Analysis.ipynb  # Full EDA in Python (Pandas/NumPy/Matplotlib)
├── reports/
│   └── Supermarket_Sales_Report.docx     # Business report with charts & recommendations
├── dashboard/
│   └── Supermarket_Sales_Dashboard.xlsx  # Excel KPI dashboard with pivot tables & charts
├── charts/
│   └── *.png                             # All 12 exported chart images
└── README.md
```

## 🎯 Objective

Analyze historical retail transaction data to answer:
1. Which product generates the highest sales?
2. Which branch performs best?
3. Which category sells the most?
4. What is the most popular payment method?
5. Do Members spend more than Normal customers?
6. What is the average customer rating?

Plus extended analysis on gender, day-of-week patterns, correlation between variables, and branch × category performance.

## 🔑 Key Findings

| Question | Answer |
|---|---|
| Top product | **Cheese** — ₹27,906.30 |
| Top branch | **Branch C, Mumbai** — ₹72,469.45 |
| Top category | **Beverages** — ₹56,108.24 |
| Most popular payment | **UPI** — 127 transactions (25.4%) |
| Members vs. Normal spend | **No** — Normal customers average ₹497.07/txn vs. ₹483.14 for Members |
| Average rating | **3.99 / 5** |

**Additional insight:** Branch A (Jaipur) has both the lowest sales *and* the lowest average rating (3.84), while Branch D (Bengaluru) has the highest rating (4.09) despite not leading on revenue — suggesting a service-quality gap at Branch A worth investigating.

## 🧹 Data Quality

- 500 rows, 13 columns, **zero missing values**, **zero duplicate rows/invoice IDs**
- `Sales = Quantity × Unit Price` validated for all 500 rows with zero discrepancies

## 💡 Business Recommendations

1. Optimize inventory around top performers (Cheese, Dairy, Beverages), especially ahead of the April sales peak.
2. Study and replicate Branch C's (Mumbai) success at the underperforming Branch A (Jaipur).
3. Strengthen digital payment infrastructure — UPI, Net Banking, and Card already make up ~76% of transactions.
4. Grow basket size among Members (who already visit more often) via bundles and cross-category coupons.
5. Investigate the service-quality gap at Branch A through operational review or mystery-shopper audits.
6. Launch a rating-uplift initiative targeting checkout speed, staff training, and store layout.

## 🛠️ Tools Used

- **Python:** Pandas, NumPy, Matplotlib
- **Jupyter Notebook** for reproducible EDA
- **Microsoft Excel** (openpyxl) for the KPI dashboard
- **Microsoft Word** for the stakeholder-facing report

## ▶️ How to Reproduce

```bash
pip install pandas numpy matplotlib jupyter
jupyter notebook notebooks/Supermarket_Sales_Analysis.ipynb
```

---
*Prepared as part of a Data Analytics & AI Internship program (IBM SkillsBuild / BharatCares track).*
