### CDN

configにCDNの設定を書くことが出来る

```ruby
# apps/web/application.rb

assets do
  # ...
  fingerprint true

  # CDN settings
  scheme 'https'
  host   '123.cloudfront.net'
  port   443
end
```

```erb
<%= stylesheet 'application' %>
# => <link href="https://123.cloudfront.net/assets/application-9ab4d1f57027f0d40738ab8ab70aba86.css" type="text/css" rel="stylesheet">
```
