# Mara NPC integration map (v0.1.12)

This update changes only pet-room interaction passages and the Mara home greeting. Named-NPC registration, schedule, shop, cafe, and relationship integration remain unchanged.

| Subsystem | Implementation |
|---|---|
| Cushion wait | Ten-minute wait has a 40% chance to roll one of seven random pet-play orders. |
| Cushion order pool | Paw, Down/Stay, Come, Fetch, Grooming, Place, and short Heel follow. Player can end the wait instead. |
| Daily training | Once-per-day session selects one of seven random lessons. |
| Training lesson pool | Basic obedience, Heel, Paw, Fetch, Place, Grooming Manners, and Settle. |
| Leash handling | Uses vanilla leash widgets; lead remains slack in narrative and is detached on completion and stop. |
| Rewards | Successful training grants +2 Mara Dominance and +1 Mara Trust. Stopping has no completion reward. |
| Aftercare | Water, a comfort check, and a short transition out of role are included at the end of training. |
| Save compatibility | No new persistent fields; `objectVersion.mara` advances to 8. |

Only `variables-maraUpdate.twee` and `loc-danube-homes/work.twee` are changed by the v0.1.12 incremental patch.