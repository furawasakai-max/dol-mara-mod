# DoL Mara Mod v0.1.16

A Yareth-style direct source modification for vanilla **Degrees of Lewdity 0.5.13.8**.

## v0.1.16: Night Cage Timing Fix and Detailed Discipline

This update fixes the premature dawn-unlock message after a failed night escape. The old condition also treated any hour greater than or equal to 07:00 as morning, which incorrectly included 22:00 and 23:00. The return passage now compares the current absolute game timestamp with the stored next-07:00 release timestamp only.

The one-hour failed-lockpick punishment now follows a multi-stage structure inspired by the pacing of Avery's vanilla dungeon event:

- Mara randomly chooses a whip or cane for the night punishment.
- The player is secured to the padded X-frame with broad-lined cuffs.
- The session proceeds through three described rounds: five strokes, six measured strokes, and three final strokes.
- Each round uses the vanilla `<<masopain 15>>` effect once, protected against duplicate application if the passage is revisited.
- A stop/release option appears before and between rounds. Stopping ends the session early, but does not clear the failed-escape lockout.
- A completed session consumes exactly 60 in-game minutes: five minutes to the dungeon, 20 + 20 + 10 minutes for the rounds, and five minutes to return to the cage.
- Mara clips the lead to the collar and returns the player to the same cushioned cage. The cage is relocked if the stored 07:00 timestamp has not yet arrived.
- If the session ends at or after 07:00, Mara unlocks the cage immediately. The message reports the actual current time instead of claiming it is seven prematurely.

The night-cage timestamp and migration from v0.1.15 remain unchanged. No new persistent save fields are added; `objectVersion.mara` remains 10.

## Release history

- v0.1.0–v0.1.9: Base Mara NPC, shop, home, relationship systems, and cafe events.
- v0.1.10: Handler/Pet reaffirmation, collar inspection, and house rules.
- v0.1.11: Pet-room hub, cushion, bowl, cage sleep, and initial command training.
- v0.1.12: Random cushion orders and seven random training lessons.
- v0.1.13: Discipline room, daily random offer, whip/cane choices, and Masochism progress reward.
- v0.1.14: Harsher dialogue throughout pet-role scenes.
- v0.1.15: Night cage after 22:00, Skulduggery escape attempt, failed-attempt punishment, and 07:00 release.
- v0.1.16: Fixes premature dawn unlock and expands the failed-escape punishment into three detailed, timed rounds.

## Installation

### Clean vanilla 0.5.13.8

Use the single cumulative patch:

    patch --dry-run -p1 -i patches/Mara_v0.1.16-Full.patch
    patch -p1 -i patches/Mara_v0.1.16-Full.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.16 bash compile.sh

### Existing v0.1.15 source tree

Use only the incremental patch:

    patch --dry-run -p1 -i patches/Mara_v0.1.16-NightCageDisciplineFix.patch
    patch -p1 -i patches/Mara_v0.1.16-NightCageDisciplineFix.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.16 bash compile.sh

Do not apply the incremental patch directly to clean vanilla source. Back up your save before testing.

## Validation

- Tweego compilation succeeded in the v0.1.16 development tree.
- The incremental patch applies to the v0.1.15 source file with zero rejects and reproduces it byte-for-byte.
- The cumulative full patch dry-runs and applies to clean vanilla 0.5.13.8.
- All 17 modified/added source files from the full patch match the final development tree byte-for-byte.
- The clean full-patch verification tree compiles successfully.
- Static Mara passage targets have no missing links; no duplicate Mara passage names were detected.
- The full session's time allocations total exactly 60 minutes.
- In-game runtime testing is still needed for lockpick outcomes, pain effects, stop links, and dawn timing.

The repository source excludes vanilla game files and compiled HTML; those are supplied separately as release artifacts.