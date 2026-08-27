# Demo tickets

Fictional support tickets to paste into the classifier's `TextArea` live on
stream. Each file has the raw ticket text to copy-paste, plus a short host
note (not part of the pasted text) on what it's meant to demonstrate.

Suggested order: 1 → 4 are the clean cases, one per category. 5 and 6 are
edge cases — good for "let's see what it does with something messy" once
the happy path is proven.

| # | File | Expected category | Why it's here |
|---|------|--------------------|----------------|
| 1 | `ticket-1-billing.md` | billing | Clean, unambiguous billing complaint |
| 2 | `ticket-2-bug.md` | bug | Clean bug report with a stack trace |
| 3 | `ticket-3-howto.md` | how-to | Clean "how do I..." question |
| 4 | `ticket-4-other.md` | other | Vague/off-topic, no clear category |
| 5 | `ticket-5-mixed-billing-bug.md` | ambiguous (billing or bug) | Genuinely straddles two categories — good discussion point on how an LLM classifier handles ambiguity, not a "gotcha" |
| 6 | `ticket-6-rambling.md` | other (feature request) | Long, informally written, no clear ask — tests whether the model still returns a sane short reply instead of rambling back |
