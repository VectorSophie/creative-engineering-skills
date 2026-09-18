---
name: write-for-reviewers
description: Structure a conference or journal paper so a skeptical reviewer can quickly understand the problem, contribution, evidence, and limits. Use when drafting or restructuring a manuscript whose story is unclear, sections feel disconnected, the Introduction or Related Work is weak, or technically correct material is hard to review. Not for sentence-level grammar polishing when the argument and section roles are already settled.
license: MIT
---

# Write for Reviewers

A paper is not a lab notebook arranged into sections. It is an argument a busy skeptical reader must reconstruct correctly on the first pass. Make that reconstruction cheap.

## 1. Decide the Paper Before Writing the Paper

**Know the contribution in one defensible sentence before optimizing prose.**

- State the problem, the technical or empirical delta, and the evidence that makes the delta matter.
- Separate the core contribution from supporting engineering, implementation detail, and future work.
- If three different one-sentence summaries describe three different papers, the story is not settled yet.

## 2. Make the Introduction a Contract

**Page one tells the reviewer what the rest must prove.**

- Establish why the problem matters, why existing approaches leave a real gap, what you do differently, and what evidence supports the contribution.
- Contribution bullets should be claims the body actually fulfills, not a shopping list of everything implemented.
- Do not spend half the Introduction teaching background that belongs later.

Failure signal: after the Introduction, a reviewer still cannot predict what result would make the paper successful.

## 3. Give Every Paragraph One Job

**A paragraph should make one move in the argument.**

- Put the paragraph's role near the beginning: motivate, contrast, define, explain, justify, report, or limit.
- Preserve explicit sentence-to-sentence relations rather than relying on topical proximity.
- If a paragraph needs two topic sentences, it probably needs to become two paragraphs.

## 4. Make Related Work Explain the Delta

**Related Work is comparison, not bibliography narration.**

- Group prior work by the dimensions that matter to your contribution.
- State both what earlier work accomplishes and the precise limitation or difference relevant here.
- Avoid novelty by omission; the strongest nearby work should be the easiest comparison to find.

## 5. Make Evaluation Answer Reviewer Questions

**Experiments exist to resolve doubts raised by the claims.**

- Design sections and figures around questions a reviewer will ask: does it work, compared with what, why, where, at what cost, and under what limitations?
- Put decisive evidence close to the claim it resolves.
- Treat limitations as part of the argument's boundary, not an apology appended after acceptance has already been demanded.

## The final test

A reviewer can skim the title, abstract, introduction, figures, and conclusion and reconstruct the same contribution, evidence, and scope you intended.
