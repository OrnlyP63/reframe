# reframe

A Claude Code skill that turns one problem into **3-5 other problems worth solving** — fast. Instead of critiquing your problem or jumping to solutions, it surfaces sibling, adjacent, broader, narrower, and underlying problems around the same situation, so you can pick a better one to attack. Output is a bare list of problem statements — no critique, no solutions, no jargon.

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

Output is a bare list of other problems — no critique, no solutions, no jargon.

```
> reframe this: our CI pipeline takes 35 minutes, so people stop waiting and merge without watching it

- Developers merge code whose test results they never actually saw.
- A failing build does not stop a merge from happening.
- The feedback loop between writing code and knowing it broke something is too long.
- The test suite spends most of its time on a small subset of slow checks.
- Nobody owns or trusts the pipeline's pass/fail signal.
```

## Triggers

The skill activates on phrases like "reframe this", "reframe the problem", "other framings", "I'm stuck on X", "look at this differently", or "am I solving the right problem".

## License

MIT — see [LICENSE](LICENSE).
