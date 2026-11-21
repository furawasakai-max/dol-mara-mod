# Mara v0.1.12 runtime test plan

The source compiles. The incremental patch applies to v0.1.11 with zero rejects; the cumulative patch applies to clean vanilla 0.5.13.8 with zero rejects, and the full-patch verification tree compiles. In-game verification remains necessary.

## Cushion random order

- [ ] Load a save with `petRulesEstablished` true.
- [ ] Enter Mara's pet room and use Wait on the cushion.
- [ ] Confirm the passage advances ten minutes.
- [ ] Repeat across multiple waits and confirm roughly 40% trigger a random order over a sufficiently large sample.
- [ ] Confirm triggered orders include Paw, Down/Stay, Come, Fetch, Grooming, Place, and Heel.
- [ ] Confirm each order is short and does not require prolonged crawling.
- [ ] Confirm following the order takes another five minutes and returns to the pet room.
- [ ] Confirm End waiting returns to the pet room without triggering the action.
- [ ] Confirm no-order waits finish normally and mention Mara checking comfort.

## Random daily training

- [ ] Begin training and confirm one of seven lessons is selected at random.
- [ ] Repeat in separate test saves/days to see all seven: basic obedience, Heel, Paw, Fetch, Place, Grooming Manners, Settle.
- [ ] Confirm the lead attaches only when the collar can accept it and remains slack during movement.
- [ ] Confirm the player can stop in the lesson passage and the lead is detached.
- [ ] Confirm stopping gives no Dominance/Trust completion reward.
- [ ] Confirm completion grants exactly +2 Dominance and +1 Trust.
- [ ] Confirm training cannot be started again that in-game day once a session has begun.
- [ ] Confirm the session ends with the lead removed, water offered, and a comfort check.

## Safety and regression

- [ ] Confirm all crawl sequences are brief and take place on the soft mat/rug/cushion.
- [ ] Confirm Mara does not pull the player by the collar or neck.
- [ ] Test an existing cursed neck item and confirm training code does not overwrite it.
- [ ] Confirm the cushion and training event options remain separate from cage sleep and the pet bowl.
- [ ] Confirm the pet bowl, cage sleep, housework, and house-leave outfit restoration still work.
- [ ] Confirm non-pet house visits and previous reward values remain unchanged.
- [ ] Confirm cafe random topics and the v0.1.10 rules scene are unaffected.

## Save compatibility

- [ ] Load a v0.1.11 save and confirm Mara progression is preserved.
- [ ] Confirm `objectVersion.mara` advances to 8.
- [ ] Confirm no new persistent save fields are required.