### directory

"admin"用のUIを追加した場合は下記のようになる

```
apps
├── admin
│   ├── application.rb
│   ├── assets
│   │   ├── favicon.ico
│   │   ├── images
│   │   ├── javascripts
│   │   └── stylesheets
│   ├── config
│   │   └── routes.rb
│   ├── controllers
│   ├── templates
│   │   └── application.html.erb
│   └── views
│       └── application_layout.rb
└── web
    ├── application.rb
    ├── assets
    │   ├── favicon.ico
    │   ├── images
    │   ├── javascripts
    │   └── stylesheets
    ├── config
    │   └── routes.rb
    ├── controllers
    │   ├── books
    │   │   ├── create.rb
    │   │   ├── index.rb
    │   │   └── new.rb
    │   └── home
    │       └── index.rb
    ├── templates
    │   ├── application.html.erb
    │   ├── books
    │   │   ├── create.html.erb
    │   │   ├── index.html.erb
    │   │   └── new.html.erb
    │   └── home
    │       └── index.html.erb
    └── views
        ├── application_layout.rb
        ├── books
        │   ├── create.rb
        │   ├── index.rb
        │   └── new.rb
        └── home
            └── index.rb
```
