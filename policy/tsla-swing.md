# TSLA Swing Strategy

## Objective

Capture multi-day to multi-month upside trends in TSLA common stock while limiting downside with predefined stops and small position sizing.

## Data required

- A current timestamped TSLA quote and normal bid/ask spread.
- At least 60 completed daily bars adjusted for splits.
- Current account equity, cash, buying power, TSLA position, and open orders.
- The next confirmed TSLA earnings date and material company news.

No order is allowed if any required item is unavailable or contradictory.

## Setup

A new long setup exists only when all conditions pass:

1. The prior completed daily close is above both the 20-day and 50-day exponential moving averages.
2. The 20-day EMA is above the 50-day EMA.
3. TSLA trades above the highest completed daily high of the prior 20 sessions.
4. The proposed entry is no more than 0.25 times the 14-day ATR above that breakout level.
5. TSLA earnings are more than two regular trading sessions away.
6. There is no position or pending TSLA entry order.
7. The current time is outside the first 30 minutes and final 15 minutes of the regular session.

The 9:30 ET check is observation only. A breakout seen at the open must remain valid at the 11:30 ET check before entry.

## Entry and initial stop

- For fractional shares, a regular-session day market buy is permitted by explicit user authorization, subject to every other setup and risk rule. Verify the fresh ask is at or below the chase ceiling immediately before submission; market fills can differ. For whole shares, submit a day limit buy at or below the maximum permitted chase price. The fractional protective-stop implementation must be resolved before entry.
- Place the initial stop below the lower of:
  - entry minus two times the 14-day ATR; or
  - the most recent confirmed daily swing low.
- Size the order using `policy/risk-policy.md`.
- Cancel an unfilled day order at the close. Reassess it from fresh data on the next session.

## Position management

- Never add to a losing position.
- At a gain of two initial risk units (`2R`), raise the stop to at least the entry price.
- After `2R`, trail the stop below the higher of the 20-day EMA or the most recent confirmed daily swing low, while never lowering an existing stop.
- A completed daily close below the 20-day EMA is a thesis warning. Exit on the next liquid regular-session check if the price has not recovered above that EMA.
- Exit immediately when the hard stop is triggered or verified news makes the original thesis invalid.
- Review before earnings. Unless the open profit is at least `2R` and the protected stop is at or above entry, close before the earnings release.

## Monitoring decisions

Each scheduled check must produce one of: `NO CHANGE`, `WATCH`, `ENTER`, `MANAGE`, `EXIT`, or `BLOCKED`. Stay quiet for `NO CHANGE`; record and report the others when they are material.
