# DoL Mara Mod

A Yareth-style source modification that adds Mara as a named NPC and Love Interest to **vanilla Degrees of Lewdity 0.5.13.8**.

## Project status

**v0.1.0 alpha:** The user has confirmed that the base mod works in-game.

**v0.1.1:** Added native relationship and money gain feedback.

**v0.1.2:** Reformatted reward feedback so it appears on its own line, with one plus/minus sign per stat and clear spacing around the cash reward. Tweego compilation and incremental patch application succeeded. The revised visual layout still needs in-game confirmation.

## Current features

- Mara registered in the named-NPC and Love Interest systems.
- New-save initialization and existing-save migration hook.
- Love, Trust, and Dominance relationship support.
- Cheat Menu controls for Mara's relationship stats.
- Danube house introduction event.
- Pet shop passage linked from Shopping Centre (09:00-14:00).
- House and shop tasks with vanilla money rewards.
- Relationship and cash feedback on Mara's shop and house work.
- Initial romance, private collection, and Handler/Pet proposal scenes.

## Repository layout

- [Base source patch v0.1.0](patches/Mara_v0.1.0.patch): unified diff against vanilla 0.5.13.8.
- [Stat feedback patch v0.1.1](patches/Mara_v0.1.1-StatFeedback.patch): apply after v0.1.0.
- [Reward layout patch v0.1.2](patches/Mara_v0.1.2-StatLayout.patch): apply after v0.1.1.
- [Patch instructions](patches/README.md): application and compatibility instructions.
- [Mara design document](docs/Mara_Design.md): original character, progression, and implementation notes.
- [Runtime test plan](docs/TEST_PLAN.md): new-save, existing-save, and stat feedback checks.
- [Changelog](CHANGELOG.md): release notes.

The patch modifies vanilla source files directly. It is **not** a ModLoader package. It does not include the vanilla game source or compiled game HTML.

## Build

Start with a clean vanilla DoL 0.5.13.8 source tree. Apply v0.1.0, then v0.1.1, then v0.1.2 in that order using the instructions in [patches/README.md](patches/README.md). Compile with the source tree's Tweego-based `compile.sh` script.

Do not apply these patches to another DoL version without reviewing the source differences.

## Known limitations

- Pet shop is a passage link, not a separately registered map node.
- Work activities are simple choice passages, not a fully balanced shift/event system.
- House and shop first-meeting flags are separate.
- No custom art is included.
- The private collection is an introductory scene, not a complete equipment mechanic.
- The v0.1.2 reward layout has compile and patch-application validation but still needs an in-game visual check.
- Some features in the original design document remain planned rather than implemented in this alpha.

## License and upstream assets

This repository contains source patches intended to be applied to a separately obtained copy of DoL 0.5.13.8. It does not redistribute the vanilla game source or compiled game HTML. Respect the game's upstream license and asset permissions when distributing derivatives.
