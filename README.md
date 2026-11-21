# DoL Mara Mod v0.1.14

A Yareth-style direct source modification for vanilla **Degrees of Lewdity 0.5.13.8**.

## v0.1.14: Mara's Harsher Pet-Role Dialogue

Mara's dialogue during the established Handler/Pet arrangement is now colder, sharper, and more openly dismissive. She treats the player as a badly behaved, incompetent pet who needs constant direction, rather than speaking with the patient and cheerful tone used in earlier scenes.

The revised voice covers the second pet confirmation, collar inspection, house rules, pet-room welcome, cushion waiting and random orders, pet-bowl meal, cage sleep, command training, housework while in pet mode, and discipline-room events. Dialogue uses curt commands, dry criticism, impatience, and occasional insults such as "useless little thing" and "hopeless pet".

The tone change is limited to pet-role scenes. Mara's ordinary shop interactions, cafe conversations, romance scenes, and her non-pet house visits retain their previous dialogue. Existing stop and decline paths remain available.

## Mechanics unchanged

- No relationship thresholds, stat rewards, or activity timers changed.
- No random chance or daily event logic changed.
- Pet-room activities, bowl effects, cage sleep, random lessons, and discipline-room reward remain as in v0.1.13.
- No new save fields or migration are required. objectVersion.mara remains 9.

## Release history

- v0.1.0–v0.1.9: Base Mara NPC, shop, home, relationship systems, and cafe events.
- v0.1.10: Handler/Pet reaffirmation, collar inspection, and house rules.
- v0.1.11: Pet-room hub, cushion, bowl, cage sleep, and initial command training.
- v0.1.12: Random cushion orders and seven random training lessons.
- v0.1.13: Discipline room, daily random offer, whip/cane choices, and Masochism progress reward.
- v0.1.14: Harsher dialogue throughout the pet-role scenes.

## Installation

### Clean vanilla 0.5.13.8

Use the single cumulative patch from the downloadable v0.1.14 source ZIP:

    patch --dry-run -p1 -i patches/Mara_v0.1.14-Full.patch
    patch -p1 -i patches/Mara_v0.1.14-Full.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.14 bash compile.sh

### Existing v0.1.13 source tree

Use only the incremental patch from the downloadable v0.1.14 source ZIP:

    patch --dry-run -p1 -i patches/Mara_v0.1.14-RoughMaraDialogue.patch
    patch -p1 -i patches/Mara_v0.1.14-RoughMaraDialogue.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.14 bash compile.sh

Do not apply the incremental patch directly to clean vanilla source. Back up your save before testing.

## Validation

- Tweego compilation succeeded in the v0.1.14 development tree.
- Incremental patch applies to v0.1.13 source with zero rejects; both modified files match byte-for-byte.
- Cumulative full patch applies to clean vanilla 0.5.13.8.
- All 17 modified/added source files match the final assembled tree byte-for-byte.
- Clean full-patch verification tree compiles successfully.
- git diff --check is clean.
- Browser runtime testing of revised dialogue flow remains outstanding.

The repository contains source patches and documentation, not vanilla game source or compiled game HTML.