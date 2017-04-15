### Params

* validationも書ける

```ruby
# apps/web/controllers/signup/create.rb
module Web::Controllers::Signup
  class Create
    include Web::Action
    MEGABYTE = 1024 ** 2

    params do
      required(:name).filled(:str?)
      required(:email).filled(:str?, format?: /@/).confirmation
      required(:password).filled(:str?).confirmation
      required(:terms_of_service).filled(:bool?)
      required(:age).filled(:int?, included_in?: 18..99)
      optional(:avatar).filled(size?: 1..(MEGABYTE * 3))
    end

    def call(params)
      if params.valid?
        # ...
      else
        # ...
      end
    end
  end
end
```
