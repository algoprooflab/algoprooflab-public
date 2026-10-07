# Security and credential handling

## Secrets that remain with the buyer

- wallet private key;
- seed phrase;
- Polymarket API key, secret and passphrase;
- Telegram bot token;
- VPS password and SSH key.

None of these secrets is required to purchase a license or bind it to a VPS.

## Data the shop may store

- buyer Telegram ID;
- order number;
- non-secret VPS binding code;
- license type and expiration;
- delivered product version;
- payment identifier and status;
- interface language and acquisition source.

## Client-package checks

Before release, the archive is scanned for common Telegram-token formats, private keys, filled API secrets and local developer paths. The published checksum lets a buyer verify that the downloaded archive matches the released package.

Do not publish private keys, tokens, passwords or full configuration files in GitHub Issues. Contact [@algoproof_support](https://t.me/algoproof_support) for a private support channel.
