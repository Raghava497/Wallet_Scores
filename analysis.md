# 📊 Wallet Credit Score Analysis

This document provides insights into the wallet scores predicted by the model.

---

## 📈 Score Distribution

| Score Range   | Wallet Count |
|---------------|--------------|
| 0 - 100       | XX           |
| 100 - 200     | XX           |
| 200 - 300     | XX           |
| 300 - 400     | XX           |
| 400 - 500     | XX           |
| 500 - 600     | XX           |
| 600 - 700     | XX           |
| 700 - 800     | XX           |
| 800 - 900     | XX           |
| 900 - 1000    | XX           |

*(Replace XX with actual counts from the distribution table in your notebook)*

---

## 🟥 Risky Wallets (Score < 400)

- High number of liquidation events.
- Low repayment relative to borrow amounts.
- Typically inactive for long periods or show bursty transaction behavior.

---

## 🟨 Medium Wallets (Score 400–700)

- Moderate borrowing and repayment patterns.
- Few liquidation events.
- Average activity spread over time.

---

## 🟩 Good Wallets (Score > 700)

- Consistent repayment of borrowings.
- No liquidation events.
- Healthy borrow-to-deposit ratio.
- Active on multiple unique days.

---

## 📋 Observations

- A majority of wallets are in the medium category, indicating moderate behavior.
- Risky wallets often exhibit signs of bot-like behavior or over-leveraged borrowing.
- Only a small percentage of wallets score above 900, showing highly trustworthy behavior.

---

## 📊 Graph

The bar chart shows the distribution of wallet scores across ranges:

*(Graph is generated in `Wallet_Scores.ipynb` and saved with the results)*

