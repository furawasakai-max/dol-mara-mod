# Mara Love Interest: night cage routine (v0.1.15)

## Night entry

If the player remains in Mara's house at or after 22:00 and before 07:00, the normal pet-room menu is replaced with the night cage routine. This reuses the cushioned cage sleep point already present in the room.

## Lockpick escape

The option appears only when current Skulduggery is at least 400. The check uses the vanilla `skulduggerycheck` widget at difficulty 700. A successful attempt unlocks the cage and links to the normal house-leave passage.

A failed attempt makes noise and routes to Mara's response. The failure timestamp, `nightCageCaughtUntil`, is set to the next 07:00. This blocks repeated escape attempts and remains active across the game's daily reset.

## Failed-attempt discipline

Mara takes the player to the dungeon for a one-hour non-graphic reprimand. At the end, she attaches a lead when the worn collar supports it and returns the player to the same cushioned cage. The cage locks again if it is still before 07:00. If the one-hour passage crosses 07:00, Mara unlocks the cage on return.

## Sleep and morning

Choosing sleep uses the native DoL sleep widget and runs its normal sleep, waking, and sleep effects. The passage calculates whole sleep hours and then advances any remaining minutes to exactly 07:00 using the native time system. Mara arrives at dawn, unlocks the cage, detaches an attached lead, clears the caught timestamp, and returns the player to the pet-room menu.

## Save compatibility

The v0.1.15 migration adds `nightCageCaughtUntil` with a default of 0 and advances `objectVersion.mara` to 10. Existing Mara relationship, pet-house, training, and discipline-room progress is preserved.

## Relevant source

- `game/04-Variables/variables-maraUpdate.twee`: night check, lockpick, failed attempt, discipline, sleep, and dawn unlock passages.