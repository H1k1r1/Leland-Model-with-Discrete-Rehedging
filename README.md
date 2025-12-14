# Leland-Model-with-Discrete-Rehedging

One of the central challenges in managing an options portfolio is optimizing the cost of dynamic hedging. The classic Black-Scholes model assumes the possibility of continuous cost-free reinsurance, which is unrealistic. Leland's model (1985) eliminates this limitation by introducing transaction costs and discrete hedging.

In real conditions, liquidity providers (market makers) are forced to choose the optimal frequency of re-hedging their option positions: too frequent hedging increases total costs, too rare — accumulates gamma risk. This interaction can have far-reaching consequences for the stability of the market and the emergence of tail risks.

The purpose of this study is to build a multi—agent simulation (ABM) of a market with several types of traders who differ in the frequency of delta hedging, and statistically test hypotheses about the impact of hedging frequency on costs, volatility, and systemic risk.
