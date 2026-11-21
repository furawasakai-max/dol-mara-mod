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

The cafe interaction follows the general random-topic pattern used by Avery's mansion conversations. The player sees one action, "Sit and chat with Mara (0:30)". After 30 minutes, the game randomly selects one of three subjects: pets, the player's life, or the weather. The player is not shown a subject menu.

Each completed conversation grants +1 Mara Love and +1 Mara Trust. After the chat, there is a 25% chance Mara says goodbye and heads home. She also leaves automatically when the time reaches 19:00. A full 30-minute chat is not offered after 18:30. Continuing to chat starts another 30-minute interaction and rolls a new topic.

The number of completed cafe conversations is stored in $mara.cafeChats and displayed in the Journal.

## Handler/Pet house routine

The existing Handler/Pet proposal and its unlock requirements are unchanged. After the player accepts it, a later visit to Mara's house offers a second confirmation. If the player agrees again, Mara's dialogue shifts from cheerful to firm and authoritative. She orders the player to undress, wear her black leather collar, crawl on all fours, and wait while she inspects the collar fit, posture, and response to instructions.

Mara then states four rules for the time spent inside her home:

1. The player speaks only when Mara permits it.
2. The player stays naked and collared while inside Mara's house.
3. The player follows Mara's instructions.
4. Breaking the rules or disobeying Mara results in punishment, within the boundaries agreed to by both characters.

The player can defer the second confirmation or stop before the collar scene. After the rules are established, later house visits automatically apply the house outfit. The player's previous clothes and neckwear are stored on entry and restored when leaving. A neck item marked cursed by vanilla cannot be replaced, so an already-locked neck item remains in place.

## House-work tea break

After each of Mara's three housework tasks, there is a 20% chance per task attempt for Mara to offer a short rest, limited to once per in-game day. Accepting takes 10 minutes, shows Mara bringing tea and biscuits, reduces Stress by 6 and Tiredness by 4, and adds 1 Mara Love. The player then returns to the same task's completion passage; normal task rewards are applied once. Declining adds no time or rest effects.

## Relationship and UI integration

Mara is registered as a Love Interest through the vanilla Attitudes eligibility and loveInterestAdd flow. She appears in Social's Primary Relationships after being met, with Love, Trust, and Dominance. The Journal records her shop/home progress, housework breaks, cafe conversations, private collection, romance, and Handler relationship.

## Save compatibility

v0.1.10 adds three Mara fields: petRulesEstablished, petHouseDressed, and petNeckWasNaked. They are initialized without resetting existing Mara progress. objectVersion.mara advances to 6.

## Relevant source files

- game/04-Variables/variables-maraUpdate.twee: Mara initialization, relationship, cafe, and pet-house passages.
- game/03-JavaScript/named-npc.js: shared Mara status and shop/home/cafe schedule.
- game/base-system/overlays/journal.twee: Mara Journal and activity counters.
- game/overworld-town/loc-cafe/main.twee: random evening Ocean Breeze Cafe approach.
- game/overworld-town/loc-danube-homes/work.twee: Mara's house visits, work tasks, and pet-house entry/exit.
- game/03-JavaScript/ingame.js and game/base-system/attitudes.twee: Love Interest eligibility and assignment.
- game/base-system/overlays/social.twee: Mara's relationship panel.

## Not included

Custom portraits/sprites, dedicated combat behaviour, and specific sex-scene hooks are not implemented. The vanilla persistent-npcs.twee file remains untouched because Mara is a named NPC, not a generated NPC.