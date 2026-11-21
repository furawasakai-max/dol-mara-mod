# Applying Mara v0.1.9

Target: vanilla Degrees of Lewdity 0.5.13.8.

## Clean installation

From clean vanilla 0.5.13.8 source, apply the v0.1.8 full patch first, then the v0.1.9 topic update:

    patch --dry-run -p1 -i /path/to/Mara_v0.1.8-Full.patch
    patch -p1 -i /path/to/Mara_v0.1.8-Full.patch
    patch --dry-run -p1 -i /path/to/Mara_v0.1.9-RandomCafeTopic.patch
    patch -p1 -i /path/to/Mara_v0.1.9-RandomCafeTopic.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.9 bash compile.sh

## Upgrade from v0.1.8

For a source tree already patched through v0.1.8, apply only:

    patch --dry-run -p1 -i /path/to/Mara_v0.1.9-RandomCafeTopic.patch
    patch -p1 -i /path/to/Mara_v0.1.9-RandomCafeTopic.patch

The incremental patch changes only game/04-Variables/variables-maraUpdate.twee. It is not for clean vanilla source.

## Behaviour

- The cafe introduction has one conversation action: **Sit and chat with Mara (0:30)**.
- After the 30-minute time passage, a random topic is selected with equal probability from pets, the player's life, or the weather.
- Each completed chat still grants +1 Mara Love and +1 Mara Trust.
- After the chat, the existing 25% chance for Mara to say goodbye remains in place. She still leaves automatically at 19:00.
- If the player chooses to continue chatting, the next 30-minute interaction rolls a new random topic.
- The cafe presence chance, schedule, away messages, and Journal conversation count are unchanged.

This uses the same overall pattern as Avery's mansion conversation: one chat action followed by a random topic selection inside the conversation passage.