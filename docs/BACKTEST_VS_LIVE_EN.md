# Backtest, demo mode and live trading

[Русская версия](BACKTEST_VS_LIVE_RU.md)

Different forms of strategy evidence answer different questions and should not be combined into one number.

## Historical test

A backtest applies fixed rules to past data. It can show signal frequency, period-by-period results, modeled drawdown and sensitivity to price and costs.

Its main risks are selecting a favorable period, using information that would not have been available at decision time and assuming unrealistic execution.

## Out-of-sample check

Rules are developed on one dataset and then applied without changes to a later period. This reduces overfitting risk but still uses historical data.

## Demo mode

Demo mode processes current markets in real time without submitting orders. It validates data collection, timing, decision logic and notifications. It does not prove fill price, fees or partial-fill behavior.

## Live trading

A live journal records submitted and filled orders. It should include decision time, strategy version, requested and filled amounts, average price, fees, settlement result and execution errors.

Live trading tests delays, order-book conditions and API behavior. A short live period can still be lucky, so duration, trade count and sample structure matter.

## AlgoProof Lab validation chain

1. State a testable hypothesis.
2. Freeze the rules and assign a version.
3. Run a historical calculation and cost stress test.
4. Apply the rules to a later period without changes.
5. Run demo mode.
6. Start live trading at minimum size.
7. Compare expected and actual execution.
8. Publish a separate report after a sufficient period.

