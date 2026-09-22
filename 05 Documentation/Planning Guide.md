
This document defines how story planning is organized and how the major planning tools relate to one another.

Planning is the source of truth for **what the author currently intends, explores, or has not yet resolved**. Planning is not the same as canon.

Established story-world facts belong in the Wiki. What actually happens on the page belongs in the Manuscript.

---

# Planning Architecture

Planning operates at several different levels:

```text
03 Planning/
    Character Arcs/
        Character Arcs.md
        [Character Arc notes...]

    Notes/
        Open Questions.md

    Plot/
        [Project Name] - Story Structure.md

        Plot Threads/
            [Plot Thread notes...]

        Plot Threads.base
```

Each part answers a different question:

| Planning Tool | Primary Question |
| --- | --- |
| Story Structure | What is the overall shape of the novel? |
| Plot Thread | How does this particular narrative thread develop? |
| Character Arc | How does this character change through the story? |
| Open Questions | What important decisions have not been made yet? |
| Scene Properties | What does this individual Scene need to accomplish? |

These tools should work together without becoming duplicate outlines of the same story.

---

# Planning vs. Canon

Planning describes **intention**.

The Wiki describes **established fictional truth**.

For example, an established fact about a character belongs in that Character's Wiki entry.

A possible future choice that character may make belongs in Planning.

When a planned development becomes established as story-world truth, harvest the resulting fact into the appropriate Wiki entry.

---

# Story Structure

The Story Structure note provides the highest-level view of the novel's narrative design.

It answers questions such as:

- What is the story fundamentally about?
- What dramatic question drives the novel?
- What thematic questions are being explored?
- What situation exists when the story begins?
- What major movements shape the novel?
- Which Plot Threads and Character Arcs are central?
- What major reveals need to occur?
- What structural dependencies exist?
- What important structural questions remain unresolved?

The Story Structure should remain **higher-level than a Scene outline**.

It is not meant to serve as a chronological list of every Scene or beat.

---

## Story Structure Properties

Recommended Properties:

```yaml
---
type: story_structure
status: developing
project:
---
```

### status

Recommended values:

- `developing`
- `outlined`
- `drafting`

**`developing`** — the overall structure is actively being explored or assembled. Major structural decisions may still be unresolved.

**`outlined`** — a coherent intended structure has been established and can guide manuscript development.

**`drafting`** — the structure is actively being expressed and tested through manuscript drafting. It represents the story's current intended shape but remains flexible as discoveries made during writing reshape the plan.

Story Structure status describes the structure's relationship to the writing process, not its degree of permanence.

A story may move backward or forward between these states as the manuscript develops.

---

## Story Structure Sections

A standard Story Structure note uses:

```markdown
# [Project Name] — Story Structure

## Story Premise

## Central Dramatic Question

## Thematic Questions

## Starting Situation

## Major Story Movements

### I —

### II —

### III —

### IV —

### V —

## Major Plot Threads

## Major Character Arcs

## Major Reveals

## Dependencies

## Unresolved Structural Questions

## Notes
```

The five Story Movements are intentionally neutral containers.

They may correspond to acts, phases, locations, escalating conflicts, or another structure appropriate to the novel.

The system does not require a particular story theory or beat sheet.

Leave movements blank until the story provides a reason to define them.

---

## Story Premise

A concise description of the novel's central situation, conflict, or narrative engine.

This is an author-facing statement rather than marketing copy.

## Central Dramatic Question

The primary narrative question whose resolution substantially defines the novel.

## Thematic Questions

Questions the story explores rather than propositions it must prove.

These may remain open-ended.

## Starting Situation

The important conditions already in place when the manuscript begins.

This is especially useful for distinguishing pre-story history from events that need to occur on the page.

## Major Story Movements

The largest structural changes or phases of the novel.

Use these to understand the overall shape of the story rather than to catalog Scenes.

## Major Plot Threads

Links to Plot Threads important enough to affect the novel's overall structure.

## Major Character Arcs

Links to Character Arcs important enough to affect the novel's overall structure.

## Major Reveals

Important information whose revelation changes the reader's or characters' understanding of the story.

## Dependencies

Structural prerequisites.

Use this section when one development must occur before another can work effectively.

## Unresolved Structural Questions

Important structural decisions that remain open.

These may also be represented in `Open Questions.md` when they need broader tracking.

## Notes

Additional structure-level observations that do not belong elsewhere.

---

# Plot Threads

A Plot Thread tracks the development of a specific narrative question, conflict, mystery, relationship, character concern, or world-level issue across the story.

A Plot Thread should be large enough to develop across multiple Scenes.

It is not necessary to create a Plot Thread for every event or Scene goal.

---

## Plot Thread Properties

Recommended Properties:

```yaml
---
type: plot_thread
thread_type:
status: planned
characters: []
locations: []
organizations: []
related_lore: []
introduced:
resolved:
---
```

---

## thread_type

Recommended values:

- `main`
- `subplot`
- `mystery`
- `relationship`
- `character`
- `world`

Use the type that best describes the thread's primary narrative function.

Additional type values can be added should the project demonstrate a need.

---

## Plot Thread status

Recommended values:

- `planned`
- `active`
- `resolved`
- `abandoned`

**`planned`** — intended but not yet meaningfully introduced.

**`active`** — established in the manuscript and still developing.

**`resolved`** — the thread has reached its intended narrative resolution.

**`abandoned`** — the thread was intentionally removed from the current story plan.

---

## characters

Characters whose actions, goals, relationships, or circumstances are central to the thread.
## locations

Locations materially important to the development of the thread.
## organizations

Organizations materially involved in the thread.
## related_lore

Lore whose rules or implications materially shape the thread.
## introduced

Link to the Scene that meaningfully establishes the Plot Thread for the reader.
## resolved

Link to the Scene that meaningfully resolves the Plot Thread.

Leave blank while unresolved.

---

# Plot Thread Body

A standard Plot Thread uses:

```markdown
# Overview

## Story Question

## Beginning

## Development

## Escalation

## Resolution

## Key Reveals

## Dependencies

## Notes
```

---

## Overview

A concise description of the thread and its role in the story.

## Story Question

The narrative question that keeps the thread active.

A useful Story Question creates uncertainty that can develop over multiple Scenes.

## Beginning

The state of the thread when it first becomes narratively relevant.

This may include conditions already established before the manuscript begins.

## Development

The actual planned developments, turns, discoveries, confrontations, or changes that move the thread forward.

This section answers:

> **What happens within this thread?**

## Escalation

The conceptual shape of increasing pressure, danger, cost, complexity, or consequence.

This section answers:

> **How does this thread become harder, more dangerous, or more consequential as it develops?**

Development and Escalation are related but not identical.

**Development** records planned events or changes.

**Escalation** describes the pattern by which those developments intensify.

## Resolution

The intended outcome of the thread.

Leave this open when the resolution has not yet been decided.

Planning notes should represent current intention without pretending undecided material has already been solved.

## Key Reveals

Important information disclosed through the thread.

## Dependencies

Developments that must occur elsewhere for this thread to function.

These may involve:

- other Plot Threads
- Character Arcs
- Wiki knowledge
- specific Scenes
- structural reveals

## Notes

Additional possibilities, alternatives, or observations relevant to the thread.

---

# Character Arcs

A Character Arc tracks planned transformation across the story.

A Character Wiki entry answers:

> **Who is this character?**

A Character Arc answers:

> **How does the story change this character?**

 A Character Arc is not meant to store the Character's general biography or established personality which are captured in the Character Wiki entry.

---

## Character Arc Properties

Recommended Properties:

```yaml
---
type: character_arc
status: planned
character: []
arc_type:
plot_threads: []
related_characters: []
starting_state:
ending_state:
---
```

---

## status

Recommended values:

- `planned`
- `active`
- `resolved`

**`planned`** — the intended transformation exists but has not meaningfully begun in the manuscript.

**`active`** — the transformation is underway.

**`resolved`** — the arc has reached its intended end state.

---

## character

Link to the Character whose transformation is being tracked.

The Character Arc owns this relationship.

There is no need to add reciprocal `character_arcs` Properties to Character Wiki entries solely to duplicate the same relationship. Backlinks provide the reverse connection.

---

## arc_type

Recommended values:

- `positive`
- `negative`
- `flat`
- `transformation`

These labels describe the broad shape of the intended arc.

They are organizational tools rather than requirements imposed on the story.

---

## plot_threads

Plot Threads that materially drive, reveal, or depend on the Character Arc.

## related_characters

Other Characters whose relationships materially influence the transformation.

## starting_state

A concise description of the Character's important state near the beginning of the arc.

## ending_state

A concise description of the intended end state.

These Properties provide at-a-glance reference.

The body of the Character Arc contains the nuance.

---

# Character Arc Body

A standard Character Arc uses:

```markdown
# Overview

## Central Question

## Starting State

## Ending State

## Central Contradiction

## Pressure

## Progression

### Stage 1 —

### Stage 2 —

### Stage 3 —

### Stage 4 —

### Stage 5 —

## Relationships

## Key Choices

## Costs

## Payoffs

## Notes
```

---

## Overview

Briefly describe the overall transformation and what drives it.

## Central Question

The fundamental question explored through the Character's transformation.

## Starting State

Who the Character is emotionally, socially, philosophically, or behaviorally near the beginning of the arc.

## Ending State

Who the Character is intended to become.

Consider what has been:

- gained
- lost
- preserved
- rejected
- transformed

## Central Contradiction

The tension at the heart of the Character's transformation.

A useful contradiction creates pressure between things the Character wants, values, believes, or needs.

## Pressure

The forces that repeatedly push the Character toward change.

Pressure may come from:

- circumstances
- relationships
- Plot Threads
- consequences
- internal conflict
- repeated choices

## Progression

The broad stages through which the transformation develops.

Progression describes **how the Character changes**, not every event involving the Character.

The five-stage structure is a planning aid rather than a required formula.

Rename, remove, or add stages when the story requires it.

## Relationships

How important relationships influence, resist, enable, or reveal the transformation.

## Key Choices

Decisions that meaningfully move the Character from the Starting State toward the Ending State.

Progression and Key Choices serve different purposes:

- **Progression** describes the trajectory of change.
- **Key Choices** identifies actions that cause or demonstrate that change.

## Costs

What the Character sacrifices, loses, risks, damages, or leaves behind as the arc develops.

A Cost does not need to be negative in every arc, but tracking consequences helps prevent transformation from feeling effortless.

## Payoffs

Places where accumulated transformation should become visible to the reader.

Payoffs may occur through:

- choices
- behavior
- relationships
- competence
- sacrifice
- confrontation
- changed reactions to familiar situations

## Notes

Additional possibilities, uncertainties, or observations relevant to the arc.

Use language such as `may`, `possible`, or `remains to develop` when something is intentionally undecided.

Planning should guide the manuscript without pretending every future choice is fixed.

---

# Character Arc Index

`Character Arcs.md` serves as a lightweight index of existing Character Arc notes.

A Base is not required until the number or complexity of Character Arcs demonstrates a useful reason for one.

The goal is to avoid creating infrastructure merely for symmetry with other planning systems.

---

# Open Questions

`Open Questions.md` stores unresolved authorial questions.

Use it when a decision matters enough to preserve but has not yet been answered.

Examples of appropriate questions include:

- How does a particular technology work?
- What motivates an organization to tolerate a situation?
- What historical event produced a current custom?
- When should a major revelation occur?
- What consequence should follow an important choice?

Open Questions may concern:

- worldbuilding
- character
- plot
- structure
- continuity
- research needs

The presence of a question does not make any possible answer canon.

---

# Resolving Open Questions

When an Open Question is answered, harvest the result into the appropriate source of truth.

For example:

```text
Worldbuilding decision
        ↓
Wiki

Narrative decision
        ↓
Plot Thread / Character Arc / Story Structure

Scene-specific decision
        ↓
Scene Properties or manuscript

Requires factual investigation
        ↓
Research
```

After the result has been harvested, remove or mark the original question as resolved according to the current organization of `Open Questions.md`.

`Open Questions.md` is not intended to become a second Wiki containing answers that exist nowhere else.

---

# How the Planning Layers Work Together

The planning tools describe the story at different scales.

A useful conceptual flow is:

```text
Story Structure
      ↓
Plot Threads ←→ Character Arcs
      ↓              ↓
           Scenes
```

This is not a strict hierarchy.

Plot Threads may reshape Story Structure.

Character Arcs may create new Plot Threads.

Drafted Scenes may reveal that an Arc or Thread needs to change.

The purpose of the structure is to give each kind of information a natural home, not to force story development into a one-way process.

---

# Story Structure vs. Plot Thread

Use **Story Structure** when the information concerns the shape of the novel as a whole.

Use a **Plot Thread** when the information concerns the development of one particular narrative question or conflict.

Story Structure may link to a Plot Thread without duplicating its detailed Development and Escalation sections.

---

# Plot Thread vs. Character Arc

Use a **Plot Thread** to track what happens to a narrative conflict, question, mystery, relationship, or situation.

Use a **Character Arc** to track how a Character changes.

The same events may contribute to both.

It is not necessary to duplicate the same explanation in both notes. Instead, record each consequence from the perspective appropriate to that note.

A Plot Thread asks:

> **How does this situation develop?**

A Character Arc asks:

> **How does this development change the Character?**

---

# Planning vs. Scene Planning

Planning notes track development across the story.

Scene Properties track the function of an individual Scene.

Scene Properties work best when they describe what the individual Scene contributes rather than reproducing an entire Plot Thread or Character Arc.

Link the relevant Plot Thread where useful, then describe the specific function of this Scene.

See [[Manuscript Workflow]] for Scene-level planning rules.

---

# Planning vs. Wiki

A planned event is not automatically an established Event.

A possible future relationship is not automatically an established Character relationship.

A proposed world rule is not automatically Lore.

The Wiki should reflect established fictional truth.

Planning may contain:

- possibilities
- intentions
- alternatives
- unresolved outcomes
- future developments

When those decisions become established, harvest the resulting facts into the Wiki.

See [[Wiki Property Guide]].

---

# Planning Workflow

A typical planning workflow is:

1. Capture unresolved ideas or questions.
2. Decide whether the issue belongs at the Story Structure, Plot Thread, Character Arc, or Scene level.
3. Develop the idea in the smallest appropriate planning context.
4. Link related planning notes where the relationship is meaningful.
5. Create or update Scenes when developments become concrete enough to write.
6. Allow drafting to challenge the plan.
7. Update Planning when manuscript developments change current intentions.
8. Harvest newly established fictional facts into the Wiki.
9. Resolve or remove obsolete Open Questions.

Planning does not need to be complete before drafting begins.

---

# Avoiding Overplanning

The planning system exists to make the story easier to understand and write.

It should not require every possible future development to be decided in advance.

Leave information blank when it is genuinely undecided.

Prefer:

- meaningful structure
- clear narrative questions
- useful dependencies
- important choices
- visible consequences

over exhaustive prediction of every beat.

A blank section can represent productive uncertainty.

---

# Guiding Principle

> **Plan at the level where the information naturally belongs.**

Use:

- **Story Structure** for the novel's overall shape.
- **Plot Threads** for developing narrative situations.
- **Character Arcs** for transformation.
- **Open Questions** for unresolved decisions.
- **Scene Properties** for individual Scene function.

Link these layers where useful, but do not make each one repeat the others.