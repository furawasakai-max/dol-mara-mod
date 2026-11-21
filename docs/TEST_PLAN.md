# Mara v0.1.8 runtime test plan

The source compiles. The incremental v0.1.7 upgrade patch and cumulative clean-install patch both apply with zero rejects and reproduce the working source files byte-for-byte. JavaScript syntax checks and schedule-function tests passed. Browser testing is still required.

## Random cafe appearance

- [ ] Meet Mara at her shop or home first.
- [ ] Visit Ocean Breeze Cafe before 17:00 and confirm the Mara interaction is not offered.
- [ ] Enter the cafe between 17:00 and 18:59 and check whether Mara is present.
- [ ] If she is present, confirm the Approach Mara link appears.
- [ ] If she is absent, leave and re-enter several times and confirm the result does not reroll that evening.
- [ ] On another in-game day, check again and confirm a fresh daily roll occurs.
- [ ] Confirm Mara does not make a cafe appearance before the player has met her at the shop or home.
- [ ] Confirm she is no longer available at the cafe at 19:00.

## Cafe conversation topics

- [ ] Select Talk about pets (0:30). Confirm the scene mentions adorable pets, especially kittens.
- [ ] Select Ask about your life (0:30). Confirm Mara asks how the player's life has been and listens.
- [ ] Select Chat about the weather (0:30). Confirm the casual weather dialogue appears.
- [ ] For each topic, confirm exactly 30 minutes pass.
- [ ] For each completed chat, confirm Mara Love increases by 1 and Trust increases by 1.
- [ ] Confirm the reward display shows the correct positive stat indicators.
- [ ] Confirm the Journal cafe conversation count increments once per completed conversation.

## Goodbye and departure

- [ ] After a completed chat, observe the 25% chance that Mara decides to head home.
- [ ] When she says goodbye, confirm she is marked as having left for the day.
- [ ] Return to Ocean Breeze Cafe after the goodbye and confirm the Approach Mara link is gone.
- [ ] Confirm the player can visit Mara at home after her departure.
- [ ] Confirm a full 30-minute chat is not offered after 18:30.
- [ ] Confirm a chat that ends at 19:00 triggers the automatic goodbye.

## Location schedule regression

- [ ] While Mara is at the cafe, visit her home and confirm it says she is at Ocean Breeze Cafe.
- [ ] While Mara is at the cafe, visit her shop and confirm it says she is at Ocean Breeze Cafe.
- [ ] Confirm neither location offers housework or shop interactions while she is at the cafe.
- [ ] Confirm shop hours (09:00-13:59) and the normal home schedule remain unchanged.

## Save migration and regression

- [ ] Load a copy of a v0.1.7 save with Mara's existing stats and flags.
- [ ] Confirm the v0.1.8 initializer adds cafeChats = 0 without resetting Love, Trust, Dominance, work progress, or event flags.
- [ ] Complete a cafe conversation, save, reload, and confirm the Journal count persists.
- [ ] Confirm housework tea breaks, shop work, and existing rewards still work.