# Demo tickets — answer key

Each `ticket-N.md` contains nothing but the raw message to paste into
the classifier's `TextArea` — no subject line, no category hint,
nothing that gives away what it's "supposed" to be. That's deliberate:
a viewer reading the raw text shouldn't be sure either. This file is
where the expected answer lives, so you can compare it against what
the model actually returns, live.

Suggested order: 1 → 4 first (each leans toward one category once you
read closely), then 5 and 6 as harder cases once the happy path is
proven.

## ticket-1.md — expected: billing

Two near-identical charges around the same time, no explanation of
what changed on the user's end. Reads as confusion, not an accusation
— nothing here uses the word "charged," "refund," or "duplicate."
A good reply acknowledges the possible duplicate charge and asks for
the transaction dates/amounts to confirm.

## ticket-2.md — expected: bug

An intermittent freeze on larger files, described entirely in
non-technical language — no error message, no export, no browser
mentioned. The signal is "stops responding" + "doesn't happen every
time" (points to a size/load-triggered defect), not user error. A good
reply asks for file size, browser, and steps to reproduce.

## ticket-3.md — expected: how-to

Ambiguous on purpose: could read as "something's broken" but is
actually someone unsure how to verify a setup step (team members after
an invite) rather than reporting that it failed. A good reply points
to wherever membership/permissions are confirmed, without assuming
anything is broken.

## ticket-4.md — expected: other

Deliberately contentless — no feature, no error, no ask. The
interesting outcome here isn't the label so much as whether the model
resists inventing a specific problem it wasn't told about.

## ticket-5.md — expected: ambiguous (billing and bug both present)

Two real threads in one message: a plan-change action that won't
complete, and a charge that landed anyway. Both are legitimate reads;
neither is "more correct." Good discussion point on stream for what a
single-label classifier does with a ticket that doesn't have one true
category — and what a two-label version would look like.

## ticket-6.md — expected: other (feature request, buried)

A rambling, low-signal message where the actual ask (some way to see
what a teammate is doing at the same time) is buried in stream-of-
consciousness and never stated as a request. Tests whether the model
extracts the underlying idea and gives a short, sane reply — or just
mirrors the rambling back at length.
