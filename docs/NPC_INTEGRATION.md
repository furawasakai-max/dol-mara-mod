# Mara NPC integration map (v0.1.9)

This release retains the vanilla named-NPC integration and changes only the player-facing cafe conversation selection.

| Subsystem | Implementation |
|---|---|
| Named NPC data | Mara remains in $NPCName / $NPCNameList with named-NPC defaults and versioned initialization. |
| Status / schedule | maraSchedule() and maraStatusCheck() use the vanilla statusCheck() flow. Mara can be at the shop, home, or Ocean Breeze Cafe. |
| Love Interest | isPossibleLoveInterest() and vanilla loveInterestAdd connect Mara to Attitudes. |
| Social panel | Mara appears in Primary Relationships after meeting her; Trust display is limited to Mara. |
| Journal | Tracks work, accepted housework tea breaks, and completed cafe conversations. |
| Cafe presence | After meeting Mara, a stable 40% daily roll may place her at Ocean Breeze between 17:00 and 18:59. |
| Cafe conversation | One 30-minute action automatically selects a random topic: pets, the player's life, or the weather. |
| Conversation rewards | Each completed chat grants +1 Love and +1 Trust and increments the Journal counter. |
| Departure | After each chat, Mara has a 25% chance to say goodbye and return home. She also leaves automatically at 19:00. |

The random cafe topic is selected in the Mara Cafe Conversation passage using the same overall one-action-then-random-topic pattern as Avery's mansion conversations. This release does not change the cafe schedule or save-data structure. The vanilla persistent-npcs.twee remains unchanged because Mara is a named NPC, not a generated NPC.