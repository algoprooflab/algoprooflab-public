# Calculation methodology

[Русская версия](METHODOLOGY_RU.md)

## Data

The study uses resolved Bitcoin Up/Down 5m markets and the observed price of the selected outcome around the modeled entry time.

## Costs

The base calculation:

- adds 0.005 to the observed price as a slippage allowance;
- applies the fee model `0.07 × (1 − price)`;
- uses the same fixed 1 USDC stake for every row;
- skips an entry when the price exceeds 0.52.

The stress test doubles the slippage allowance.

## Period split

The result is not shown only as one total. The study period is split into two consecutive monthly blocks. Both blocks had to remain positive before the strategy could receive `ACTIVE` status.

## Limitations

Historical prices do not guarantee execution. Live trading may differ because of order-book movement, partial fills, fee changes, VPS or API delays, market outages and data-source differences.

The recommended sequence is demo mode, minimum live stake and a buyer-controlled execution journal.
