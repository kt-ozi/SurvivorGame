# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:


## usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|age|string|null: false|
|gender|string|null: false|
|email|string|null: false, unique: true|
|password|string|null: false|

### Association
- has_many :resurves
- has_many :demands
- has_many :messages

## itemsテーブル

|Column|Type|Options|
|------|----|-------|
|itemname|string|null: false|

### Association
- has_many :resurves
- has_many :demands

## messagesテーブル

|Column|Type|Options|
|------|----|-------|
|content|string|null: false|
|user_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user

## resurvesテーブル

|Column|Type|Options|
|------|----|-------|
|date|string|null: false|
|user_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
- has_many :histories

## demandsテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|item_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
- belongs_to :item
- has_many :histories

## historiesテーブル

|Column|Type|Options|
|------|----|-------|
|resurves_id|integer|null: false, foreign_key: true|
|demands_id|integer|foreign_key: true|

### Association
- belongs_to :resurve
- belongs_to :demand


* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
