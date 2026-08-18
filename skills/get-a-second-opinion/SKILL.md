---
name: get-a-second-opinion
description: Route consequential decisions and output through a check that doesn't share your context or reasoning trail, instead of trusting your own re-read. Use before shipping a security-sensitive change, an irreversible operation, a high-stakes architectural decision, or any output where your own review keeps saying "looks good" without having actually stress-tested it. Not for routine work where a self-check is proportionate, and not a substitute for prove-it's demonstrated evidence — this is about who checks, not whether you ran the thing.
license: MIT
---

# Get a Second Opinion

Re-reading your own reasoning confirms your own reasoning — that's not a check, it's an echo. The blind spots that produced a decision are still there when you review it with the same mind that made it. A second opinion only works if it's actually independent.

## 1. Know What Needs a Second Look

**Not everything does — match the rigor to the stakes.**

- Security-sensitive changes, irreversible operations, public APIs, and decisions expensive to unwind warrant an independent check. Routine work doesn't.
- If you'd hesitate to explain the choice to a skeptical colleague without hedging, it probably needs one.

Failure signal: you can't name what a second look would even be checking for.

## 2. Make the Check Actually Independent

**No shared context, no shared reasoning trail.**

- A fresh subagent, a different tool (linter, test suite, a security scanner), or a person with no stake in the original decision — not a second pass by the same reasoning that produced the first answer.
- If the "reviewer" saw every step that led here, it isn't a second opinion, it's a recap.

## 3. Hand Over the Output, Not the Justification

**Give the reviewer what was built, not why you think it's right.**

- Leading with your reasoning primes the check to agree with it. Show the artifact — the diff, the decision, the output — and let the check form its own view.
- If you must explain context, explain the problem, not your solution's defense.

## 4. Disagreement Is Signal, Not Noise

**When the independent check disagrees, that's information to resolve — not explain away.**

- Don't reflexively overrule a second opinion because you're confident in the first one; confidence isn't evidence.
- Don't silently accept it either. Understand the disagreement, then decide — and say what you decided and why.

## The final test

The opinion was second, not an echo, if it came from somewhere that could have said no.
