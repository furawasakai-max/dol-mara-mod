# Applying the Mara source patches

Target: vanilla Degrees of Lewdity 0.5.13.8.

## Clean install

The downloadable Mara v0.1.5 ZIP includes a cumulative `Mara_v0.1.5-Full.patch` that applies directly to clean vanilla 0.5.13.8 source.

From the source root:

    patch --dry-run -p1 -i /path/to/Mara_v0.1.5-Full.patch
    patch -p1 -i /path/to/Mara_v0.1.5-Full.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.5 bash compile.sh

## Upgrade from v0.1.4

For a source tree already patched through v0.1.4, apply only:

    patch --dry-run -p1 -i /path/to/Mara_v0.1.5-ShoppingCentre.patch
    patch -p1 -i /path/to/Mara_v0.1.5-ShoppingCentre.patch

The incremental patch is specifically based on v0.1.4 and must not be applied to clean vanilla source.

## v0.1.5 Shopping Centre changes

- Removes the extra Mara shortcut that appeared above the Shopping Centre description.
- Replaces the normal vanilla Pet shop row with `Mara's Pet Shop (0:01)`, preserving its original position and pet-shop icon.
- Updates the night/exposed shop-list entry to use the Mara Pet Shop passage as well.
- Adds the vanilla `getouticon` before every `Leave the shop` action in Mara's passage, including its off-duty/closed view.
- Does not change Mara's daily schedule, work choices, time costs, money rewards, or relationship gains.

## v0.1.4 schedule

Mara's daily schedule:
- Shop: 09:00 through 13:59.
- Home: 14:00 through 08:59.

While Mara is at the shop, her house visit displays:

    No one is home. Mara is at the shop.

While she is at home, entering the shop displays:

    Mara isn't at the shop right now. She's at home on Danube Street.

## Stat feedback

The v0.1.1 and v0.1.2 updates use vanilla DoL's native stat feedback macros. They respect Blind Stats. Reward summaries appear below the narrative with one sign per changed stat and money separated by spacing.

Back up saves before testing. Compilation and patch application are verified; an in-game visual check of the v0.1.5 layout is still recommended.