# Mara Love Interest: discipline room design (v0.1.13)

## Dungeon-room access

The pet-room hub links to a separate discipline room. On the first visit each in-game day, a 1-100 roll is stored under `$daily.mara.disciplineRoll`. A result of 35 or lower offers one session. This prevents repeated entry from rerolling the same day. Declining or completing the offer marks it handled for that day.

## Session selection

When an offer appears, the player chooses a whip or a cane, then confirms the session. Mara checks the agreed stop word and signal before securing the player to a padded X-frame with broad lined cuffs. The discipline itself is implied, rather than shown graphically.

A stop link remains available after restraint. Choosing it causes Mara to release the player immediately, with no explanation required and no reward. Completing the session releases the player, offers water, and awards +20 Masochism progress with the vanilla `<<masochism 20>>` widget. Both instruments award the same amount. The vanilla stat is capped at 1000; its level tier is recalculated by the game's daily effect system.

## Save compatibility

No new persistent save fields are introduced. The daily roll and handled state live under `$daily.mara`, and `objectVersion.mara` advances to 9.

## Relevant source file

- `game/04-Variables/variables-maraUpdate.twee`: pet-room link, daily random offer, tool selection, X-frame scene, stop/release, and Masochism reward.