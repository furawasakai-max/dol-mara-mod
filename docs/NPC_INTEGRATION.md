# Mara NPC integration map (v0.1.15)

This update adds a night-only cage routine to the established pet house. Named-NPC registration, schedules, shop, cafe, relationship integration, daytime pet-room activities, and prior rewards remain unchanged.

| Subsystem | Implementation |
|---|---|
| Night trigger | When the player remains in Mara's house at or after 22:00 and before 07:00, the pet-room menu routes to the locked cage. |
| Cage | Reuses the existing cushioned cage sleep point. |
| Lockpick gate | The option appears only at Skulduggery 400 or above; the native check uses difficulty 700. |
| Success | Unlocks the cage and lets the player leave through the existing house-leave path. |
| Failure | Makes noise, brings Mara to the room, and stores a caught-until timestamp for the next 07:00. |
| Discipline | Failure routes to a one-hour non-graphic dungeon reprimand, followed by a lead attachment and return to the cage. |
| Relock | Cage remains locked after the return until 07:00. If the hour crosses 07:00, the cage is opened immediately. |
| Sleep | Uses vanilla sleep and wake effects, then advances the remaining time to exactly 07:00. |
| Dawn | Mara unlocks the cage at 07:00 and removes the lead if attached. |
| Save compatibility | Adds `nightCageCaughtUntil` migration and advances `objectVersion.mara` to 10. |

Only `game/04-Variables/variables-maraUpdate.twee` is changed by the v0.1.15 incremental patch.