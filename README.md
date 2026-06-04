# reframe

A Claude Code skill that turns one problem into **3-5 other problems worth solving** — fast. Instead of critiquing your problem or jumping to solutions, it surfaces sibling, adjacent, broader, narrower, and underlying problems around the same situation, so you can pick a better one to attack. Each is a short paragraph describing the problem in depth — no critique, no solutions, no jargon.

### Why reframe?

- **Prevents solving the wrong problem** — fix the actual root cause, not the symptom.
- **Unlocks creativity** — challenges assumptions and blind spots, widening the solution space.
- **Alters emotional impact** — turns something you *suffer from* into an objective you can *tackle*.

> **The classic example — the slow elevator.** Problem: "the elevator is too slow, tenants complain." Expensive solutions: new lift, faster motor. The reframe: "the *wait* feels annoying." Cheap, better solutions: add mirrors or play music — the wait stops feeling agonizing. Same facts, different question, far better answer.

It works on work, productivity, and personal problems alike.

## Two skills

This repo ships two complementary reframing skills:

- **`reframe`** — instant. Give it a problem, get 3-5 other problems back as a list. No back-and-forth.
- **`ask-to-reframe`** — interactive. It asks one probing question at a time, narrowing your problem until a sharp new perspective emerges, then gives a before→after. Use it when you don't yet know what the real problem is.

Both install together (see below).

## Install

### A. As a plugin (recommended)

```
/plugin marketplace add OrnlyP63/reframe
/plugin install reframe@reframe
```

### B. As a plain skill (manual copy)

Copy the skill folders into your Claude Code skills directory:

- macOS / Linux: `~/.claude/skills/`
- Windows: `%USERPROFILE%\.claude\skills\`

Copy both `skills/reframe/` and `skills/ask-to-reframe/`. Restart your session. Confirm with `/skills` (or check the skill list).

## Usage

Just describe a problem and ask to reframe it. Output is a bare list of other problems — each a short paragraph, no critique, no solutions, no jargon.

```
> reframe this: our CI pipeline takes 35 minutes, so people stop waiting and merge without watching it

- **Unverified merges** — Code lands on the main branch while its test results are still running or unread. The team's effective quality gate is "looks fine to the author," not the suite, so regressions reach everyone before anyone notices.

- **Unenforced signal** — A red build does not actually block a merge. Whether CI passes or fails has become advisory, so the cost of ignoring it is zero and people rationally do.

- **Slow feedback loop** — The gap between writing a change and learning it broke something is long enough that developers context-switch away. By the time a failure surfaces, the author has moved on and the fix is far more expensive.

- **Concentrated cost** — Most of the 35 minutes is likely spent on a small subset of checks, while the rest finish quickly. The pipeline's pain is not evenly spread, and the team treats it as one monolithic wait.

- **Ownership gap** — No one clearly owns the pipeline's health or trusts its result. Flaky or unclear failures erode confidence until the green checkmark stops meaning anything.
```

It works on personal and productivity problems too, not just technical ones:

```
> reframe this: I keep procrastinating on writing my thesis

- **Unclear next action** — "Write my thesis" is not a task you can sit down and do; it's a mountain with no obvious first step. The real problem may be that there is no concrete, five-minute action defined, so every work session starts with the friction of deciding what to even open.

- **Avoidance of a feeling** — Procrastination is often a way to escape an emotion attached to the work — fear it won't be good enough, dread of a hard chapter, shame about being behind. The problem here isn't time management at all; it's that sitting down forces contact with something uncomfortable.

- **Misaligned reward timing** — The payoff for thesis work is months away while distractions pay off instantly. The problem is a structural mismatch between effort now and reward much later, which makes almost anything else feel more rewarding in the moment.

- **Ambiguous standard of "done"** — Without a clear bar for what "good enough" looks like for a section, the work feels infinite and unwinnable. The problem is that an undefined finish line makes starting feel pointless because it never feels finishable.

- **Environment and competing demands** — The hours, place, and surrounding obligations may simply not leave a protected space for deep work. The problem could be that thesis time is the first thing sacrificed whenever anything else appears, rather than a lack of will.
```

### Interactive: `ask-to-reframe`

When you don't yet know the real problem, let it interview you — one question at a time:

```
> /ask-to-reframe I want to grow my YouTube channel

Q: When you say "grow," my guess is you mean more subscribers — but is the
   thing you actually want reach, income, or something a subscriber count
   only stands in for?
> Honestly income. Subs are just what I thought I needed.

Q: So is the problem "not enough subscribers," or "not enough of my existing
   audience pays me"? My guess: you may already have enough viewers to earn
   from, just no way they can.
> ...yeah, I have ~20k views/month and zero ways to pay me.

Q: Then would adding 10k subscribers change anything if none of them could
   pay you either? My guess: no — the bottleneck is monetization, not size.
> No, it wouldn't.

**Before:** I want to grow my YouTube channel.
**After:** The real problem is that my existing 20k monthly viewers have no
way to pay me — it's a monetization problem, not an audience-size problem.
```

## Triggers

`reframe` activates on phrases like "reframe this", "other framings", "I'm stuck on X", "look at this differently", or "am I solving the right problem". `ask-to-reframe` activates on "ask to reframe", "interview me about this problem", "narrow this down", or "help me find the real problem".

## License

MIT — see [LICENSE](LICENSE).
