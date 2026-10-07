# AlgoProof Lab

**Verifiable research, self-hosted trading software and strategy reports for prediction markets.**

[English](README.md) | [Русский](README_RU.md)

![AlgoProof Lab](assets/algoprooflab-avatar-v1.png)

AlgoProof Lab has researched crypto-market automation since 2022. This public repository explains how prediction-market prices, shares, order books, execution and strategy validation work. It also contains reproducible reports and sample data for our first Polymarket client package.

The commercial strategy source code and downloadable client are not published here. Buyers run the client on their own VPS and keep control of their credentials, funds and risk settings.

## Laboratory live trading

Current continuous live-trading journal: **September 15 through October 7, 2026**.

| Metric | Value |
|---|---:|
| Completed real trades | 469 |
| Profitable / losing trades | 271 / 198 |
| Profitable outcomes | 57.78% |
| Net result after fees | **+485.82 USDC** |

The laboratory tested several strategy versions during this period. These figures therefore describe the verified laboratory account as a whole, not the claimed performance of one product. See the [live-trading explanation](docs/LIVE_TRADING_EN.md) and the machine-readable files in [`data`](data/).

## First product: SALEBOT-5M-BR72

Historical study period: **August 4 through October 4, 2026**.

| Metric | Value |
|---|---:|
| Closed markets in the source dataset | 17,564 |
| Strategy trades | 471 |
| Profitable outcomes | 56.26% |
| Result at a fixed 1 USDC stake | +30.02 USDC |
| Maximum modeled drawdown | 9.35 USDC |
| Stress test with doubled slippage | +25.18 USDC |

### Linear stake illustration

| Stake per trade | Arithmetic result | Arithmetic maximum drawdown |
|---:|---:|---:|
| 20 USDC | +600.40 USDC | 187 USDC |
| 40 USDC | +1,200.80 USDC | 374 USDC |
| 100 USDC | +3,002 USDC | 935 USDC |
| 400 USDC | +12,008 USDC | 3,740 USDC |

This table multiplies the same 471 historical signals. It does **not** prove that larger orders could have filled at the original prices. The standard license is currently limited to 100 USDC per trade; the 400 USDC line is shown only as an arithmetic scale illustration and requires separate order-book validation.

## Start here

- [Polymarket from zero: markets, shares and resolution](docs/POLYMARKET_FROM_ZERO_EN.md)
- [Share price, quantity and PnL](docs/SHARES_PRICE_AND_PNL_EN.md)
- [Order books, liquidity and slippage](docs/ORDERBOOK_AND_LIQUIDITY_EN.md)
- [How a trading bot works](docs/HOW_TRADING_BOT_WORKS_EN.md)
- [Backtest, demo mode and live trading](docs/BACKTEST_VS_LIVE_EN.md)
- [Calculation methodology](docs/METHODOLOGY_EN.md)

## Evidence and product information

- [Historical BR72 report](docs/BR72_REPORT_EN.md)
- [Live laboratory trading](docs/LIVE_TRADING_EN.md)
- [Product access and strategy updates](docs/PRODUCT_ACCESS_EN.md)
- [Installation overview](docs/INSTALLATION_OVERVIEW_EN.md)
- [Frequently asked questions](docs/FAQ_EN.md)
- [Public summary in JSON](data/BR72_PUBLIC_SUMMARY.json)
- [Sample trade rows in CSV](data/BR72_SAMPLE_TRADES.csv)
- [Live public summary](data/LIVE_PUBLIC_SUMMARY.json)
- [Security and credential handling](SECURITY_EN.md)
- [Release history](CHANGELOG.md)

## What the buyer receives

- a self-hosted client package;
- an initial setup wizard;
- control and notifications through the buyer's own Telegram bot;
- demo mode without order submission;
- live mode with local stake and daily-loss limits;
- one 48-hour trial per Telegram account and VPS;
- installation instructions from VPS rental through startup;
- installation support;
- either one fixed strategy or automatic strategy changes during an active update plan.

The shop never asks for or stores a buyer's wallet private key, seed phrase, Polymarket API secret, Telegram bot token or VPS password.

## Access options

- **200 USD** — client bot and one fixed strategy with no time limit;
- **400 USD** — client bot and automatic strategy changes for 30 days;
- **200 USD** — another 30 days of strategy updates.

If the update plan expires, the client keeps using the last strategy it received.

Open the bilingual Telegram shop: [@algoproof_shop_bot](https://t.me/algoproof_shop_bot?start=github).

Digital-product payments inside Telegram are invoiced in Telegram Stars. USDT purchases are handled through [@algoproof_support](https://t.me/algoproof_support) after the buyer receives an order number and exact payment instructions. Never send anyone a private key, seed phrase or wallet password.

## Status

```text
Product: SALEBOT-5M-BR72
Version: 1.0.0
Strategy status: ACTIVE
Public evidence: available
Sales: closed beta
```

- Telegram publication channel: [@algoprooflab](https://t.me/algoprooflab)
- Telegram shop: [@algoproof_shop_bot](https://t.me/algoproof_shop_bot?start=github)
- Support: [@algoproof_support](https://t.me/algoproof_support)
