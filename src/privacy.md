# Privacy in Mostro

## User Communication Privacy with Mostro
Communication between Mostrod and users takes place through [Mostro clients](./clients.md) using [NIP-59](https://github.com/nostr-protocol/nips/blob/master/59.md) events. Within these events, the content and the public key of the sender are encrypted with an ephemeral key, preventing the public revelation of the identity of those interacting with Mostro. To enhance privacy, Mostro clients automatically generate a new private key for users for each order they take or create. This way, when Mostro sends NIP-59 events to users, the generated event will display a public key that is used only for that operation, ensuring a new `"identity"` for each exchange and preventing buy and sell transactions from being linked to a single person.

Mostro clients will never share users’ private keys with a Mostro instance or its administrator under any circumstances.

### Reputation Mode

Mostro offers users the option to operate in a `reputation mode`. In this mode, users identify themselves to the Mostro instance they are using with a fixed public key that acts as a primary identifier, allowing that instance to associate a [reputation](./reputation.md) with the user based on ratings received from their counterparts after completing transactions. Although this public key is known to that particular Mostro instance, it is not shared with other users or exposed publicly, thereby preserving individual privacy. In this mode, each new order continues to use ephemeral keys, protecting the details of each exchange from third parties.

### Full Private Mode

For users who prioritize privacy above all else, Mostro offers `full private mode`. In this mode, users do not send any fixed identifying key to the Mostro instance they use. Instead, each transaction exclusively uses ephemeral keys generated for that specific exchange. This means that the Mostro instance has no way to link orders from the same user, providing the highest level of anonymity. Thus, not even a Mostro instance can determine which transactions belong to the same person.

Since in `full private mode` there is no fixed key associated with the user, it is not possible to build or maintain a reputation. When someone in this mode creates a new order, their reputation will appear as 0, just as if they were a new user. However, for those who value absolute privacy over trust based on ratings, this mode is ideal.

## Privacy in User-to-User Communication
Communication between the buyer and seller during a transaction occurs directly from client to client through an end-to-end encrypted chat, integrated into the Mostro clients. This system uses a simplified version of NIP-59 to hide metadata from external observers, and messages are directed to a unique shared public key generated using advanced cryptography ([Elliptic Curve Diffie-Hellman or ECDH](https://mostro.network/protocol/chat.html#shared-key)). This "shared master key" is known only to the buyer and seller, ensuring that neither the Mostro instance where they are transacting nor third parties can access the conversation content. Additionally, since each transaction generates new and unique keys, privacy remains intact even between transactions with the same counterparty.

In case of a [dispute](./disputes.md), this shared key provides an effective solution: either party can choose to voluntarily share it with the designated mediator. With it, the mediator can decrypt only the conversation of that specific transaction, accessing an immutable copy of the messages, which cannot be altered or deleted. This allows disputes to be resolved fairly and transparently, exposing any attempts at deception without compromising the default privacy of users and only revealing information when necessary and with consent.
