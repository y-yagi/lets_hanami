## 性能測定(PostgreSQL)

```
Warming up --------------------------------------
           ar_insert     6.000  i/100ms
       sequle_insert     6.000  i/100ms
Calculating -------------------------------------
           ar_insert     63.033  (± 4.8%) i/s -    318.000  in   5.060691s
       sequle_insert     67.586  (± 4.4%) i/s -    342.000  in   5.071939s

Comparison:
       sequle_insert:       67.6 i/s
           ar_insert:       63.0 i/s - same-ish: difference falls within error

Warming up --------------------------------------
           ar_select    22.000  i/100ms
       sequel_select   119.000  i/100ms
Calculating -------------------------------------
           ar_select    222.513  (± 3.6%) i/s -      1.122k in   5.049322s
       sequel_select      1.033k (±22.0%) i/s -      4.998k in   5.122542s

Comparison:
       sequel_select:     1033.0 i/s
           ar_select:      222.5 i/s - 4.64x  slower
```
