---
publish: true
permalink: /Other/Nodes/Copyright and PDF Process.md
description: Working notes on copyright, Creative Commons licensing (under review), and a non-destructive process for adding metadata to PDFs.
created: 2026-05-31
modified: 2026-10-06T05:52:34.244Z
published: 2026-05-31
tags:
  - copyright
  - license
  - process
  - pdf
---

[[Other/Obsidian/License]] | [[Copyright]] | [[Other/Nodes/Colophon]]

# Copyright and PDF Process

_Working notes. The license is **not yet settled** — see "Decision pending" below. Nothing here is committed until reviewed before publishing._

---

## Where things stand

- An existing [[Other/Obsidian/License]] note already states **CC BY-NC-SA 4.0** for work on one.yoso.one.
- An older [[Copyright]] note says "All rights reserved, Yoso Tattoo 2009–2024."
- These two **contradict each other** — one reserves all rights, the other grants broad reuse. This needs resolving before publishing.
- The [[Other/Nodes/Colophon]] gestures at "offered freely" and marks AI-assisted notes with `AI: true`.

The point of this note: hold the thinking in one place, and document a safe PDF process — _without_ committing to anything yet.

---

## Decision pending — which license

Creative Commons offers a spectrum from most open to most protective. For handwritten, spiritual, and artistic notes, the realistic candidates:

- **CC BY** — reuse and adapt, even commercially, **with credit**. Most permissive.
- **CC BY-NC** — reuse with credit, **non-commercial only**.
- **CC BY-NC-SA** _(current draft choice)_ — credit + non-commercial + **share-alike** (derivatives carry the same license). The "copyleft" option.
- **CC BY-NC-ND** — credit + non-commercial + **no derivatives** (shared whole, not remixed). Most protective while still shareable.
- **All rights reserved** — the older Copyright note's stance; maximal control, no granted reuse.

### The tension to resolve

- **SA (share-alike)** invites others to _build on_ the work, as long as they pass the freedom forward. Good if the aim is a living, growing commons.
- **ND (no derivatives)** lets the work _circulate_ but stay intact. Good for finished writing or art that shouldn't be altered, remixed, or taken out of context.

For handwritten notes that are personal and contemplative, **ND** protects their integrity; **SA** treats them as seeds for others. This is a values choice, not a technical one — worth sitting with before publishing.

### A possible middle path

Different licenses for different material:

- **Finished essays / artworks** → BY-NC-ND (circulate, don't alter)
- **Notes / concepts meant as seeds** → BY-NC-SA (build on, pass forward)
- **Source material by others** (Hirst press kit, academic PDFs, etc.) → **no license applied** — not mine to license.

---

## Two layers of marking

1. **Metadata (invisible)** — fields embedded in the PDF file: Author, Title, Subject, Keywords, and a Rights/Copyright string. Shows in Get Info, Adobe, document properties. Travels with the file. **Changes no pixels.** Safe for any PDF that is genuinely mine.
2. **Visible mark (optional, later)** — a faint footer or corner line ("© Yoso · yoso.one · CC BY-NC-SA 4.0") stamped on each page. More committal; decide license first.

Start with metadata only. Add visible marks later, if at all.

---

## PDF metadata process (safe, non-destructive)

**Principles**

- **Never overwrite originals.** Write stamped copies to a separate output folder; review; only then replace.
- **Only stamp PDFs that are mine.** Skip source material authored by others.
- **One folder at a time.** Review a small batch before running vault-wide.

**What gets written**

- `Author`: Yoso
- `Title`: (kept from existing, or filename)
- `Subject`: (optional — short description)
- A custom **Rights/Copyright** field, e.g.
  `© Yoso, yoso.one — licensed CC BY-NC-SA 4.0` _(or whichever license is chosen)_

**Tooling**

- Python with **`pypdf`** (read/write PDF metadata) — lightweight, no rendering.
- Install once: `pip3 install pypdf --break-system-packages`
- A script walks the chosen folder, reads each PDF, sets the metadata fields, writes to `…/_stamped/` copies.
- Originals stay untouched until manually swapped in.

**Important caveats**

- PDF tools can't reach the vault from Claude's side — the script runs **locally in Terminal**, same pattern as the property scripts.
- Some PDFs are scans or have quirks; `pypdf` preserves content but always **spot-check** a few stamped copies before trusting the batch.
- Metadata is easily stripped by others — it is provenance, not protection. It records intent; it does not enforce it.

**Which PDFs are mine** _(to confirm before any run)_

- Likely mine: `Shinsei_Notes_Log.pdf`, `108 pearls.pdf`, `the white snake.pdf`, consciousness appendices, etc.
- **Not mine — do not stamp:** `DAMIEN-HIRST_PRESS-KIT_EN.pdf`, `akira-HN.pdf`, and any other third-party document.
- A full list should be reviewed by hand before the first run.

---

## Open questions to settle before publishing

1. Resolve the **Copyright vs License contradiction** (all-rights-reserved vs CC).
2. Choose **one license**, or the **per-material split** above.
3. Decide **metadata only**, or metadata **plus** a visible page mark.
4. Confirm the **list of PDFs that are genuinely mine**.
5. Decide whether the license also belongs in note **frontmatter** (a `license:` property), not just in PDFs — so it travels with the markdown too.

_Revisit this note when ready. Commit to nothing until reviewed._
