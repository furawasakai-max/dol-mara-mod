# DoL Mara Mod

A Yareth-style source modification that adds Mara as a named NPC and Love Interest to **vanilla Degrees of Lewdity 0.5.13.8**.

## Project status

**Alpha source patch.** Tweego compilation succeeded. Browser runtime testing has not yet been completed. Back up saves and test using copies.

## Current features

- Mara registered in the named NPC and Love Interest systems.
- New-save initialization and existing-save migration hook.
- Love, Trust, and Dominance relationship support.
- Cheat Menu controls for Mara's relationship stats.
- Danube house introduction event.
- Pet shop passage linked from Shopping Centre (9:00-14:00).
- House and shop tasks with vanilla money rewards.
- Initial romance, private collection, and Handler/Pet proposal scenes.

## Source layout

The patch modifies vanilla source files directly. It is **not** a ModLoader package.

- `game/04-Variables/variables-maraUpdate.twee`: Mara state and scene passages.
- `game/04-Variables/variables-static.twee`, `npcNamed.twee`, `variables-start2.twee`, `variables-versionUpdate.twee`: registration and initialization/migration.
- `game/base-system/named-npcs.twee`, `widgets.twee`, `overlays/cheats.twee`: relationship integration and Cheat Menu.
- `game/overworld-town/loc-danube-homes/work.twee`, `loc-shop/main.twee`: house and pet shop content.
- `Mara.md`: detailed patch notes and limitations.

## Build

Apply the patch files to the matching vanilla DoL 0.5.13.8 source tree, then compile with the project's Tweego-based `compile.sh` script. Do not apply to another game version without reviewing the source differences.

## Known limitations

- Pet shop is a passage link, not a separately registered map node.
- Work activities are simple choice passages, not a fully balanced shift/event system.
- House and shop first-meeting flags are separate.
- No custom art is included.
- Runtime testing is still required for new saves, migrated saves, event selection, Cheat Menu controls, and reward handling.

## License and upstream assets

This repository contains a source patch intended to be applied to a separately obtained copy of DoL 0.5.13.8. It does not include the vanilla game source or compiled game HTML. Respect the game's upstream license and asset permissions when distributing derivatives.
