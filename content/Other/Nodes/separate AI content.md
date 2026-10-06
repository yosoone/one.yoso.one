---
publish: true
permalink: /Other/Nodes/separate AI content.md
created: 2026-05-29
modified: 2026-10-06T05:52:34.270Z
published: 2026-05-29
---

# Claude

i wils need to go through my entire vault and edit clean to separate the ai content yet keep it related to the topic, what would you recommend?

15:36

## Claude responded: Good question.

Good question. A few thoughts before recommending:

**The core problem** Your notes are a mix of your own thinking, quotes, and AI-generated content — often blended in the same file. Separating them while keeping the connection is the challenge.

**My recommendation: the `AI: true` note as a companion**

Rather than editing existing notes in place (risky, slow, loses context), create a companion note for each note that has significant AI content:

- `Shinsei - Essence.md` (AI: true) stays as is — pure AI synthesis
- `Shinsei.md` (AI: false) stays as your raw thinking
- The two are linked — your note links to the AI companion, the AI companion links back

You already have this pattern in the Shinsei folder. **Scale it vault-wide.**

**Practical workflow**

1. Use the `AI` property you just added as your triage filter — build a dataview query showing all `AI: false` notes so you can go through them one by one
2. For each note with mixed content: cut AI sections into a new companion note named `[Original] - AI.md`, set `AI: true`, link bidirectionally
3. For notes that are entirely AI: just flip to `AI: true`, no split needed
4. For your own writing with AI edits: keep as `AI: false` but add a comment like `<!-- AI edited -->` at the section level

**What I'd avoid** Doing this all at once. It's a vault-wide project — better as a slow, note-by-note practice where touching a note to read or update it triggers the clean-up.

**Simplest first step** Build the dataview query now, so you have a clean triage dashboard. Want me to write that?
