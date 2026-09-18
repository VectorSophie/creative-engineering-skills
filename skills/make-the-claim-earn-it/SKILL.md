---
name: make-the-claim-earn-it
description: Keep research claims no stronger than the evidence, assumptions, and scope that support them. Use when drafting or revising Abstract, Introduction, Results, Discussion, Contributions, security claims, causal claims, benchmark comparisons, or any sentence that generalizes from experiments. Not for copy-editing prose whose scientific claims are already fixed and verified.
license: MIT
---

# Make the Claim Earn It

The paper does not get a stronger conclusion because the sentence sounds better with one. Every important claim has to earn its strength from evidence, assumptions, and scope.

## 1. Pair Every Major Claim With Evidence

**No headline claim without a path to what establishes it.**

- For each central claim, name the experiment, theorem, analysis, dataset, or observation that supports it.
- If the support is indirect, correlational, simulated, or partial, say so in the claim rather than hiding the limitation elsewhere.
- If you cannot identify evidence for a sentence, either add the missing work or weaken/remove the sentence.

Failure signal: the Abstract says something that no result section can point back to.

## 2. Match Scope to What Was Tested

**One benchmark is evidence about one benchmark until proven otherwise.**

- Do not generalize across datasets, populations, models, threat models, hardware, languages, or operating conditions you did not evaluate without an explicit argument.
- State boundary conditions that materially affect the result.
- Distinguish empirical coverage from hoped-for generality.

The test: could the claim survive if a reviewer appended “under what conditions?” to the end of the sentence?

## 3. Name the Assumptions That Carry the Result

**Hidden assumptions are borrowed certainty.**

- Surface assumptions about data quality, independence, attacker capability, trusted components, model access, resource budgets, measurement validity, or theoretical premises.
- In security work, state the adversary and its capabilities before claiming a defense is effective.
- In causal work, separate association from intervention unless the design actually supports causality.

## 4. Compete With Alternative Explanations

**A result is stronger when obvious rival explanations have been tested.**

- Ask what else could have produced the observed effect: leakage, confounding, extra compute, parameter count, tuning budget, implementation quality, sampling, or metric choice.
- Add the cheapest decisive control, ablation, or baseline that distinguishes your explanation from the strongest plausible alternative.
- When alternatives remain unresolved, report them as uncertainty rather than pretending the preferred mechanism won.

## 5. Let Negative Evidence Change the Story

**The narrative follows the results, not the other way around.**

- Preserve failed replications, contradictory settings, and meaningful null results when they bound the contribution.
- Do not cherry-pick seeds, metrics, subsets, or baselines solely because they make the claim cleaner.
- If evidence weakens during the project, revise the contribution statement before polishing the prose.

## The final test

For every major sentence, a skeptical reviewer can trace claim → evidence → assumptions → scope and find no jump where confidence appears from nowhere.
