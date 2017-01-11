## 性能測定(SQLite)

```
Warming up --------------------------------------
           ar_insert     1.000  i/100ms
       sequle_insert     1.000  i/100ms
Calculating -------------------------------------
           ar_insert     12.216  (± 8.2%) i/s -     61.000  in   5.019179s
       sequle_insert     12.159  (± 8.2%) i/s -     61.000  in   5.082690s

Comparison:
           ar_insert:       12.2 i/s
       sequle_insert:       12.2 i/s - same-ish: difference falls within error

Warming up --------------------------------------
           ar_select    62.000  i/100ms
       sequel_select   150.000  i/100ms
Calculating -------------------------------------
           ar_select    630.595  (± 1.6%) i/s -      3.162k in   5.015577s
       sequel_select      1.463k (± 7.7%) i/s -      7.350k in   5.064096s

Comparison:
       sequel_select:     1462.6 i/s
           ar_select:      630.6 i/s - 2.32x  slower
```
