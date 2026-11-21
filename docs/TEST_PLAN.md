# Mara v0.1.17 runtime test plan

The v0.1.17 source compiles. The incremental patch applies to v0.1.16 with zero rejects; the cumulative full patch applies directly to clean vanilla 0.5.13.8, and the clean full-patch tree compiles. In-game verification remains outstanding.

## Mara availability

- [ ] Visit Mara's house between 09:00 and 13:59. Confirm the house page states that Mara is at the shop and is unavailable for house activities.
- [ ] Confirm an established pet player can enter the empty house and stay; a player without the pet-house arrangement cannot use the new stay flow.
- [ ] Visit Mara's house between 17:00 and 18:59 on a cafe day. Confirm the house page states that Mara is at Ocean Breeze Cafe and is unavailable for house activities.
- [ ] Confirm the empty-house flow hides the cushion, bowl, cage sleep, command training, and discipline-room interaction while Mara is out.
- [ ] Confirm the player can still leave the house.

## Pre-departure order: pet shop

- [ ] At 07:00-08:59, visit Mara when she is home and confirm the option to stay while she goes to the pet shop.
- [ ] Choose it and confirm Mara assigns one of the three greeting positions at random.
- [ ] Confirm the stated return time is 14:00.
- [ ] Choose each of the three actual waiting positions in separate test saves.
- [ ] Confirm the wait advances to 14:00 and the return check runs.

## Pre-departure order: cafe

- [ ] At 14:00-16:59, choose the cafe stay option.
- [ ] On a successful cafe roll, confirm Mara assigns a random position and the return is scheduled for 19:00.
- [ ] On a failed cafe roll, confirm Mara stays home, no away assignment is created, and the existing daily roll remains false for the 17:00 schedule.
- [ ] Confirm the daily cafe roll is shared with the existing cafe schedule and cannot be rerolled by revisiting.

## Position and return check

- [ ] Confirm the random order can be front door, cushioned cage, or discipline room.
- [ ] Choose the matching place and confirm Mara finds the player there without a punishment event.
- [ ] Choose a different place and confirm Mara notices the mismatch and initiates the discipline-room reprimand.
- [ ] Leave the house during an active order and confirm the actual position is marked absent.
- [ ] Return after Mara's scheduled return and confirm the absent/wrong-position punishment is triggered.
- [ ] Save/reload while the assignment is active and confirm expected place and return time persist.

## Reprimand

- [ ] Confirm Mara randomly chooses whip or cane.
- [ ] Confirm the route totals 60 minutes when completed: five-minute escort, three 15-minute rounds, and ten-minute return.
- [ ] Confirm each round applies `masopain 10` only once, including across save/reload.
- [ ] Confirm the stop option appears before and between rounds, releases the player, and ends the session early.
- [ ] Confirm all waiting and punishment state is cleared when the player returns to the pet room.

## Outfit and regression

- [ ] On the empty-house notice, choose to leave without entering and confirm clothing is not changed.
- [ ] Enter the empty house and confirm the pet-house outfit and collar are applied.
- [ ] Leave the house and confirm the stored clothes/neckwear are restored.
- [ ] Confirm the 22:00 locked-cage routine and 07:00 unlock are unchanged.
- [ ] Confirm daytime cushion orders, pet bowl, cage sleep, command training, discipline room, optional housework, and cafe conversations remain unchanged.
- [ ] Load a v0.1.16 save and confirm Mara progression is preserved and `objectVersion.mara` advances to 11.