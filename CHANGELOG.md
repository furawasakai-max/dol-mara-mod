# Changelog

## v0.1.5 - Shopping Centre Pet Shop Entry

- Removed the additional Mara Pet Shop shortcut above the Shopping Centre description.
- Replaced the existing vanilla Pet shop entry in the main-floor shop list with Mara's Pet Shop, in the original position.
- Preserved the original pet-shop icon.
- Updated the night/exposed shop-list entry to point to the Mara Pet Shop passage too.
- Added the vanilla get-out icon to each Leave the shop action, including when Mara is at home.
- Kept Mara's schedule, work tasks, time costs, and rewards unchanged.

Validation:
- Tweego compilation succeeded.
- Incremental v0.1.5 patch applies over v0.1.4 with zero fuzz.
- Cumulative v0.1.5 patch applies to clean vanilla 0.5.13.8 with zero fuzz.
- Compiled HTML contains Mara's Pet Shop in the existing shop-list position and the standard get-out icon.
- In-game visual confirmation remains recommended.

## v0.1.4 - Daily shop / home schedule

- Mara works at the pet shop from 09:00 until 14:00.
- During shop hours, visiting her Danube Street home displays: "No one is home. Mara is at the shop."
- Outside shop hours, Mara is at home and can be visited there.
- During home hours, the shop displays a notice that Mara is at home on Danube Street.
- The random first house introduction only appears while Mara is at home.
- Both locations remain available after the player has met Mara, but interaction follows her current location.

## v0.1.3 - Persistent visits and welcoming dialogue

- Meeting Mara at either her pet shop or her Danube Street home unlocks repeat visits to both locations.
- Rewrites first-meeting and return dialogue to welcome the player and invite them to help.
- Preserves existing work choices, time costs, money rewards, and relationship gains.

## v0.1.2 - Reward stat layout

- Moved stat and cash feedback below the narrative onto a separate reward line.
- Replaced repeated plus indicators for +2/+3 with one positive indicator per changed stat.
- Added whitespace between relationship feedback and money.
- Kept all underlying values unchanged.

## v0.1.1 - Native stat feedback

- Added visible Love, conditional Trust, and Dominance feedback to Mara's shop and house interactions.
- Reused vanilla stat display macros, preserving Blind Stats behaviour.

## v0.1.0 - Mara alpha

- Added Mara as a named NPC and Love Interest.
- Added a Danube Street house-work encounter and a pet shop passage.
- Added basic work rewards, relationship stats, Cheat Menu controls, and initial relationship scenes.
- User confirmed that the base alpha works in-game.