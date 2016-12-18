### [round to even](https://github.com/rails/rails/commit/a3478f1685a507874c710c8461cbfd6be84d95c0)

* Kernel#sprintf や String#% で、%f指定の精度に丸める時に、ちょうど半分の時に丸める方向を、その上の桁が偶数になるように丸めるように変更になっており、その影響の対応

```ruby
# 2.3
sprintf('%0.1f', 5.55)  #=> "5.5"

# 2.4
sprintf('%0.1f', 5.55)  #=> "5.6"
```

* テストの修正だけ
