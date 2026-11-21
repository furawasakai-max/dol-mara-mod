# Changelog

## v0.1.12 - Random Pet-Play Events and Training

- Added a 40% random order chance during each ten-minute cushion wait.
- Added seven possible cushion orders: Paw, Down/Stay, Come, Fetch, Grooming, Place, and short Heel follow.
- Added a player choice to follow the random order or end the wait.
- Replaced the fixed daily command sequence with one of seven random lessons.
- Added lesson variants for basic obedience, Heel, Paw, Fetch, Place, grooming manners, and Settle.
- Kept crawling brief and on soft surfaces; the lead remains slack and is not used to pull on the neck.
- Added a stop option before/during training and a water/comfort check when the session ends.
- Preserved the once-per-day training limit and the existing +2 Mara Dominance / +1 Mara Trust completion reward.
- No new persistent save fields; advanced `objectVersion.mara` to 8.

Validation:
- Tweego compilation succeeded.
- Incremental patch applies to v0.1.11 with zero rejects and reproduces the updated source files byte-for-byte.
- Full patch applies to clean vanilla 0.5.13.8 with zero rejects; all 17 modified/added source files match byte-for-byte.
- The full-patch verification tree compiled successfully.
- Runtime testing remains outstanding.

## Previous releases

- **v0.1.11:** Added the pet-room hub, cushion wait, pet bowl, cushioned cage sleep point, and initial command-training event.
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