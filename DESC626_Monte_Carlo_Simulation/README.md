# DESC 626 – Monte Carlo Simulation

**Course:** DESC 626 – Simulation Modeling  
**Project:** Financial Analysis with Monte Carlo Technique  
**Tools Used:** Excel, Analytic Solver
**Dataset:** NVIDIA historical stock prices (252 trading days)  

---

## 📊 Project Overview

This project applied Monte Carlo simulation to evaluate whether investing in NVIDIA stock over the next year would be a sound financial decision. Given the volatile nature of the stock market, we aimed to simulate thousands of possible price trajectories using the Geometric Brownian Motion model to assess the stock’s risk and potential return. The simulation generated both daily and annual outcomes, helping visualize the probability distribution of future prices.

---

## 🧾 Report Breakdown

### 1. 📥 Application Domain & Objective

- **Application Area:** Financial Analysis  
- **Problem Statement:** Should we invest in NVIDIA this upcoming year?
- **Objective:** Forecast stock performance using Monte Carlo simulation to inform investors and analysts about the risk/return trade-off.

---

### 2. 📉 Input Variables & Distribution

We modeled stock prices using **Geometric Brownian Motion (GBM)**, which assumes:
- Stock prices follow a **log-normal distribution**
- They fluctuate randomly but trend predictably based on:
  - **Log return** (percent change of stock price over time)
  - **Drift (μ):** average of historical log returns
  - **Volatility (σ):** standard deviation of log returns
  - **Delta (Δt):** small time increment (1/252 for each trading day)
  - **Starting Price:** $85.91 (as of April 4, 2024)

We used 252 days of historical closing prices for NVIDIA to calculate these variables.

---

### 3. 🧪 Simulation Development & Execution

- Built two models: one manual in Excel, one using Analytic Solver
- Ran **1,000 trials** per day to simulate daily price fluctuations for 252 days
- Applied random sampling to generate price paths

📂 See:  
- `Monte Carlo Simulation - main.xlsm`  
- `Monte Carlo Simulation - single day distribution.xlsm`

---

### 4. 📊 Summary Statistics & Results

- **Day 1 Distribution Mean:** $94.31  
- **Value at Risk (95%):** $94.67  
- **Conditional VaR:** $94.29  
- **Simulated Trajectory:** Generally trended downward and stabilized near the starting value

📌 **Conclusion:** Based on the simulation, the stock does not meet the expected return threshold. The risk outweighs the reward → **Do not invest**.

---

### 5. ✨ Additional Features

1. **Conditional Formatting:**  
   - Green cells indicate price increases  
   - Red cells indicate price decreases  
2. **Profit/Loss Threshold Lines:**  
   - 10% Profit: $103.74  
   - 10% Loss: $84.88  
   - These lines are visualized on the price trajectory graph for easier interpretation.

---

### 6. 💡 How Monte Carlo Helped

- Allowed us to quantify risk by simulating a wide range of possible outcomes
- Helped visualize the effect of volatility and drift
- Provided confidence intervals to support data-driven investment decisions

---

### 7. ⚠️ Drawbacks & Limitations

- Relies heavily on **historical data** that may not reflect future trends
- **Cannot account for external shocks** (e.g., tariffs, economic policy changes)
- The GBM model does not fully replicate **real market dynamics**

---

## 📂 Project Files

| File Name                                       | Description                                           |
|------------------------------------------------|-------------------------------------------------------|
| `Monte Carlo Simulation - main.xlsm`           | Full-year simulation using Excel and VBA             |
| `Monte Carlo Simulation - single day distribution.xlsm` | Distribution analysis for a single day         |
| `MCS_Report.pdf`                               | Final report detailing all phases of the simulation  |
| `MCS_Presentation_Slides.pdf`                  | In-class presentation summarizing the project        |
| `README.md`                                    | This file – summary and project documentation        |

---

## 📌 Key Takeaways

- Monte Carlo simulation is powerful for assessing financial decisions under uncertainty.
- While it doesn’t guarantee accuracy, it provides a framework to model potential outcomes and guide strategy.
- For NVIDIA in this scenario, the projected outcomes do **not justify an investment** due to insufficient return versus risk.

