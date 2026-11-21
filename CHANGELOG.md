# Changelog

## v0.1.7 - Mara's housework tea break

- Added a 20% chance per housework task attempt for Mara to notice the player has been working hard and offer a rest.
- Limited the offer to once per in-game day.
- Added accept and politely-decline choices.
- Accepting takes 10 minutes. Mara brings tea and biscuits, sits with the player, and keeps them company.
- Accepting reduces Stress by 6 and Tiredness by 4, and increases Mara Love by 1.
- After the break, the player returns to the same task's completion passage, where the normal task payment and relationship reward are applied once.
- Declining continues the task without extra time or rest effects.
- Added a persistent accepted-break count to Mara's Journal.
- Existing housework time costs and rewards are unchanged; shop work is unaffected.
- Adapted the interruption pattern from the vanilla Farm Pigs Feed Nausea passages without copying their pregnancy/nausea trigger.

Validation:
- Tweego compilation succeeded.
- Incremental v0.1.7 patch applies on top of v0.1.6 with zero rejects.
- Cumulative v0.1.7 patch applies to clean vanilla 0.5.13.8 with zero rejects.
- Both resulting source trees match the v0.1.7 working source byte-for-byte.
- In-game event chance and reward-flow testing remains outstanding.

## Previous releases

- **v0.1.6:** Integrated Mara into vanilla named-NPC status, Love Interest eligibility, Attitudes, Social, Journal, appearance defaults, and save migration.
- **v0.1.5:** Replaced the Shopping Centre Pet Shop row with Mara's Pet Shop and added the standard leave icon.
- **v0.1.4:** Added the daily shop/home schedule.
- **v0.1.3:** Added persistent visits to both Mara locations.
- **v0.1.2:** Reformatted reward stat feedback.
- **v0.1.1:** Added native stat feedback.
- **v0.1.0:** Added the initial Mara NPC, shop, house work, relationship stats, and early events.