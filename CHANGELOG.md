# Changelog

## v0.1.10 - Pet House Rules

- Added a follow-up option at Mara's house after the Handler/Pet proposal is accepted.
- Added a second verbal confirmation before the role-play scene.
- Changed Mara's dialogue from cheerful to firm and authoritative after the player confirms.
- Added the collar, undressing, crawling, and non-explicit inspection scene.
- Added the four requested rules: speech by permission, nude and collared while inside Mara's home, following Mara's instructions, and punishment for breaking the rules.
- Reapplies the house outfit on later visits and restores the prior outfit on exit.
- Adds three safe save migration fields and advances Mara's object version to 6.
- Leaves existing romance, proposal requirements, housework rewards, and cafe events unchanged.

Validation:
- Tweego compilation succeeded.
- The incremental patch applies to v0.1.9 source with zero rejects and reproduces both changed source files byte-for-byte.
- The cumulative patch applies to clean vanilla 0.5.13.8 with zero rejects.
- In-game validation of the new scene, clothing restoration, and save/reload behaviour remains outstanding.

## v0.1.9 - Random cafe conversation topic

- Replaced the three visible cafe conversation choices with a single 30-minute "Sit and chat with Mara" action.
- Randomly selects one of the three existing topics after each conversation begins: pets, the player's life, or the weather.
- Follows the random-topic pattern used by Avery's mansion chat.
- Preserves +1 Mara Love and +1 Mara Trust for each completed chat.
- Preserves the post-chat 25% goodbye chance, automatic 19:00 departure, and repeated-chat flow.
- Does not change the evening cafe appearance roll or Mara's shop/home schedule.

## Previous releases

- v0.1.8: Added random evening Ocean Breeze Cafe visits and three conversation topics.
- v0.1.7: Added the random housework tea break.
- v0.1.6: Integrated Mara into vanilla named-NPC status, Attitudes, Social, Journal, and save migration.
- v0.1.5: Replaced the Shopping Centre Pet Shop row with Mara's Pet Shop and added the standard leave icon.
- v0.1.4: Added the daily shop/home schedule.
- v0.1.3: Added persistent visits to both Mara locations.
- v0.1.2: Reformatted reward stat feedback.
- v0.1.1: Added native stat feedback.
- v0.1.0: Added the initial Mara NPC, shop, house work, relationship stats, and early events.