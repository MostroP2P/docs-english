# Privacy in Mostro

## User Communication Privacy with Mostro

Communication between Mostrod and users takes place through [Mostro clients](./clients.md) using Mostro's protocol v2: each message is a signed Nostr event of kind 14 whose content is encrypted with [NIP-44](https://github.com/nostr-protocol/nips/blob/master/44.md), so only your client and the node can read it. To enhance privacy, Mostro clients automatically generate a new key for each order you take or create, and that key signs your messages. Relays can see that a one-time key talks to a Mostro node, but not what it says, and buy and sell transactions cannot be linked to a single person from the outside.

Mostro clients will never share users' private keys with a Mostro node or its administrator under any circumstances.

Since version 0.19.0, Mostro nodes speak only protocol v2. Clients that still use the old protocol (NIP-59 gift wraps) cannot trade on them.

### Reputation Mode

Mostro offers users the option to operate in `reputation mode`, the default in the [Mostro App](./mostro-mobile.md). In this mode, your client proves to the Mostro node you are using that the order belongs to your fixed identity key. That proof travels inside the encrypted message, so only that node learns it. The node can then associate a [reputation](./reputation.md) with you based on ratings received from your counterparts after completing transactions. Your identity key is not shared with other users or exposed publicly, and each new order continues to use one-time keys, protecting the details of each exchange from third parties.

### Full Privacy Mode

For users who prioritize privacy above all else, Mostro offers `full privacy mode`. In this mode, your client sends no identity proof to the Mostro node. Each transaction uses only the one-time key generated for that exchange, so the node has no way to link orders from the same user, providing the highest level of anonymity.

Since in `full privacy mode` there is no fixed key associated with you, it is not possible to build or keep a reputation: you neither give nor receive ratings, your reputation appears as 0 to your counterparts, and your trades cannot be [restored](./backup-restore.md) on another device. You also cannot [import a reputation](./reputation-import.md).

In the Mostro App you switch between both modes under *Account → Privacy*; the choice is kept until you change it.

## Privacy in User-to-User Communication

Communication between the buyer and seller during a transaction occurs directly from client to client through an end-to-end encrypted chat, integrated into the Mostro clients. Both clients derive a shared key using [Elliptic Curve Diffie-Hellman (ECDH)](https://mostro.network/protocol/chat.html#shared-key). Each message is encrypted with NIP-44 and signed by the sender's trade key, then wrapped in a kind-14 event addressed to that shared key. This "shared master key" is known only to the buyer and seller, ensuring that neither the Mostro node where they are transacting nor third parties can read or inject messages. Additionally, since each transaction generates new and unique keys, privacy remains intact even between transactions with the same counterparty.

In case of a [dispute](./disputes.md), this shared key provides an effective solution: either party can choose to voluntarily share it with the solver. With it, the solver can decrypt only the conversation of that specific transaction, accessing an immutable copy of the messages, which cannot be altered or deleted. This allows disputes to be resolved fairly and transparently, exposing any attempts at deception without compromising the default privacy of users and only revealing information when necessary and with consent.

Some nodes use [Serbero](./disputes.md#serbero-the-automated-assistant), an automated dispute assistant. If you write to it during a dispute, your messages are processed by an automated service that the node's operator uses.

## Other Details

- Push notifications carry no content: they only tell your device that there is something to see in the app.
- If you connect a wallet through Nostr Wallet Connect (NWC), its connection string stays on your device.
- Importing your reputation from another source links your accounts on both sides. See [Importing Your Reputation](./reputation-import.md).
