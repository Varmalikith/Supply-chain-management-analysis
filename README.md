# 📦 Supply Chain Analysis Project
### End-to-End Data Analytics Portfolio Project | DataCo Global Dataset

---

## 📌 Project Overview

This project performs a complete end-to-end supply chain analysis on the **DataCo Global Supply Chain Dataset** — covering 180,519 real transactions across 5 global markets, 50+ product categories, and 4 shipping modes (2015–2018).

The goal is to identify delivery bottlenecks, analyse profitability, detect root causes of late deliveries, and build a machine learning model to predict delivery risk before shipment.

---

## 📊 Key Business Metrics

| Metric | Value |
|---|---|
| Total Orders | 180,519 |
| Total Sales | $36.78M |
| Total Profit | $3.97M |
| Profit Margin | 10.78% |
| Late Delivery Rate | 57.3% |
| Avg Delay (Late Orders) | 1.62 days |
| Top Market | Europe |
| Top Category | Fishing |
| Worst Region | Central Asia |
| ML Model Accuracy | 69.6% |

---

## 🗂️ Project Structure

```
supply-chain-analysis/
│
├── DataCoSupplyChainDataset.csv       # Raw dataset (180,519 rows × 53 columns)
├── supply_chain_analysis.py           # Main analysis script (all 6 steps + 11 charts)
├── Supply_Chain_Analysis_Report.pdf   # Full professional PDF report
├── README.md                          # This file
│
└── charts/
    ├── 01_delivery_status.png
    ├── 02_sales_by_category.png
    ├── 03_shipping_mode_analysis.png
    ├── 04_market_performance.png
    ├── 05_time_series.png
    ├── 06_bottleneck_detection.png
    ├── 07_root_cause_analysis.png
    ├── 08_profit_analysis.png
    ├── 09_heatmap.png
    ├── 10_order_status_segment.png
    └── 11_ml_results.png
```

---

## 🔬 Analysis Pipeline

### Step 1 — Data Loading & First Look
- Load 180,519 rows × 53 columns
- Inspect data types, shape, and sample records

### Step 2 — Exploratory Data Analysis (EDA)
- Delivery status distribution
- Sales by product category (Top 15)
- Missing value identification

### Step 3 — Data Cleaning & Feature Engineering
- Parse order and shipping dates
- Create `Shipping Delay`, `Is_Late`, `Year`, `Month`, `Quarter`, `Profit_Flag`, `Revenue_per_unit`
- Validate late delivery rate and profitable order share

### Step 4 — Bottleneck Detection
- Average shipping delay by region (Top 12)
- Late delivery rate by product category (Top 12)
- Identified Central Asia as worst-performing region

### Step 5 — Root Cause Analysis
- Correlation matrix of operational features vs. late delivery
- Late rate by customer segment
- Department-level sales vs. profit comparison

### Step 6 — Machine Learning (Late Delivery Risk Prediction)
- Model: **Random Forest Classifier** (150 trees, max depth 12)
- Train/Test Split: 80/20 stratified
- Accuracy: **69.6%** on 36,104 held-out orders
- Top features: scheduled shipping days, shipping mode, discount rate

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python 3 | Core language |
| Pandas | Data loading, cleaning, feature engineering |
| NumPy | Numerical operations |
| Matplotlib | Charts and visualisations |
| Seaborn | Heatmaps and advanced plots |
| Scikit-Learn | Random Forest model, evaluation metrics |
| ReportLab | PDF report generation |

---

## ⚙️ How to Run

### 1. Clone the Repository
```bash
git clone https://github.com/Varmalikith/supply-chain-analysis.git
cd supply-chain-analysis
```

### 2. Install Dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn reportlab
```

### 3. Run the Analysis
```bash
python supply_chain_analysis.py
```

### 4. Outputs
- All 11 charts saved to `charts/` folder
- `Supply_Chain_Analysis_Report.pdf` generated automatically

---

## 📈 Charts Generated

| # | Chart | Insight |
|---|---|---|
| 1 | Delivery Status Distribution | 57.3% late delivery rate identified |
| 2 | Top 15 Categories by Sales | Fishing leads revenue at $36.8M total |
| 3 | Shipping Mode Analysis | Standard Class drives highest late volume |
| 4 | Market Performance | Europe is top market; Africa smallest |
| 5 | Time Series (Monthly + Annual) | Consistent YoY growth with Q4 seasonality |
| 6 | Bottleneck Detection | Central Asia worst region; Golf Bags worst category |
| 7 | Root Cause Analysis | Shipping delay (r=0.816) is top driver |
| 8 | Profit Analysis | 10.78% margin; Fan Shop leads departments |
| 9 | Late Delivery Heatmap | Second Class + Q4 = highest risk combo |
| 10 | Order Status & Segment | Consumer segment drives highest revenue |
| 11 | ML Feature Importance & Confusion Matrix | 69.6% accuracy on real data |

---

## 🔍 Key Findings

- **57.3% late delivery rate** is 3–4× above the industry benchmark of 15–20%
- **Central Asia** is the worst-performing region with +0.65 days average delay
- **Golf Bags & Carts** has the highest category-level late rate at 68.9%
- **Shipping Delay** is the strongest predictor of late delivery risk (r = 0.816)
- **Europe** leads all markets in sales volume
- **Q4** consistently shows elevated late rates — pre-emptive carrier booking recommended
- Machine learning model can flag ~70% of late deliveries **before shipment**

---

## 💡 Business Recommendations

1. **🔴 CRITICAL** — Audit carrier contracts for Central Asia routes and implement dynamic routing for Standard Class
2. **🟡 HIGH** — Renegotiate Second Class SLAs; route high-value orders through premium carriers in Q4
3. **🟢 MEDIUM** — Invest in regional DC capacity in Europe to protect market leadership
4. **🔵 ML DEPLOY** — Embed the Random Forest model as a pre-shipment risk score in the order management system
5. **🟣 GROWTH** — Separate logistics strategies for bulky categories (Golf, Fishing, Water Sports)

---

## 📁 Dataset

- **Source:** [DataCo Smart Supply Chain Dataset — Kaggle](https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis)
- **Records:** 180,519 transactions
- **Features:** 53 columns
- **Period:** January 2015 – January 2018
- **Markets:** LATAM, Europe, Pacific Asia, USCA, Africa

---

## 👤 Author

**Likith Varma**  
MBA Candidate — Business Analytics | Woxsen University  
Data Analyst Intern — Bluestock Fintech Pvt. Ltd.  
GitHub: [github.com/Varmalikith](https://github.com/Varmalikith)

---

## 📄 License

This project is for educational and portfolio purposes.  
Dataset credit: DataCo Global via Kaggle.
