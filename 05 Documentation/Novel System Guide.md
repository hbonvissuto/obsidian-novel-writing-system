# Novel Writing System

This vault is designed as a reusable environment for planning, writing, documenting, and compiling a longform fiction project in Obsidian.

The system separates four kinds of information:

1. **Manuscript** — what actually happens on the page.
2. **Wiki** — what is established as true about the story world.
3. **Planning** — what the author intends, explores, or has not yet resolved.
4. **Research** — real-world or source information used to inform the fiction.

This separation allows each part of the vault to have a clear source of truth.

---

# Core Principle

> **Store information according to what it is, not merely where it is currently useful.**

A fact about a character belongs in the Wiki even if it was discovered while outlining a scene.

A possible future development belongs in Planning even if it concerns an established character.

Historical research belongs in Research even if it may eventually inspire fictional canon.

Manuscript prose belongs in Scene notes even when it establishes new worldbuilding.

---

# Folder Structure

## `00 Dashboard`

Project navigation and short-term working context.

The Dashboard answers:

- Where do I write?
- Where do I plan?
- Where is the Wiki?
- What am I currently working on?
- What needs attention next?

The Dashboard is not a source of truth for story information.

Temporary reminders may live in its Scratchpad, but important information should eventually be moved into its proper location.

---

## `01 Manuscript`

The authoritative manuscript source.

Individual Scene notes are stored inside the Longform project folder.

Longform controls manuscript order.

Scene Properties provide author-facing metadata and relationships to the Wiki and Planning system.

Compiled manuscripts are generated output and should not be edited directly.

See [[Manuscript Workflow]].

---

## `02 Wiki`

The source of truth for established information about the fictional world.

Wiki entity types include:

- Characters
- Locations
- Organizations
- Events
- Lore
- Items

Use the Wiki for information that is established as true rather than merely planned, proposed, researched, or questioned.

See [[Wiki Property Guide]] for property vocabulary and linking conventions.

---

## `03 Planning`

Author-facing story development.

Planning contains information about what the story may or should do rather than established world truth.

Major planning tools include:

- Story Structure
- Plot Threads
- Character Arcs
- Open Questions

See [[Planning Guide]].

---

## `04 Research`

Real-world information, source material, and research used to inform the fictional world or manuscript.

Research does not become fictional canon merely because it has been collected.

Decisions derived from research should be transferred into the appropriate Wiki entry when they become established.

See [[Research Guide]].

---

## `05 Documentation`

Instructions for using and maintaining the novel-writing system itself.

Documentation describes the system rather than the fictional project.

---

## `90 Templates`

Reusable note templates.

Templates define the standard starting structure for recurring note types.

Do not store project-specific story information in templates.

---

## `99 Attachments`

Non-Markdown files used by the vault.

Current organization:

- `Images/`
- `Maps/`
- `Reference/`

Attachments should have one canonical file location even when referenced by multiple notes.

---

# Sources of Truth

The system uses the following ownership model:

| Question | Source of Truth |
| --- | --- |
| What is true about the fictional world? | Wiki |
| What do we currently intend to happen? | Planning |
| What actually happens on the page? | Manuscript |
| What is the authoritative scene order? | Longform |
| What real-world information informed a decision? | Research |
| How does the system itself work? | Documentation |
| What am I working on right now? | Dashboard |

Avoid maintaining the same information manually in multiple locations.

Links and backlinks should connect sources of truth rather than duplicate their contents.

---

# System Note Types

The `type` Property identifies the primary role of a structured note within the system.

Current system types include:

| Type | Area | Purpose |
| --- | --- | --- |
| `character` | Wiki | Character entity |
| `location` | Wiki | Location entity |
| `organization` | Wiki | Organization entity |
| `event` | Wiki | Significant fictional event |
| `lore` | Wiki | Story-world rule, system, custom, or concept |
| `item` | Wiki | Significant physical object |
| `scene` | Manuscript | Manuscript Scene |
| `plot_thread` | Planning | Developing narrative thread |
| `character_arc` | Planning | Planned character transformation |
| `story_structure` | Planning | Novel-level structural plan |
| `research` | Research | Real-world investigation or source work |
| `dashboard` | Dashboard | Project navigation and working context |

These values provide a consistent vocabulary for Properties, Bases, and future organization.

Additional types can be introduced when a project develops a meaningful need for them.

---

## Status Values

`status` is contextual rather than universal.

Different note types use different status values because they track different kinds of work.

For example, a Scene moves through writing stages, while a Plot Thread tracks narrative state and Lore tracks the state of a worldbuilding decision.

Refer to the relevant system guide or template for the recommended status values for each note type.

---

# Wiki

The Wiki describes established story-world truth.

A Wiki entry should represent a meaningful entity or concept rather than every noun appearing in the manuscript.

Properties store structured relationships and classifications.

Prose stores nuance.

> **Properties reveal relationships. Prose explains them.**

See [[Wiki Property Guide]].

---

# Planning

Planning describes intended narrative development.

## Story Structure

Provides the novel-level view of the story.

Use it for:

- major story movements
- major threads and arcs
- important reveals
- structural dependencies
- unresolved structural questions

It should remain higher-level than a scene outline.

## Plot Threads

Track individual narrative questions, conflicts, mysteries, relationships, or developments across the story.

A Plot Thread owns the development of that particular narrative thread.

## Character Arcs

Track planned character transformation.

A Character Wiki entry describes who the character is.

A Character Arc describes how the story is intended to change them.

## Open Questions

Stores unresolved authorial questions that should not yet be treated as canon.

When a question is resolved, transfer the established answer into the appropriate source-of-truth note.

See [[Planning Guide]].

---

# Manuscript

The manuscript consists of individual Scene notes managed by Longform.

Scene bodies contain manuscript prose.

Scene Properties contain author-facing metadata such as:

- POV
- status
- characters
- locations
- organizations
- events
- lore
- items
- plot threads
- purpose
- conflict
- outcome
- continuity

Record entities that are meaningfully present or relevant to the Scene rather than everything merely mentioned.

Longform controls authoritative manuscript order.

Compiled files are generated output.

See [[Manuscript Workflow]].

---

# Research

Research records information gathered from outside the fictional world.

A Research note may contain:

- a research question
- findings
- sources
- possible story applications
- canon harvested from the research

Possible applications are not canon.

When a decision becomes established fictional truth, record it in the appropriate Wiki entry.

See [[Research Guide]].

---

# Linking Philosophy

Links should represent meaningful relationships rather than exhaustive cross-referencing.

Ask:

> **Would I reasonably want to discover this note while reviewing the linked entity or concept?**

If yes, the link is probably useful.

If not, the relationship may be incidental.

Prefer meaningful links over comprehensive tagging.

Use backlinks instead of maintaining unnecessary reciprocal properties.

---

# Typical Workflow

Story development does not need to follow a rigid sequence, but a common workflow is:

1. Develop an idea in Planning or Research.
2. Resolve any necessary worldbuilding decisions.
3. Harvest established fictional truth into the Wiki.
4. Update relevant Plot Threads, Character Arcs, or Story Structure.
5. Plan a Scene using its Properties.
6. Draft manuscript prose in the Scene body.
7. Update metadata when the drafted Scene establishes or changes meaningful relationships.
8. Compile the manuscript through Longform when needed.

The direction can also reverse.

Drafting may reveal new worldbuilding, structural problems, character developments, or research questions.

When that happens, move the resulting information into the appropriate source of truth rather than allowing it to remain stranded in manuscript comments or temporary notes.

---

# Harvesting

**Harvesting** is the process of taking useful decisions produced during brainstorming, outlining, drafting, or research and placing them into their permanent source-of-truth notes.

Examples:

- established world fact → Wiki
- unresolved possibility → Open Questions
- intended narrative development → Plot Thread
- intended character transformation → Character Arc
- novel-level structural decision → Story Structure
- real-world information → Research
- manuscript text → Scene

Harvest regularly enough that important information does not remain trapped in temporary notes, conversations, or scratchpads.

---

# System Philosophy

The system should support writing rather than become a second project to maintain.

Prefer:

- native Markdown
- Obsidian Properties
- Wikilinks and backlinks
- Bases where they provide useful views
- a small plugin footprint
- simple controlled vocabularies
- human-readable files
- portable relative relationships

Avoid adding:

- metadata without a demonstrated use
- reciprocal properties that duplicate backlinks
- Bases that provide no useful view
- folders for categories that do not yet need them
- multiple sources of truth for the same information
- automation whose maintenance costs more than the problem it solves

When uncertain, begin with the simpler structure and allow actual writing to demonstrate what additional organization is necessary.