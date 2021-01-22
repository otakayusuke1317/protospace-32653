# テーブル設計

## users テーブル

| Column     | Type   | Options     |
| ---------- | ------ | ----------- |
| email      | string | not nill    |
| password   | string | not nill    |
| name       | string | not null    |
| profile    | text   | not null    |
| occupation | text   | not nill    |
| position   | text   | not nill    |

### Association

- has_many :users_prototypes
- has_many :users, through: usee_comments

##  prototypesテーブル

| Column       | Type       | Options  |
| -------------| ---------- | ---------|
| title        | string     | not null |
| catch_copy   | text       | not null |
| concept      | text       | not null |
| image        |
| user         | references 

### Association

- has_many :users_comments
- has_many :users, through: comments

##  commentsテーブル

| Column     | Type   | Options     |
| ---------- | ------ | ----------- |
| text       | text   | not null    |
| user       | references
| prototype  | references

### Association

- belongs_to :users
- belongs_to :prototypes