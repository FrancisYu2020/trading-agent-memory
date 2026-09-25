\# Trading Agent Instructions



Before performing trading analysis, read:



\- `policy/risk-policy.md`

\- `policy/allowed-strategies.md`

\- `models/option-valuation.md`

\- the current month's file under `journal/`



\## Source of truth



\- Robinhood is the source of truth for balances, positions, orders, fills and P\&L.

\- Git stores strategy rules, assumptions and decision logs.

\- Query Robinhood before evaluating portfolio exposure.

\- Do not rely on old journal entries for current positions.



\## Order safety



\- Default to read-only analysis.

\- Never submit, modify, roll or cancel an order without explicit approval in the current conversation.

\- Approval must include symbol, contract, side, quantity and limit price.

\- Show the complete order and resulting portfolio exposure before requesting approval.



\## Option analysis



\- Do not treat delta as real-world probability.

\- High IV alone does not establish positive expected value.

\- Separate market-implied values from independent forecasts.

\- Include bid/ask spread, collateral yield, fees and tail scenarios.

\- Calculate expected value before Kelly sizing.

\- Use at most one-quarter Kelly after portfolio risk limits.

\- If positive expected value is not supported, use zero position.



\## Security



Never store passwords, tokens, account numbers, tax documents or personal identifiers in this repository.

