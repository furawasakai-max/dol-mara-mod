# Applying Mara v0.1.10

Target: vanilla Degrees of Lewdity 0.5.13.8.

## Clean installation

For a clean vanilla source tree, apply the incremental patches in version order, from v0.1.0 through v0.1.10. The patch files are listed in this folder. Alternatively, use the cumulative Mara_v0.1.10-Full.patch from the downloadable v0.1.10 source ZIP.

## Upgrade from v0.1.9

For a source tree already patched through v0.1.9, apply only:

    patch --dry-run -p1 -i /path/to/Mara_v0.1.10-PetHouseRules.patch
    patch -p1 -i /path/to/Mara_v0.1.10-PetHouseRules.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.10 bash compile.sh

The incremental patch changes only:
- game/04-Variables/variables-maraUpdate.twee
- game/overworld-town/loc-danube-homes/work.twee

Do not apply the incremental patch directly to clean vanilla source.

## Behaviour

- After accepting the Handler/Pet proposal, returning to Mara's house reveals a second-confirmation option.
- The affirmative response leads to Mara's firm collar demand, an undressing and crawling scene, and a non-explicit inspection.
- Mara then states the four house rules: speak only when permitted, stay naked and collared in her house, obey her instructions, and expect punishment for breaking the rules.
- The player can defer the confirmation or stop before the collar scene.
- After the rules are established, Mara reapplies the house outfit on future visits and restores the previous outfit when the player leaves.
- Existing relationship unlock requirements, housework rewards, and cafe interactions remain unchanged.

Compilation and patch application were verified. The new scene still needs in-game testing.