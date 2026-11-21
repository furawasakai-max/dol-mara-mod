# Mara NPC integration map (v0.1.11)

This release keeps Mara's vanilla named-NPC integration and replaces the established pet-house landing page with a pet-room activity hub.

| Subsystem | Implementation |
|---|---|
| Named NPC data | Mara remains in the vanilla named-NPC arrays and uses `C.npc.Mara`. |
| Status / schedule | `maraSchedule()` and `maraStatusCheck()` keep Mara at her shop, home, or Ocean Breeze Cafe according to the existing schedule. |
| Pet-house outfit | `maraPetHousewear` applies the house outfit and collar; `maraPetHouseLeave` restores stored clothing on exit. |
| Pet-room hub | `Mara Danube Pet House` now offers cushion waiting, a bowl meal, cage sleep, command training, optional housework, and leaving. |
| Cushion waiting | Ten-minute wait scene where Mara checks that the player remains on the cushion. |
| Pet bowl | Once-per-day scene; Hunger -500 and Stress -3. |
| Cage sleep | Uses native `generateSleepLinks`, `sleep`, `wakingEffects`, and `sleepeffects` widgets. |
| Command training | Once per day; uses vanilla `leash`, `attach_leash`, and `detach_leash` widgets where supported by the equipped collar. |
| Training rewards | Successful completion grants +2 Mara Dominance, +1 Mara Trust, and increments `petTrainingSessions`. Stopping has no completion reward. |
| Housework | Still available as a separate optional activity. Pet-mode task completion returns to the pet room; non-pet completion keeps the former exit behaviour. |
| Save compatibility | `petTrainingSessions` is initialized for older saves; `objectVersion.mara` advances to 7. |

The incremental v0.1.11 patch changes `variables-maraUpdate.twee` and the Mara section of `loc-danube-homes/work.twee`. It does not change named-NPC registration or the cafe schedule.