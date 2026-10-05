# Pandora Defuse: spec (v1)

Solo mod for Borderlands: The Pre-Sequel. Counter-Strike: Source is rules inspiration only (no assets, no VAC exposure).

## Match
Best of 5 (first to 3). Each round: 15 s buy phase, 115 s round, bomb timer 40 s, plant 3 s, defuse 10 s. Player alternates attacker/defender. 3 AI allies vs 4 Hyperion bots.

## Economy
Start $800. Kill reward by weapon, plant/defuse $300, win $3250, loss $1400 (+$500 per consecutive loss, cap $3400), max $16000. Cash carries over between rounds. See sheets/economy.json.

## Build order
1. Inspect the game: confirm SDK install, find map, weapon, pawn and kill-event objects. Fill every `null` in the sheets, then update `hooks.verified`.
2. Spike the riskiest piece first: the custom bomb (h_bomb).
3. Buy menu + cash, then rounds, then bots/allies.
4. Preflight: list every unfilled cell and unresolved cross-sheet reference (weapon_ref, needs). Build only when clean.
5. Package, then Melty inspect_package, validate_recipe, one_click_check, upload, screenshot, test, publish.

## Open items
- Does Melty install a loader for this game? (game_info)
- Does a similar mashup already exist? (search_mashups)
- Credits, license, remix choice.
- Real gameplay screenshot.
- Content generation costing money (fal.ai) needs approval first. v1 needs none.

## Never
Do not put the Melty token in any file.
