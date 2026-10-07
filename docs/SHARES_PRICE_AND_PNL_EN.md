# Share price, quantity and PnL

[Русская версия](SHARES_PRICE_AND_PNL_RU.md)

## Stake and share quantity are different

Allocating 20 USDC to a trade does not mean buying 20 shares. Quantity depends on price:

```text
share quantity = trade amount / share price
```

At a price of $0.60, 20 USDC buys about 33.33 shares before fees and rounding. If that outcome wins, each share pays $1:

```text
gross payout = share quantity × $1
gross PnL = payout − purchase cost
```

The example pays about $33.33 and produces about $13.33 gross profit.

## The same stake at different entry prices

| Share price | Approximate shares | Gross profit if the outcome wins |
|---:|---:|---:|
| 0.40 | 50.00 | +30.00 USDC |
| 0.50 | 40.00 | +20.00 USDC |
| 0.60 | 33.33 | +13.33 USDC |
| 0.80 | 25.00 | +5.00 USDC |
| 0.90 | 22.22 | +2.22 USDC |

If the outcome loses, the position loses its purchase cost: 20 USDC in this example.

The higher the share price, the more often the strategy must be correct to offset occasional full-position losses. A high win rate alone therefore does not prove profitability.

## Why real PnL differs

The simple formula assumes the whole order fills at one price. Real execution may include:

- several order-book levels;
- partial fills;
- price movement between signal and submission;
- fees;
- rounding;
- cancelled or rejected orders.

A useful journal records the requested amount, filled quantity, average fill price, fees and final outcome.

Continue with [order books, liquidity and slippage](ORDERBOOK_AND_LIQUIDITY_EN.md).

