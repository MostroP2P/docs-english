# Account Backup and Restoration

Your identity on Mostro is based on a private key that clients automatically generate when you create your account. This key is represented as a 12-word phrase (seed phrase) that you must store securely.

## Why Backup Matters

Without a backup of your 12-word phrase, you could lose:

- Access to active trades: if you switch devices or reinstall the app during an exchange, you won't be able to continue the operation
- Your reputation: the ratings you've accumulated are tied to your identity; without a backup, you'd start from scratch
- History: you won't be able to recover information from previous trades

## How to Back Up

Each [Mostro client](./clients.md) has its own way of displaying and backing up your 12-word phrase. Check the documentation of the client you use to learn how.

The important things are:

- Write down the 12 words in the correct order
- Store them in a safe and private place
- Do not share them with anyone
- Do not store them in plain text on internet-connected devices

## Restoring Your Account

If you need to switch devices, reinstall the app, or use a different client, you can restore your identity by importing your 12-word phrase.

When restoring:

- You recover your identity and reputation
- You can continue trades that were active
- You can access from any compatible Mostro client

The exact restoration process depends on the client you use. Check the specific client documentation for detailed steps.

## Important: Full Privacy Mode

If you operate in [full privacy mode](./privacy.md), orders created in that mode cannot be recovered when restoring your account. Only orders created in reputation mode can be restored.

This is because in full privacy mode there is no fixed key associated with your identity, so Mostro cannot link those operations to your restored account.

## Recommendations

- Back up as soon as you create your account, before your first trade
- Verify that you wrote the words correctly before you need them
- Consider keeping more than one copy in different secure locations
- Never share your phrase with anyone, not even Mostro support
- If you value being able to recover active trades, use reputation mode
