#  Aave V2 Wallet Credit Scoring

This project assigns a **credit score (0–1000)** to wallets interacting with the Aave V2 protocol based on their historical transaction behavior.

Higher scores indicate reliable and responsible usage, while lower scores reflect risky, bot-like, or exploitative behavior.

---

## 📊 Features Used for Scoring

| Feature                     | Description                                         |
|------------------------------|-----------------------------------------------------|
| total_transactions           | Total number of wallet actions                     |
| total_deposit_usd            | Total USD value deposited                          |
| total_borrow_usd             | Total USD value borrowed                           |
| repay_to_borrow_ratio        | Ratio of repaid to borrowed amounts                |
| borrow_to_deposit_ratio      | Ratio of borrowed to deposited amounts             |
| liquidation_count            | Number of liquidation events (penalty applied)     |
| active_days                  | Number of unique days the wallet was active        |
| avg_tx_gap_hours             | Average time between transactions (in hours)       |

---

##  Machine Learning Model

- **Algorithm:** Random Forest Regressor
- **Synthetic Labels:** Generated from engineered features
- **Score Scale:**  
  - 0 (worst) to 1000 (best)
- **Wallet Categories:**  
  - 🟥 **Risky**: score < 400  
  - 🟨 **Medium**: 400–700  
  - 🟩 **Good**: score > 700  

---

## ✅ Model Evaluation

| Metric                     | Value    |
|-----------------------------|----------|
| Mean Absolute Error (MAE)   | 3.41     |
| Root Mean Squared Error     | 9.62     |
| R² Score                    | 0.9975   |

---

## 🚀 How to Run

1. Place your transaction JSON file (e.g., `user-wallet-transactions.json`) in your working directory.
2. Open `Wallet_Scores.ipynb` in Google Colab or Jupyter Notebook.
3. Run all cells to:
   - Extract features
   - Train the model
   - Predict wallet scores
4. Output:
   - `wallet_scores.csv` containing wallet addresses, predicted scores, and categories.

---

## 📂 Outputs

- **wallet_scores.csv**: Wallets with predicted credit scores and classifications.
- **Score Distribution Graph:** Shows how wallet scores are spread across ranges.

---

##  Extensibility

This project can be extended by:
- Using real labeled data for supervised learning.
- Adding more on-chain behavior features and protocol usage patterns.

---


