# Dispute Management

If your counterparty is unresponsive, you suspect a scam attempt, or a misunderstanding arises that you are unable to resolve, you can initiate a dispute.

## How It Works

When you start a dispute, you will be attended to by the administrator of the Mostro node you are using, or by a person designated by that administrator (solver). When a solver takes the dispute, Mostro sends you and your counterparty a message with that solver's public key, so your client knows who to talk to in the dispute chat. Only follow the instructions of the solver Mostro assigned: anyone else who writes to you about the dispute may be an impostor.

## Resolution

There is no standard method for resolving disputes across all Mostro nodes. Each administrator can decide how to manage disputes generated in their node and what evidence to request from users to make the most appropriate decision.

When the administrator decides which user is in the right, they will have Mostro release the sats to the appropriate user. Administrators do not charge any extra fee for resolving disputes.

## Chat Evidence

During a trade, the buyer and the seller communicate through an end-to-end encrypted chat. This chat generates a "shared master key" known only to both parties.

If a dispute arises, either party can choose to voluntarily share this key with the solver. With it, the solver can access a copy of the conversation that cannot be altered or deleted. This allows disputes to be resolved fairly, exposing any attempted deception.
For more details on how this privacy system works, see the [Privacy in Mostro](./privacy.md) section.

## Important Timeframes

The users involved must initiate a dispute well before the [hold invoice](./hold-invoice.md) paid by the seller expires, so that the administrator has enough time to request evidence from both parties and make an appropriate decision.

Time continues to run from when the order was accepted and does not stop when a dispute is opened. The administrator must resolve it before the time expires, so users should not wait too long to initiate one. You can read more about timeframes [here](./times.md).

## Automatic Dispute

Mostro opens a dispute on its own in only one case: the buyer has marked the fiat as sent, the seller has not released the sats, and the [hold invoice](./hold-invoice.md) is about to expire.

Shortly before the hold invoice expires and the sats are returned to the seller, Mostro checks the order. If it is still waiting for the seller to release the sats, Mostro opens a dispute so that an administrator can decide while the sats are still locked. Without that dispute, the hold invoice would expire and the sats would return to the seller, even if the buyer had already sent the fiat.

What you should know about this automatic dispute:

- It is registered in the buyer's name, because it is the buyer's payment that is at stake. The buyer will see it as their own dispute, and the seller will see it as a dispute opened by their counterparty.
- It works like any other dispute: an administrator or solver takes it and attends to both parties.
- The administrator has very little time to resolve it before the hold invoice expires: 12 blocks with the default settings. In theory that is 120 minutes, since a block is mined every 10 minutes on average, but blocks do not arrive at fixed intervals, so that time can be longer or shorter. If that time runs out, the sats return to the seller and Mostro can no longer intervene. Do not wait for the automatic dispute: if your counterparty stops responding, open the dispute yourself as soon as possible.
- If the buyer never marked the fiat as sent, Mostro does not open a dispute. It cancels the order before the hold invoice expires, and the sats return to the seller.

## Anti-Abuse Bond in Disputes

If you trade on a node that requires an [anti-abuse bond](./anti-abuse-bond.md), the administrator may claim the bond of whoever acted in bad faith when resolving the dispute. Part of that bond is given to the honest counterparty as compensation. See [Anti-Abuse Bond](./anti-abuse-bond.md) to learn how it works.
