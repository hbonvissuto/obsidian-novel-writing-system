# Novel Writing System

A reusable Obsidian workspace for planning, worldbuilding, drafting, revising, and compiling a longform fiction project.

The system uses native Obsidian features wherever practical, with Longform (plugin) providing manuscript organization and compilation.

This vault is distributed in a neutral starting state. Before beginning a new novel, complete the initialization steps below to give the project its identity and connect the manuscript-specific components to the new project.

> [!important]
> Make a copy of the Novel Template base folder before beginning a new project.
>
> Keep the original template folder clean so it can be reused for future projects.

---

# Before You Begin

This system assumes that the following Obsidian features are available and enabled:

- Properties
- Bases
- Templates
- Backlinks
- standard Markdown and Wikilinks
- the Longform community plugin

The template already contains the intended configuration for these features.

You **do not** need to recreate the Bases, configure the Templates folder, rebuild the Longform compilation workflow, or configure the attachment folder during normal initialization.

---
# 1. Copy the Template

Create a copy of the `Novel Template` vault folder.

Rename the copied vault folder to the title of the new project.

For example:

    Novel Template

becomes:

    My Novel

**Open the copied folder as a new vault** in Obsidian.

The original `Novel Template` folder should remain unchanged so that it can be reused later.

---

# 2. Rename the Manuscript Project Folder

Navigate to:

    01 Manuscript/

The fresh template contains:

    01 Manuscript/
    ├── Compiled/
    ├── Manuscript/
    │   └── Index.md
    └── Scenes.base

Rename:

    Manuscript/

to the title of the novel.

For example:

    01 Manuscript/
    ├── Compiled/
    ├── My Novel/
    │   └── Index.md
    └── Scenes.base

Do not rename `Index.md`.

`Index.md` contains the Longform project definition.

Longform follows the renamed project folder automatically, so the Longform project does not need to be recreated after this change.

---

# 3. Initialize the Novel Dashboard

Open:

    00 Dashboard/Novel Dashboard.md

The filename `Novel Dashboard.md` remains unchanged. It describes the note's function within the system rather than the name of the individual project.

Set the `project` Property to the title of the novel.

For example:

    ---
    type: dashboard
    project: My Novel
    ---

Change the note's heading from:

    # Novel Title

to:

    # My Novel

The Dashboard also contains an italicized placeholder beneath the title.

Replace it when useful with a central question, premise, thematic statement, or other short touchstone for the novel.

For example:

    > *What would someone sacrifice to save the people they love?*

This is optional and can remain a placeholder while the project is still taking shape.

---

# 4. Initialize Story Structure

Open:

    03 Planning/Plot/Story Structure.md

Set its `project` Property to the title of the novel.

For example:

    ---
    type: story_structure
    status: developing
    project: My Novel
    ---

Keep the filename:

    Story Structure.md

and the heading:

    # Story Structure

unchanged.

Like `Novel Dashboard.md`, the filename describes the note's role within the system rather than the identity of the particular novel.

The rest of Story Structure may remain blank until the project develops enough to use it.

---

# 5. Initialize Longform

Open the Longform pane:

![[Pasted image 20260921215345.png]]

The template contains an existing Longform project named:

    Novel

There is no need to create a new Longform project.

## Project Title

Open:

**Longform → Project**

Change:

    Title: Novel

to the title of the project.

For example:

    Title: My Novel

The remaining project settings should already be configured as:

    Scene Folder: /
    Scene Template: 90 Templates/Scene Template.md

Leave these settings unchanged.

The `/` Scene Folder means that manuscript Scenes live directly inside the Longform project folder.

---

# 6. Configure the Compilation Destination

Open:

**Longform → Compile**

The template contains the standard compilation workflow:

1. Strip Frontmatter
2. Remove Comments
3. Remove Links
4. Concatenate Text
5. Save as Note

This workflow is already configured and normally does not need to be rebuilt.

Under **Save as Note**, change the output path from:

    ../Compiled/Novel - Compiled

to:

    ../Compiled/My Novel - Compiled

using the actual project title.

Compiled manuscripts will therefore be written to:

    01 Manuscript/Compiled/

For example:

    01 Manuscript/Compiled/My Novel - Compiled.md

> [!important]
> Compiled manuscripts are generated output.
>
> Make manuscript revisions in the source Scene notes and compile again rather than editing the compiled manuscript directly.

---

# 7. Update the Scenes Base

Open:

    01 Manuscript/Scenes.base

The template initially filters Scenes from:

    01 Manuscript/Manuscript

Because the manuscript folder was renamed during initialization, this filter must be updated manually.

Change the folder filter to:

    01 Manuscript/My Novel

using the actual project title.

Keep the existing:

    type is scene

filter and the existing Base views.

> [!note]
> Obsidian updates normal links when the manuscript folder is renamed, but the folder filter inside `Scenes.base` does not automatically follow the rename. This is therefore a required initialization step.

---

# 8. Verify Template Configuration

The vault is already configured to use:

    90 Templates

as the Obsidian Templates folder.

No change should normally be necessary.

The system includes templates for:

- Characters
- Events
- Items
- Locations
- Lore
- Organizations
- Plot Threads
- Research
- Scenes
- Character Arcs

Longform is already configured to use:

    90 Templates/Scene Template.md

when creating new Scenes.

---

# 9. Verify Attachment Configuration

The template is configured to place new attachments in:

    99 Attachments/Images

The attachment structure is:

    99 Attachments/
    ├── Images/
    ├── Maps/
    └── Reference/

These folders provide canonical locations for files used by the project.

Typically:

- `Images/` contains artwork, visual references, illustrations, and similar images.
- `Maps/` contains geographic, architectural, or spatial maps.
- `Reference/` contains PDFs, scans, diagrams, and other research-source files.

**No attachment-setting change should normally be required during initialization.**

---

# 10. Create a Test Scene

Before beginning substantial work, it is useful to verify that the initialized manuscript pipeline is functioning.

In the Longform **Scenes** tab, create:

    001 - Test Scene

The new note should appear inside:

    01 Manuscript/My Novel/

It should also appear automatically:

- in the Longform Scenes list
- in `01 Manuscript/Scenes.base`

Open the Scene.

It should contain the standard Scene Properties, including:

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

If the Scene appears in Longform and `Scenes.base`, the manuscript project, Scene Template, and Base filter are connected correctly.

The test Scene may then be deleted.

---

# 11. Optional Compilation Test

A new project can also verify the complete manuscript pipeline before drafting begins.

Create or reuse a temporary Scene and add a small amount of test prose.

For example:

    This is the first paragraph of the test novel.

    <!-- This comment should disappear from the compiled manuscript. -->

    The protagonist enters [[Test Location]] and looks around.

    This is the final paragraph.

Run the standard Longform compilation workflow.

The compiled manuscript should contain:

    This is the first paragraph of the test novel.

    The protagonist enters Test Location and looks around.

    This is the final paragraph.

Verify that:

- Scene Properties/frontmatter are absent
- temporary comments are absent
- Wikilink syntax is removed while visible text remains
- author-facing Scene filenames do not appear as manuscript headings
- the output appears under `01 Manuscript/Compiled/`

Once verified, delete the temporary Scene and compiled test output.

---

# Initialization Checklist

Before beginning the novel, confirm:

- [ ] The `Novel Template` was copied rather than modified directly.
- [ ] The copied vault has been given the project's name.
- [ ] `01 Manuscript/Manuscript/` has been renamed to the project's name.
- [ ] `Novel Dashboard.md` has the correct `project` Property.
- [ ] The Dashboard H1 displays the project's name.
- [ ] `Story Structure.md` has the correct `project` Property.
- [ ] Longform's project Title has been changed from `Novel` to the project's name.
- [ ] Longform still uses `/` as the Scene Folder.
- [ ] Longform still uses `90 Templates/Scene Template.md` as the Scene Template.
- [ ] The Longform compile output uses the project's name.
- [ ] `Scenes.base` filters the renamed manuscript folder.
- [ ] Obsidian Templates uses `90 Templates`.
- [ ] New attachments are directed to `99 Attachments/Images`.
- [ ] A test Scene can be created successfully.
- [ ] The test Scene appears in both Longform and `Scenes.base`.
- [ ] Compilation produces clean reader-facing prose.

Once these checks pass, the novel is initialized and ready for use.

---

# Where Information Belongs

The system separates information according to what it represents.

| Information | Home |
| --- | --- |
| What actually happens on the page | `01 Manuscript/` |
| Established fictional truth | `02 Wiki/` |
| Intended story development | `03 Planning/` |
| Real-world research and sources | `04 Research/` |
| Instructions for using the system | `05 Documentation/` |
| Reusable note structures | `90 Templates/` |
| Images, maps, and reference files | `99 Attachments/` |

Longform controls manuscript Scene order.

Individual Scene notes are the authoritative source for manuscript prose.

Bases provide views over source metadata rather than becoming separate sources of truth.

---

# Start Working

Once initialization is complete, there is no required order in which the novel must be developed.

You may begin by:

- creating a Character
- developing the Story Structure
- creating a Plot Thread
- recording an Open Question
- researching a subject
- building the Wiki
- creating the first Scene
- or simply beginning to draft

The system is intended to support different writing processes rather than prescribe one.

Properties, Planning notes, Wiki entries, and other infrastructure can be filled in as they become useful.

> **The system exists to support the novel, not to become a prerequisite for writing it.**

---

# Further Documentation

For a deeper explanation of the system, see:

- [[05 Documentation/Novel System Guide|Novel System Guide]]
- [[05 Documentation/Manuscript Workflow|Manuscript Workflow]]
- [[05 Documentation/Planning Guide|Planning Guide]]
- [[05 Documentation/Research Guide|Research Guide]]
- [[02 Wiki/Wiki Property Guide|Wiki Property Guide]]

`Novel System Guide` is the best place to begin after initialization.
