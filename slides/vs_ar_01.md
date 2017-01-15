## Sequel vs Active Record

* ARにあるよく使うであろう機能は大体揃っている
  * が、counter cacheのように無い機能もある
  * 詳細は[Sequel for ActiveRecord Users](https://github.com/jeremyevans/sequel/blob/master/doc/active_record.rdoc)参照
* 逆にDB固有の機能についてはsequelの方がサポートが厚い印象
  * viewの作成や、window関数をメソッドとして呼べる、等々
