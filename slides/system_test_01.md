### [System tests](https://github.com/rails/rails/pull/26703)

* ブラウザを使用してテストを行う為の仕組み
* ActionDispatch::SystemTestCase というクラスが提供されおり、このクラスでは Capybara::DSL がincludeされており、Capybaraのメソッドが使える状態になっている
  * 一時別gemにするか、というような話もあったが、最終的にAction Pack配下に含まれた
