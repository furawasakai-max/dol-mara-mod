# Mara Love Interest

## Named-NPC registration

Mara is registered through the vanilla named-NPC structures:

- setup.NPCNameList and $NPCNameList
- setup.loveInterestNpc
- setup.loveAlias
- the aligned named-NPC metadata arrays in npcNamed.twee
- the Mara migration entry in updateNewNamedNpcs

The NPC uses the existing C.npc.Mara record. Its relationship values are Love, Lust, Trust, and Dominance. Mara's current work events principally increase Love, with conditional Trust and Dominance gains.

## Location and schedule

Mara's schedule is centralised in maraSchedule() in game/03-JavaScript/named-npc.js and exposed through the named-NPC statusCheck() switch.

- Pet shop: 09:00-13:59.
- Danube Street home: 14:00-08:59.

The shop and house passages use the shared status check. After the first meeting, both locations remain discoverable, but interaction is limited to her current location.

## Relationship and event progression

- Shop and house work increase Love.
- Selected tasks grant Trust after Mara's Love reaches 50.
- Shop tasks also increase Dominance.
- Trust unlocks the private collection scene.
- Love 100 and Trust at least 50 unlock the romance confession.
- Accepting the confession sets the romance flag and registers Mara through the vanilla loveInterestAdd widget.
- The Handler/Pet proposal requires romance, Trust greater than 70, and Dominance at least 100.

## UI integration

Mara appears in the Social overlay's Primary Relationships after the player has met her. Her relationship panel displays Love, Trust, and Dominance. Trust is configured for Mara only, so the global Social stat list does not expose Trust for unrelated NPCs.

The Journal has a Mara section describing her shop schedule, house/work progress, private collection, romance, and Handler relationship.

## Save compatibility

The v0.1.6 initialiser sets objectVersion.mara to 2. Older alpha saves that have met Mara but have not yet initialised her named-NPC record are migrated through the vanilla initnpc widget. The migration restores saved relationship, body, pronoun, appearance, state, clothes, and other stored fields after initialisation.

Test this with a copy of an existing v0.1.5 save. Do not use the only copy of an important save.

## Vanilla source integration map

- game/04-Variables/variables-static.twee: name and Love Interest registration.
- game/04-Variables/npcNamed.twee: metadata arrays, NPC defaults, appearance defaults, and migration.
- game/03-JavaScript/named-npc.js: statusCheck(), maraStatusCheck(), and maraSchedule().
- game/03-JavaScript/ingame.js: isPossibleLoveInterest().
- game/base-system/named-npcs.twee: NPC increment whitelist, initialization, and outfit setup.
- game/base-system/attitudes.twee: Love Interest assignment and debug unlock.
- game/base-system/widgets.twee: relationship clamps and Social stat display configuration.
- game/base-system/overlays/social.twee: Primary Relationships registration.
- game/base-system/overlays/journal.twee: Mara Journal section.
- game/04-Variables/variables-maraUpdate.twee: Mara state and event passages.
- game/04-Variables/variables-versionUpdate.twee: migration call.
- game/overworld-town/loc-shop/main.twee and loc-danube-homes/work.twee: shop/house events and interaction.

## Not included yet

Custom portraits/sprites, dedicated combat behaviour, and specific sexual-scene hooks are not implemented in v0.1.6. The vanilla persistent-npcs.twee file is not modified because it handles generated NPC persistence rather than Mara's named-NPC record.