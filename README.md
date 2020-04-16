# DB設計

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|passwaord|string|null: false|
|username|string|null: false|

### Association
- has_many :chats
- has_many :messge


## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user


## chatsテーブル

|Column|Type|Options|
|------|----|-------|
|group|string|foreign_key: true|
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
