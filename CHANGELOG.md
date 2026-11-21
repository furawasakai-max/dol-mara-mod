# Changelog

## v0.1.8 - Mara's evening cafe chats

- Added a 40% once-per-day chance for Mara to visit Ocean Breeze Cafe between 17:00 and 18:59, after the player has met her at the shop or home.
- The daily presence roll is saved so revisiting locations cannot reroll her availability.
- Added an Approach Mara interaction at Ocean Breeze Cafe when she is present.
- Added three 30-minute conversations: pets, the player's life, and the weather.
- Each completed chat adds 1 Mara Love and 1 Mara Trust.
- After each chat, a 25% chance has Mara say goodbye and head home; she also leaves automatically at 19:00.
- Prevented starting a 30-minute chat when there is not enough time before 19:00.
- Updated Mara's shop and home passages to show that she is away at the cafe rather than allowing interaction at the wrong location.
- Added a persistent cafe conversation count to Mara's Journal and migrated older saves with a default of zero.
- Existing shop/home schedules and housework rewards are unchanged.

Validation:
- Tweego compilation succeeded.
- JavaScript syntax checks passed for named-npc.js and ingame.js.
- Incremental v0.1.8 patch applies to v0.1.7 source with zero rejects.
- Cumulative v0.1.8 patch applies to clean vanilla 0.5.13.8 with zero rejects.
- Both resulting source trees match the v0.1.8 working source byte-for-byte.
- In-game cafe availability, time cost, conversation rewards, goodbye chance, and Journal count still require player testing.

## Previous releases

- **v0.1.7:** Added a random once-per-day Mara housework tea break.
- **v0.1.6:** Integrated Mara into named-NPC status, Attitudes, Social, Journal, appearance defaults, and save migration.
- **v0.1.5:** Replaced the Shopping Centre Pet Shop row with Mara's Pet Shop and added the standard leave icon.
- **v0.1.4:** Added the daily shop/home schedule.
- **v0.1.3:** Added persistent visits to both Mara locations.
- **v0.1.2:** Reformatted reward stat feedback.
- **v0.1.1:** Added native stat feedback.
- **v0.1.0:** Added the initial Mara NPC, shop, house work, relationship stats, and early events.