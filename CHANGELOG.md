# Changelog

## v0.1.11 - Pet Room and Command Training

- Changed Mara's established Handler/Pet house visit to lead into a dedicated pet-room hub.
- Added a cushion wait activity (10 minutes).
- Added a once-per-day pet-bowl meal (10 minutes, Hunger -500, Stress -3).
- Added a cushioned cage sleep point with native sleep-duration links and sleep/wake effects.
- Added once-per-day command training: Down, Heel, Stay, and Come.
- Uses the vanilla leash attachment and detachment widgets during the training scene.
- Training includes following Mara on all fours around the room; completion grants +2 Mara Dominance and +1 Mara Trust.
- Added a stop option throughout training; stopping removes the lead and gives no completion reward.
- Kept housework available as an optional activity from the pet room. Pet-mode chores return to the room after completion.
- Added `petTrainingSessions` save migration and advanced `objectVersion.mara` to 7.
- Preserved non-pet house visits, prior housework rewards, cafe events, and the v0.1.10 pet-house outfit handling.

Validation:
- Tweego compilation succeeded.
- The incremental patch applies to v0.1.10 source with zero rejects and recreates both modified source files byte-for-byte.
- The full patch applies to clean vanilla 0.5.13.8 with zero rejects; all 17 changed files match byte-for-byte.
- The full-patch verification tree compiles successfully.
- In-game verification of sleep/wake, leash transitions, and daily limits remains outstanding.

## Previous releases

- **v0.1.10:** Added the Handler/Pet reaffirmation, collar inspection scene, four house rules, outfit handling, and migration.
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