# Risk Policy

## Hard limits

- Maximum loss at the initial stop: 0.50% of current account equity.
- Maximum TSLA market value: 10% of current account equity.
- Maximum total exposure opened under this autonomous mandate: 10% of account equity.
- Maximum concurrent TSLA swing positions: one.
- No margin borrowing, short sales, options, leveraged products, or averaging down.

Position size is the smaller of:

1. `floor((account equity × 0.005) / (entry price - initial stop))`
2. `floor((account equity × 0.10) / entry price)`

If either input cannot be verified, position size is zero.

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
