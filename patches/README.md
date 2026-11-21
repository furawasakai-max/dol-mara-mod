# Applying Mara v0.1.13

Target: vanilla Degrees of Lewdity 0.5.13.8.

## Clean installation

Use the single cumulative patch from clean vanilla:

    patch --dry-run -p1 -i patches/Mara_v0.1.13-Full.patch
    patch -p1 -i patches/Mara_v0.1.13-Full.patch

## Upgrade from v0.1.12

For a source tree already patched through v0.1.12, apply only:

    patch --dry-run -p1 -i patches/Mara_v0.1.13-DisciplineRoom.patch
    patch -p1 -i patches/Mara_v0.1.13-DisciplineRoom.patch

The incremental patch changes only `game/04-Variables/variables-maraUpdate.twee`.
Do not apply it directly to clean vanilla source.

## Behaviour

- The pet-room hub gains a separate discipline-room destination.
- The first room visit each in-game day rolls a 35% chance for a discipline offer. The roll is stored for the day, so revisiting does not reroll.
- On a successful roll, the player may choose a whip or cane session, confirm, or decline.
- The confirmed scene uses a padded X-frame and broad lined restraints. The actual discipline is implied rather than graphically depicted.
- The player can stop before or during the session. Mara immediately releases the player, and stopping gives no reward.
- Completing either implement's session awards +20 Masochism progress via the vanilla widget.
- No persistent save fields are added. `objectVersion.mara` advances to 9.

The cumulative patch dry-runs and applies to clean vanilla 0.5.13.8. Both clean and incremental source trees compile. In-game runtime testing remains necessary.