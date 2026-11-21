# Mara v0.1.10 runtime test plan

The v0.1.10 source compiles. The incremental update applies to a v0.1.9 source tree with zero rejects, and the cumulative full patch applies to clean vanilla 0.5.13.8. The new scenes and outfit transitions still require in-game verification.

## Handler/Pet confirmation

- [ ] Load a save where Mara's Handler/Pet proposal has been accepted.
- [ ] Approach Mara's house while she is home.
- [ ] Confirm "Talk about your arrangement" appears.
- [ ] Choose "I need more time" and confirm the rules are not activated.
- [ ] Re-enter the option and choose the affirmative response.
- [ ] Confirm Mara's tone changes from cheerful to firm after the second confirmation.
- [ ] Choose to wear the collar and continue.

## Collar scene and rules

- [ ] Confirm removable clothing is stored and the black leather collar is worn when the neck slot is available.
- [ ] Confirm the scene describes the player crawling on all fours and Mara inspecting posture, collar fit, and response to instructions.
- [ ] Confirm the four rules appear: speech by permission, nude and collared in Mara's home, follow Mara's instructions, and punishment for breaking rules.
- [ ] Confirm the rules flag is saved.

## Repeat visits and outfit restoration

- [ ] Leave Mara's house and confirm previous clothes and neckwear are restored.
- [ ] Return while Mara is home and confirm the house outfit is reapplied automatically.
- [ ] Confirm housework options remain available.
- [ ] Complete each of the three housework tasks and confirm the outfit is restored on exit.
- [ ] Take a tea break during housework and confirm the house outfit remains active until leaving.
- [ ] Test a save/reload while the rules are active.

## Save compatibility

- [ ] Load a pre-v0.1.10 save with no new Mara fields and confirm initialization does not reset existing relationship progress.
- [ ] Confirm objectVersion.mara advances to 6.
- [ ] Test with the player wearing no neckwear, ordinary neckwear, and an engine-locked/cursed neck item.

## v0.1.9 regression

- [ ] Confirm the cafe still offers one "Sit and chat with Mara (0:30)" action.
- [ ] Confirm topics are randomly selected from pets, the player's life, and the weather.
- [ ] Confirm each completed chat grants +1 Love and +1 Trust.
- [ ] Confirm the post-chat goodbye chance and 19:00 departure remain intact.