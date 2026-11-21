# Mara v0.1.7 runtime test plan

The v0.1.7 source compiles. Both the incremental v0.1.6 upgrade patch and cumulative clean-install patch apply with zero rejects and reproduce the working source tree exactly. The new event still needs in-game confirmation.

## Event chance and daily limit

- [ ] Complete Organize Pet Supplies and check whether the tea-break offer appears.
- [ ] Repeat with Clean Animal Equipment.
- [ ] Repeat with Prepare Food Supplies.
- [ ] Repeat housework attempts and confirm the offer is occasional, not guaranteed (20% per attempt).
- [ ] If the offer triggers, complete more housework on the same day and confirm it cannot trigger a second time.
- [ ] Advance to the next in-game day and confirm the offer can trigger again.
- [ ] Confirm shop work never triggers this housework event.

## Accepting the break

- [ ] Confirm Mara naturally notices the player has been working and offers tea.
- [ ] Accept the ten-minute break.
- [ ] Confirm Mara brings tea and biscuits and stays to keep the player company.
- [ ] Confirm time advances by 10 minutes.
- [ ] Confirm Mara Love increases by exactly 1.
- [ ] Confirm Stress decreases by 6 and Tiredness decreases by 4.
- [ ] Confirm the player returns to the same task's completion passage.
- [ ] Confirm the task's normal money, Love, and conditional Trust rewards are awarded once, not twice.
- [ ] Confirm the accepted-break count appears in Mara's Journal.

## Declining the break

- [ ] Trigger the offer and politely decline.
- [ ] Confirm the task continues to its completion passage without an additional time cost.
- [ ] Confirm no tea, stress, tiredness, or Love effect is applied.
- [ ] Confirm the daily offer remains used up after declining.

## Save and regression

- [ ] Load a copy of an existing v0.1.6 save and confirm Mara's stats and work progress remain intact.
- [ ] Save and reload after accepting a break; confirm the Journal count persists.
- [ ] Confirm housework choices still cost 30, 45, and 30 minutes respectively, with the 10-minute rest added only on acceptance.
- [ ] Confirm all housework payments and relationship rewards remain unchanged.
- [ ] Confirm the shop/home schedule and shop tasks are unaffected.