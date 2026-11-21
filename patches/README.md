# Applying Mara v0.1.7

Target: vanilla Degrees of Lewdity 0.5.13.8.

## Clean installation

The v0.1.7 source ZIP contains the cumulative `Mara_v0.1.7-Full.patch` that applies directly to clean vanilla 0.5.13.8 source.

From the source root:

    patch --dry-run -p1 -i /path/to/Mara_v0.1.7-Full.patch
    patch -p1 -i /path/to/Mara_v0.1.7-Full.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.7 bash compile.sh

## Upgrade from v0.1.6

For a source tree already patched through v0.1.6, download `Mara_v0.1.7-HouseRestBreak.patch` from this folder and apply:

    patch --dry-run -p1 -i /path/to/Mara_v0.1.7-HouseRestBreak.patch
    patch -p1 -i /path/to/Mara_v0.1.7-HouseRestBreak.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.7 bash compile.sh

The incremental patch is not for clean vanilla source. Back up saves before testing.

## Event details

- The check occurs during each of Mara's three housework tasks: Organize Pet Supplies, Clean Animal Equipment, and Prepare Food Supplies.
- Each attempt has a 20% chance to show the offer, with at most one offer per in-game day.
- Accepting costs 10 additional minutes, applies the vanilla tea prop, reduces Stress by 6 and Tiredness by 4, and adds 1 Mara Love.
- After tea, the player returns to the same task's completion passage. Normal payment and task relationship rewards are applied once.
- Declining returns to that completion passage without the extra time or rest effects. The daily offer is still used up.
- Accepted breaks are counted in Mara's Journal.
- Shop work is unaffected.

The pattern is adapted from the vanilla Farm Pigs Feed Nausea / Farm Pigs Feed Nausea 2 work interruption. Mara's event is independent of the original pregnancy/nausea conditions.