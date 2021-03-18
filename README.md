# テーブル設計

## usersテーブル

| Column   | Type   | Options     |
| -------- | ------ | ----------- |
| name     | string | null: false |
| email    | string | null: false |
| password | string | null: false |

## postsテーブル
| Column   | Type       | Options                          |
| -------- | -----------| -------------------------------- |
| title    | string     | null: false                      |
| content  | text       | null: false                      |
| user     | references | null: false, foreign_key: true   |

## messagesテーブル
| Column   | Type       | Options                          |
| -------- | -----------| -------------------------------- |
| title    | string     | null: false                      |
| content  | text       | null: false                      |
| user     | references | null: false, foreign_key: true   |
| post     | references | null: false, foreign_key: true   |