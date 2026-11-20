# DoL Mara Mod

A Yareth-style source modification that adds Mara as a named NPC and Love Interest to **vanilla Degrees of Lewdity 0.5.13.8**.

## Project status

**Alpha source patch.** Tweego compilation succeeded. Browser runtime testing has not yet been completed. Back up saves and test using copies.

## Current alpha features

- Mara registered in the named-NPC and Love Interest systems.
- New-save initialization and existing-save migration hook.
- Love, Trust, and Dominance relationship support.
- Cheat Menu controls for Mara's relationship stats.
- Danube house introduction event.
- Pet shop passage linked from Shopping Centre (09:00-14:00).
- House and shop tasks with vanilla money rewards.
- Initial romance, private collection, and Handler/Pet proposal scenes.

## Repository layout

- [Source patch](patches/Mara_v0.1.0.patch): unified diff against vanilla 0.5.13.8.
- [Patch instructions](patches/README.md): application and compatibility instructions.
- [Mara design document](docs/Mara_Design.md): original character, progression, and planned implementation notes.
- [Runtime test plan](docs/TEST_PLAN.md): new-save and existing-save test checklist.

The patch modifies vanilla source files directly. It is **not** a ModLoader package. It does not include the vanilla game source or the compiled game HTML.

## Build

Start with a clean vanilla DoL 0.5.13.8 source tree. Apply the patch using the instructions in [patches/README.md](patches/README.md), then compile with the source tree's Tweego-based `compile.sh` script.

Do not apply it to another game version without reviewing the source differences.

## Known limitations

- Pet shop is a passage link, not a separately registered map node.
- Work activities are simple choice passages, not a fully balanced shift/event system.
- House and shop first-meeting flags are separate.
- No custom art is included.
- The private collection is an introductory scene, not a complete equipment mechanic.
- Browser runtime testing is still required for new saves, migrated saves, event selection, Cheat Menu controls, and reward handling.
- Some features in the original design document remain planned rather than implemented in this alpha.

## License and upstream assets

This repository contains a source patch intended to be applied to a separately obtained copy of DoL 0.5.13.8. It does not redistribute the vanilla game source or compiled game HTML. Respect the game's upstream license and asset permissions when distributing derivatives.
