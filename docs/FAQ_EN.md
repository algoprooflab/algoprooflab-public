# Frequently asked questions

[Русская версия](FAQ_RU.md)

## Does the shop receive access to the buyer's wallet?

No. Secrets are entered directly on the buyer's VPS. License issuance needs only the generated VPS code.

## Can I test without real money?

Yes. Demo mode generates decisions and journal entries without submitting orders.

## What is the 48-hour trial?

It is the complete client for one VPS, limited to 48 hours and a maximum 3 USDC stake. The buyer can install it, connect a personal Telegram bot and begin in demo mode.

## Why can a strategy be replaced or removed?

Markets change. If new validation or live measurements no longer meet the criteria, a strategy can move to `WATCH` and later be removed from the active channel.

## How do automatic strategy updates work?

The 400 USD plan includes the client and 30 days of access to the active strategy. When the laboratory changes the active version, the client receives the new version during its next permission refresh. The strategy source is not delivered; the server produces a signed signal and the client verifies it before applying local limits.

After expiration, the bot remains on the last strategy it received. Another 30 days costs 200 USD.

## What is a fixed strategy?

The 200 USD plan assigns one selected strategy to the license without a time limit. Later changes to the active channel do not affect that license.

## Can the stake be increased?

The license sets a maximum. The buyer chooses the actual stake while considering liquidity and risk. A historical 1 USDC result cannot be carried to larger orders without separate execution validation.
