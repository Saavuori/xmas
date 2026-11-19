# 🎄 ELFRED – Santa's AI Head Elf

**Live app:** https://saavuori.github.io/xmas/ · **Slides:** https://saavuori.github.io/xmas/slides.html

ELFRED reads the elves' list (read-only), weighs the evidence and recommends Nice / Leaning Nice / Santa Review / Needs a Nudge, with highlighted receipts. Santa makes the final call.

## What it does
- **Reads stories**: one row per child with a free-text behaviour story (e.g. `Child name, Location, age, What they want for present, behavior during the year`). ELFRED splits each story into clauses, finds good deeds and slips, understands *always/once* and *never/stopped*, and estimates when in the year each happened (recent months count more).
- Also reads **observation logs** (one row per observation with date, elf and category).
- Handles odd CSV exports: whole lines wrapped in quotes, `;` or tab separators.
- **Chat**: "Is Aino nice?", "Who needs my review?", "How is Finland doing?", "Which wishes are approved?", "I'm exhausted".
- **Guardrail**: "Delete …" is refused. The list is never changed.
- **Santa's overrides** (stored beside the list in the browser, never in it):
  - ✍️ *Santa's notes*: "note for Lumi: baked cookies for the reindeer" → re-scored live
  - 🖋 *Santa's seal*: "put Iida on the nice list" → stamped final verdict
  - 🎅 *Christmas spirit dial*: Grumpy ↔ Jolly shifts every verdict

Load your own list with **📄 Load list CSV**. The file never leaves the browser.
`data/demo-list.csv` is in story format and `data/demo-observations.csv` is in observation-log format.
