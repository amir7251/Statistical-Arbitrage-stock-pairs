#Project statement:
An Excel pairs-trading backtest on two ETF pairs—SPY–IVV (same index trackers) and SPY–EEM (U.S. vs Emerging Markets)—using a 60-day Z-score of the spread to trade mean reversion.
Rules: enter when |Z|\ge2; exit when |Z|\le0.5; stop when |Z|\ge3.
You hold one position at a time (−1/0/+1). P&L is prior position × change in spread; equity = 100 + CumPnL. You also compute drawdowns, Sharpe/Sortino (proxy), time in market, and turnover.

#Interpreting the results:
.Total CumPnL: SPY–IVV +13.18, SPY–EEM +10.28 → roughly +13% vs +10% on the base-100 equity curve.
•	Max drawdown: IVV −0.57% vs EEM −1.39% → shallower risk on IVV.
•	Sharpe (proxy): IVV 2.24, EEM 2.71 → EEM delivered more return per unit of total volatility in this sample.
•	Sortino (proxy): IVV 3.34, EEM 1.36 → IVV had much cleaner downside (fewer/lighter losses).
•	Time in position: IVV 12.4%, EEM 16.4% → strategy is selective; EEM fired slightly more.
•	Trades: both 1 completed trade → treat risk metrics as indicative, not definitive.
•	Turnover (per bar): IVV 0.064, EEM 0.032 → low churn.
