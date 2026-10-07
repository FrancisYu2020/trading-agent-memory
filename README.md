## Current monitoring scope - 2026-10-07

The user selected SPCX as the monitoring target. Read policy/spcx-monitor.md. SPCX replaces TSLA and the previous candidate basket in routine scans. This is a monitoring request, not an order instruction or expanded autonomous trading authorization. Do not open new TSLA positions from this monitor. Preserve all existing risk limits and any existing-position protections.
# Trading Agent Memory

This repository stores the rules, journal, trade records, and post-trade reviews for the trading workflow.

New tasks should read `HANDOFF.md` first, then follow the required reading order in `AGENTS.md`.

The current autonomous scope is deliberately narrow: long TSLA common stock, held for days to months, with no margin, options, shorting, or averaging down. `AGENTS.md` defines the required reading order, and the files under `policy/` contain the binding trading rules.

The scheduled monitor runs every 30 minutes from 09:30 through 15:30 America/New_York on regular weekdays. It stays quiet when nothing material changes and never treats an unavailable broker connection as a completed trade.
