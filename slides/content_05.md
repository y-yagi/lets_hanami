### [Array#sum](https://github.com/rails/rails/commit/7ad4690b2149fbb23faa179c21698b92ff383c73)

* Ruby 2.4でArray#sumが追加されました
* しかし、Railsには太古の昔よりArray#sumが存在しており、かつ、Ruby本体に追加されたArray#sumはRailsのArray#sumと挙動が違いました
  * RailsのArray#sumはNumeric以外のClassに対してもsum出来る
* そのため、Rails(というかActive Support)を利用している場合、引き続きRailsのArray#sumがよばれるようになっています
