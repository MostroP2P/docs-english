# Is a Mostro Node Working?

Before you trade, or when something takes longer than usual, you can check the state of the main Mostro nodes on the public status page:

**[status.mostro.network](https://status.mostro.network)**

Every minute, each node publishes a signed health report on Nostr. The page reads those reports straight from the relays, checks them in your browser, and compares the Lightning node of each monitored node with public block explorers.

| Colour | Meaning |
|---|---|
| 🟢 Operational | The node reports itself healthy and passes the independent checks. |
| 🟡 Degraded | Something is not fully right, or the node is in maintenance. |
| 🔴 Down | The node reports a serious problem, its Lightning node is behind the chain, or it stopped reporting. |
| ⚪ Not monitored | The node is listed but not yet checked. |

Under each node you can see the last 90 days. Green means the node is working as far as it can tell; it does not guarantee that every trade succeeds.

## Maintenance

A node in maintenance does not accept new orders or takes, but trades that are already open can still be completed, cancelled or disputed. Operators turn it on for planned work. Nodes also turn it on by themselves when their Lightning node falls out of sync, and turn it off again when it recovers.

## If your sats are late

If the node's own Lightning node has a problem, Mostro does not give up on your payment: it waits and pays automatically once the problem is solved, and that delay does not count as a failed payment on your side. If your payment fails for another reason, for example a route problem, Mostro retries a few times and then asks you for a new invoice: keep the app open and send one, or the payment cannot complete. If the node stays red for a long time, contact its operator (see [Support and Contact](./support-and-contacts.md)).

## Comparing nodes in the app

In the [Mostro App](./mostro-mobile.md), *Settings → Network → Mostro Node* shows each node's status, fee and deposit, and *About → Connected node* shows the limits, currencies and times of the node you use.
