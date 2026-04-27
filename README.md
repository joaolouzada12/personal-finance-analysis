# 📊 Personal Finance Analysis

> Exploratory data analysis of personal financial transactions to understand spending patterns, income behavior, and financial habits over time.

---

## 📁 Project Structure

```
personal-finance-analysis/
│
├── data/
│   └── raw/
│       └── personal_transactions.csv
│
├── images/
│   ├── expenses_category.png
│   ├── monthly_expenses.png
│   └── monthly_balance.png
│
├── notebooks/
│   └── analysis.ipynb
│
└── README.md
```

---

## 🗂️ Dataset

**Source:** [Personal Finance Dataset — Kaggle](https://www.kaggle.com/datasets/bukolafatunde/personal-finance)

The dataset contains individual financial transactions with the following columns:

| Column | Description |
|---|---|
| `Date` | Transaction date |
| `Description` | Transaction description |
| `Amount` | Transaction value |
| `Transaction Type` | `credit` or `debit` |
| `Category` | Spending/income category |
| `Account Name` | Account identifier |

---

## 🛠️ Tech Stack

- **Python 3**
- **Pandas** — data manipulation and aggregation
- **NumPy** — conditional classification logic
- **Matplotlib** — chart rendering
- **Seaborn** — statistical visualizations

---

## 🔍 Methodology

### 1. Data Cleaning & Preparation
- Date parsing from string to `datetime`
- Validation of missing values (none found)
- Extraction of temporal features: year, month, day of week, year-month period

### 2. Transaction Classification

Transactions were classified into four types using `np.select`:

| Class | Criteria |
|---|---|
| `income` | `credit` + Category = `Paycheck` |
| `expense` | `debit` transactions |
| `transfer` | Category = `Credit Card Payment` |
| `other` | Remaining credit transactions |

### 3. Analysis Modules

- **Expenses by Category** — identifying the main cost drivers
- **Monthly Expense Trend** — tracking spending evolution over time
- **Monthly Income Trend** — evaluating earnings consistency over time
- **Monthly Balance** — net financial position (income − expenses) per month

---

## 📊 Key Findings

### 💸 Spending Distribution
- **Housing (Mortgage & Rent)** is the largest expense category, reflecting a high fixed-cost structure
- **Home Improvement** ranks second, suggesting either a renovation period or seasonal behavior
- Essential categories (Groceries, Utilities, Restaurants) show relatively stable and similar spending levels

### 📈 Expense Trend
- Monthly expenses remain mostly stable between **$2,000–$2,500**
- Two significant spending spikes occur around **mid-2018 and mid-2019**, likely due to extraordinary events (renovations, travel)
- A slight increase is noticeable in **November–December**, consistent with holiday seasonality

### ⚖️ Monthly Balance
- The financial balance is **positive in most months**, indicating a sustainable financial situation
- A **significant negative balance in mid-2018** aligns with the previously identified expense spike
- Balance fluctuations are primarily driven by **expense variability** rather than income changes, which remains consistent throughout the period

---

## ▶️ How to Run

1. Clone this repository
```bash
git clone https://github.com/joaolouzada12/personal-finance-analysis.git
cd personal-finance-analysis
```

2. Install dependencies
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

3. Download the dataset from Kaggle and place it at `data/raw/personal_transactions.csv`

4. Open and run the notebook
```bash
jupyter notebook notebooks/analysis.ipynb
```

---

## 📌 Author

Developer by **[João Louzada]**  
[Joao Louzada - Linkedin](https://www.linkedin.com/in/jo%C3%A3o-louzada-402503219/) · [joaolouzada12 - GitHub](https://github.com/joaolouzada12)
