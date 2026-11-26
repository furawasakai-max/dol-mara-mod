# DoL Mara Mod v0.1.18

A Yareth-style direct source modification for vanilla **Degrees of Lewdity 0.5.13.8**.

## v0.1.18: Automatic vanilla-style Willpower checks

Updates Mara's 30-minute endurance event so each five-minute interval automatically performs a standard DoL Willpower check when the interval passage loads. The player no longer has to select a separate “Make the Willpower check” option.

- Six five-minute intervals, for a total of 30 in-game minutes.
- Each interval adds 500 player arousal.
- Uses the game's native willpowerdifficulty widget, which sets the willpowerSuccess variable and displays the normal skill-check difficulty according to the player's settings.
- Difficulty scales by interval: the random check's upper bound rises from 500 at interval one to 1000 at interval six.
- Success automatically displays the result and offers the next five-minute interval; passing interval six completes the event.
- Failure automatically enters the existing failure outcome and opens the discipline-room route.
- The player can still stop the session between checks.

## Installation

This patch is incremental from the v0.1.16 source baseline. It contains the v0.1.17 endurance event plus the v0.1.18 automatic-check correction.

### Existing v0.1.16 source tree

    patch --dry-run -p1 -i patches/Mara_v0.1.18-EnduranceWillpowerCheck.patch
    patch -p1 -i patches/Mara_v0.1.18-EnduranceWillpowerCheck.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.18 bash compile.sh

### Clean vanilla 0.5.13.8

Apply the v0.1.16 cumulative patch first, then the v0.1.18 incremental patch:

    patch --dry-run -p1 -i patches/Mara_v0.1.16-Full.patch
    patch -p1 -i patches/Mara_v0.1.16-Full.patch
    patch --dry-run -p1 -i patches/Mara_v0.1.18-EnduranceWillpowerCheck.patch
    patch -p1 -i patches/Mara_v0.1.18-EnduranceWillpowerCheck.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.18 bash compile.sh

Do not apply the v0.1.18 patch on top of v0.1.17; it already contains the v0.1.17 event changes. Back up saves and test on a copy.

## Validation

- Tweego compilation succeeded for the v0.1.18 development tree.
- The event now uses DoL's native Willpower difficulty widget and willpowerSuccess result instead of a custom skill comparison and a separate check-selection passage.
- Browser runtime testing remains outstanding for interval timing, check difficulty, success/failure transitions, and stop handling.

## Source and license

The repository contains source patches intended to be applied to a separately obtained copy of DoL 0.5.13.8. It does not include vanilla game source or compiled HTML. Respect the game's upstream license and asset permissions when distributing derivatives.
