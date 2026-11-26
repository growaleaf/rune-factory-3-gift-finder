# Rune Factory 3 Special Gift Finder

Static page. Search an item to see which villagers love it or like it. Or pick a villager to see their full loved/liked gift lists.

## Data

Parsed from `../source_steamah.html` (steamah.com, "Rune Factory 3 Special Gifting Guide for All Villagers", posted September 7, 2023, fetched 2026-11-26) via `../parse.py` into `../parsed.json`, then embedded in `data.js`.

24 villagers covered by the source, all 24 parsed cleanly with a non-empty Loved and Liked list; none were skipped. Two villager sections in the source markup omit the colon after the "Loved"/"Liked" label (Marian's "Loved", Raven's "Liked"); the parser handles both forms. One source item name has a typo ("Orange Juicewimg]" in Ondorus's liked list); it is copied verbatim rather than corrected, so nothing is invented. Nothing is invented to fill gaps; villagers or items not in the source are simply not listed.

## Files

- `index.html` — the page
- `data.js` — the 24 villagers' gift data (also usable from Node via `module.exports`)
- `test.js` — known-answer tests, run with `node test.js`

## Caveat

Single source, no disliked list. Community gift guides can disagree with each other and with in-game behavior. Verify in-game.
