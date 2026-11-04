# Accepted Currencies and Payment Methods

Mostro is a peer-to-peer (P2P) exchange, so it technically supports any currency and payment method, as long as there is a counterparty willing to make the trade.

However, each Mostro node operator can decide which fiat currencies to enable on their node. Before trading, make sure the node you choose supports the currency you want to trade with.

To price orders at market, each node takes the bitcoin price from one or more sources chosen by its operator, such as [yadio.io](https://yadio.io/), CoinGecko or Blockchain.com, and combines them. In the [Mostro App](./mostro-mobile.md) you can see which ones your node uses under *About → Node technical data*. If no source quotes your currency, you can still use Mostro by creating an order with a fixed amount of sats in exchange for a fixed amount of your currency.

The app only offers the currencies that the selected node accepts. Some nodes also accept dollar stablecoins (USDT, USDC, DOC) and bitcoin on other networks (on-chain BTC, Liquid, Rootstock): see [Stablecoins and Bitcoin on Other Networks](./stablecoins.md).

If your currency is not available on any existing node or does not appear as an option in the clients, you have two paths:

- Contact the administrator of an unrestricted node to explore the possibility of adding it
- Run your own Mostro node for your community, with the currencies and payment methods you need
