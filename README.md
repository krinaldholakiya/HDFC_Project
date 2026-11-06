<div align="center">

# -- ! HDFC Bank Performance Analytics Dashboard ! --
### *Interactive Power BI Report for Deposits, Loan Portfolio & Branch Performance*

[![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-Measures%20%26%20Time%20Intelligence-004C8F?style=for-the-badge&logo=microsoft&logoColor=white)](https://learn.microsoft.com/en-us/dax/)
[![Power Query](https://img.shields.io/badge/Power%20Query-ETL%20from%20CSV-0078D4?style=for-the-badge&logo=microsoftexcel&logoColor=white)](https://learn.microsoft.com/en-us/power-query/)
[![Data Model](https://img.shields.io/badge/Data%20Model-Star%20Schema-ED1C24?style=for-the-badge&logo=databricks&logoColor=white)](https://learn.microsoft.com/en-us/power-bi/guidance/star-schema)


## Video Link-https://drive.google.com/file/d/1czKl3FSc-GszWGMvTFMf_oYf7Ea6Wu1n/view?usp=sharing
<br/>

> *"Numbers become decisions the moment they are placed next to a target."*

</div>

---

## 📋 Table of Contents

- [📌 Overview](#-overview)
- [🎯 Problem Statement](#-problem-statement)
- [✨ Key Features](#-key-features)
- [🏗️ Project Structure](#️-project-structure)
- [🔄 Project Workflow](#-project-workflow)
- [🧱 Part A — Data Model & DAX](#-part-a--data-model--dax)
- [📊 Part B — Dashboard Pages](#-part-b--dashboard-pages)
- [🛠️ Tech Stack](#️-tech-stack)
- [📈 Results & Insights](#-results--insights)
- [🏆 Advantages](#-advantages)
- [📄 License](#-license)
- [👤 Author](#-author)
- [🙏 Acknowledgements](#-acknowledgements)

---

## 📌 Overview

The **HDFC Bank Performance Analytics Dashboard** is a multi-page, interactive **Power BI** report that analyses a banking dataset of **500 branches**, **100,000 accounts**, **500,000 transactions** and **150,000 loan repayments** across **8 cities**, **5 regions** and **10 banking products** (2023–2025). It demonstrates core business-intelligence concepts such as **star-schema modeling**, **DAX measures**, **target-vs-actual tracking**, **previous-year comparisons** and **executive-style visual storytelling**.

This project is designed to:
- Build a clean **star-schema data model** from raw CSV files using Power Query
- Practice writing **DAX measures** for deposits, loan book, EMI, NPA and branch KPIs
- Compare **actual deposits against branch targets** month by month
- Design a consistent, branded **1920 × 1080 dashboard** with navigation, slicers and insight panels

---

## 🎯 Problem Statement

> **Objective:** Build an interactive banking dashboard that helps management track deposit performance against targets, monitor the loan portfolio and compare branch performance.

You are building a reporting solution for a bank's regional and head-office teams. The report must let users slice data by **Year, Quarter, Month, Zone and Region**, and answer questions such as *"Are branches meeting their deposit targets?"*, *"How healthy is the loan book?"* and *"Which regions and branches lead?"*

| 📂 Dashboard Page | 📄 Type | 🔍 Description |
|-------------------|---------|----------------|
| Deposits vs Targets | Performance | Actual deposits vs targets, achievement %, YoY growth, city and region split |
| Loan Portfolio | Risk & Growth | Loan book, active loans, EMI collection, NPA %, product-wise breakdown |
| Branch Performance | Operational | Branch count, transactions, average transaction value, branch ranking |

The goal is to demonstrate **end-to-end Power BI skills** — from raw data to a polished, interactive banking report.

---

## ✨ Key Features

| Feature | Description |
|--------|-------------|
| 📑 **3 Report Pages** | Deposits vs Targets, Loan Portfolio and Branch Performance |
| 🧭 **Page Navigator** | Built-in navigation plus action buttons for moving between pages |
| 🎛️ **5 Slicers** | Year, Quarter, Month, Zone and Region filter the visuals |
| 📐 **Star Schema Model** | 4 dimension tables and 3 fact-style tables linked through Branch, Account and Date keys |
| 🧮 **50+ DAX Measures** | KPIs, previous-year comparisons, growth %, achievement % and dynamic labels |
| 🎯 **Target vs Actual** | `BranchDepositTargets` table enables achievement % and monthly target tracking |
| ▲▼ **Dynamic PY Subtitles** | Text measures like `Previous Year: ₹ 25,019 Cr ▲ 50.15%` sit under each KPI |
| 🏅 **Branch Ranking** | `RANKX` measure ranks branches by deposit target achievement |
| 🗺️ **Map Visuals** | City-level bubbles for deposits, loan book and deposit totals |
| 💡 **Key Insight Panels** | Narrative text boxes beside the charts summarising what the data says |
| 🖥️ **Fit-to-Page Layout** | All pages designed at 1920 × 1080 for presentation-ready viewing |

---

## 🏗️ Project Structure

```
📦 hdfc-bank-analytics/
│
├── 📄 HDFC-Project.pbix         ← Power BI report (model + 3 report pages)
│
├── 📁 Dataset/                  ← Source CSV files loaded through Power Query
│   ├── BranchDepositTargets.csv
│   ├── DimAccount.csv
│   ├── DimBranch.csv
│   ├── DimDate.csv
│   ├── DimProduct.csv
│   ├── FactLoanRepayments.csv
│   └── FactTransactions.csv
│
└── 📄 README.md                 ← Project documentation
```

> ℹ️ The `.pbix` file points to a local `Dataset` folder. After downloading, update the file path in **Transform data → Data source settings**.

---

## 🔄 Project Workflow

```
Raw CSV Files (7 tables)
          │
          ▼
┌─────────────────────────────┐
│   Power Query (ETL)         │  ← Promote headers, set data types
└────────────┬────────────────┘
             │
             ▼
┌─────────────────────────────┐
│   Data Model (Star Schema)  │  ← Relationships on Branch, Account
│                             │    and Date keys
└────────────┬────────────────┘
             │
             ▼
┌─────────────────────────────┐
│   DAX Measures              │  ← KPIs, targets, PY comparisons
└────────────┬────────────────┘
             │
     ┌───────┴────────┐
     ▼                ▼
┌─────────────┐   ┌──────────────────┐
│  Visuals    │   │ Slicers + Page   │
│  & Insights │   │ Navigation       │
└──────┬──────┘   └────────┬─────────┘
       │                   │
       ▼                   ▼
┌─────────────────────────────┐
│   3-Page Interactive Report │
└────────────┬────────────────┘
             │
             ▼
   Share / Publish to Power BI Service ✅
```

---

## 🧱 Part A — Data Model & DAX

### 📝 1. What is the Data Model?

The model follows a **star schema**: descriptive **dimension** tables (branch, account, product, date) surround the transactional **fact** tables (transactions, loan repayments) and a **targets** table. Slicers on a dimension filter every connected table.

---

### 🗺️ 2. Tables — Overview

| Table | Type | Key Columns | Rows (approx.) |
|-------|------|-------------|----------------|
| 🗓️ **DimDate** | Dimension | DateKey, Date, Year, Quarter, Month, MonthName | 1,096 (2023–2025) |
| 🏦 **DimBranch** | Dimension | BranchID, BranchName, City, Zone, Region, Latitude, Longitude | 500 |
| 👤 **DimAccount** | Dimension | AccountID, BranchID, ProductCode, CustomerName | 100,000 |
| 📦 **DimProduct** | Dimension | ProductCode, ProductName | 10 |
| 💸 **FactTransactions** | Fact | TransactionID, DateKey, AccountID, BranchID, ProductCode, TransactionType, Amount | 500,000 |
| 🏠 **FactLoanRepayments** | Fact | RepaymentID, DateKey, AccountID, BranchID, ProductCode, EMIAmount, OutstandingBalance | 150,000 |
| 🎯 **BranchDepositTargets** | Target | BranchID, Year, Month, DepositTarget, DateKey | 18,000 |

**Products:** Savings · Current · Salary · Fixed Deposit · Home Loan · Personal Loan · Vehicle Loan · Education Loan · Business Loan · Credit Card

**Transaction types:** Deposit · Withdrawal · ATM · UPI · NEFT · RTGS · EMI

---

### 🔗 3. Relationships

```
                       DimDate
                          ▲
                          │ DateKey
          ┌───────────────┼────────────────┐
          │               │                │
  FactTransactions  FactLoanRepayments  BranchDepositTargets
          │               │                │
          └───────────────┼────────────────┘
                          │ BranchID
                          ▼
                      DimBranch ◄──── DimAccount (BranchID)

FactTransactions    ──► DimAccount   (AccountID, inactive)
FactLoanRepayments  ──► DimAccount   (AccountID, inactive)
```

---

### 🧮 4. Core DAX Measures

**Deposits & Targets**
```dax
Total Deposits =
CALCULATE(SUM(FactTransactions[Amount]), FactTransactions[TransactionType] = "Deposit")

Deposit Target (Cr) = DIVIDE(SUM(BranchDepositTargets[DepositTarget]), 10000000)

Achievement % = DIVIDE([Total Deposits (Cr)], [Deposit Target (Cr)], 0)
```

**Loan Portfolio**
```dax
Total Loan Book (Cr) = DIVIDE(SUM(FactLoanRepayments[OutstandingBalance]), 10000000, 0)

Active Loans = DISTINCTCOUNT(FactLoanRepayments[AccountID])

Total EMI Collection (Cr) = DIVIDE(SUM(FactLoanRepayments[EMIAmount]), 10000000, 0)

NPA % = DIVIDE([Total NPA Amount], SUM(FactLoanRepayments[OutstandingBalance]), 0)
```

**Branch & Transaction KPIs**
```dax
Total Branches = DISTINCTCOUNT(DimBranch[BranchID])

Average Transaction Value =
DIVIDE(SUM(FactTransactions[Amount]), DISTINCTCOUNT(FactTransactions[TransactionID]), 0)

Branch Rank =
IF(ISINSCOPE(DimBranch[BranchName]),
   RANKX(ALLSELECTED(DimBranch[BranchName]), [Achievement %], , DESC, DENSE))
```

**Time Intelligence — Previous Year Comparison**
```dax
Previous Year Deposits =
CALCULATE([Total Deposits], SAMEPERIODLASTYEAR(DimDate[Date]))

Deposit Growth % =
DIVIDE([Total Deposits] - [Previous Year Deposits], [Previous Year Deposits], 0)

Loan Book Subtitle =
"Previous Year: ₹ " & FORMAT([Previous Year Loan Book (Cr)], "#,##0") &
" Cr   ▲ " & FORMAT([Loan Book Growth %], "0.00%")
```

**Key Concepts Used:**

| Concept | Detail |
|---------|--------|
| 🔁 `CALCULATE()` | Changes filter context (e.g., Deposit transactions only) |
| 🗓️ `SAMEPERIODLASTYEAR()` / `DATEADD()` | Previous-year and two-years-back comparisons |
| 🏅 `RANKX()` + `ISINSCOPE()` | Branch ranking that only appears at branch level |
| ➗ `DIVIDE()` | Safe division that avoids divide-by-zero errors |
| 🧾 `VAR … RETURN` | Readable intermediate calculations |
| 🔤 `FORMAT()` | Builds dynamic "Previous Year ▲▼" subtitles for KPI cards |

---

## 📊 Part B — Dashboard Pages

### 🗺️ 5. Pages — Overview

| # | Page | Main Visuals | Key Measures |
|---|------|--------------|--------------|
| 1️⃣ | **Deposits vs Targets** | KPI cards, actual-vs-target column chart, deposit trend line, region donut, city map, branch table | Total Deposits (Cr), Deposit Target (Cr), Achievement %, YoY Deposit Growth % |
| 2️⃣ | **Loan Portfolio** | KPI cards, loan-book treemap, active-loans bar & donut, EMI trend line, city map, branch matrix | Total Loan Book (Cr), Active Loans, EMI Collection (Cr), NPA % |
| 3️⃣ | **Branch Performance** | KPI cards, EMI-by-branch bar, transaction-type donut, transactions line, deposit & loan column chart by region, city map, matrix | Total Branches, Total Transactions (Mn), Average Transaction Value, Achievement % |

---

### 🎯 6. Deposits vs Targets

> Answers: *Are we meeting our deposit goals?*

- Cards for **Total Deposits, Deposit Target, Achievement % and YoY growth**, each with a previous-year subtitle
- Clustered column chart of **Actual Deposits vs Deposit Target by month**
- Deposit share by **Region** (donut) and by **City** (map)
- Branch table with deposits, target, achievement % and growth

---

### 🖼️ 1.Deposits vs Targets

<img src="Assets/Screenshot 2026-11-06 090404.png">



### 🏠 7. Loan Portfolio

> Answers: *How big and how healthy is the loan book?*

- Total loan book, active loans, EMI collection and **NPA %** with previous-year comparison
- Loan book by **product** (treemap) and active loans by product (bar and donut)
- EMI collection trend over time and a branch-level matrix of loan book, EMI and NPA

---

### 🖼️ 2.Loan Portfolio

<img src="Assets/Screenshot 2026-11-06 090521.png">


### 🏦 8. Branch Performance

> Answers: *Which regions and branches lead, and how active is the network?*

- Total branches, total transactions (in millions) and **average transaction value**
- Transaction mix by type (Deposit, Withdrawal, ATM, UPI, NEFT, RTGS, EMI)
- Deposits vs loan book by region and EMI collection by branch
- Branch matrix with deposits, loan book, transactions and achievement %

---
### 🖼️ 3.Branch Performance

<img src="Assets/Screenshot 2026-11-06 091556.png">



## 🛠️ Tech Stack

| Tool | Version | Purpose |
|------|---------|---------|
| 📊 **Power BI Desktop** | Latest | Report authoring and visualisation |
| 🧮 **DAX** | Built-in | Measures, KPIs, targets and time intelligence |
| 🔧 **Power Query (M)** | Built-in | Loading CSV files and setting data types |
| 🗃️ **CSV Files** | — | Source data for dimensions, facts and targets |
| 🗺️ **Map Visual** | Built-in | City-level geographic analysis |
| 🖼️ **PNG Icons** | — | Custom KPI and navigation icons inside the report |

---

## 📈 Results & Insights

After exploring the dashboard (data as on **30 Apr 2025**), the following insights are produced:

- 🏦 **Large Network** — **500 branches** across **8 cities** (Ahmedabad, Bengaluru, Chennai, Delhi, Hyderabad, Mumbai, Pune, Surat) and **5 regions**, with **North** having the most branches (116)
- 🏠 **Loan Book** — Total outstanding loan book is about **₹37,567 Cr**, with **~78K active loans**
- 💳 **EMI Collection** — About **₹382.67 Cr** collected, showing strong growth over the previous year
- 📉 **Asset Quality** — NPA % is reported at about **1.95%**, an improvement from **2.56%** in the previous year
- 🌍 **Regional Leaders** — **North** leads in both loan book and EMI collection, while **East** is the lowest in both
- 🔁 **Balanced Transaction Mix** — All seven transaction types stay within a narrow ~14% share each, with **EMI** the most used
- 🎯 **Target Tracking** — Monthly actual deposits are measured against branch targets, with branches ranked by achievement %
- 📈 **Growth Signals** — Transactions, active loans and loan book all show healthy previous-year growth

---

## 🏆 Advantages

| Advantage | Detail |
|-----------|--------|
| 🎓 **Portfolio Ready** | Covers modeling, DAX, targets, visual design and storytelling in one project |
| 🔄 **Reusability** | Measures follow a repeatable *Value → PY → Growth → Subtitle* pattern |
| 📚 **Educational** | Shows how star schema, relationships and filter context work together |
| 🧭 **Easy Navigation** | Page navigator and action buttons guide users across pages |
| 🎛️ **Fully Interactive** | Slicers cross-filter visuals; maps and charts drill into detail |
| 📏 **Scalable** | Handles 500K transactions and 150K loan records smoothly |
| 🧪 **Extensible** | Easy to add pages (Customer Segments, Risk, Forecasting) or new measures |
| 🛡️ **Safe Calculations** | `DIVIDE()` with default values prevents errors in KPI labels |

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for full details.

```
MIT License — Free to use, modify, and distribute with attribution.
```

---

## 👤 Author

<div align="center">

### Krinal Dholakiya

[![GitHub](https://img.shields.io/badge/GitHub-krinaldholakiya-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/krinaldholakiya)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/krinaldholakiya/)

> *"Every dashboard starts with a question — and the best ones answer it at a glance."*

**🎓 Role:** Data Analyst | Power BI Enthusiast \
**📍 Location:** India\
**🛠️ Skills:** Power BI · DAX · Power Query · Data Modeling · Dashboard Design

</div>

---

## 🙏 Acknowledgements

Special thanks to the following resources and communities that made this project possible:

- 📚 [Microsoft Power BI Docs](https://learn.microsoft.com/en-us/power-bi/) — Official Power BI reference
- 🧮 [DAX Guide](https://dax.guide/) — Complete DAX function reference
- 🔧 [Power Query M Docs](https://learn.microsoft.com/en-us/powerquery-m/) — M language reference
- ⭐ [Star Schema Guidance](https://learn.microsoft.com/en-us/power-bi/guidance/star-schema) — Data modeling best practices
- 📖 [SQLBI](https://www.sqlbi.com/) — In-depth DAX and modeling articles
- 💬 [Power BI Community](https://community.fabric.microsoft.com/) — Problem-solving support
- 🎨 [Flaticon](https://www.flaticon.com/) — Icon inspiration

---

<div align="center">

---

*Made with ❤️ — Last updated: 6 November, 2026*

</div>
