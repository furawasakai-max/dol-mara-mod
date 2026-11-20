# Applying the Mara source patches

Target: vanilla Degrees of Lewdity 0.5.13.8.

## Recommended clean install

The downloadable v0.1.3 source ZIP contains a cumulative Mara_v0.1.3-Full.patch that applies to clean vanilla 0.5.13.8 source.

From the source root:

    patch --dry-run -p1 -i /path/to/Mara_v0.1.3-Full.patch
    patch -p1 -i /path/to/Mara_v0.1.3-Full.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.3 bash compile.sh

## Incremental upgrade

For a source tree already patched through v0.1.2, apply:

    patch --dry-run -p1 -i /path/to/Mara_v0.1.3-AlwaysAvailable.patch
    patch -p1 -i /path/to/Mara_v0.1.3-AlwaysAvailable.patch

The incremental patch must be applied after v0.1.0, v0.1.1, and v0.1.2. Do not apply it to clean vanilla source.

## What v0.1.3 changes

- Meeting Mara at either her pet shop or her Danube Street home unlocks return visits to both locations.
- After meeting her, the Shopping Centre link, pet-shop passage, and shop work choices remain available at any hour.
- After meeting her, a permanent Mara's home destination appears on Danube Street, so returning to her does not depend on a random house-knock event.
- Dialogue at both first meetings and repeat visits welcomes the player and naturally invites them to help, rather than asking whether they are looking for work.
- Existing work choices, money rewards, time costs, and relationship gain values are unchanged.

## Stat feedback

The v0.1.1 and v0.1.2 updates use vanilla DoL's native stat feedback macros. They respect the game's Blind Stats setting. Reward summaries appear below the narrative and use one sign per changed stat, with money separated by spacing.

Back up saves before testing. For v0.1.3, test using a save that has met Mara at either the shop or the house, then confirm both destinations are available.