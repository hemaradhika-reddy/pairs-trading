# Pairs Trading Strategy – RELIANCE & ONGC

## Objective
Implement a market-neutral pairs trading strategy using cointegration and mean-reversion.

## Data
- Source: Yahoo Finance data  via `yfinance` API
- Stocks: RELIANCE & ONGC
- Period: 2018–2024
- Frequency: Daily Adjusted Close

## Methodology
1. Test for cointegration between RELIANCE & ONGC.
2. Compute spread and Z-score.
3. Generate trading signals:
   - Z > 1.5: Short RELIANCE, Long ONGC
   - Z < -1.5: Long RELIANCE, Short ONGC
   - Z ≈ 0: Exit positions
4. Backtest strategy and calculate cumulative returns.
5. Compute Sharpe ratio as performance metric.

## Results
- Sharpe Ratio: 1.45 (example)
- Plots: `results/price_chart.png`, `results/zscore_chart.png`, `results/cumulative_returns.png`

## Limitations
- No transaction costs
- Static hedge ratio
- Assumes daily close execution
