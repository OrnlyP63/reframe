---
name: reframe
description: Reframe a stated problem into 3-5 other problems, then let the user pick one to reframe deeper — recursive, drill-down problem reframing. Surfaces sibling/adjacent/underlying problems at every level; never critiques and never gives solutions. Use when the user says "reframe this", "reframe the problem", "other problems", "show me different problems", "I'm stuck on X", "look at this differently", or wants alternative problems around the same situation.
---

# Reframe

Take one problem and give back 3-5 *other problems* worth solving around the
same situation — fast. Surface sibling, adjacent, and underlying problems the
user could pursue instead. Brainstorming aid, not an interview.

**Canonical example — the slow elevator:** "The elevator is too slow" reframes
into other problems: *the wait feels boring*, *people have nothing to do while
waiting*, *the lobby is unpleasant*. Each is a different problem to attack.

## Output: recursive reframing

Reframe a problem into a numbered list of other problems, then let the user pick
one to **reframe deeper**. Always reframe — never solve.

A numbered list of other problems. Each item is **one short paragraph** (≈2-4
sentences), not a single line. End with one prompt line inviting the user to
pick one to reframe further.

```
1. **<short problem name>** — <a paragraph stating the problem: what it is, who
   has it, why it matters, and how it differs from the parent problem. No fix.>
2. **<short problem name>** — <another paragraph, a genuinely different problem.>
   ... (3-5 total)

_Reply with a number to reframe that one deeper._
```

When the user picks a number (or names one), treat **that problem as the new
parent** and reframe *it* into its own 3-5 sub/adjacent/underlying problems, same
format, same closing prompt. Repeat as deep as the user wants.

Hard rules:
- Output **other problems** — sibling, adjacent, broader, narrower, or underlying — relative to the current parent problem.
- **Do NOT critique** the problem (no "this is the wrong target", no "why X instead of Y").
- **Never give solutions, fixes, methods, or tools** — at any depth. This is a pure reframing tool.
- Each item is a problem stated as a paragraph — describe it in depth (context, who it affects, why it matters), but stay at the problem level.
- Numbered list, 3-5 items, no lens names, no other commentary. Always end with the pick-a-number prompt.

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
- Stay at the problem level at every depth — never critique, never solve. The skill only ever reframes.
