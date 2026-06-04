# reframe

A Claude Code skill that turns one problem into **3-5 fresh perspectives** — fast. Reframing shifts your perspective to redefine an issue so you ask better questions and attack the root cause instead of the surface annoyance. It is a brainstorming aid, **not a solver**: it gives you new ways to see the problem and deliberately stops short of solutions, so you don't short-circuit your own thinking. Output is a bare list of perspectives — a mix of provocative questions and reframe statements.

### Why reframe?

- **Prevents solving the wrong problem** — fix the actual root cause, not the symptom.
- **Unlocks creativity** — challenges assumptions and blind spots, widening the solution space.
- **Alters emotional impact** — turns something you *suffer from* into an objective you can *tackle*.

> **The classic example — the slow elevator.** Problem: "the elevator is too slow, tenants complain." Expensive solutions: new lift, faster motor. The reframe: "the *wait* feels annoying." Cheap, better solutions: add mirrors or play music — the wait stops feeling agonizing. Same facts, different question, far better answer.

It works on work, productivity, and personal problems alike.

## Install

### A. As a plugin (recommended)

```
/plugin marketplace add OrnlyP63/reframe
/plugin install reframe@reframe
```

### B. As a plain skill (manual copy)

Copy the `skills/reframe/` folder into your Claude Code skills directory:

- macOS / Linux: `~/.claude/skills/reframe/`
- Windows: `%USERPROFILE%\.claude\skills\reframe\`

Restart your session. Confirm with `/skills` (or check the skill list).

## Usage

Just describe a problem and ask to reframe it:

> reframe this: our onboarding flow has a 40% drop-off at the signup step

Output is a bare list of perspectives — no headers, no solutions, no jargon.

```
> reframe this: our CI pipeline takes 35 minutes, so people stop waiting and merge without watching it

- What if the real issue isn't the 35 minutes, but that a red build doesn't block the merge?
- This is a trust problem, not a speed problem — people skip CI because failures are slow, flaky, or unclear.
- One stage probably eats most of the 35 minutes; the rest is fine.
- "Fast enough to wait for" is a different goal than "fast" — what would have to be true to finish in 5?
- Who is CI actually for here — the author, or the next person who has to trust this merge?
```

## Triggers

The skill activates on phrases like "reframe this", "reframe the problem", "other framings", "I'm stuck on X", "look at this differently", or "am I solving the right problem".

## License

MIT — see [LICENSE](LICENSE).
