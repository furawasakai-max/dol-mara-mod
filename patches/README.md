# Applying Mara v0.1.16

Target: vanilla Degrees of Lewdity 0.5.13.8.

## Clean installation

Use the single cumulative patch:

    patch --dry-run -p1 -i patches/Mara_v0.1.16-Full.patch
    patch -p1 -i patches/Mara_v0.1.16-Full.patch

## Upgrade from v0.1.15

For a source tree already patched through v0.1.15, apply only:

    patch --dry-run -p1 -i patches/Mara_v0.1.16-NightCageDisciplineFix.patch
    patch -p1 -i patches/Mara_v0.1.16-NightCageDisciplineFix.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.16 bash compile.sh

The incremental patch changes only `game/04-Variables/variables-maraUpdate.twee`. Do not apply it directly to clean vanilla source.

## What changed

- Removed the erroneous `or Time.hour gte 7` test. That condition treated 22:00 and 23:00 as morning.
- The cage is opened after punishment only when `Time.date.timeStamp >= $mara.nightCageCaughtUntil`.
- The failed-escape punishment now has a five-minute escort, three timed rounds (20, 20, and 10 minutes), and a five-minute return, totalling exactly one hour.
- Whip or cane is selected at random. Each round has a native Masochism-pain effect and a release option remains available between rounds.
- Before 07:00, Mara returns the player to the same cage and locks it again. At or after 07:00, Mara unlocks the cage and removes the lead.

Compilation, incremental patching, and clean-install patching were verified. Runtime testing is still needed for gameplay timing and effects.