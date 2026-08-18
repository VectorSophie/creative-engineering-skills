---
name: close-the-loop
description: Design agent work that runs unsupervised across many iterations — scheduled loops, /loop runs, background or cron-triggered agents, self-triggering pipelines. Use when setting up a recurring or autonomous task, when work will run more than one tick without a human watching, or when asked to "keep going until X," "run this on a schedule," or "loop until done." Requires a real stop condition, a real check each tick, and state that lives outside the conversation. Not for a single interactive turn or a task that finishes in one pass.
license: MIT
---

# Close the Loop

An agent loop with no way to fail is a machine for producing confident garbage at scale, faster than a human ever could. An agent loop with no way to stop is a liability wearing an automation costume. Before letting an agent run itself, engineer the loop — not just the prompt inside it.

## 1. Write the Stop Condition First

**Before the first tick runs, know what makes it stop — and put that in the loop, not in your head.**

- Every loop needs an iteration ceiling, a cost or token budget, or a checkable done-condition — ideally more than one, since any single guard can fail to fire.
- A no-progress detector matters as much as a max count: the same error, the same empty diff, or the same failing check N ticks running means stop, not retry harder.
- "Keep going until it's done" is not a stop condition unless "done" is something the loop itself can test.

Failure signal: you can describe what the loop does but not what makes it quit.

## 2. Verify Every Tick, Not Just the Last One

**A loop that only checks its work at the end ran blind the whole way there.**

- Each iteration needs a real check before the next one starts: tests, lint, a diff review, the actual command run — something capable of saying no.
- An iteration that "looks right" and was never actually run is the ordinary unverified-completion mistake, just repeated automatically until it compounds across every future tick.
- If a tick can't verify itself cheaply, the unit of work is too large — shrink it until it can.

## 3. One Durable Unit Per Tick

**Small, complete, and checked in — never a half-step held together by conversation memory.**

- Each iteration finishes one discrete thing and leaves the result somewhere durable: a commit, a file, a row in a tracker — not just this turn's context.
- State that lives only in conversation history doesn't survive a compaction, a restart, or a crash between ticks. State on disk does.
- Resist growing one tick to cover "just a bit more" — a loop's power comes from many small verified steps, not fewer large unverified ones.

## 4. Anchor Intent Outside the Conversation

**Each tick re-reads the goal from a record — it never re-derives it from vibes.**

- Put the objective and standing constraints somewhere every tick reads first, before deciding what to do next.
- A loop that reinterprets its own purpose each iteration drifts exactly as fast as a long conversation does, just with nobody watching it happen.
- If the anchor and the actual work disagree, that's a contradiction to stop and reconcile — not a signal to trust whichever is more recent.

## 5. Escalate Instead of Spinning

**When the loop can't make progress, its job is to say so — not to keep trying at your expense.**

- Repeated failure, budget exhaustion, and a stop condition firing are all successful outcomes for the loop's design, even when the underlying task failed. Report what happened and why.
- Silent infinite retries are worse than a crash — a crash gets noticed.
- A loop that pauses to ask a real question at a genuine decision point is doing its job; one that guesses past it to keep the streak alive is not.

## Safety boundaries

Autonomy across ticks is still bounded by the authorization granted for the task. Running unattended never expands it. Never let a loop, on its own initiative:

- push, publish, deploy, purchase, or alter external infrastructure beyond what was explicitly authorized for the loop
- widen its own stop conditions or budget mid-run because it wants to keep going
- treat "no human objected" as consent — nobody was watching, that's the point of a loop
- retry past a repeated failure by weakening the check that's failing it

## The final test

The loop is engineered, not just prompted, when you can point to what makes it stop, what checks each step, and where its memory lives — without reading the transcript to find out.
