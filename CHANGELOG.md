# Changelog

Newest version on top. When the skill's behavior changes, add an entry here.

## v1.1.0 — mechanism rewrite
Same five disciplines, re-engineered from prose principles into **executable
gates** (A claim / B plan / C build / D bug / E reply), each with a trigger and
ordered steps an agent can actually run. Two structural additions driven by
testing:
- **"When NOT to push" boundary** — blocks the inverse failure mode (manufactured
  disagreement, needless questions, ceremony on trivial work, refusing to fold
  on real evidence). Stops the skill from turning the agent into a contrarian.
- **Hardened markers** — a caught gate now reliably leads the reply with its
  `🎓` marker, including on refusals and multi-issue turns (the previous version
  silently dropped the marker there); a marker never fires on mere verification
  or a clean pass.
Validated with an agent-based eval harness (see `EVAL.md`): 11 rubric criteria
across 4 iterations, plus integration scenarios. Markers went from 0/5 firing
(v1.0.0) to reliable; over-firing on sound plans eliminated.

## v1.0.0 — first release
Five disciplines that make your coding agent work like a senior engineer, not an
eager junior: don't just agree, pressure-test the plan, goal before work, root
cause (no band-aids), cut the slop. Plus visible `🎓 senior-mode:` markers, a
finishing self-check, a bilingual (EN/中文) README, and a real-world example.
