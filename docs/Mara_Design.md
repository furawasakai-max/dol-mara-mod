# Mara Love Interest: night cage discipline revision (v0.1.16)

## Dawn-release bug

The v0.1.15 punishment return used `Time.date.timeStamp gte $mara.nightCageCaughtUntil or Time.hour gte 7`. The second condition was incorrect because 22:00 and 23:00 also satisfy `Time.hour >= 7`. v0.1.16 removes that condition and uses the absolute stored timestamp only.

## Multi-stage failed-escape discipline

A failed lockpick chooses either the whip or cane. Mara takes the player to the padded X-frame, checks the agreed stop signal, and secures the player with broad-lined cuffs. The scene is inspired by the multi-stage structure of Avery's vanilla dungeon event, but uses new Mara-specific, non-graphic prose.

- First round: five measured strokes, 20 minutes, one `<<masopain 15>>` effect.
- Second round: six measured strokes with a pause, 20 minutes, one `<<masopain 15>>` effect.
- Final round: three last strokes, 10 minutes, one `<<masopain 15>>` effect.

Each round has a stop/release link. Stopping ends the session early but does not clear the failed-escape lockout. Each round's pain effect has a daily guard so revisiting a passage does not apply it twice.

## Exact one-hour timing

The completed route is 5 minutes to the dungeon + 20 + 20 + 10 minutes for the rounds + 5 minutes back to the cage = 60 minutes. After return, the current timestamp is compared with the stored next-07:00 release time. Before that time the cage is relocked; at or after that time Mara unlocks it and removes the lead.

## Save compatibility

No new persistent save field is added. The prior `nightCageCaughtUntil` migration remains; `objectVersion.mara` remains 10.

## Stay-at-home orders (v0.1.17)

When the player has established the Handler/Pet arrangement, Mara is not available in her house while her schedule places her at the pet shop or Ocean Breeze Cafe. The player can still enter the empty house. While Mara is away, the empty-house page only offers a waiting-place selection or leaving; normal pet-room activities and Mara's discipline-room interaction are unavailable.

Before the 09:00 shop shift, the player can choose to stay until Mara returns at 14:00. Between 14:00 and 16:59, the player can choose to stay for a possible cafe visit. The existing 40% daily cafe roll determines whether Mara actually goes; on a successful roll she returns at 19:00. If the player enters while Mara is already away and no assignment is active, a note left by Mara initiates the same random assignment.

Mara randomly selects one greeting position: by the front door, inside the cushioned cage, or in the discipline room. The player's chosen position is recorded and compared with Mara's order on return. Matching positions end normally. A mismatch, or leaving the house while an assignment is active, triggers a discipline-room reprimand when Mara returns or when the player next visits after her return.

The reprimand uses a randomly selected whip or cane and three timed rounds. The completed route is 5 minutes to the room, three 15-minute rounds, and 10 minutes back to the pet room. Each round has one guarded Masochism-pain effect and a stop/release choice. The waiting and punishment state is saved on Mara, survives reloads, and is cleared when the reprimand ends.

Save migration initializes the new waiting fields and advances `objectVersion.mara` to 11.
