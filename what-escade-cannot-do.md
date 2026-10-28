# What Escade cannot do

Most of this page is a list of things Escade is unable to do. An escrow is only worth using if the party running it is unable to abuse it, and "unable" must mean something stronger than "promises not to".

## Escade cannot move your funds

Not with permission, not in an emergency, not if you ask us to.

Every instruction in both programs that moves money at someone's choice requires a signature from the buyer or the seller. The only others are the settlements and burns that become possible when a time limit runs out. Anyone can send those, but the program decides the outcome from the escrow's own timestamps, and the money can only go to the two of you or be burned. There is no instruction that Escade can sign that moves money anywhere else. The wallet Escade uses to rule on disputes has exactly one privilege — writing a proposed ruling — and that instruction transfers nothing.

We still retain upgrade authority for the program whilst the devnet beta is live. This will be burnt when moving to mainnet. 

## Escade cannot enforce its own rulings

We can say what we think should happen. We cannot make it happen. A published ruling sits on the escrow doing nothing until one of the two parties signs to execute it.

This is sometimes frustrating and it is not an oversight. A system where Escade both decides and executes is a system where Escade holds your money.

## Escade cannot freeze, reverse or claw back

There is no instruction to freeze an escrow, nothing that reverses a completed release, and no mechanism to recover funds after a release has settled. Once the program pays out, that is final for everyone including us.

## Escade cannot verify what is in the envelope

No marketplace can. This is covered in [If something goes wrong](disputes.md), but it belongs on this page too, because it is the most important limit on what the dispute process is worth. Escade sees dispatch and receipt. It does not see the contents, so please take photographs and keep as much evidence as possible in case a dispute arises. 

## Escade does not buy, sell or trade cards

We hold no inventory and take no position in any transaction. Revenue is listing fees, paid to a fee wallet outside the program created account. This is our source of income. 

## Why it is built this way

Partly because it is an academically backed, and efficient way to run an escrow marketplace. Partly for a more specific reason.

Under the new UK cryptoassets regime coming into force in October 2027, safeguarding or administering someone else's cryptoassets is a regulated activity. The legislation turns on **control** — whether the firm can move the assets.

Escade is designed to sit outside that perimeter by construction rather than by argument. The programs cannot move your funds independently, so there is nothing for Escade to safeguard. That interpretation is our own and has not been confirmed by the FCA as of yet; we intend to put it to them rather than rely on it. But it is why you will never see Escade add a feature that lets us release an escrow "to help" — doing so would not just break the trust model, it would change what Escade legally is and put us in scope before we have completed the necessary requirements. 

The full regulatory analysis, with the specific provisions, is in the technical paper rather than here.


