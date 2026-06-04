# reframe

A Claude Code skill that turns one problem into **3-5 sharper alternative framings** — fast. It is a brainstorming aid, not a solver: when you're stuck or suspect you're solving the wrong problem, it restates the problem through named lenses (inversion, zoom out/in, stakeholder swap, constraint flip, root problem, analogy) and recommends one framing to pursue.

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

Example output:

```
**Problem:** 40% of users abandon onboarding at the signup step.

1. **Inversion** — How would we design signup to guarantee drop-off? (then invert each cause)
2. **Root problem** — Is the issue signup itself, or that users reach signup unconvinced?
3. **Stakeholder swap** — What does the user feel at the signup screen that we don't see?
4. **Constraint flip** — What if signup weren't required before first value?

**Recommended framing:** Root problem — fix *why* they hesitate, not the form fields. The drop-off is likely a symptom of low perceived value at that point.
```

### Another example — a real, everyday problem

> reframe this: our CI pipeline takes 35 minutes, so people stop waiting and merge without watching it

```
**Problem:** A 35-minute CI run is too slow to wait for, so developers merge without confirming it passed.

1. **Inversion** — How would we design CI so nobody ever trusts it? (slow, flaky, unclear failures — then fix each)
2. **Root problem** — Is the real issue the 35 minutes, or that a red build doesn't block the merge?
3. **Zoom in** — Which single stage eats most of those 35 minutes?
4. **Stakeholder swap** — From a reviewer's view, what would make waiting feel worth it?
5. **Constraint flip** — What if CI had to finish in 5 minutes — what would we cut, cache, or parallelize?

**Recommended framing:** Root problem — make a failing build actually block the merge. Speed matters, but unenforced CI is the thing causing bad merges, not the duration.
```

## Triggers

The skill activates on phrases like "reframe this", "reframe the problem", "other framings", "I'm stuck on X", "look at this differently", or "am I solving the right problem".

## License

MIT — see [LICENSE](LICENSE).
