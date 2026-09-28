# Latest scheduled monitor run

- Trigger: 2026-09-28 15:31:18 ET; broker quotes verified at 15:32:14-16 ET.
- Connection: SUCCESS. First scheduled run after migration verified through actual account, portfolio, equity positions/orders, quotes and historical-data calls.
- Session: normal NYSE trading day and regular hours (NYSE official calendar checked).
- Account value/cash/unleveraged buying power: USD 500; pending deposits USD 500. Equity positions and equity orders: empty.
- Decision: BLOCKED for authorized TSLA execution; read-only candidate screen has no qualifying breakout. No trades.
- TSLA fractional-stop implementation remains unresolved, whole shares exceed the USD 100 cap, and next confirmed earnings date was not found on Tesla IR. News scan was preliminary and is not complete pre-trade clearance.
- Replacement tickers remain analysis-only. All five symbols are below prior-20-session highs.
- 184 split-adjusted completed daily bars per symbol, through 2026-09-25. EMA uses SMA seed; ATR14 uses Wilder smoothing. No current incomplete bar included.

| Symbol | Live price | EMA20 | EMA50 | ATR14 | Prior 20-session high | Trend passes | Breakout |
|---|---:|---:|---:|---:|---:|---|---|
| TSLA | 357.6068 | 365.5968 | 362.7191 | 12.7322 | 386.8300 | Yes | No |
| NVTS | 11.8150 | 11.7983 | 12.7326 | 0.7720 | 12.6300 | No | No |
| SOUN | 5.9200 | 6.3322 | 6.6258 | 0.2808 | 7.3300 | No | No |
| APLD | 24.6250 | 26.8456 | 28.4938 | 1.7386 | 29.1500 | No | No |
| SMCI | 42.1398 | 39.2304 | 36.4643 | 2.3314 | 43.7599 | Yes | No |

Using only 2*ATR as stop distance gives an upper bound of 1 NVTS share or 4 SOUN shares under USD 2.50 risk. These are NOT proposed orders: the required swing-low stop can reduce these quantities, and entry signals, earnings/news checks and symbol authorization are missing. APLD and SMCI fail even the 1-share 2*ATR risk test.
