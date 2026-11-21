# Mara Love Interest

## Named-NPC registration

Mara is registered through the vanilla named-NPC structures:

- setup.NPCNameList and $NPCNameList
- setup.loveInterestNpc
- setup.loveAlias
- the aligned named-NPC metadata arrays in npcNamed.twee
- the Mara migration entry in updateNewNamedNpcs

The NPC uses the existing C.npc.Mara record. Its relationship values are Love, Lust, Trust, and Dominance.

## Location and schedule

Mara's schedule is centralised in maraSchedule() in game/03-JavaScript/named-npc.js and exposed through the named-NPC statusCheck() switch.

- Pet shop: 09:00-13:59.
- Danube Street home: 14:00-08:59.

The shop and house passages use the shared status check. After the first meeting, both locations remain discoverable, but interaction is limited to her current location.

## House-work rest break (v0.1.7)

After each completed house-work task (Organize Pet Supplies, Clean Animal Equipment, or Prepare Food Supplies), Mara has a 25% chance to notice the player's effort and suggest a short rest. She makes two cups of tea and sits with the player.

- Accepting the tea applies the vanilla tea prop, reduces Stress by 6, and adds 1 Mara Love.
- Declining simply ends the visit; it does not apply tea or relationship effects.
- The completed task's money and normal relationship rewards are unchanged.
- The break is part of the completed work visit and adds no separate time cost.
- Accepted breaks are counted in $mara.restBreaks and shown in the Mara Journal section.

## Relationship and event progression

- Shop and house work increase Love.
- Selected tasks grant Trust after Mara's Love reaches 50.
- Shop tasks also increase Dominance.
- Trust unlocks the private collection scene.
- Love 100 and Trust at least 50 unlock the romance confession.
- Accepting the confession registers Mara through the vanilla loveInterestAdd widget.
- The Handler/Pet proposal requires romance, Trust greater than 70, and Dominance at least 100.

## UI integration

Mara appears in the Social overlay's Primary Relationships after the player has met her. Her relationship panel displays Love, Trust, and Dominance. Trust is configured for Mara only.

The Journal has a Mara section describing her shop schedule, house/work progress, accepted tea breaks, private collection, romance, and Handler relationship.

## Save compatibility

The v0.1.6 initializer sets objectVersion.mara to version 2 and later v0.1.7 raises it to version 3. Older saves receive a default restBreaks value of zero without replacing their Mara record. The field persists as part of $mara.

Test this with a copy of an existing v0.1.6 save. Do not use the only copy of an important save.

## Source integration map

- game/04-Variables/variables-static.twee: name and Love Interest registration.
- game/04-Variables/npcNamed.twee: metadata arrays, NPC defaults, and migration.
- game/03-JavaScript/named-npc.js: statusCheck(), maraStatusCheck(), and maraSchedule().
- game/03-JavaScript/ingame.js: isPossibleLoveInterest().
- game/base-system/attitudes.twee: Love Interest assignment and debug unlock.
- game/base-system/overlays/social.twee: Primary Relationships registration.
- game/base-system/overlays/journal.twee: Mara Journal section, including tea-break count.
- game/04-Variables/variables-maraUpdate.twee: Mara state, rest-offer widget, tea passage, and relationship passages.
- game/overworld-town/loc-danube-homes/work.twee: first meeting, house work, and rest-offer hooks.
- game/overworld-town/loc-shop/main.twee: shop availability, dialogue, and shop tasks.

## Not included yet

Custom portraits/sprites, dedicated combat behaviour, and specific sexual-scene hooks are not implemented in v0.1.7. The vanilla persistent-npcs.twee file remains unchanged because it handles generated NPC persistence rather than Mara's named-NPC record.