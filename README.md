# DoL Mara Mod v0.1.11

A Yareth-style direct source modification for vanilla **Degrees of Lewdity 0.5.13.8**.

## v0.1.11: Pet Room and Command Training

After the Handler/Pet house rules are established, Mara's home now leads to a dedicated pet-room hub instead of sending the player directly into housework.

The room provides four main activities:

- **Wait on the cushion:** spend ten minutes waiting for Mara to give an instruction.
- **Eat from the pet bowl:** a once-per-day meal scene, taking ten minutes and reducing Hunger by 500 and Stress by 3.
- **Rest in the cushioned cage:** a dedicated sleep point using the game's native sleep-duration options and sleep/wake effects.
- **Command training:** a once-per-day training event in which Mara clips a lead to the player's collar and gives the commands Down, Heel, Stay, and Come. The player crawls on all fours while following her around the room. Completing the session grants +2 Mara Dominance and +1 Mara Trust. The player can stop the session at any stage; stopping ends the scene without completion rewards.

Housework remains available as a separate optional activity from the pet room. In pet mode, completed chores return the player to the room rather than sending them outside. Existing non-pet house visits and rewards remain unchanged.

The save migration advances `objectVersion.mara` to 7 and initializes `petTrainingSessions` for older saves.

## Release history

- v0.1.0: Base Mara NPC, shop, house work, relationship stats, and early scenes.
- v0.1.1: Native relationship stat feedback.
- v0.1.2: Separate reward line and single stat indicators.
- v0.1.3: Persistent access to both Mara locations after first meeting.
- v0.1.4: Daily shop/home schedule.
- v0.1.5: Mara's Pet Shop replaces the vanilla Pet Shop row in Shopping Centre.
- v0.1.6: Native named-NPC integration and save migration.
- v0.1.7: Housework tea break.
- v0.1.8: Random evening cafe visits and conversation topics.
- v0.1.9: Random cafe conversation topic selection.
- v0.1.10: Handler/Pet reaffirmation, collar inspection, and house rules.
- v0.1.11: Pet-room hub, cushion waiting, pet-bowl meal, cage sleep point, command training, and save migration.

## Installation

### Clean vanilla 0.5.13.8

Use `Mara_v0.1.11-Full.patch` from the downloadable v0.1.11 source ZIP:

    patch --dry-run -p1 -i Mara_v0.1.11-Full.patch
    patch -p1 -i Mara_v0.1.11-Full.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.11 bash compile.sh

### Existing v0.1.10 source tree

Use only `Mara_v0.1.11-PetRoomTraining.patch` from the downloadable source ZIP:

    patch --dry-run -p1 -i Mara_v0.1.11-PetRoomTraining.patch
    patch -p1 -i Mara_v0.1.11-PetRoomTraining.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.11 bash compile.sh

Do not apply the incremental patch directly to clean vanilla source. Back up your save before testing.

## Validation

- Tweego compilation succeeded for v0.1.11.
- The incremental patch applies to v0.1.10 source with zero rejects and reproduces both changed source files byte-for-byte.
- The cumulative full patch applies to clean vanilla 0.5.13.8 with zero rejects; all 17 changed/added source files match the final source tree byte-for-byte.
- The full-patch verification tree also compiles successfully.
- Static passage and link-target checks passed.
- Browser runtime testing is still required for cage sleep/wake behaviour, collar/leash transitions, and the daily activity limits.

The repository contains source patches and documentation, not the vanilla game source or compiled game HTML.