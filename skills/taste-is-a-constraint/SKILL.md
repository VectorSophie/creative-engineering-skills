---
name: taste-is-a-constraint
description: Make AI-built interfaces and creative output distinctive instead of samey. Use when building or restyling a UI, designing a landing page, starting a visual or creative project, or whenever the output risks looking like every other AI-generated app. Demands concrete references and constraints before code, bans the default aesthetic, and forces one distinctive choice per project. Not for backend logic, CLIs with no visual surface, or projects with an existing design system to follow.
license: MIT
---

# Taste Is a Constraint

Generic output is not a model limitation - it is what you get when nothing constrains the design. The same font, the same icon set, the same purple accent, the same left-rail sidebar: that is the absence of decisions, shipped. Treat taste as an input you must acquire before coding, not a quality that emerges after.

## 1. References Before Code

**Never design from adjectives.**

- "Modern and clean" produces the default. Get or propose concrete references instead: a specific site, poster, era, genre, or physical object the design should feel like.
- If the user gave no references, propose two or three sharply different directions in one sentence each and pick one - don't ask them to design by questionnaire.
- Extract rules from the reference: its palette, its type personality, its density, its motion. Write them down before the first component.

The test: could someone guess your reference from the finished screen? If nothing would tip them off, the reference never made it into the work.

## 2. Ban the Defaults

**The default stack of choices is the samey look. Refuse it as a set.**

- Inter (or the framework's default font), the stock icon set, indigo/purple accents, gray-on-white cards, rounded-everything, left sidebar + card grid: each is fine alone; together they are the AI-generated uniform.
- Before styling, name which of these defaults you are rejecting and what replaces them.
- Component libraries are allowed; their default theme is not.

Failure signal: the palette contains `#6366f1` and you can't say why.

## 3. One Distinctive Choice

**Every project gets at least one decision nobody would generate by accident.**

- An unexpected type pairing, a committed color, an asymmetric layout, a texture, a motion signature - one deliberate risk, executed consistently.
- Distinctive is not decorated. One strong choice carried everywhere beats five clever ones scattered around.
- Protect the choice when it causes friction; friction is usually the sign it's actually distinctive.

## 4. Design From the Content

**Lay out the real thing, not the template.**

- Use the project's actual words, data, and imagery from the first draft - lorem ipsum and placeholder cards make every layout converge on the same grid.
- Let the content's shape pick the structure: dense tables want density, one hero action wants emptiness, a narrative wants a reading column.
- Delete every element that exists because templates have one (hero subtitle, three-feature row, stat band) rather than because this product needs it.

## The final test

Put the screen next to three AI-built apps. If a stranger can't instantly tell which one is yours, the taste never became a constraint - go back to principle 1.
