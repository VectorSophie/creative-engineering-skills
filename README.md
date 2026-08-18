# creative-engineering-skills

Skills that make a coding agent behave less like a ticket executor and more like a trusted founding engineer: judgment on ambiguous work (`make-it-yours`), distinctive output (`taste-is-a-constraint`), long-session focus (`keep-the-plot`), demonstrated completion (`prove-it`), and safe unattended execution (`close-the-loop`).

## The problem

Given a substantial or ambiguous task, coding agents tend to: implement the suggested solution literally without asking what problem it solves, produce a plan and stop, offer five equivalent stacks instead of choosing one, ask permission for reversible decisions, scaffold broadly before proving anything works, and declare completion without verification.

## What `make-it-yours` changes

The first skill in this collection, **make-it-yours**, teaches one doctrine:

> Before implementing a substantial project or feature, understand it deeply enough to develop an informed technical point of view.

Then act on it: inspect what exists, research what's genuinely uncertain, commit to a defensible direction, build a working vertical slice, and verify the outcome. Ask the user only when unresolved ambiguity materially affects the result. Ownership never means expanding scope, ignoring safety boundaries, or acting without authorization.

## Core principles

| Principle | One line |
|-----------|----------|
| **Find the Real Problem** | Separate the objective from the suggested implementation; preserve the objective. |
| **Inspect Reality** | The repository knows things the request doesn't say — read it first. |
| **Research the Unknowns** | Primary sources, only for genuine uncertainty; stop when you can decide and defend. |
| **Form a Position** | Classify uncertainty — resolve it, ask about it, or just choose — then commit. |
| **Build the Smallest Proof** | A working slice through the riskiest part beats a finished plan. |
| **Verify the Outcome** | Done means demonstrated, not asserted. |

The full instructions live in [`skills/make-it-yours/SKILL.md`](skills/make-it-yours/SKILL.md) — that file is the canonical source. Everything else here summarizes it.

## The other skills

Each targets a specific, widely felt failure of agent-assisted work. Each `SKILL.md` is its own canonical source.

- **[`taste-is-a-constraint`](skills/taste-is-a-constraint/SKILL.md)** — kills the samey AI-app look (same font, purple accent, card grid). References before code, ban the default aesthetic, one distinctive choice per project, design from real content. For visual and creative work, not backends.
- **[`keep-the-plot`](skills/keep-the-plot/SKILL.md)** — fights long-session drift. Decisions written down the moment they're made, re-anchoring on the objective at checkpoints, catching contradictions before they ship, pruning dead context. For multi-hour or resumed work, not quick tasks.
- **[`prove-it`](skills/prove-it/SKILL.md)** — completion means demonstrated behavior. Run the real thing, treat green tests as necessary but not sufficient, show output instead of adjectives, report what wasn't verified. For any nontrivial "done" claim.
- **[`close-the-loop`](skills/close-the-loop/SKILL.md)** — engineers safety into autonomous, unattended runs. A real stop condition, per-tick verification, durable state outside the conversation, escalation instead of silent retrying. For scheduled loops, `/loop` runs, and cron- or background-triggered agents.

## Installation

Claude Code is the primary target.

**Local, works now** (from within Claude Code, using your local clone's path):

```
/plugin marketplace add C:\Workspace\creative-engineering-skills
/plugin install creative-engineering-skills@creative-engineering-skills
```

**From GitHub, after this repository is published:**

```
/plugin marketplace add VectorSophie/creative-engineering-skills
/plugin install creative-engineering-skills@creative-engineering-skills
```

## Usage

Once installed, Claude Code discovers the skill automatically when a task matches its description, or you can invoke it directly:

```
/creative-engineering-skills:make-it-yours
/creative-engineering-skills:taste-is-a-constraint
/creative-engineering-skills:keep-the-plot
/creative-engineering-skills:prove-it
/creative-engineering-skills:close-the-loop
```

## When it triggers

Intended for substantial or ambiguous work:

- starting a greenfield project or turning a rough idea into working software
- planning and implementing a major feature or choosing architecture
- entering an unfamiliar technical domain or evaluating an uncertain stack
- broad requests that require research and judgment

Not for tiny bug fixes, one-line edits, formatting, mechanical renames, version bumps, or tasks with a complete authoritative spec. The skill itself scales its ceremony down to zero for trivial work.

## How to tell it's working

- The agent states the real objective before writing code, and pushes back on over-complex suggested implementations.
- Research produces a decision with named assumptions, not a pile of links.
- The first deliverable is a running vertical slice, not a plan or empty scaffolding.
- Clarifying questions are rare, and each one names the decision that depends on the answer.
- Completion reports say what was verified and what remains uncertain.

## Repository structure

```
creative-engineering-skills/
├── .claude-plugin/
│   ├── plugin.json          # plugin metadata
│   └── marketplace.json     # marketplace catalog (this repo is its own marketplace)
├── skills/                  # one directory per skill; each SKILL.md is canonical
│   ├── make-it-yours/
│   ├── taste-is-a-constraint/
│   ├── keep-the-plot/
│   ├── prove-it/
│   └── close-the-loop/
├── CLAUDE.md                # maintenance guidance for this repo
├── EXAMPLES.md              # weak vs. ownership-oriented responses
├── README.md
├── LICENSE
└── .gitignore
```

`CLAUDE.md` here is repo-maintenance guidance, not a copy of the skill — there is deliberately only one full version of the instructions.

## Customization and future skills

Fork or clone, then edit `skills/make-it-yours/SKILL.md` — Claude Code follows the [Agent Skills](https://agentskills.io) format, so the file is portable to other Agent Skills-compatible tools by copying the directory. To adapt it for an `AGENTS.md`-based tool, paste the skill body (below the frontmatter) into that file. Add new skills as `skills/<name>/SKILL.md`; the `skills/` directory is discovered automatically. See `CLAUDE.md` for the conventions.

## Tradeoffs

The skill biases toward autonomy and momentum over check-ins. That's the point, but it means the agent will make more independent calls on medium-stakes choices — review its stated assumptions rather than expecting a question for each one. It adds a small amount of up-front inspection and research to substantial tasks; on genuinely trivial work it should add nothing.

## Attribution

The compact, behavioral format is inspired by small skill repositories such as `andrej-karpathy-skills`. All content here is original; no endorsement or affiliation is implied.

## License

MIT — see [LICENSE](LICENSE).
