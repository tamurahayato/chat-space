# DB設計

## usersテーブル
|Column|Type|Options|
|------|----|-------|
|nickname|string|null: false|
|adress|integer|unique|
|password|integer|precision: 10, scale: 5|

### Association
- belongs_to :user