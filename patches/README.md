# Applying Mara v0.1.15

Target: vanilla Degrees of Lewdity 0.5.13.8.

## Clean installation

Use the single cumulative patch:

    patch --dry-run -p1 -i patches/Mara_v0.1.15-Full.patch
    patch -p1 -i patches/Mara_v0.1.15-Full.patch

## Upgrade from v0.1.14

For a source tree already patched through v0.1.14, apply only:

    patch --dry-run -p1 -i patches/Mara_v0.1.15-NightCageRoutine.patch
    patch -p1 -i patches/Mara_v0.1.15-NightCageRoutine.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.15 bash compile.sh

The incremental patch changes only `game/04-Variables/variables-maraUpdate.twee`. Do not apply it directly to clean vanilla source.

## Night behaviour

- After 22:00, the normal pet-room activity menu is replaced by the locked cage night routine.
- The cage is the cushioned sleep point already used during daytime.
- If Skulduggery is at least 400, the player can attempt to pick the lock. The vanilla skill check difficulty is 700.
- Success unlocks the cage and lets the player leave.
- Failure makes noise. Mara arrives and takes the player to the discipline room for a one-hour non-graphic reprimand, then leashes and returns the player to the cage.
- The failed-attempt lock holds until 07:00; repeated entry cannot reroll it.
- Choosing sleep invokes native sleep and wake effects, then advances exactly to 07:00.
- At 07:00, Mara unlocks the cage and removes an attached lead.
- If the one-hour reprimand crosses 07:00, the cage is unlocked on return.

The incremental patch applies to v0.1.14. The cumulative patch applies to clean vanilla 0.5.13.8. Both source paths compile. Runtime testing is still needed.