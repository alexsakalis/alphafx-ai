# Changelog

All notable changes to AlphaFX AI are documented in this file.

## 0.2.0-alpha

### Added

- BOS Engine: confirmed-close breaks beyond an unconsumed swing high/low
- CHoCH Engine: structure breaks against tracked structural direction
- One structure-break event per confirmed swing (consumed swing state)
- Optional dashed structure lines at active swing highs and lows
- Optional BOS / CHoCH chart labels
- Dashboard Last Event row (Bullish/Bearish BOS and CHoCH)
- TradingView alert conditions for all four structure-break events

### Changed

- Indicator version bumped to 0.2.0-alpha
- Dashboard expanded to eight rows and shows v0.2

### Non-repainting

- Structure breaks require `barstate.isconfirmed` and close beyond the level
- Swings remain confirmed pivots only (`pivotLength` left/right)

## 0.1.0-alpha

### Added

- EMA Trend Engine (20 / 50 / 200)
- Confirmed swing detection with HH / HL / LH / LL labels
- Structure bias and alignment score
- Market bias dashboard
