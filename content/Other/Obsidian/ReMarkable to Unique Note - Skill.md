---
publish: true
permalink: /Other/Obsidian/ReMarkable to Unique Note - Skill.md
description: Claude skill for processing reMarkable PDFs into Obsidian Unique Notes — naming rules, properties, topic linking, sketch cropping.
created: 2026-09-09
modified: 2026-10-06T05:52:34.971Z
published: 2026-09-09
tags:
  - obsidian
  - skill
  - workflow
  - remarkable
---

[[Obsidian|Obsidian]] | [[Style Guide|Style Guide]] | [[Claude instructions|Claude Instructions]]

_Source: Claude, Anthropic, claude-sonnet-4-6, conversation with author, 9 September 2026._

# Skill: ReMarkable → Obsidian Unique Note

A Claude skill (`remarkable-unique-note`) that processes a reMarkable PDF upload into a correctly structured Obsidian Unique Note in Yoso's vault.

The `.skill` file can be installed from the Style folder or downloaded from the chat session where it was created.

---

## Vault Path

```
/Users/yoso/Library/Mobile Documents/iCloud~md~obsidian/Documents/Yoso Synch/
```

---

## Step 1 — Read PDF

1. Run `pdfinfo` to get creation time (UTC)
2. Rasterize with `pdftoppm -jpeg -r 150` for handwriting transcription
3. If sketches or diagrams are present, crop as JPG using PIL

---

## Step 2 — Determine Filename

**Date:** always from the uploaded filename (e.g. `260909` = 2026-09-09). Never trust PDF metadata for date.

**Time:** use HHMM from filename if present (e.g. `260909-0900-freedom.pdf` → `0900`). If no time in filename, omit HHMM entirely.

**MD filename format:**

- With time: `YYYY-MM-DD-HHMM-title.md`
- Without time: `YYYY-MM-DD-title.md`

**PDF rename format:**

- With time: `YYMMDD-HHMM-title.pdf`
- Without time: `YYMMDD-title.pdf`

---

## Step 3 — Transcribe

- Transcribe all handwriting accurately
- Identify hashtags (e.g. `#SHINSEI`) → add to YAML tags, always UPPERCASE
- Identify sketches/diagrams → crop as JPG named `YYYY-MM-DD_sketch.jpg`

---

## Step 4 — Create Unique Note

**Output folder** — by topic, not a single inbox:

| Case | Note goes to | PDF goes to |
|---|---|---|
| Tagged `#SHINSEI` | `_ Dojo/Personal Practice/Shinsei/Unique Notes/` | `…/shinsei-unique-notes-pdf/` |
| Tagged `#KOKORO` | `_ Dojo/Personal Practice/Kokoro/Unique Notes/` | `…/kokoro-unique-notes-pdf/` |
| Tagged `#JAPAN` | `Other/Japan/Unique Notes/` | `…/japan-unique-notes-pdf/` |
| No topic tag | `Other/Unique Notes/` | `Other/99 Files/Daily Notes PDF/` |

_(“Daily Notes PDF” is a legacy folder name — it is just the general PDF store.)_

**Standard properties** — see [[Note Properties Reference]]. `type: unique` is required; without it the note appears in no index.

```yaml
---
date: YYYY-MM-DD
last_updated: YYYY-MM-DD
type: unique
publish: false
private: false
AI: true
AI_role: transcription
description:
tags:
compiled: false
integrated: false
---
```

**Opening line:** `[[TopicName]]` — topic and index links only. There is no daily note to link to.

**Always embed:** `![[YYMMDD[-HHMM]-title.pdf]]`

**Embed sketch if cropped:** `![[YYYY-MM-DD_sketch.jpg]]`

---

## Step 5 — Update the topic index

Add the note to the topic's `_<Topic> Unique Notes Index.md` under `## Unique Notes`.

There is no daily note to create or update — Daily Notes are retired.

---

## Step 6 — Topic Note Linking

When hashtag or topic name in filename:

1. Add to topic index under `## Related Unique Notes`
2. Add backlink in unique note opening line
3. If matching Node note exists, add bidirectional link there too

**Rules:**

- `#SHINSEI` → `[[Shinsei]]`
- Tags always UPPERCASE in YAML
- Topic names always capitalised

---

## Step 7 — Sketch JPG

Present for download → user moves it beside the note's PDF, in that topic's PDF folder.

---

## Step 8 — End of Process

```
✅ Unique Note: <topic>/Unique Notes/YYYY-MM-DD[-HHMM]-title.md
PDF → that topic's PDF folder (rename to YYMMDD[-HHMM]-title.pdf)
JPG → same folder (if sketch)
```

---

## Key Rules

- Never trust PDF metadata over filename for date/time
- Always embed the PDF — no exceptions
- No HHMM when not in filename
- Unique Notes: no `rating`, no `status`
- `AI: false` for handwritten notes
- Description always written by Claude, one line
- Bidirectional links always
