# Obsidian Novel Writing System

A reusable Obsidian workspace for planning, worldbuilding, drafting, revising, and compiling longform fiction.

The system combines a Longform-managed manuscript with an interconnected story Wiki, flexible planning tools, research notes, reusable templates, and Obsidian Bases. It is designed to keep the novel itself at the center while giving supporting information a clear place to live.

> **The system exists to support the novel, not to become a prerequisite for writing it.**

---

## What This Is

The Obsidian Novel Writing System is a reusable starting point for managing a novel inside a single Obsidian vault.

It provides dedicated spaces for:

- drafting and organizing manuscript Scenes
- maintaining a story Wiki for characters, locations, organizations, events, lore, and items
- developing plot threads, character arcs, story structure, and open questions
- collecting real-world research separately from fictional canon
- managing reusable note templates and Properties
- viewing project information dynamically through Obsidian Bases
- compiling manuscript Scenes into clean reader-facing prose with Longform

The system is intended to work with different writing processes rather than prescribe one.

An extensive outliner can build the Wiki and Planning sections before drafting. A discovery writer can begin with the first Scene and add structure only when it becomes useful. A project can also move back and forth between those approaches as it develops.

---

## Design Philosophy

### Markdown Is the Source of Truth

The durable parts of the project live in ordinary Markdown notes and Obsidian Properties.

Bases provide dynamic views over that information rather than becoming separate databases that must be maintained independently.

Longform manages manuscript organization and compilation, while the individual Scene notes remain the authoritative source for manuscript prose.

### Separate Different Kinds of Information

The system gives different kinds of information different homes:

| Information | Home |
| --- | --- |
| What actually happens on the page | `01 Manuscript/` |
| Established fictional truth | `02 Wiki/` |
| Intended story development | `03 Planning/` |
| Real-world research and sources | `04 Research/` |
| Instructions for using the system | `05 Documentation/` |
| Reusable note structures | `90 Templates/` |
| Images, maps, and reference files | `99 Attachments/` |

This separation helps distinguish what **is true in the story** from what you **intend to happen**, what has actually made it **onto the page**, and what comes from **outside research**.

### Add Structure When It Helps

There is no required order for developing a novel.

Properties, Wiki entries, Plot Threads, Character Arcs, research notes, and other infrastructure can be filled in as they become useful.

The system should grow alongside the novel rather than requiring the novel to conform to the system.

---

## What's Included

A fresh copy contains the following structure:

```text
00 Dashboard/
    Novel Dashboard.md

01 Manuscript/
    Compiled/
    Manuscript/
        Index.md
    Scenes.base

02 Wiki/
    Characters/
        Characters.base
    Events/
        Events.base
    Items/
        Items.base
    Locations/
        Locations.base
    Lore/
        Lore.base
    Organizations/
        Organizations.base
    Wiki Home.md
    Wiki Property Guide.md

03 Planning/
    Character Arcs/
        Character Arcs.md
    Notes/
        Open Questions.md
    Plot/
        Plot Threads/
        Plot Threads.base
        Story Structure.md

04 Research/

05 Documentation/
    Manuscript Workflow.md
    Novel System Guide.md
    Planning Guide.md
    Research Guide.md

90 Templates/
    Character Arc Template.md
    Character Template.md
    Event Template.md
    Item Template.md
    Location Template.md
    Lore Template.md
    Organization Template.md
    Plot Thread Template.md
    Research Template.md
    Scene Template.md

99 Attachments/
    Images/
    Maps/
    Reference/
```

The template begins in a neutral state so that it can be copied and initialized for a new novel without carrying project-specific material from another story.

---

## Requirements

### Obsidian

This system requires **Obsidian 1.9.10 or later**. It uses the following Obsidian features:

- Properties
- Bases
- Templates
- Backlinks
- Wikilinks
- standard Markdown

Bases is a core part of the system and is used throughout the vault to provide dynamic views over Markdown notes and their Properties.

The template includes the configuration needed for its folder structure, Properties, Bases, Templates, and attachment handling.

### Longform

[Longform](https://github.com/kevboh/longform) is the only required community plugin.

Longform provides:

- manuscript project management
- Scene ordering
- automatic use of the Scene Template
- manuscript compilation

The template includes its intended Longform project configuration and compilation workflow, but **Longform itself is not bundled with this repository**.

Install and enable Longform through Obsidian's Community Plugins interface after opening the vault.

No other community plugins are required for the core system.

---

## Getting Started

You do not need Git or any programming tools to use this system.

The easiest way to begin is to download a copy of the template from GitHub and use it as the starting point for your novel.

1. Click **Code → Download ZIP** on this repository's GitHub page.
2. Extract the downloaded ZIP file somewhere on your computer.
3. Rename the extracted folder to the title of your novel.
4. Open the renamed folder as an Obsidian vault.
5. Install and enable the Longform community plugin.
6. Complete the **Project Initialization** steps below.
7. Create a test Scene to verify the manuscript pipeline.
8. Start writing.

Once downloaded, the novel is an ordinary local Obsidian vault. You do not need GitHub to continue using it.

The template already contains its folder structure, Bases, note templates, Property configuration, attachment structure, and Longform workflow. Project initialization connects those reusable components to the identity of your new novel.

Once initialized, you can begin wherever the novel needs you: create a Character, explore the Story Structure, start a Plot Thread, collect Research, build the Wiki, or simply write the first Scene.

---

# Project Initialization

> [!note]
> The downloaded template becomes the starting point for your novel. During initialization, you will personalize its neutral project settings with your novel's title.
>
> Keeping a separate untouched copy of the template is optional and is only necessary if you want a convenient local starting point for future novels.


## 1. Create Your Novel Vault

After downloading the repository as a ZIP file, extract it somewhere on your computer.

The extracted folder is the starting vault for your novel.

Rename that folder to the title of your project.

For example:

```text
novel-template
```

becomes:

```text
My Novel
```

You may place the folder wherever you normally keep your writing projects or Obsidian vaults.

Open Obsidian and choose:

**Open folder as vault**

Select the renamed project folder.

Your novel now has its own local Obsidian vault.

---

## 2. Rename the Manuscript Project Folder

Navigate to:

```text
01 Manuscript/
```

The fresh template contains:

```text
01 Manuscript/
├── Compiled/
├── Manuscript/
│   └── Index.md
└── Scenes.base
```

Rename:

```text
Manuscript/
```

to the title of the novel.

For example:

```text
01 Manuscript/
├── Compiled/
├── My Novel/
│   └── Index.md
└── Scenes.base
```

Do not rename `Index.md`.

`Index.md` contains the Longform project definition.

Longform follows the renamed project folder automatically, so the Longform project does not need to be recreated after this change.

---

## 3. Initialize the Novel Dashboard

Open:

```text
00 Dashboard/Novel Dashboard.md
```

The filename `Novel Dashboard.md` remains unchanged. It describes the note's function within the system rather than the name of the individual project.

Set the `project` Property to the title of the novel.

For example:

```yaml
---
type: dashboard
project: My Novel
---
```

Change the note's heading from:

```markdown
# Novel Title
```

to:

```markdown
# My Novel
```

The Dashboard also contains an italicized placeholder beneath the title.

Replace it when useful with a central question, premise, thematic statement, or other short touchstone for the novel.

For example:

```markdown
> *What would someone sacrifice to save the people they love?*
```

This is optional and can remain a placeholder while the project is still taking shape.

---

## 4. Initialize Story Structure

Open:

```text
03 Planning/Plot/Story Structure.md
```

Set its `project` Property to the title of the novel.

For example:

```yaml
---
type: story_structure
status: developing
project: My Novel
---
```

Keep the filename:

```text
Story Structure.md
```

and the heading:

```markdown
# Story Structure
```

unchanged.

Like `Novel Dashboard.md`, the filename describes the note's role within the system rather than the identity of the particular novel.

The rest of Story Structure may remain blank until the project develops enough to use it.

---

## 5. Initialize Longform

Open the Longform pane.

The template contains an existing Longform project named:

```text
Novel
```

There is no need to create a new Longform project.

### Project Title

Open:

**Longform → Project**

Change:

```text
Title: Novel
```

to the title of the project.

For example:

```text
Title: My Novel
```

The remaining project settings should already be configured as:

```text
Scene Folder: /
Scene Template: 90 Templates/Scene Template.md
```

Leave these settings unchanged.

The `/` Scene Folder means that manuscript Scenes live directly inside the Longform project folder.

---

## 6. Configure the Compilation Destination

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

```text
../Compiled/Novel - Compiled
```

to:

```text
../Compiled/My Novel - Compiled
```

using the actual project title.

Compiled manuscripts will therefore be written to:

```text
01 Manuscript/Compiled/
```

For example:

```text
01 Manuscript/Compiled/My Novel - Compiled.md
```

> [!important]
> Compiled manuscripts are generated output.
>
> Make manuscript revisions in the source Scene notes and compile again rather than editing the compiled manuscript directly.

---

## 7. Update the Scenes Base

Open:

```text
01 Manuscript/Scenes.base
```

The template initially filters Scenes from:

```text
01 Manuscript/Manuscript
```

Because the manuscript folder was renamed during initialization, this filter must be updated manually.

Change the folder filter to:

```text
01 Manuscript/My Novel
```

using the actual project title.

Keep the existing:

```text
type is scene
```

filter and the existing Base views.

> [!note]
> Obsidian updates normal links when the manuscript folder is renamed, but the folder filter inside `Scenes.base` does not automatically follow the rename. This is therefore a required initialization step.

### Already Configured for You

The template includes several settings that should not require changes during normal project initialization.

Obsidian is configured to use:

```text
90 Templates
```

as its Templates folder.

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

Longform is configured to use:

```text
90 Templates/Scene Template.md
```

when creating new manuscript Scenes.

New attachments are configured to use:

```text
99 Attachments/Images
```

The attachment structure also provides:

```text
99 Attachments/
├── Images/
├── Maps/
└── Reference/
```

These settings are part of the reusable template configuration and normally do not need to be changed when initializing a new novel.

---

## 8. Create a Test Scene

Before beginning substantial work, it is useful to verify that the initialized manuscript pipeline is functioning.

In the Longform **Scenes** tab, create:

```text
001 - Test Scene
```

The new note should appear inside:

```text
01 Manuscript/My Novel/
```

It should also appear automatically:

- in the Longform Scenes list
- in `01 Manuscript/Scenes.base`

Open the Scene.

It should contain the standard Scene Properties, including:

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

If the Scene appears in Longform and `Scenes.base`, the manuscript project, Scene Template, and Base filter are connected correctly.

The test Scene may then be deleted.

---

## 9. Optional Compilation Test

A new project can also verify the complete manuscript pipeline before drafting begins.

Create or reuse a temporary Scene and add a small amount of test prose.

For example:

```markdown
This is the first paragraph of the test novel.

<!-- This comment should disappear from the compiled manuscript. -->

The protagonist enters [[Test Location]] and looks around.

This is the final paragraph.
```

Run the standard Longform compilation workflow.

The compiled manuscript should contain:

```markdown
This is the first paragraph of the test novel.

The protagonist enters Test Location and looks around.

This is the final paragraph.
```

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

- [ ] The downloaded template has been extracted to a local folder.
- [ ] The vault folder has been renamed to the project's name.
- [ ] The project folder has been opened as an Obsidian vault.
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

# Further Documentation

For a deeper explanation of the system, see:

- [[05 Documentation/Novel System Guide|Novel System Guide]]
- [[05 Documentation/Manuscript Workflow|Manuscript Workflow]]
- [[05 Documentation/Planning Guide|Planning Guide]]
- [[05 Documentation/Research Guide|Research Guide]]
- [[02 Wiki/Wiki Property Guide|Wiki Property Guide]]

`Novel System Guide` is the best place to begin after initialization.