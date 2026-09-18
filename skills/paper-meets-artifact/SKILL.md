---
name: paper-meets-artifact
description: Keep empirical paper claims traceable to the code, data, configurations, and runs that produced them. Use when a manuscript reports experiments, benchmarks, measurements, generated figures or tables, ablations, or released artifacts and the provenance must survive beyond the current session. Not for purely expository writing with no underlying computational or experimental artifact.
license: MIT
---

# Paper Meets Artifact

Six months after an experiment, “where did this number come from?” should be a lookup, not an archaeological expedition through shell history. The paper and the artifact are two views of the same result.

## 1. Give Every Important Result a Provenance Path

**A number in the paper should have somewhere to go.**

For each important table cell, figure, or quantitative claim, preserve a path like:

`claim → figure/table → processed output → analysis script → raw result → run config → code/environment`

The exact storage system does not matter. The ability to trace the result does.

## 2. Keep Raw Evidence Distinct From Presentation

**Derived output may change; the observation it came from should not.**

- Preserve raw run outputs or measurements separately from cleaned, aggregated, or plotted data.
- Make transformations explicit in code or documented commands.
- Do not hand-edit final CSVs, plots, or tables in ways that cannot be reconstructed.

Failure signal: the only copy of a reported result is inside the LaTeX table.

## 3. Record the Run, Not Just the Code

**A repository commit alone does not identify an experiment.**

Capture the parameters that materially determine the result: dataset/version, seed, model/checkpoint, hardware when relevant, dependency/environment information, command or config, and code revision.

Use whatever mechanism fits the project: config files, manifests, experiment logs, metadata JSON, a tracker, or a small plain-text record. Bureaucracy is optional; provenance is not.

## 4. Keep One Source of Truth for Reported Results

**The paper should consume results, not fork them.**

- Generate tables and figures from canonical result data whenever practical.
- Avoid separately maintained copies of the same metric in notebooks, spreadsheets, manuscript source, and slides.
- When a result is superseded, make the replacement explicit so stale values cannot survive in a forgotten figure.

## 5. Re-Run the Critical Path

**Reproducibility is demonstrated behavior, not repository aesthetics.**

- Before submission or artifact release, regenerate at least the central reported result from the recorded procedure.
- Verify that regenerated figures/tables agree with the manuscript.
- If compute, hardware, data access, or nondeterminism prevents a full rerun, test the closest feasible path and state the gap explicitly.

This composes with `prove-it`: the paper's evidence pipeline is another system that must actually run.

## 6. Preserve the Gaps

**Unknown provenance should stay visible until repaired.**

- Mark results whose source run, environment, or transformation cannot be reconstructed.
- Do not fabricate metadata after the fact to make the artifact look complete.
- A known provenance hole is fixable; an invented provenance trail is scientific fiction.

## The final test

For every result that matters to the contribution, another researcher or future-you can identify what ran, on what inputs, with which code and configuration, and how that output became the value shown in the paper.
