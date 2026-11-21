# Mara NPC integration map (v0.1.10)

This release retains vanilla named-NPC integration and adds a Handler/Pet house routine using the existing relationship state.

| Subsystem | Implementation |
|---|---|
| Named NPC data | Mara remains in $NPCName / $NPCNameList with named-NPC defaults and versioned initialization. |
| Status / schedule | maraSchedule() and maraStatusCheck() use vanilla statusCheck(). Mara can be at the shop, home, or Ocean Breeze Cafe. |
| Love Interest | isPossibleLoveInterest() and vanilla loveInterestAdd connect Mara to Attitudes. |
| Social panel | Mara appears in Primary Relationships after meeting her; Love, Trust, and Dominance are displayed. |
| Journal | Tracks work, accepted housework tea breaks, completed cafe conversations, and relationship progression. |
| Cafe conversation | One 30-minute action randomly selects pets, the player's life, or the weather. |
| Cafe departure | The post-chat 25% goodbye chance and automatic 19:00 departure remain unchanged. |
| Handler/Pet progression | The accepted proposal adds a later house-visit confirmation, collar inspection scene, and four house rules. |
| House outfit | maraPetHousewear uses vanilla undress and neckwear widgets with a dedicated maraHouse clothing-storage key. |
| Outfit restoration | maraPetHouseLeave restores the stored outfit when the player exits Mara's home. |
| Save compatibility | petRulesEstablished, petHouseDressed, and petNeckWasNaked are initialized safely; objectVersion.mara advances to 6. |

The house rules apply only while the player is in Mara's home. The player can defer the second confirmation or stop before the collar scene. A neck item marked cursed by vanilla cannot be replaced, so an already-locked item is left in place. The vanilla persistent-npcs.twee remains unchanged because Mara is a named NPC, not a generated NPC.