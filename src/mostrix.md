# MostriX

MostriX is a Mostro client with a TUI (Terminal User Interface) primarily focused on Mostro node administrators. Its visual terminal interface allows managing disputes and administering the node efficiently, without the need to type commands manually.

![mostrix](./assets/images/mostrix.png)

> **Note:** MostriX is in active development. Some features may be incomplete or require additional testing.

## Installation

```bash
git clone https://github.com/MostroP2P/mostrix.git
cd mostrix
cargo run
```

Requirements: Rust 1.90 or higher.

## Implemented Features

- View order book
- Create buy and sell orders
- Create buy orders with Lightning Address
- Take orders (buy and sell)
- Confirm fiat sent
- Release sats
- Add new invoice if payment fails
- Automatic 12-word seed generation
- Key management according to the Mostro protocol
- Configuration via settings.toml file

## Features in Development

- Peer-to-peer chat
- List own orders
- Cooperative cancellation
- Rate counterparties
- Dispute flow

## Configuration

MostriX is configured through a `settings.toml` file. On first run, it is automatically created at `~/.mostrix/settings.toml`.

Main parameters:

- `mostro_pubkey`: Public key of the Mostro node
- `nsec_privkey`: Your Nostr private key
- `relays`: List of relays to connect to
- `currencies`: Fiat currencies you're interested in

## More Information

MostriX is a FOSS project. You can visit its [GitHub repository](https://github.com/MostroP2P/mostrix) to learn more about its development, report bugs, or propose improvements.
