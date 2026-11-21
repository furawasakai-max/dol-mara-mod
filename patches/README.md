# Applying Mara v0.1.6

Target: vanilla Degrees of Lewdity 0.5.13.8.

## Clean installation

The cumulative `Mara_v0.1.6-Full.patch` is included in the downloadable `Mara_YarethStyle_SourcePatch_0.1.6.zip`.

From the root of a clean 0.5.13.8 source tree, after extracting the source ZIP:

    patch --dry-run -p1 -i /path/to/Mara_v0.1.6-Full.patch
    patch -p1 -i /path/to/Mara_v0.1.6-Full.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.6 bash compile.sh

## Upgrade from v0.1.5

For a source tree that already has the v0.1.5 full patch applied, download [Mara_v0.1.6-NPCIntegration.patch](Mara_v0.1.6-NPCIntegration.patch) from this folder and apply:

    patch --dry-run -p1 -i /path/to/Mara_v0.1.6-NPCIntegration.patch
    patch -p1 -i /path/to/Mara_v0.1.6-NPCIntegration.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.6 bash compile.sh

The incremental patch is not for clean vanilla source. Back up saves before testing.

## Validation summary

Both patches were applied to their respective source baselines with zero rejects. The cumulative and incremental patched files were checked against the v0.1.6 working source. Tweego compilation succeeded. This does not replace runtime testing in a browser.