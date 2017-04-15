### Assets

```
# apps/web/application.rb
...
configure do
  # ...
  assets do
  end
end

configure :production do
  assets do
    fingerprint true
  end
end
...
```

```erb
<%= javascript 'application' %>
# => <script src="/assets/application-d1829dc353b734e3adc24855693b70f9.js" type="text/javascript"></script>

<%= stylesheet 'application' %>
# => <link href="/assets/application-d1829dc353b734e3adc24855693b70f9.css" type="text/css" rel="stylesheet">
```
