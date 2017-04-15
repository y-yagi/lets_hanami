### apps directory

アプリ名(下記例だと"web")配下に各種ファイルが格納される

```
apps
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
