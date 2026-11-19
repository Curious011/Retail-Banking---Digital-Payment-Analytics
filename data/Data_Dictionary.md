# Data Dictionary

This repository contains two core relational tables supporting the **Finance Analytics Dashboard**: `customers` and `finance_transactions`.

---

## 1. `customers.csv`
Contains demographic and segmentation profiles for **5,000 registered customers** across India.

| Column Name | Data Type | Description | Sample Values |
| :--- | :--- | :--- | :--- |
| `customer_id` | Text (PK) | Unique identifier for each customer | `C00001`, `C00002` |
| `fisrt_name` | Text | Customer's first name | `Karan`, `Ishaan` |
| `second_name` | Text | Customer's last name | `Sharma`, `Patel` |
| `gender` | Text | Gender of customer | `Male`, `Female` |
| `date_of_birth` | Date | Date of birth (DD-MM-YYYY) | `14-08-1988` |
| `city` | Text | Resident city | `Mumbai`, `Bengaluru`, `Ahmedabad` |
| `state` | Text | Resident state | `Maharashtra`, `Karnataka`, `Gujarat` |
| `occupation` | Text | Employment / occupation type | `Salaried`, `Business Owner`, `Freelancer`, `Student`, `Retired`, `Self Employed` |
| `customer_segment`| Text | Tier segmentation | `Retail`, `Premium`, `SME`, `Corporate`, `Wealth` |
| `annual_income` | Decimal | Annual income in INR | `988416.79`, `457149.28` |
| `join_date` | Date | Account opening date | `15-04-2021` |

---

## 2. `finance_transactions.csv`
Contains **50,069 multi-channel financial transaction records** spanning January 2023 through April 2026.

| Column Name | Data Type | Description | Sample Values |
| :--- | :--- | :--- | :--- |
| `transaction_id` | Text (PK) | Unique transaction reference | `T00000001`, `T00000002` |
| `transaction_date` | Date | Date of transaction execution | `21-02-2025` |
| `account_id` | Text | Associated bank account number | `A001795`, `A004859` |
| `customer_id` | Text (FK) | Relational key mapping to `customers.csv` | `C00001`, `C00124` |
| `transaction_type` | Text | Nature of transaction | `Loan EMI`, `Deposit`, `Transfer`, `Withdrawal`, `Card Payment`, `Bill Payment`, `Investment`, `Interest Credit`, `Fee Charge`, `Refund` |
| `channel` | Text | Channel / rail used | `UPI`, `Mobile App`, `Net Banking`, `POS`, `ATM`, `Branch`, `Auto Debit` |
| `merchant_category`| Text | Spending / merchant category | `Rent`, `Salary`, `Groceries`, `Shopping`, `Bank Charges`, `Entertainment`, `Food Delivery`, `Healthcare`, `Education`, `Insurance` |
| `amount` | Decimal | Transaction value in INR | `15400.00`, `250.50` |
| `fee_amount` | Decimal | Service fee captured by institution | `24.50`, `0.00` |
| `tax_amount` | Decimal | Statutory tax deducted (GST/TDS) | `4.41`, `0.00` |
| `currency` | Text | Currency code | `INR` |
| `transaction_status`| Text | Settlement outcome | `Success`, `Failed`, `Pending` |
| `is_fraud` | Text | Confirmed fraud indicator | `No`, `Yes` |
| `risk_score` | Integer | Automated risk score (1–100) | `21`, `63`, `88` |
| `reference_no` | Text | Payment gateway reference identifier | `REF8835851139` |
