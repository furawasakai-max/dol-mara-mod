# Applying Mara v0.1.7

Target: vanilla Degrees of Lewdity 0.5.13.8.

## Clean installation

The downloadable v0.1.7 source ZIP includes the cumulative `Mara_v0.1.7-Full.patch` that applies directly to clean vanilla 0.5.13.8 source.

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

The new `maraHouseRestOffer` widget is called after each completed house task. It has a 1-in-4 chance to show Mara's offer. If the player accepts, the tea passage applies `wearProp "tea"`, reduces Stress by 6, increases Mara's Love by 1, and increments `$mara.restBreaks`. The Journal displays the accepted-break count. Declining has no stat effect.

This event does not change the house-work task's existing pay, task time, or relationship reward. It does not appear during shop work.