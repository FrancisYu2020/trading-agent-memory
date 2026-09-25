# Trading Agent Handoff

Read this file first when starting a new Codex or ChatGPT task for the trading workflow.

## Objective

Monitor TSLA on regular U.S. trading days at 09:30, 11:30, 13:30, and 15:30 America/New_York. Trade only multi-day to multi-month TSLA common-stock long swings under the repository policies. Avoid intended intraday trading.

## Required reading

1. `AGENTS.md`
2. `policy/risk-policy.md`
3. `policy/allowed-strategies.md`
4. `policy/tsla-swing.md`
5. The current month's file under `journal/`

## Current authorization and limits

- The user authorized autonomous TSLA common-stock long swing execution inside the repository rules.
- Initial stop risk must not exceed 0.50% of verified account equity.
- TSLA market value and total mandate exposure must not exceed the smaller of USD 100 or 20% of verified account equity.
- No options, margin borrowing, short sales, leveraged products, other symbols, or averaging down.
- The 09:30 check is observation only; the first permitted entry decision is 11:30.
- Broker or app approval requirements still apply to every action.

## Broker connection state

The original Codex task could not see any Robinhood account, market-data, position, or order tools even though the user reported that Robinhood was connected at the account level. No account data was read and no order was submitted.

At the start of a replacement task, explicitly select or mention the Robinhood app and perform a read-only connection test first:

> Read current account equity, cash, buying power, TSLA positions, and open orders. Do not place, modify, or cancel an order during this connection test.

Do not claim the connection works unless the task receives live, timestamped broker data. After verification, record the result in the current journal without storing account numbers, credentials, tokens, or other secrets.

## Automation

The original task created an active heartbeat named `TSLA 波段监控` with automation ID `tsla`. It is attached to the original task and runs at the four monitoring times above. It remains blocked when Robinhood tools are absent.

If monitoring moves to a replacement task that can access Robinhood, create or move the schedule there and then disable the original automation to prevent duplicate checks. Never run two order-capable monitors for the same mandate.

## Repository workflow

Repository: `git@github.com:FrancisYu2020/trading-agent-memory.git`

Before analysis, run `git pull --ff-only`. After a material journal or trade-record change, run `git diff --check`, commit with a clear message, and push to `origin`. Never force-push or store secrets.

## 2026-09-25 update - fractional shares

- User explicitly clarified that fractional shares are intended. Whole-share flooring is superseded by fractional sizing; the 0.50% risk limit remains unchanged; the concentration cap was subsequently raised as recorded below.
- User confirmed this is their private GitHub repository and explicitly authorized pushing the journal containing balances and trading data. Continue excluding account identifiers, credentials, tokens, and secrets.
- Read-only Robinhood connectivity is verified; see the September journal.
- The user subsequently authorized fractional-share market entries during regular trading hours; limit orders remain the default for whole shares. Execution remains BLOCKED only on the unresolved fractional protective-stop mechanism. A monitoring-only stop has not been approved. See the updated risk and strategy policies.

## 2026-09-25 update - USD 100 exposure cap

- User authorized raising the USD 50 position cap to USD 100 to improve whole-share feasibility. Apply the smaller of USD 100 or 20% of verified equity, without automatically increasing the dollar cap if equity grows.
- Initial-stop risk remains 0.50% of equity (USD 2.50 at the last verified USD 500 equity). Do not tighten a technical stop merely to fit this budget.
- The user wants a replacement in an active technology theme. Candidates have been discussed, but no specific replacement ticker has been selected; this cap change alone does not authorize orders in every discussed ticker.
