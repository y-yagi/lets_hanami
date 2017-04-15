### directory

"bookshelf" というプロジェクトがあった場合、ルートディレクトリ配下は下記のような構成になる

```
tree -L 2
.
├── Gemfile
├── Gemfile.lock
├── Rakefile
├── apps
│   └── web
├── config
│   ├── boot.rb
│   ├── environment.rb
│   └── initializers
├── config.ru
├── db
│   ├── migrations
│   └── schema.sql
├── lib
│   ├── bookshelf
│   └── bookshelf.rb
├── public
│   └── assets
└── spec
    ├── bookshelf
    ├── features_helper.rb
    ├── spec_helper.rb
    ├── support
    └── web
```
