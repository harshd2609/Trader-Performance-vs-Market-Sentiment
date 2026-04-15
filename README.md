# 📊 Hyperliquid Trader Behavior vs Market Sentiment Analysis

## 🔹 Objective

Analyze how market sentiment (Fear vs Greed) impacts trader behavior and performance on Hyperliquid.
The goal is to uncover actionable patterns that can inform smarter trading strategies.

---

## 🔹 Datasets Used

### 1. Bitcoin Market Sentiment

* Columns: `date`, `classification` (Fear / Greed)

### 2. Historical Trader Data (Hyperliquid)

* Key Columns:

  * `Account`
  * `Coin`
  * `Execution Price`
  * `Size USD`
  * `Side`
  * `Timestamp`
  * `Closed PnL`

---

## 🔹 Data Preparation

* Converted timestamps into datetime format
* Extracted **daily date** from trade timestamps
* Aligned both datasets on **daily level (date)**
* Merged sentiment data with trade data

### ✔ Key Step:

Each trade is mapped to its corresponding market sentiment (Fear/Greed)

---

## 🔹 Feature Engineering

The following key metrics were created:

* **Daily PnL per trader**
* **Win rate** (profitable trades ratio)
* **Average trade size (Size USD)** → used as a proxy for risk
* **Number of trades per day**
* **Long/Short ratio**
* **Drawdown proxy** (average negative PnL)

---

## 🔹 Analysis

### 1. Performance vs Sentiment

* Compared:

  * Average PnL
  * Win rate
  * Drawdown proxy

### 2. Behavioral Changes

Analyzed how traders behave differently in Fear vs Greed:

* Trade frequency
* Position size (risk-taking)
* Long vs Short bias

### 3. Trader Segmentation

Identified key trader groups:

* **High Risk vs Low Risk** (based on trade size)
* **Frequent vs Infrequent traders**
* **Consistent vs Inconsistent traders** (based on PnL volatility)

---

## 🔹 Key Insights

1. **Higher risk-taking during Greed**

   * Traders increase trade size during Greed periods
   * Indicates confidence and aggressive positioning

2. **Defensive behavior during Fear**

   * Increase in short positions
   * Lower trade sizes and reduced exposure

3. **Performance varies with sentiment**

   * Greed periods show higher average PnL but also higher volatility
   * Fear periods show more stable but lower returns

4. **High-risk traders are less consistent**

   * Larger position sizes lead to higher PnL swings
   * Lower overall win rate stability

5. **Frequent traders perform better**

   * Especially during volatile (Fear) conditions

---

## 🔹 Strategy Recommendations

### ✅ 1. Sentiment-Based Risk Adjustment

* Reduce position size during Fear periods
* Allow moderate risk during Greed periods

### ✅ 2. Trade Frequency Strategy

* Frequent traders can operate in both conditions
* Infrequent traders should avoid high-volatility (Fear) markets

### ✅ 3. Risk Control Rule

* Avoid large position sizes if win rate is low
* Maintain controlled exposure to reduce drawdowns

---

## 🔹 Tools & Technologies

* Python (Pandas, NumPy)
* Matplotlib / Seaborn
* Jupyter Notebook

---

## 🔹 How to Run

```bash
pip install -r requirements.txt
jupyter notebook
```

---

## 🔹 Conclusion

This analysis demonstrates that market sentiment significantly influences trader behavior and performance.
Understanding these patterns enables better risk management and more informed trading decisions.

---

## 🚀 Future Improvements

* Build predictive models for trader profitability
* Cluster traders into behavioral archetypes
* Develop an interactive dashboard (Streamlit)

---
