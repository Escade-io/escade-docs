# Escade

Escade is a peer-to-peer (P2P) marketplace for the buying, selling and trading of physical collectibles. Every payment is held by our payment and transaction processing supplier until the card has been delivered and checked, so nobody is paid for a card that never arrives.

You list an item for sale or trade. Someone buys it, or accepts the trade, and pays. That payment is held, not passed on. You post the card using a tracked InPost delivery to the other party's locker. Once it has arrived and the inspection window has closed with no problem raised, the seller is paid. If something goes wrong, there is a defined way out, described in [If something goes wrong](disputes.md).

> **Escade is moving from blockchain to card payments.** Trading is paused while we make the switch. These pages describe how Escade works from now on.

## Why Escade was created

Ever since I was a kid, I have collected Pokémon cards, and one problem I've always had was that nobody I knew around me also collected. So, I never had anyone to trade the cards I didn't like or want with, and as I grew up nobody ever solved my problem. Methods emerged over time such as Facebook Marketplace, Reddit, Swap, Cozmor, etc, but none ever really satisfied me and assured me I had a consistent and reliable way to trade these cards. Therefore, I decided to take matters into my own hands last year and solve the problem for myself, and this is how Escade was born. 

At first it was a toy project, a chance for me to learn more about backend infastrucutre and get some hands on experience with rust in an attempt to improve my CV and get more technical jobs in the banking industry. As time evolved, I started to see the validity of the actual business behind what I was doing and believing in the vision and future of it. The toy project morphed into something more... a desire to build the largest peer-to-peer marketplace in the world - a secure and trusted place to trade all your collectibles!

## What makes it different

**Trading products peer-to-peer is what Escade was created for**

Businesses like eBay and Vinted are constrained here. Their whole business model revolves around the holding of payment for goods and services until the buyer agrees that fulfilment is satisfactory. However, this model cannot accommodate transactions that effectively have two buyers who do not exchange currency. This is where Escade steps in: we turn a card-for-card swap into two linked sales, so both traders get the same protection a buyer gets on any good marketplace.

**Holding payment protects against defection from cooperation**

In a card for card trade where there is effectively two buyers there are two ways to manage cooperation and mediation. The first of which is to have an independent adjudicator who takes custody of the cards from both parties prior to the swap and have them conduct a quality and fraud analysis to determine if it meets specifications for the transaction. However, this introduces multi leg shipping which at least doubles shipping costs for the customers. It also has high start up capital requirements since its manual, and requires a physical premise for receiving deliveries and conducting analysis. The second of which is to have an independent adjudicator hold payment from both parties until the transaction is completed. This also has disadvantages in that it ties up customers' money for the length of the trade.

Given we are a start-up with limited funds we have opted to use the second choice as it keeps operational costs low for now providing headroom to grow, and through combining held payments and a trust scoring algorithm borrowing features from marketplaces you might already be familiar with, we are confident we can reduce negative customer experiences and fraud to normal marketplace levels.

**A swap is two linked sales**

When you swap your card for someone else's, you are selling your card to them and buying theirs from them, each at the agreed price. Both of you pay when the trade is accepted, and both payments are held. When both cards have arrived and checked out, each of you is paid for the card you sent, so the money cancels out and the cards have swapped. If one side never sends their card, the side that did is still paid for theirs. Nobody can walk off with a card without paying for it.

**Trust decides who ships first**

Our proprietary trust scoring engine, Delphi, scores users based on their activity on Escade. In a swap, the trader with the lower score ships first, and the other ships once that parcel is on its way. That way an honest trader is never left having posted a card to someone who never posts theirs. Traders who both have high scores can ship at the same time.

**Everyone who gets paid is identity-checked**

To receive money on Escade you verify your identity with our payment processing supplier. A banned trader cannot simply start again with a new email address.

**Delivery is tracked and recorded**

All tracking IDs are verified against InPost's API. The public tracking API is available in the UK; it is only the label creation and returns API we are awaiting access to. This means that in the event of a dispute we can verify if something was posted, and where it was posted to.

**There is a £50 limit to transactions**

Initially there is a cap of £50 per listing, and lower limits for new accounts.

## Start here

- [Your first trade](first-trade.md) — account setup to a finished trade, step by step
- [The problem Escade solves](the-problem.md) — what goes wrong in card trades, and what doesn't
- [How Escade works](how-it-works.md) — step by step, both flows
- [If something goes wrong](disputes.md) — refunds, returns and disputes
- [What Escade cannot do](what-escade-cannot-do.md) — the limits
- [Payments and fees](collateral-and-fees.md) — what you pay and when you get paid
- [Known limitations](limitations.md) — what is unfinished, in our own words
- [References](references.md) — list of sources
- [Appendix](appendix.md) — data to aid in discussion
