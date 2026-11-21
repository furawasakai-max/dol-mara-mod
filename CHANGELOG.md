# Changelog

## v0.1.17 - Stay-at-Home Orders

- Mara is now unavailable for house interactions while she is at the pet shop or Ocean Breeze Cafe.
- The player can enter and remain in Mara's empty house while she is away, but Mara's pet activities and discipline-room interactions are hidden until she returns.
- Added a pre-departure waiting order before the 09:00 shop shift.
- Added a pre-cafe waiting order before the 17:00 cafe period, using the existing 40% daily cafe roll.
- Mara randomly assigns one greeting position: front door, cushioned cage, or discipline room.
- Added three player waiting-position choices and a timed wait until Mara returns at 14:00 or 19:00.
- Added a return check: correct position receives a terse acknowledgement; wrong position, leaving the house, or being absent triggers discipline.
- The reprimand randomly selects whip or cane, includes three timed rounds and one guarded Masochism-pain effect per round, and has a stop/release option.
- Entering the empty house applies the pet-house outfit; choosing to leave before entering does not alter clothing. Leaving during an active order marks the player as absent.
- Added save migration for the waiting assignment and punishment-session state; advances `objectVersion.mara` to 11.

Validation:
- Tweego compilation succeeded for v0.1.17.
- Incremental patch applies to v0.1.16 source with zero rejects; both changed source files match byte-for-byte.
- Cumulative full patch applies to clean vanilla 0.5.13.8; all 17 changed/added source files match the development tree byte-for-byte.
- The clean full-patch verification tree compiles successfully.
- Static Mara passage-link checks found no missing targets or duplicate names.
- In-game runtime testing remains outstanding.

## Previous releases

- **v0.1.16:** Fixed premature dawn unlock and expanded failed-lockpick punishment into three timed rounds.
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