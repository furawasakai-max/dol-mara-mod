# Mara runtime test plan

The user has confirmed that the v0.1.0 base mod works in-game. The v0.1.1 and v0.1.2 display updates have compiled and their incremental patches apply cleanly. The revised reward layout still needs in-game visual confirmation.

## New save

- [ ] Start a new game and confirm Mara appears in the named-NPC system.
- [ ] Confirm Mara's displayed name, title, pronouns, and generated appearance.
- [ ] Open the Cheat Menu and test Mara's Love, Trust, and Dominance controls.
- [ ] Visit Shopping Centre during 09:00-13:59 and open Mara's Pet Shop.
- [ ] Visit outside those hours and confirm the shop is unavailable.
- [ ] Test each shop task, passage return, time flow, relationship rewards, and money reward.
- [ ] Confirm each reward appears beneath the narrative on its own separated line.
- [ ] Confirm each stat uses one plus sign, not repeated plus signs for +2 or +3.
- [ ] Confirm money is spaced from the stat feedback and includes a positive sign.
- [ ] Confirm conditional Trust feedback appears exactly when Trust increases.
- [ ] Test Browse, private collection threshold, romance threshold, and Handler proposal threshold.
- [ ] Visit Danube Street and confirm the Mara house event enters the work event pool.
- [ ] Test each house task and its money/stat rewards.
- [ ] Enable Blind Stats and confirm relationship notices are hidden while stats still update.

## Negative stat display pattern

No current Mara work task reduces relationships. When a future choice does reduce a stat, use the corresponding native negative macro, such as `llove Mara`, `ltrust`, or `ldom Mara`. Confirm that the minus indicator appears in the expected red styling.

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
