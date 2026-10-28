# If something goes wrong

Most disputes are disagreements on condition, where the card should be returned. Escade handles that case first and separately, because it is an extremely common one.

## Sending it back: returns

**In a sale,** if the card arrives and it is not what was described, the buyer can start a return rather than confirming receipt. The seller does not have to accept a return; the return is automatically enforced. From there:

1. **Buyer starts the return.** The escrow moves to a returning state, and a fresh delivery window begins. Nothing moves yet.
2. **Buyer posts the card back.** Once the delivery code has been input, the escrow's state is marked as returned.
3. **Seller confirms the return** when the card has arrived. This refunds the price and delivery to the buyer and returns the collateral to both.

If the seller goes quiet once the card has been posted back, the return is treated as received when the window runs out and the buyer is refunded. If the buyer starts a return and never posts the card, the sale completes in the seller's favour when the window runs out.

A seller who thinks the card that came back is not the one they sent, or not in the condition it left in, can dispute the return. The buyer's collateral is what a bad-faith return puts at risk.

On a return each side has paid for one leg of postage: the seller sent the card; the buyer sends it back. That is why the delivery fee is refunded back to the buyer.

**In a trade,** a return needs both sides. One party requests it and the other must accept. Then each side sends back the cards it received and confirms the cards it sent have come back, and both collaterals are refunded. If only one side sends their cards back before the window runs out, that side receives both collaterals. A request nobody accepts changes nothing, and the trade completes at the end of the delivery window as normal.

No third party is involved at any point. This is the route we expect most disputes to take, and it is the only route where everybody walks away whole.

## When you cannot agree: Disputes

A dispute freezes the escrow and Escade knows to get involved because we are notified when a transaction enters a disputed state. In a sale, the buyer can dispute once the card has been dispatched and before they confirm receipt, and the seller can raise one during a return on the leg they confirm. In a trade, either side can raise a dispute once the other's card has been dispatched and before they have confirmed it, and the other side can raise one during the return leg.

**Escade proposes a ruling and signs for it.** We review what both sides have submitted and write a proposed split to the escrow, as a percentage to each party. The ruling is published and recorded with a timestamp. This is the first of the two signatures (out of three) required. **It moves nothing.**

**One of the parties signs for it.** Either party can then sign to carry out the ruling, and the figure they sign must match the published ruling exactly. A ruling that was revised after you reviewed it cannot be executed in its place. This is the second of the two signatures (out of three) required.

This is two signatures doing two different jobs. Escade's signature says what should happen. One party's signature makes it happen. Neither one alone can move a lamport out of the escrow. That separation is not a convenience — it is the thing that keeps Escade from being a custodian of your money, and it is described further in [What Escade cannot do](what-escade-cannot-do.md).

**There is no decline button.** If you think a ruling is wrong, and both parties fail to sign for Escade's ruling, the collaterals will face a burn. We need to disincentivise defection from cooperation and one effective way to mitigate harmful actors is to ensure their expected value from defection is lower than cooperation until Delphi knows they can be trusted and collateral requirements can be lowered. 

## If nobody accepts the ruling

A dispute cannot stay open forever. A ruling must be proposed and accepted within 21 days of the dispute being raised. Once that window closes, anyone can trigger a burn: everything in the escrow is sent to Solana's incinerator address, where it is permanently destroyed. The only exception is the small deposit Solana charges to keep the account open, which goes back to the creator when the account is closed.

Nobody wins. The buyer does not get the money, the seller does not get the money, and Escade does not get the money. This is intentional and it is the backstop that makes the rest of the process work. If refusing a ruling were free, the party who stood to lose would always refuse. Because refusal eventually destroys the collateral, both sides have a reason to accept a ruling that is roughly fair rather than hold out for one that is perfect.

It is a bad outcome by design. It exists so that it rarely must be used.

## What we can rule on

Being straight about this matters more than sounding capable.

**Strong evidence:** who created the escrow, who accepted it, who dispatched and when, who confirmed, what tracking said, what the listing claimed. All of this is timestamped.

**Weak evidence:** what condition the card was in when it was sealed into the envelope. We were not there. Neither was the ledger. A tracking number proves a parcel was delivered, not what was in it.

So Escade rules confidently on performance — did you post it, did you post it on time, did you confirm, did damage occur during shipping, etc. It rules much less confidently on condition, and the dispute procedure puts the burden of proof on whoever raised the dispute: if the evidence does not settle the question, the ruling goes against the party who brought it. That rule exists so that a complaint nobody can verify is not a free option.


