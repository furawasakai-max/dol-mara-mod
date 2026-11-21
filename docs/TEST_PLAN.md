# Mara v0.1.9 runtime test plan

The v0.1.9 source compiles. The incremental patch applies to v0.1.8 source, and the v0.1.8 full patch followed by the v0.1.9 update applies to clean vanilla 0.5.13.8. Both routes reproduce the final source tree. Random topic selection still needs in-game confirmation.

## Single conversation action

- [ ] Visit Ocean Breeze Cafe between 17:00 and 18:59 on a day when Mara is present.
- [ ] Approach Mara and confirm the page offers one conversation action rather than three topic choices.
- [ ] Confirm the action reads "Sit and chat with Mara (0:30)".
- [ ] Select it and confirm exactly 30 minutes pass.

## Random topic selection

- [ ] Repeat conversations across multiple visits and confirm the topic is selected automatically.
- [ ] Confirm the pets topic mentions the adorable kittens and animals at Mara's shop.
- [ ] Confirm the life topic has Mara ask about the player's life and listen to the response.
- [ ] Confirm the weather topic is casual conversation about the weather over coffee.
- [ ] Confirm there are no player-facing topic-selection buttons before the conversation.
- [ ] Confirm a fresh random topic is rolled for each new chat, including when choosing Continue chatting.

## Rewards and departure

- [ ] Confirm every completed topic awards exactly +1 Mara Love and +1 Mara Trust.
- [ ] Confirm the Journal cafe conversation counter increases once per completed conversation.
- [ ] Confirm the existing 25% post-chat goodbye chance is unchanged.
- [ ] Confirm Mara leaves automatically when the chat reaches 19:00.
- [ ] Confirm a new 30-minute chat is not offered after 18:30.
- [ ] Confirm manually saying goodbye still prevents another cafe approach for that day.

## Regression

- [ ] Confirm the 40% daily cafe appearance chance remains stable when revisiting locations.
- [ ] Confirm the shop/home absence notices still point to the cafe while Mara is there.
- [ ] Confirm shop/home schedule and housework tea break are unchanged.
- [ ] Save and reload after a cafe chat and confirm the Journal count persists.