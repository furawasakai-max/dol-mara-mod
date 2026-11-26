# DoL Mara Mod v0.1.17

A Yareth-style direct source modification for vanilla **Degrees of Lewdity 0.5.13.8**.

## v0.1.17: Endurance Training

Adds a 30-minute endurance challenge to Mara's pet-room hub while retaining the v0.1.16 night-cage timing fix.

- Six five-minute intervals.
- Each interval increases player arousal by 500.
- Each interval ends with an escalating Willpower check, using a random threshold from 1-500 through 1-1000.
- Passing all six intervals grants +2 Mara Dominance and +1 Trust.
- Failing a check reduces Willpower by one and opens a route to Mara's discipline room.
- The player can stop at any time without a failure penalty.

## Source layout

The patch modifies vanilla source files directly. It is **not** a ModLoader package.

- `game/04-Variables/variables-maraUpdate.twee`: Mara state and scene passages.

## Installation

### Clean vanilla 0.5.13.8

Apply the v0.1.16 cumulative patch, then the v0.1.17 incremental patch:

    patch --dry-run -p1 -i patches/Mara_v0.1.16-Full.patch
    patch -p1 -i patches/Mara_v0.1.16-Full.patch
    patch --dry-run -p1 -i patches/Mara_v0.1.17-EnduranceTraining.patch
    patch -p1 -i patches/Mara_v0.1.17-EnduranceTraining.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.17 bash compile.sh

### Existing v0.1.16 source tree

Apply only the v0.1.17 incremental patch:

    patch --dry-run -p1 -i patches/Mara_v0.1.17-EnduranceTraining.patch
    patch -p1 -i patches/Mara_v0.1.17-EnduranceTraining.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.17 bash compile.sh

Back up your save and test using a copy. Browser runtime testing remains outstanding.

## License and upstream assets

This repository contains source patches intended to be applied to a separately obtained copy of DoL 0.5.13.8. It does not include vanilla game source or compiled HTML. Respect the game's upstream license and asset permissions when distributing derivatives.
