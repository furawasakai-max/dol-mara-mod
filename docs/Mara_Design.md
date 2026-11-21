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