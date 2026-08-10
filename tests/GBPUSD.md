# GBPUSD Validation Checklist

**Version under test:** 1.0.0  
**Suggested timeframes:** 15m, 1H  
**Focus:** London session confluence

## Compile

- [ ] Script compiles in Pine Editor with no errors

## London session

- [ ] London box starts/ends at configured session times
- [ ] London Complete event locks high/low
- [ ] London high/low break alerts fire on confirmed closes only

## Structure quality

- [ ] During London, BOS/CHoCH remain non-repainting
- [ ] EQH/EQL around London highs/lows behave as expected
- [ ] MTF align useful vs 1H/4H higher timeframe

## Confidence / Risk

- [ ] Killzone session contributes when trend/structure is directional
- [ ] Risk model SL distance reasonable in GBP volatility

## Notes

_Tester / date / issues:_
