---
publish: true
permalink: /Other/Obsidian/Publish/Site Footer.md
title: Site Footer
description: Site-wide footer for the published knowledge base — licence, credit, links. CSS and HTML versions for Quartz.
draft: true
created: 2026-09-28
modified: 2026-10-06T05:52:34.972Z
published: 2026-09-28
tags:
  - footer
  - license
  - publishing
  - quartz
  - CSS
---

# Site Footer

Site-wide footer for the published knowledge base. Applied once at the theme level — never stamped into individual notes.

---

## Content

```
© Yoso · Licensed under CC BY-NC-SA 4.0 · Colophon
```

Three elements:

- **Credit** — © Yoso
- **Licence** — CC BY-NC-SA 4.0 → links to creativecommons.org
- **Colophon** — links to `/Colophon`

---

## For Quartz — HTML Component

Quartz v5 uses a component system. The footer goes in `quartz/components/Footer.tsx` (or a custom component added to the layout in `quartz.layout.ts`).

Place this in your Quartz layout as the page footer:

```html
<footer class="yoso-footer">
  <hr />
  <p>
    © Yoso &nbsp;·&nbsp;
    <a href="https://creativecommons.org/licenses/by-nc-sa/4.0/" target="_blank" rel="license noopener noreferrer">
      CC BY-NC-SA 4.0
      <img src="https://mirrors.creativecommons.org/presskit/icons/cc.svg" alt="CC" />
      <img src="https://mirrors.creativecommons.org/presskit/icons/by.svg" alt="BY" />
      <img src="https://mirrors.creativecommons.org/presskit/icons/nc.svg" alt="NC" />
      <img src="https://mirrors.creativecommons.org/presskit/icons/sa.svg" alt="SA" />
    </a>
    &nbsp;·&nbsp;
    <a href="/Colophon">Colophon</a>
  </p>
</footer>
```

---

## For Quartz — CSS

Add to `quartz/styles/custom.scss` (or your custom CSS file):

```css
.yoso-footer {
  margin-top: 4rem;
  padding-top: 1.5rem;
  border-top: 1px solid var(--lightgray);
  font-size: 0.8rem;
  opacity: 0.65;
  text-align: center;
}

.yoso-footer img {
  height: 18px;
  margin-left: 3px;
  vertical-align: text-bottom;
  opacity: 0.7;
}

.yoso-footer a {
  color: inherit;
  text-decoration: none;
}

.yoso-footer a:hover {
  opacity: 1;
  text-decoration: underline;
}
```

---

## For Obsidian Publish — CSS only (text version)

If switching to Obsidian Publish, paste into `publish.css`:

```css
.markdown-preview-section::after {
  content: "© Yoso · CC BY-NC-SA 4.0 · yoso.one";
  display: block;
  margin-top: 4rem;
  padding-top: 1.5rem;
  border-top: 1px solid var(--background-modifier-border);
  font-size: 0.8rem;
  opacity: 0.6;
  text-align: center;
}
```

Note: CSS `content:` cannot render images or clickable links — text only for Publish.

---

## Licence Text (for Colophon)

Add this line to [[Colophon]]:

> Content on this site is licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) — share freely, credit Yoso, non-commercial, same licence.

---

## Open Questions

- [ ] Confirm domain for the © line (yoso.one, or other?)
- [ ] Add "Subscribe" link to footer once Buttondown is set up
- [ ] Verify Quartz selector once running locally

---

_See also: [[Footer]] · [[Colophon]] · [[Publishing Progress]] · [[GitHub and Publishing Ethics]]_
