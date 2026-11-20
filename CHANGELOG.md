# Changelog

## v0.1.2 - Reward stat layout

- Moved stat and cash feedback below the narrative, onto a separate reward line.
- Replaced repeated plus indicators for +2/+3 with a single positive indicator for each changed stat.
- Added whitespace between the stat feedback and money amount.
- Kept all underlying Love, Trust, Dominance, and money values unchanged.
- Documented the native negative feedback macros for future choices.

Validation:
- Tweego compilation succeeded.
- The v0.1.2 incremental patch applies on top of v0.1.1 without rejects.
- The resulting three updated source files match the local v0.1.2 working tree byte-for-byte.
- In-game visual confirmation of the revised layout remains outstanding.

## v0.1.1 - Native stat feedback

- Added visible Love feedback to Mara's shop introduction.
- Added Love, conditional Trust, and Dominance feedback to shop work rewards.
- Added Love and conditional Trust feedback to Danube house-work rewards.
- Added Love and Dominance feedback to the private collection scene.
- Prefixed Mara's cash rewards with a visible plus sign.
- Reused DoL's native stat feedback macros, so relationship notices respect Blind Stats.
- Added this as an incremental patch over v0.1.0 in the repository.

## v0.1.0 - Mara alpha

- Added Mara as a named NPC and Love Interest.
- Added a Danube Street house-work encounter and a pet shop passage.
- Added basic work rewards, relationship stats, Cheat Menu controls, and initial relationship scenes.
- User confirmed that the base alpha works in-game.
- No browser test results or compatibility claim for other DoL versions are implied.
