# DoL Mara Mod v0.1.10

A Yareth-style direct source modification for vanilla **Degrees of Lewdity 0.5.13.8**.

## v0.1.10: Pet House Rules

After accepting Mara's Handler/Pet proposal, returning to Mara's house now presents a separate option to reaffirm the arrangement. If the player agrees again, Mara's tone changes from cheerful to firm and authoritative. She orders the player to undress, wear her black leather collar, crawl on all fours, and submit to a non-explicit inspection.

Mara then explains four house rules:

1. The player speaks only when Mara allows it.
2. The player stays naked and collared for the duration of each visit to Mara's home.
3. The player follows Mara's instructions.
4. Breaking the rules or disobeying Mara results in punishment, within the boundaries agreed to by both characters.

The player can defer the second confirmation or stop before the collar scene. The rules apply inside Mara's house. On later visits, the house outfit is reapplied automatically, and the player's prior clothing is restored when leaving.

The update adds three save fields and advances objectVersion.mara to 6. Existing Handler/Pet unlock requirements are unchanged.

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
- v0.1.10: Handler/Pet reaffirmation, collar inspection scene, house rules, repeat-visit outfit handling, and save migration.

## Installation

### Clean vanilla 0.5.13.8

Apply the incremental patches in version order, from v0.1.0 through v0.1.10. The patch files are in the repository's patches folder. For a single-patch clean install, use Mara_v0.1.10-Full.patch from the downloadable v0.1.10 source ZIP.

### Existing v0.1.9 source tree

Use only patches/Mara_v0.1.10-PetHouseRules.patch:

    patch --dry-run -p1 -i patches/Mara_v0.1.10-PetHouseRules.patch
    patch -p1 -i patches/Mara_v0.1.10-PetHouseRules.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.10 bash compile.sh

Do not apply the incremental patch directly to clean vanilla source. Back up your save before testing.

## Validation

- Tweego compilation succeeded for v0.1.10.
- The incremental patch applies to v0.1.9 source with zero rejects and reproduces both updated source files byte-for-byte.
- The cumulative full patch applies to clean vanilla 0.5.13.8 with zero rejects and reproduces the updated Mara source files.
- Save migration defaults all new fields without resetting existing Mara progress.
- Browser runtime testing is still needed for the new house scene, clothing restoration, and save/reload behaviour.

The repository contains source patches and documentation, not the vanilla game source or compiled game HTML.