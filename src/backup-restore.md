# Account Backup and Restoration

Your identity on Mostro is based on a private key that clients automatically generate when you create your account. This key is represented as a 12-word phrase (seed phrase) that you must store securely.

## Why Backup Matters

Without a backup of your 12-word phrase, you could lose:

- Access to active trades: if you switch devices or reinstall the app during an exchange, you won't be able to continue the operation
- Your reputation: the ratings you've accumulated are tied to your identity; without a backup, you'd start from scratch
- History: you won't be able to recover information from previous trades

## How to Back Up

In the [Mostro App](./mostro-mobile.md), go to *Account → Secret Words* and tap **Show words**. The app guides you in three steps: write the 12 words on paper, tap three of them to check you wrote them right, done. Until you do it, the app reminds you with a *Secure your reputation* banner.

The app does not include your keys in your phone's cloud backup or device transfer, so the 12 words are the only way to get your account back on a new device.

Other [Mostro clients](./clients.md) have their own way of displaying your 12-word phrase. Check their documentation.

The important things are:

- Write down the 12 words in the correct order
- Store them in a safe and private place
- Do not share them with anyone
- Do not store them in plain text on internet-connected devices

## Restoring Your Account

If you need to switch devices, reinstall the app, or use a different client, you can restore your identity by importing your 12-word phrase.

When restoring:

- You recover your identity and reputation
- In the Mostro App, you can continue trades that were active (reputation mode only). mostro-cli cannot resume an in-flight trade from the 12 words alone: for that it needs its `~/.mcli/mcli.db` file
- You can access from any compatible Mostro client

In the Mostro App, go to *Account → Import Mostro User* and enter your 12 words. The app asks the node you use for your orders and trades and rebuilds them. Restoring works per node: when you switch to another node, the app restores what you have there too. Before importing, if the current user still has trades in progress, the app warns you that *"This user still has sats in play"*.

If you used the old Mostro Mobile app, you can import the same 12 words into the new Mostro App: both use the same keys. Finish any open trade in the old app first.

## Important: Full Privacy Mode

If you operate in [full privacy mode](./privacy.md), orders created in that mode cannot be recovered when restoring your account. Only orders created in reputation mode can be restored.

This is because in full privacy mode there is no fixed key associated with your identity, so Mostro cannot link those operations to your restored account.

## Recommendations

- Back up as soon as you create your account, before your first trade
- Verify that you wrote the words correctly before you need them
- Consider keeping more than one copy in different secure locations
- Never share your phrase with anyone, not even Mostro support
- If you value being able to recover active trades, use reputation mode
