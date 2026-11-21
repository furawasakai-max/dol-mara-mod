# DoL Mara Mod v0.1.8

A Yareth-style direct source modification for vanilla **Degrees of Lewdity 0.5.13.8**.

## v0.1.8: Mara's evening café visits

After the player has met Mara at her shop or home, she has a **40% chance per in-game day** to spend part of the early evening at Ocean Breeze Cafe. The daily roll is made the first time her schedule is checked between **17:00 and 18:59** and is saved for that day, so revisiting locations cannot reroll her availability.

When present, Mara can be approached at the cafe. The player can choose one of three conversations:

- **Talk about pets (30 minutes):** Mara talks about the adorable kittens and the personalities of the animals she cares for.
- **Ask about your life (30 minutes):** Mara asks how the player's life has been and listens to them.
- **Chat about the weather (30 minutes):** They exchange casual thoughts about the weather and the comfort of the cafe.

Each completed conversation adds **+1 Mara Love** and **+1 Mara Trust**. After each chat there is a **25% chance** Mara decides it is time to head home. If the conversation reaches 19:00, she leaves automatically. Once she has left, she is considered at home for the rest of that day and cannot be approached at the cafe again.

While Mara is at the cafe, her shop and home passages report that she is away and point the player to Ocean Breeze Cafe. Full 30-minute conversations are not offered after 18:30. Her existing shop/home schedule is otherwise unchanged. The Journal records the number of cafe conversations. Existing v0.1.7 saves initialize the new counter to zero without resetting previous progress.

## Release history

- v0.1.0: Base Mara NPC, shop, house work, relationship stats, and early scenes.
- v0.1.1: Native relationship stat feedback.
- v0.1.2: Separate reward line and single stat indicators.
- v0.1.3: Persistent access to both Mara locations after first meeting.
- v0.1.4: Daily shop/home schedule.
- v0.1.5: Mara's Pet Shop replaces the vanilla Pet Shop row in Shopping Centre.
- v0.1.6: Named-NPC status, Attitudes, Social, Journal, and save migration integration.
- v0.1.7: Random housework rest and tea interruption.
- v0.1.8: Random evening cafe appearance and three 30-minute conversation topics.

## Installation

### Clean vanilla 0.5.13.8

Use `Mara_v0.1.8-Full.patch` from the downloadable v0.1.8 source ZIP:

    patch --dry-run -p1 -i patches/Mara_v0.1.8-Full.patch
    patch -p1 -i patches/Mara_v0.1.8-Full.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.8 bash compile.sh

### Existing v0.1.7 source tree

Use only [Mara_v0.1.8-CafeChats.patch](patches/Mara_v0.1.8-CafeChats.patch):

    patch --dry-run -p1 -i patches/Mara_v0.1.8-CafeChats.patch
    patch -p1 -i patches/Mara_v0.1.8-CafeChats.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.8 bash compile.sh

Do not apply the incremental patch directly to clean vanilla source. Back up your save before testing.

## Validation

- Tweego compilation succeeded.
- JavaScript syntax checks passed for `named-npc.js` and `ingame.js`.
- The incremental patch applies to v0.1.7 source with zero rejects.
- The cumulative patch applies to clean vanilla 0.5.13.8 with zero rejects.
- Both patched source trees reproduce the v0.1.8 working source byte-for-byte.
- The schedule function was tested for shop/home/cafe hours, stable daily rolls, and the post-goodbye return home state.
- Browser runtime testing of the actual cafe interaction, time cost, relationship gains, goodbye chance, and Journal count remains required.

The repository contains source patches and documentation, not the vanilla game source or compiled game HTML.