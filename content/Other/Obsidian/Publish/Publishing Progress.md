---
publish: true
permalink: /Other/Obsidian/Publish/Publishing Progress.md
title: Publishing Progress
description: Running log of publishing platform decisions and vault preparation work
draft: true
created: 2026-09-28
modified: 2026-10-06T05:52:34.973Z
published: 2026-09-28
tags:
  - publishing
  - quartz
  - obsidian
  - progress
---

# Publishing Progress

A running record of decisions made and work completed toward publishing the Yoso Synch vault as a public knowledge base.

---

## Platform Decision

After exploring multiple options, the current direction is **Quartz v5** hosted on **Cloudflare Pages**.

### Options Considered

| Platform | Status | Reason |
|---|---|---|
| Obsidian Publish | Considered | No RSS, \$96/yr, seamless mobile |
| Quartz + Memberstack | Considered | Membership now "maybe one day" |
| Ghost | Considered | Breaks vault-native workflow |
| Squarespace | Ruled out | No Obsidian integration |
| Quartz (free) | **Current direction** | Free, RSS, full control, vault-native |

### Key Factors

- **Flow** — writing stays in Obsidian, publishing via YAML flag (`publish: true`)
- **RSS** — essential for building a loyal readership
- **Free** — Cloudflare Pages + GitHub = zero ongoing cost
- **Knowledge base feel** — graph view, backlinks, wikilinks all native
- **Mobile** — occasional; Working Copy app on iOS as workaround
- **Membership** — "maybe one day"; can switch to Quartz + Memberstack later
- **Mailing list** — Buttondown planned (free up to 100 subscribers)

---

## Vault Preparation — Completed

### Foundation Files

| File | Purpose |
|---|---|
| `index.md` | Homepage — welcome + full vault index |
| `Colophon.md` | Who tends this space, contact, disclaimer |

### Past Projects — Yopunk\* Archive

15 notes created under `Projects/Past Projects/`:

- C.O.D.E.X · Glitch Punk · Yo Punk 2.0
- Aum — Home · Synth3sis · Neotopia
- Dreams & Conflicts · Home — AUM
- We Want Your Soul · Rupture
- China Power Off · Acid Mario
- Tamasii · Sueño · The Lure of Stuff
- Past Projects Index

Each note includes full YAML, project description, images linked from WordPress, internal wikilinks.

Source: [yopunk833100184.wordpress.com](https://yopunk833100184.wordpress.com)

### YAML Standardisation

Two scripts written to vault root:

**`set_draft_true.py`** — sets `draft: true` vault-wide. Run and confirmed.

**`add_missing_props.py`** — adds missing YAML properties by note type:

- Daily Notes → full daily schema
- Unique Notes → standard schema
- Nodes/everything else → node schema

### Index (`index.md`)

Lists all vault notes organised by theme:

- The Dojo · Kokoro · Reiki · Seasonal · Haiku · Japan · Yosokuro
- Projects (including Past Projects) · AI · Nodes (9 sub-themes)
- Profile · Network · Sources · Daily Notes · Unique Notes

---

## Next Steps

- [ ] Run `add_missing_props.py` across vault
- [ ] `node --version && git --version` — confirm environment
- [ ] Clone Quartz v5 locally
- [ ] Configure vault path + `publish: true` filter
- [ ] Run `npx quartz build --serve` — preview locally
- [ ] Push to GitHub
- [ ] Connect Cloudflare Pages (auto-deploy on push)
- [ ] Adapt `publish.css` for Quartz
- [ ] Set up Buttondown mailing list
- [ ] Decide on custom domain
- [ ] Select first notes to publish

---

## Content Strategy

- Knowledge freely available — no paywall
- Paid offerings (courses, workshops, prints) link out to Squarespace/external
- Model: open knowledge → audience → paid work
- Influences: Gwern (gwern.net), Andy Matuschak (notes.andymatuschak.org)

---

_See also: [[GitHub and Publishing Ethics]]_
