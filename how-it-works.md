# How Escade works

There are two flows. A **sale** swaps money for a card. A **trade** swaps a card for a card. A trade is really two sales linked together, so both flows follow the same rules: the buyer pays, the payment is held, the card is posted, and the seller is paid once it has arrived and been checked.

Payments are taken and held by our payment and transaction processing supplier, not passed to the seller straight away. Postage is bought from InPost directly, locker to locker, and you enter the tracking number on Escade. We then read InPost's tracking API; Escade does not create labels or shipments yet.

## Selling a card

**1. You list it.** You set a price, describe the condition and pay the listing fee.

**2. A buyer buys it.** They pay the price plus a delivery fee. The payment is held. You are not paid yet. Until you dispatch, you can still cancel, and the buyer gets back everything they paid.

**3. You post the card within 7 days.** Then enter the tracking number on Escade. If you never dispatch, the buyer is refunded in full once the 7 days pass, and your trust score drops.

**4. The card arrives and the inspection window runs.** The buyer has 3 days after delivery to check the card and report a problem. They can confirm receipt sooner if they are happy.

**5. You are paid.** Once the buyer confirms, or the inspection window closes with no problem raised, you receive the price and the delivery fee.

## Trading a card for a card

A trade is two linked sales. If you swap card X for someone else's card Y, you are buying card Y from them and they are buying card X from you, each at the agreed price.

1. One trader creates the trade and pays the listing fee.
2. The other accepts. Each of you pays the agreed price of the cards you will receive. Both payments are held.
3. Escade decides who ships first. Usually the trader with the lower trust score posts first, within 7 days. The other trader posts once that parcel shows as on its way, also within 7 days. If you both have high trust scores, you can both post straight away.
4. Both cards arrive, and each of you has 3 days to check what you received.
5. Once both inspection windows close with no problem raised, each of you is paid for the cards you sent. The two payments cancel out, and the cards have swapped.

Because each side is a sale in its own right, each side is protected on its own.

- **If the first trader never posts,** the trade is cancelled and both payments are refunded. The other trader never sent anything, so has lost nothing.
- **If the second trader never posts** after receiving a card, the first trader is refunded for the card they did not receive, and is paid in full for the card they sent. The trader who did not post has simply bought a card at the agreed price, and their trust score takes the hit.

Once a trade is accepted, neither of you can cancel it alone. One trader requests the cancel and the other must agree. If both agree before anything has been posted, both payments are refunded in full.

## Who decides what

Most steps are yours: listing, buying, accepting, posting, confirming. The clock handles the rest: if a deadline passes, the outcome is fixed in advance (a refund if a card was never posted, payment to the seller if no problem was raised in time).

Escade only steps in when something is reported as wrong. We then review the evidence from both sides and decide whether the buyer is refunded, in full or in part, or the seller is paid. See [If something goes wrong](disputes.md).

## The time limits

| Step | Time limit |
| --- | --- |
| Listing stays open | 21 days |
| Posting a card after a sale or your turn in a trade | 7 days |
| Checking a card after delivery | 3 days |
| Posting a return | 7 days |
