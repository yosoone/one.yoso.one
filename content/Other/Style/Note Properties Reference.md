---
publish: true
permalink: /Other/Style/Note Properties Reference.md
description: Canonical reference for YAML properties on every note type in the vault — the single source of truth that the Style Guide and the formatting skills defer to.
created: 2026-09-02
modified: 2026-10-06T05:52:34.852Z
published: 2026-09-02
tags:
  - reference
  - properties
---

[[Style Guide]]

# Note Properties — Reference

_The single source of truth for YAML frontmatter. [[Style Guide]] and the vault's formatting skills defer to this file — change it here first, then propagate._

---

## Two note types

**There are no Daily Notes.** Every dated note is a Unique Note. `type: daily` is retired — never write it, and correct it wherever it survives.

Unique Notes are identified by the `type` property, **not by folder**. There is no `Daily Notes/` folder. They live wherever they belong:

- `Other/Unique Notes/` — general
- `_ Dojo/Personal Practice/Shinsei/Unique Notes/`
- `_ Dojo/Personal Practice/Kokoro/Unique Notes/`
- `Other/Japan/Unique Notes/`

So never query them by folder path. Query the property, and a note stays findable wherever it moves:

```javascript
dv.pages()
  .where(p => !p.file.path.includes("99 templates")
           && p.type === "unique"
           && p.date)
```

The `99 templates` exclusion matters — a bare `dv.pages()` otherwise returns the template itself. The vault-wide view is [[_Unique Notes Timeline]].

---

## Unique Notes

`<folder>/Unique Notes/YYYY-MM-DD-HHMM-title.md`
_(No HHMM if not in the source filename. A bare `YYYY-MM-DD.md` is also valid.)_

```yaml
---
date: YYYY-MM-DD
last_updated: YYYY-MM-DD
type: unique
published: false
private: false
AI: false
AI_role:
AI_source:
description:
tags:
compiled: false
integrated: false
---
```

A note written as a day's log may also carry the tracking fields, placed after `private`:

```yaml
mood:
energy:
wake_up:
bed_time:
morning_meditation: false
physical: false
HN: false
RMK: false
CNCPT: false
AN: false
```

These are optional. Topic notes omit them; the morning note keeps them. The live template is `Other/99 templates/Daily/Daily_Note.md`.

---

## All Other Notes

Any note that is not a Unique Note.

```yaml
---
date: YYYY-MM-DD
last_updated: YYYY-MM-DD
rating: 0
status: draft
type: 
published: false
private: false
AI: false
AI_role:
AI_source:
description:
tags:
---
```

---

## Values

**Status:** `draft` · `editing` · `review` · `complete`
**Type:** `unique` (Unique Notes) · `artwork` (catalogue records) · `research` · `essay` · `reference` · `concept` · `log` · (blank if untyped)
**Rating:** 0 (unrated) to 10
**AI:** `true` only when content is primarily AI-generated
**AI\_role:** free text describing what Claude/AI actually did — e.g. `transcription`, `tagging and descriptions`, `co-writing`, `full draft`, `formatting only`. Leave blank if `AI: false`.
**AI\_source:** the attribution line — `Claude, Anthropic, <model>, conversation with author, <day month year>`. Leave blank if `AI: false`.

---

## Notes

- `published: true` — when the note is live on the site
- `private: true` — personal notes not for publication
- `AI: true` — the reference to Claude lives in the properties only (`AI_role`, `AI_source`). No attribution line, footnote, "AI Source" section or "Claude's framing" in the body, captions or diagrams.
- `AI_role` — sits directly under `AI:`. Describes the actual contribution, so the AI property carries more than a bare true/false.
- `AI_source` — sits directly under `AI_role`. The full attribution line.
- `rating` and `status` — never on Unique Notes
- `type` — always present on every note
- `compiled` / `integrated` — Unique Notes only
- `type: artwork` — catalogue records carry an extra identification, creation, physical, status and rights block. The field set and its conventions are in [[Artwork Cataloguing]]; the live template is `Other/99 templates/Artwork_template.md`.
