# Transatlantic Translator

A tiny, self-contained web app that translates between **British English** and **American English** in both directions, live as you type.

**Use it:** download `index.html` and open it in any modern browser. No build step, no dependencies, works offline.

## Features

- Toggle direction (British → American / American → British), or **Swap** to feed the translation back in.
- **160+ vocabulary pairs** (boot/trunk, lorry/truck, flat/apartment, crisps/chips, chips/fries, car park/parking lot, …), including multi-word phrases and auto-generated plurals.
- **Spelling rules** with exception lists:
  - `-our`/`-or` (colour → color, but not *four*, *hour*, *flour*, *glamour*)
  - `-ise`/`-ize`, `-yse`/`-yze` (organise → organize, but not *exercise*, *surprise*, *advertise*; size/prize/seize are left alone going the other way)
  - `-re`/`-er` (centre → center, but not *acre*, *ogre*, *genre*, *massacre*)
  - doubled L (travelling → traveling, cancelled → canceled)
  - plus explicit pairs: defence/defense, catalogue/catalog, grey/gray, paediatric/pediatric, …
- Whole-word matching, preserved capitalisation (`Lift` → `Elevator`, `CAR PARK` → `PARKING LOT`) and punctuation.
- Changed words are highlighted; hover to see the original.

Ambiguous words (e.g. *line*, *fall*, *story*, *check*) are translated in one direction only, so ordinary American text isn't mangled.

## Extending

All data lives at the top of the `<script>` in `index.html`: add pairs to `VOCAB` (vocabulary) or `SPELLING` (spelling variants) as `['british', 'american', flags]`, and tweak the exception lists below them.
