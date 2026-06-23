# Example: "build me a stock dashboard"

A real session (translated from Chinese). The user wanted to build a personal
A-share market dashboard from a screenshot. Watch senior-mode refuse to build on
a fuzzy goal, catch its *own* mistake, kill a dead-data trap, and talk the user
out of over-building — all before writing a line of code.

---

**User:** I saw a feed someone shared today. I want to build a personal A-share
info source, like this screenshot.

**Agent:**

> 🎓 senior-mode: the goal's still fuzzy — pinning it down before I build anything.

First, a reality I have to call out so we don't build in the wrong direction:

Most of what's in that screenshot — intraday hot-takes, broker notes, WeChat-group
chatter — is **hand-curated**. It comes from paid research and private groups.
There's no public API that produces it.

What *can* be automated is the other half: company filings, sector moves, price
changes, individual-stock moves — aggregated from public sources into a daily
close summary.

Before I design anything, pin these down: *(asks: final form? content focus?
free vs paid data?)*

→ **Goal before work** + **Root cause** — it challenges the premise instead of
cheerfully building the impossible half.

---

**User:** Quotes + sector moves, free sources only, form TBD.

**Agent:**

> 🎓 senior-mode: last round I labeled AkShare as "paid" — that was wrong. AkShare
> is completely free. For "free-only + quotes/sectors", it's the standard answer.

**Three traps you must know first, or the build is wasted:**

1. **Northbound-flow data is gone.** Real-time disclosure was halted in Aug 2024 —
   only quarterly holdings remain. Plenty of tutorials still teach scraping it;
   that code is all dead now. Don't put it in the requirements.
2. **Anti-scraping is shaky.** Fine for your own daily use, not a public service —
   you'll get blocked.
3. **Trading-day / intraday.** Check for trading days; intraday real-time isn't
   available from free sources — close-of-day summary only.

→ **Don't just agree** — it corrects its *own* earlier error — plus **Root cause**,
surfacing the dead-data constraint nobody mentions.

---

**Agent (the plan):**

Don't build a dashboard first — frontend + deploy + scraping upkeep is expensive
and tends to die half-built. Instead:

- **Phase 1:** a local Python script — pull the data, generate a markdown summary,
  open it locally. Prove the data pulls and looks right.
- **Phase 2:** schedule it for 15:30 + push to chat/email.
- **Phase 3:** a dashboard — only if you actually need it.

Confirm two things and I'll start: Python installed? All five modules, or the
three core ones first?

→ **Pressure-test the plan** — it kills the over-built dashboard — plus **Cut the
slop**: phased, concrete, confirms before running.

---

*Five disciplines, one session: it pinned the goal, corrected itself, found the
root constraint, and handed over a plan you can actually run — instead of "You're
absolutely right!" and a dashboard built on dead data.*
