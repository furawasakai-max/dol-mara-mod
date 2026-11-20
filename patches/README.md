# Applying the Mara source patches

Target: vanilla Degrees of Lewdity 0.5.13.8.

1. Obtain and extract a clean, unmodified 0.5.13.8 source tree.
2. Apply the base patch:

   ```sh
   patch --dry-run -p1 -i /path/to/Mara_v0.1.0.patch
   patch -p1 -i /path/to/Mara_v0.1.0.patch
   ```

3. Apply the v0.1.1 native stat feedback patch:

   ```sh
   patch --dry-run -p1 -i /path/to/Mara_v0.1.1-StatFeedback.patch
   patch -p1 -i /path/to/Mara_v0.1.1-StatFeedback.patch
   ```

4. Apply the v0.1.2 reward layout patch:

   ```sh
   patch --dry-run -p1 -i /path/to/Mara_v0.1.2-StatLayout.patch
   patch -p1 -i /path/to/Mara_v0.1.2-StatLayout.patch
   ```

5. Compile using the source tree's Tweego-based `compile.sh`.

Both update patches are incremental. v0.1.1 expects v0.1.0 to be applied first. v0.1.2 expects v0.1.1 to be applied. Do not apply either update patch directly to an unmodified vanilla source tree.

## Display behaviour

The v0.1.2 patch places the reward summary beneath the event text, with blank-line spacing before and after it. Each stat displays one sign, regardless of whether its actual change is one, two, or three points.

- Love: positive `glove Mara`; negative `llove Mara` / `lllove Mara` / `llllove Mara`.
- Trust: positive `gtrust`; negative `ltrust` / `lltrust` / `llltrust`.
- Dominance: positive `gdom Mara`; negative `ldom Mara` / `lldom Mara` / `llldom Mara`.
- Money: vanilla `moneyGain` with a visible plus sign and spacing.

These native relationship notices respect the game's Blind Stats setting. The v0.1.2 update changes presentation only; it does not change the amount of Love, Trust, Dominance, or money awarded.

Keep an untouched copy of the base source and back up saves before testing. Recheck the stat displays with Blind Stats both off and on.
