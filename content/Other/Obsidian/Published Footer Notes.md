---
publish: true
permalink: /Other/Obsidian/Published Footer Notes.md
description: Working notes on adding a site-wide footer (license, credit) to published notes — options, trade-offs, and a ready-to-use CSS draft. To review before publishing.
created: 2026-05-31
modified: 2026-10-06T05:52:34.967Z
published: 2026-05-31
tags:
  - legal
  - license
  - footer
  - publish
  - process
---

[[Other/Obsidian/License]] | [[Copyright]] | [[Copyright and PDF Process]] | [[Footer]]

# Published Footer — Notes

_Working notes on putting a footer (license + credit) on every published note. **Nothing committed** — review before publishing. Tied to the license decision still pending in [[Copyright and PDF Process]]._

---

## The goal

A consistent footer on every **published** page — license, credit, maybe a link back — without cluttering the working vault or editing notes one by one.

Key principle: **the footer belongs to the published layer, not the notes.** Stamping a footer into all ~6000 markdown files would clutter the vault, risk inconsistency, and be painful to change. Far better to inject it once at publish time. Notes stay clean; the footer shows only on the live site.

---

## What already exists

- [[Footer]] (in Nodes) already holds the **full CC BY-NC-SA 4.0 markup** — the official Creative Commons chooser HTML with the cc / by / nc / sa icon badges. Content is mostly done; it just needs to be _applied site-wide_ rather than living as a note.
- That same Footer note also has older campaign content (travel dates 2024, newsletter prompts, hashtags) mixed in — the license block is the reusable part; the rest is dated.

---

## Three ways to add it (Obsidian Publish)

### Option 1 — CSS footer via `publish.css` _(simplest)_

A CSS rule appends a footer to every published page automatically.

- **Pros:** one edit, applies everywhere, zero per-note work, easy to change, never touches the notes.
- **Cons:** pure CSS injects **text and symbols** cleanly but struggles with the CC **badge images**. Realistically this means a text-only line ("licensed CC BY-NC-SA 4.0" with a link), dropping the icon badges.
- **Best when:** clean text footer is enough.

### Option 2 — Publish's built-in footer setting _(keeps badges)_

Obsidian Publish has a site-wide footer field in its settings panel that can hold HTML.

- **Pros:** can carry the **full badge markup** from [[Footer]]; still site-wide and central.
- **Cons:** a little more setup; HTML lives in Publish settings rather than the vault.
- **Best when:** the CC icon badges matter visually.

### Option 3 — Embedded footer note _(most flexible, most work)_

A single published note embedded at the foot of others.

- **Pros:** edit the footer as a normal note.
- **Cons:** embedding sitewide is fiddly; not worth it versus 1 or 2.

---

## Recommendation

Start with **Option 1 (CSS text footer)** for simplicity and zero maintenance. Move to **Option 2** later if the icon badges are wanted. Keep the rich badge version in [[Footer]] as the source for Option 2.

---

## Ready-to-use CSS draft (Option 1)

_To paste into `publish.css` when publishing — left here, not applied. Adjust the license once decided._

```css
/* Site-wide footer on every published page */
.published-container .markdown-preview-section::after {
  content: "© Yoso · yoso.one · Licensed under CC BY-NC-SA 4.0";
  display: block;
  margin-top: 4rem;
  padding-top: 1.5rem;
  border-top: 1px solid var(--background-modifier-border, #ddd);
  font-size: 0.8rem;
  opacity: 0.6;
  text-align: center;
}
```

Notes on the draft:

- The exact selector (`.published-container .markdown-preview-section`) should be **verified against the live Publish DOM** before trusting it — Publish's class names change between versions.
- CSS `content:` cannot hold a clickable link. For a real link to the license, use Option 2.
- Update the license string the moment the license is settled (see [[Copyright and PDF Process]]).

---

## Open questions (review before publishing)

1. **Which license** does the footer state? — pending in [[Copyright and PDF Process]]. The footer must match whatever is finally chosen (and must not contradict [[Copyright]]).
2. **Text footer or badge footer?** — decides Option 1 vs 2.
3. **What does it link to?** — the CC license page, a `/license` page, the [[Colophon]], or nothing.
4. **Per-material licensing?** — if finished work and seed-notes get _different_ licenses, a single sitewide footer can't express that; would need per-note frontmatter (`license:`) plus conditional display.
5. **Tidy [[Footer]]** — separate the reusable license block from the dated 2024 campaign content.

_Revisit alongside [[Copyright and PDF Process]] when preparing to publish._
