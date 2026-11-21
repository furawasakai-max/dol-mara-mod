# Applying Mara v0.1.12

Target: vanilla Degrees of Lewdity 0.5.13.8.

## Clean installation

Use the cumulative `Mara_v0.1.12-Full.patch` from the downloadable v0.1.12 source ZIP:

    patch --dry-run -p1 -i Mara_v0.1.12-Full.patch
    patch -p1 -i Mara_v0.1.12-Full.patch

## Upgrade from v0.1.11

For a source tree already patched through v0.1.11, apply only:

    patch --dry-run -p1 -i patches/Mara_v0.1.12-RandomPetPlay.patch
    patch -p1 -i patches/Mara_v0.1.12-RandomPetPlay.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.12 bash compile.sh

Do not apply the incremental patch directly to clean vanilla source.

## Random content

- Cushion wait: 40% chance per wait of a random order from Paw, Down/Stay, Come, Fetch, Grooming, Place, or short Heel follow.
- Training: one lesson per day, selected randomly from basic obedience, Heel, Paw, Fetch, Place, Grooming Manners, or Settle.
- The player can end the wait or stop training. Stopping removes the lead and gives no completion reward.
- Completing training retains the existing +2 Dominance / +1 Trust reward.
- The event text uses brief, soft-surface movement, a slack lead, stop choices, and a water/comfort check.

Compilation and both patch paths were verified. Runtime testing is still needed for actual random rolls, leash transitions, and daily reset behaviour.