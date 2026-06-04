# reframe

A Claude Code skill that turns one problem into **3-5 sharper alternative framings** — fast. Reframing shifts your perspective to redefine an issue so you ask better questions and attack the root cause instead of the surface annoyance. It is a brainstorming aid, not a solver: when you're stuck or suspect you're solving the wrong problem, it restates the problem through named lenses (challenge assumptions, how→why, root problem, inversion, broaden context, stakeholder swap, constraint flip, emotional reframe, analogy) and recommends one framing to pursue.

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

Output is two sections — fresh perspectives, then the solutions they unlock. No framework jargon.

```
> reframe this: our CI pipeline takes 35 minutes, so people stop waiting and merge without watching it

**New perspectives**
- The real issue may not be the 35 minutes — it's that a red build doesn't block the merge.
- Trust, not speed: people skip CI because failures are slow, flaky, or unclear.
- One stage probably eats most of the 35 minutes; the rest is fine.
- "Fast enough to wait for" is a different goal than "fast" — what if it had to finish in 5?

**Solutions**
- Make a failing build actually block merge (branch protection / required check).
- Profile the pipeline; parallelize or cache the one slow stage.
- Surface a clear pass/fail status inline on the PR so waiting isn't needed.
- Split smoke tests (fast, blocking) from the full suite (slow, post-merge).
```

## Triggers

The skill activates on phrases like "reframe this", "reframe the problem", "other framings", "I'm stuck on X", "look at this differently", or "am I solving the right problem".

## License

MIT — see [LICENSE](LICENSE).
