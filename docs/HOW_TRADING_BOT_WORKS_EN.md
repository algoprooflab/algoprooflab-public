# How a trading bot works

[Русская версия](HOW_TRADING_BOT_WORKS_RU.md)

A trading bot is not a single “guess the direction” command. It is a sequence of checks. Every stage may allow a trade, reduce its size or stop execution.

## 1. Data collection

The client receives the target market, timestamps, prices and orders. Data must be fresh: a delayed quote may no longer describe a five-minute market.

## 2. Market validation

The bot checks the market identifier, end time, available outcomes and trading status. A closed market, incomplete data or a market outside the strategy scope becomes a logged skip.

## 3. Strategy decision

The strategy returns one of three decisions:

- buy `UP`;
- buy `DOWN`;
- skip the market.

No trade is a valid result. If the price is outside a limit, liquidity has disappeared or the signal is too weak, forcing a purchase only adds risk.

## 4. Local risk controls

Even after receiving a signal, the client checks the maximum stake, daily-loss limit, market type, signal age, license state, selected mode and the buyer's manual stop setting.

A remote strategy update cannot raise limits configured locally on the buyer's VPS.

## 5. Submission and fill confirmation

The client submits an order and verifies its actual state. “Order accepted” does not mean fully filled. The journal records the order ID, filled quantity, average price, fees and any remaining quantity.

## 6. Settlement

After resolution, the client links the outcome to the actual filled order and updates the journal. PnL is calculated from filled quantity rather than the originally requested amount.

## 7. Telegram

Telegram is used as a control panel and notification channel. Trading credentials remain in the VPS configuration and are not sent to the shop.

## Demo and live modes

Demo mode runs the decision pipeline and writes logs without submitting an order. Live mode adds order submission and fill verification. Execution testing should begin with the smallest permitted position size.

