### [ActiveSupport.to_time_preserves_timezone](https://github.com/rails/rails/commit/c9c5788a527b70d7f983e2b4b47e3afd863d9f48)

* Ruby 2.4でDateTimeクラスとTimeクラスのto_timeメソッドを呼びだした際、元のオブジェクトのタイムゾーンを保持するようになりました
* これはバグ修正なのですが、既存の挙動と変わってしまう為、Rubyのバージョンアップ時に挙動が変わってしまいます
* そこでRailsはto_timeをラップし、configの値によりto_timeの挙動を変える、という対応を行っています
* ActiveSupport.to_time_preserves_timezoneがtrueの場合はRuby 2.4以降の挙動、falseの場合は2.3までの挙動を行うようになっています
