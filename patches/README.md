# Applying Mara v0.1.11

Target: vanilla Degrees of Lewdity 0.5.13.8.

## Clean installation

Use the cumulative patch from the downloadable v0.1.11 source ZIP:

    patch --dry-run -p1 -i Mara_v0.1.11-Full.patch
    patch -p1 -i Mara_v0.1.11-Full.patch

It includes the complete Mara source changes through v0.1.11.

## Upgrade from v0.1.10

For a source tree already patched through v0.1.10, apply only:

    patch --dry-run -p1 -i Mara_v0.1.11-PetRoomTraining.patch
    patch -p1 -i Mara_v0.1.11-PetRoomTraining.patch

The incremental update changes only:
- `game/04-Variables/variables-maraUpdate.twee`
- `game/overworld-town/loc-danube-homes/work.twee`

Do not apply the incremental patch directly to clean vanilla source.

## Behaviour

- The established pet-house route opens a pet-room hub.
- The player can wait on a cushion for ten minutes, eat from the pet bowl once per day, sleep in a cushioned cage, or begin command training.
- Cage sleeping uses the game's native `generateSleepLinks`, `sleep`, `wakingEffects`, and `sleepeffects` systems.
- Command training is available once per day. Mara clips a lead to the collar and issues Down, Heel, Stay, and Come commands while the player crawls on all fours around the room.
- Completing training grants +2 Mara Dominance and +1 Mara Trust. Stopping ends the event and removes the training lead without completion rewards.
- Housework remains an optional separate activity; pet-mode chores return to the pet room.

Compilation and patch application were verified. Runtime testing is still needed for sleep/wake behaviour, leash transitions, and daily activity limits.