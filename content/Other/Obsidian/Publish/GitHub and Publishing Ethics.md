---
publish: true
permalink: /Other/Obsidian/Publish/GitHub and Publishing Ethics.md
title: GitHub and Publishing Ethics
description: Ethical considerations and practical guidelines for using GitHub and publishing vault content publicly
draft: true
created: 2026-09-28
modified: 2026-10-06T05:52:34.973Z
published: 2026-09-28
tags:
  - github
  - ethics
  - publishing
  - open-source
  - licensing
---

# GitHub and Publishing Ethics

Practical and ethical considerations for publishing the Yoso Synch vault via Quartz on GitHub and Cloudflare Pages.

---

## GitHub — What It Is and What It Means

GitHub is a platform for hosting code and content using Git version control. When you push your Quartz site to GitHub:

- Your **published notes** (those with `publish: true`) become part of the repository
- The repository can be **public** (anyone can see the source) or **private** (only you)
- Every change is tracked with a timestamp and commit message — a permanent record

### Public vs Private Repository

| | Public repo | Private repo |
|---|---|---|
| Source visible | Yes — anyone can read raw markdown | No |
| Site still public | Yes — Cloudflare serves it either way | Yes |
| Cost | Free | Free (GitHub allows private repos) |
| Recommendation | **Private** — keeps vault source contained | |

**Recommendation: use a private repository.** Your site is public; your source doesn't need to be. This protects notes you accidentally leave in the build, personal details in YAML, and draft content.

---

## Content Ethics

### Your Own Writing

Everything you write is yours. Publishing it openly under your name is a statement of authorship. Be consistent — don't publish anonymously and under your name simultaneously for the same work.

### Quoting and Citing Others

When your notes quote teachers, books, or sources:

- **Always attribute** — include the author, title, and where possible a link
- **Paraphrase generously** — direct quotes should be brief and clearly marked
- **Don't reproduce substantial portions** of copyrighted works even in a personal knowledge base made public
- Teachers whose words you carry — Rinpoche, Uchiyama, Nagai — deserve named attribution every time

### AI-Generated Content

Your vault uses the `AI: true` property to flag AI-assisted notes. On the public site:

- **Disclose AI involvement** — either in the note itself or in your Colophon
- A simple line is enough: _"Some notes in this space were drafted or expanded with AI assistance."_
- This is increasingly standard practice and builds trust rather than undermining it

### Other People's Images

The Past Projects notes link to images hosted on your own WordPress — this is fine. For any future notes embedding external images:

- Link to images you own or have rights to
- Don't hotlink images from other people's sites without permission
- Prefer uploading to your own hosting (99 Files folder → Cloudflare)

### Personal Information

Before publishing any note, check it doesn't contain:

- Other people's names in contexts they wouldn't expect to be public
- Private correspondence
- Location data or personal details about others
- Financial or medical information

Your `draft: true` vault-wide setting is your safety net — nothing publishes unless you explicitly set `publish: true`.

---

## Licensing Your Work

When you publish without a licence, all rights are reserved by default — technically no one can share or reuse your work. For a knowledge base built on the principle that knowledge should be free, consider:

### Recommended: Creative Commons

**CC BY-NC 4.0** — Attribution, Non-Commercial

- Anyone can share and adapt your work
- Must credit you (Yoso)
- Cannot use it commercially
- Aligns with your values — free knowledge, protected from commercial exploitation

Add to your Colophon:

```
© Yoso. Content licensed under CC BY-NC 4.0 unless otherwise noted.
```

---

## Quartz-Specific Considerations

Quartz itself is MIT licensed — you can use it freely, modify it, and don't need to open-source your own content because of it.

Your `quartz.config.ts` will contain your vault path and configuration — keep this in your **private** repository.

If you ever customise Quartz's source code significantly, consider contributing improvements back upstream — this is good open-source citizenship.

---

## Summary Checklist Before Going Live

- [ ] Repository set to **private**
- [ ] `draft: true` on all notes not intended for publication
- [ ] AI disclosure added to Colophon
- [ ] Licence statement added to Colophon (CC BY-NC 4.0 recommended)
- [ ] All quotes attributed with author and source
- [ ] No third-party images hotlinked without permission
- [ ] No private information about other people in published notes
- [ ] `publish: true` set only on notes you have reviewed

---

_See also: [[Publishing Progress]] · [[Colophon]]_
