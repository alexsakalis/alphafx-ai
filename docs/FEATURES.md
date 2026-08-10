# Features

## Premium / Discount

- Equilibrium = midpoint of active confirmed swing high / low
- Premium / Discount / Equilibrium band classification
- Optional equilibrium line and background shade
- Optional risk gate: longs only in discount, shorts only in premium

## Killzone Arming

- Configurable London Open and New York Open windows
- Arms confidence quality bonus only while killzone is active
- Optional requirement for Risk model readiness

## Breaker Blocks

- Created when an order block is invalidated by confirmed close-through
- Direction flips (failed bullish OB → bearish breaker)
- Mitigation / fill lifecycle with alerts

## Profile Presets

- **Scalp** — tighter pivots, more reactive zones, HTF `15`
- **Intraday** — balanced defaults, HTF `60`
- **Swing** — larger pivots, stricter FVG/risk gates, HTF `240`
- **Custom** — uses manual inputs for all tunable parameters

Visual toggles (labels, boxes, lines, dashboard) stay user-controlled in every profile.

## Trend Engine

- Fast / medium / slow EMA stack (default 20 / 50 / 200)
- Optional price filter against slow EMA
- Bullish / bearish / neutral trend state
- Optional trend background

## Market Structure

- Confirmed pivot highs / lows
- HH / HL / LH / LL / EH / EL classification
- Structure bias from latest high/low pair

## BOS / CHoCH

- Break only on confirmed close beyond unconsumed swing
- One break event per swing
- BOS with structure, CHoCH against structure
- Optional structure lines and event labels
- Alert conditions for all four events

## Order Blocks

- Bullish OB = last bearish candle before bullish BOS/CHoCH
- Bearish OB = last bullish candle before bearish BOS/CHoCH
- Mitigation and invalidation lifecycle
- Configurable lookback and max active OBs

## Fair Value Gaps

- Confirmed 3-candle imbalance detection
- Optional ATR size filter
- Optional structure-alignment filter
- Mitigation and full-fill lifecycle

## Liquidity

- Equal highs (EQH) and equal lows (EQL)
- ATR tolerance matching
- Sweep = wick beyond level + reclaim close
- One sweep per pool

## Sessions

- Asian / London / New York session tracking
- Configurable timezone and session windows
- Confirmed range updates; lock on session end
- Session high / low break alerts

## Multi-Timeframe

- Confirmed HTF EMA trend
- Chart vs HTF alignment / conflict states
- Structure-to-HTF alignment labels

## Confidence Engine

- Weighted confluence score (0–100)
- Grades: LOW / MEDIUM / HIGH / VERY HIGH
- Directional bullish / bearish confidence
- Explicitly not a win-rate forecast

## Risk Engine

- Direction gated by confidence
- Stop beyond confirmed swing ± ATR buffer
- TP1 / TP2 from reward:risk multiples
- Suggested size from equity and risk percent
- Educational model only

## Dashboard & Alerts

- Live status table for all major engines
- TradingView `alertcondition` coverage for structure, OB, FVG, liquidity, sessions, MTF, confidence, and risk
