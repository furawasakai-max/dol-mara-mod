# Changelog

## v0.1.3 - Persistent visits and welcoming dialogue

- Meeting Mara at either her pet shop or her Danube Street home now unlocks repeat visits to both locations.
- Keeps the Mara's Pet Shop link available in Shopping Centre after the first meeting, regardless of time.
- Removes the shop-hours restriction from Mara's shop passage and work menu after the first meeting.
- Adds a permanent Mara's home destination to Danube Street after the first meeting.
- Adds a dedicated repeat-visit passage for the house.
- Rewrites the first-meeting and return dialogue at both places to welcome the player and invite them to help.
- Preserves existing task options, time costs, money rewards, and relationship gains.

Validation:
- Cumulative v0.1.3 patch applies to clean vanilla 0.5.13.8 source.
- Cumulative v0.1.3 source compiled with Tweego.
- Incremental v0.1.3 patch applies over the v0.1.2 source tree and reproduces the three changed source files byte-for-byte.
- In-game testing of the newly added repeat visits remains outstanding.

## v0.1.2 - Reward stat layout

- Moved stat and cash feedback below the narrative, onto a separate reward line.
- Replaced repeated plus indicators for +2/+3 with a single positive indicator for each changed stat.
- Added whitespace between the stat feedback and money amount.
- Kept all underlying Love, Trust, Dominance, and money values unchanged.

## v0.1.1 - Native stat feedback

- Added visible Love feedback to Mara's shop introduction.
- Added Love, conditional Trust, and Dominance feedback to shop work rewards.
- Added Love and conditional Trust feedback to Danube house-work rewards.
- Reused DoL's native stat feedback macros, preserving Blind Stats behaviour.

## v0.1.0 - Mara alpha

- Added Mara as a named NPC and Love Interest.
- Added a Danube Street house-work encounter and a pet shop passage.
- Added basic work rewards, relationship stats, Cheat Menu controls, and initial relationship scenes.
- User confirmed that the base alpha works in-game.