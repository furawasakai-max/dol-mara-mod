# Mara runtime test plan

The user confirmed that the v0.1.0 base mod works in-game. The v0.1.1 and v0.1.2 stat-feedback updates compiled. The v0.1.3 persistent-availability update also compiles and its full patch applies to a clean 0.5.13.8 source tree. The new dialogue and access flow still need in-game confirmation.

## New save and first meetings

- [ ] Start a new game and confirm Mara appears in the named-NPC system.
- [ ] Open Shopping Centre during 09:00-13:59 and meet Mara at the pet shop.
- [ ] Confirm the first shop dialogue naturally invites the player to help.
- [ ] Knock on Danube Street houses until Mara's first house encounter appears.
- [ ] Confirm the first house dialogue naturally invites the player to help.
- [ ] Confirm both introductions lead to their existing work choices and preserve rewards.

## Persistent shop access

- [ ] After meeting Mara at the shop, leave and return to Shopping Centre outside 09:00-14:00.
- [ ] Confirm the Mara's Pet Shop link remains visible.
- [ ] Enter the pet shop outside normal hours and confirm Mara welcomes the player back.
- [ ] Open Help Mara with the shop and confirm all three work options remain available.
- [ ] Complete each task and verify time, money, Love, conditional Trust, and Dominance behave as before.

## Persistent house access

- [ ] After meeting Mara at her house, return to Danube Street.
- [ ] Confirm a permanent Mara's home link appears in Places of interest.
- [ ] Open it during day and at night and confirm Mara is available.
- [ ] Confirm her return dialogue welcomes the player and offers housework.
- [ ] Select Help Mara with the house and verify all existing work options and rewards remain unchanged.
- [ ] Choose Just stop by to say hello and confirm return to Danube Street.

## Stat feedback

- [ ] Confirm rewards appear beneath the narrative with clear spacing.
- [ ] Confirm each stat uses one sign, not repeated plus signs for +2 or +3.
- [ ] Confirm money is separated from stat feedback and displays as a positive amount.
- [ ] Confirm conditional Trust feedback appears only when Trust increases.
- [ ] Enable Blind Stats and confirm relationship notices are hidden while stats still update.

## Existing save

- [ ] Back up a save that has already met Mara at both the shop and the house.
- [ ] Load it in v0.1.3 and confirm both visit locations remain available.
- [ ] Confirm Love, Trust, Dominance, work counters, and event flags are preserved after saving and reloading.

## Known scope gaps

- The shop is a passage linked from Shopping Centre, not an independent map node.
- The alpha has fixed work choices, not a full random shift/event system.
- The private collection is an introductory scene, not a complete equipment mechanic.
- No custom art is included.