# Escade

Escade is a peer-to-peer (P2P) marketplace for buying, selling, and trading physical collectibles, where the money is held by a program on the Solana blockchain until both parties to the transaction are satisfied with its fulfilment and outcome.

You list a product for sale or trade, then send collateral to a Solana program. Someone purchases the item, or accepts the trade, then they send their collateral, and in the case of a purchase the requested sales price to the program. The SOL sits in a program created account that neither party nor Escade can move independently. For now, the card gets posted off the platform via InPost by purchasing delivery to the other party’s locker details until we get API access from InPost. When the buyer confirms it arrived as described, or the delivery window runs out with no dispute raised, the program releases the payment. If something goes wrong and a transaction leads to a dispute, there is a defined way out as described in [Disputes](disputes.md).

## Why Escade was created

Ever since I was a kid, I have collected Pokémon cards. However, one problem I always had was that nobody I knew around me also collected cards and I never had anyone to trade cards I didn't want with. As I grew up nobody ever solved my problem, methods emerged over time such as Facebook Marketplace, Reddit, Swap, Cozmor, etc, but none ever really satisfied me and assured me I had a reliable way to trade these cards. So, I decided to take matters into my own hands last year and solve the problem for myself. This is when Escade was born. 

The secondary collectibles market has always relied on trust, and for the most part consumers are honest and trustworthy, with most participants completing transactions successfully with no issue. The problem with secondary market transactions is not that people are dishonest, it is what happens when two people disagree upon whether the conditions of a contract were fulfilled. This can happen for various reasons such as disagreement on item quality, non-receipt of a product, non-receipt of payment, or fake and fraudulent items. Traditional e-commerce venues resolve disagreements like this by acting as a mediator, adjudicating the process by collecting evidence and distributing a verdict, ultimately determining who gets what funds.

## What makes it different

**Trading products peer-to-peer is what Escade was created for** 

Businesses like eBay and Vinted are constrained here. Their whole business model revolves around the holding of payment for goods and services until the buyer agrees the fulfilment is satisfactory. However, this model cannot accommodate transactions that effectively have two buyers who do not exchange currency. This is where Escade steps in: our whole business model is designed around the trading of goods amongst parties where no purchase value is exchanged.

**Collateral protects against defection from cooperation**

Upon initialisation of a trade listing, the submitting party sends a percentage of the requested cards' value set by Delphi in collateral to a program created account where it is stored until the listing is either cancelled or the trade is accepted and completed. Cancellation can only occur prior to acceptance, or afterwards via a request to the other party. If cancelled, the collateral is refunded in full, the listing fee is not. Upon acceptance, the accepting party then sends a percentage of the receiving cards' value set by Delphi in collateral to the same account. Both parties now have an incentive to not defect from the trade as they want their collateral staked back. 

A shop transaction works with the submitting party sending a percentage of the listed card's value set by Delphi in collateral to a program created account. Again, it is stored until the listing is either cancelled or the listing is bought and delivery completed. There is no two-sided delivery; a delivery fee is taken from the buyer and held within the escrow account too. This then goes to the seller upon completion as they essentially front the delivery fee via InPost delivery purchase externally. 

**Collateral requirements change based upon user history**

Our proprietary trust scoring engine, Delphi, analyses and scores users based upon past activity. Fresh accounts or low scoring users will post enough to ensure that defection leads to a loss. The more successful completions, the lower the collateral requirements should go. 

**Escade never takes direct custody of your funds** 

The account where collateral is temporarily held is created by a Solana program. Money leaves it only when you or the person you are trading with signs, or when a time limit written into the program runs out, and then only to one of you or to be burned. There is no path by which Escade can release, redirect, or freeze what is in there.

**Escade can rule on a dispute but cannot enforce the ruling** 

If a trade goes wrong and the two of you cannot agree, we review the evidence and publish a proposed split. That ruling is written to the escrow and moves nothing. One of you then must sign to execute it. Two separate signatures, neither sufficient alone.

**Backing out costs something** 

Both sides post collateral, which you get back when the trade completes honestly. Committing to a deal and never posting your card, or losing a dispute, costs you something. This is what makes a promise on Escade worth more than a promise in a Facebook group.

**Delivery is tracked and recorded** 

All tracking IDs are verified against InPost's API. The public tracking API is available in the UK; it is only the label creation and returns API we are awaiting access to. This means that in the event of a dispute we can indeed verify if something was posted, and where it was posted to, etc. 

## Start here

- [Your first trade](first-trade.md) — wallet setup to a finished trade, step by step
- [The problem Escade solves](the-problem.md) — what goes wrong in card trades, and what doesn't
- [How a sale works](how-it-works.md) — step by step, both flows
- [Disputes](disputes.md) — refunds, returns, and disputes
- [What Escade cannot do](what-escade-cannot-do.md) — the limits, deliberately
- [Collateral and fees](collateral-and-fees.md) — what you pay and what you get back
- [Known limitations](limitations.md) — what is unfinished, in our own words
- [References](references.md) — List of sources
- [Appendix](appendix.md) — Data to aid in discussion



