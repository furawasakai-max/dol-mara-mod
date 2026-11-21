# Changelog

## v0.1.15 - Night Cage Routine

- Added a locked-cage night routine when the player remains in Mara's home after 22:00.
- The cage is the existing cushioned sleep point.
- Added a lockpick escape option only when Skulduggery is at least 400; the vanilla check uses difficulty 700.
- A successful check unlocks the cage and allows the player to leave Mara's house.
- A failed check makes noise and brings Mara to the room.
- Mara takes the player to the discipline room for a one-hour non-graphic reprimand, then leashes and returns the player to the cage.
- The cage is locked again after the failed escape until 07:00.
- Added a sleep option that uses native sleep/wake effects and advances the remaining time exactly to 07:00.
- At 07:00, Mara arrives, unlocks the cage, and detaches the lead if attached.
- If the one-hour reprimand crosses 07:00, the cage is unlocked immediately on return.
- Added safe migration for `nightCageCaughtUntil`; advances `objectVersion.mara` to 10.

Validation:
- Tweego compilation succeeded.
- Incremental patch applies to v0.1.14 source with zero rejects and reproduces the changed Mara passage file byte-for-byte.
- Cumulative full patch applies directly to clean vanilla 0.5.13.8 with zero rejects; all 17 changed/added source files match byte-for-byte.
- Clean full-patch verification tree compiled successfully.
- Static passage-link and time-boundary checks passed.
- In-game runtime testing remains outstanding.

## Previous releases

- **v0.1.14:** Rewrote Mara's pet-role dialogue to be colder and more dismissive.
- **v0.1.13:** Added Mara's discipline room, daily random offer, whip/cane choices, X-frame scene, and +20 Masochism progress.
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