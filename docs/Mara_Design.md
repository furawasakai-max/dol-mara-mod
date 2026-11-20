# Mara Love Interest

## NPC registration and relationship stats

- setup.NPCNameList
- setup.loveInterestNpc
- setup.loveAlias
- $NPCNameList
- $NPCName
- C.npc.Mara.love
- C.npc.Mara.trust
- C.npc.Mara.dom

## Save data

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
- Meeting Mara at either her pet shop or her Danube Street home unlocks return access to both locations.
- Mara follows a daily schedule based on the previously established shop hours:
  - 09:00-13:59: at the pet shop.
  - 14:00-08:59: at home on Danube Street.
- During shop hours, visiting her home displays: "No one is home. Mara is at the shop." No house interactions are offered.
- During home hours, entering her shop displays: "Mara isn't at the shop right now. She's at home on Danube Street." The player can follow the link to her home.
- The initial random Danube house introduction only enters the event pool while Mara is at home.
- First-meeting and return dialogue at both locations welcomes the player and invites them to help.
- Shop and house tasks keep their existing money and relationship rewards.
- Stat feedback uses native DoL display macros and sits on a separate reward line below the scene narrative.

## File Reference

- game/04-Variables/variables-static.twee: Mara NPC and Love Interest setup.
- game/04-Variables/npcNamed.twee: named NPC metadata and old-save migration.
- game/04-Variables/variables-maraUpdate.twee: Mara save state and relationship passages.
- game/04-Variables/variables-start2.twee and variables-versionUpdate.twee: initialization and migration.
- game/base-system/named-npcs.twee: NPC increment whitelist and Trust support.
- game/base-system/widgets.twee: relationship clamps.
- game/base-system/overlays/cheats.twee: Cheat Menu controls.
- game/overworld-town/loc-shop/main.twee: shop location, schedule availability, dialogue, and work tasks.
- game/overworld-town/loc-street/danube.twee: permanent house destination after meeting Mara.
- game/overworld-town/loc-danube-homes/work.twee: first meeting, home schedule, return visit, and house-work tasks.

## Progression outline

1. Meet Mara at the pet shop during shop hours or at her home outside shop hours.
2. That first meeting unlocks both her shop and home for future visits.
3. Visit the shop between 09:00 and 13:59 to browse, talk, or help with work.
4. Visit her home between 14:00 and 08:59 through the permanent Mara's home destination on Danube Street.
5. Shop and house work increase Love; selected actions also increase Trust and Dominance.
6. Love and Trust thresholds unlock private collection and romance events.
7. The Handler/Pet proposal requires an established romance route and the required relationship levels.

## Limitations

- The shop is a passage linked from Shopping Centre, not an independently registered map node.
- The schedule is currently the same every day; no weekday/weekend variation is implemented.
- Work activities remain fixed choices instead of a balanced random shift/event system.
- No custom art is included.
- The v0.1.4 schedule compiles and both patch paths apply, but the in-game presence/absence behaviour still needs testing.