# Your first trade

This page takes you through making your first sale and/or trade on Escade. Currently the platform is in beta testing on Solana's devnet, a test network where SOL is free and has no value, so nothing here costs you real money whilst we smooth everything out and market the product.

## 1. Set up a wallet

We suggest using Phantom wallet to connect to Escade. All other wallets should work, but we cannot guarantee there won't be any issues, and Phantom is by far the most tested on the platform so far.

1. Install Phantom from [phantom.com](https://phantom.com), as a browser extension or mobile app.
2. Create a wallet and write down the recovery phrase somewhere offline. Anyone with that phrase controls the wallet, and nobody, including Escade, can recover it for you.
3. Switch Phantom to devnet: **Settings → Developer Settings → Testnet Mode**, then choose **Solana devnet**.

## 2. Get some devnet SOL

Copy your wallet address from Phantom, paste it into the [Solana faucet](https://faucet.solana.com), and request devnet SOL. A couple of SOL covers several test transactions. If the faucet limits you, try again later or sign up for gitbook and make one commit on your account.

## 3. Create your Escade account

1. Click **Signup** 
2. Register an account with your email and a secure password.
3. Go to **Dashboard** and click **Change Details**. Add your details, enter your postcode and pick an InPost locker from the map. You cannot buy or accept a trade without a locker and details, because that is where your cards are delivered.
4. Click **Select Wallet** in the menu bar and connect your Phantom wallet.

The first time you buy, list or trade, Phantom asks you to **sign a message**. This proves the wallet is yours and links it to your account. Signing a message moves no funds and costs nothing. You only do it once per wallet.

## What each Phantom popup means

Every action that touches the escrow opens a Phantom popup. Read it before approving it. There are only two kinds:

- **Sign message** links your wallet to your account. It does not move any SOL.
- **Approve transaction** sends a transaction to Escade's escrow program. Phantom shows the SOL leaving or entering your wallet. Check that the amount matches what Escade showed you before approving.

If an amount looks wrong, reject the popup and let us know in our Discord. Nothing happens until you approve.

## Buying a card

1. Go to **Shop**, find a card and click **Add to cart**.
2. Open your cart and click **Proceed to Checkout**.
3. Approve the transaction in Phantom. It pays the price, the delivery fee and your collateral into the escrow. You get one popup per item in your cart.
4. Wait for the seller to post the card. Its tracking appears on your **Dashboard** under **Shop Confirmed Transactions**.
5. Collect the card from your locker and check it against the listing.
6. Click **Confirm receipt** and approve. This pays the seller and returns your collateral.
7. A second popup closes the escrow account, which returns the account deposit to the seller. Please approve it. It moves none of your own funds.

If the card is not what was described, click **Return card** instead of confirming, or **Dispute**. See [If something goes wrong](disputes.md).

## Selling a card

1. Go to **Shop**, open a set and click **Submit Listing**.
2. Choose the card, its variant, condition and, if graded, the grading details. Escade suggests a price where it has one. You can set any price you like, up to the £50 beta cap.
3. Click **Submit** and approve the transaction. It pays the listing fee and posts your collateral, plus the small account deposit.
4. When someone buys, the sale appears on your **Dashboard** under **Shop Confirmed Transactions**. If you cannot fulfil it, **Cancel order** refunds the buyer in full and returns your collateral, if you have not dispatched.
5. Buy InPost postage to the buyer's locker on InPost's own website or app.
6. Post the card, then click **Input tracking ID**, choose InPost, enter the tracking number and approve the transaction. You must dispatch within the 7-day dispatch window, or you lose half your collateral.
7. Once the buyer confirms, you are paid the price and delivery, and your collateral comes back.

## Trading card for card

1. Go to **Trade**. To create a trade, open a set, click **Submit Trade**, mark the cards you **Offer** and the cards you **Want**, then click **Submit** and approve. You pay the listing fee and post collateral.
2. To accept someone else's trade, open it, click **Add to trade cart**, then **Accept Trades** in your trade cart, and approve. You post collateral.
3. Both of you buy InPost postage to each other's locker, post your cards, and click **Input tracking ID** on the trade in your **Dashboard**.
4. When the other side's cards arrive and check out, click **Confirm receipt**. The second confirmation returns both collaterals.
5. Approve the final popup that closes the escrow account.

Once a trade is accepted, neither of you can cancel it alone. Use **Request cancel**; the other side then sees **Agree to cancel**. If you have already bought postage, tell the other trader before either of you cancels.

## Where to get help

If a step fails, the error message starting with **FESC**, **BESC** or **RESC** tells us where it went wrong. Send it to us in Discord along with the listing or trade number.


