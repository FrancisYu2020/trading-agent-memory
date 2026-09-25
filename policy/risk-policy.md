# Risk Policy

## Hard limits

- Maximum loss at the initial stop: 0.50% of current account equity.
- Maximum TSLA market value: the smaller of USD 100 or 20% of current account equity.
- Maximum total exposure opened under this autonomous mandate: the smaller of USD 100 or 20% of current account equity. Include open buy-order commitments when checking available exposure capacity.
- Maximum concurrent TSLA swing positions: one.
- No margin borrowing, short sales, options, leveraged products, or averaging down.

Fractional shares are permitted; do not round down to whole shares.

Raw share size is the minimum of:

1. `(account equity * 0.005) / (entry price - initial stop)`
2. `min(100 USD, account equity * 0.20) / entry price`
3. `verified unleveraged buying power / entry price`

Round down only to broker-supported fractional precision (currently at most six decimal places). Recheck risk, exposure, cash availability, minimum order size, and supported order types after rounding. Entry price must exceed the initial stop. If required inputs cannot be verified, size is zero.

The user explicitly permits fractional-share market entries during regular trading hours. The current connector does not support fractional stop orders; the protective-stop requirement remains unresolved. Fractional entries remain BLOCKED until a compatible stop mechanism or an explicitly approved stop-policy revision exists. Periodic monitoring is not an approved substitute for broker-held stops.

## Execution controls

- Fractional-share entries may use market orders during regular trading hours, as explicitly authorized by the user. Use limit orders for whole-share entries. Do not trade an abnormal spread. For market entries, size against a fresh ask, verify the chase ceiling immediately before submission, and reconcile actual fill price, quantity, exposure, and initial-stop risk afterward. A market order does not guarantee the quoted price or the chase ceiling; record any slippage or risk breach and apply the account-risk controls.
- Define the stop and profit-management plan before submitting an entry.
- Do not enter during the first 30 minutes or final 15 minutes of the regular session.
- Do not open a position within two regular trading sessions before a scheduled TSLA earnings release.
- Do not chase an entry more than 0.25 daily ATR above the trigger.
- Do not submit an order with stale quotes, unknown buying power, a trading halt, a pending corporate action, or conflicting market data.
- Do not loosen a stop after entry.
- Avoid same-day exits. They are allowed only for a hard stop, a material thesis invalidation, or an account-risk breach.

When uncertainty remains after checking available evidence, use zero size and write `NO TRADE` in the journal only if the decision is materially different from the previous check.
