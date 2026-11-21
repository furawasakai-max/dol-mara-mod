# DoL Mara Mod v0.1.7

A Yareth-style direct source modification for vanilla **Degrees of Lewdity 0.5.13.8**.

## v0.1.7: Mara's house-work tea break

During Mara's housework, there is a **20% chance per task attempt** that she notices the player has been working hard and asks them to take a short break. The offer can appear at most once per in-game day.

The player can accept or politely decline. Accepting takes 10 minutes. Mara brings tea and biscuits, sits with the player, and keeps them company. The break reduces Stress by 6 and Tiredness by 4, and increases Mara's Love by 1. The player then returns to the same task's completion passage, so its normal payment and relationship rewards are still awarded once.

Declining adds no extra time and continues the task normally. The existing 30/45/30-minute task costs, task rewards, and all shop work are unchanged. Accepted breaks are recorded in Mara's Journal.

## Release history

- v0.1.0: Base Mara NPC, shop, house work, relationship stats, and early scenes.
- v0.1.1: Native relationship stat feedback.
- v0.1.2: Separate reward line and single stat indicators.
- v0.1.3: Persistent access to both Mara locations after first meeting.
- v0.1.4: Daily shop/home schedule.
- v0.1.5: Mara's Pet Shop replaces the vanilla Pet Shop row in Shopping Centre.
- v0.1.6: Named-NPC status, Attitudes, Social, Journal, and save migration integration.
- v0.1.7: Random housework rest and tea interruption.

## Installation

### Clean vanilla 0.5.13.8

Use `Mara_v0.1.7-Full.patch` from the v0.1.7 source ZIP:

    patch --dry-run -p1 -i patches/Mara_v0.1.7-Full.patch
    patch -p1 -i patches/Mara_v0.1.7-Full.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.7 bash compile.sh

### Existing v0.1.6 source tree

Use only `Mara_v0.1.7-HouseRestBreak.patch` from this repository:

    patch --dry-run -p1 -i patches/Mara_v0.1.7-HouseRestBreak.patch
    patch -p1 -i patches/Mara_v0.1.7-HouseRestBreak.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.7 bash compile.sh

Do not apply the incremental patch directly to clean vanilla source. Back up saves before testing.

## Validation

- Tweego compilation succeeded.
- The incremental patch applies to the v0.1.6 source baseline with zero rejects.
- The cumulative patch applies to clean vanilla 0.5.13.8 with zero rejects.
- Both resulting source trees match the v0.1.7 working source byte-for-byte.
- Browser runtime testing of the event chance, time cost, return flow, and stat effects remains necessary.

The repository contains source patches and documentation, not the vanilla game source or compiled game HTML.