# Changelog

## v0.1.13 - Mara's Discipline Room

- Added a separate discipline room to the pet-house hub.
- Added a 35% chance for Mara to offer a session on the player's first visit to the room each in-game day.
- The daily roll persists for the rest of the day, preventing repeated entry from rerolling the offer.
- Added a player choice between a whip session and a cane session.
- Added an explicit confirmation before the session begins, with an agreed stop word/signal and stop/release choices before and during the event.
- Added a padded X-frame scene; the discipline itself is implied and non-graphic.
- Completing either session grants +20 to the vanilla Masochism progress value. Declining or stopping grants nothing.
- Uses the native `<<masochism 20>>` widget; the value is capped at 1000 and the level tier is recalculated by vanilla daily effects.
- No new persistent save fields; advances `objectVersion.mara` to 9.

Validation:
- Tweego compilation succeeded.
- Incremental patch applies to v0.1.12 source and reproduces the changed Mara passage file byte-for-byte.
- The single cumulative full patch dry-runs and applies to clean vanilla 0.5.13.8.
- All 17 modified/added source files match the final working tree byte-for-byte.
- The clean full-patch verification tree compiles.
- Runtime testing remains outstanding.

## Previous releases

- **v0.1.12:** Added random pet-play orders during cushion waiting and seven random daily training lessons.
- **v0.1.11:** Added the pet-room hub, cushion wait, pet bowl, cushioned cage sleep point, and initial training.
- **v0.1.10:** Added the Handler/Pet reaffirmation, collar inspection, four house rules, and repeat-visit outfit handling.
- **v0.1.9:** Added automatic random cafe conversation topics.
- **v0.1.8:** Added random evening Ocean Breeze Cafe visits and conversations.
- **v0.1.7:** Added the random housework tea break.
- **v0.1.6:** Integrated Mara into vanilla named-NPC status, Attitudes, Social, Journal, and save migration.
- **v0.1.5:** Replaced the Shopping Centre Pet Shop row with Mara's Pet Shop and added the standard leave icon.
- **v0.1.4:** Added the daily shop/home schedule.
- **v0.1.3:** Added persistent visits to both Mara locations.
- **v0.1.2:** Reformatted reward stat feedback.
- **v0.1.1:** Added native stat feedback.
- **v0.1.0:** Added the initial Mara NPC, shop, house work, relationship stats, and early events.