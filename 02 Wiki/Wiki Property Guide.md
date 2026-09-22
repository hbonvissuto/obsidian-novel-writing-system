# Wiki Property Guide

This document defines how Wiki entries are documented, classified, and linked.

The Wiki is the source of truth for established information about the story world.

It records **what is true**, rather than what is planned to happen in the manuscript.

Planning information belongs in `03 Planning/`. Manuscript information belongs in `01 Manuscript/`.

---

# General Principles

## Properties vs. Prose

Properties store structured information that is useful for filtering, browsing, linking, and identifying relationships between Wiki entities.

Use note prose for nuance, explanation, history, uncertainty, and information that does not benefit from structured metadata.

Do not create a property simply because a fact could theoretically be represented as metadata.

## Controlled Vocabulary

- Use lowercase values unless the value is a `[[Wiki Link]]`.
- Prefer singular nouns: `city`, not `cities`.
- Use the established vocabulary in this guide whenever possible.
- Add a new value only when an existing value does not adequately describe the entity.
- Leave a property blank when information is unknown.
- Do not use `unknown`, `n/a`, or `none` unless that state itself is meaningful.

## Wiki Links

When a property refers to another established Wiki entity, use an Obsidian `[[Internal Link]]` rather than plain text.

Example:

`[[The Choir]]`

Use links to represent **meaningful relationships**, not every possible association.

Ask:

> **Would I reasonably want this entity to appear when reviewing the linked entity's backlinks or related entries?**

If yes, create the relationship.

If not, leave it out.

Prefer fewer meaningful links over exhaustive tagging.

## Relationship Ownership

Do not create reciprocal properties solely to represent the same relationship in both directions.

If one entity naturally owns the relationship, record it there and allow Obsidian backlinks to expose the reverse relationship.

Explain complicated or nuanced relationships in prose rather than attempting to encode the entire relationship in Properties.

---

# Wiki Entity Types

Every Wiki entry uses the `type` property to identify its fundamental entity type.

Supported Wiki types:

- `character`
- `location`
- `organization`
- `event`
- `lore`
- `item`

These values describe the kind of Wiki entity represented by the note.

Planning and manuscript note types such as `scene`, `plot_thread`, `character_arc`, `story_structure`, and `dashboard` are documented separately and are not Wiki entity types.

---

# Character

## Required Type

`type: character`

## role

Describes the character's narrative function.

Recommended values:

- `protagonist`
- `antagonist`
- `deuteragonist`
- `major`
- `supporting`
- `minor`
- `background`

Use `role` for narrative importance, not occupation, profession, social class, or political position.

## species

The established name for the character's species.

Current values include:

- `human`
- `vampire`
- `half-vampire`

Add setting-specific species as they become established.

## status

Describes the character's current state in the story world.

Recommended values:

- `alive`
- `dead`
- `missing`
- `unknown`

Use `unknown` only when the character's status is genuinely unknown rather than merely undecided by the author.

## aliases

Use Obsidian's Aliases property for established alternate names, nicknames, titles, or identities.

Examples:

- `Fi`
- `Vigil`

## affiliations

List of meaningful `[[Organization]]` relationships.

Example:

`[[The Choir]]`

An affiliation does not necessarily imply formal membership.

Explain the nature of complicated relationships in prose.

## locations

List of `[[Location]]` entries meaningfully associated with the character.

Use this for important or persistent relationships such as home, workplace, territory, or another location strongly connected to the character.

Do not list every location the character visits.

## first_appearance

Link to the first manuscript Scene in which the character appears.

---

# Location

## Required Type

`type: location`

## aliases

Use Obsidian's Aliases property for established alternate names, historical names, colloquial names, or local nicknames.

Example:

`Bell Quarter`

Aliases:

- `Bells`
- `The Bell`

## location_type

Describes the primary kind of location.

### Geographic

- `world`
- `continent`
- `country`
- `region`
- `territory`
- `wilderness`
- `forest`
- `mountain`
- `river`
- `lake`

### Settlement

- `city`
- `town`
- `village`
- `settlement`

### Subdivision

- `district`
- `neighborhood`
- `street`

### Structure

- `building`
- `residence`
- `palace`
- `castle`
- `fortress`
- `temple`
- `tavern`
- `shop`
- `market`
- `warehouse`
- `prison`
- `monument`

### Other

- `ruin`
- `underground`
- `site`

Prefer the most specific useful term.

Do not create unnecessary distinctions between location types unless they are useful for browsing or filtering the Wiki.

## status

Describes the location's current physical or functional state.

Recommended values:

- `active`
- `abandoned`
- `destroyed`
- `ruined`
- `hidden`

## parent_location

Link to the location that directly contains this location.

Example:

If `[[Bell Quarter]]` is a district within `[[Barrowmere]]`:

`parent_location: [[Barrowmere]]`

Prefer `parent_location` for the immediate geographic hierarchy.

## region

Link to a broader geographic region when that relationship is useful independently of `parent_location`.

Example:

`[[Northern Marches]]`

Do not populate `region` merely to duplicate `parent_location`.

## first_appearance

Link to the first manuscript Scene in which the location appears.

---

# Organization

## Required Type

`type: organization`

## organization_type

Describes the organization's primary function or identity.

### Government / Political

- `government`
- `political`
- `noble_house`
- `court`

### Religious

- `religious`
- `religious_order`

### Military / Security

- `military`
- `guard`
- `militia`

### Economic

- `merchant`
- `guild`
- `company`

### Criminal / Covert

- `criminal`
- `gang`
- `secret_society`
- `intelligence`

### Social / Academic

- `academic`
- `civic`
- `social`

Add setting-specific categories only when an established value does not adequately describe the organization.

## status

Describes the organization's current state.

Recommended values:

- `active`
- `inactive`
- `dissolved`
- `destroyed`
- `secret`

## leader

Link to the current primary `[[Character]]` leader when one exists.

Use prose for organizations with complex leadership structures rather than attempting to encode the entire hierarchy in this property.

## headquarters

Link to the organization's single primary `[[Location]]` headquarters when one exists.

## areas_of_influence

List of `[[Location]]` entries where the organization exercises meaningful influence, authority, control, or sustained activity.

Do not list every location in which a member has appeared.

## first_appearance

Link to the first manuscript Scene where the organization appears or becomes meaningfully relevant to the reader.

---

# Event

## Required Type

`type: event`

## event_type

Describes the primary nature of the event.

Prefer the most specific useful value.

### Personal

- `birth`
- `death`
- `marriage`
- `betrayal`
- `disappearance`

### Conflict

- `battle`
- `attack`
- `murder`
- `uprising`
- `war`

### Political / Social

- `political`
- `coronation`
- `treaty`
- `law`
- `protest`

### Discovery / Change

- `discovery`
- `invention`
- `founding`
- `destruction`
- `migration`

### Other

- `historical`
- `supernatural`
- `disaster`
- `other`

Use a more specific value instead of `historical` whenever possible.

`historical` describes an event primarily useful as historical background when no more specific established category adequately describes it.

## status

Describes the event's chronological state.

Recommended values:

- `upcoming`
- `ongoing`
- `completed`
- `uncertain`

Use `uncertain` when the event's occurrence or current state is genuinely uncertain within established canon.

## date

Human-readable in-world date or chronology description.

Examples:

- `Year 417`
- `Third Day of Winter`
- `approximately 80 years before the story`

## end_date

Use only when the event spans a meaningful period and recording its end separately is useful.

## location

Link to the primary `[[Location]]` where the event occurs.

Use prose or related links for geographically complex events.

## participants

List of important `[[Character]]` participants.

Include characters whose participation meaningfully defines or affects the event.

## organizations

List of `[[Organization]]` entries meaningfully involved in the event.

## related_events

List of directly related `[[Event]]` entries.

Use this for meaningful causal, chronological, or historical relationships rather than every event occurring near the same time.

## first_appearance

Link to the first manuscript Scene where the reader encounters or learns about the event.

---

# Lore

## Required Type

`type: lore`

Lore represents systems, rules, concepts, customs, knowledge, and other worldbuilding that are better represented as subjects than as discrete characters, locations, organizations, events, or items.

## lore_type

A Lore entry may use multiple `lore_type` values.

Use every type that materially describes what the note fundamentally explains, but prefer approximately 1–3 values.

Do not add a type merely because the subject happens to touch that area.

### World / Nature

- `supernatural`
- `biology`
- `ecology`
- `geography`

### Society

- `culture`
- `custom`
- `religion`
- `politics`
- `law`
- `economy`

### Knowledge

- `history`
- `folklore`
- `language`
- `technology`
- `medicine`

### Systems

- `magic`
- `resource`
- `currency`

Examples:

`Vampire Feeding` → `biology`

`Tooth Economy` → `economy`, `currency`

A supernatural cause does not automatically make something `supernatural`.

Use `supernatural` when the note fundamentally explains supernatural rules or phenomena.

## status

Describes the **authorial status** of the Lore entry rather than its state within the fictional world.

Recommended values:

- `canon` — established world fact
- `developing` — current working concept not yet fully established
- `question` — unresolved worldbuilding issue represented as a Lore entry
- `deprecated` — formerly used concept no longer considered canon

Unresolved questions that do not yet warrant their own Wiki entry should remain in the project's Open Questions note rather than creating placeholder Lore.

## scope

Describes the general scale or population to which the Lore applies.

Recommended values:

- `world`
- `regional`
- `local`
- `cultural`
- `organizational`
- `individual`

`scope` describes the **kind of scope**, not the specific entity.

Use the appropriate related property to identify the entity itself.

Example:

For `Clover's Blood`:

`scope: individual`

and:

`related_characters: [[Clover]]`

## related_locations

List of `[[Location]]` entries meaningfully connected to the Lore.

## related_organizations

List of `[[Organization]]` entries meaningfully connected to the Lore.

## related_characters

List of `[[Character]]` entries meaningfully connected to the Lore.

Do not list every character affected by a universal world rule.

For example, a general rule of vampire biology does not need links to every vampire character.

## related_lore

List of closely connected `[[Lore]]` concepts.

Use this when another Lore entry materially helps explain, depend upon, contrast with, or contextualize the current entry.

## first_appearance

Link to the first manuscript Scene where the concept becomes meaningfully relevant to the reader.

---

# Item

## Required Type

`type: item`

Items are discrete physical objects that have enough narrative, historical, cultural, or mechanical significance to warrant their own Wiki entry.

Do not create Item entries for ordinary objects solely because they appear in the manuscript.

## aliases

Use Obsidian's Aliases property for alternate names, historical names, nicknames, titles, or other established names for the item.

## item_type

Describes the primary kind of object.

Recommended values:

- `weapon`
- `tool`
- `artifact`
- `relic`
- `document`
- `book`
- `token`
- `currency`
- `clothing`
- `jewelry`
- `container`
- `key`
- `medicine`
- `technology`
- `resource`
- `other`

Prefer the most specific useful term.

Use `artifact` for an unusual or significant object whose importance primarily comes from its special properties or function.

Use `relic` for an object whose significance primarily comes from its historical, cultural, or religious importance.

Use `currency` for a physical object that functions as currency. The economic or monetary system surrounding it should be represented as Lore with `lore_type: currency`.

## status

Describes the item's current state or availability.

Recommended values:

- `active`
- `lost`
- `destroyed`
- `hidden`
- `unknown`

Use:

- `active` — the item still exists and its whereabouts or availability are not otherwise notable
- `lost` — the item may still exist but its location is unknown
- `destroyed` — the item no longer exists in usable form
- `hidden` — the item's location is deliberately concealed
- `unknown` — its current state has not been established

## owner

Link to the current owner or possessor when meaningful and known.

This will usually be a `[[Character]]` or `[[Organization]]`.

Leave blank when the item has no meaningful owner or its ownership is unknown.

## creator

Link to the entity responsible for creating the item when relevant.

This may be a `[[Character]]`, `[[Organization]]`, or another appropriate Wiki entity.

## origin

Link to the Wiki entity most useful for representing the item's origin.

This may be a `[[Location]]`, `[[Organization]]`, `[[Event]]`, or another appropriate entity.

Explain complicated origins in prose rather than attempting to encode the item's entire history in this property.

## locations

List of important `[[Location]]` entries associated with the item.

Use this for meaningful or persistent location relationships, not every place through which the item has passed.

## related_lore

List of closely related `[[Lore]]` concepts.

Use this for systems, rules, customs, technologies, economies, or supernatural principles that meaningfully explain the item.

Example:

`[[Tooth Economy]]`

## first_appearance

Link to the first manuscript Scene in which the item appears or becomes meaningfully relevant to the reader.

---

# First Appearance Rule

The `first_appearance` property identifies the first manuscript Scene in which an entity becomes meaningfully present to the reader.

It is available for:

- Characters
- Locations
- Organizations
- Events
- Lore
- Items

Do not treat a trivial name-drop as a first appearance unless that mention meaningfully introduces the entity or concept to the reader.

Use a link to the Scene note.

Example:

`[[001 - Clover and René Aqueduct Rendezvous]]`

---

# Linking Philosophy

Wiki links should reveal useful story-world relationships rather than attempt to reproduce every possible connection between notes.

## Link when the relationship is meaningful

A relationship is usually worth recording when it helps answer questions such as:

- Where does this character belong?
- What organization influences this location?
- Who participated in this event?
- What Lore explains this Item?
- Which characters are specifically connected to this Lore?
- What larger location contains this place?

## Do not link merely because something is mentioned

Incidental references do not require structured relationships.

A character mentioning another character does not automatically establish an `affiliations` relationship.

A character visiting a location once does not automatically make it one of their `locations`.

A universal world rule does not need `related_characters` links to everyone affected by it.

## Prefer the natural owner of a relationship

When one note naturally owns a relationship, record it there rather than maintaining duplicate reciprocal properties.

Use backlinks to discover the reverse relationship.

## Use prose for complexity

Properties should remain concise and structurally useful.

If understanding a relationship requires explanation, exceptions, chronology, motivation, uncertainty, or context, describe it in the body of the appropriate Wiki note.

> **Properties reveal relationships. Prose explains them.**