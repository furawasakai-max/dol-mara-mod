# Applying the Mara source patches

Target: vanilla Degrees of Lewdity 0.5.13.8.

1. Obtain and extract a clean, unmodified 0.5.13.8 source tree.
2. Apply the base patch:

   ```sh
   patch --dry-run -p1 -i /path/to/Mara_v0.1.0.patch
   patch -p1 -i /path/to/Mara_v0.1.0.patch
   ```

3. Apply the stat feedback update on top of v0.1.0:

   ```sh
   patch --dry-run -p1 -i /path/to/Mara_v0.1.1-StatFeedback.patch
   patch -p1 -i /path/to/Mara_v0.1.1-StatFeedback.patch
   ```

4. Compile using the source tree's Tweego-based `compile.sh`.

The v0.1.1 patch is incremental. It expects the v0.1.0 changes to be present first. Do not apply it directly to an unmodified vanilla source tree.

The update uses built-in DoL stat feedback macros: `glove`, `gglove`, `ggglove`, `gtrust`, `ggtrust`, `gdom`, and `ggdom`. Cash rewards continue to use the vanilla `moneyGain` widget and now show a leading plus sign.

Keep an untouched copy of the base source and back up saves before testing. Test migrated saves on copies. Recheck the stat displays with Blind Stats both off and on.
