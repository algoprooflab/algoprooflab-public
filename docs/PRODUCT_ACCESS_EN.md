# Product access and automatic strategy changes

[Русская версия](PRODUCT_ACCESS_RU.md)

The client is installed once on the buyer's VPS. It contains the Polymarket connection, Telegram control, local risk limits, trade journal and license checks. Commercial strategy logic remains on the AlgoProof server and produces signed signals for licensed clients.

## Fixed strategy — 200 USD

- client bot and one-VPS license;
- one selected strategy version with no time limit;
- later changes to the active strategy do not replace it;
- security updates to the client are released separately.

## Strategy updates — 400 USD

- client bot and one-VPS license;
- the current active strategy;
- automatic strategy changes for 30 days;
- no reinstallation or credential re-entry when the strategy changes.

The client renews its permission every ten minutes. It then receives a license-bound signed signal and verifies the signature before any execution.

## Renewal — 200 USD for 30 days

A renewal adds another 30 days of automatic changes. Without renewal, the client keeps using the last strategy received before expiration; access to later changes pauses.

## Strategy-change process

1. The laboratory registers a new version separately from production.
2. The version passes internal checks and receives an identifier.
3. The owner changes the `ACTIVE` channel to the new version.
4. Active update plans receive it during the next permission refresh.
5. Fixed licenses remain on their assigned version.
6. The change date and strategy identifier are added to release history.

Wallet private keys, API secrets, Telegram tokens and VPS passwords remain on the buyer's server.

