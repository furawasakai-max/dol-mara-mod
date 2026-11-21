# Mara NPC integration map (v0.1.7)

This release builds on the vanilla named-NPC integration in v0.1.6 and adds one house-work interruption event.

| Subsystem | Implementation |
|---|---|
| Named NPC data | Mara remains in `$NPCName` / `$NPCNameList` with named-NPC defaults and versioned initialization. |
| Status / schedule | `maraSchedule()` and `maraStatusCheck()` join the existing `statusCheck()` switch. |
| Love Interest | `isPossibleLoveInterest()` and vanilla `loveInterestAdd` connect Mara to Attitudes. |
| Social panel | Mara appears in Primary Relationships after meeting her; Trust display is limited to Mara. |
| Journal | Shows house/shop progress and accepted tea-break count. |
| Housework event | `maraHouseworkBreakCheck` gives a 20% chance during each of three Mara housework tasks, with a once-per-day limit. |
| Break effects | Accepting takes 10 minutes, applies the tea prop, reduces Stress by 6 and Tiredness by 4, and increases Mara Love by 1. |
| Save compatibility | `maraInit` defaults `restBreaks` on old saves and sets `objectVersion.mara` to 3. |

The event uses the vanilla Farm Pigs Feed Nausea work-interruption structure as a reference, but it does not reuse pregnancy or nausea conditions. The vanilla `persistent-npcs.twee` remains untouched because Mara is a named NPC, not a generated NPC.