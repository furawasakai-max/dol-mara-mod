# Mara NPC integration map (v0.1.17)

This release adds a waiting-order flow for the existing pet-house arrangement. Mara's shop/cafe schedule and all previous pet-room activities are unchanged.

| Subsystem | Implementation |
|---|---|
| Mara availability | Existing `maraSchedule()` continues to place Mara at the shop 09:00-13:59 and at Ocean Breeze Cafe 17:00-18:59 on the existing 40% daily roll. House passages no longer present Mara as available while those statuses are active. |
| Empty house | An established pet can enter while Mara is away, but only waiting-position and leave choices appear. Pet activities and discipline interactions are hidden. |
| Shop pre-departure | Between 07:00 and 08:59, Mara can assign a random position before leaving; she returns at 14:00. |
| Cafe pre-departure | Between 14:00 and 16:59, the player can choose to stay. The existing cafe daily roll decides whether Mara goes; on a successful roll she returns at 19:00. |
| Greeting position | Randomly selects front door, cushioned cage, or discipline room. The player chooses the actual position. |
| Return check | Compares `petWaitActual` with `petWaitExpected` when Mara returns. Matching positions end normally; mismatches or absence trigger discipline. |
| Absence handling | Leaving during an active order sets the actual position to 0. If the player is away when Mara returns, the return check runs on their next house visit. |
| Reprimand | Random whip/cane, three 15-minute rounds, 5-minute escort, 10-minute return. Each round has one guarded `masopain 10` effect and a stop/release choice. |
| Outfit | Pet-house clothing is applied after entering the empty house, not merely on the empty-house notice. Normal leave restores stored clothing. |
| Save compatibility | Adds waiting assignment and active-punishment fields; `objectVersion.mara` advances to 11. |

The v0.1.17 incremental patch changes only `variables-maraUpdate.twee` and the Mara section of `loc-danube-homes/work.twee`.