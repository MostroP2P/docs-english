# Exchange Times

Mostro is designed for bitcoin-to-fiat exchanges to be fast, so it is recommended to use instant fiat payment methods.

Each Mostro node operator can set their own time frames for each step of the exchange, fostering competition among Mostro nodes and allowing users to select the one that best fits their needs. In the [Mostro App](./mostro-mobile.md) you can see the times of the node you use under *About → Connected node* (*Expiration*) and *About → Node technical data*. The trade screen also shows a countdown for each step.

The figures below are typical values; check your node for the exact ones.

When an offer is posted, it usually remains in the order book for *24 hours* (some nodes keep orders up to 72 hours). If no one takes it within that time, it will be automatically deleted.

Once someone takes an offer, they usually have *15 minutes* to either pay the [hold invoice](./hold-invoice.md) if they are the seller or provide an invoice if they are the buyer. If they do not complete their part within that time frame, the order will be automatically reposted. However, if they do, then the counterparty will have the same time to complete their corresponding action (either paying the hold invoice or providing an invoice, depending on their role in the exchange); if they fail to do so, the order will be canceled and not reposted.

After the seller pays the hold invoice and the buyer provides their invoice, they have until shortly before the expiration of the [hold invoice](./hold-invoice.md) to finalize the exchange. That time is measured in Bitcoin blocks, which arrive about every 10 minutes on average. On most nodes the hold invoice lasts 144 blocks (about 1 day) and Mostro steps in about 20 hours after the seller paid; on nodes with longer hold invoices, such as the default node of the app (about 2 days), Mostro steps in after about 46 hours. During this time, the buyer must send the fiat payment, and the seller must release the sats upon confirming receipt of the fiat. For this reason, it is recommended to only use instant fiat payment methods.

If the exchange has not been completed when Mostro steps in:

- If the buyer has not marked the fiat as sent, Mostro cancels the order and the sats are returned to the seller's wallet.
- If the buyer has marked the fiat as sent, Mostro [opens a dispute automatically](./disputes.md#automatic-dispute), so that an administrator can resolve it in the little time left before the hold invoice expires.

Within this validity period, users can successfully complete the exchange, [cancel it](./cancelling-an-order.md) cooperatively, or open a [dispute](./disputes.md). After the [hold invoice](./hold-invoice.md) expires, Mostro has no ability to intervene in that order.

If both participants in a transaction are online and use instant fiat payment methods, the transactions can be completed almost instantly.
