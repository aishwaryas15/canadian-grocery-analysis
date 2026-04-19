🛒 Canadian Grocery Inflation Crisis 2020–2026
> **How much more Canadians pay for groceries — and who profited**
A full-stack data analysis project examining 6 years of Canadian grocery price data, corporate profit growth, and affordability erosion. Built with Python, SQL, and Power BI.
![Dashboard Preview](assets/page1_national_overview.png)
---
📌 Key Findings
Metric	Value
Standard grocery basket increase (2020→2026)	+36.0%
Peak basket cost	$129.63 (Aug 2025)
Big 3 grocer combined profit growth	+39.4%
Hours of work to buy groceries (2023 peak)	4.07 hrs (up from 3.52 in 2020)
Worst single item increase	Pork shoulder +145%
Food items up over 50% since 2020	39 items
Loblaws margin vs Food CPI correlation	r = 0.848
Food inflation vs general inflation gap	+11 percentage points
---
📊 Dashboard Pages
Page 1 — National Overview
KPI cards, monthly basket cost timeline, top 10 price increases, greedflation evidence, corporate profit comparison
Page 2 — Category Deep Dive
Heatmap of every item every year, category inflation waves, price volatility scatter chart, most unstable items ranking
Page 3 — The Human Cost
Basket cost as % of monthly wage, hours of work to buy groceries, year-by-year cost waterfall, full affordability index table
---
🗂️ Project Structure
```
canadian-grocery-analysis/
│
├── data/
│   ├── raw/
│   │   ├── cpi_categories.csv
│   │   ├── food_prices.csv
│   │   └── corporate_profits.csv
│   │
│   └── processed/
│       ├── basket_cost_monthly.csv
│       ├── category_inflation.csv
│       ├── greedflation_correlation.csv
│       ├── combined_grocer_profits.csv
│       ├── affordability_index.csv
│       ├── item_volatility.csv
│       ├── food_prices_clean.csv
│       ├── cpi_clean.csv
│       ├── corporate_profits_clean.csv
│       └── max_pct_changes.csv
│
├── notebooks/
│   └── canadian_grocery_analysis.ipynb
│
├── powerbi/
│   └── canadian_grocery_dashboard.pbix
│
├── assets/
│   ├── page1_national_overview.png
│   ├── page2_category_deep_dive.png
│   └── page3_human_cost.png
│
├── canadian_grocery_inflation_summary.pdf
└── README.md
```
---
🔍 Detailed Findings
Basket Cost Analysis
A standard 20-item grocery basket cost $93.02 in February 2020. By February 2026 it cost $126.49 — a 36% increase. The basket peaked at $129.63 in August 2025, and prices have never returned to pre-pandemic baseline levels.
Biggest Price Increases
Food Item	2020 Price	Peak Price	Increase
Pork shoulder, per kg	$4.05	$9.93	+145%
Olive oil, 1 litre	$6.37	$17.14	+118%
Cantaloupe, unit	$2.18	$4.65	+112%
Strawberries, 454g	$2.90	$6.74	+111%
Beef striploin, per kg	$18.43	$38.27	+102%
Iceberg lettuce, unit	$1.89	$4.35	+99%
White sugar, 2kg	$1.70	$3.36	+98%
Category Breakdown
Category	2022 YoY	2023 YoY	Peak Year
Pantry	+20.1%	+13.0%	2022
Meat	+10.4%	+3.5%	2022 & 2025
Dairy	+8.7%	+5.8%	2022
Produce	+8.2%	+4.1%	2022
2022 was the simultaneous crisis year — every category spiked together.
Greedflation Analysis
Pearson correlation between Loblaws profit margin and Food CPI: r = 0.848
Combined Big 3 (Loblaws, Sobeys, Metro) net profit: $3.15B (2020) → $4.39B (2024)
Profit growth of +39.4% almost exactly matched basket cost growth of +36%
Loblaws margin expanded from 3.4% → 4.2% during the inflation crisis
Affordability Index
Year	Basket Cost	Hours to Buy	% of Monthly Wage
2020	$96.74	3.52 hrs	2.13%
2021	$101.07	3.56 hrs	2.13%
2022	$114.07	3.86 hrs	2.32%
2023	$122.47	4.07 hrs	2.39%
2024	$124.06	4.02 hrs	2.34%
2025	$125.62	3.99 hrs	2.30%
2026	$124.85	3.96 hrs	2.28%
Wages grew +20.1% while groceries grew +36% — a permanent 16-point affordability gap.
---
🛠️ Tools & Technologies
Tool	Purpose
Python 3.12	Data cleaning, transformation, analysis
pandas	Data manipulation and aggregation
SQLite	Relational database and SQL queries
Jupyter Notebook	Reproducible analysis pipeline
Power BI Desktop	Interactive 3-page dashboard
---
📁 Data Sources
Source	Description	Table
Statistics Canada 18-10-0004-01	Monthly CPI by category	cpi_data
Statistics Canada 18-10-0245-01	Retail food prices 110 items	food_prices
Yahoo Finance + Annual Reports	Loblaws, Sobeys, Metro financials	corporate_profits
Statistics Canada 14-10-0063-01	Average weekly earnings	affordability_index
---
🚀 How to Run
1 — Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/canadian-grocery-analysis.git
cd canadian-grocery-analysis
```
2 — Install dependencies
```bash
pip install pandas numpy sqlite3 jupyter
```
3 — Run the notebook
```bash
jupyter notebook notebooks/canadian_grocery_analysis.ipynb
```
Run all cells in order — Phase 1 loads and cleans data, Phase 2 runs analysis.
4 — Open the dashboard
Open `powerbi/canadian_grocery_dashboard.pbix` in Power BI Desktop
All data connections point to `data/processed/` folder
If prompted to refresh data, click Refresh
---
💡 Methodology
Basket Definition: 20 representative items selected across Meat, Dairy, Pantry and Produce categories. Baseline set at February 2020 (pre-pandemic). All percentage changes calculated relative to this baseline.
Greedflation Correlation: Pearson correlation coefficient calculated between Loblaws annual profit margin and annual average Food CPI. A coefficient above 0.7 is considered a strong positive relationship.
Affordability Index: Basket cost divided by approximate monthly wage (Statistics Canada average weekly earnings × 52 / 12). Hours calculated by dividing basket cost by average hourly wage for that year.
Volatility Measurement: Coefficient of Variation (standard deviation / mean × 100) used to measure price instability independent of price level. Higher CV% means more unpredictable pricing.
---
📬 Connect
If you found this project interesting, feel free to connect on LinkedIn or reach out with questions.
---
Data current as of February 2026. All prices in Canadian dollars.
