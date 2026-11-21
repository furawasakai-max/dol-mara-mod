# Mara Love Interest

## Pet-house progression

The existing Handler/Pet proposal and its unlock requirements remain unchanged. After accepting the proposal, the player returns for a second confirmation. The collar inspection and four house rules are established in v0.1.10. While inside Mara's home, the player uses the house outfit and collar; leaving restores the previously stored clothes and neckwear.

## Pet-room hub

Once the rules are established, Mara's house opens to a dedicated pet-room hub instead of making housework the primary activity.

- **Cushion:** the player can spend ten minutes waiting for Mara's next instruction.
- **Pet bowl:** once per day, Mara serves a simple meal in a low bowl. Eating takes ten minutes and reduces Hunger by 500 and Stress by 3.
- **Cushioned cage:** a separate sleep point with the vanilla one-to-eight-hour and Just sleep options. It uses the normal sleep, waking, and sleep-effect systems.
- **Command training:** once per day Mara leads the player through Down, Heel, Stay, and Come commands. The player gets down on all fours and crawls around the room while following a lead clipped to the collar. The lead is removed when the session ends. Completion grants +2 Mara Dominance and +1 Mara Trust. The player may stop at any stage; stopping grants no completion reward.
- **Housework:** chores remain available, but are a separate optional activity. In pet mode, completing a task returns the player to the pet room rather than outside.

## Save compatibility

v0.1.11 adds `petTrainingSessions`, initializes it to zero for existing saves, and advances `objectVersion.mara` to 7. Daily activity flags are stored under `$daily.mara` and reset with the game's daily state.

## Existing systems retained

Mara's Pet Shop entry, named-NPC status and schedule, Love Interest integration, Social and Journal entries, housework reward values, tea break, Ocean Breeze Cafe appearance and random conversation topics, and the previous pet-house outfit handling are unchanged.

## Relevant source files

- `game/04-Variables/variables-maraUpdate.twee`: save migration, house outfit widgets, pet-room hub, bowl, cage sleep, and command-training passages.
- `game/overworld-town/loc-danube-homes/work.twee`: house entry and optional housework routing.
- `game/03-JavaScript/named-npc.js`: Mara's shared status and schedule.
- `game/base-system/bdsm.twee`: vanilla leash attachment and detachment widgets.
- `game/base-system/sleep.twee`: vanilla sleep-hour handling.
- `game/overworld-town/loc-home/widgets.twee`: vanilla sleep-duration link generator.