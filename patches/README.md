# Applying Mara v0.1.17

Target: vanilla Degrees of Lewdity 0.5.13.8.

## Clean installation

Use the cumulative patch:

    patch --dry-run -p1 -i patches/Mara_v0.1.17-Full.patch
    patch -p1 -i patches/Mara_v0.1.17-Full.patch

## Upgrade from v0.1.16

Use only the incremental patch:

    patch --dry-run -p1 -i patches/Mara_v0.1.17-StayInHouseOrders.patch
    patch -p1 -i patches/Mara_v0.1.17-StayInHouseOrders.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.17 bash compile.sh

The incremental patch changes only:
- `game/04-Variables/variables-maraUpdate.twee`
- `game/overworld-town/loc-danube-homes/work.twee`

Do not apply the incremental patch directly to clean vanilla source.

## Behaviour

- Mara is away from her house while at the pet shop (09:00-13:59) or Ocean Breeze Cafe (17:00-18:59, on her existing 40% daily roll).
- Before the shop or cafe outing, the player can choose to stay at the house. Mara assigns a random greeting position: front door, cushioned cage, or discipline room.
- If the player enters while Mara is already away, a note supplies a new random order. No Mara activities are available during her absence.
- The player chooses where to wait and advances time to 14:00 or 19:00.
- Being in the assigned position is accepted. Being in another place or leaving the house triggers a discipline-room reprimand when Mara returns or when the player next enters after her return.
- The reprimand randomly chooses whip/cane, uses three timed rounds, has a stop/release option, and totals 60 minutes if completed.
- Waiting state persists through save/reload. `objectVersion.mara` advances to 11.

Compilation and both patch routes were verified. In-game verification of the timing, position check, and punishment flow remains necessary.