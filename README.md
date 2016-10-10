#データベースの構築

##テーブル

* products
* images
* comments
* users
* likes
* protoytpes_tags

##アソシエーション

* productモデル

+ has_many :images
+ has_many :comments
+ has_many :likes
+ balongs_to :user

* imageモデル

+ belongs_to :product

* commentモデル

+ belongs_to :user
+ belongs_to :product

* userモデル

+ has_many :products
+ has_many :comments
+ has_many :likes

* likesモデル

+ balongs_to :user
+ belongs_to :product

##テーブルのカラム(カラム)

###productsテーブル

* title(string)
* catch_copy(string)
* concept(text)
* user_id(integer)

###imagesテーブル

* product_id(integer)
* role(string)
* imageのダウンロードのためのgemによるカラム

###commentsテーブル

* user_id(integer)
* product_id(integer)
* text(text)

###usersテーブル

* name(string)
* profile(text)
* works(text)
* group(string)
* deviseによるカラム諸々
* avatarを入れるのでgemによるカラム諸々

###likesテーブル

* user_id(integer)
* product_id(integer)

###protoytpes_tags

