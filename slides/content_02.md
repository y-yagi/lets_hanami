### [strict checking on key length](https://github.com/rails/rails/commit/8ee269cf51c58b0600a3fa536219637f240e888d)

* Railsのverification/signingはデフォルトではaes-256-cbcが使われている為、key sizeも本来32byteであるべきだったのですが、64byteになってしまっていました
* ただ、Ruby 2.3までは要求されるよう大きいkey sizeを指定しても問題無かった(Ruby内部で切り捨てていた)のですが、Ruby 2.4ではkey sizeを厳密に見るようになり、必要なkey sizeより大きい値を指定するとエラーになるようになった為、key sizeを調整しています
* これの影響でそもそもrails serverが動かなかった
