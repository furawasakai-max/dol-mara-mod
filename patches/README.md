# Applying the Mara source patches

Target: vanilla Degrees of Lewdity 0.5.13.8.

## Clean install

1. Obtain and extract a clean, unmodified 0.5.13.8 source tree.
2. Apply the following patches in order:

   - Mara_v0.1.0.patch
   - Mara_v0.1.1-StatFeedback.patch
   - Mara_v0.1.2-StatLayout.patch
   - Mara_v0.1.3-AlwaysAvailable.patch
   - Mara_v0.1.4-ShopSchedule.patch

For each patch, test before applying:

    patch --dry-run -p1 -i /path/to/PATCH_NAME.patch
    patch -p1 -i /path/to/PATCH_NAME.patch

3. Compile from the source root:

    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.4 bash compile.sh

## Upgrade from v0.1.3

For a source tree already patched through v0.1.3, apply only:

    patch --dry-run -p1 -i /path/to/Mara_v0.1.4-ShopSchedule.patch
    patch -p1 -i /path/to/Mara_v0.1.4-ShopSchedule.patch

The v0.1.4 patch is incremental. It must not be applied directly to clean vanilla source.

## v0.1.4 schedule

Mara's daily schedule reuses the previously established shop hours:

- Shop: 09:00 through 13:59.
- Home: 14:00 through 08:59.

While Mara is at the shop, her house visit displays:

    No one is home. Mara is at the shop.

While she is at home, entering the shop displays:

    Mara isn't at the shop right now. She's at home on Danube Street.

The random first house introduction is also suppressed while Mara is at the shop. The player can still see both location links after meeting Mara, but only her current location offers interaction.

## Earlier stat feedback

The v0.1.1 and v0.1.2 updates use vanilla DoL's native stat feedback macros. They respect Blind Stats. Reward summaries appear below the narrative with one sign per changed stat and money separated by spacing.

Back up saves before testing. The schedule is set for every day and has not yet been confirmed in-browser.