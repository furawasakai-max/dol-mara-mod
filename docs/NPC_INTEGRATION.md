# Mara NPC integration map (v0.1.13)

This update adds the discipline-room destination and events to Mara's established pet-room hub. Named-NPC registration, schedule, shop, cafe, relationship integration, and previous pet-play activities remain unchanged.

| Subsystem | Implementation |
|---|---|
| Pet-room hub | Adds the Visit Mara's discipline room link. |
| Random offer | First visit each in-game day rolls once; 35% chance to offer a session. |
| Instrument choice | Player can choose the whip or cane after the offer. |
| Restraint scene | Uses a padded X-frame, broad lined cuffs, and an agreed stop word/signal. Discipline is implied/non-graphic. |
| Stop flow | Stop link is available before and during the session; stopping releases the player and gives no reward. |
| Masochism reward | Completion of either tool session adds +20 to the vanilla `$masochism` progress value. |
| Save compatibility | No new persistent fields. Daily state stores the room roll; `objectVersion.mara` advances to 9. |

The v0.1.13 incremental patch changes only `game/04-Variables/variables-maraUpdate.twee`. The cumulative full patch includes 17 source files and applies to clean vanilla 0.5.13.8.