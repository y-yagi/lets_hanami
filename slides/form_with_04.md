#### [Unification of form_for and form_tag into form_with](https://github.com/rails/rails/pull/26976)

* デフォルトで`remote: true`になっている、id属性は出力しないようになっている、等form_forと微妙にデフォルトの挙動が違う箇所があるのでちょっと注意が必要
* form_for と form_tag は緩くdeprecateになっていく予定です
