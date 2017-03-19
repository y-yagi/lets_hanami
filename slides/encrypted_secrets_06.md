### [Encrypted secrets](https://github.com/rails/rails/pull/28038)

* 暗号化方式にはaes-128-gcm が使われている
* Rails 5.1.beta1リリース後に変更されているので、もしRails 5.1.beta1時点で既に使用していた場合、対応が必要
  * Ref: https://gist.github.com/kaspth/bc37989c2f39a5642112f28b1d93f343
