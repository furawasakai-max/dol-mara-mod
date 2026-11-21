# DoL Mara Mod v0.1.12

A Yareth-style direct source modification for vanilla **Degrees of Lewdity 0.5.13.8**.

## v0.1.12: Random Pet-Play Events and Training

Each ten-minute cushion wait now has a **40% chance** to trigger a short, random pet-play order. Possible orders include Paw, Down/Stay, Come, Fetch, Grooming, Place, and a short Heel follow. The player can follow the instruction or end the wait.

Starting the daily training session selects one random lesson from seven options: basic obedience, Heel, Paw, Fetch, Place, Grooming Manners, or Settle. Training remains once per in-game day. Completing a lesson preserves the existing +2 Mara Dominance and +1 Mara Trust reward. The player can stop before or during training, which removes the lead without awarding the completion reward.

The new event text keeps crawling brief and on soft surfaces, uses a slack lead rather than neck pressure, and includes water and a comfort check at the end. See [Pet-play research notes](docs/PET_PLAY_RESEARCH.md) for curated sources and the design mapping.

## Release history

- v0.1.0: Base Mara NPC, shop, house work, relationship stats, and early scenes.
- v0.1.1: Native relationship stat feedback.
- v0.1.2: Separate reward line and single stat indicators.
- v0.1.3: Persistent access to both Mara locations after first meeting.
- v0.1.4: Daily shop/home schedule.
- v0.1.5: Mara's Pet Shop replaces the vanilla Pet Shop row in Shopping Centre.
- v0.1.6: Native named-NPC integration and save migration.
- v0.1.7: Housework tea break.
- v0.1.8: Random evening cafe appearance and conversations.
- v0.1.9: Random cafe conversation topic selection.
- v0.1.10: Handler/Pet reaffirmation, collar inspection, and house rules.
- v0.1.11: Pet-room hub, cushion, bowl, cage sleep, and initial training.
- v0.1.12: Random cushion orders and seven random training lessons.

## Installation

### Clean vanilla 0.5.13.8

Use the cumulative full patch from the downloadable v0.1.12 source ZIP:

    patch --dry-run -p1 -i Mara_v0.1.12-Full.patch
    patch -p1 -i Mara_v0.1.12-Full.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.12 bash compile.sh

### Existing v0.1.11 source tree

Use only `patches/Mara_v0.1.12-RandomPetPlay.patch`:

    patch --dry-run -p1 -i patches/Mara_v0.1.12-RandomPetPlay.patch
    patch -p1 -i patches/Mara_v0.1.12-RandomPetPlay.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.12 bash compile.sh

Do not apply the incremental patch directly to clean vanilla source. Back up your save before testing.

## Validation

- Tweego compilation succeeded.
- The incremental patch applies to v0.1.11 source with zero rejects and reproduces both changed source files byte-for-byte.
- The cumulative full patch applies to clean vanilla 0.5.13.8 with zero rejects; all 17 modified/added source files match the final working tree byte-for-byte.
- The full-patch verification tree compiled successfully.
- Static passage checks passed and `git diff --check` is clean.
- Browser runtime testing remains outstanding for actual random rolls, leash state, stop links, and daily reset behaviour.

The repository contains source patches and documentation, not the vanilla game source or compiled game HTML.