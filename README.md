# DoL Mara Mod v0.1.17

A Yareth-style direct source modification for vanilla **Degrees of Lewdity 0.5.13.8**.

## v0.1.17: Stay-at-Home Orders

Mara is no longer available for house interactions while her schedule places her at the pet shop or Ocean Breeze Cafe. The player can still enter the empty house after accepting the Handler/Pet arrangement, but Mara's pet-room activities and discipline-room interactions are unavailable while she is out.

Before leaving for the shop, Mara can assign a waiting position. The player can choose to remain at her house and wait for her return at 14:00. Before a possible cafe visit, the player can choose to stay for that outing; the existing 40% daily cafe roll determines whether Mara actually goes. If she does, she returns at 19:00.

Mara randomly chooses one of three greeting positions:

1. Near the front door.
2. Inside the cushioned cage.
3. In the discipline room.

The player chooses where to wait and advances time until Mara returns. If the player is in the assigned position, Mara finds them there and the waiting event ends normally. If they choose another position, leave the house, or otherwise fail to be at the assigned place, Mara discovers the mismatch and takes them to the discipline room for a one-hour reprimand. The reprimand randomly uses the whip or cane, has three timed rounds, applies the vanilla Masochism-pain effect once per round, and retains a stop/release option. Leaving the house during an active instruction marks the player's position as absent; if they return after Mara's scheduled return, the mismatch is handled on their next visit.

If the player enters while Mara is already away and no instruction is active, a note left by Mara assigns a new random waiting position. The player can wait in the house or leave. The house outfit is applied only after entering and is restored when leaving.

## Schedule and behaviour

- Pet shop: 09:00-13:59; Mara returns home at 14:00.
- Ocean Breeze Cafe: 17:00-18:59 on the existing 40% daily roll; Mara returns home at 19:00.
- Before the shop shift (07:00-08:59), the pet-room hub and house entrance offer the shop waiting order.
- Before the cafe period (14:00-16:59), the player can request the cafe waiting order. If the daily cafe roll is false, Mara stays home and no away order is started.
- While Mara is away, she is not available in her house. The empty-house flow only allows the player to choose a waiting place or leave.
- The waiting assignment persists through save/reload and is checked against the scheduled return timestamp.

## Punishment flow

The full reprimand lasts 60 in-game minutes: five minutes to the discipline room, three 15-minute rounds, and ten minutes to return. The whip or cane is selected randomly. Each round's `masopain 10` effect is guarded so it cannot apply twice on save/reload. Stopping releases the player and ends the session early.

## Save compatibility

The update adds waiting-order and punishment-session fields to Mara's save data and safely defaults them for older saves. `objectVersion.mara` advances to 11. Existing relationship values, pet-house progress, cage lock state, training, and discipline-room progress are preserved.

## Release history

- v0.1.0-v0.1.9: Base Mara NPC, shop, home, relationship systems, and cafe events.
- v0.1.10: Handler/Pet reaffirmation, collar inspection, and house rules.
- v0.1.11: Pet-room hub, cushion, bowl, cage sleep, and initial command training.
- v0.1.12: Random cushion orders and seven random training lessons.
- v0.1.13: Discipline room, daily random offer, whip/cane choices, and Masochism progress reward.
- v0.1.14: Harsher dialogue throughout pet-role scenes.
- v0.1.15: Night cage after 22:00, Skulduggery escape attempt, failed-attempt punishment, and 07:00 release.
- v0.1.16: Night-cage timing fix and multi-stage failed-escape punishment.
- v0.1.17: Mara unavailable during shop/cafe shifts; random waiting positions and punishment for failing to greet her in the assigned place.

## Installation

### Clean vanilla 0.5.13.8

Use the cumulative full patch:

    patch --dry-run -p1 -i patches/Mara_v0.1.17-Full.patch
    patch -p1 -i patches/Mara_v0.1.17-Full.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.17 bash compile.sh

### Existing v0.1.16 source tree

Use only the incremental patch:

    patch --dry-run -p1 -i patches/Mara_v0.1.17-StayInHouseOrders.patch
    patch -p1 -i patches/Mara_v0.1.17-StayInHouseOrders.patch
    FORCE_VERSION=0.5.13.8-Mara-Alpha-0.1.17 bash compile.sh

Do not apply the incremental patch directly to clean vanilla source. Back up your save before testing.

## Validation

- Tweego compilation succeeded in the v0.1.17 development tree.
- The incremental patch applies to v0.1.16 source with zero rejects and reproduces both changed source files byte-for-byte.
- The cumulative patch applies directly to clean vanilla 0.5.13.8; all 17 modified/added source files match the development tree byte-for-byte.
- The clean full-patch verification tree compiles successfully.
- Static Mara passage-link checks found no missing targets or duplicate passage names.
- `git diff --check` is clean.
- In-game testing of return-position checks, daily cafe timing, and the discipline route remains outstanding.

The repository contains source patches and documentation, not vanilla game source or compiled game HTML.