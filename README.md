# DoL Mara Mod v0.1.7

A Yareth-style direct source modification for vanilla **Degrees of Lewdity 0.5.13.8**.

## v0.1.7: Mara's house-work tea break

There is now a **25% chance after each completed Mara house-work task** that Mara notices the player has been working steadily and asks them to take a short rest. She puts the kettle on and brings two cups of tea, sitting with the player for a quiet break.

The player may accept or politely decline. Accepting the tea:

- Reduces Stress by 6.
- Increases Mara's Love by 1.
- Adds one accepted tea break to Mara's Journal progress.
- Does not add extra time; the pause is part of the completed work visit.

The event can occur after Organize Pet Supplies, Clean Animal Equipment, or Prepare Food Supplies. Existing task payments, time costs, and relationship rewards are unchanged. Shop work is unaffected.

## Release history

- v0.1.0: Base Mara NPC, shop, house work, relationship stats, and early scenes.
- v0.1.1: Native relationship stat feedback.
- v0.1.2: Separate reward line and single stat indicators.
- v0.1.3: Persistent access to both Mara locations after first meeting.
- v0.1.4: Daily shop/home schedule.
- v0.1.5: Mara's Pet Shop replaces the vanilla Pet Shop row in Shopping Centre.
- v0.1.6: Named-NPC status, Attitudes, Social, Journal, and save migration integration.
- v0.1.7: Random house-work rest and tea event.

## Installation

### Clean vanilla 0.5.13.8

Use `Mara_v0.1.7-Full.patch` from the v0.1.7 source ZIP:

    patch --dry-run -p1 -i patches/Mara_v0.1.7-Full.patch
    patch -p1 -i patches/Mara_v0.1.7-Full.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.7 bash compile.sh

### Existing v0.1.6 source tree

Use only `Mara_v0.1.7-HouseRestBreak.patch`:

    patch --dry-run -p1 -i patches/Mara_v0.1.7-HouseRestBreak.patch
    patch -p1 -i patches/Mara_v0.1.7-HouseRestBreak.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.7 bash compile.sh

Do not apply the incremental patch directly to clean vanilla source. Back up your save before testing.

## Validation

- Tweego compilation succeeded.
- Incremental v0.1.7 patch applied to the v0.1.6 source baseline with zero rejects.
- Cumulative v0.1.7 patch applied to clean vanilla 0.5.13.8 with zero rejects.
- The three updated source files from the incremental patch match the final source tree byte-for-byte.
- Runtime testing of the random event appearance, tea effects, and Journal count is still required.

The repository contains source patches and documentation, not the vanilla game source or compiled game HTML.