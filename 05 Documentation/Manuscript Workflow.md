# Manuscript Workflow

This document defines how manuscript Scenes are created, organized, linked, drafted, and compiled.

The manuscript is the source of truth for **what actually happens on the page**.

Story-world facts belong in the Wiki. Intended narrative development belongs in Planning. The Scene body itself is reserved for manuscript prose.

---

# Manuscript Architecture

The manuscript is built from individual Scene notes managed by Longform.

A typical project uses:

```text
01 Manuscript/
    [Project Name]/
        Index.md
        001 - Scene Name.md
        002 - Scene Name.md
        ...
    Compiled/
        [Project Name] - Compiled.md
    Scenes.base
```

The Longform project folder contains the source Scene notes.

`Scenes.base` remains outside the Longform project folder so that Longform does not interpret it as manuscript content.

Compiled manuscripts are stored separately under:

`01 Manuscript/Compiled/`

---

# Authority and Order

## Scene Notes

Individual Scene notes are the authoritative source for manuscript prose.

Make manuscript revisions in the Scene notes rather than in compiled output.

## Longform

Longform is the authoritative source for manuscript Scene order.

Do not rely solely on:

- filenames
- folder order
- `scene_number`
- Base sorting

to determine manuscript order.

Those systems may assist navigation, but Longform controls compilation order.

## Compiled Manuscript

Compiled manuscripts are generated output.

Do not make manuscript revisions directly in:

`01 Manuscript/Compiled/`

Make changes in the appropriate source Scene and compile again.

---

# Scene Naming

Use a numeric prefix followed by a concise author-facing description.

Example:

`001 - Arrival at the Station

Scene filenames exist for author navigation and organization.

They are not intended to appear as reader-facing manuscript headings.

The numeric prefix provides a convenient visual reference but does not replace Longform as the authoritative source of manuscript order.

---

# Scene Properties

Every Scene uses:

`type: scene`

Recommended Scene properties:

- `chapter`
- `scene_number`
- `pov`
- `status`
- `characters`
- `locations`
- `organizations`
- `events`
- `lore`
- `items`
- `timeline`
- `plot_threads`
- `purpose`
- `conflict`
- `outcome`
- `continuity`

## chapter

The chapter or manuscript section to which the Scene currently belongs.

Examples:

- `Chapter 1`
- `Chapter 2`
- `Prologue`
- `Epilogue`

Chapter is metadata rather than a required physical folder structure.

This allows Scenes to remain directly inside the Longform project while still being grouped or filtered by chapter.

## scene_number

Numeric reference for the Scene within the manuscript.

Examples:

`1`

`2`

`3`

Use this for navigation, reference, and Base sorting.

Longform remains authoritative for actual manuscript order.

## pov

Link to the `[[Character]]` whose point of view governs the Scene.

Leave blank for Scenes without a defined POV.

## status

Describes the current writing state of the Scene.

Recommended values:

- `planned`
- `outlined`
- `draft`
- `revised`
- `final`

Use:

**`planned`** — the Scene exists conceptually but has not been substantially outlined.

**`outlined`** — the Scene's structure or major beats have been established.

**`draft`** — prose drafting is underway or a first draft exists.

**`revised`** — the Scene has undergone substantive revision.

**`final`** — the Scene is considered complete for the current manuscript version.

---

# Scene Entity Linking

Scene Properties connect the manuscript to the Wiki.

Record entities that are **meaningfully present or relevant to the Scene**, not everything merely mentioned.

The purpose of Scene metadata is to reveal useful relationships between the manuscript and the story world.

Ask:

> **Would I reasonably want this Scene to appear when reviewing this entity's backlinks or related Scenes?**

If yes, include the entity.

If not, leave it out.

Prefer fewer meaningful links over exhaustive tagging.

> **Metadata should reveal relationships, not reproduce every reference in the manuscript.**

## characters

List important `[[Character]]` entries meaningfully present in the Scene.

Include characters who participate or whose involvement is materially important.

Characters who are merely mentioned generally do not need to be included.

## locations

List `[[Location]]` entries where the Scene takes place or which are directly relevant to what occurs.

Locations that are merely mentioned in dialogue, memory, or exposition do not generally need to be included under properties.

## organizations

List `[[Organization]]` entries meaningfully involved in the Scene.

Include an organization when its members, actions, authority, goals, resources, or influence materially affect what happens.

## events

List significant `[[Event]]` entries directly depicted, caused, discovered, remembered, investigated, or substantially discussed.

A passing reference to a historical event does not necessarily require an Event link.

## lore

List `[[Lore]]` concepts materially relevant to the Scene.

Include Lore when its rules, implications, customs, systems, or information meaningfully affect what happens or what the reader learns.

Lore links are most useful when the concept is materially relevant rather than simply implicit in the Scene.

## items

List significant `[[Item]]` entries directly relevant to the Scene.

Include an Item when its presence, possession, use, discovery, loss, or significance matters.


---

# Planning Relationships

## plot_threads

List Plot Threads that the Scene meaningfully affects.

Link a Plot Thread when the Scene:

- establishes it
- advances it
- complicates it
- reveals important information about it
- substantially changes it
- resolves it

The qualifying question is:

> **Does this Scene meaningfully change or develop this thread?**

---

# Chronology

## timeline

Human-readable in-world chronological placement of the Scene.

Examples:

`Day 1 - Morning`

`Day 3 - After Midnight`

`Two weeks after [[Event Name]]`

`timeline` describes **story chronology**.

`scene_number` and Longform describe **manuscript organization**.

These are intentionally separate because a novel may contain flashbacks, parallel events, nonlinear storytelling, or later restructuring.

---

# Scene Planning Properties

The following Properties provide lightweight Scene-level planning without placing permanent author notes in the manuscript body.

## purpose

A concise author-facing description of what the Scene needs to accomplish.

Focus on narrative function rather than summarizing everything that happens.

## conflict

The primary source of tension, opposition, uncertainty, or resistance driving the Scene.

This may be:

- external
- interpersonal
- internal
- environmental
- or a combination

## outcome

The meaningful change produced by the Scene.

Ask:

> **What is different by the end of this Scene because the Scene occurred?**

## continuity

Author-facing reminders about Scene-specific continuity requirements, dependencies, setup, payoff, or details that must remain consistent elsewhere.

Use `continuity` for information specifically needed while writing or revising this Scene.

---

# Scene Body

The body of a Scene note is reserved for **manuscript prose**.

It is not meant to include permanent author-facing:

- planning sections
- metadata
- summaries
- outlines
- continuity notes
- headings used only for organization

Scene planning information belongs in Properties.

World information belongs in the Wiki.

Larger narrative planning belongs in Planning.

Keeping the Scene body clean ensures that the source manuscript remains easy to compile and export.

---

# Temporary Author Comments

Temporary drafting reminders may appear inside manuscript prose using Markdown or HTML comments.

Example:

`<!-- CHECK: Does the Protagonist know this yet? -->`

Use comments for short-lived drafting reminders such as:

- fact checking
- continuity checks
- missing description
- wording to revisit
- unresolved drafting decisions

The system works best when temporary author comments are reviewed and sorted into the system accordingly, rather than becoming permanent storage for important story information.

Once resolved, either remove the comment or harvest the information into the appropriate Wiki, Planning, Research, or Scene Property location.

The standard Longform compilation workflow removes comments from reader-facing output.

---

# Wikilinks in Manuscript Prose

Wikilinks are generally unnecessary inside manuscript prose because meaningful story relationships should already be represented in Scene Properties.

If a Wikilink is useful while drafting, it may be used - but generally it is not recommended to include Wikilinks in prose merely to maximize connectivity.

The goal of the manuscript is to remain readable as manuscript prose.

---

# Scene Template

The standard Scene template is:

```yaml
---
type: scene
chapter:
scene_number:
pov:
status: planned
characters: []
locations: []
organizations: []
events: []
lore: []
items: []
timeline:
plot_threads: []
purpose:
conflict:
outcome:
continuity:
---
```

The body beneath the Properties is left blank for manuscript prose.

---

# Scenes Base

`Scenes.base` provides useful views of manuscript metadata without controlling manuscript order.

Useful views may include:

- All Scenes
- Planned
- Drafting
- Revision
- By Chapter

Bases are views over source metadata.

Editing a Scene's Properties changes the source data represented by the Base.

The Base itself is not the manuscript and does not replace Longform.

---

# Longform Project

Each novel uses a Longform project with its own project folder.

For example:

```text
01 Manuscript/
    [Project Name]/
        Index.md
        [Scenes...]
```

The project Index serves Longform's project structure.

Scenes remain directly inside the project folder unless actual manuscript use demonstrates a need for additional physical organization.

Chapter structure is represented through metadata rather than requiring Chapter folders.

---

# Compilation

Compilation transforms source Scene notes into reader-facing manuscript output.

The standard Longform compile workflow is:

1. `Strip Frontmatter`
2. `Remove Comments`
3. `Remove Links`
4. `Concatenate Text`
5. `Save as Note`

Do not prepend Scene titles during compilation.

Scene filenames are author-facing organizational labels rather than reader-facing manuscript content.

Compiled output should be saved outside the Longform project folder under:

`01 Manuscript/Compiled/`

Example:

`01 Manuscript/Compiled/[Project Name] - Compiled.md`

---

# Compilation Responsibilities

The compilation pipeline intentionally separates author-facing infrastructure from reader-facing prose.

## Strip Frontmatter

Removes Scene Properties from output.

## Remove Comments

Removes temporary author-facing drafting comments.

## Remove Links

Removes Obsidian Wikilink syntax while retaining visible text.

## Concatenate Text

Combines Scenes according to Longform's manuscript order.

## Save as Note

Writes the resulting manuscript to the Compiled folder.

---

# Compilation Principle

> **Compile from the source. Never repair the generated output.**

If the compiled manuscript contains an error caused by manuscript prose, fix the source Scene.

If it contains an error caused by metadata or compilation configuration, fix the source metadata or workflow.

Then compile again.

This ensures that the individual Scene notes remain authoritative.

---

# Drafting Workflow

A typical Scene workflow is:

1. Create the Scene from the Scene Template.
2. Give it an author-facing filename.
3. Add it to the Longform project.
4. Place it in the intended Longform order.
5. Populate known Scene Properties.
6. Outline enough information to write the Scene.
7. Set `status: outlined` when appropriate.
8. Draft prose in the Scene body.
9. Use temporary comments when necessary.
10. Update meaningful entity and Plot Thread links as the Scene develops.
11. Change `status` as the Scene moves through drafting and revision.
12. Harvest newly established world or planning information into its appropriate source-of-truth notes.
13. Compile through Longform when reader-facing output is needed.

Properties do not need to be completely populated before drafting begins.

Do not let metadata completion become a prerequisite for writing! (This system is not meant to provide creative new procrastination techniques :P)

---

# Revision Workflow

When revising a Scene:

1. Read the Scene in the context of surrounding Longform order.
2. Revise the source Scene rather than compiled output.
3. Recheck `purpose`, `conflict`, and `outcome`.
4. Verify meaningful entity links still reflect the actual Scene.
5. Check `continuity` requirements.
6. Remove resolved temporary comments.
7. Harvest any newly established canon or planning decisions.
8. Update the Scene's status when appropriate.
9. Recompile as needed.

---

# Guiding Principle

The manuscript system exists to make writing easier.

Scene metadata should help answer useful questions about the manuscript without becoming an administrative burden.

When deciding whether to add metadata, links, folders, or additional structure, ask:

> **Will this help me write, navigate, understand, revise, or compile the novel?**

If not, the simpler solution is usually preferable.