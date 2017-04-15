### Params

* ホワイトリスト処理は "params"メソッドで行う

```ruby
module Web::Controllers::Signup
  class Create
    include Web::Action

    params do
      required(:email).filled
      required(:password).filled

      required(:address).schema do
        required(:country).filled
      end
    end

    def call(params)
      puts params[:email]             # => "alice@example.org"
      puts params[:password]          # => "secret"
      puts params[:address][:country] # => "Italy"

      puts params[:admin]             # => nil
    end
  end
end
```
