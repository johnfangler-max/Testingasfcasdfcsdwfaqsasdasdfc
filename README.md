# Pandora Defuse

A solo mod for **Borderlands: The Pre-Sequel**: a best-of-5 bomb-plant/defuse match against Hyperion bots with AI teammates, with Counter-Strike-style buy phases and cash that carries between rounds.

Counter-Strike: Source is inspiration only (rules, no assets). Players need only Borderlands: The Pre-Sequel.

**Status: design only.** Nothing is built or tested yet. Every game-object reference in `sheets/` is `null` until the game is inspected.

## Layout
- `docs/SPEC.md`: match rules, economy, build order, open items
- `sheets/`: the design source of truth (one JSON sheet per game system). Change a sheet before changing code.
- `mod/`: mod code goes here (generated from the sheets)

## Next steps
1. Inspect the game and fill the `null` cells and `hooks.verified`.
2. Spike the custom bomb (`h_bomb`) first.
3. Run the preflight (unfilled cells, unresolved cross-sheet references) before every build.
4. Package, validate with Melty (`inspect_package`, `validate_recipe`, `one_click_check`), then upload, add a real screenshot, test and publish.

License, credits and remix choice are not decided yet (see `sheets/melty_listing.json`).

Never commit the Melty token or any secrets.
