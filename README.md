# DoL Mara Mod v0.1.9

A Yareth-style direct source modification for vanilla **Degrees of Lewdity 0.5.13.8**.

## v0.1.9: Random cafe conversation topic

Mara's Ocean Breeze Cafe interaction now follows the conversation pattern used by Avery's mansion conversations. The player no longer chooses the subject from a three-option menu.

When Mara is present, the player chooses one action, **Sit and chat with Mara (0:30)**. After the 30-minute time passage, the game randomly selects one of three topics:

1. Pets and the adorable animals Mara cares for at her shop.
2. The player's life, with Mara asking how things have been and listening to the answer.
3. The weather and casual conversation over coffee.

Each completed conversation still grants +1 Mara Love and +1 Mara Trust. The existing post-chat 25% goodbye chance, automatic 19:00 departure, cafe availability roll, away messages, and Journal counter are unchanged. Continuing for another chat rolls a fresh random topic.

## Release history

- v0.1.0: Base Mara NPC, shop, house work, relationship stats, and early scenes.
- v0.1.1: Native relationship stat feedback.
- v0.1.2: Separate reward line and single stat indicators.
- v0.1.3: Persistent access to both Mara locations after first meeting.
- v0.1.4: Daily shop/home schedule.
- v0.1.5: Mara's Pet Shop replaces the vanilla Pet Shop row in Shopping Centre.
- v0.1.6: Named-NPC status, Attitudes, Social, Journal, and save migration integration.
- v0.1.7: Random housework rest and tea interruption.
- v0.1.8: Random evening cafe appearance and three conversation topics.
- v0.1.9: Cafe chat automatically selects a random conversation topic, following Avery's mansion chat pattern.

## Installation

### Clean vanilla 0.5.13.8

Apply the incremental patches in version order, from v0.1.0 through v0.1.9. The patch files are in the repository's `patches/` folder. For a single-patch clean install, use `Mara_v0.1.9-Full.patch` from the downloadable v0.1.9 source ZIP.

### Existing v0.1.8 source tree

Use only `patches/Mara_v0.1.9-RandomCafeTopic.patch`:

    patch --dry-run -p1 -i patches/Mara_v0.1.9-RandomCafeTopic.patch
    patch -p1 -i patches/Mara_v0.1.9-RandomCafeTopic.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.9 bash compile.sh

Do not apply the incremental patch directly to clean vanilla source. Back up your save before testing.

## Validation

- Tweego compilation succeeded.
- The incremental patch applies to v0.1.8 source with zero rejects and reproduces the updated Mara passage file byte-for-byte.
- The cumulative v0.1.8 base patch plus v0.1.9 update applies to clean vanilla 0.5.13.8 with zero rejects and reproduces all modified source files byte-for-byte.
- The compiled source contains a single 30-minute chat action and randomly selects among the three existing conversation subjects.
- Browser runtime testing is still needed to confirm random dialogue selection and repeated chat flow in-game.

The repository contains source patches and documentation, not the vanilla game source or compiled game HTML.