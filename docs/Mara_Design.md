# Mara Love Interest

## Mara variables

### NPC registration and relationship stats

- setup.NPCNameList
- setup.loveInterestNpc
- setup.loveAlias
- $NPCNameList
- $NPCName
- C.npc.Mara.love
- C.npc.Mara.trust
- C.npc.Mara.dom

### Save data

- $mara.version
- $mara.metShop
- $mara.metHouse
- $mara.shopHelp
- $mara.houseHelp
- $mara.privateCollectionSeen
- $mara.romanceUnlocked
- $mara.handlerProposalSeen
- $mara.handlerRelationship

## Current implementation

- Mara is registered as an adult female named NPC and Love Interest.
- New saves and existing saves initialize Mara state without resetting her existing relationship values.
- Love, Trust, and Dominance are supported by the NPC increment/clamp logic and Cheat Menu.
- Her first Danube Street house introduction remains part of the vanilla house-knock event pool.
- Meeting Mara at either her shop or her home unlocks return access to both locations.
- After the first meeting, Shopping Centre shows the Mara's Pet Shop link at any hour. The shop passage and work options are also available at any hour.
- After the first meeting, Danube Street displays a permanent Mara's home destination. Returning to Mara no longer depends on another random house-knock event.
- First-meeting and return dialogue at both locations welcomes the player and naturally invites them to help. The shop introduction mentions that Mara lives on Danube Street; the house introduction points the player toward her shop.
- Shop and house tasks keep their existing money and relationship rewards.
- Stat feedback uses native DoL display macros and is arranged on a separate reward line beneath the scene narrative.

## File Reference

- game/04-Variables/variables-static.twee: Mara NPC and Love Interest setup.
- game/04-Variables/npcNamed.twee: named NPC metadata and old-save migration.
- game/04-Variables/variables-maraUpdate.twee: Mara save state and relationship passages.
- game/04-Variables/variables-start2.twee and variables-versionUpdate.twee: initialization and migration.
- game/base-system/named-npcs.twee: npc increment whitelist and Trust support.
- game/base-system/widgets.twee: relationship clamps.
- game/base-system/overlays/cheats.twee: Cheat Menu controls.
- game/overworld-town/loc-shop/main.twee: shop link, availability, dialogue, and work tasks.
- game/overworld-town/loc-street/danube.twee: permanent house destination after meeting Mara.
- game/overworld-town/loc-danube-homes/work.twee: first meeting, return visit, and house-work tasks.

## Progression outline

1. Meet Mara at the pet shop during its usual first-visit hours or through the Danube Street house event.
2. That first meeting unlocks both her shop and home for future visits.
3. Return to the shop at any hour to browse, talk, or help with work.
4. Return to her home through the permanent Mara's home destination on Danube Street.
5. Shop and house work increase Love; selected actions also increase Trust and Dominance.
6. Love and Trust thresholds unlock private collection and romance events.
7. The Handler/Pet proposal requires an established romance route and the required relationship levels.

## Limitations

- The shop is a passage linked from Shopping Centre, not an independently registered map node.
- Work activities remain fixed choices instead of a balanced random shift/event system.
- No custom art is included.
- The romance and Handler/Pet route remains a basic passage-based implementation.
- The v0.1.3 access and dialogue changes compiled and patch-verified; an in-game pass with an existing Mara save is still required.