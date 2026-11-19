# DAX Measures Reference

All core business logic, KPIs, and time-intelligence calculations are modeled using DAX (Data Analysis Expressions) within Power BI Desktop.

---

## 1. Core Portfolio KPIs

### Total Amount
Calculates the gross monetary volume across all transactions.
```dax
Total Amount = SUM(finance_transactions[amount])
```

### Total Transactions
Counts the total number of executed transaction records.
```dax
Total Transaction = COUNTROWS(finance_transactions)
```

### Average Transaction Value (ATV)
Computes the mean transaction size with division safeguards.
```dax
Avg Transaction Value = 
DIVIDE(
    [Total Amount],
    [Total Transaction],
    0
)
```

### Total Fees
Sums the operational fee revenue captured by the institution.
```dax
Total Fees = SUM(finance_transactions[fee_amount])
```

### Total Tax
Calculates the statutory tax liabilities (GST / TDS) processed.
```dax
Total Tax = SUM(finance_transactions[tax_amount])
```

---

## 2. Time-Intelligence & Year-over-Year (YoY) Calculations

### Prior Year (PY) Amount
```dax
PY Amount = 
CALCULATE(
    [Total Amount],
    SAMEPERIODLASTYEAR('calendar table'[Date])
)
```

### YoY % Growth (Amount)
```dax
YOY % Amount = 
VAR CurrentAmount = [Total Amount]
VAR PriorAmount = [PY Amount]
RETURN
DIVIDE(
    CurrentAmount - PriorAmount,
    PriorAmount,
    0
)
```

### Prior Year (PY) Transactions
```dax
PY Transaction = 
CALCULATE(
    [Total Transaction],
    SAMEPERIODLASTYEAR('calendar table'[Date])
)
```

### YoY % Growth (Transactions)
```dax
YOY % Transaction = 
VAR CurrentTxns = [Total Transaction]
VAR PriorTxns = [PY Transaction]
RETURN
DIVIDE(
    CurrentTxns - PriorTxns,
    PriorTxns,
    0
)
```

### Prior Year (PY) Fees & YoY % Growth
```dax
PY Fees = 
CALCULATE(
    [Total Fees],
    SAMEPERIODLASTYEAR('calendar table'[Date])
)

YOY % Fees = 
DIVIDE(
    [Total Fees] - [PY Fees],
    [PY Fees],
    0
)
```

### Prior Year (PY) Tax & YoY % Growth
```dax
PY Tax = 
CALCULATE(
    [Total Tax],
    SAMEPERIODLASTYEAR('calendar table'[Date])
)

YOY % Tax = 
DIVIDE(
    [Total Tax] - [PY Tax],
    [PY Tax],
    0
)
```

---

## 3. Dynamic Field Parameters (`Metric.Metric`)

To enable seamless 1-click measure switching without cluttering the canvas, Power BI **Field Parameters** were implemented:

```dax
Metric = {
    ("Total Amount", NAMEOF('finance_transactions'[Total Amount]), 0),
    ("Total Transaction", NAMEOF('calendar table'[Total Transaction]), 1),
    ("Total Fees", NAMEOF('calendar table'[Total Fees]), 2),
    ("Total Tax", NAMEOF('calendar table'[Total Tax]), 3),
    ("Avg Transaction Value", NAMEOF('calendar table'[Avg Transaction Value]), 4)
}
```
This enables users to dynamically toggle the **State** and **Customer Segment** charts across volume, value, fee yields, and tax metrics from a single dropdown slicer.
