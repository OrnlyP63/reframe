---
name: reframe
description: Reframe a stated problem into 3-5 other problems worth solving instead, then solve the one the user picks. Two steps — first surface sibling/adjacent/underlying problems (no critique, no solutions), then on a picked number give solutions for that one problem only. Use when the user says "reframe this", "reframe the problem", "other problems", "show me different problems", "I'm stuck on X", "look at this differently", or wants alternative problems around the same situation.
---

# Reframe

Take one problem and give back 3-5 *other problems* worth solving around the
same situation — fast. Surface sibling, adjacent, and underlying problems the
user could pursue instead. Brainstorming aid, not an interview.

**Canonical example — the slow elevator:** "The elevator is too slow" reframes
into other problems: *the wait feels boring*, *people have nothing to do while
waiting*, *the lobby is unpleasant*. Each is a different problem to attack.

## Output: two steps

**Step 1 — reframe into other problems.** A numbered list of other problems.
Each item is **one short paragraph** (≈2-4 sentences), not a single line. End
with one prompt line inviting the user to pick one for solutions.

```
1. **<short problem name>** — <a paragraph stating the problem: what it is, who
   has it, why it matters, and how it differs from the stated problem. No fix.>
2. **<short problem name>** — <another paragraph, a genuinely different problem.>
   ... (3-5 total)

_Reply with a number and I'll give solutions for that problem._
```

Step 1 hard rules:
- Output **other problems** — sibling, adjacent, broader, narrower, or underlying.
- **Do NOT critique the user's stated problem** (no "this is the wrong target", no "why X instead of Y").
- **Do NOT give solutions in step 1** — only the problems and the closing prompt.
- Each item is a problem stated as a paragraph — describe it in depth (context, who it affects, why it matters), but stay at the problem level.
- Numbered list, 3-5 items, no lens names, no other commentary.

**Step 2 — solve the chosen one.** When the user picks a number (or names one),
give concrete solutions for *that single problem only*: 3-5 actionable
approaches, one short paragraph or bullet each. Do not re-solve the others.

## How to find other problems (internal — never show this)

Move along these directions, keep the 3-5 that give genuinely different problems:

- Broader — the larger problem this one is a part of.
- Narrower — a smaller, sharper sub-problem inside it.
- Underlying — the root problem causing this one.
- Adjacent — a neighboring problem in the same situation.
- Goal-shifted — the problem if the real goal were the *why* behind the ask.
- Stakeholder — the problem as it exists for a different party (user, operator, customer, future self).
- Analogous — the same shape of problem in another domain.

Works across business, productivity, and personal problems.

## Rules

- Speed over ceremony. No multi-turn questioning.
- Problems must be genuinely different from each other and from the stated one — no rephrasing.
- One paragraph each (≈2-4 sentences) with real detail. If the input is vague, surface best-guess other problems anyway — never stall to ask.
- Step 1 stays at the problem level — never critique, never solve. Solutions come only in step 2, only for the picked problem.
