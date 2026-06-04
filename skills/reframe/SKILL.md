---
name: reframe
description: Reframe a stated problem into 3-5 alternative framings, fast. Use when the user says "reframe this", "reframe the problem", "other framings", "I'm stuck on X", "look at this differently", "am I solving the right problem", or otherwise wants fresh angles on a problem instead of a direct solution.
---

# Reframe

Turn one problem into 3-5 sharper alternative framings — fast. This is a
brainstorming aid, not a solver and not an interview. Do not interrogate the
user; produce framings from what they gave you.

## Quick start

1. Restate the user's problem in one neutral line: `**Problem:** ...`
2. Emit 3-5 reframes, each using a named lens (see below). Pick the lenses that
   actually fit this problem — do not force all of them.
3. Close with one `**Recommended framing**` and a one-line why.

If the problem is vague, make best-guess framings and state the assumption in
one line — never stall to ask clarifying questions.

## Lenses (pick the 3-5 most useful)

- **Inversion** — solve the opposite, or ask how to cause/worsen the problem on purpose.
- **Zoom out** — what broader goal is this problem really serving?
- **Zoom in** — the smallest concrete instance where it bites.
- **Stakeholder swap** — frame it from another party's point of view (user, boss, customer, future self).
- **Constraint flip** — remove the constraint everyone assumes, or add one that forces creativity.
- **Root problem** — "what if this isn't the real problem?" Name the problem behind it.
- **Analogy** — what is this like in a different domain, and how is that solved there?

## Output format

```
**Problem:** <one-line restatement>

1. **<Lens>** — <one-line reframed problem statement>
2. **<Lens>** — <one-line reframed problem statement>
3. **<Lens>** — <one-line reframed problem statement>
   ...

**Recommended framing:** <which one to pursue> — <why, one line>
```

## Rules

- Speed over ceremony. No multi-turn questioning.
- Each reframe is a *problem restatement*, not a solution.
- Different lenses must yield genuinely different framings — no rephrasing the
  same angle.
- Keep each framing to one line.
