# creative-engineering-skills

Skills that make an agent behave less like a ticket executor and more like a trusted collaborator: engineering judgment on ambiguous work, distinctive output, long-session focus, demonstrated completion, safe unattended execution, independent verification, precise execution of explicit direction, and a research-paper layer for citation grounding, claim-evidence alignment, reviewer pressure-testing, venue compliance, visual evidence, rebuttals, and artifact traceability.

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
- **[`get-a-second-opinion`](skills/get-a-second-opinion/SKILL.md)** — routes consequential decisions through a check with no shared context or reasoning trail, instead of a self-reread. Know what needs one, keep it actually independent, hand over the output not the justification, treat disagreement as signal. For security-sensitive, irreversible, or high-stakes work.
- **[`honor-the-brief`](skills/honor-the-brief/SKILL.md)** — once direction is specific, implement exactly that instead of drifting back toward a grander version. Recognize when judgment's already been made, build the boundary not the backstory, flag deviations instead of folding them in silently. The mirror image of `make-it-yours`: for direction that's already closed, not open.


### Research and paper skills

These stay deliberately modular: invoke the one failure mode the paper actually has instead of loading a conference-writing encyclopedia into every research task.

- **[`cite-what-you-read`](skills/cite-what-you-read/SKILL.md)** — citations become evidence only after both the source and the exact cited claim are verified. Separates discovered, read, and claim-verified literature instead of letting search results masquerade as scholarship.
- **[`make-the-claim-earn-it`](skills/make-the-claim-earn-it/SKILL.md)** — keeps claim strength bounded by evidence, assumptions, scope, and plausible alternative explanations. The research equivalent of `prove-it`.
- **[`write-for-reviewers`](skills/write-for-reviewers/SKILL.md)** — structures a paper as an argument a skeptical reviewer can reconstruct quickly: contribution first, Introduction as contract, one job per paragraph, Related Work as technical delta.
- **[`red-team-the-paper`](skills/red-team-the-paper/SKILL.md)** — runs genuinely independent pre-submission review across distinct lenses, then collapses criticism into an evidence-backed concern-to-fix map instead of a stack of reviewer role-play.
- **[`answer-the-reviewers`](skills/answer-the-reviewers/SKILL.md)** — turns received reviews into direct answers, evidence, manuscript changes, and traceable commitments without wasting the rebuttal on defensive rhetoric.
- **[`honor-the-venue`](skills/honor-the-venue/SKILL.md)** — treats current venue rules as an authoritative brief. Verifies the correct year and submission phase instead of trusting conference folklore cached in model memory.
- **[`make-the-figure-argue`](skills/make-the-figure-argue/SKILL.md)** — makes figures and tables carry a specific piece of evidence honestly, legibly, and reproducibly. Every panel needs a reason to exist.
- **[`paper-meets-artifact`](skills/paper-meets-artifact/SKILL.md)** — keeps reported results traceable from manuscript claim back through figure/table, processed output, script, raw run, configuration, and code/environment.

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
/creative-engineering-skills:get-a-second-opinion
/creative-engineering-skills:honor-the-brief
/creative-engineering-skills:cite-what-you-read
/creative-engineering-skills:make-the-claim-earn-it
/creative-engineering-skills:write-for-reviewers
/creative-engineering-skills:red-team-the-paper
/creative-engineering-skills:answer-the-reviewers
/creative-engineering-skills:honor-the-venue
/creative-engineering-skills:make-the-figure-argue
/creative-engineering-skills:paper-meets-artifact
```

## When it triggers

Intended for substantial or ambiguous work:

- starting a greenfield project or turning a rough idea into working software
- planning and implementing a major feature or choosing architecture
- entering an unfamiliar technical domain or evaluating an uncertain stack
- broad requests that require research and judgment
- research manuscripts where citations, claims, reviewer expectations, figures, venue rules, rebuttals, or experiment provenance need disciplined handling

Not for tiny bug fixes, one-line edits, formatting, mechanical renames, version bumps, or tasks with a complete authoritative spec. The skill itself scales its ceremony down to zero for trivial work.

## How to tell it's working

- The agent states the real objective before writing code, and pushes back on over-complex suggested implementations.
- Research produces a decision with named assumptions, not a pile of links.
- The first deliverable is a running vertical slice, not a plan or empty scaffolding.
- Clarifying questions are rare, and each one names the decision that depends on the answer.
- Completion reports say what was verified and what remains uncertain.
- Paper claims stay traceable to evidence and scope; citations are verified at claim level; reviewer concerns produce concrete fixes rather than reassurance.
- Submission-specific work checks the current venue rules and keeps figures and reported results reproducible from their underlying artifacts.

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
│   ├── close-the-loop/
│   ├── get-a-second-opinion/
│   ├── honor-the-brief/
│   ├── cite-what-you-read/
│   ├── make-the-claim-earn-it/
│   ├── write-for-reviewers/
│   ├── red-team-the-paper/
│   ├── answer-the-reviewers/
│   ├── honor-the-venue/
│   ├── make-the-figure-argue/
│   └── paper-meets-artifact/
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

The engineering skills bias toward autonomy and momentum over check-ins. That's the point, but it means the agent will make more independent calls on medium-stakes choices — review its stated assumptions rather than expecting a question for each one. The research skills bias toward traceability and evidential discipline, which adds verification work around literature, claims, experiments, and venue constraints. On genuinely trivial work, both layers should add nothing.

## Attribution

The compact, behavioral format is inspired by small skill repositories such as `andrej-karpathy-skills`. The research-paper layer also draws conceptual inspiration from `TianyuCodings/Tianyu_writing_skills` and `hzwer/WritingAIPaper`, `a-attia/scicomp-research-skills`, `Orchestra-Research/AI-Research-SKILLs`, `euzun/security-paper-writing`, `AlexWortega/ai-peer-review-skill`, `vaskers5/paper-rebuttal-skill`, `Yuan1z0825/nature-skills`, and `LeonChaoX/qinyan-academic-skills`. The skills here are original compact behavioral distillations rather than vendored copies; no endorsement or affiliation is implied.

## License

MIT — see [LICENSE](LICENSE).
