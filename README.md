# Leland Model with Discrete Rehedging

## Description

One of the central challenges in managing an options portfolio is optimizing the cost of dynamic hedging. The classic Black-Scholes model assumes the possibility of continuous cost-free reinsurance, which is unrealistic. Leland's model (1985) eliminates this limitation by introducing transaction costs and discrete hedging.

In real conditions, liquidity providers (market makers) are forced to choose the optimal frequency of re-hedging their option positions: too frequent hedging increases total costs, too rare — accumulates gamma risk. This interaction can have far-reaching consequences for the stability of the market and the emergence of tail risks.

**The purpose of this study** is to build a multi—agent simulation (ABM) of a market with several types of traders who differ in the frequency of delta hedging, and statistically test hypotheses about the impact of hedging frequency on costs, volatility, and systemic risk.

---

## Visual analysis of the results

### Fig. 1. Price trajectories

A comparison of the "frequent" (blue) and "rare" (orange) hedging scenarios shows:
- **Frequent**: a more jagged, volatile microstructure (noise from frequent trades is visible)
- **Rare**: smoother with long-term drift (rare tipping events)

### Fig. 2. Distribution of transaction costs

**H1 histogram** clearly demonstrates:
- Blue (frequent): concentrated in the 2-4 cost range (narrow, stable distribution)
- Orange (infrequent): Wide tail, peak at 0-1% (rare but major events)

This confirms that with frequent hedging, costs ** are distributed more evenly**, which is important for risk planning.

### Fig. 3. Volatility vs costs

The graph "Realized Volatility vs Transaction Costs" shows **the absence of a clear pattern**: green bars (low cost) and red (high cost) overlap, which corresponds to p-value = 0.579 (Hypothesis 2).

### Fig. 4. Costs vs curtosis (H3)

The scatter plot shows **a negative trend** (r = -0.410):
- On the left (low cost): points at the top (high kurtosis)
- On the right (high costs): dots at the bottom (low kurtosis)
- One outlier (kurtosis ~700) corresponds to a simulation with extremely rare hedges

### Fig. 5. Extreme events

The box plot shows that the distribution of extreme events between "frequent" and "rare" hedging **is superimposed**, which corresponds to p = 0.236 for the t-test.

<img width="1389" height="1190" alt="image" src="https://github.com/user-attachments/assets/ee38e0a0-41ac-4021-9e47-054379b69a3c" />


---

