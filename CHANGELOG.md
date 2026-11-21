# Changelog

## v0.1.9 - Random cafe conversation topic

- Replaced the three visible cafe conversation choices with a single 30-minute "Sit and chat with Mara" action.
- Randomly selects one of the three existing topics after each conversation begins: pets, the player's life, or the weather.
- Follows the random-topic pattern used by Avery's mansion chat.
- Preserves +1 Mara Love and +1 Mara Trust for each completed chat.
- Preserves the post-chat 25% goodbye chance, automatic 19:00 departure, and repeated-chat flow.
- Does not change the evening cafe appearance roll or Mara's shop/home schedule.

Validation:
- Tweego compilation succeeded.
- The incremental patch applies to v0.1.8 source with zero rejects and reproduces the updated passage file byte-for-byte.
- The v0.1.8 full patch plus v0.1.9 update applies to clean vanilla 0.5.13.8 with zero rejects and reproduces all modified source files byte-for-byte.
- In-game verification of random topic selection and repeat chat flow remains outstanding.

## Previous releases

- **v0.1.8:** Added random evening Ocean Breeze Cafe visits and three conversation topics.
- **v0.1.7:** Added the random housework tea break.
- **v0.1.6:** Integrated Mara into vanilla named-NPC status, Attitudes, Social, Journal, and save migration.
- **v0.1.5:** Replaced the Shopping Centre Pet Shop row with Mara's Pet Shop and added the standard leave icon.
- **v0.1.4:** Added the daily shop/home schedule.
- **v0.1.3:** Added persistent visits to both Mara locations.
- **v0.1.2:** Reformatted reward stat feedback.
- **v0.1.1:** Added native stat feedback.
- **v0.1.0:** Added the initial Mara NPC, shop, house work, relationship stats, and early events.