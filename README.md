# DB設計

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|id|integer|null: false, foreign_key: true|
|email|integer|null: false, foreign_key: true|
|passwaord|integer|null: false, foreign_key: true|
|nickname|string|null: false, foreign_key: true|

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
|group|string|null: false, foreign_key: true|
|member|string|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user


## messgeテーブル

|Column|Type|Options|
|------|----|-------|
|id|integer|null: false, foreign_key: true|
|group|string|null: false, foreign_key: true|
|member|string|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user


## tagsテーブル

|Column|Type|Options|
|------|----|-------|
|id|integer|null: false, foreign_key: true|
|name|string|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user
