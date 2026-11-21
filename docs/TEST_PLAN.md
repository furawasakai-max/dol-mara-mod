# Mara v0.1.13 runtime test plan

The v0.1.13 source compiles. The incremental patch applies to v0.1.12 source, and the cumulative patch dry-runs/applies to clean vanilla 0.5.13.8. The clean full-patch source tree also compiles. In-game verification remains necessary.

## Room entry and daily chance

- [ ] Load a save where `petRulesEstablished` is true.
- [ ] Enter Mara's pet room and choose Visit Mara's discipline room.
- [ ] Confirm the room describes the padded X-frame, restraints, whip, cane, and safety release.
- [ ] On the first visit that day, confirm the game rolls once and either offers a session or says none is scheduled.
- [ ] Leave and re-enter several times on the same day; confirm the offer does not reroll.
- [ ] Advance to a new in-game day and confirm a fresh roll occurs.

## Whip and cane choices

- [ ] When the offer appears, choose to hear the session options.
- [ ] Confirm both Whip and Cane choices are available.
- [ ] Choose each option in separate test saves/days and confirm Mara's description uses the selected implement.
- [ ] Confirm the final explicit confirmation appears before the player is restrained.
- [ ] Choose Not today and confirm no Masochism progress is awarded.

## X-frame session and stop flow

- [ ] Confirm the player is described being secured to a padded X-frame with broad, lined cuffs.
- [ ] Confirm Mara checks the agreed stop word and signal before beginning.
- [ ] Confirm the session itself remains implied and non-graphic.
- [ ] Confirm a Stop and be released now link is available while restrained.
- [ ] Stop the session and confirm Mara releases the player, returns the player to the pet room, and awards no Masochism progress.
- [ ] Complete a session and confirm Mara releases the player and offers water.

## Masochism reward

- [ ] Confirm each completed whip session adds exactly +20 to `$masochism`.
- [ ] Confirm each completed cane session adds exactly +20 to `$masochism`.
- [ ] Confirm the stat does not increase on decline or stop.
- [ ] Navigate back/re-enter the completion passage and confirm the daily reward cannot be duplicated.
- [ ] Confirm the stat remains capped at 1000.
- [ ] Advance the day and confirm vanilla daily effects update the Masochism level tier when a threshold is crossed.

## Regression and saves

- [ ] Confirm cushion random orders and daily command training remain available.
- [ ] Confirm pet bowl, cage sleep, optional housework, and house-leave clothing restoration still work.
- [ ] Confirm non-pet house visits are unchanged.
- [ ] Confirm the v0.1.12 save loads without losing Mara relationship progress.
- [ ] Confirm `objectVersion.mara` advances to 9 and no new persistent fields are required.