# Backtesting & Validation

AlphaFX AI is an **overlay indicator**, not a strategy script. TradingView Strategy Tester PnL is not the primary validation path.

## Validation approach

Use visual + alert validation on historical charts:

1. Confirm pivots only print after right-side confirmation.
2. Confirm BOS/CHoCH appear on candle close, not mid-bar.
3. Confirm OBs/FVGs do not jump using future bars.
4. Confirm HTF trend changes only after HTF bar close.
5. Confirm risk levels update on confirmed bars only.

## Recommended matrices

| Symbol | Timeframes | Focus |
|--------|------------|-------|
| EURUSD | 5m, 15m, 1H | Sessions, EQH/EQL, BOS |
| GBPUSD | 15m, 1H | London killzone confluence |
| XAUUSD | 15m, 1H, 4H | OB/FVG density, volatility stops |
| NAS100 | 5m, 15m, 1H | Trend + MTF alignment |

Detailed checklists live in:

- [`tests/EURUSD.md`](../tests/EURUSD.md)
- [`tests/GBPUSD.md`](../tests/GBPUSD.md)
- [`tests/XAUUSD.md`](../tests/XAUUSD.md)
- [`tests/NAS100.md`](../tests/NAS100.md)

## Pass criteria for 1.0.0

- [ ] Compiles cleanly on TradingView Pine v6
- [ ] No intentional repaint observed in spot checks
- [ ] Dashboard values match visible engine state
- [ ] Alerts fire once per intended transition
- [ ] Risk model shows WAIT when confidence is weak
- [ ] Drawing limits do not crash common settings

## What not to claim

Do not present confluence confidence or risk RR as historical expectancy or guaranteed edge without a separate, controlled strategy study.
