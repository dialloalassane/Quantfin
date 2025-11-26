# 📈 Hidden Markov Model (HMM) – Bitcoin Trading Strategy

*A quantitative framework for regime-switching trading using BTC/USD data*

---

## 🔍 Overview

This project implements and compares a **Hidden Markov Model (HMM)**–based trading strategy using daily Bitcoin market data.
By learning **hidden market regimes** (e.g., bull, bear, sideways) directly from historical returns, the model adapts trading positions dynamically and is benchmarked against a traditional **Buy-and-Hold** approach.

The goal is to demonstrate how probabilistic state models can enhance systematic crypto trading.

---

## 📊 Features

### **Data Processing**

* Uses BTC/USD price data (Open, High, Low, Close, Volume).
* Computes daily returns (`pct_change`) and log-returns.

### **Hidden Markov Model**

* Gaussian HMM from *hmmlearn*.
* Compares multiple state counts (1–8).
* Selects the optimal model using **Bayesian Information Criterion (BIC)**.
* Learns latent regimes with distinct volatility patterns.

### **Trading Logic**

* Position switching based on predicted hidden states.
* Long-only and regime-filter variations.
* Full comparison against Buy-and-Hold.

### **Visualization**

* Regime-colored price chart.
* Single-plot portfolio curves.
* Returns distribution by regime.

---

## 📂 Dataset

The BTC/USD data used in this project can be downloaded here:

📎 **Kaggle Dataset**
👉 [https://www.kaggle.com/datasets/prasoonkottarathil/btcinusd](https://www.kaggle.com/datasets/prasoonkottarathil/btcinusd)

Download the CSV file and place it in the project directory.

---

## 🛠 Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/yourusername/hmm-trading-strategy.git
cd hmm-trading-strategy
pip install -r requirements.txt
```

### Requirements

* Python 3.8+
* pandas
* numpy
* matplotlib
* seaborn
* hmmlearn
* scikit-learn

---

## ▶️ Usage

Open the main Jupyter Notebook:

```bash
jupyter notebook HMM_bitcoin.ipynb
```

Inside the notebook, you can:

1. Load and preprocess BTC data
2. Compute returns
3. Train HMM models and choose optimal number of states
4. Simulate strategy performance
5. Visualize portfolio and regime charts

---

## 🧠 Key Concepts

### **Hidden Markov Models**

The HMM assumes that price returns depend on unobserved (“hidden”) market regimes.
Examples of hidden regimes:

* **Bull** → low volatility, positive drift
* **Bear** → high volatility, negative drift
* **Sideways** → moderate volatility

Each day, the model infers the most likely regime and adjusts trading rules accordingly.

### **Model Selection: BIC**

We evaluate different numbers of hidden states and choose the configuration with the lowest **Bayesian Information Criterion**:

[
\text{BIC} = -2\log(L) + k\log(n)
]

Lower BIC = more efficient model.

---

## 📘 Example Output

* Regime-segmented BTC/USD plot
* Hidden state probabilities
* Strategy vs Buy-and-Hold cumulative returns
* Volatility per regime

---

## 📄 Project Structure

```
├── data/
│   └── btcusd.csv
├── HMM_bitcoin.ipynb
├── requirements.txt
├── README.md
```

---

## 📌 Notes

* This project is for educational and research purposes only.
* Trading cryptocurrencies involves substantial risk.

---

## 🙌 Contributions

Pull requests and improvements are welcome!
If you add features—such as optimization, risk management, or hyperparameter tuning—feel free to open a PR.

