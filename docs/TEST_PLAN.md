# Mara v0.1.11 runtime test plan

The v0.1.11 source compiles. The incremental patch applies to v0.1.10 source with zero rejects, and the cumulative patch applies to clean vanilla 0.5.13.8 with zero rejects. In-game verification is still required for sleep, leash state, and daily limits.

## Pet-room entry

- [ ] Load a v0.1.10 save where `petRulesEstablished` is true.
- [ ] Visit Mara while she is home and enter the pet room.
- [ ] Confirm the room presents cushion waiting, pet-bowl meal, cage sleep, command training, optional housework, and leave options.
- [ ] Confirm the player remains in Mara's house outfit and collar while using the room activities.

## Cushion waiting

- [ ] Select "Wait on the cushion for an order (0:10)".
- [ ] Confirm ten minutes pass and Mara's short instruction scene appears.
- [ ] Return to the pet room.

## Pet bowl

- [ ] Select "Eat from the pet bowl (0:10)".
- [ ] Confirm ten minutes pass, Hunger decreases by 500 (clamped by the vanilla widget), and Stress decreases by 3.
- [ ] Confirm the bowl option is marked as used for the rest of the day.
- [ ] Advance to a new day and confirm the bowl option becomes available again.

## Cage sleep point

- [ ] Enter the cage and confirm sleep-duration options from one to eight hours, plus Just sleep when tiredness is above zero.
- [ ] Select a fixed sleep duration and confirm time advances correctly.
- [ ] Select Just sleep in a separate test and confirm the normal sleep logic stops at the expected condition.
- [ ] Confirm waking effects and sleep effects execute and the player returns to Mara's pet room.
- [ ] Save and reload while in the pet room, then test cage sleep again.

## Command training

- [ ] Start training and confirm a lead is attached to the player's collar when the collar can accept a leash.
- [ ] Follow Down and confirm the player is described lowering onto all fours.
- [ ] Follow Heel and confirm the player crawls around the room after Mara.
- [ ] Follow Stay and Come, then confirm the lead is detached at completion.
- [ ] Confirm completion adds +2 Mara Dominance, +1 Mara Trust, and increments `petTrainingSessions` once.
- [ ] Confirm training is unavailable again for the rest of the day, then becomes available after the daily reset.
- [ ] Test Stop at each stage and confirm the lead is detached, no completion reward is granted, and the player returns to the pet room.
- [ ] Test a save with a cursed or otherwise locked neck item and confirm training does not overwrite the locked item.

## Housework and regression

- [ ] Confirm housework remains an optional activity from the pet room.
- [ ] Complete each task and confirm the original reward values remain unchanged.
- [ ] Confirm pet-mode tasks return to the pet room without restoring the street outfit.
- [ ] Confirm non-pet house visits still display the original greeting and housework choices.
- [ ] Confirm the house-leave path restores the player's previous clothes and neckwear.
- [ ] Confirm the housework tea break still returns to the selected task completion.
- [ ] Confirm cafe random topics and their +1 Love / +1 Trust rewards remain unchanged.

## Save compatibility

- [ ] Load a pre-v0.1.11 save and confirm `petTrainingSessions` initializes to 0.
- [ ] Confirm `objectVersion.mara` advances to 7.
- [ ] Confirm existing Mara Love, Lust, Trust, Dominance, romance, handler, cafe, and housework progress is preserved.