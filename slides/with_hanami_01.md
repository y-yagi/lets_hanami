## With Rails

* [sequel\-rails](https://github.com/TalentBox/sequel-rails)というRailsでsequelを使うためのgemがある
  * ARだけloadしないようにして、他のcomponentはそのまま使用出来る(はず)
* sequelにはActiveModel pluginというSequel::ModelクラスのオブジェクトをActiveModel::Lintのテストをとおす為のpluginがある
  * これを使えばAR同様に、Sequel::Modelのオブジェクトをform_forに渡す等は出来る
  * [sequel/active\_model](https://github.com/jeremyevans/sequel/blob/master/lib/sequel/plugins/active_model.rb)
