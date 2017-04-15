### Layout

* Layoutもクラスで管理されているので、Layoutを追加したい場合、Layout用のクラスを追加する必要がある

```ruby
# app/web/views/login_layout.rb
module Web
  module Views
    class LoginLayout
      include Web::Layout
    end
  end
end
```
