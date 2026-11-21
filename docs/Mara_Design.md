# Mara Love Interest

## Named-NPC registration

Mara is registered through the vanilla named-NPC structures:

- setup.NPCNameList and $NPCNameList
- setup.loveInterestNpc
- setup.loveAlias
- aligned named-NPC metadata arrays in npcNamed.twee
- Mara's migration entry in updateNewNamedNpcs

Mara uses the existing C.npc.Mara record, with Love, Lust, Trust, and Dominance relationship values.

## Location and schedule

Mara's schedule is centralised in maraSchedule() in game/03-JavaScript/named-npc.js and exposed through statusCheck().

- Pet shop: 09:00-13:59.
- Danube Street home: 14:00-08:59.

Both locations remain discoverable after the first meeting, but interaction is limited to Mara's current location.

## House-work tea break (v0.1.7)

During each of Mara's three housework tasks, a 20% chance check can interrupt the work and have Mara offer the player a short rest. The event can occur at most once per in-game day.

- Accepting takes 10 minutes, shows Mara bringing tea and biscuits, reduces Stress by 6 and Tiredness by 4, and adds 1 Mara Love.
- After tea, the player returns to the same task's completion passage. The task's regular money and relationship rewards are applied once.
- Declining continues to task completion without extra time or rest effects.
- Accepted breaks are counted in Mara's Journal.
- The event's structure is adapted from the vanilla Farm Pigs Feed Nausea work interruption without its pregnancy/nausea trigger.

## Relationship and UI integration

Mara is registered as a Love Interest through the vanilla Attitudes eligibility and loveInterestAdd flow. She appears in Social's Primary Relationships after being met, with Love, Trust, and Dominance. The Journal records her shop/home progress, accepted tea breaks, private collection, romance, and Handler relationship.

## Save compatibility

maraInit defaults restBreaks to zero in older saves and advances objectVersion.mara to 3. The existing Mara stat and appearance migration remains intact.

## Relevant source files

- game/04-Variables/variables-maraUpdate.twee: Mara save state, initialization, rest-offer widget and tea passage.
- game/base-system/overlays/journal.twee: Mara Journal and accepted-break count.
- game/overworld-town/loc-danube-homes/work.twee: the three housework task interruptions and completion passages.
- game/03-JavaScript/named-npc.js: shared Mara status and schedule.
- game/03-JavaScript/ingame.js and game/base-system/attitudes.twee: Love Interest eligibility and assignment.
- game/base-system/overlays/social.twee: Mara relationship panel.

## Not included

Custom portraits/sprites, dedicated combat behaviour, and specific sexual-scene hooks are not implemented in v0.1.7. The vanilla persistent-npcs.twee file remains untouched because it manages generated NPC persistence, whereas Mara is a named NPC.