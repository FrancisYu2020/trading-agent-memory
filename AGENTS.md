## Current monitoring scope - 2026-10-07

The user selected SPCX as the monitoring target. Read policy/spcx-monitor.md. SPCX replaces TSLA and the previous candidate basket in routine scans. This is a monitoring request, not an order instruction or expanded autonomous trading authorization. Do not open new TSLA positions from this monitor. Preserve all existing risk limits and any existing-position protections.
# Trading Agent Instructions

Before analyzing a trade or placing an order, read:

- `policy/risk-policy.md`
- `policy/allowed-strategies.md`
- `policy/tsla-swing.md`
- `models/option-valuation.md` when options are involved
- the current month's journal

Treat these files as the source of truth. Never infer a looser rule from a past trade.

The current autonomous mandate is limited to long TSLA common-stock swing trades. Orders are allowed only when every rule in the policy files passes. Options, margin, short sales, leverage, and other symbols require fresh explicit approval.

If data is missing, stale, contradictory, or the broker connection cannot be verified, take no market action. A valid decision can be `NO TRADE`.

Record every material thesis change, signal, submitted order, fill, cancellation, stop update, exit, and completed-trade review. Never store credentials, account numbers, tax data, or other secrets in this repository.
