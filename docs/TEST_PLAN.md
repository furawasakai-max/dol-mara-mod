# Mara runtime test plan

The user has confirmed that the v0.1.0 alpha works in-game. The v0.1.1 stat-feedback update has compiled successfully but still needs a visual check in the game.

## New save

- [ ] Start a new game and confirm Mara appears in the named-NPC system.
- [ ] Confirm Mara's displayed name, title, pronouns, and generated appearance.
- [ ] Open the Cheat Menu and test Mara's Love, Trust, and Dominance controls.
- [ ] Visit Shopping Centre during 09:00-13:59 and open Mara's Pet Shop.
- [ ] Visit outside those hours and confirm the shop is unavailable.
- [ ] Test each shop task, passage return, time flow, relationship rewards, and money reward.
- [ ] Confirm shop tasks display the correct Love, Trust, and Dominance gain notices.
- [ ] Confirm cash rewards display as positive amounts and match the wallet change.
- [ ] Test Browse, private collection threshold, romance threshold, and Handler proposal threshold.
- [ ] Visit Danube Street and confirm the Mara house event enters the work event pool.
- [ ] Test each house task and its money/stat rewards.
- [ ] Confirm house tasks display the correct Love and conditional Trust notices.
- [ ] Enable Blind Stats and confirm relationship notices are hidden while stats still update.

## Existing save migration

- [ ] Make a copy of a pre-Mara 0.5.13.8 save.
- [ ] Load the copy with the Mara build.
- [ ] Confirm the named-NPC migration creates Mara without resetting other NPC data.
- [ ] Save, reload, and confirm Mara's relationship values and event flags persist.
- [ ] Confirm the Cheat Menu and all Mara passages remain usable.
- [ ] Load the user's supplied working save copy and verify Mara's current progress is preserved.

## Known scope gaps

- The shop is a passage linked from Shopping Centre, not an independent map node.
- The alpha has simple fixed work tasks, not a full random shift/event system.
- The private collection is an introductory scene, not a complete equipment mechanic.
- The original design's richer work-history fields and some planned files are not implemented yet.
- No custom art is included.
