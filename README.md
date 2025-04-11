# **VOLT v5 – BTCUSDT 5m Strategy**

**VOLT v5** is a fast-acting, trend-confirmation strategy optimized for **manual execution** or **alert-based monitoring** on the **5-minute BTCUSDT chart**. It combines PineScript alerts with Python-based backtesting and parameter sweep tooling to surface high-quality, risk-aware trade signals.

📱 **Live Signals**: [t.me/volt\_signals](https://t.me/volt_signals)  
🧠 Questions: [@cavpatrol](https://twitter.com/cavpatrol)

---

## **🧐 Strategy Overview**

This 5-minute strategy uses:

* **EMA crossover**: Fast EMA crosses above Slow EMA  
* **Price confirmation**: Price \> both EMAs  
* **Volatility logic**: SL/TP levels based on ATR

📏 Optimized via parameter sweep:

* `fast` EMA: 13  
* `slow` EMA: 55  
* `ATR Length`: 21  
* `SL`: 2.0 × ATR  
* `TP`: 3.5 × ATR

🧠 Plus institutional filters:

* ADX \> 20  
* Volume spike  
* RSI strength  
* Breakout \+ ATR median alignment

---

## **🔁 Sweep \+ Backtest**

The full system supports:

* ✅ `sweep_results.json`: Raw parameter output  
* ✅ `sweep_analysis.json`: PnL-ranked results  
* ✅ Python CLI backtest  
* ✅ Realism via slippage/commission

To replicate or evolve:

python run.py \--mode sweep  
python sweep/postprocess.py  
---

## **🖥️ Files Included**

| File | Purpose |
| ----- | ----- |
| `volt_alerts_generated.pine` | PineScript for real-time alerts |
| `volt_strategy_generated.pine` | PineScript for TradingView backtesting |
| `sweep_analysis.json` | Sorted list of backtested configurations |

---

## **📈 Sample Backtest (Python)**

| Metric | Value |
| :---- | :---- |
| PnL | $3,751.18 |
| Win Rate | 75.0% |
| Max Drawdown | $555.62 |
| Trades | 8 |
| Config Used | `13/55 EMAs`, ATR 21, SL 2.0, TP 3.5 |

🚪 Strategy favors **clean breakouts** and avoids chop via multi-filter logic.

---

## **🔔 Alerts via Telegram**

You can receive clean BTCUSDT alerts via:

📱 [t.me/volt\_signals](https://t.me/volt_signals)

Signals include:

* ✅ “Buy Signal”  
* 🛍“Stop Loss Hit”  
* 🎯 “Take Profit Hit”

Set these via TradingView with the `volt_alerts_generated.pine` script.

---

## **🧰 System Integration Ready**

This repo can plug into:

* 🧠 Your own Python signal dashboards  
* 📊 A TradingView setup (multi-chart, multi-timeframe)  
* ↺ Gmail → Telegram alert pipeline (included in VOLT core)

---

## **🤝 Want the Full VOLT System?**

This repo is a minimal public template.

To access:

* ✅ Full codebase  
* ✅ Sweep runner and strategy visualizer  
* ✅ Help integrating with your stack

🔗 DM [@cavpatrol](https://twitter.com/cavpatrol) on Twitter

---

**Not financial advice. Built for education and research. Use responsibly.**

