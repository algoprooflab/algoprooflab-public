# Order books, liquidity and slippage

[Русская версия](ORDERBOOK_AND_LIQUIDITY_RU.md)

## What the order book shows

An order book lists active buy and sell orders. Each level contains a price and an available number of shares.

Three values are often confused:

- **last price** — the price of a completed trade;
- **best ask** — the cheapest active sell order;
- **average fill price** — the weighted average of every part of your executed order.

For a small order, these values may be close. For a large order, they can differ materially.

## Example of a larger order

| Available quantity | Price |
|---:|---:|
| 100 shares | 0.50 |
| 200 shares | 0.53 |
| 400 shares | 0.57 |

An order for 50 shares can fill entirely at 0.50. An order for 400 shares consumes the first two levels and part of the third, giving a higher average price.

The difference between the expected price and the actual fill is slippage. When a strategy has a small expected edge, even a few extra cents may remove it.

## Why a $1 result cannot always be multiplied

Multiplying a 1 USDC historical result by 20, 100 or 400 shows arithmetic scale only. It does not prove that the larger order could have filled at the same price.

Large-stake validation requires historical order-book snapshots or real execution at a similar size. Useful measurements include depth before a price limit, weighted average price, partial fills, signal-to-fill delay and rejected orders.

## Limit and aggressive orders

A limit order sets the highest acceptable purchase price. It protects against an unexpectedly expensive fill but may fill partially or not at all.

An aggressive order increases the chance of immediate execution but can consume several order-book levels. The correct choice depends on how quickly the signal decays and how much expected edge remains after costs.

