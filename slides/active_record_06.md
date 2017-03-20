#### [Deprecate the behavior of AR::Dirty inside of after\_\(create\|update\|save\) callbacks](https://github.com/rails/rails/pull/25337)

* 現状のAPIとは別に、明示的に変更したattributesや、DBに保存されている値を取得するようのAPIが準備されるので、そちらを使う必要があります
  * 追加されたAPIについて、名前は変えるかもーという話もあったのですが、一旦今の状態でfix(のはず)
  * が、これらのAPIをpublic APIにするかどうかはまだ決まってなかった
  * https://github.com/rails/rails/pull/28472
