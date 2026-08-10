# AlphaFX AI

Professional Smart Money Concepts indicator for TradingView, written in Pine Script v6.

**Version:** 1.2.0  
**Status:** Professional Release

## What it is

AlphaFX AI is a modular, confirmed-structure SMC toolkit — not a simple buy/sell signal script.

It combines trend, market structure, BOS/CHoCH, order blocks, fair value gaps, liquidity, sessions, multi-timeframe confirmation, confluence confidence, and educational risk guidance.

## Core principles

- Clean engine architecture
- Confirmed pivots and closed-bar breaks
- Non-repainting policy by design
- Signal quality over signal quantity
- Maintainable, documented Pine Script

## Engines

| Engine | Purpose |
|--------|---------|
| Trend | 20 / 50 / 200 EMA state |
| Swing / Structure | Confirmed HH / HL / LH / LL |
| BOS / CHoCH | Confirmed structure breaks |
| Order Blocks | Last opposing candle before break |
| Fair Value Gaps | Confirmed 3-candle imbalances |
| Liquidity | EQH / EQL pools and sweeps |
| Sessions | Asian / London / New York ranges |
| Multi-Timeframe | Confirmed HTF trend alignment |
| Confidence | Confluence score and grade |
| Risk | Structure-based SL / TP / size model |
| Premium / Discount | Equilibrium from active swing range |
| Killzone Arming | London / NY open windows for quality gating |
| Breaker Blocks | Failed OBs flipped into opposite zones |

## Profiles

| Profile | Intent |
|---------|--------|
| Scalp | Faster structure, lower HTF (`15`), looser confidence gate |
| Intraday | Balanced defaults (recommended starting point) |
| Swing | Larger pivots, HTF `240`, stricter confluence / risk gates |
| Custom | Full manual control of tunable inputs |

## Install (TradingView)

1. Open TradingView Pine Editor
2. Paste contents of [`pine/AlphaFX_AI.pine`](pine/AlphaFX_AI.pine)
3. Save and add to chart
4. Choose a Profile, then tune visuals as needed

## Repository layout

```text
alphafx-ai/
├── pine/AlphaFX_AI.pine
├── docs/
│   ├── ARCHITECTURE.md
│   ├── FEATURES.md
│   ├── ROADMAP.md
│   ├── BACKTESTING.md
│   ├── CHANGELOG.md
│   └── RELEASE.md
├── tests/
├── assets/
├── README.md
├── LICENSE
└── VERSION
```

## Documentation

- [Architecture](docs/ARCHITECTURE.md)
- [Features](docs/FEATURES.md)
- [Roadmap](docs/ROADMAP.md)
- [Backtesting / validation](docs/BACKTESTING.md)
- [Changelog](docs/CHANGELOG.md)
- [Release notes](docs/RELEASE.md)

## Important notes

- Confidence measures confluence quality, **not** win probability.
- Risk levels are educational guidance, **not** broker execution.
- This indicator does not place trades.
- Past structure behavior does not guarantee future results.

## License

MIT — see [LICENSE](LICENSE).
