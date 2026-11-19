# 📊 Finance Analytics & Digital Banking Performance Dashboard

[![Live Dashboard](https://img.shields.io/badge/Live_Dashboard-View_Interactive_Report-0078D4?style=for-the-badge&logo=powerbi&logoColor=white)](https://app.powerbi.com/view?r=eyJrIjoiMTQ5OTY0YTctN2I2NC00NzMxLWE1NzItZDU2MTA0YTFkZjY2IiwidCI6IjUxMzRkZDExLWZlNDEtNGY3My1iODIyLTg0NDljN2Y1MzA4MCJ9)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Measures_&_Formulas-00758F?style=for-the-badge)
![Domain](https://img.shields.io/badge/Domain-Banking_&_Payments-2ea44f?style=for-the-badge)

An interactive, enterprise-grade **Power BI Commercial Banking & Digital Payments Analytics Dashboard** designed to evaluate transaction velocity, diagnose operational payment settlement failures, and uncover customer segment profitability across **50,069 multi-channel transactions** and **₹45.61 Crore ($5.5M+) in gross transaction turnover**.

> 🔗 **Live Interactive Report**: [Click here to view the live published dashboard](https://app.powerbi.com/view?r=eyJrIjoiMTQ5OTY0YTctN2I2NC00NzMxLWE1NzItZDU2MTA0YTFkZjY2IiwidCI6IjUxMzRkZDExLWZlNDEtNGY3My1iODIyLTg0NDljN2Y1MzA4MCJ9)

---

## 📌 Business Problem & Objectives

### The Business Context
In commercial retail banking and payment operations, financial institutions process millions of daily transactions across diverse rails—including **UPI, Mobile Banking, Net Banking, Point-of-Sale (POS), ATMs, Auto Debit, and physical Branches**. Without centralized business intelligence, banking executives and operations managers face critical blind spots:

1. **Payment Settlement & Failure Friction**: Inability to isolate where and why transactions fail (terminal failures vs. clearing delays), causing customer friction and revenue loss.
2. **High-Value Drop-Off Cliffs**: Lack of visibility into why high-ticket payments drop off at significantly higher rates, impacting VIP and corporate clientele.
3. **Geographic Concentration Risk**: Difficulty tracking regional revenue distribution across Indian states to identify saturated vs. underpenetrated growth markets.
4. **Product-Level Take-Rate Economics**: Inability to evaluate net fee yields and tax collections across distinct transaction categories (Loan EMIs, Deposits, Transfers, Card Payments, and Fee Charges).

### The Analytical Solution
This Power BI reporting system was engineered to deliver actionable, data-driven answers across two core analytical levels:
* **Overview Analysis Dashboard**: High-level portfolio tracking, real-time KPI scorecards with Prior Year (PY) and Year-over-Year (YoY) variances, state-level performance benchmarking, monthly seasonality, and customer segment analysis enabled by dynamic **Field Parameters** (`Metric`).
* **Transactions Audit & Drill-Through Dashboard**: Row-level audit ledger allowing operational teams to seamlessly drill through from high-level visual charts down into granular settlement records by Customer Name, State, Category, and Transaction Status.

---

## 🖼️ Dashboard Preview

| Overview Analysis (Executive & Portfolio Health) | Transactions (Drill-Through Audit View) |
| :---: | :---: |
| ![Overview Analysis](assets/overview_view.png) | ![Transactions View](assets/transactions_view.png) |

---

## 📈 Key Performance Indicators (KPI Summary)

### 1. Overall Portfolio Scale & Health (Full Time-Series)
| Metric | Measure Name | Value | Formatted Display | Business Meaning |
| :--- | :--- | :---: | :---: | :--- |
| **Gross Transaction Value (GTV)** | `Total Amount` | **₹456,141,514.47** | **₹45.61 Cr** (456.1M) | Total money processed across all rails |
| **Total Transactions** | `Total Transaction` | **50,069** | **50.1K** | Total volume of executed payments |
| **Average Transaction Value (ATV)** | `Avg Transaction Value`| **₹9,110.26** | **9.11K** | Mean transaction size |
| **Total Service Fees** | `Total Fees` | **₹727,094.06** | **727.1K** | Net operational fee revenue captured (15.9 bps take-rate) |
| **Total Statutory Tax** | `Total Tax` | **₹130,952.41** | **131.0K** | Total GST / TDS deducted |
| **Customer Retention** | `Active Customer Base` | **3,983 active** | **79.7%** | 3,983 transacting users vs. 1,017 inactive (20.3% dormant) |

---

### 2. FY 2025 Focused Performance (Dashboard Baseline)
*Matches the exact live online dashboard display:*

| KPI Card | Current 2025 Value | Prior Year (PY 2024) | YoY % Change | Status Indicator |
| :--- | :---: | :---: | :---: | :---: |
| **Total Amount** | **₹ 137.53M** | 135.62M | **+1.40%** | 🟢 Upward Growth |
| **Total Transactions** | **14.94K** | 15.03K | **-0.57%** | 🟡 Stable Volume |
| **Avg Transaction Value** | **9.20K** | 9.02K | **+1.99%** | 🟢 Higher Ticket Size |
| **Total Fees** | **₹ 216.94K** | 217.32K | **-0.17%** | 🟡 Steady Revenue |
| **Total Tax** | **39.04K** | 39.15K | **-0.27%** | 🟡 Steady Collection |

---

### 3. Settlement Status Performance Grid (FY 2025)
| Transaction Status | Volume (Txns) | Share (%) | Amount (INR) | Value Share (%) | Operational Impact |
| :--- | :---: | :---: | :---: | :---: | :--- |
| **Success** | 12,846 | 85.85% | 117.56M | 85.38% | Cleanly settled transactions |
| **Failed** | 1,517 | **10.14%** | **14.37M** | **10.44%** | Technical drops, timeouts & card limits |
| **Pending** | 601 | 4.02% | 5.76M | 4.18% | Clearing pipeline latency / gateway delays |
| **Total At-Risk (Failed + Pending)**| **2,118** | **14.15%** | **20.13M** | **14.62%** | **Total capital exposed to operational friction** |

---

## 🔍 Deep Analytical Insights

### 1. Payment Failure Diagnostics & High-Ticket Drop-Off
* In 2025, **10.4% of total volume (14M across 1,517 transactions) resulted in terminal failure**, with an additional **4.2% (6M) stuck in pending status**, creating a total of **20M in at-risk throughput**.
* **High-Ticket Cliff**: While transactions below ₹50,000 exhibited a stable ~10% failure rate, **transactions exceeding ₹100,000 spiked to a 21.7% failure rate** (5 out of 23 failed), pinpointing daily bank transfer caps and 2FA authentication timeouts on high-value settlements.

### 2. Geographic Clustering (Top 6 States = 67% of Volume)
* In 2025, **66.9% (~67%) of total turnover (92M out of 138M)** was concentrated in just 6 states:
  1. **Maharashtra:** **22M** (21.81M — 15.8%)
  2. **Karnataka:** **16M** (15.96M — 11.6%)
  3. **Gujarat:** **15M** (15.38M — 11.2%)
  4. **Tamil Nadu:** **14M** (13.83M — 10.0%)
  5. **Uttar Pradesh:** **13M** (13.18M — 9.6%)
  6. **Madhya Pradesh:** **12M** (12.02M — 8.7%)
* *Strategic Implication:* High clustering in urban economic centers exposes the institution to regional policy/economic shocks, while high-growth markets like Rajasthan (6.55M), West Bengal (6.33M), and Telangana (5.56M) represent clear expansion opportunities.

### 3. Product Mix & Debt Servicing Dominance
* Across the full portfolio, **Loan EMIs (₹131.1M / 28.8%)** and **Fund Transfers (₹120.9M / 26.5%)** account for **55.24% of all monetary turnover**.
* *Behavioral Finding:* Customers primarily utilize this institution as a debt-servicing and money-movement rail, leaving merchant card spend (₹26.9M / 5.9%) under-monetized.

### 4. Customer Acquisition & Dormancy Gap
* Out of 5,000 registered accounts, **1,017 customers (20.34%) have zero lifetime transactions**, highlighting significant Customer Acquisition Cost (CAC) leakage due to a lack of structured onboarding activation nudges.

### 5. Segment Value Disparity (Volume vs. Margin)
* **Retail** accounts for **55.0% of 2025 volume (75.8M across 8,143 transactions)**.
* However, **Premium (25.7M / 2,781 txns)** and **SME (21.1M / 2,369 txns)** clients generate the highest annual customer value (**>₹1.18 Lakhs per user**), proving that retaining business and affluent tiers yields higher lifetime revenue per account.

---

## 🛠️ Data Model & Technical Implementation

* **Schema Architecture**: Built on a relational **Star Schema** centered on the `finance_transactions` fact table:
  * `customers` (Dimension) $\xrightarrow{1:\infty}$ `finance_transactions` on `customer_id`
  * `calendar table` (Dimension) $\xrightarrow{1:\infty}$ `finance_transactions` on `transaction_date`
  * `Metric` (Field Parameter table) for dynamic visual measure switching
* **DAX Implementation**: 15+ custom DAX measures utilizing `CALCULATE`, `SAMEPERIODLASTYEAR`, `DIVIDE`, and variable logic (see [DAX_Measures.md](DAX_Measures.md) for full formulas).
* **Dynamic Field Parameters (`Metric`)**: Enables stakeholders to toggle bar charts and categorical visuals between *Total Amount*, *Total Transaction*, *Total Fees*, *Total Tax*, and *Avg Transaction Value* dynamically.
* **Two-Tier Drill-Through Architecture**: Users can right-click any customer segment, state, or transaction type on Page 1 and drill through to Page 2 with filtered audit records preserved.
* **Power Query ETL**: Implemented data hygiene transformations to trim whitespace anomalies across channels, resolve typographic artifacts (`M@bile App`), standardize currency codes, and establish a custom date dimension table.

---

## 📂 Repository Structure

```text
├── assets/
│   ├── overview_view.png              # Page 1: Executive Overview screenshot
│   └── transactions_view.png          # Page 2: Transactions Audit Grid screenshot
├── DAX_Measures.md                    # Complete DAX formulas & technical reference
├── Finance_Analytics_Dashboard.pbix   # Complete interactive Power BI report file
├── .gitignore                         # Git exclusion rules for Power BI & cache files
└── README.md                          # Master project documentation
```

---

## 🚀 How to Open and Explore

1. **View the Live Dashboard (No installation required):**
   * [Open the interactive Power BI report in your browser](https://app.powerbi.com/view?r=eyJrIjoiMTQ5OTY0YTctN2I2NC00NzMxLWE1NzItZDU2MTA0YTFkZjY2IiwidCI6IjUxMzRkZDExLWZlNDEtNGY3My1iODIyLTg0NDljN2Y1MzA4MCJ9).
2. **Explore locally via Power BI Desktop:**
   * Clone this repository:
     ```bash
     git clone https://github.com/Curious011/Finance-Analytics-Dashboard.git
     ```
   * Download and install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free).
   * Open `Finance_Analytics_Dashboard.pbix` to interact with the local data model, slicers, and drill-through features.

---

## 👤 Author
* **Harsh Sharma**
* **Project**: Commercial Banking & Digital Payments Performance Analytics
* **Tools**: Power BI, DAX, Power Query, Financial Data Analysis
