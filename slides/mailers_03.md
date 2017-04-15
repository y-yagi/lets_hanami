### Mailers

```ruby
class Mailers::Welcome
  include Hanami::Mailer

  from    'noreply@bookshelf.org'
  to      'user@example.com'
  subject 'Welcome to Bookshelf'
end

```

```
Mailers::Welcome.deliver

Mailers::Welcome.deliver(format: :html)
Mailers::Welcome.deliver(format: :txt)
```
