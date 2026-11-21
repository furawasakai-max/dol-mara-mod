# Mara House-work Rest Event (v0.1.7)

## Design

After each completed house-work task, the game rolls a 1-in-4 chance to show Mara's rest offer. The offer can appear after:
- Organize Pet Supplies
- Clean Animal Equipment
- Prepare Food Supplies

It does not appear during Mara's shop work.

## Scene

Mara notices the player has been working steadily and asks them to sit down for a few minutes while she makes tea. She brings two cups and sits with the player while they take a short break.

## Player choices

- Accept her offer of tea: play the tea scene, apply the vanilla tea prop, reduce Stress by 6, increase Mara Love by 1, and increment the accepted tea-break counter.
- Thank her and finish up: return to Danube Street with no additional effects.

## Balance

The tea break is included in the work visit, so it does not consume additional time. Task time, payment, and ordinary relationship rewards remain unchanged. The event counter is stored in $mara.restBreaks and displayed in the Mara Journal section.

## Compatibility

The v0.1.7 initializer creates restBreaks for new saves and adds it with a zero default to existing Mara saves. It does not reset other Mara variables.