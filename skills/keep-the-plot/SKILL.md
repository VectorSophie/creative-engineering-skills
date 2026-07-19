---
name: keep-the-plot
description: Stay on-objective through long working sessions. Use during extended multi-hour or multi-session work on one project, large refactors or migrations, resumed work after a break or context compaction, or whenever there's a risk of contradicting earlier decisions, drifting code style, or forgetting agreed constraints. Records decisions durably, re-anchors on the objective at checkpoints, and detects contradiction before it ships. Not for short single-task sessions where the whole plot fits in view.
license: MIT
---

# Keep the Plot

Long sessions fail in a predictable way: early decisions fade, style drifts, and the agent starts contradicting agreements it made an hour ago. Drift is a context problem, not a capability problem - so fight it with durable records and deliberate re-anchoring, not with hope.

## 1. Decisions Outlive the Conversation

**The moment a decision is made, write it somewhere that survives.**

- Constraints and choices agreed in conversation ("use Zod", "no new dependencies", "keep the old API working") go into a durable home the moment they're made: the project's notes file, a code comment at the point of impact, or the commit message - whichever the next reader will actually see.
- Record the why in one clause; a bare rule invites relitigating it later.
- One list, one place. Scattered decision fragments are how contradictions start.

The test: if this session ended right now, would the next one rediscover every constraint? Anything answered "no" isn't written down yet.

## 2. Re-anchor at Checkpoints

**Restate the objective before each new phase - from the record, not from memory.**

- At natural seams (a subtask done, a break, a compaction, a new file area), reread the objective and decision list before continuing.
- Say where you are in one line: what's done, what's next, what's deliberately deferred.
- After a context compaction or session resume, treat your memory of the plot as unreliable until checked against the record and the actual state of the code.

Failure signal: you're about to start a phase and can't state the original objective without scrolling.

## 3. Notice Contradiction Before It Ships

**When new work disagrees with old work, stop - one of them is wrong.**

- Before changing behavior, check whether the current shape was an agreed decision or an accident. Reversing an agreement silently is the classic drift failure.
- Style drift counts: if new code stops matching the conventions of the first hour, you've lost the thread, not improved it.
- When a decision genuinely needs reversing, reverse it explicitly: update the record, say what changed and why.

## 4. Prune What No Longer Matters

**A plot buried in dead context is as lost as one never written.**

- Failed experiments, superseded plans, and debug detours are done - summarize the lesson in a line and let the detail go.
- Keep the working set small: the objective, the live constraints, the current slice. Everything else is archive.
- Don't hoard context as a substitute for the record; principle 1 is what makes pruning safe.

## The final test

You've kept the plot when hour four's work could be reviewed by hour one's author and nothing would surprise them - or where it would, the record already explains why.
