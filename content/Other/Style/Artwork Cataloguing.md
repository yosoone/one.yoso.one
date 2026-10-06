---
publish: true
permalink: /Other/Style/Artwork Cataloguing.md
aliases:
  - Artwork Cataloguing
  - Tombstone
description: Cataloguing conventions for artwork records — the tombstone label, accession numbering, how to write dimensions, media, dates and durations, time-based works and their display specifications, and which museum standards the fields come from.
created: 2026-09-16
modified: 2026-10-06T05:52:34.850Z
published: 2026-09-16
tags:
  - style
  - artwork
  - reference
---

[[Style Guide]] | [[Note Properties Reference]] | [[Artwork Catalogue - Best Practice]] | [[Artwork_template]]

# Artwork Cataloguing — Conventions

> **Scope.** This note is the _house rules_: exactly how to write a dimension, an accession number, a medium line. For the reasoning behind them — the standards, the principles, the references — see [[Artwork Catalogue - Best Practice]].

Rules for filling in [[Artwork_template]]. The field set follows the museum standards below; the house conventions are the choices made where those standards allow several.

---

## 1. Which standard, and why

Four standards govern art cataloguing, and they nest.

**CDWA** — _Categories for the Description of Works of Art_, maintained by the Getty Vocabulary Program — is the foundational document. It runs to around 540 categories and subcategories, of which a small subset is marked **core**: the minimum needed to identify and describe a work unambiguously.[^1] The template uses the core subset and ignores the rest.

**CCO** — _Cataloging Cultural Objects_ — is the content standard built on CDWA and VRA Core: it governs how to _format_ what goes in each field, where CDWA governs which fields exist.[^2]

**Object ID** is the minimum-viable standard, developed by the Getty and now administered by ICOM in collaboration with police, customs, the art trade and insurers. It defines nine categories and is the checklist to satisfy if a work is ever lost or stolen.[^3] Its nine: type of object, materials and techniques, measurements, inscriptions and markings, distinguishing features, title, subject, date or period, maker — plus photographs and a short description.[^4]

**VRA Core** is the visual-resources equivalent, useful mainly for the distinction it enforces between the _work_ and an _image of_ the work.[^2]

**House position.** Fill the Object ID nine on every work without exception — that is the insurance and recovery floor. Fill the wider CDWA core where it applies. Everything below that is optional and can wait.

---

## 2. The tombstone

The wall label. Galleries print it in a fixed order and so does the vault:

```
Artist
Title, date
Medium
Dimensions
Credit line / accession number
```

Conventions:

- **Title in italics.** Japanese title in angle brackets after it, on first appearance: _Rainbow_ 〈虹〉.
- **Untitled** is not italicised, and takes a bracketed qualifier where one helps: Untitled _(Waterfall series)_.
- **Date** is the year of completion. A range for works made over time: 2024–2026. Uncertain dates take `ca.` — not `c.`, not `circa`.
- **Medium before dimensions**, always.
- **Credit line** is where a museum names the donor. For your own work it carries the accession number, and after sale the collection: _Private collection, Tokyo_.

For a time-based work the medium line carries the format and the duration, and the dimensions line usually reads `dimensions variable`:

> **Yoso**
> _The Lure of Stuff_, 2005
> single-channel video and sound installation, 12 min 30 sec
> dimensions variable
> 2005-INS-003

---

## 3. Accession numbers

Museums number by year, source, and sequence. The vault's form:

```
YEAR-SERIES-NNN
2026-SHI-014
```

Series codes: `SHI` Shinsei · `YOS` Yosokuro · `INS` installation · `MIS` uncategorised.

Numbers run within the year, never reused, never renumbered after a work is destroyed or lost — the record survives the object. Editions take the accession of the work plus the edition fraction; they are not separately accessioned.

---

## 4. Dimensions

**Height before width before depth**, centimetres, one decimal place. Inches in parentheses only if the record is going somewhere that needs them.

```
dimensions: 45.5 × 33.0 cm
dimensions: 180.0 × 90.0 × 4.5 cm
```

**Scrolls take two measurements.** The image (本紙 _honshi_) and the full mounted scroll, since the mount is a separate object made by a separate hand:

```
dimensions: 98.0 × 34.5 cm (image)
dimensions_mounted: 187.0 × 46.0 cm (full mount)
```

**Photographs take three**, potentially — image, sheet, and frame. Record image and sheet at minimum.

**Irregular works** take the greatest extent in each direction, noted as such: `42.0 × 38.0 cm (irregular)`.

**Sight dimensions** — what is visible inside a frame or mount — are recorded as `(sight)` and never confused with the sheet.

---

## 5. Medium

Describe materials then support, in that order, in ordinary words:

```
sumi ink on kozo paper
sumi ink and mineral pigment on silk, mounted as a hanging scroll
gelatin silver print
pigment print on Hahnemühle Photo Rag
single-channel video, colour, stereo sound
four-channel audio installation
```

Avoid the auction-catalogue abstractions — "mixed media" says nothing. If a work genuinely combines many materials, list the significant ones and close with "and other materials".

Japanese terms: romanise, italicise on first use with a gloss, then use freely — _kozo_ (paper mulberry), _sumi_ (ink stick).

---

## 6. Editions

Photographs and prints:

```
edition: 3/15          # third of fifteen
edition: AP 1/3        # artist's proof
edition: unique
```

Record the edition size at the point the edition is declared, and never increase it. If a work exists in more than one size, each size is a separate edition and a separate accession.

---

## 7. Signature and seal

Say _what_, _where_, and _how_:

```
signature: signed 'Yoso' in ink, lower left
seal: rakkan in vermilion, lower left below signature
```

For unsigned work say so — `signature: unsigned` — rather than leaving the field blank, which reads as unchecked rather than checked and negative.

---

## 8. Time-based works

Museums call anything with duration _time-based media_. Tate's definition covers film, slides, video, audio, performance and software — works that have "the dimension of time."[^5] Three things change when a work has duration.

### Duration is a dimension

Record it where a physical work records size. `HH:MM:SS`, or `MM:SS` under an hour. Generative or indeterminate works take `variable`, with the range noted if there is one. Installations take `dimensions variable` on the dimensions line and give real measurements in the display specification instead.

### The work is not the file

The work/image distinction VRA Core enforces applies here with more force, because carriers fail. A video work is not its ProRes file any more than a painting is its canvas — but unlike canvas, the file becomes unreadable. Record:

- `master_format` — what the archival master actually is
- the original carrier, where the work began on one
- every migration, dated, in the display specification

Migration is not a conservation failure to be hidden; it is the normal life of the work, and an undocumented migration is how a work quietly becomes a different work.

### The work exists only when installed

The Guggenheim's position is that a media artwork's behaviours and limits of variability can only be established on the occasion of its installation — how it responds to spatial constraints, what venue-specific realities do to it, what happens as equipment properties change.[^6] The display specification is therefore part of the work's identity, not documentation added afterwards.

Pip Laurenson, who built Tate's time-based media conservation practice, describes the goal as specifying a work "thickly": artists who set out their requirements in detail leave less to be improvised once they are no longer available to ask. Her caution is worth keeping in view — the installation will always be richer than the specification.[^7]

One judgement has to be made explicitly and recorded: **is the equipment work-defining?** A CRT monitor may be a neutral carrier in one work and constitutive in another, and the answer determines whether a future installer may substitute. Laurenson's argument is that this is case-specific and cannot be settled by a general rule — so settle it per work, in writing, while you can.[^8]

---

## 9. Photographs of the work

Object ID puts photography ahead of description, on the practical grounds that an object without an image is rarely recovered.[^3]

Minimum per work: one overall view, straight on, even light, colour target in frame if the work is colour-critical. Then details — signature, seal, any damage, any distinguishing feature. Verso for anything on paper.

File naming follows the accession:

```
2026-SHI-014_overall.jpg
2026-SHI-014_detail-seal.jpg
2026-SHI-014_verso.jpg
```

The image is not the work. Keep the distinction in the record — it is the one thing VRA Core exists to enforce.[^2]

---

## 10. What to leave empty

A blank field means _not yet checked_. A field filled with `unknown`, `none`, or `unsigned` means _checked, and this is the answer_. The difference matters when the record is used years later, so prefer the explicit negative to the silent blank wherever the question has actually been asked.

---

## Footnotes

[^1]: "[Introduction](https://www.getty.edu/research/publications/electronic_publications/cdwa/introduction.html)," _Categories for the Description of Works of Art_, Getty Research Institute, accessed 16 September 2026. CDWA is maintained by the Getty Vocabulary Program; the current version dates to 2016.
[^2]: "[The CDWA and Other Metadata Standards](https://www.getty.edu/publications/categories-description-works-art/other-metadata-standards/)," _Categories for the Description of Works of Art_, Getty Research Institute, accessed 16 September 2026, on the relationship between CDWA, CCO, VRA Core, CDWA Lite and LIDO.
[^3]: "[Object ID](https://icom.museum/en/resources/standards-guidelines/objectid/)," International Council of Museums, accessed 16 September 2026. ICOM signed an agreement with the J. Paul Getty Trust in October 2004 for worldwide use of the standard; the checklist exists in seventeen languages.
[^4]: Robin Thornes, _[Introduction to Object ID: Guidelines for Making Records That Describe Art, Antiques, and Antiquities](https://www.getty.edu/publications/virtuallibrary/0892365722.html)_ (Los Angeles: Getty Research Institute, 1999).
[^5]: "[Time-Based Media](https://www.tate.org.uk/about-us/conservation/time-based-media)," Tate, accessed 16 September 2026. Tate's collection of time-based media spans the 1960s to the present; the Time-Based Media Conservation team has been developing standards of care since the early 1990s.
[^6]: "[Time-Based Media](https://www.guggenheim.org/conservation/time-based-media)," Solomon R. Guggenheim Museum, accessed 16 September 2026: "since a media artwork exists only in its installed state, a deeper understanding of its behaviors and limits of variability can be established only on the occasion of its installation."
[^7]: Pip Laurenson, "[Authenticity, Change and Loss in the Conservation of Time-Based Media Installations](https://www.tate.org.uk/research/tate-papers/06/authenticity-change-and-loss-conservation-of-time-based-media-installations)," _Tate Papers_ 6 (2006).
[^8]: Pip Laurenson, "[The Management of Display Equipment in Time-Based Media Installations](https://www.tate.org.uk/research/tate-papers/03/the-management-of-display-equipment-in-time-based-media-installations)," _Tate Papers_ 3 (2005), arguing that the appropriate conservation approach depends on the significance of the display equipment to the particular installation, and is case-specific.

---

## Bibliography

Getty Research Institute. _Categories for the Description of Works of Art_. Los Angeles: J. Paul Getty Trust. https://www.getty.edu/publications/categories-description-works-art/.

International Council of Museums. "Object ID." https://icom.museum/en/resources/standards-guidelines/objectid/.

Laurenson, Pip. "Authenticity, Change and Loss in the Conservation of Time-Based Media Installations." _Tate Papers_ 6 (2006).

———. "The Management of Display Equipment in Time-Based Media Installations." _Tate Papers_ 3 (2005).

Solomon R. Guggenheim Museum. "Time-Based Media." https://www.guggenheim.org/conservation/time-based-media.

Tate. "Time-Based Media." https://www.tate.org.uk/about-us/conservation/time-based-media.

Thornes, Robin. _Introduction to Object ID: Guidelines for Making Records That Describe Art, Antiques, and Antiquities_. Los Angeles: Getty Research Institute, 1999.

Visual Resources Association. _VRA Core 4.0_. Library of Congress. https://www.loc.gov/standards/vracore/.

---

## Source

Claude, Anthropic, claude-opus-5, conversation with author, 16 September 2026.
