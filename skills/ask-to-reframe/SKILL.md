---
name: ask-to-reframe
description: Interactively reframe a problem by asking one probing question at a time until it narrows to a sharp new perspective. The conversational sibling of `reframe` — instead of listing other problems instantly, it interviews the user, one question per turn, then delivers a before→after reframe. Use when the user says "ask to reframe", "interview me about this problem", "narrow this down", "help me find the real problem", "question me until we find the right framing", or wants to be asked questions rather than handed a list.
---

# Ask to Reframe

Narrow a vague problem to a sharp new perspective by **asking, not telling**.
One question per turn. Each answer steers the next question. When the problem
has visibly narrowed, stop and deliver the reframe. This is the interactive
sibling of the `reframe` skill (which lists other problems instantly).

## Loop

1. **Get the problem.** If the user supplied one on invocation, start questioning
   immediately. If not, ask: "What problem are we reframing?" — then begin.
2. **Ask one probing question** aimed at a hidden assumption, the real goal, who
   has the problem, what "solved" looks like, or what would have to be true for
   it to stop mattering. Include a **suggested answer** the user can accept or
   correct (e.g. _"My guess: it's really about X — right?"_). One question only.
3. **Wait** for the answer. Use it to sharpen your model of the problem and pick
   the next, more pointed question.
4. **Repeat** until the problem has clearly narrowed — usually 3-7 questions.
   Stop earlier if a reframe is already obvious; stop immediately if the user
   says stop. Never exceed ~7 questions without delivering a reframe.
5. **Deliver the reframe** (see format).

## Question rules

- Exactly one question per turn, plus its suggested answer. Never batch.
- Each question must build on the last answer — no generic checklist.
- Probe assumptions and goals, not implementation. Stay at the problem level.
- Short. No preamble, no commentary between questions.

## Final output (before → after)

When narrowed enough, end the loop with:

```
**Before:** <the problem as the user first stated it>
**After:** <the sharper, reframed problem — one or two sentences, the new
perspective the questioning uncovered>
```

- Land on **one** new perspective, not a menu.
- State it as a *problem/framing*, **not a solution** — no fixes, methods, or tools.
- Stop there. The user takes it from the sharpened problem.

## Rules

- Ask, don't lecture. The user holds the knowledge; you steer with questions.
- Suggested answers are guesses to react to, never the final reframe.
- If the user's answers contradict your guess, follow their answers.
- One perspective, before→after, no solutions.
