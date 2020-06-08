# DB設計

## usersテーブル
|Column|Type|Options|
|------|----|-------|
|nickname|string|null: false|
|adress|integer|unique|
|password|integer|precision: 10, scale: 5|

### Association
- has_many :messages
- has_many :groups

## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|body|text|------|
|image|string|-----|
|group_id|integer|-----|
|user_id|ineger|------|

### Association
- belongs_to :user
- belongs_to :group

## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|-----|

### Association
- belongs_to :user
- has_many :messages

## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer	|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user