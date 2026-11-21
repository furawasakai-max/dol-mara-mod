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
- Ocean Breeze Cafe: randomly available from 17:00-18:59, with a 40% daily chance after the player has met her.
- Danube Street home: 14:00-08:59 when she is not at the cafe.

The cafe roll is stored in $daily.mara.cafePresent and is not rerolled by revisiting locations. When she leaves the cafe, $daily.mara.cafeDeparted keeps her at home for the rest of that day.

## Evening cafe conversations

The cafe interaction now follows the general random-topic pattern used by Avery's mansion conversations. The player sees one action, "Sit and chat with Mara (0:30)". After 30 minutes, the game randomly selects one of three subjects: pets, the player's life, or the weather. The player is not shown a subject menu.

Each completed conversation grants +1 Mara Love and +1 Mara Trust. After the chat, there is a 25% chance Mara says goodbye and heads home. She also leaves automatically when the time reaches 19:00. A full 30-minute chat is not offered after 18:30. Continuing to chat starts another 30-minute interaction and rolls a new topic.

The number of completed cafe conversations is stored in $mara.cafeChats and displayed in the Journal. The cafe schedule, goodbye logic, and save-data structure are unchanged by v0.1.9.

## House-work tea break

After each of Mara's three housework tasks, there is a 20% chance per task attempt for Mara to offer a short rest, limited to once per in-game day. Accepting takes 10 minutes, shows Mara bringing tea and biscuits, reduces Stress by 6 and Tiredness by 4, and adds 1 Mara Love. The player then returns to the same task's completion passage; normal task rewards are applied once. Declining adds no time or rest effects.

## Relationship and UI integration

Mara is registered as a Love Interest through the vanilla Attitudes eligibility and loveInterestAdd flow. She appears in Social's Primary Relationships after being met, with Love, Trust, and Dominance. The Journal records her shop/home progress, housework breaks, cafe conversations, private collection, romance, and Handler relationship.

## Save compatibility

No new save fields are introduced by v0.1.9. Existing v0.1.8 saves retain their cafe chat count and progression.

## Relevant source files

- game/04-Variables/variables-maraUpdate.twee: random cafe topic selection and conversation passages.
- game/03-JavaScript/named-npc.js: shared Mara status and shop/home/cafe schedule.
- game/base-system/overlays/journal.twee: Mara Journal and cafe conversation count.
- game/overworld-town/loc-cafe/main.twee: random evening Approach Mara link.
- game/overworld-town/loc-shop/main.twee and loc-danube-homes/work.twee: cafe absence notices.
- game/03-JavaScript/ingame.js and game/base-system/attitudes.twee: Love Interest eligibility and assignment.
- game/base-system/overlays/social.twee: Mara's relationship panel.

## Not included

Custom portraits/sprites, dedicated combat behaviour, and specific sex-scene hooks are not implemented in v0.1.9. The vanilla persistent-npcs.twee file remains untouched because it manages generated NPC persistence, whereas Mara is a named NPC.