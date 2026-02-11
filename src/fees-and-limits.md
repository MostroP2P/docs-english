# Exchange Fees and Limits

Each operator of a Mostro node can set their own fees and limits per transaction, fostering competition among different nodes and allowing users to select the one that best suits their needs.

## Fees

Fees are charged to both the buyer and the seller for each completed transaction. The exact percentage depends on the Mostro node you use.

The Mostro node currently active on mainnet (`npub1stagewtcks78nvs4vkzm4skqzytk5gwj46kkm8mu2awqqklgswgqfvtamr`) charges a 0.3% fee to both the buyer and the seller.

## Limits

Each node also defines the minimum and maximum amounts allowed per transaction. The main node on mainnet allows exchanges from 100 sats to 20,000 sats per operation.

## Multiple Mostro Nodes

Mostro is designed to be a decentralized system where multiple operators can run their own nodes. This means that:

- There is competition among nodes to offer the best service
- Each operator defines their own fees, limits, and accepted currencies
- Users are free to choose which node to trade on
- If one node goes down, others remain available

## Development Contribution

Each Mostro node automatically contributes a percentage of its earnings to the project's development fund. This contribution comes from the operator's earnings and is not charged extra to users.

This system ensures the sustainability of Mostro's development in a transparent way: all contributions are published as events on Nostr and can be verified by anyone.

For more details on how this system works, you can read the full article: [Sustainable Funding for Mostro Development](https://mostro.network/blog/dev-fee-sustainability/)
