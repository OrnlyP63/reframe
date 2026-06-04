# reframe

A Claude Code skill that turns one problem into **3-5 other problems worth solving** — fast. Instead of critiquing your problem or jumping to solutions, it surfaces sibling, adjacent, broader, narrower, and underlying problems around the same situation, so you can pick a better one to attack. Each is a short paragraph describing the problem in depth — no critique, no solutions, no jargon.

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

Output is a bare list of other problems — each a short paragraph, no critique, no solutions, no jargon.

```
> reframe this: our CI pipeline takes 35 minutes, so people stop waiting and merge without watching it

- **Unverified merges** — Code lands on the main branch while its test results are still running or unread. The team's effective quality gate is "looks fine to the author," not the suite, so regressions reach everyone before anyone notices.

- **Unenforced signal** — A red build does not actually block a merge. Whether CI passes or fails has become advisory, so the cost of ignoring it is zero and people rationally do.

- **Slow feedback loop** — The gap between writing a change and learning it broke something is long enough that developers context-switch away. By the time a failure surfaces, the author has moved on and the fix is far more expensive.

- **Concentrated cost** — Most of the 35 minutes is likely spent on a small subset of checks, while the rest finish quickly. The pipeline's pain is not evenly spread, and the team treats it as one monolithic wait.

- **Ownership gap** — No one clearly owns the pipeline's health or trusts its result. Flaky or unclear failures erode confidence until the green checkmark stops meaning anything.
```

## Triggers

The skill activates on phrases like "reframe this", "reframe the problem", "other framings", "I'm stuck on X", "look at this differently", or "am I solving the right problem".

## License

MIT — see [LICENSE](LICENSE).
