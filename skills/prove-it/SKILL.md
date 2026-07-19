---
name: prove-it
description: Completion means demonstrated behavior, not asserted success. Use before claiming any nontrivial work is done, fixed, or passing - after implementing a feature, fixing a bug, finishing a refactor or migration, or when tests pass but the real flow hasn't been exercised. Requires running the actual thing, showing evidence, and reporting what remains unverified. Not for doc-only or comment-only changes with no runtime surface, or trivial edits whose correctness is visible on sight.
license: MIT
---

# Prove It

"Should work" is a guess wearing a suit. The trust gap with agent-written code isn't capability - it's that nobody watched the code actually run. Close it the only way that works: demonstrate behavior, show the evidence, and be precise about what you didn't check.

## 1. Run the Real Thing

**Exercise the path you built, the way it will actually be used.**

- Drive the feature end-to-end: the command, the endpoint, the screen - not just the module in isolation.
- Include the unhappy path you touched: the error case, the empty input, the second run.
- If the real path can't be run here (needs hardware, credentials, production), say so explicitly and run the closest safe approximation - never silently substitute a weaker check.

The test: did you observe the new behavior happen, or only infer it from code that looks right?

## 2. Tests Are Necessary, Not Sufficient

**A green suite proves the tests pass, not that the work is done.**

- Run the existing tests, and add one for the behavior you changed - the smallest check that fails if your logic breaks.
- Then ask what the suite can't see: wiring, config, startup order, the integration seam between tested units. That's where "all tests pass" and "it doesn't work" coexist.
- A test you wrote to pass isn't evidence until you've seen it fail for the right reason at least once - mentally or actually.

## 3. Evidence, Not Adjectives

**Show the output; don't characterize it.**

- Paste the actual result: the command and its output, the response body, the before/after behavior. "Verified ✓" with nothing attached is an assertion, not evidence.
- Make the demonstration cheap to re-run: the exact command beats a description of what you did.
- If verifying required setup, state it - evidence that can't be reproduced expires with the session.

Failure signal: your completion message contains "works correctly" but no output a reviewer could inspect.

## 4. Report the Uncovered Remainder

**Honesty about what wasn't verified is part of the proof.**

- Say plainly: tested X and Y; did not test Z, because W. An accurate partial claim beats an inflated complete one.
- Failed or flaky results get reported with their output, not smoothed over - a known failure is information, a hidden one is a trap.
- Never let the desire to be done upgrade "probably" to "definitely." The reader will act on your claim.

## The final test

The work is proven when a skeptical reviewer could confirm your claim from what you showed them - without trusting you, and without asking what "done" meant.
