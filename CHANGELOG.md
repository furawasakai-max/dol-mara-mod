# Changelog

## v0.1.7 - Mara's house-work rest break

- Added a 25% chance after each completed Danube house-work task for Mara to ask the player to take a short break.
- Mara prepares tea and sits with the player while they rest.
- The player can accept the tea or politely decline.
- Accepting tea reduces Stress by 6 and increases Mara's Love by 1.
- Added a persistent count of accepted tea breaks to Mara's Journal section.
- Added restBreaks save initialization for both new and existing Mara saves.
- Existing task times, money, and relationship rewards are unchanged; shop work is unaffected.

Validation:
- Tweego compilation succeeded.
- Incremental patch applies to v0.1.6 source with zero rejects and the changed files match byte-for-byte.
- Cumulative patch applies to clean vanilla 0.5.13.8 with zero rejects.
- In-game random event appearance and reward effects still require player testing.

## Previous releases

- v0.1.6: Named-NPC lifecycle, Attitudes, Social, Journal, and save migration integration.
- v0.1.5: Mara's Pet Shop replaces the original Pet Shop entry in Shopping Centre; standard exit icon.
- v0.1.4: Daily shop/home schedule.
- v0.1.3: Persistent visits to both Mara locations.
- v0.1.2: Readable reward feedback layout.
- v0.1.1: Native stat feedback.
- v0.1.0: Initial Mara NPC, shop, house work, relationships, and event passages.