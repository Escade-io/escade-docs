# Escade

Escade is a peer-to-peer (P2P) marketplace for the buying, selling, and trading of physical collectibles. To ensure delivery of products throughout a transaction, both parties submit collateral in USDC which is then held by a program on the Solana blockchain until successful fulfilment of the transaction and delivery.

So, you list an item for sale or trade, then send collateral to the Solana program and sign for the transaction. Someone then purchases the item, or accepts the trade, sending over their collateral to the program in the process, and in the case of a purchase the requested sales price. The USDC sits in a program created account that neither party nor Escade can move independently. For now, the card gets posted off the platform via InPost by purchasing delivery to the other party’s locker details until we get API access from InPost. When the buyer confirms it arrived as described, or the delivery window runs out with no dispute raised, the program releases the payment. If something goes wrong and a transaction leads to a dispute, there is a defined way out as described in [Disputes](disputes.md).

## Why Escade was created

Ever since I was a kid, I have collected Pokémon cards, and one problem I've always had was that nobody I knew around me also collected. So, I never had anyone to trade the cards I didn't like or want with, and as I grew up nobody ever solved my problem. Methods emerged over time such as Facebook Marketplace, Reddit, Swap, Cozmor, etc, but none ever really satisfied me and assured me I had a consistent and reliable way to trade these cards. Therefore, I decided to take matters into my own hands last year and solve the problem for myself, and this is how Escade was born. 

At first it was a toy project, a chance for me to learn more about backend infastrucutre and get some hands on experience with rust in an attempt to improve my CV and get more technical jobs in the banking industry. As time evolved, I started to see the validity of the actual business behind what I was doing and believing in the vision and future of it. The toy project morphed into something more... a desire to build the largest peer-to-peer marketplace in the world - a secure and trusted place to trade all your collectibles!

## What makes it different

**Trading products peer-to-peer is what Escade was created for** 

Businesses like eBay and Vinted are constrained here. Their whole business model revolves around the holding of payment for goods and services until the buyer agrees that fulfilment is satisfactory. However, this model cannot accommodate transactions that effectively have two buyers who do not exchange currency. This is where Escade steps in: our whole business model is designed around the trading of goods amongst parties where no purchase value is exchanged.

**Collateral protects against defection from cooperation**

In a card for card trade where there is effectively two buyers there are two ways to manage cooperation and mediation. The first of which is to have an indepdent adjudicator who takes custody of the cards from both parties prior to the swap and have them conduct a quality and fraud analysis to determine if it meets specifications for the transaction. However, this introduces multi leg shipping which increase shipping costs by double at least for the customers. It also has high start up capital requirements since its manual, and requires a physical premise for receiving deliveries and conducting analysis. The second of which is to have an independent adjudicator hold collateral from both parties until the transaction is completed. This also has disadvantages in that it locks up customers capital and makes a trade temporarily a rather costly method of transacting. It also leads to customers maybe taking on a risk they loose collateral despite transacting honestly. Especially considering collateral needs to be set high enough that defection leads to a negative return, at least initially until we build a user profile.

Given we are a start-up with limited funds we have opted to use the second choice as it keeps operational costs low for now providing headroom to grow, and through combining collateral and a trust scoring algorithm borrowing features from marketplaces you might already be familiar with, we are confident we can reduce negative customer experiences and fraud to normal non-crypto business operating levels. 

Upon initialisation of a trade listing, the submitting party sends a percentage of the requested cards' value set by Delphi in collateral to a program created account where it is stored until the listing is either cancelled or the trade is accepted and completed. Cancellation can only occur prior to acceptance, or afterwards via a request to the other party. If cancelled, the collateral is refunded in full, the listing fee is not. Upon acceptance, the accepting party then sends a percentage of the receiving cards' value set by Delphi in collateral to the same account. Both parties now have an incentive to not defect from the trade as they want their collateral staked back. 

A shop transaction works with the submitting party sending a percentage of the listed card's value set by Delphi in collateral to a program created account. Again, it is stored until the listing is either cancelled or the listing is bought and delivery completed. There is no two-sided delivery; a delivery fee is taken from the buyer and held within the escrow account too. This then goes to the seller upon completion as they essentially front the delivery fee via InPost delivery purchase externally. 

**Collateral requirements change based upon user history**

Our proprietary trust scoring engine, Delphi, analyses and scores users based upon past activity - both on the blockchain and on the platform. Fresh accounts or low scoring users will post enough to ensure that defection leads to a loss. The more successful completions, the lower the collateral requirements should go. 

**Escade never takes direct custody of your funds** 

The account where collateral is temporarily held is created by a Solana program. Money leaves it only when you or the person you are trading with signs, or when a time limit written into the program runs out, and then only to one of you or to be burned. There is no method by which Escade can release, redirect, or freeze what is in there.

**Escade can rule on a dispute but cannot enforce the ruling** 

If a trade goes wrong and the two of you cannot agree, we review the evidence and publish a proposed split. That ruling is written to the escrow and moves nothing. One of you then must sign to execute it. Two separate signatures, neither sufficient alone.

**Delivery is tracked and recorded** 

All tracking IDs are verified against InPost's API. The public tracking API is available in the UK; it is only the label creation and returns API we are awaiting access to. This means that in the event of a dispute we can indeed verify if something was posted, and where it was posted to, etc. 

**There is a £50 limit to transactions**

Initially there will be a hard cap on listings over £50 and for wallets that hold over a certain value in them. 

## Start here

- [Your first trade](first-trade.md) — wallet setup to a finished trade, step by step
- [The problem Escade solves](the-problem.md) — what goes wrong in card trades, and what doesn't
- [How Escade works](how-it-works.md) — step by step, both flows
- [Disputes](disputes.md) — refunds, returns, and disputes
- [What Escade cannot do](what-escade-cannot-do.md) — the limits, deliberately
- [Collateral and fees](collateral-and-fees.md) — what you pay and what you get back
- [Known limitations](limitations.md) — what is unfinished, in our own words
- [References](references.md) — List of sources
- [Appendix](appendix.md) — Data to aid in discussion



