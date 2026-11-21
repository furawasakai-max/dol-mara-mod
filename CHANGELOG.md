# Changelog

## v0.1.16 - Night Cage Timing Fix and Detailed Discipline

- Fixed the false morning branch: `Time.hour >= 7` also evaluates true at 22:00 and 23:00. The dungeon return now uses only the stored absolute timestamp for the next 07:00 release.
- Reworked the failed-lockpick punishment to use three stages, following the pacing pattern of Avery's vanilla dungeon event.
- Mara randomly selects a whip or cane for the night scene.
- Added detailed but non-graphic descriptions for five opening strokes, six measured middle strokes, and three final strokes.
- Added one `<<masopain 15>>` effect for each completed round, guarded against duplicate application on passage revisit.
- Added a stop/release route at the start and between each round.
- The completed route remains exactly one hour: five minutes escort + 20 + 20 + 10 minutes for the three rounds + five minutes return.
- Returning before 07:00 relocks the same cushioned cage; returning at or after 07:00 unlocks it and removes the lead.
- No new persistent save fields; `objectVersion.mara` remains 10.

Validation:
- Tweego compilation succeeded for v0.1.16.
- Incremental patch applies to v0.1.15 with zero rejects and recreates the changed source file byte-for-byte.
- Cumulative full patch applies to clean vanilla 0.5.13.8; all 17 modified/added files match the development tree byte-for-byte.
- Clean full-patch verification tree compiled successfully.
- Static passage-link checks and time-allocation checks passed.
- In-game runtime testing remains outstanding.

## Previous releases

- **v0.1.15:** Added the night cage routine, Skulduggery escape check, failed-attempt punishment, and dawn unlock.
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