#### [Add :skip_pipeline option to several asset tag helpers](https://github.com/rails/rails/pull/26226)

```ruby
asset_path("application.js")
# => "/assets/application-85e543ffb6766161629d4b7a5dd540252230a0f0e5287de6701be45c52d107de.js"

asset_path("application.js", skip_pipeline: true)
# => "/application.js"
```
