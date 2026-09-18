---
name: red-team-the-paper
description: Stress-test a research manuscript before submission using independent reviewer perspectives and a concrete concern-to-fix map. Use for pre-submission review, internal mock review, novelty and methodology checks, experimental completeness, reproducibility review, or when the authors have become too familiar with the draft to see its weaknesses. Not for responding to reviews already received; use answer-the-reviewers for that.
license: MIT
---

# Red-Team the Paper

Authors learn the paper's intended meaning; reviewers only see what survived onto the page. A useful pre-submission review tries to reject the artifact that actually exists, not approve the paper the authors meant to write.

## 1. Keep the Review Independent

**Do not prime the reviewer with the defense.**

- Give an independent reviewer the manuscript and necessary task context, not the full reasoning trail that produced it.
- Use a fresh subagent, separate model, domain expert, or other genuinely independent pass when the stakes justify it.
- The authoring agent may synthesize findings afterward, but it should not manufacture all the criticism from the same context and call that independent review.

This composes with `get-a-second-opinion`: the manuscript is the output being checked.

## 2. Use Distinct Review Lenses

**Different failure modes deserve different reviewers.**

At minimum cover the perspectives that matter to the paper:

- novelty and literature positioning,
- methodology and assumptions,
- experimental design and statistics,
- domain-specific correctness,
- reproducibility and artifact quality,
- hostile-but-fair overall review.

Do not force every lens into every paper. A theoretical proof and a systems measurement paper fail differently.

## 3. Require Evidence for Criticism

**Reviewer confidence is not evidence either.**

- Tie each concern to a concrete passage, missing experiment, unsupported claim, contradictory result, or verified piece of prior work.
- Distinguish “I disagree with the choice” from “the paper does not justify the choice.”
- Do not fabricate missing literature or pretend an unverified citation defeats the novelty claim.

## 4. Classify What the Concern Demands

**Not every criticism needs another experiment.**

Classify each issue as one of:

- contribution-threatening,
- needs new evidence,
- needs analysis or control,
- needs explanation or scope change,
- needs citation or positioning,
- presentation only.

This prevents cosmetic edits from disguising a scientific gap and prevents expensive experiments from being run to fix wording.

## 5. Collapse Reviews Into a Concern Map

**The deliverable is an actionable synthesis, not a pile of reviewer personas.**

For every material concern, record:

`Concern | Evidence | Severity | Reviewers | Proposed fix | Status`

Combine duplicates, preserve unique high-value objections, and keep genuine disagreement visible instead of averaging it away.

## 6. Re-Review the Fixes, Not the Old Paper

**A resolved comment is only resolved if the revision actually closes it.**

- Re-run the relevant lens after major changes.
- Verify that fixes did not introduce contradictions elsewhere in the manuscript.
- Stop when remaining concerns are explicit tradeoffs or limitations, not because the authors are tired of reading criticism.

## The final test

The paper has been reviewed by a process capable of surprising its authors, and every serious concern has a visible disposition rather than a reassuring adjective.
