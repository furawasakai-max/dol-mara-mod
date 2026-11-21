# v0.1.7 runtime test plan

The source compiles, and both patch routes apply cleanly. Test this update using a copy of an existing save with Mara already met.

## Event chance and trigger

- [ ] Complete Organize Pet Supplies and confirm the rest offer can appear.
- [ ] Complete Clean Animal Equipment and confirm the rest offer can appear.
- [ ] Complete Prepare Food Supplies and confirm the rest offer can appear.
- [ ] Repeat several house-work tasks to confirm the event is occasional (25% per completed task), not guaranteed.
- [ ] Confirm shop work does not trigger the house rest event.

## Dialogue and choices

- [ ] Confirm Mara naturally notices the player has been working and asks them to take a short break.
- [ ] Confirm she prepares two cups of tea and sits with the player.
- [ ] Accept the tea and confirm the tea scene plays.
- [ ] Decline the tea and confirm the player returns to Danube Street without receiving tea effects.
- [ ] Confirm the normal Continue option is hidden when the rest offer appears, so the player chooses accept or decline.

## Effects and progression

- [ ] Confirm accepting tea reduces Stress by 6.
- [ ] Confirm accepting tea increases Mara's Love by 1.
- [ ] Confirm accepted tea-break count increases by one.
- [ ] Confirm the work task's normal money reward and relationship increases remain unchanged.
- [ ] Confirm the event does not advance time separately from the completed work task.

## Journal and saves

- [ ] Open Journal after accepting tea and confirm the tea-break count is recorded.
- [ ] Load an existing v0.1.6 save and confirm restBreaks initializes to zero without resetting Mara's existing stats or progress.
- [ ] Accept a tea break, save, reload, and confirm the count persists.

## Existing core systems

- [ ] Confirm Mara appears in Social after meeting her.
- [ ] Confirm Mara can be selected from Attitudes after accepting the romance route.
- [ ] Confirm shop/home schedule and Pet Shop placement are unchanged.