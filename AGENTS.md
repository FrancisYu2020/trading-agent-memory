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
