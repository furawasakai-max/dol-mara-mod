# Mara v0.1.16 runtime test plan

The v0.1.16 source compiles. The incremental patch applies to v0.1.15 with zero rejects. The cumulative patch applies to clean vanilla 0.5.13.8, all 17 modified/added source files match the development tree, and the clean full-patch tree compiles. In-game runtime testing remains necessary.

## Fix for premature dawn unlock

- [ ] At 22:00, fail the lockpick and complete the session. Confirm Mara returns the player to the cage and locks it again.
- [ ] Repeat at 23:00 and after midnight. Confirm the player remains locked before 07:00.
- [ ] Fail at 05:30 and complete the session. Confirm the return still relocks the cage before 07:00.
- [ ] Fail at 06:00 and complete all rounds. The full one-hour session should finish at 07:00, and Mara should unlock the cage.
- [ ] Fail at 06:30 and complete all rounds. Confirm the session finishes after 07:00 and Mara unlocks the cage.
- [ ] Confirm the message uses the current time from `<<ampm>>`, not a hard-coded "It's seven already" line.

## Detailed punishment flow

- [ ] Confirm a failed lockpick triggers Mara's arrival and a random whip or cane selection.
- [ ] Confirm the player is secured to the padded X-frame with broad-lined cuffs.
- [ ] Confirm Stage 1 has five described strokes and applies `masopain 15` once.
- [ ] Confirm Stage 2 has six described strokes and applies `masopain 15` once.
- [ ] Confirm Stage 3 has three final described strokes and applies `masopain 15` once.
- [ ] Confirm the complete route consumes exactly 60 minutes: escort 5 + stages 20, 20, and 10 + return 5.
- [ ] Confirm a stop link is available before the first round and between all rounds.
- [ ] Stop during each round in separate test saves. Confirm Mara releases the player, returns them to the cage, and does not clear the until-07:00 lockout.
- [ ] Revisit or reload a completed round and confirm its `masopain` effect does not apply a second time.
- [ ] Confirm the lead is attached only when the collar supports it.

## Sleep and dawn regression

- [ ] Choose the sleep option from 22:00, midnight, 06:30, and 06:59; confirm the player wakes at exactly 07:00.
- [ ] Confirm native sleep, waking effects, and sleep effects still execute.
- [ ] Confirm Mara unlocks the cage and detaches an attached lead.

## Regression and save compatibility

- [ ] Confirm Skulduggery 400+ gate and difficulty 700 check remain unchanged.
- [ ] Confirm successful lockpicking still lets the player leave.
- [ ] Confirm failed attempts still cannot be repeated before dawn.
- [ ] Confirm cushion orders, training, discipline-room event, pet bowl, daytime cage sleep, housework, and outfit restoration remain unchanged.
- [ ] Load a v0.1.15 save and confirm existing Mara progress remains intact; no migration is required.