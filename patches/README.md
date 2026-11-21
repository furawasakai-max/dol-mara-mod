# Applying Mara v0.1.14

Target: vanilla Degrees of Lewdity 0.5.13.8.

## Clean installation

Use the cumulative patch from the downloadable v0.1.14 source ZIP:

    patch --dry-run -p1 -i patches/Mara_v0.1.14-Full.patch
    patch -p1 -i patches/Mara_v0.1.14-Full.patch

## Upgrade from v0.1.13

Apply only the incremental patch:

    patch --dry-run -p1 -i patches/Mara_v0.1.14-RoughMaraDialogue.patch
    patch -p1 -i patches/Mara_v0.1.14-RoughMaraDialogue.patch

The incremental patch changes:
- game/04-Variables/variables-maraUpdate.twee
- game/overworld-town/loc-danube-homes/work.twee

Do not apply the incremental patch directly to clean vanilla source.

## Dialogue scope

The sharper, more dismissive tone is limited to the established pet arrangement. The second confirmation, collar scene, house rules, pet-room activities, random orders, training, pet-mode housework, and discipline room all use Mara's revised voice. Ordinary shop, cafe, romance, and non-pet interactions are unchanged.

All mechanics remain unchanged: activity chances, time passage, Masochism and relationship rewards, stop/decline links, and save fields.

Compilation and both patch routes were verified. Browser runtime testing of revised passage flow remains outstanding.