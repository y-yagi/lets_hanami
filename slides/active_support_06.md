#### [Add ActiveSupport::Duration#before, #after](https://github.com/rails/rails/pull/27721)

* ActiveSupport::Duration#before, #after メソッドを追加
  * 中身は #until, #sinceのalias

```ruby
2.weeks.since(customer_start_date)
5.days.until(today)

# どちらも同じ

2.weeks.after(customer_start_date)
5.days.before(today)
```
