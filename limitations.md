# Known limitations

Written in our own words, because you will find most of these out anyway and it is better that you find them here.

**Escade cannot verify an item's condition or what was received.** The dispute process is strong on whether you posted a card and when, and weak on what state it was in. Therefore, if your complaint rests entirely on condition, in shop buy and sell transactions the buyer can always send the card back for a refund instead, and the seller cannot refuse the return. If two parties disagree on what was posted and received, then understand that we are mediating based on descriptions, evidence, and history, not on the card.

**The dispute process depends on a single mediator.** That is Escade. The academic literature on escrow is clear that a single internal arbiter is the weakest link in any design like this, and the honest answer is that it is a trade-off: the alternative is a panel, which is slow and expensive, or an on-chain vote, which is gameable. What we have done instead is make sure that the mediator cannot move funds independently.

**No trade or purchase on Escade is private.** Solana is a public ledger. Transaction amounts, wallet addresses, timestamps and escrow states are visible to anyone who looks, now and permanently. Pseudonymous is not anonymous, and a wallet that trades regularly accumulates a history that can be analysed.

**A bad reputation can be abandoned.** Reputation on Escade is tied to wallets and emails. These can both be replaced to some degree with not too much difficulty. To mitigate this, Delphi makes reputation farming expensive, as it costs listing fees and transaction fees to reduce collateral, and on-chain activity analysis can link accounts together. Reputation farming is still an issue alongside abandonment. Collateral and fees make building a fake reputation expensive and less profitable, but they do not stop somebody walking away from an account and wallet to start again. No marketplace has solved this to date. 

**Burned collateral is genuinely gone.** If a dispute ends without either party accepting a ruling, everything in the escrow is burned. We cannot recover it, reverse it, or make you whole. This is the mechanism working as designed. Because of changing regulation in the UK, we cannot assume full control of the program created accounts which means we cannot fully mediate in the way we would like. All mediation requires 2 of 3 signatures to release any funds: Escade's ruling, then one party executing it. In the event Escade and the two parties cannot agree, collateral may be burnt. If we cannot assume control, our only option left is deterrence of defection.

**The parameters are estimates.** Collateral percentages, the listing fee (5%), time windows (7 to 21 days) — these are our current best guesses, not figures derived from how the market behaves. We do not have enough transaction history yet to set them from evidence, and we intend to revise them once we do. If they are set wrong, the symptom will be sellers refusing to list or disputes resolving badly.

**The regulatory position is ours, not the FCA's.** We believe Escade sits outside the UK cryptoasset safeguarding regime because the programs cannot move your funds. We have not had that confirmed, and we are seeking confirmation ahead of the regime coming into force in October 2027. Our recent attempts to reach out to the FCA to confirm this have not yielded much clarity. 

**Escade is not an insurer.** There is no guarantee, no protection fund, and no promise to make you whole. We may choose to compensate someone in a case that was clearly fraud, as a one-off decision, and you should not plan around it. A promise to compensate would be an insurance product, which is a regulated thing we are not.

---

If any of this is a dealbreaker, that is a reasonable conclusion to reach, and we would rather you reached it now. A fully technical analysis of the limitations is available within the upcoming Escade whitepaper. 


