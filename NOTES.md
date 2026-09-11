# Mga Nota sa Paggula — Translation Notes

*Kini nga payl nagpakita sa matag bersikulo nga gihikap sa kamot sa tawo o
sa usa ka desisyon. Ang ubang mga nota Iningles — bahin sa Hebreohanong
estruktura ug mga pakisayran.*

This file records every verse where a human hand or a ruling touched the
Cebuano rendering — the fifty-second chair, the fourth Austronesian — so any
verse can be audited. Rails: the Selah Cebuano discipline (Yahweh / Elohim at
the Name seat; ⟨את⟩ total; ⟨…⟩ supplied words only; Sheol never *impyerno*;
Mesiyas never *Kristo*; Ginoo/GINOO, Jehova, Diyos/Dios at the Name seat
rejected).

## The burn and the gleaning (2026-09-01)

Relay lit 14:46, moved on 20:35 with **35 residue** (pressed one per call).
Census rounds: **493 → 43 → 356 → …** (see below) to zero. Final census:
Yahweh 5,805 · Elohim 2,154 · ⟨את⟩ in 7,385 verses · every leak class zero.

## Model tics found on this chair — exposed

- **⟨silа⟩ with a Cyrillic а** (U+0430) — the model's habitual fill for the
  Hebrew plural suffix, invisible to the script-bleed check because bracket
  content is stripped first. Mechanical corpus pass (а → a), run three times
  as re-renders reintroduced it (22 + 3 + 1 files).
- **⟨is⟩** — the English copula as a fill; Cebuano needs none. Adding *is* to
  the census stoplist flagged 356 verses; the re-renders brought some back,
  so a mechanical strip (`strip-is!`) now removes it corpus-wide (110 + 4 + 4).
- **Dios beside an Elohim gloss** — the sentence carrying *Dios/Diyos* where
  the gloss already renders Elohim (Ezra 8:21, 8:23, 3:11; Gen 46:1; Job 15:4
  fill) → Elohim, per the rails.

## Tooling issues met on this chair (the clone lessons continue)

- `rel` path offset: `"/ceb/"` is five characters (the mg `/zu/` lesson in a
  new coat) — Tekoa's reported refs were mangled until fixed.
- Regex `d[iy]os` matches *dios* but never *diyos* (needs both letters) —
  the Tekoa plural class was dead until `di?y?os`.
- The classifier only knew token-seats; *diyos* appearing only in the
  sentence (no diyos-bearing token) fell to garble — translation-only
  clauses added (lowercase lawful; capital → Elohim).

## Hand-repaired verses (2026-09-01)

Scripts hold every pair: `dev/scripts/ceb_hand_fixes.clj` (passes 1–2).
Marker discipline: never a blanket ⟨את⟩ replace; markers kept where true
(2 Sam 17:8 both markers kept while the doubled phrase was unduplicated;
Exod 20:23 אתי and Exod 12:48/12:38 אתם = *with*, not the marker; Deut 7:24
אֹתָם = the marker → ⟨את⟩ sila; Ezra 10:3's phantom ⟨אֵת⟩ removed — the verse
has none). Script bleed dropped (⟨ҫедек⟩, ⟨kāmaґ⟩, ⟨部分⟩→⟨pipila⟩, 【kiyor】→
⟨kiyor⟩, an html span in Zech 1:16); רב־טבחים rendered (2 Kgs 25:12); *mga
shoots* → *mga saha* (Ps 128:3); Dan 3:12 Aramaic יתהון → *kanila*.

## Per-token floors (2026-09-01)

- **Diyos/Dios**: 155 verses carry the lowercase word — the gods of the
  nations, idol seats, all lawful (Tekoa: 0 garble · 229 lawful · capital
  fixes to Elohim where the gloss already said so).
- **Ginoo**: token-level against the surfaces: **יהוה → Ginoo: 0.** The 51
  review hits are human lords (אדני *akong ginoo*, בעלי, גברת mistress).

## Aleph-tav audit

`audit :ceb` → `repair! :ceb`: first pass 26 strays stripped, 15 sentence
edits, 3 added, 59 misaligned re-rendered; second pass 2 misaligned →
re-rendered; final **misaligned 0 · stray 0 · missing 0**.

## Open for Scott

- UI catalog flags (`docs/language/stragglers/ceb.md`, 30): the `pung-`
  parts-of-speech coinages; *Ngalan sa Dios* vs *Balaang Ngalan*; *tabon sa
  dughan* for the breastplate; *lanot* for fiber.
- The rails' gate specimen writes `ang` unbracketed; the corpus brackets it
  (⟨ang⟩ as a supplied article) — one ruling wanted.
- README/CONTRIBUTING point at selahproject.com/support while LICENSE says
  selahproject.com — the same split exists in the so and az chairs.
