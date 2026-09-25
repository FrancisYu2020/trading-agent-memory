# Trading Agent Memory

This repository stores the rules, journal, trade records, and post-trade reviews for the trading workflow.

New tasks should read `HANDOFF.md` first, then follow the required reading order in `AGENTS.md`.

The current autonomous scope is deliberately narrow: long TSLA common stock, held for days to months, with no margin, options, shorting, or averaging down. `AGENTS.md` defines the required reading order, and the files under `policy/` contain the binding trading rules.

The scheduled monitor runs at 09:30, 11:30, 13:30, and 15:30 America/New_York on regular weekdays. It stays quiet when nothing material changes and never treats an unavailable broker connection as a completed trade.
