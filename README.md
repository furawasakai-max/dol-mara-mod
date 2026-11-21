# DoL Mara Mod v0.1.15

A Yareth-style direct source modification for vanilla **Degrees of Lewdity 0.5.13.8**.

## v0.1.15: Night Cage Routine

When the player is still in Mara's house after 22:00, the pet-room hub switches to a locked-cage night routine. The cage is the existing cushioned sleep point, not a separate room or a second bed.

- **Lockpick escape:** if Skulduggery is at least 400, a lockpick option appears. The vanilla skill check uses difficulty 700. Passing unlocks the cage and lets the player leave Mara's house.
- **Failed escape:** a failed attempt makes noise. Mara arrives, takes the player to the discipline room for a one-hour non-graphic reprimand, then attaches the lead and returns the player to the cage. The cage is locked again until morning.
- **Sleep until morning:** choosing to sleep uses vanilla sleep and waking effects, then advances the remaining time to exactly 07:00. Mara comes to unlock the cage and releases the lead if one is attached.
- **Dawn edge case:** if the one-hour reprimand crosses 07:00, Mara returns the player to the cage and unlocks it immediately instead of keeping the player past morning.

A failed lockpick stores the next 07:00 release time so repeated entry cannot reroll the check before dawn. The new `nightCageCaughtUntil` save field is migrated safely; `objectVersion.mara` advances to 10.

## Release history

- v0.1.0–v0.1.9: Base Mara NPC, shop, home, relationship systems, and cafe events.
- v0.1.10: Handler/Pet reaffirmation, collar inspection, and house rules.
- v0.1.11: Pet-room hub, cushion, bowl, cage sleep, and initial command training.
- v0.1.12: Random cushion orders and seven random training lessons.
- v0.1.13: Discipline room, daily random offer, whip/cane choices, and Masochism progress.
- v0.1.14: Harsher dialogue throughout pet-role scenes.
- v0.1.15: After-22:00 locked cage routine, Skulduggery escape attempt, failed-attempt discipline, and 07:00 release.

## Installation

### Clean vanilla 0.5.13.8

Use the single cumulative patch:

    patch --dry-run -p1 -i patches/Mara_v0.1.15-Full.patch
    patch -p1 -i patches/Mara_v0.1.15-Full.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.15 bash compile.sh

### Existing v0.1.14 source tree

Use only the incremental patch:

    patch --dry-run -p1 -i patches/Mara_v0.1.15-NightCageRoutine.patch
    patch -p1 -i patches/Mara_v0.1.15-NightCageRoutine.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.15 bash compile.sh

Do not apply the incremental patch directly to clean vanilla source. Back up your save before testing.

## Validation

- Tweego compilation succeeded in the v0.1.15 development tree.
- Incremental patch applies to v0.1.14 with zero rejects and reproduces the changed Mara passage file byte-for-byte.
- Cumulative full patch applies directly to clean vanilla 0.5.13.8; all 17 modified/added source files match byte-for-byte.
- The clean full-patch verification tree compiles successfully.
- Static passage-link and time-boundary checks passed.
- In-game runtime testing remains outstanding for lockpicking, failed escape, the one-hour punishment path, and sleep/wake behaviour.

The repository contains source patches and documentation, not vanilla game source or compiled game HTML.