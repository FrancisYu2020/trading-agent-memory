# Latest scheduled monitor run

- Trigger 2026-10-02 11:31:07 ET; actual broker check/quotes 11:32:11-19 ET. Regular session; calendar verified in today's opening check.
- Git pull --ff-only succeeded; required instructions, policies and October journal read. Starting tree clean.
- Connection SUCCESS: fresh discovery and successful calls to accounts, portfolio, equity positions/orders, quotes and split-adjusted daily history.
- Account value/cash/buying power/unleveraged buying power USD 500; pending deposits USD 0. Equity positions and orders empty, no pagination cursor. No broker writes.
- Decision BLOCKED: TSLA fractional stops unresolved, whole share exceeds USD 100 cap and technical entry fails. Initial risk budget USD 2.50 unchanged.
- 188 completed split-adjusted daily bars through October 1; SMA-seeded EMA20/50 and Wilder ATR14 recomputed; current unfinished bar excluded. Quotes active/traded.

| Symbol | Quote | Prior close | EMA20 | EMA50 | ATR14 | Prior20 high | Trend | Breakout |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | --- | --- |
| TSLA | 373.26 | 354.11 | 362.0041 | 361.5426 | 11.8243 | 386.83 | Fail | No |
| NVTS | 12.645 | 12.12 | 11.8026 | 12.5952 | 0.8183 | 12.9 | Fail | No |
| SOUN | 5.8777 | 6.05 | 6.2046 | 6.5242 | 0.2685 | 6.946 | Fail | No |
| APLD | 25.45 | 24.16 | 26.1013 | 27.9189 | 1.6421 | 29.15 | Fail | No |
| SMCI | 43.12 | 41.92 | 39.9644 | 37.2016 | 2.2595 | 43.7599 | Pass | No |

- Candidates remain analysis-only and no qualifying breakout. No complete candidate earnings/news clearance.
- Material news: issuer search result today reports over 486,000 Q3 deliveries and 13.7 GWh storage deployments. Syndicated company-release search results report October 21 after-close earnings. Direct issuer and syndicated page opens failed; retain date as reported pending full-source verification, not a cleared trading gate.
- Sources: https://ir.tesla.com/press-release/tesla-third-quarter-2026-production-deliveries-and-deployments and https://uk.finance.yahoo.com/news/tesla-third-quarter-2026-production-130600521.html .
- Journal updated for new delivery announcement and reported earnings date. Notify once; no trade.
