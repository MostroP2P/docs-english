# Clients. How to use Mostro

To use Mostro, you need to access it through a specific client. Below, we will cover several of them, which will allow you to interact both with Mostrod and with your counterpart in an operation.

The available Mostro clients so far are:
- **[Mostro App](./mostro-mobile.md)** (operational, beta): the official app, for Android, iOS, Windows, macOS, Linux and the web.
- **[Mostro-cli](./mostro-cli.md)** (operational): command line client.
- **[MostriX](./mostrix.md)** (operational): TUI client, which operates in the terminal with an enhanced appearance, with a mode for dispute solvers.

The old *Mostro Mobile* app (version 1) is deprecated: use the new Mostro App. Dispute solvers also have [Bosstro](https://github.com/MostroP2P/bosstro), an Android app for resolving disputes; it is not for trading.

Each client has particular features, so users can choose which one to use according to their interests and switch between them when they consider it convenient. The clients are responsible for creating, storing, and managing their users' Nostr keys. To learn how clients handle user privacy, read [here](./privacy.md).

Although some clients are already operational, they are under constant development, with new features being implemented, UX improvements, bug fixes, etc. You may encounter bugs; if this happens, please report them. Your feedback is very important.

**Note:** Two users using different Mostro clients can exchange sats; however, for direct communication between them, they must take into account what type of messages their respective clients accept. Clients must implement this [peer-to-peer chat](https://mostro.network/protocol/chat.html), but if a client has not yet implemented it, its users will not be able to view messages sent from a client that has implemented it. Similarly, this could occur with other functionalities. Developers of each client make their best effort to update them as soon as possible.

Since version 0.19.0, Mostro nodes speak only protocol v2. The current versions of the three clients above use it; older clients that still use NIP-59 gift wraps cannot trade on current nodes.

Mostro is a FOSS project, so anyone interested can create a client to interact with it. We encourage you to develop your own client or collaborate on the development of existing ones to enhance the experience of P2P Bitcoin exchanges without KYC on Nostr!

To learn more details about them, keep reading this documentation.