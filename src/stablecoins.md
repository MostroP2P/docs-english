# Stablecoins and Bitcoin on Other Networks

Some Mostro nodes let you trade Lightning sats for **dollar stablecoins** or for **bitcoin on other networks**, besides local currencies. Lightning sats are always one side of the trade. The other side is paid directly between the two of you, on the network named in the order.

| Code | What it is | Order amount in |
|---|---|---|
| `USDT` | Tether USD | coins (like dollars) |
| `USDC` | USD Coin | coins (like dollars) |
| `DOC` | Dollar on Chain, on Rootstock | coins (like dollars) |
| `BTC` | Bitcoin on-chain | sats |
| `LBTC` | L-BTC on the Liquid network | sats |
| `RBTC` | RBTC on Rootstock | sats |

Typical uses are moving between Lightning and Liquid or Rootstock (a swap), getting on-chain bitcoin for Lightning sats, or buying and selling sats for dollars without a bank.

## Which nodes offer them

Only nodes whose operator enabled them. The [Mostro App](./mostro-mobile.md) (version 2.1.2 or later) shows these codes in the currency list under **Stablecoins** and **Bitcoin on other networks**, but only those the selected node accepts. You can compare nodes under *Settings → Network → Mostro Node* and in *About*.

## How the price works

- **Stablecoins** are worth one dollar each, so a USDT order is priced exactly like a USD order. The [premium or discount](./fees-and-limits.md) works the same way.
- **BTC, LBTC and RBTC** are counted 1:1 in sats. An order for 100,000 means 100,000 sats of that asset (0.001 RBTC). At market price, the premium is the price of the swap: selling 100,000 sats of RBTC with a 1% premium means you lock 99,000 Lightning sats and receive 100,000 sats of RBTC. In the app you enter these amounts in sats.
- If a node accepts a code but does not price it at market, the app tells you *"This node doesn't quote {code} at market price. Set a fixed amount in sats."*

Mostro's usual [fee](./fees-and-limits.md) applies on top, as in any trade.

## The payment method is the network

The payment method of the order says on which network the asset is paid: for example `USDT (Tron)`, `USDT (Ethereum)`, `USDC (Base)`, `DOC (Rootstock)`, `BTC (On-chain)`, `LBTC (Liquid)` or `RBTC (Rootstock)`. An order can list several networks; agree in the chat on which one you will use. Mostro does not check the network or the address.

## Step by step

**If you are selling sats** (you receive the asset):

1. Pay the [hold invoice](./hold-invoice.md) as in any trade.
2. Share your receiving address in the trade chat. Make sure it is an address for the network you agreed on.
3. When the buyer marks the payment as sent, check with the transaction ID they pasted in the chat that the full amount arrived **and is confirmed**.
4. Only then tap **Release sats**.

**If you are buying sats** (you send the asset):

1. Send the asset **on the exact network** of the order, to the address the seller shared in the chat. You pay the network fee: the seller must receive the full amount.
2. Paste the transaction ID in the chat. It is your proof if there is a [dispute](./disputes.md). For Liquid, paste the **unblinded** transaction link: Liquid hides the amount, and that link shows it to the seller and to the solver.
3. Tap **I've sent the payment**.

## Safety rules

- **Wrong network, lost funds.** A stablecoin sent on a different network than the address belongs to can be lost for good.
- **Transfers can't be undone.** Mostro only holds the Lightning side; it never sees or checks the other transfer.
- **Wait for confirmation.** Never release on an unconfirmed transfer.
- **Mind the clock.** You have the same time as in any trade (see [Exchange Times](./times.md)). Use a network fee high enough for the transfer to confirm in time; a cheap on-chain transaction can take hours.
- **Stablecoins can lose their peg.** Their price is assumed to be one dollar. If one drifts far from that, think twice before trading it.

## Disputes

If something goes wrong, open a [dispute](./disputes.md) as usual. There is no bank statement here: the solver checks the transaction ID (or the unblinded Liquid link) in a block explorer for that network. That is why pasting it in the chat matters.

## Other clients

[mostro-cli](./mostro-cli.md) and [MostriX](./mostrix.md) can create these orders only at a fixed price for now, and do not show BTC, LBTC and RBTC amounts in sats. Older versions of the app have the same limitation.
