# Applying Mara v0.1.8

Target: vanilla Degrees of Lewdity 0.5.13.8.

## Clean installation

The downloadable v0.1.8 source ZIP contains the cumulative `Mara_v0.1.8-Full.patch`.

From the source root:

    patch --dry-run -p1 -i /path/to/Mara_v0.1.8-Full.patch
    patch -p1 -i /path/to/Mara_v0.1.8-Full.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.8 bash compile.sh

## Upgrade from v0.1.7

For a source tree already patched through v0.1.7, download `Mara_v0.1.8-CafeChats.patch` from this folder and apply:

    patch --dry-run -p1 -i /path/to/Mara_v0.1.8-CafeChats.patch
    patch -p1 -i /path/to/Mara_v0.1.8-CafeChats.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.8 bash compile.sh

The incremental patch is not for clean vanilla source. Back up saves before testing.

## Event rules

- Mara must already have been met at her shop or Danube Street home.
- Between 17:00 and 18:59, there is a 40% chance she is at Ocean Breeze Cafe. The chance is rolled once per in-game day and remains stable for that evening.
- The player can approach her and choose one of three 30-minute chat topics: pets, the player's life, or the weather.
- Each completed conversation adds 1 Mara Love and 1 Mara Trust.
- After each chat, there is a 25% chance that Mara says goodbye and returns home. She also leaves automatically at 19:00.
- A full 30-minute chat is not offered after 18:30.
- While Mara is at the cafe, her shop and home passages show an away notice and point the player to Ocean Breeze.
- The Journal tracks the number of completed cafe conversations.

The v0.1.8 initializer adds `cafeChats` to older saves without resetting existing Mara data. `objectVersion.mara` advances to 5.