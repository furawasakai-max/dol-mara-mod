# Applying the Mara source patch

Target: vanilla Degrees of Lewdity 0.5.13.8.

1. Obtain and extract a clean, unmodified 0.5.13.8 source tree.
2. Copy `Mara_v0.1.0.patch` into the source tree root, or use its full path.
3. From the source tree root, check that the patch applies:

   ```sh
   patch --dry-run -p1 -i /path/to/Mara_v0.1.0.patch
   ```

4. Apply it:

   ```sh
   patch -p1 -i /path/to/Mara_v0.1.0.patch
   ```

5. Compile using the source tree's Tweego-based `compile.sh`.

Do not apply the patch to another DoL version without reviewing the changed source locations. Keep an untouched copy of the base source and back up saves before testing. Test migrated saves on copies.

The patch was checked against a fresh extraction of the 0.5.13.8 archive: it applied without rejects, and all ten resulting changed/added source files matched the alpha working tree. This confirms patch application, not in-browser game behaviour.
