# Mara v0.1.14 dialogue test plan

The v0.1.14 source compiles. The incremental patch applies to v0.1.13 with zero rejects, and the cumulative full patch applies to clean vanilla 0.5.13.8. The clean full-patch source tree also compiles. Revised dialogue still requires in-game review.

## Pet-house tone

- [ ] Load a save where petRulesEstablished is true.
- [ ] Enter Mara's house and confirm the greeting is terse and dismissive, not cheerful.
- [ ] Confirm the pet-room hub describes the player as an incompetent pet and gives short directions.
- [ ] Confirm the cushion wait and no-order outcome use Mara's new impatient tone.
- [ ] Trigger several random cushion orders and review all seven command lines and responses.
- [ ] Eat from the bowl and confirm Hunger -500 and Stress -3 remain unchanged, with the new dialogue.
- [ ] Enter the cage and confirm sleep-duration options and sleep/wake mechanics remain unchanged.

## Training

- [ ] Confirm training introduction uses the revised tone.
- [ ] Review all seven random lesson introductions and outcomes.
- [ ] Confirm the lead stays slack, stop option remains available, and the lead is removed on completion and stop.
- [ ] Confirm completion still grants +2 Mara Dominance and +1 Trust.
- [ ] Confirm once-per-day training limit remains unchanged.

## Discipline room

- [ ] Confirm the random offer remains 35% on the first room visit per in-game day and does not reroll on re-entry.
- [ ] Review whip and cane selection dialogue.
- [ ] Confirm the stop word and stop/release options remain clear.
- [ ] Confirm decline and stop still award no Masochism.
- [ ] Confirm completing either tool session still awards +20 Masochism progress.
- [ ] Confirm the revised tone does not remove player confirmation or stop controls.

## Optional housework and regression

- [ ] In pet mode, confirm housework introduction and task-completion remarks use the rougher tone.
- [ ] Confirm non-pet housework dialogue remains unchanged.
- [ ] Confirm housework rewards, tea-break effects, and task durations remain unchanged.
- [ ] Confirm ordinary shop, cafe, romance, and non-pet house visits retain their prior dialogue.
- [ ] Confirm collar/clothing restoration when leaving Mara's home.
- [ ] Confirm a v0.1.13 save loads without a migration or loss of Mara progress.