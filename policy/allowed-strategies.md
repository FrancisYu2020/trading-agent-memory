## Current monitoring scope - 2026-10-07

The user selected SPCX as the monitoring target. Read policy/spcx-monitor.md. SPCX replaces TSLA and the previous candidate basket in routine scans. This is a monitoring request, not an order instruction or expanded autonomous trading authorization. Do not open new TSLA positions from this monitor. Preserve all existing risk limits and any existing-position protections.
# Allowed Strategies

## Autonomous execution

- Long TSLA common stock under `policy/tsla-swing.md` and `policy/risk-policy.md`.

## Analysis only unless the user gives fresh explicit approval

- Cash-secured puts.
- Covered calls.
- Defined-risk option spreads.
- Long positions in any symbol other than TSLA.

## Prohibited under the autonomous mandate

- Naked or unsecured options.
- Margin borrowing or leveraged products.
- Short stock.
- Averaging down or martingale sizing.
- 0DTE or intended intraday trading.
- Any order that exceeds the risk or concentration limits.
