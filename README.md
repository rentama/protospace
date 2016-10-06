# データベースの構築

##groupモデル >> product,user
###groupsテーブル

* name(string)

##productモデル >> image,comment,like
###productsテーブル

* title(string)
* catch_copy(string)
* concept(text)
* group_id(integer)
* user_id(integer)

##imageモデル
###imagesテーブル

* product_id(integer)
* imageのダウンロードのためのgemによるカラム

##commentモデル
###commentsテーブル

* user_id(integer)
* product_id(integer)
* text(text)

##userモデル >> product,comment,like
###usersテーブル

* name(string)
* profile(text)
* works(text)
* group_id(integer)
* deviseによるカラム諸々
* avatarを入れるのでgemによるカラム諸々

##likeモデル
###likesテーブル

* user_id(integer)
* product_id(integer)

###タグ用のテーブル(gem 'acts-as-taggable-on'によって作るテーブル)

