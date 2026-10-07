# SPCX monitoring policy

Effective 2026-10-07: user requested switching the monitoring target to SPCX.

- Instrument: Space Exploration Technologies Corp. (SpaceX), Class A common stock, Nasdaq SPCX. Issuer IPO release identifies June 12, 2026 as trading start. Verify instrument identity when fetching history; do not mix earlier same-ticker securities into bars.
- Source: https://ir.spacex.com/updates/releases-details/2026/Space-Exploration-Technologies-Corp--Announces-Pricing-of-Initial-Public-Offering/default.aspx
- Existing heartbeat tsla is renamed SPCX 波段监控, with the same thread and half-hour weekday schedule, 09:30-15:30 America/New_York. Skip holidays and after early closes. This configuration does not guarantee on-time runtime; record actual timestamps.
- This replaces routine TSLA/NVTS/SOUN/APLD/SMCI scanning. Read all stock positions/orders to detect actual exposure, while focusing market analysis on SPCX.
- Monitoring only: no SPCX order authority is inferred. No new TSLA entries from the switched monitor. Retain existing-position protective stops and inspect risk.
- Read risk-policy.md, allowed-strategies.md, tsla-swing.md (technical framework only), and current monthly journal.
- Apply the existing long-swing observation framework to SPCX: >=60 completed split-adjusted daily bars, close above EMA20/EMA50, EMA20 above EMA50, current price above prior20 completed highs, chase ceiling breakout + 0.25 ATR14, confirmed earnings more than two regular sessions away, and material news review. Do not call partial checks a fully cleared signal.
- Before 11:30 ET observe only; at/after 11:30 assess full conditions. Report relative volume only with a valid comparison period; intraday accumulated volume requires historical same-time comparison for an intraday relative-volume claim.
- Evaluate technical stops below the lower of entry minus 2 ATR14 and the confirmed swing low. Never compress stops to fit capital.
- Existing exposure ceiling min(USD 100, equity * 20%) and initial risk equity * 0.50% remain unchanged. Fractional protective stops remain unresolved; periodic observation cannot replace broker stops. Monitoring-target change does not resolve this block.
- Each check rediscover/call broker account, portfolio, stock positions/orders and timestamped SPCX quotes. Classify WATCH/NO CHANGE/BLOCKED accurately; notify meaningful changes only. Record work/monitor-status.md, and material changes in the journal. Commit/push without secrets.
