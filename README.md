# Replicating-Portfolio Backtester in C#/.NET

Console application that **backtests the replication of a derivative** on historical market data: at
each rebalancing date it computes the option's price and deltas, rebalances a self-financing portfolio,
and outputs the portfolio value against the option value over time.

> Co-authored with **Tariq Sereir** ([@tsereir](https://github.com/tsereir)) – course project, Grenoble INP – Ensimag (2023–2024).

## What it does

- Loads test parameters (JSON) and market data (CSV), then groups the market data into daily data feeds.
- **Rebalancing oracles**: regular period (every *n* dates) or weekly (fixed weekday).
- Self-financing portfolio: holds the deltas in the risky assets and the remainder in the risk-free account,
  capitalised between rebalancing dates.
- Writes the replicating-portfolio history to a JSON file.

## Usage

```bash
dotnet run --project BacktestConsole -- <test-params.json> <market-data.csv> <output.json>
```
