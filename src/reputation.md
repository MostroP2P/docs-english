# Reputation System

Upon successfully completing a purchase or sale of sats, Mostro will ask you to rate your counterparty, and your counterparty will also rate you. The reputation system uses a 5-star rating scale, where 1 star represents the lowest rating and 5 stars the highest, allowing you to evaluate the transaction experience.

Reputation in Mostro is calculated iteratively, combining the mean and standard deviation of ratings and successful transactions. This means that during your first transactions, even if you receive maximum ratings, your initial reputation will not be very high; instead, it will progressively increase as you accumulate more successful transactions with good evaluations.   
This calculation is based on: [https://math.stackexchange.com/questions/2148877/iterative-calculation-of-mean-and-standard-deviation](https://math.stackexchange.com/questions/2148877/iterative-calculation-of-mean-and-standard-deviation).

## Where your reputation lives

Your reputation is kept by each Mostro node, for your identity, and only in [reputation mode](./privacy.md#reputation-mode): in full privacy mode you neither give nor receive ratings. In the [Mostro App](./mostro-mobile.md) you can see your own reputation on the node you use under *Account*. If you switch to another node, you start with the reputation you have there.

## Bringing your reputation with you

If you earned a reputation on [@lnp2pBot](https://t.me/lnp2pbot) or on another Mostro node, you can import it into the node you use now, as long as that node trusts the source. Your counterparties then see your reputation from both places combined. See [Importing Your Reputation](./reputation-import.md).
