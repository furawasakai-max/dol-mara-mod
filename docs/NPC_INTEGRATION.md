# Mara NPC integration map (v0.1.6)

This document maps the checklist supplied for the project to the actual vanilla 0.5.13.8 source integration.

| NPC subsystem | v0.1.6 implementation |
|---|---|
| $NPCName / $NPCNameList data | Mara is appended to setup.NPCNameList; metadata arrays and migration entry are aligned in npcNamed.twee. |
| Love Interest registration | setup.loveInterestNpc, setup.loveAlias, isPossibleLoveInterest(), and loveInterestAdd are connected. |
| Stat widgets | Mara remains whitelisted for npcincr; Love, Trust, and Dominance are clamped and displayed. Negative changes use negative npcincr values in this vanilla version. |
| Location / encounter | Mara's maraSchedule() is called through statusCheck(). Shop and Danube house passages use the shared schedule. |
| Event chain | Existing introduction, work, private collection, romance, and Handler passages remain. Romance acceptance now participates in the vanilla Attitudes selection system. |
| Journal | Mara's progression summary appears after the player has met her. |
| Character / relationship UI | Mara is added to Social's Primary Relationships after meeting her, with Love, Trust, and Dominance. |
| Save compatibility | $objectVersion.mara is set to version 2. Legacy alpha records are initialized as named NPCs while previous stat and appearance data is restored. |
| Portrait / sprites | Not implemented. No custom art was provided. |
| Combat / sex-scene hooks | Not implemented in this release. |

## Why persistent-npcs.twee is untouched

Vanilla persistent-npcs.twee handles generated NPCs through $NPCList and $per_npc. Mara is a named NPC in $NPCName and is accessed through C.npc.Mara. Her initialization belongs in the named-NPC and save-version flow, not the generated-NPC persistence path.

## Save migration behaviour

When the player has met Mara and C.npc.Mara.init is not yet 1, maraInit captures the existing Mara record, calls the vanilla initnpc widget, and then restores saved relationship/body/appearance/state fields. This lets older v0.1.5 saves receive the vanilla named-NPC initialization without wiping accumulated Love, Trust, Dominance, or progress flags.