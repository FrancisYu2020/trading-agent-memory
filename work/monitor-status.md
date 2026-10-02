# Latest scheduled monitor run

- Trigger 2026-10-02 13:32:10 ET; actual broker quotes/check 13:33:03-10 ET. Regular session; exchange calendar verified at today's opening check.
- Git pull --ff-only succeeded; AGENTS, HANDOFF, all required policies and October journal read. Starting tree clean.
- Connection SUCCESS: freshly discovered and successfully called accounts, portfolio, equity positions/orders, quotes and split-adjusted historical data.
- Account value/cash/buying power/unleveraged buying power USD 500; pending deposits USD 0. Equity positions/orders empty; no pagination cursor. No broker writes.
- Decision BLOCKED: fractional protective stops unresolved; whole TSLA share exceeds USD 100 ceiling; technical setup fails. Initial risk budget USD 2.50 unchanged.
- SMA-seeded EMA20/50 and Wilder ATR14 recomputed from 188 completed split-adjusted daily bars through October 1. Quotes active/traded; unfinished current bar excluded.

| Symbol | Quote | Prior close | EMA20 | EMA50 | ATR14 | Prior20 high | Trend | Breakout |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | --- | --- |
| TSLA | 372.355 | 354.11 | 362.0041 | 361.5426 | 11.8243 | 386.83 | Fail | No |
| NVTS | 12.3699 | 12.12 | 11.8026 | 12.5952 | 0.8183 | 12.9 | Fail | No |
| SOUN | 5.8399 | 6.05 | 6.2046 | 6.5242 | 0.2685 | 6.946 | Fail | No |
| APLD | 25.035 | 24.16 | 26.1013 | 27.9189 | 1.6421 | 29.15 | Fail | No |
| SMCI | 43.23 | 41.92 | 39.9644 | 37.2016 | 2.2595 | 43.7599 | Pass | No |

- Candidates remain analysis-only; none meets both trend and breakout. SMCI remains below 43.7599 and its two-ATR risk per whole share exceeds USD 2.50. No complete candidate earnings/news clearance.
- News search still centers on today's previously recorded Q3 delivery announcement. Reported October 21 after-close earnings date remains supported by syndicated company-release snippets, but issuer/Business Wire full-page retrieval failed again; retain pending full-source verification.
- Sources: https://ir.tesla.com/press-release/tesla-third-quarter-2026-production-deliveries-and-deployments ; https://www.businesswire.com/news/home/20261002169209/en/ .
- No new material account, order, signal or authorization change since prior check. No journal update or repeated news notification.
