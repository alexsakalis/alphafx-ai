# EURUSD Validation Checklist

**Version under test:** 1.0.0  
**Suggested timeframes:** 5m, 15m, 1H  
**Timezone for sessions:** America/New_York

## Compile

- [ ] Script compiles in Pine Editor with no errors

## Structure / BOS / CHoCH

- [ ] HH/HL/LH/LL labels appear only after pivot confirmation delay
- [ ] BOS prints on candle close beyond swing, once per swing
- [ ] CHoCH prints when break opposes structural direction

## OB / FVG / Liquidity

- [ ] Bullish OB forms after bullish BOS/CHoCH
- [ ] FVG boxes appear on confirmed 3-candle gaps
- [ ] EQH/EQL form on near-equal swings
- [ ] Sweep requires wick beyond + reclaim close

## Sessions / MTF

- [ ] Asian/London/NY boxes track expected windows
- [ ] HTF trend changes only after HTF close

## Confidence / Risk

- [ ] Confidence rises with aligned confluence
- [ ] Risk shows WAIT below confidence threshold
- [ ] Valid LONG/SHORT model places SL beyond swing

## Notes

_Tester / date / issues:_
