# DB設計

## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|password|string|null: false|
|username|string|null: false|
### Association
- has_many :groups
- has_many :messeges

## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## messegesテーブル
|Column|Type|Options|
|------|----|-------|
|body|text|null: false|
|image|string|null: false|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
- has_many :users_tags
- has_many  :tags,  through:  :users_tags

## tagsテーブル
|Column|Type|Options|
|------|----|-------|
|username|string|null: false|
### Association
- has_many :users_tags
- has_many  :users,  through:  :users_tags

## users_tagsテーブル
|Column|Type|Options|
|------|----|-------|
|messeges_id|integer|null: false, foreign_key: true|
|tag_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :user
- belongs_to :tag

