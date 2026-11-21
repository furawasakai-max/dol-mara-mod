# Mara NPC integration map (v0.1.8)

This release builds on the vanilla named-NPC integration in v0.1.6 and adds an evening cafe schedule and three repeatable conversation topics.

| Subsystem | Implementation |
|---|---|
| Named NPC data | Mara remains in $NPCName / $NPCNameList with named-NPC defaults and versioned initialization. |
| Status / schedule | maraSchedule() and maraStatusCheck() use the vanilla statusCheck() flow. Mara can be at the shop, home, or Ocean Breeze Cafe. |
| Love Interest | isPossibleLoveInterest() and vanilla loveInterestAdd connect Mara to Attitudes. |
| Social panel | Mara appears in Primary Relationships after meeting her; Trust display is limited to Mara. |
| Journal | Tracks work, accepted housework tea breaks, and completed cafe conversations. |
| Housework event | A once-per-day 20% tea-break interruption can occur during Mara housework. |
| Cafe presence | After meeting Mara, a stable 40% daily roll may place her at Ocean Breeze between 17:00 and 18:59. |
| Cafe conversations | Three 30-minute chat topics each grant +1 Love and +1 Trust. |
| Departure | After each chat, Mara has a 25% chance to say goodbye and return home. She also leaves automatically at 19:00. |
| Save compatibility | maraInit defaults cafeChats on old saves and advances objectVersion.mara to 5. |

The cafe appearance roll and departure flag use $daily.mara, so the result remains stable for the in-game day. The cafe event is not available until the player has met Mara at her shop or home. The vanilla persistent-npcs.twee remains unchanged because Mara is a named NPC, not a generated NPC.