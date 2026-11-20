# DoL Mara Mod

A Yareth-style source modification that adds Mara as a named NPC and Love Interest to **vanilla Degrees of Lewdity 0.5.13.8**.

## Project status

- **v0.1.0:** Base Mara NPC, shop, house work, relationships, and initial scenes. User confirmed it works in-game.
- **v0.1.1:** Native stat feedback.
- **v0.1.2:** Readable reward-line layout.
- **v0.1.3:** Persistent visits to both Mara locations after the first meeting.
- **v0.1.4:** Daily location schedule. Mara is at the shop from 09:00 to 13:59 and at home during other hours. The other location displays an absence notice rather than allowing interaction.

## Current features

- Mara registered in the named-NPC and Love Interest systems.
- New-save initialization and existing-save migration hook.
- Love, Trust, and Dominance relationship support and Cheat Menu controls.
- First meeting through the Danube house event or the pet shop.
- Both shop and home remain discoverable after meeting Mara.
- Mara is only interactable at her current scheduled location.
- At the house during shop hours, the message reads: "No one is home. Mara is at the shop."
- At the shop outside shop hours, the player is directed to her home on Danube Street.
- Shop and house work tasks with vanilla money rewards and native stat feedback.
- Initial romance, private collection, and Handler/Pet proposal scenes.

## Repository layout

- Base source patch v0.1.0: patches/Mara_v0.1.0.patch
- Stat feedback patch v0.1.1: patches/Mara_v0.1.1-StatFeedback.patch
- Reward layout patch v0.1.2: patches/Mara_v0.1.2-StatLayout.patch
- Persistent visit patch v0.1.3: patches/Mara_v0.1.3-AlwaysAvailable.patch
- Location schedule patch v0.1.4: patches/Mara_v0.1.4-ShopSchedule.patch
- Patch instructions: patches/README.md
- Mara design document: docs/Mara_Design.md
- Runtime test plan: docs/TEST_PLAN.md
- Changelog: CHANGELOG.md

The patches modify vanilla source files directly. This is **not** a ModLoader package. The repository does not include the vanilla game source or compiled game HTML.

## Build

Start with a clean vanilla 0.5.13.8 source tree. Apply patches v0.1.0, v0.1.1, v0.1.2, v0.1.3, and v0.1.4 in that order using patches/README.md. Compile with the source tree's Tweego-based compile.sh.

Do not apply these patches to another DoL version without reviewing source differences.

## Known limitations

- Mara's shop is a passage linked from Shopping Centre, not an independent map node.
- Her current daily schedule uses the established 09:00-14:00 shop hours every day.
- Work activities are fixed task choices, not a full random shift/event system.
- No custom art is included.
- v0.1.4 compiles and both patch paths verify, but the scheduled presence/absence messages need in-game confirmation.

## License and upstream assets

This repository contains source patches intended to be applied to a separately obtained copy of DoL 0.5.13.8. It does not redistribute the vanilla game source or compiled game HTML. Respect the game's upstream license and asset permissions when distributing derivatives.