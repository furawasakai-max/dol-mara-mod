# Changelog

## v0.1.6 - Core named-NPC integration

- Added maraSchedule() and maraStatusCheck() to the vanilla statusCheck() flow in named-npc.js.
- Added Mara to isPossibleLoveInterest() and connected romance acceptance to loveInterestAdd, so the vanilla Attitudes UI can select her.
- Added Mara to the debug unlock flow for Love Interests.
- Added Mara to Social's Primary Relationships after the player meets her, including Love, Trust, and Dominance display. Trust is only shown for Mara.
- Added a Mara Journal section for location, work count, private collection, romance, and Handler progression.
- Registered Mara's vanilla outfit set options and black-hair appearance default.
- Added $objectVersion.mara migration to initialize Mara as a named NPC without erasing old alpha relationship/body/appearance/state data.
- Fixed the Danube first-meeting event to pass through the Mara introduction passage consistently.

Validation:
- Tweego compilation succeeded.
- The full v0.1.6 patch applies to clean vanilla 0.5.13.8.
- The incremental v0.1.6 patch applies on top of v0.1.5.
- Runtime checks for the Social panel, Attitudes assignment, Journal, and old-save migration remain to be completed in-game.

## Previous releases

- **v0.1.5:** Replaced the original Pet Shop row with Mara's Pet Shop in the Shopping Centre list and added the standard leave icon.
- **v0.1.4:** Added the daily shop/home schedule.
- **v0.1.3:** Added persistent cross-location visits.
- **v0.1.2:** Reformatted reward stat feedback.
- **v0.1.1:** Added native stat feedback.
- **v0.1.0:** Added the initial Mara named NPC, shop, house work, relationship stats, and early event passages.