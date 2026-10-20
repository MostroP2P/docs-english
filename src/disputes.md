# Dispute Management

If your counterparty is unresponsive, you suspect a scam attempt, or a misunderstanding arises that you are unable to resolve, you can initiate a dispute.

## How It Works

When you start a dispute, you will be attended to by the administrator of the Mostro node you are using, or by a person designated by that administrator (solver). Upon opening the dispute, Mostro will provide you with a unique token number, and your counterparty will receive a different one. Both tokens will be revealed to the administrator handling the dispute. When the administrator contacts you and your counterparty, they will tell you your token, allowing you to verify that they are the designated person and ensuring they are not an impostor.

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

A few hours before the hold invoice expires (24 blocks, about 4 hours, with the default settings), Mostro checks the order. If it is still waiting for the seller to release the sats, Mostro opens a dispute so that an administrator can decide while the sats are still locked. Otherwise the hold invoice would expire and the sats would return to the seller, even if the buyer had already sent the fiat.

What you should know about this automatic dispute:

- It is registered in the buyer's name, because it is the buyer's payment that is at stake. The buyer will see it as their own dispute, and the seller will see it as a dispute opened by their counterparty.
- It works like any other dispute: both parties receive their token and are attended to by an administrator or solver.
- The administrator has very little time to resolve it, about two hours, before the hold invoice expires. If that time runs out, the sats return to the seller and Mostro can no longer intervene. Do not wait for the automatic dispute: if your counterparty stops responding, open the dispute yourself as soon as possible.
- If the buyer never marked the fiat as sent, Mostro does not open a dispute. It cancels the order before the hold invoice expires, and the sats return to the seller.

## Anti-Abuse Bond in Disputes

If you trade on a node that requires an [anti-abuse bond](./anti-abuse-bond.md), the administrator may claim the bond of whoever acted in bad faith when resolving the dispute. Part of that bond is given to the honest counterparty as compensation. See [Anti-Abuse Bond](./anti-abuse-bond.md) to learn how it works.
