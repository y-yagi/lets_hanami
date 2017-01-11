## Associations

* Associationsも使える。メソッド名はARと異なる。

|Active Record|Sequel|
|----|---|
|belongs_to|many_to_one|
|has_one|one_to_one|
|has_many|one_to_many|
|has_and_belongs_to_many|many_to_many|

* 他にもhas_many :through相当のmany_through_many等がある(pluginで提供)
