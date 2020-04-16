# DB設計

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|id|integer|null: false, foreign_key: true|
|email|integer|null: false, foreign_key: true|
|passwaord|integer|null: false, foreign_key: true|
|nickname|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## chatテーブル

|Column|Type|Options|
|------|----|-------|
|id|integer|null: false, foreign_key: true|
|group|integer|null: false, foreign_key: true|
|member|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## messgeテーブル

|Column|Type|Options|
|------|----|-------|
|id|integer|null: false, foreign_key: true|
|group|integer|null: false, foreign_key: true|
|member|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## tagsテーブル

|Column|Type|Options|
|------|----|-------|
|id|integer|null: false, foreign_key: true|
|name|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user
