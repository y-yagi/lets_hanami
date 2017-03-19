### [Optional Webpack support](https://github.com/rails/rails/pull/27288)

* rails newコマンドにwebpackオプションを指定すると、[webpacker](https://github.com/rails/webpacker)をGemfileに追加、及び、webpackerのinstall task(webpacker:install)が実行されるようになっている
* 引数にwebpackerがサポートしているJSのライブラリを指定可能

```ruby
rails new myapp --webpack=react
```
* この場合、上記ライブラリ用のinstall task(e.g. webpacker:install:react)も合わせて実行される
