# Mara Love Interest: Pet-play event design (v0.1.12)

## Cushion waiting

Each ten-minute cushion wait rolls a 40% chance of a random order. The selected order is Paw, Down/Stay, Come, Fetch, Grooming, Place, or a short Heel follow. The player can follow the order (five additional minutes) or end the wait. A failed roll remains a quiet waiting scene with Mara checking comfort.

## Random training

The existing daily training entry point remains once per in-game day. Starting it selects one of seven lessons: basic obedience, Heel, Paw, Fetch, Place, Grooming Manners, or Settle. The player may stop before completion. Completion retains +2 Mara Dominance and +1 Trust; stopping grants no completion reward. The lead is detached at both endpoints.

## Care and safety details

Training text uses the soft mat/rug/cushion, short crawling durations, a slack lead, and verbal/hand cues instead of neck pressure. It includes a stop link and ends with water and a comfort check. Pet-play roleplay does not remove consent or the ability to stop.

## Save compatibility

No new persistent data fields are introduced. The `objectVersion.mara` marker advances to 8.

## Relevant source files

- `game/04-Variables/variables-maraUpdate.twee`: cushion random order, random training lessons, training completion and stop passages.
- `game/overworld-town/loc-danube-homes/work.twee`: short Mara home-entry greeting update.