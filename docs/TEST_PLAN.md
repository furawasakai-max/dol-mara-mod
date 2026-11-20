# Mara runtime test plan

The user confirmed that the v0.1.0 base mod works in-game. v0.1.5 compiles and both incremental and cumulative patches apply with zero fuzz. The Shopping Centre layout should still be checked visually in-game.

## v0.1.5 Shopping Centre layout

- [ ] Open Shopping Centre during normal daytime and confirm there is only one Mara Pet Shop entry.
- [ ] Confirm it appears in the original Pet shop row between Hairdressers and Tattoo parlour.
- [ ] Confirm the entry reads "Mara's Pet Shop (0:01)" and keeps the pet-shop icon.
- [ ] Confirm there is no separate Mara shortcut above the Shopping Centre description.
- [ ] Open the night/exposed shop list and confirm its pet-shop entry also routes to Mara's Pet Shop.
- [ ] Enter Mara's Pet Shop during 09:00-13:59 and confirm Mara is present.
- [ ] Confirm the Leave the shop action has the standard get-out icon.
- [ ] Visit outside 09:00-14:00 and confirm Mara is shown as being at home on Danube Street.
- [ ] Confirm Leave the shop also has the get-out icon on the off-duty/closed view.
- [ ] Confirm the link to visit Mara at home still works.

## Schedule regression

- [ ] Test 08:59: Mara is at home.
- [ ] Test 09:00: Mara is at the shop.
- [ ] Test 13:59: Mara is at the shop.
- [ ] Test 14:00: Mara is at home.
- [ ] Confirm the random first house introduction does not appear while Mara is at the shop.

## Work and save regression

- [ ] Confirm shop and house work options and rewards are unchanged.
- [ ] Confirm reward-line spacing and stat indicators remain unchanged.
- [ ] Save and reload, confirming both meeting flags and relationship values persist.
- [ ] Test an existing save that has already met Mara at one or both locations.