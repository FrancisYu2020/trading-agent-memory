# Risk Policy

## Hard limits

- Maximum loss at the initial stop: 0.50% of current account equity.
- Maximum TSLA market value: 10% of current account equity.
- Maximum total exposure opened under this autonomous mandate: 10% of account equity.
- Maximum concurrent TSLA swing positions: one.
- No margin borrowing, short sales, options, leveraged products, or averaging down.

Fractional shares are permitted; do not round down to whole shares.

Raw share size is the minimum of:

1. `(account equity * 0.005) / (entry price - initial stop)`
2. `(account equity * 0.10) / entry price`
3. `verified unleveraged buying power / entry price`

Round down only to broker-supported fractional precision (currently at most six decimal places). Recheck risk, exposure, cash availability, minimum order size, and supported order types after rounding. Entry price must exceed the initial stop. If required inputs cannot be verified, size is zero.

Fractional sizing does not waive limit-entry or protective-stop requirements. The current Robinhood interface supports fractional quantities only for regular-session market orders, not limit or stop orders. Until a compatible execution method or explicitly approved policy revision exists, fractional entries remain BLOCKED. Do not silently substitute market entries or periodic monitoring for broker-held stops.

## Execution controls

- Use limit orders for entries. Do not cross an abnormal spread.
- Define the stop and profit-management plan before submitting an entry.
- Do not enter during the first 30 minutes or final 15 minutes of the regular session.
- Do not open a position within two regular trading sessions before a scheduled TSLA earnings release.
- Do not chase an entry more than 0.25 daily ATR above the trigger.
- Do not submit an order with stale quotes, unknown buying power, a trading halt, a pending corporate action, or conflicting market data.
- Do not loosen a stop after entry.
- Avoid same-day exits. They are allowed only for a hard stop, a material thesis invalidation, or an account-risk breach.

When uncertainty remains after checking available evidence, use zero size and write `NO TRADE` in the journal only if the decision is materially different from the previous check.
