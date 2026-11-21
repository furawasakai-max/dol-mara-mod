# DoL Mara Mod v0.1.13

A Yareth-style direct source modification for vanilla **Degrees of Lewdity 0.5.13.8**.

## v0.1.13: Mara's Discipline Room

The pet-room hub now includes a separate discipline room at the back of Mara's house. A padded X-frame, broad lined cuffs, a safety release, a whip, and a cane are described as part of the room.

### Random offer

The first time the player visits the room each in-game day, the game rolls a **35% chance** for Mara to offer a discipline session. The result is stored in the daily state, so leaving and re-entering does not reroll the encounter that day. The player can decline without penalty.

### Session choices

When an offer appears, the player chooses either the whip or the cane, then confirms whether to begin. Mara checks the agreed stop word and signal before the player is secured to the padded X-frame. The discipline itself is implied rather than graphically narrated. The scene includes a stop/release option before and during the session.

Completing either instrument's session grants **+20 Masochism progress** through the vanilla `<<masochism 20>>` widget. Declining or stopping grants no Masochism progress. The underlying Masochism value is capped by the vanilla system at 1000; its level tier is recalculated by the game's daily effects. The reward is progress, not an immediate direct level increase.

The update adds no persistent save fields. It uses `$daily.mara` flags, which reset with the game's daily state, and advances `objectVersion.mara` to 9.

## Release history

- v0.1.0: Base Mara NPC, shop, house work, relationship stats, and early scenes.
- v0.1.1: Native relationship stat feedback.
- v0.1.2: Separate reward line and single stat indicators.
- v0.1.3: Persistent access to both Mara locations after first meeting.
- v0.1.4: Daily shop/home schedule.
- v0.1.5: Mara's Pet Shop replaces the vanilla Pet Shop row in Shopping Centre.
- v0.1.6: Native named-NPC integration and save migration.
- v0.1.7: Housework tea break.
- v0.1.8: Random evening cafe appearance and conversations.
- v0.1.9: Random cafe conversation topic selection.
- v0.1.10: Handler/Pet reaffirmation, collar inspection, and house rules.
- v0.1.11: Pet-room hub, cushion, bowl, cage sleep, and initial training.
- v0.1.12: Random cushion orders and seven random training lessons.
- v0.1.13: Discipline room, daily random offer, whip/cane choices, X-frame scene, and Masochism progress reward.

## Installation

### Clean vanilla 0.5.13.8

Use the single cumulative patch:

    patch --dry-run -p1 -i patches/Mara_v0.1.13-Full.patch
    patch -p1 -i patches/Mara_v0.1.13-Full.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.13 bash compile.sh

### Existing v0.1.12 source tree

Use only the incremental patch:

    patch --dry-run -p1 -i patches/Mara_v0.1.13-DisciplineRoom.patch
    patch -p1 -i patches/Mara_v0.1.13-DisciplineRoom.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.13 bash compile.sh

Do not apply the incremental patch directly to clean vanilla source. Back up your save before testing.

## Validation

- Tweego compilation succeeded in the v0.1.13 development tree.
- The incremental patch applies to the v0.1.12 source tree and reproduces the changed Mara passage file byte-for-byte.
- The cumulative single full patch dry-runs and applies to clean vanilla 0.5.13.8.
- All 17 modified/added source files from the full patch match the final working source byte-for-byte.
- The clean full-patch verification tree compiles successfully.
- Static passage and `git diff --check` checks passed.
- In-game runtime testing remains outstanding for the random offer, stop links, and Masochism reward.

The repository contains source patches and documentation, not the vanilla game source or compiled game HTML.