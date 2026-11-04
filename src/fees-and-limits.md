# Exchange Fees and Limits

Each operator of a Mostro node can set their own fees and limits per transaction, fostering competition among different nodes and allowing users to select the one that best suits their needs.

## Fees

The node's fee is split in half between the buyer and the seller for each completed transaction. The exact percentage depends on the Mostro node you use: most community nodes charge between 0.5% and 1% in total.

For example, a node with a 1% fee charges 0.5% to the buyer and 0.5% to the seller. The [Mostro App](./mostro-mobile.md) shows the **total** fee of each node, under *Settings → Network → Mostro Node* and in *About → Connected node*. When you pay the hold invoice as a seller, the app tells you how many sats of it are the fee.

Resolving a [dispute](./disputes.md) costs nothing extra. The [anti-abuse deposit](./anti-abuse-bond.md) some nodes ask for is not a fee: you get it back when you trade in good faith.

## Limits

Each node also defines the minimum and maximum amount in sats allowed per transaction. You can see them in the app under *About → Connected node* (*Min order* and *Max order*), and the app checks your order against them before publishing it.

## Multiple Mostro Nodes

Mostro is designed to be a decentralized system where multiple operators can run their own nodes. This means that:

- There is competition among nodes to offer the best service
- Each operator defines their own fees, limits, and accepted currencies
- Users are free to choose which node to trade on
- If one node goes down, others remain available

You can check whether a node is working on the [status page](./node-status.md).

## Development Contribution

Each Mostro node automatically contributes a percentage of its earnings to the project's development fund. This contribution comes from the operator's earnings and is not charged extra to users.

This system ensures the sustainability of Mostro's development in a transparent way: all contributions are published as events on Nostr and can be verified by anyone.

For more details on how this system works, you can read the full article: [Sustainable Funding for Mostro Development](https://mostro.network/blog/dev-fee-sustainability/)
