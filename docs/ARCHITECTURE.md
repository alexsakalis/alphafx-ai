# Architecture

AlphaFX AI is built as a dependency-ordered engine pipeline in a single Pine Script v6 file.

## Pipeline

```text
Inputs
  → Trend Engine
  → Swing Engine
  → Structure Engine
  → BOS Engine
  → CHoCH Engine
  → Order Block Engine
  → Fair Value Gap Engine
  → Liquidity Engine
  → Session Engine
  → Multi-Timeframe Engine
  → Confidence Engine
  → Risk Engine
  → Dashboard
  → Alerts
```

Later engines consume state from earlier engines. Dependencies are never skipped.

## Design rules

1. **Confirmed structure only** — pivots use equal left/right length.
2. **Closed-bar breaks** — BOS/CHoCH and many lifecycle events require `barstate.isconfirmed`.
3. **One event per swing/pool** where applicable — consumed flags prevent duplicates.
4. **HTF safety** — `request.security(..., series[1], lookahead_off)`.
5. **No future-looking data** — if a feature would repaint, it must be justified before implementation.
6. **Quality over quantity** — features must improve understanding or confluence quality.

## State ownership

| State | Owner |
|-------|--------|
| `trendState` | Trend Engine |
| Swing highs/lows + labels | Swing / Structure |
| `structuralDirection`, `lastEvent` | BOS / CHoCH |
| OB arrays | Order Block Engine |
| FVG arrays | Fair Value Gap Engine |
| EQH/EQL pools | Liquidity Engine |
| Session ranges | Session Engine |
| `htfTrendState`, MTF align | Multi-Timeframe Engine |
| `confidenceScore` / direction | Confidence Engine |
| SL / TP / size model | Risk Engine |

## Drawing limits

Configured for production density:

- `max_labels_count = 500`
- `max_lines_count = 350`
- `max_boxes_count = 300`

## Future modularization

`pine/modules/` is reserved for optional extraction of engines into includes/modules if TradingView workflow and team process justify splitting the monolithic script.
