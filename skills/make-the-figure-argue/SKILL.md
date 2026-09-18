---
name: make-the-figure-argue
description: Make research figures and tables carry a specific piece of evidence clearly, honestly, and reproducibly. Use when designing, revising, or reviewing plots, tables, multi-panel figures, architecture diagrams, captions, or visual evidence for a paper. Not for decorative illustrations whose purpose is purely aesthetic.
license: MIT
---

# Make the Figure Argue

A paper figure is compressed evidence. If the reader has to decode ornamental clutter before discovering what comparison matters, the figure is consuming attention instead of earning it.

## 1. Give Every Figure a Question

**Know what the reader should learn before choosing the chart.**

- Write the figure's intended takeaway as a question or comparison first.
- Choose the visual form that makes that comparison easiest to inspect.
- If a figure supports several unrelated claims, split it unless the interaction between them is itself the point.

Failure signal: the explanation starts with “this figure shows...” but cannot finish with why the figure exists.

## 2. Encode the Comparison Honestly

**Visual emphasis must match evidential importance.**

- Use scales, aggregation, normalization, ordering, and uncertainty representations that preserve the actual relationship.
- Avoid truncated axes, selective ranges, hidden failed runs, or smoothing choices that manufacture visual separation.
- When the conclusion depends on variance, distribution, or paired observations, show that structure rather than only a mean.

## 3. Make the Figure Survive Separation From the Prose

**A reviewer should understand the evidence from the figure and caption together.**

- Label axes, units, datasets, conditions, baselines, and abbreviations.
- Write captions that state what is being compared and the experimental context, not merely restate the title.
- Keep legends and typography readable at the paper's final rendered size.

## 4. Make Every Panel Earn Its Space

**More panels do not imply more evidence.**

- Remove panels that repeat the same conclusion without adding a new condition, mechanism, limitation, or diagnostic.
- Order panels to follow the argument, not the order experiments happened.
- Use tables when exact values matter more than visual trend recognition.

## 5. Make the Visual Reproducible

**The publication image should come from data, not hand-edited memory.**

- Generate data-driven figures and tables from versioned scripts and recorded inputs whenever practical.
- Keep manual annotations or post-processing explicit and reproducible.
- Prefer vector or venue-appropriate high-resolution output, and verify the exported artifact rather than trusting the interactive preview.

## 6. Design for More Than One Pair of Eyes

**Color is a channel, not the only channel.**

- Preserve distinguishability through labels, markers, line styles, position, or pattern where color alone would fail.
- Check grayscale and common color-vision deficiencies when the figure relies on categorical color distinctions.
- Do not encode meaning through tiny visual differences the final PDF will erase.

## The final test

A skeptical reader can identify the comparison, inspect the evidence, understand the conditions, and reproduce the visual without needing an oral explanation from the authors.
