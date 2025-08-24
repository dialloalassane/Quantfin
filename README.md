# Hidden Markov Model (HMM) Trading Strategy

## 📌 Overview

This project implements and compares a **Hidden Markov Model (HMM)**-based dynamic trading strategy with a **Buy-and-Hold** benchmark.
The HMM identifies underlying market regimes using historical price data, enabling the strategy to adapt dynamically.

---

## 🔍 Features

* **Data preprocessing**: load, clean, and filter market data (2021–present).
* **Return calculations**:

  * Simple returns (`pct_change`)
  * Log returns (`np.log`)
* **HMM training**:

  * Gaussian HMM from `hmmlearn`
  * Different covariance structures (`full`, `diag`, `tied`, `spherical`)
  * Model selection via **Bayesian Information Criterion (BIC)** minimization
* **Strategy simulation**:

  * Position switching based on predicted hidden states
  * Comparison with Buy-and-Hold
* **Visualization**:

  * Portfolio value curves
  * Y-axis capped at 5000 for better comparability

---

## ⚙️ Installation

```bash
git clone https://github.com/yourusername/hmm-trading-strategy.git
cd hmm-trading-strategy
pip install -r requirements.txt
```

**Requirements**:

* Python 3.8+
* pandas
* numpy
* matplotlib
* hmmlearn
* scikit-learn

---

## 📊 Usage

Run the main Jupyter Notebook to:

1. Load historical data.
2. Compute returns.
3. Train the HMM and select the optimal number of states.
4. Simulate portfolio values.
5. Visualize results.

```bash
jupyter notebook HMM_Strategy.ipynb
```

---

## 🧠 Key Concepts

### Hidden Markov Models

The HMM assumes the market alternates between hidden regimes (e.g., bull, bear, sideways).
By fitting an HMM to returns data, we can estimate the probability of each regime at a given time.

### Model Selection: BIC

The **BIC** formula:

$$
\text{BIC} = -2 \cdot \log L + k \cdot \log N
$$

* $\log L$ = total log-likelihood
* $k$ = number of parameters
* $N$ = number of observations
  ✅ **Lower BIC is better**.

---

## 📈 Example Output

* **Dynamic Strategy vs Buy-and-Hold** plot:

  * X-axis: Date
  * Y-axis: Portfolio Value (max displayed: 5000)
  * Title includes `(Y-axis max = 5000)`

---

## 📌 Notes

* Always sort data by ascending date before computing returns.
* Log returns will appear inverted if data is sorted descending.
* The HMM requires multiple observations in the test set — cannot score with only 1 sample.



If you want, I can also **include an architecture diagram** in the README showing the pipeline from **Data → Returns → HMM Training → Strategy Simulation → Plotting**.
Do you want me to add that?
