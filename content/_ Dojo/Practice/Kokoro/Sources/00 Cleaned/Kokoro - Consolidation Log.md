---
publish: true
permalink: /_ Dojo/Practice/Kokoro/Sources/00 Cleaned/Kokoro - Consolidation Log.md
description: Record of the Kokoro folder cleanup — which raw notes were merged into which cleaned notes, which duplicates were found, what was dropped and why, and what remains unverified
created: 2026-09-13
modified: 2026-10-06T05:52:35.085Z
published: 2026-09-13
tags:
  - kokoro
  - log
  - vault
---

[[_Kokoro]] | [[_Kokoro Index]] | [[Kokoro - Vault Map]]

# Kokoro — Consolidation Log

> **Status.** Non-destructive. Nothing in `Sources/01 Raw/` has been deleted, moved, or edited. The cleaned notes are new files in `Sources/00 Cleaned/`. This log records what went where so the raw layer can be retired safely when you are ready.
>
> **Excluded by request:** `Sources/_Unite in Kokoro, personal.md` was not read and is not reflected anywhere in the cleaned set.

---

## 1. The cleaned set

| Note | Covers |
|---|---|
| [[Kokoro - The Word and Its Range]] | Etymology, Sanskrit and Chinese inheritance, dictionary definitions, semantic range, the untranslatability debate, modern live uses, ordinary speech |
| [[Kokoro - Japanese Buddhism - Heart-Mind in Doctrine and Practice]] | Doctrinal history, Nara to Meiji — moved into `00 Cleaned` on 13 September 2026 after a source check; see §8 |
| [[Kokoro in Practice]] | _Mushin_, _makoto_, _hana_, gassho, honouring each cell, the _ki_–_kokoro_ bridge, coherence without fixity |
| This log | What merged, what was dropped, what needs checking |

**Keepers left in place.** These were already single-purpose and well sourced. They were not merged, only cross-linked:

- [[Kokoro - Cultivation - Merit and Energy]] — the cultivation essay
- [[Kokoro - Cultivation - Models]] — its two figures
- [[Kokoro - Soseki - Union Across Three Axes]] — the novel, seven critical threads
- [[Kokoro for a Liquid Reality]] — the Bauman–Nishida essay
- [[Unite in Kokoro - Essay]] — the contemplative essay
- [[Kokoro and Shraddha claude|Kokoro and Shraddha]] — comparative philology
- [[Imagining Union - Claude]] and [[A Drop Briefly - Union in Liquid Reality - Claude]] — reflections, kept as a distinct genre
- Unique Notes — both retained in `Unique Notes/`

---

## 2. Merged into [[Kokoro - The Word and Its Range]]

| Source note | What was taken | What was left behind |
|---|---|---|
| `Unite in Kokoro - 心.md` | Kōjien and Nihon kokugo daijiten definitions, collocation with _kanjiru_, English equivalents, _shinzō_ distinction, _kokoro no nōto_ | Three verbatim repetitions of the same section within the file; four repetitions of the same "Further reading" block; the "Other Draft" prose, which is Yoso's own writing and belongs with the personal essay |
| `Unite in Kokoro Draft Before review.md` | Švarcová's "mental space" gloss; _wa no kokoro_ / _Nihon no kokoro_ | Everything else duplicates the above |
| `Kokoro as Body, Heart, Mind -draft.md` | _kogori_/_kogoru_ etymology, _shinshin ichinyo_, _hara ga tatsu_, _kokoro o komeru_, Kyoto Kokoro Research Center | KOKORO scale statistics, Bushidō section, IBUKI android, Mark Divine / SEALFIT material — see §4 |
| `Kokoro in Japanese Thought...md` | _kotodama_, Watsuji's _aidagara_, Kyoto Kokoro Initiative, Kawai's open-to-closed shift, _kokorozashi_ | The "holographic principle" framing and the _kokutai_ / emperor / _genbun-itchi_ nation-building argument — see §4 |
| `Is Kokoro a Relevant Concept?.md` | The four-domain table; Nakaya, Sasaki, Benedict, Yamaguchi, Sherlock citations | The Consensus interface boilerplate; the long undifferentiated reference dump |
| `kokoro in daily life.md` | Nothing not already present elsewhere | See §3 and §4 |
| `kokoro in daily life 1.md` | Nothing — exact duplicate | See §3 |
| `kokoro in gratitude.md` | _kokoro kara_ / _kokoro yori_ constructions, the _hontō ni_ / _makoto ni_ contrast, _ojigi_, _omiyage_, _enryo_ | Pedagogical-implications sections; the invented Kansai slang example |
| `Kokoro in Buddhism - Perplexity.md` | Sherlock's framing of _kokoro_ as dynamic field; _mushin_ as Buddhist paradox | Nothing of substance; the note was short and largely absorbed |

---

## 3. Merged into [[Kokoro in Practice]]

| Source note | What was taken |
|---|---|
| `Gassho, Bowing and Intention.md` | The full handwritten transcription, Yoso's own lines, the Kierkegaard quote and its kept variant, the practice guidance |
| `Honour Each Cell in Your Body.md` | The gassho verse, the breath verse, the practice paragraph, "microcosm and macrocosm" |
| `Kokoro and Spirit.md` | The _ki_ / _jing_ / _prāṇa_ / _spiritus_ table, the _neidan_ refinement sequence, the "one training from different angles" conclusion |
| `Unite in Kokoro - Essay.md` | _Mushin_ section, _makoto_ and the waterfall line, Zeami's _kabu-isshin_ and _hana_, the closing practice paragraph |
| `Kokoro for a Liquid Reality.md` | Waterfall, ripple, and open hand, in short practice form only — the essay remains the full treatment |
| `2026-09-02-kokoro-shinsei-dojo-challenge.md` | The three-circle structure and the paradox-of-depiction passage |
| `2026-06-15-kokoro-energy-field.md` | The Bhagavad Gītā line on connected energy |

---

## 4. Duplicates found

1. **`kokoro in daily life.md` ≡ `kokoro in daily life 1.md`** — byte-for-byte identical bodies. The `1` copy has no frontmatter and a stray Perplexity logo plus a scratch line ("Memory, The bird and the butterfly, Kyoto - Yuji?"). A third copy sits at `Nodes/99 Files/kokoro in daily life`.
2. **`Unite in Kokoro - 心.md`** — contains its own research section three times verbatim and its "Further reading" block four times. Roughly 60% of the file is self-duplication.
3. **`Unite in Kokoro Draft Before review.md`** — an earlier draft of the same material. Also exists in `Nodes/`.
4. **`Kokoro Bibliography.md`** ("mmm... ask the genius...") and **`Kokoro Bibliography 1.md`** ("insert by subject name / D.T. Suzuki?") — two empty stubs. A third copy of the first sits in `Nodes/`.
5. **`2026-09-02-1111-kokoro-shinsei-dojo-challenge.md`** (in `01 Raw/Kokoro/`) ≈ **`2026-09-02-kokoro-shinsei-dojo-challenge.md`** (in `Unique Notes/`) — near-identical. The Unique Notes copy has correct `type: unique` frontmatter and is the one to keep.
6. **Flowchart, Mindmap, and Concept Graph canvas** — three renderings of the same map, all at `b 0.1`, all companions to `Unite in Kokoro - 心`. The mindmap is the most complete.
7. **The KOKORO scale and Radio Taiso material** appears in both `Kokoro as Body, Heart, Mind` and `kokoro in daily life`.
8. **The _mushin_ discussion** appears in four notes: `Kokoro in Buddhism`, `Unite in Kokoro - Essay`, `Kokoro for a Liquid Reality`, and `Kokoro as Body, Heart, Mind`.

---

## 5. Dropped, and why

**Fabricated or misattributed statistics.** The two `kokoro in daily life` notes and parts of `Kokoro as Body, Heart, Mind` carry precise-looking figures with no traceable source: 23% higher factory-team productivity from Radio Taiso; 78% of elderly practitioners with better joint mobility; 27% cortisol reduction and 19% alpha-wave increase from bathing; 92% plastic-waste reduction; 68% less _kaiseki_ leftovers; 17% emotional-IQ gain and 31% resilience gain from _Kokoro no Nōto_; "200 hours minimum" community service. None of these are supportable from the cited pages. They were dropped entirely rather than hedged.

**Misattributions in the same notes.** "Project lead Tereza Nakaya" conflates Teresa Nakaya, author of the _Adeptus_ article on moral education, with Kyoto's _Shimatsu-no-Kokoro_ sustainability programme — unrelated. "Developer Mark Divine" of the _mamoru_ app conflates the SEALFIT founder with an unrelated platform. Both dropped.

**The KOKORO scale numbers.** The RIKEN scale is real, but the two raw notes give mutually contradictory figures for the same 2011 study (one says security fell from +32 to −58; the other says anxiety spiked to −82.3 ±6.7). At most one can be right. Dropped pending a look at the RIKEN page itself.

**The "holographic principle" framing.** `Kokoro in Japanese Thought` builds an argument that _kokoro_ functions holographically across aesthetics, ethics, and the nation-state, with the emperor as microcosm of _kokutai_. The cited sources — chiefly the Stanford encyclopedia entry on Japanese philosophy — do not support this, and the _kokutai_ strand carries wartime-ideology baggage that the note handles without comment. Noted as an essayistic extrapolation in [[Kokoro - The Word and Its Range]] §3, not reproduced.

**Not about _kokoro_.** `Consciousness.md` (a large general-consciousness note with its own separate life in the vault), `Heart, Body and intention as one!...md` (Buddhist praxis generally), `Home — AUM.md` (artwork), `The Gift of Presence - draft.md` (a thin Gemini output — its one usable element, the haiku, is Yoso's).

**Empty.** `Unite in Kokoro Glitch.md` (four words), both bibliography stubs.

---

## 6. Still to check

- **Routledge attribution.** `Kokoro - Soseki` credits the encyclopedia's _Kokoro_ entry to Meera Viswanathan; `Unite in Kokoro - Essay` and `Kokoro for a Liquid Reality` credit it to John C. Maraldo. One is wrong. **Still open.**
- \~~**`Kokoro and Shraddha claude.md` has broken frontmatter**~~ — fixed 13 September 2026, and the note was rebuilt with a proper comparison; see §8.
- \~~**The _kogori_ / _kogoru_ etymology** rests on two popular articles~~ — replaced 13 September 2026 with the four-theory account from the Japanese dictionaries (Gotō 2020); the earlier claim that _kokoro_ never named the organ was also corrected. See [[Kokoro - The Word and Its Range]] §1.
- \~~**Zeami on _kokoro_** is cited through a clown-theatre essay~~ — replaced 13 September 2026 with Pilgrim (1969) and Rimer/Yamazaki (1984) in both [[Kokoro in Practice]] and the doctrinal note.
- **`Sources/00 Cleaned` was empty until now** — the folder existed as an intention. It is now in use.

---

## 7. Suggested next step

When you are satisfied with the two cleaned notes, the raw layer can be reduced. Safe to retire outright: both `kokoro in daily life` files, both bibliography stubs, `Unite in Kokoro Glitch`, `Unite in Kokoro Draft Before review`, and the duplicate `2026-09-02-1111` note. Everything else should be kept until its links are re-pointed — several notes elsewhere in the vault link into `Unite in Kokoro - 心` by section anchor.

---

## 8. Second pass — 13 September 2026

A source-verification pass over the core set, after the consolidation.

| Note | What was checked | What changed |
|---|---|---|
| [[Kokoro - The Word and Its Range]] | Etymology against Japanese philological references; Sasaki citation | §1 rewritten: four competing etymologies, origin marked undetermined; **factual correction** — _kokoro_ did name the heart organ in Old Japanese (Kojiki 712), the organ sense narrowed in Heian; Sasaki corrected from "Kōichi, 19–33" to Ken-ichi, 3–19; Gotō 2020 and Miyaji 1979 added; Mermaid diagram added |
| [[Kokoro and Shraddha claude\|Kokoro and Shraddha]] | Śraddhā etymology; Nakaya citation; the comparison itself | Frontmatter fixed; comparison developed from four lines into a full section with table and diagram; Nakaya corrected from "Tomáš, 2017" to Teresa, 2019; Hara 1964 added |
| [[Kokoro in Practice]] | Zeami sourcing; Kierkegaard quote; duplication with the doctrinal note | §1 trimmed; Pilgrim and Rimer/Yamazaki replace the two blogs; **misattribution corrected** — "Life is not a problem to be solved" is Radhakrishnan's, not Kierkegaard's; Yuasa added to §6 |
| [[Kokoro - Japanese Buddhism - Heart-Mind in Doctrine and Practice]] | Dates and attributions throughout (Kūkai, Shunzei, Chōmei, Dōgen, Nichiren, Baigan, Saigyō at _Shinkokinshū_ 362, Sōseki's 1894–95 retreat) | All held. Zeami paragraph added to §5; redundant Wikipedia citations dropped; **moved from `01 Raw` to `00 Cleaned`** to match its listing in the Index |

**Merge decision.** The doctrinal note and _Kokoro in Practice_ were considered for merging and kept separate: one is a history resting on scholarship, the other a practice manual half in Yoso's own voice. They cross-reference at every point where they touch.

---

## Source

Claude, Anthropic, claude-opus-5, conversation with author, 13 September 2026. §8 and the updates to §1 and §6 by Claude, Anthropic, claude-sonnet-4-6, conversation with author, 13 September 2026.
