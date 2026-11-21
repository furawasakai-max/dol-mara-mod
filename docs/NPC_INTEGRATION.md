# Mara NPC integration map (v0.1.16)

This release corrects the night-cage dawn test and expands the failed-lockpick discipline scene. Named-NPC registration, schedule, shop, cafe, pet-room activities, and relationship integration remain unchanged.

| Subsystem | Implementation |
|---|---|
| Night-cage lockout | Stores the next 07:00 release as an absolute DateTime timestamp. |
| Dawn check | The punishment return compares `Time.date.timeStamp` with `nightCageCaughtUntil`; it no longer uses `Time.hour >= 7`, which incorrectly matched 22:00 and 23:00. |
| Tool selection | Failed lockpick selects either whip or cane for the night scene. |
| Restraint scene | Padded X-frame, broad-lined cuffs, and the existing stop signal. |
| Discipline structure | Three rounds with 5, 6, and 3 described strokes. Each round applies one guarded `masopain 15` effect. |
| Timing | Full route totals 60 minutes: 5-minute escort, 20 + 20 + 10-minute rounds, and 5-minute return. |
| Stop flow | Player can stop before or between rounds; Mara releases them and returns them to the still-locked cage if before 07:00. |
| Dawn release | At or after the stored 07:00 timestamp, Mara unlocks the cage and detaches the lead. |
| Save compatibility | No new fields; `objectVersion.mara` remains 10. |

Only `game/04-Variables/variables-maraUpdate.twee` changes in the v0.1.16 incremental patch.