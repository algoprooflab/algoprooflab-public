# Polymarket from zero: markets, shares and resolution

[Русская версия](POLYMARKET_FROM_ZERO_RU.md)

## What a prediction market is

A prediction market lets participants trade the possible outcomes of a future event. Each market has a question, a set of outcomes and resolution rules. A Bitcoin market, for example, may ask whether the price will finish above or below a specified level at a specified time.

Instead of buying a coin or a stock, the trader buys shares of an outcome. A two-sided market normally uses `YES/NO` or `UP/DOWN`.

## What the price means

A share is priced between $0 and $1. A price of `$0.63` is often read as the market assigning roughly a 63% probability to that outcome. It is not a fixed forecast. The price changes as participants add, cancel and execute orders.

Polymarket does not manually choose that price. It emerges from the prices at which buyers and sellers are willing to trade.

## What happens at resolution

When a market resolves:

- one winning share pays $1;
- a losing share pays $0;
- trading in that market ends.

Before resolution, a position can normally be sold to another participant at an available order-book price.

The short title is not enough to determine the winner. Every market has resolution rules, a source and provisions for exceptional cases. Those rules decide the result.

## Bitcoin Up/Down 5m markets

These markets cover a short five-minute interval. Before trading, check:

1. the exact start and end time;
2. the price source;
3. what qualifies as `UP` or `DOWN`;
4. how ties or disputed prices are handled;
5. available orders and fees.

A new market appearing frequently does not mean every market offers a useful trade. The price may already reflect the expected move, or the order book may not contain enough volume.

## Example

Buying 10 `UP` shares at $0.60 costs $6 before expenses.

- If `UP` wins, the 10 shares pay $10, for a gross result of `$10 − $6 = $4`.
- If `DOWN` wins, the shares pay $0 and the position loses $6.

The actual result depends on share quantity, execution price, fees and the final outcome.

Continue with [share price, quantity and PnL](SHARES_PRICE_AND_PNL_EN.md).

