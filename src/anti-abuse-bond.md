# Anti-Abuse Bond

The anti-abuse bond is an optional mechanism that some Mostro nodes use to make exchanges safer. The idea is simple: when entering a trade you put up a small amount of sats as collateral, which you get back in full if you act in good faith, but which you lose if you try to scam your counterparty or fail to do your part. This way, a scammer puts their own money at risk, which discourages abuse and increases the security of exchanges on Mostro.

## A node with or without a bond

Not all Mostro nodes require an anti-abuse bond. It is a feature that each administrator decides whether to enable on their node, so it is up to you to choose whether you prefer to trade on a Mostro that requires it or one that does not.

Each node that enables it sets its own rules: who it asks for the bond (whoever creates the order, whoever takes it, or both) and how much it is. The amount is usually a small percentage of the order value (for example, 1%) with a minimum in sats, but that percentage is decided by each node.

> **Tip:** You can check whether the node you are using requires an anti-abuse bond —and how much it would be— from your own Mostro client. For example, in [Mostro Mobile](./mostro-mobile.md) you can go to the *About* section and review those node details before trading.

## How is it different from the escrow?

The bond is completely independent from the [trade escrow](./hold-invoice.md). It is a second hold invoice: your sats are only "locked" in your wallet, they are not spent. If everything goes well, they are "unlocked" and returned to you without ever having left your wallet. It is not mixed with or deducted from the exchange amount.

## When do I get my bond back?

You get 100% of your bond back as long as you do your part: when you complete the trade successfully or, simply, when you do not cheat or break what was agreed. For example:

- You complete the exchange correctly.
- You cancel the order cooperatively.
- A dispute arises and the administrator does not determine that you acted in bad faith.

Under normal conditions the bond is not a cost: it returns to your wallet in full, just like the sats locked in a hold invoice.

## When can I lose it?

> **Important:** You only lose your bond if you abuse the system. This can happen in two situations:
>
> 1. **By decision in a dispute.** An administrator (solver), after reviewing the evidence, determines that you acted in bad faith and instructs Mostro to claim your bond.
> 2. **By failing to do your part and letting the time run out.** If you take or create an order and then do not respond or continue with the exchange (you don't pay, don't send the fiat, don't provide your invoice in time), you let the deadline that was your responsibility expire. This only applies if the node enabled that policy.

## Where do the sats from a claimed bond go?

When a bond is claimed, the sats are split between the node —which thereby funds the work of resolving [disputes](./disputes.md) and keeping the service running— and your honest counterparty, as compensation for the harm. The proportion of that split is defined by each node and is public, so you can know it before trading.

## Examples

> **Example — A buyer trying to scam.** Alice sells sats and Bob buys them on a node that requires an anti-abuse bond. Bob never sends the agreed fiat money, but still insists that Alice release the sats to him.
>
> Alice opens a [dispute](./disputes.md) and presents the administrator with evidence that she never received the payment. The administrator confirms that Alice is in the right, cancels the order —the escrow sats return to Alice— and claims Bob's bond, since he was trying to scam her. As compensation, Alice receives half of the sats from Bob's bond; the other half goes to the node. Bob loses his bond for having tried to abuse the system.

> **Example — A spammer cluttering the order book.** Imagine a malicious user who wants to fill the order book with offers they never intend to complete. On a node that requires an anti-abuse bond, to create each order they must lock a bond. If someone takes one of their orders and they do not respond or continue with the exchange, they let the deadline expire and lose the bond for that order. This way, filling the book with fake offers becomes expensive and stops being worthwhile.

## If you are owed your counterparty's bond

If your counterparty loses their bond and you are owed a share, your client will ask you for an invoice to send you those sats. You have a window defined by the node (for example, 15 days) to claim it; if you let it pass, you lose the right to collect that share. That is why it is best to attend to your client's request when it appears.
