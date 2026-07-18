# CLAUDE.md

Maintenance guidance for this repository. This file is for working **on** the repo, not a copy of the skill.

## What this repository is

A personal collection of compact behavioral skills for coding agents, packaged as a Claude Code plugin. Skills here teach judgment and ownership on substantial work, not mechanical procedures.

## Canonical source

`skills/make-it-yours/SKILL.md` is the single canonical version of the skill. README.md and EXAMPLES.md summarize and illustrate it — when the skill changes, update their summaries to match, but never let them grow into competing versions of the instructions.

## Style rules

- Keep skills compact: readable in a few minutes, 4–6 principles, one memorable rule per principle, imperative prose, concrete tests.
- No planning bureaucracy, giant checklists, or philosophical essays.
- No added infrastructure: no package manager, build system, CI, website, changelog, or agent-specific rule files for other tools.

## Validation

Before committing changes:

- `claude plugin validate .` — checks plugin.json, marketplace.json, and skill frontmatter.
- Parse every JSON file; check SKILL.md frontmatter is valid YAML with only supported fields (`name`, `description`, `license`).
- Confirm names stay consistent everywhere: repository, plugin, and marketplace are all `creative-engineering-skills`; the skill is `make-it-yours`.
- Confirm README installation commands match the metadata files.

## Adding a new skill

1. Create `skills/<skill-name>/SKILL.md` with `name`, a discovery-oriented `description` (state triggers *and* what it's not for), and `license: MIT`.
2. The `skills/` directory is auto-scanned; no plugin.json changes needed.
3. Add a short section to README.md and, if useful, examples to EXAMPLES.md.
4. Bump `version` in `.claude-plugin/plugin.json`.
