# v0.1.6 runtime test plan

The v0.1.5 base and location features have been confirmed by the user in-game. v0.1.6 compiles and both patch paths apply. The newly integrated NPC UI and save migration require browser tests.

## New game / first meetings

- [ ] Start a new game and confirm Mara is registered but does not appear as a met relationship before meeting her.
- [ ] Meet Mara at the pet shop and confirm her named-NPC record initializes.
- [ ] Meet Mara through the Danube house encounter and confirm it routes through the intro passage and sets metHouse.
- [ ] Confirm black hair and female pronouns are retained.

## Status and schedule

- [ ] Test 08:59, 09:00, 13:59, and 14:00.
- [ ] Confirm statusCheck routes Mara to the shop or home consistently.
- [ ] Confirm the house shows "No one is home. Mara is at the shop." during shop hours.
- [ ] Confirm the shop directs the player to Danube Street when Mara is home.
- [ ] Confirm the Danube random introduction does not appear while Mara is at the shop.

## Social / character screen

- [ ] Open Social after meeting Mara.
- [ ] Confirm Mara appears under Primary Relationships.
- [ ] Confirm Love, Trust, and Dominance display with the correct icons/ranges.
- [ ] Confirm other NPCs do not display Trust merely because Trust was added to the shared stat list.

## Attitudes / Love Interest

- [ ] Meet the Love/Trust threshold and complete Mara's romance confession.
- [ ] Confirm acceptance calls the vanilla Love Interest assignment flow.
- [ ] Open Attitudes and confirm Mara is selectable.
- [ ] Select Mara and confirm primary/secondary/tertiary assignment works.
- [ ] Re-enter the accepted passage via history and confirm it does not add Mara a second time.
- [ ] Run debugUnlockAllLoveInterests and confirm Mara unlocks without errors.

## Journal

- [ ] Open Journal after meeting Mara.
- [ ] Confirm first-meeting, work count, private collection, romance, and Handler status are reflected accurately.

## Existing v0.1.5 save migration

- [ ] Make a copy of a working v0.1.5 save where Mara has met flags and non-zero relationship/work values.
- [ ] Load the copy in v0.1.6.
- [ ] Confirm Mara's named-NPC init becomes 1.
- [ ] Confirm Love, Trust, Dominance, appearance, pronouns, work counters, and romance/Handler flags are preserved.
- [ ] Save, reload, and confirm the same values persist.

## Regression

- [ ] Existing shop/house work options and rewards still work.
- [ ] Reward-line spacing and Blind Stats behaviour remain unchanged.
- [ ] Pet Shop stays in the original Shopping Centre row with its icon and leave icon.