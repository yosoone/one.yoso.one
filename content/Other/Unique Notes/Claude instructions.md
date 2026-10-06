---
publish: true
permalink: /Other/Unique Notes/Claude instructions.md
created: 2026-05-29
modified: 2026-10-06T05:52:34.897Z
published: 2026-05-29
---

Here are your full workflow instructions to copy and paste into the new chat:

---

These are my workflow instructions, please follow them exactly:

# REMARKABLE → OBSIDIAN WORKFLOW

## PROCESS

1. Upload PDF in chat
2. Claude reads creation time from PDF metadata (UTC → JST)
3. Claude transcribes handwriting
4. Hashtags found in handwriting → added to tags in YAML, never overwrite existing tags
5. Sketches/drawings → cropped as JPG, embedded in MD
6. Claude writes a one-line description from content → added to description in YAML
7. If previous day has unresolved description → summarise all its unique notes and update it
8. When creating a Unique Note, always check if daily note exists — create it if not
9. Always check Unique Notes folder before answering anything about latest notes (phone may have created notes independently)
10. Always update daily note description when adding/updating any note for that day
11. Next day — update previous day's daily note description as full summary of all its unique notes
12. When loading a meditation note, always set morning\_meditation: true in the daily note
13. Always fill in missing descriptions when touching any note

## PDF TYPES

**TYPE 1 — DAILY NOTE:** YYMMDD.pdf (e.g. 260528.pdf)

- MD: YYYY-MM-DD.md → Daily Notes/ (auto)
- If MD exists → preserve all properties, only set RMK: true, add missing properties, append ### RMK section
- If MD does not exist → create with full template

**TYPE 2 — UNIQUE NOTE:** YYMMDD-title.pdf (e.g. 260528-tingling-sensations.pdf)

- Renamed using PDF creation time: YYMMDD-HHMM-title.pdf
- MD: YYYY-MM-DD-HHMM-title.md → Daily Notes/Unique Notes/ (auto)
- Always check if daily note exists — create it if not
- Auto-appears in daily note ## Unique Notes via dataviewjs

**TYPE 3 — MEDITATION NOTE:** voice recording + optional transcript/handwritten notes

- Filename uses audio file time (HHMM), not transcription time
- Format: YYYY-MM-DD-HHMM-meditation-\[timeofday]-\[topic].md
- Time of day: 0400-1159 → morning, 1200-1659 → afternoon, 1700-2359 → evening
- Topic extracted from content if clear, otherwise omitted
- Always set morning\_meditation: true in daily note
- Audio embed: ![[YYMMDD-HHMM-title.m4a]] at top
- ## Transcript header before transcription content
- tags: \[meditation]

## MD STRUCTURE — DAILY NOTE (from 2026-05-28 onwards)

YAML properties: date, mood, energy, wake\_up, bed\_time, morning\_meditation, physical, HN, RMK, CNCPT, AN, compiled, integrated, description, tags

Content:

```
## Unique Notes  (dataviewjs — lists all unique notes for the day with descriptions)
### RMK          (only if RMK PDF uploaded)
  ![[YYMMDD.pdf]]
  transcription
  ![[YYYY-MM-DD_sketch.jpg]]  (if sketch found)
```

Note: No section headers (First Thoughts etc.) from 2026-05-28 onwards. Existing notes before that date keep their original structure.

## MD STRUCTURE — UNIQUE NOTE

YAML properties: date, tags, description, compiled, integrated, AI

Content:

```
[[YYYY-MM-DD]] | [[Topic]]   (backlink to daily note + topic if hashtag present)
![[YYMMDD-HHMM-title.pdf]]   (if PDF type)
![[YYMMDD-HHMM-title.m4a]]   (if meditation type)
## Transcript                 (if meditation type)
transcription content
```

## FILE NAMING

| Type | Format |
|------|--------|
| Daily MD | YYYY-MM-DD.md |
| Unique MD | YYYY-MM-DD-HHMM.md or YYYY-MM-DD-HHMM-title.md |
| Daily PDF | YYMMDD.pdf |
| Unique PDF | YYMMDD-HHMM-title.pdf |
| JPG | YYYY-MM-DD\_sketch.jpg |
| Audio | YYMMDD-HHMM-title.m4a |

## OUTPUT FOLDERS

| Type | Folder |
|------|--------|
| Daily MD | Daily Notes/ (auto) |
| Unique MD | Daily Notes/Unique Notes/ (auto) |
| PDF | 99 Files/Daily Notes PDF/ (manual) |
| JPG | 99 Files/Daily Notes PDF/IMG/ (manual) |
| Audio | 99 AUDIO/meditations audio/ (manual) |

## TEMPLATES

- Daily Note: 99 templates/Daily/Daily\_Note.md
- Unique Note: 99 templates/Daily/Unique Daily/Unique Daily.md

## HASHTAG → TOPIC NOTE RULE

When a unique note contains a hashtag (e.g. #SHINSEI):

1. Find or create `TopicName.md` in the appropriate topic folder (e.g. Shinsei/Shinsei.md)
2. Add link under ## Related Unique Notes: `[[YYYY-MM-DD-HHMM-title]] — description`
3. Add backlink in unique note: `[[YYYY-MM-DD]] | [[TopicName]]`
4. If filename contains topic name (e.g. "shinsei"), auto-add the tag and link
5. Topic names always uppercase where applicable (e.g. SHINSEI → Shinsei.md)

## DASHBOARD

File: Daily Notes/dashboard\_dailynotes.md
Shows all daily notes with all properties
Booleans: true = ✅  false = ⬜
Sorted by date descending

## END OF PROCESS

- Present JPG download (if any)
- Show IMG folder path: `/Users/yoso/Library/Mobile Documents/iCloud~md~obsidian/Documents/Yoso Synch/99 Files/Daily Notes PDF/IMG/`
- PDF is manual, no folder link shown

## RULES

- Never overwrite existing YAML properties except RMK (set to true) and morning\_meditation (set to true for meditations)
- Always add missing properties when updating existing notes
- Tags: extract from handwritten hashtags, add to YAML tags list, never overwrite
- Description (unique note): Claude writes one line from content, always filled
- Description (daily note): updated every time a note is added/updated for that day; full summary written the next day
- JPG: always named YYYY-MM-DD\_sketch.jpg, always presented for manual download
- PDF creation time: always read and convert UTC → JST for filename
- Always list Unique Notes folder before answering questions about latest notes
- Unique notes do not have a draft property
- All new notes follow the Style Guide: [[Style Guide Claude]]

## VAULT PATH

/Users/yoso/Library/Mobile Documents/iCloud~md~obsidian/Documents/Yoso Synch/
