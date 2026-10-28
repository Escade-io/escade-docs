# How a sale works

There are two flows. A **sale** swaps cash for a card. A **trade** swaps a card for a card. They work the same way, except that in a trade both sides post an item and both sides confirm receipt.

Postage is bought from InPost directly, locker to locker, and you enter the tracking number on Escade. We then read InPost's tracking API; Escade does not create labels or shipments.

## Selling a card

**1. You list it.** You set a price, describe the condition, and post collateral. The listing fee is taken at this point. Your collateral goes into the escrow account the program creates for this listing.

**2. A buyer accepts.** They pay the listing price plus delivery into the same escrow account, and post collateral of their own. The money is now locked. They cannot reach it, and Escade cannot reach it. Until you dispatch, you can still cancel: the buyer gets back everything they paid and you keep your collateral.

**3. You post the card.** Then enter the tracking number on the Escade webapp. If you never dispatch, once the dispatch window passes the buyer is refunded in full and half your collateral is burned.

**4. The buyer confirms it arrived as described.** This releases the price and delivery to you and returns both lots of collateral. The sale is complete.

If the buyer goes quiet instead, the sale does not hang forever. Once the delivery window passes with no confirmation, no return and no dispute, the escrow settles as delivered: you are paid, and both lots of collateral go back. Anyone can send that settlement, but nobody chooses its outcome. The program works it out from the timestamps on the escrow.

## Trading card for card

Both sides post collateral, sized to the value of the requested cards for the submitter and the received cards for the acceptor, and the money in escrow is only collateral since there is no cash leg. Then:

1. One trader creates the trade, pays the listing fee and posts collateral.
2. The other accepts and posts collateral.
3. Both dispatch their cards.
4. Both confirm receipt.
5. Collateral returns to both.

Once accepted, a trade cannot be cancelled by one side alone. One trader requests the cancel and the other must agree, because either of you may already have bought postage and posted a card before entering the tracking number. If both agree, both collaterals come back in full.

If the dispatch window passes and only one of you has dispatched, the side that dispatched receives both collaterals. If neither of you has, half of each collateral is burned and the rest is returned. If both cards are on their way and one side never confirms, the trade settles as delivered at the end of the delivery window.

Because both sides have something at stake and both must confirm, a card-for-card trade is the case escrow suits best — and the case no existing marketplace handles, because there is no payment to hold.

## What the program will and will not do

The escrow is an account on Solana with a status that moves through defined states: active, accepted, dispatched, completed, and the refund and dispute states described in the next page.

The program reads exactly four things when deciding whether to act: **signatures**, **amounts**, **ruling** and **the clock**. That is the entire input set. It has no admin instruction, no owner privilege, and no key held by Escade that can move funds. Every step that is somebody's choice — accepting, dispatching, confirming, cancelling, returning, executing a ruling — needs a signature from the buyer or the seller. The only thing Escade can sign is a proposed ruling on a dispute, and that moves nothing.

The clock is used only for windows: how long a listing stays open (21 days), how long you must dispatch after acceptance (7 days), how long a delivery or a return has (21 days), how long a dispute stays open (21 days). When a window runs out, anyone can send the settlement, but the outcome is fixed in the program, and the money can only go to the two of you or be burned. A window expiring never pays a third party.

## What you can see

Every step writes to the Solana ledger, which is public. The escrow account carries the timestamps for each stage — created, accepted, dispatched, confirmed, disputed, ruled, completed.

When a transaction finishes, the escrow account is closed and the small deposit Solana charges to keep it open goes back to the person who created it.

Escade keeps its own event log as well, but that log is a mirror. Where the two disagree, the chain is correct.


