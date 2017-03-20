#### [Change the ERB handler from Erubis to Erubi.](https://github.com/rails/rails/pull/27757)

* ERB Handlerで使用するgemがErubisから[Erubi](https://github.com/jeremyevans/erubi)に変更された
* 合わせて、Erubis Handlerはdeprecateになった。テンプレートエンジンでdeprecateメッセージが出てるとしたらおそらくこの影響。
* ほぼ機能互換はある為、ユーザが気にすることは殆ど無いはず
* Erubiの方が大分性能的に良いので、何もせずとも早くなる(かも)
