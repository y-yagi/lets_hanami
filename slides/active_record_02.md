#### [adds support for limits in batch processing](https://github.com/rails/rails/commit/451437c6f57e66cc7586ec966e530493927098c7)

* batch処理用のメソッド(#find_in_batches、in_batches)でlimitが使えるようになった

```ruby
Post.limit(10_000).find_each do |post|
  # ...
end
```

* batch_sizeオプションも引き続き使用出来る

