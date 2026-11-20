# Mara Love Interest

## Credits

Producer: TBD  
Writer: TBD  
Coder & Editor: TBD

## Mara variables

### Added to

- `setup.NPCNameList`
- `setup.loveInterestNpc`
- `setup.loveAlias`
- `setup.colours.hair`
- `setup.npcClothesSets`
- `$NPCNameList`
- `$NPCName`
- `C.npc.Mara`

### New

- `$objectVersion.mara`
- `$mara`
  - `.introShop` — whether the player has met Mara at her High Street pet shop.
  - `.introHouse` — whether the player has met Mara through the Danube Street job-search encounter.
  - `.shop` — shop state and availability data.
  - `.house` — house availability and work state.
  - `.work` — completed jobs, current task, and work history.
  - `.work.lastPaid` — last payment issued for a completed task.
  - `.work.completed` — completed work identifiers.
  - `.events` — one-time event flags.
  - `.events.privateCollection` — whether Mara has shown the private collection.
  - `.events.handlerProposal` — whether the Handler/Pet proposal has occurred.
  - `.loveInterest` — whether Mara's romance route has been accepted.
  - `.petRelationship` — whether the player accepted the Handler/Pet relationship.

### NPC relationship stats

Mara uses the named-NPC relationship fields:

- `C.npc.Mara.love`
- `C.npc.Mara.trust`
- `C.npc.Mara.dom`

## Implemented feedback

The v0.1.1 update uses DoL's built-in stat display macros for Mara's Love, Trust, and Dominance. The v0.1.2 layout places feedback on a separate reward line below the narrative. Each stat uses one plus or minus sign regardless of the number of points changed, while the actual game values remain unchanged. Cash displays as a separate positive amount. The native relationship feedback respects Blind Stats.

Positive feedback uses `glove Mara`, `gtrust`, and `gdom Mara`. Future negative relationship outcomes should use the corresponding native negative macros, for example `llove Mara`, `ltrust`, and `ldom Mara`.

## Planned progression

- Shop and house work primarily increase Love.
- After Love reaches 50, selected personal events can also increase Trust.
- Trust unlocks Mara's personal history and private equipment events.
- Dominance increases through Mara-led Handler discussions and consensual role-play events.
- Romance confession: Love 100 and Trust at least 50.
- Handler/Pet proposal: Mara is an active Love Interest, Love 100, Trust greater than 70, and Dominance 100.

## File Reference

The following is the original planned implementation map for vanilla DoL 0.5.13.8. The current alpha patch does not yet implement every item listed here.

### Files changed

- `game/04-Variables/variables-static.twee` — add Mara to named-NPC and Love Interest setup lists, plus any aligned metadata arrays.
- `game/04-Variables/npcNamed.twee` — ensure Mara's named-NPC metadata and initialization are supported.
- `game/04-Variables/variables-start.twee` — initialize setup-level Mara defaults where required.
- `game/04-Variables/variables-start2.twee` — initialize new-game Mara state where required.
- `game/04-Variables/variables-versionUpdate.twee` — migrate existing saves and initialize missing Mara variables without resetting existing progress.
- `game/base-system/named-npcs.twee` — ensure Mara's NPC record and relationship stat handling are valid.
- `game/base-system/overlays/social.twee` — add Mara's Love Interest/social display integration if required by the vanilla implementation.
- `game/base-system/overlays/cheats.twee` — add Mara Love, Trust, and Dominance controls.
- `game/overworld-town/loc-danube-homes/work.twee` — add Mara as a random Danube Street work encounter.
- `game/overworld-town/loc-street/danube.twee` — add or link any required Mara location/navigation behaviour.
- High Street shop location passage(s) — add Mara's Pet Shop entry and opening hours (09:00–14:00), after confirming the exact target location passage in the source.

### Files added

- `game/03-JavaScript/maraUpdate.js` — Mara-specific helpers and state updates, only where Twee widgets are insufficient.
- `game/04-Variables/variables-maraUpdate.twee` — initialize `$mara` and `$objectVersion.mara` safely.
- `game/overworld-town/loc-shop/mara-shop.twee` — proposed shop passages; final path depends on the actual High Street shop location structure.
- `game/overworld-town/loc-danube-homes/mara-house.twee` — Mara's house-work passages and event widgets.
- `game/overworld-town/loc-danube-homes/mara-events.twee` — work, personal, and relationship events.
- `game/ModLI/Mara/mara-widget.twee` — optional Mod LI-specific widgets if using the DoL Plus Mod LI framework rather than vanilla-only registration.
- `game/ModLI/Mara/mara-speech.twee` — Mara-specific dialogue, if using the DoL Plus Mod LI architecture.

## Event and progression outline

1. **High Street introduction:** independent first meeting at Mara's pet shop.
2. **Danube Street introduction:** random first meeting during the existing house job-search event pool; does not require the shop introduction.
3. **Shop work:** shop is open from 09:00 to 14:00; tasks and random events reward money and relationship progress.
4. **House work:** after encountering Mara through Danube Street, the player can ask for work when she is home; payment depends on the task.
5. **Love progression:** ordinary work and positive interactions increase Love.
6. **Trust progression:** selected personal events begin granting Trust after Love reaches 50.
7. **Private collection:** Trust unlocks Mara's explanation of her interests and her private bondage/pet-play equipment.
8. **Dominance progression:** selected Mara-led events increase Mara's NPC Dominance stat.
9. **Romance confession:** at Love 100 and Trust at least 50, Mara can become an active Love Interest after the player accepts.
10. **Handler/Pet proposal:** after romance activation, Love 100, Trust greater than 70, and Dominance 100, Mara can propose the consensual Handler/Pet relationship.

## Compatibility notes

- Target game: vanilla Degrees of Lewdity 0.5.13.8 unless explicitly changed.
- Yareth's `Yareth.md` targets 0.5.12.11 and is used as an architectural/documentation reference, not copied blindly.
- DoL Plus Poppy Mod LI registration is a separate framework and must not be assumed to exist in vanilla.
- The exact High Street shop passage path, registration array order, and stat validation hooks must be confirmed against the target source before applying code changes.
- Existing saves must retain Mara's existing stats and event flags during updates.
