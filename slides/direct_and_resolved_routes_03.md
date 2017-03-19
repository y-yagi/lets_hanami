### [Direct & resolved routes](https://github.com/rails/rails/pull/23138)

**direct**

```ruby
homepage_path
# => "http://www.rubyonrails.org"

commentable_path(@user)
# => "/users/2#1"

main_path
# => "/page/index"

browse_path
# => "/products?page=1&size=10"
```
