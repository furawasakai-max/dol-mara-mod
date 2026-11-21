# Mara v0.1.15 runtime test plan

The v0.1.15 source compiles. The incremental patch applies to v0.1.14 source, and the single cumulative patch applies directly to clean vanilla 0.5.13.8. The clean full-patch tree also compiles. In-game verification remains necessary.

## Night entry

- [ ] Load a save where `petRulesEstablished` is true.
- [ ] Remain in Mara's house until 22:00.
- [ ] Confirm the normal pet-room activities are replaced by the night cage choices.
- [ ] Confirm the cushioned cage is the same sleep point used during the day.
- [ ] Confirm the night routine remains active at 23:59, 00:00, and 06:59.
- [ ] Confirm normal pet-room activities return after 07:00.

## Skulduggery escape

- [ ] Confirm the lockpick option is hidden below Skulduggery 400.
- [ ] Confirm the lockpick option appears at exactly 400 and above.
- [ ] Confirm the vanilla skill-check difficulty is 700.
- [ ] On success, confirm the cage unlocks and the player can leave via the normal house-leave passage.
- [ ] On failure, confirm noise is described and Mara arrives.
- [ ] Confirm failed attempts cannot be rerolled by leaving and re-entering before 07:00.
- [ ] Confirm the caught-until timestamp is saved and migrated for older saves.

## Failed attempt and discipline

- [ ] Confirm Mara's one-hour discipline passage consumes exactly 60 in-game minutes.
- [ ] Confirm the scene is non-graphic and keeps the existing stop/release option.
- [ ] Confirm Mara attaches the lead only when the collar supports it.
- [ ] Confirm Mara returns the player to the cushioned cage after the hour.
- [ ] Confirm the cage is locked again if the time is before 07:00.
- [ ] Confirm the cage is unlocked immediately if the hour crosses 07:00.
- [ ] Confirm the player cannot start another lockpick attempt until the stored release time.

## Sleep and dawn

- [ ] Choose sleep at 22:00 and confirm wake at exactly 07:00.
- [ ] Repeat at 22:30, 23:59, 00:00, 00:30, 06:30, and 06:59.
- [ ] Confirm native sleep, waking effects, sleep effects, and daily time processing execute.
- [ ] Confirm Mara arrives at 07:00, unlocks the cage, and detaches the lead if present.
- [ ] Confirm the morning passage returns to the pet-room menu.

## Regression and save compatibility

- [ ] Confirm daytime cage sleep remains unchanged.
- [ ] Confirm cushion orders, training, pet bowl, discipline room, and housework still work during the day.
- [ ] Confirm outfit restoration when leaving Mara's house.
- [ ] Load a v0.1.14 save and confirm existing relationship and pet-room progress is preserved.
- [ ] Confirm `objectVersion.mara` advances to 10.
- [ ] Confirm `nightCageCaughtUntil` initializes safely on an older save.