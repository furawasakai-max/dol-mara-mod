# DoL Mara Mod

A Yareth-style source modification that adds Mara as a named NPC and Love Interest to **vanilla Degrees of Lewdity 0.5.13.8**.

## Project status

**v0.1.0 alpha:** The user confirmed that the base mod works in-game.

**v0.1.1:** Added native relationship and money gain feedback.

**v0.1.2:** Reformatted reward feedback with a separate reward line, one sign per stat, and clearer spacing.

**v0.1.3:** Meeting Mara at either her shop or her Danube Street home unlocks repeat visits to both locations. The shop remains available outside its usual hours, and a permanent Mara's home destination appears on Danube Street. Both locations now use welcoming dialogue that invites the player to help.

## Current features

- Mara registered in the named-NPC and Love Interest systems.
- New-save initialization and existing-save migration hook.
- Love, Trust, and Dominance relationship support and Cheat Menu controls.
- First meeting through the Danube House Knock event pool or at the pet shop during usual hours.
- Meeting Mara at either location unlocks repeat access to both her shop and home.
- Shop and work tasks remain available at any hour after the first meeting.
- Welcoming first-meeting and return dialogue at both locations.
- House and shop work tasks with vanilla money rewards and native stat feedback.
- Initial romance, private collection, and Handler/Pet proposal scenes.

## Repository layout

- Base source patch v0.1.0: patches/Mara_v0.1.0.patch
- Stat feedback patch v0.1.1: patches/Mara_v0.1.1-StatFeedback.patch
- Reward layout patch v0.1.2: patches/Mara_v0.1.2-StatLayout.patch
- Persistent availability patch v0.1.3: patches/Mara_v0.1.3-AlwaysAvailable.patch (apply after v0.1.2).
- Patch instructions: patches/README.md
- Mara design document: docs/Mara_Design.md
- Runtime test plan: docs/TEST_PLAN.md
- Changelog: CHANGELOG.md

The patches modify vanilla source files directly. This is **not** a ModLoader package. The repository does not include the vanilla game source or compiled game HTML.

## Build

For a clean vanilla 0.5.13.8 source tree, use the cumulative Mara_v0.1.3-Full.patch included in the downloadable v0.1.3 source ZIP. Alternatively, apply the four incremental patches in order as described in patches/README.md. Compile with the source tree's Tweego-based compile.sh.

Do not apply these patches to another DoL version without reviewing source differences.

## Known limitations

- Mara's shop is a passage linked from Shopping Centre, not an independent map node.
- Work activities are fixed task choices, not a full random shift/event system.
- No custom art is included.
- The new v0.1.3 cross-location return flow compiles and patch-verifies, but should still be tested in-game with a save that has met Mara at either location.

## License and upstream assets

This repository contains source patches intended to be applied to a separately obtained copy of DoL 0.5.13.8. It does not redistribute the vanilla game source or compiled game HTML. Respect the game's upstream license and asset permissions when distributing derivatives.