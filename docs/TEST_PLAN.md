# Mara runtime test plan

The user confirmed that the v0.1.0 base mod works in-game. The v0.1.1 and v0.1.2 stat feedback updates and v0.1.3 persistent locations compiled. v0.1.4 adds a daily shop/home schedule using Mara's established 09:00-14:00 shop hours. Compilation and patch application have been verified; scheduled presence still needs in-game confirmation.

## Shop hours: 09:00-13:59

- [ ] Open Shopping Centre and enter Mara's Pet Shop.
- [ ] Confirm Mara is present and interactive.
- [ ] Confirm all shop work options are available.
- [ ] Visit Mara's home on Danube Street.
- [ ] Confirm the exact message: "No one is home. Mara is at the shop."
- [ ] Confirm no housework or personal interaction options are shown while she is away.
- [ ] Confirm the random first-house introduction does not appear while she is working at the shop.

## Home hours: 14:00-08:59

- [ ] Visit Mara's home on Danube Street.
- [ ] Confirm Mara is present and offers housework.
- [ ] Visit Mara's Pet Shop.
- [ ] Confirm the exact message: "Mara isn't at the shop right now. She's at home on Danube Street."
- [ ] Confirm the link to visit Mara at home works.
- [ ] Confirm shop interactions and work options are not shown while she is home.

## First meeting paths

- [ ] Meet Mara first at the shop during shop hours.
- [ ] Confirm both location links become available after the introduction.
- [ ] Alternatively, meet Mara first at her house outside shop hours.
- [ ] Confirm both location links become available after the introduction.
- [ ] Confirm the initial house encounter is not available while Mara is at the shop.

## Schedule boundaries

- [ ] Test 08:59: Mara is at home.
- [ ] Test 09:00: Mara is at the shop.
- [ ] Test 13:59: Mara is at the shop.
- [ ] Test 14:00: Mara is at home.

## Regression

- [ ] Confirm shop and house work rewards are unchanged.
- [ ] Confirm reward-line spacing and stat indicators remain unchanged.
- [ ] Save and reload, confirming the two meeting flags persist.
- [ ] Confirm that completing a task that crosses a schedule boundary does not lose its reward.