# XAUUSD Validation Checklist

**Version under test:** 1.0.0  
**Suggested timeframes:** 15m, 1H, 4H  
**Focus:** Volatility, OB/FVG density, ATR stops

## Compile

- [ ] Script compiles in Pine Editor with no errors

## Volatility behavior

- [ ] ATR-based FVG filter can reduce tiny gaps when raised
- [ ] Liquidity tolerance still finds meaningful EQH/EQL
- [ ] Risk ATR buffer keeps stops outside noisy wicks

## Drawing load

- [ ] Max OB/FVG/session settings do not freeze chart
- [ ] Oldest boxes/lines trim as configured

## Structure / confluence

- [ ] Displacement moves create clear OBs and FVGs
- [ ] Confidence does not stay artificially maxed in chop
- [ ] MTF conflict penalty visibly lowers confidence

## Notes

_Tester / date / issues:_
