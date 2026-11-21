# DoL Mara Mod v0.1.6

A Yareth-style direct source modification for vanilla **Degrees of Lewdity 0.5.13.8**. This release uses the named-NPC integration checklist to move Mara further into the game's existing NPC systems.

## v0.1.6 changes

- Adds `maraSchedule()` and `maraStatusCheck()` to `game/03-JavaScript/named-npc.js`, called through the existing `statusCheck()` switch. The shop is 09:00-13:59; home is 14:00-08:59.
- Adds Mara to `isPossibleLoveInterest()` in `game/03-JavaScript/ingame.js`, gated by accepted romance state and non-dismissed NPC state.
- Routes romance acceptance through the vanilla `loveInterestAdd` widget. The Attitudes menu can therefore select Mara using the existing Love Interest slots. Debug-unlock support is also added.
- Adds Mara to the Social relationship panel with Love, Trust, and Dominance display, and puts her in Primary Relationships after the player has met her.
- Adds a Mara section to the Journal, summarising meetings, work progress, private collection, romance, and the Handler relationship.
- Adds Mara's initial named-NPC clothes and appearance defaults using existing vanilla outfit sets.
- Adds a save migration using `$objectVersion.mara`. When a previous alpha save has met Mara but her named-NPC record is still uninitialised, it calls `initnpc` and restores existing relationship/body/appearance/state fields.
- Fixes the Danube first-meeting event to route through Mara's introduction passage so the house meeting flag and NPC initialization are consistently applied.

## NPC system notes

- Mara remains a named NPC in `$NPCName` / `$NPCNameList`.
- Mara uses the existing `npcincr` system. In this 0.5.13.8 source, relationship decreases are made through negative `npcincr` values; there is no separate `npcdecr` widget required for this implementation.
- `base-system/persistent-npcs.twee` is not modified: it persists generated NPCs from `$NPCList` / `$per_npc`, whereas Mara is a named NPC in `$NPCName`.
- Portraits, sprites, bespoke combat behaviour, and sexual-scene hooks remain future work.

## Installation

For a clean vanilla 0.5.13.8 source tree, use `Mara_v0.1.6-Full.patch` from the v0.1.6 source ZIP. For a source tree already patched through v0.1.5, use the [incremental NPC integration patch](patches/Mara_v0.1.6-NPCIntegration.patch) from this repository. See `patches/README.md` for commands.

Compile with the source tree's Tweego-based `compile.sh`. The repository package contains source patches and documentation, not the vanilla game source or compiled game HTML.

## Validation

- Tweego compilation succeeded.
- The cumulative patch applies to clean vanilla 0.5.13.8 source.
- The incremental patch applies to the v0.1.5 source baseline.
- Browser runtime testing of the new Social, Journal, Love Interest, and save-migration paths is still required.