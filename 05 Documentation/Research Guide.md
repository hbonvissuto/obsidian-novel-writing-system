
This document defines how research and external reference material can be organized and used within the novel-writing system.

Research is the source of truth for **real-world information, source material, and investigation used to inform the fiction**.

Research is separate from fictional canon.

Information gathered during research may influence the story, but it becomes established fictional truth only when the author makes that decision and harvests the result into the Wiki.

---

# Research Architecture

Research notes are stored under:

```text
04 Research/
```

The folder can remain relatively simple while the amount of research is small.

Additional folders, categories, or organizational systems can be introduced if the volume or nature of a project demonstrates a need for them.

Supporting non-Markdown source files may be stored under:

```text
99 Attachments/
    Reference/
```

This creates a useful distinction:

- **Research notes** contain the author's questions, findings, interpretations, and possible applications.
- **Reference attachments** contain external files used by that research.

---

# Research vs. Wiki

Research asks:

> **What can I learn that might inform the story?**

The Wiki asks:

> **What have I established as true within the fictional world?**

These are related but distinct.

A historical practice, scientific principle, architectural feature, cultural custom, or other real-world finding may inspire fictional worldbuilding without being reproduced exactly.

Research therefore remains evidence and inspiration rather than automatically becoming canon.

When research leads to an established fictional decision, the resulting story-world information can be harvested into the appropriate Wiki entry.

The original research may remain available as a record of the source material that informed the decision.

---

# Research Notes

A Research note uses:

`type: research`

Recommended Properties:

```yaml
---
type: research
status: active
---
```

The intentionally small property set keeps research lightweight.

Additional metadata can be introduced if a project develops a genuine need for more detailed source management.

---

## status

Recommended values:

- `active`
- `complete`

**`active`** — the question is still being investigated or the note is still receiving useful material.

**`complete`** — the research has answered its current purpose sufficiently for the project.

A completed Research note can always become active again if new questions emerge.

Research does not need to become exhaustive before it is considered complete.

---

# Research Note Body

The standard Research Template uses:

```markdown
# Research Question

## Findings

## Sources

## Story Applications

## Canon Harvest
```

Each section serves a different purpose.

---

## Research Question

Describe what the research is trying to understand, verify, or explore.

A focused question can help prevent research from expanding indefinitely without a clear connection to the project.

The question may be narrow or broad depending on the author's needs.

---

## Findings

Record useful information discovered during research.

This section may contain:

- summaries
- factual notes
- terminology
- historical context
- technical details
- comparisons
- observations
- excerpts or quotations where appropriate
- links to relevant supporting material

Findings represent what was learned from research rather than what has necessarily been adopted into the fictional world.

---

## Sources

Record enough information to locate important sources again.

Depending on the source, this may include:

- title
- author or creator
- publication
- date
- URL
- book or article information
- page numbers
- local reference attachment
- other identifying information useful to the author

The level of citation detail can reflect the needs of the project.

A novel-writing vault does not necessarily require academic citation standards, but a source is most useful when the author can find it again later.

---

## Story Applications

Record possible ways the research could influence the story.

These may include:

- worldbuilding possibilities
- character ideas
- setting details
- plot opportunities
- sensory details
- terminology
- technologies
- customs
- conflicts
- thematic connections

Story Applications are exploratory.

They can remain tentative, contradictory, or incomplete while the author considers how the research might be transformed into fiction.

---

## Canon Harvest

Record established fictional decisions that resulted from the research.

When possible, link to the Wiki entries where those decisions now live.

For example:

```text
Research Finding
      ↓
Possible Story Application
      ↓
Authorial Decision
      ↓
Wiki
```

The Wiki becomes the source of truth for the fictional result.

The Research note preserves where the idea came from and how it developed.

This distinction makes it possible to change the fictional version without needing to rewrite the underlying research.

---

# Research Template

The standard template is:

```yaml
---
type: research
status: active
---
```

followed by:

```markdown
# Research Question

<!-- What am I trying to understand or verify? -->

## Findings

<!-- Relevant real-world information or source-derived material. -->

## Sources

<!-- Record enough information to locate the source again. -->

## Story Applications

<!-- Possible uses in the novel. These are possibilities, not established canon. -->

## Canon Harvest

<!-- Link Wiki entries that received established facts or decisions derived from this research. -->
```

---

# Reference Attachments

External files retained for research may be stored under:

```text
99 Attachments/Reference/
```

Examples may include:

- PDFs
- scans
- downloaded documents
- diagrams
- historical reference material
- source images used primarily for research

A Research note can link to or embed these files where useful.

The attachment is the retained source material.

The Research note is the author's working understanding of that material.

---

# Images and Maps

The broader attachment structure is:

```text
99 Attachments/
    Images/
    Maps/
    Reference/
```

These categories describe how files are primarily used within the vault.

## Images

Useful for visual material embedded in or associated with project notes, such as:

- character art
- location art
- organization symbols
- item illustrations
- visual inspiration

## Maps

Useful for:

- world maps
- regional maps
- city maps
- district maps
- building layouts
- geographic sketches

Maps receive their own category because they often function as persistent working documents rather than ordinary illustrations.

## Reference

Useful for external source files retained primarily for research or consultation.

The categories are organizational conveniences rather than strict creative boundaries. Files can be moved or reorganized if another arrangement better serves the project.

---

# Attachment Location

A useful default Obsidian attachment location is:

`99 Attachments/Images`

This gives pasted and imported images a predictable location rather than allowing them to accumulate beside manuscript or Wiki notes.

Maps and reference files can be moved into their appropriate subfolders when useful.

Because Obsidian provides a single default attachment destination rather than automatically classifying files by purpose, some manual organization may still be useful.

---

# Canonical Attachment Location

An attachment generally works best with **one canonical file location**, even when multiple notes reference it.

For example, one map stored under:

`99 Attachments/Maps/`

can be embedded or linked from multiple Wiki, Planning, or Research notes.

This reduces duplicate files and makes later updates easier to manage.

---

# Portable Filenames

Because a vault may eventually move between different operating systems and synchronization tools, portable filenames reduce compatibility problems.

For broad cross-platform compatibility, filenames are best kept free of:

`< > : " / \ | ? *`

It is also useful to avoid files whose names differ only by capitalization.

For example:

```text
Character.png
character.png
```

may behave differently across filesystems.

Unicode characters and meaningful accents can generally remain part of filenames.

The goal is portability without unnecessarily stripping meaningful language from the project.

---

# Research Workflow

A typical research workflow is:

1. Identify a question that would benefit from outside information.
2. Create or update a Research note.
3. Record useful findings and sources.
4. Consider possible Story Applications.
5. Make whatever fictional decisions serve the story.
6. Harvest established fictional decisions into the Wiki.
7. Link those Wiki entries under Canon Harvest when useful.
8. Mark the research `complete` once it has sufficiently served its current purpose.

Research can be reopened whenever the story creates new questions.

---

# Research During Planning and Drafting

Research does not need to happen before outlining or drafting.

A Planning note may reveal a research question.

A Scene may expose a missing technical detail.

A Wiki entry may identify an area where the fictional system needs better grounding.

Those questions can move into Research and later return to the story as established decisions.

A useful conceptual flow is:

```text
Planning / Manuscript / Wiki
            ↓
     Research Question
            ↓
         Research
            ↓
    Story Application
            ↓
    Authorial Decision
            ↓
           Wiki
```

The process can repeat whenever the project develops new needs.

---

# Avoiding Research as Procrastination

Research can deepen a novel, but it can also expand indefinitely.

A useful stopping question is:

> **Do I know enough to make the story decision or write the material that prompted this research?**

If yes, the research may have served its purpose even if much more could theoretically be learned.

The `complete` status therefore means **sufficient for the project's current needs**, not exhaustive knowledge of the subject.

---

# Guiding Principle

> **Research informs the fiction; the author decides the fiction.**

Preserve enough information to understand and relocate useful sources.

Explore possible applications freely.

When a fictional decision becomes established, place that result in the appropriate source of truth rather than requiring the Research note itself to carry the burden of canon.