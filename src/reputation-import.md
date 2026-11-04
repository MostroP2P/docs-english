# Importing Your Reputation

If you already traded on [@lnp2pBot](https://t.me/lnp2pbot) or on another Mostro node, you don't have to start from zero. You can bring the reputation you earned there to the Mostro node you use now.

## What travels

Three figures travel with you:

- how many ratings you received,
- your average rating,
- the date of your first trade.

The source signs them in a small Nostr event, called an attestation, addressed to your Mostro identity. It is valid for 7 days. The node you import into adds those figures to the reputation you already have there. Your counterparties see a single rating, a single number of reviews and a single "trading since" date. Nothing marks a figure as imported.

> **Example:** you have 2 ratings averaging 4.5 on a Mostro node, and you import 214 ratings averaging 4.87 from lnp2pBot. Your counterparties on that node now see about 4.87 from 216 ratings, trading since the older of your two first trades (here, your first lnp2pBot trade).

## Before you start

- Use a recent version of the [Mostro App](./mostro-mobile.md).
- Use **reputation mode** (*Account → Privacy*). In [full privacy mode](./privacy.md) there is no identity to carry a reputation, so the import buttons are disabled.
- [Back up your 12 words](./backup-restore.md). Your reputation is tied to your identity.
- Select a node that accepts imports from that source. Not every node does: each operator decides which sources to trust. If the node does not import, the app tells you: *"This Mostro does not import reputation."*

## From lnp2pBot

The bot exports your reputation if your account has at least **10 completed trades** and **5 ratings received**, and is not banned.

1. In the Mostro App, open *Settings → Network → Mostro Node* and select the node where you want your reputation.
2. Go to *Settings → Network → Reputation* and tap **Import reputation**.
3. Note the public key (npub) the screen shows, then tap **Get it from lnp2pBot**. Telegram opens a private chat with the bot.
4. The first time, the bot shows the npub it will export to. Check that it is exactly the one your app shows, then tap **Confirm and export**. This links your bot account to that Mostro identity.
5. The bot sends two messages: a summary, and the attestation itself. Copy the **second message whole**.
6. Back in the app, paste it in *"Paste the reputation you received"* and tap **Check**. The app shows who issued it and your figures, for example *"★ 4.87 · 214 ratings · since …"*.
7. Tap **Import into this Mostro**. The app confirms: *"Your reputation was imported."*

> **Tip:** Open the link from the app, on a device that has Telegram. Opening the bot by hand does not work: the bot needs the link the app builds, which carries your identity.

If you need another copy later, for example to import on a second node, repeat the steps. The bot sends a new attestation for the same identity without asking you to confirm again.

## From another Mostro node

You can also carry the reputation you earned on one Mostro node (A) to another (B). Node A must offer export, and node B must trust node A.

1. Select node A. Go to *Settings → Network → Reputation → Export my reputation* and tap **Export my reputation**. Leave the authorization field empty.
2. Confirm the identity in *"Export to this identity?"* with **Export**. The app says your reputation is ready and valid for 7 days.
3. Select node B in *Settings → Network → Mostro Node*.
4. Open *Settings → Network → Reputation → Import reputation*. The attestation is already filled in and checked.
5. Tap **Import into this Mostro**.

Node A exports only the reputation you earned **on node A**: at least 10 completed trades and 5 ratings received there. Reputation you imported into node A does not travel again.

## Importing on several nodes

- You have to import separately on each node where you want your reputation.
- The same attestation works on several nodes while it is valid (7 days). After a successful import the app clears its copy, so keep the copied text, or simply export again.
- On each node you can import **once from each source**: for example, once from lnp2pBot and once from another Mostro node.

## If you change identity

- **Restoring the same 12 words** gives you the same identity. Nothing to do.
- **Moving to a new identity:** your reputation on the source is bound to your old identity. With the old identity active, go to *Reputation → Move to a new identity*, enter the new npub and tap **Sign for this Mostro** (or **Sign for lnp2pBot** if it came from the bot). Copy the authorization, valid for one hour. Then, with the new identity active, paste it in the export field (Mostro) or in the bot chat (lnp2pBot).
- **If you lost the old identity**, only the node's operator (or the lnp2pBot admins) can move it, after checking it is you.

## What you should know

- **Importing links two accounts.** The source learns which Mostro identity received your reputation, and the node you import into learns which account it came from. With lnp2pBot, Telegram sees it too. If you don't want those accounts linked, don't import.
- **It cannot be undone** by you, and it uses up that source for your identity on that node.
- **It is a snapshot.** Ratings you receive later on the source are not added.
- **Only you can use it.** An attestation is addressed to your identity: if someone else copies it, they cannot import it.

## Messages you may see

| Message | What it means |
|---|---|
| This Mostro does not import reputation. | The node you selected has import turned off. Choose another node. |
| This Mostro does not accept reputation from that source. | The node does not trust the source that signed your attestation. |
| This Mostro does not export reputation. | The node you selected does not offer export. |
| Your account cannot export its reputation yet… | You don't have 10 completed trades and 5 ratings received on that source yet. |
| Reputation can only be moved from an account that keeps its reputation… | You are in full privacy mode. Switch to reputation mode. |
| This reputation has expired. Request it again from its source. | It is more than 7 days old. Get a new one. |
| This reputation was issued for another identity than the one you are using. | You switched identity after getting it. Use the identity it was issued for, or see "If you change identity". |
| This reputation was already imported on this Mostro. | You already imported from that source on this node. |
| Your reputation there is already bound to another identity… | See "If you change identity". |
