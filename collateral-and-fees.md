# Collateral and fees

## Collateral

Both sides post collateral. In a sale, the seller posts it when listing and the buyer when accepting. In a trade, each side posts it when they create or accept the trade. It is not a fee. You get it back in full when the transaction completes honestly, and in full when a refund completes honestly.

It exists to do four things.

**It makes backing out cost something.** A seller can cancel a sale without losing any collateral until they dispatch, and the buyer gets back everything they paid. What costs something is committing and then not performing: a seller who never dispatches loses half their collateral when the dispatch window runs out, and a trader who never sends their card loses half of theirs, or all of it to the other side if the other side did send. Without this, accepting a deal and then going quiet is free, and the other side ends up carrying the cost.

**It makes a promise worth something.** Research on used-goods auctions found that letting a seller make a specific promise raised the rate at which buyers trusted them and, more importantly, the rate at which sellers followed through. A condition grade on Escade is backed by money, which is a stronger form of the same thing.

**It makes a false dispute cost something.** If you raise a dispute and the ruling goes against you, you can lose collateral you would otherwise have had back. A dispute that is free to raise is a dispute worth raising on the off-chance, and that is a tax on everybody who trades honestly.

**It makes fake reputation expensive.** On eBay, a feedback point once cost about 29 cents to manufacture, because a transaction could be notional — a penny, a joke, a favour between two accounts. On Escade, faking one means two funded wallets, real collateral locked for the duration, fees paid, and either a card actually posted or someone willing to sign a confirmation of receiving nothing.

In a trade, collateral is a percentage of the requested cards' value for the submitter and of the receiving cards' value for the acceptor. For a shop transaction it is a percentage of the listing's value. Whilst in beta, listings are capped at £50, and in a trade the cap applies to each side's cards.

## Fees

**Listing fee.** Paid when the listing is created, by the seller or by whoever creates the trade. It is 5% of the listing's value and goes to Escade's fee wallet. It is a percentage of the listing price, or for a trade of your requested card's value. It never enters the escrow balance, so it is not part of anything a dispute ruling divides, and it is not refunded if the listing is cancelled.

**Delivery fee.** In a sale, the buyer pays the delivery fee at acceptance. It is held in escrow with the price and released to the seller with it, since the seller buys postage outside Escade for now until we get full InPost API access. If the card is returned, the delivery fee goes back to the buyer, because the buyer has then paid for the return leg. In a trade, each side buys their own postage, and nothing is held for it.

**Return delivery fee.** Bought by whoever sends the card back. See [If something goes wrong](disputes.md).

**Account rent.** Solana charges a small refundable deposit to keep the escrow account open. The creator pays it and gets it back when the account is closed at the end of a transaction's lifecycle and moves to completed, resolved, refunded, cancelled or burnt.

**Solana network fees.** These are the blockchain's transaction fees and are paid by whoever signs a transaction.

The listing fee is the only fee Escade takes. There is nothing taken at the point of sale, no fee for raising a dispute, and no fee taken from a ruling.

## What happens to forfeited collateral

It goes to the other side, or it is burned. Escade never receives it.

- **A seller who never dispatches** has half their collateral burned. The buyer is refunded in full, and the seller gets the other half back.
- **A trade where neither side dispatches** has half of each collateral burned, and the rest returned.
- **A trade where only one side dispatches** pays both collaterals to the side that dispatched. The same applies on a trade return where only one side sends their cards back.
- **A dispute ruling** divides the escrow between the two of you, so collateral lost in a dispute goes to the other party.
- **A dispute that ends with no ruling accepted** has the whole escrow burned.

Burned means sent to Solana's incinerator address and destroyed. This is to disincentivise defection from cooperation and ensure that no party benefits from a burn.

This is worth being clear about, because it would be straightforward to route forfeited collateral to us and it would be a bad idea. A platform that profits from failed transactions has a reason to want transactions to fail. Keeping it out of our hands means Escade's revenue is the listing fee and nothing else, whatever happens afterwards.


