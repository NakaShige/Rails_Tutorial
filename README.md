# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

# git の操作  

* git 利用のはじまり  

git init  

git add -A  // すべての変更を追加  

git commit -m "Message"  

* リモートリポジトリを追加して Push

git remote add origin ***.git

git push -u origin --all

* ブランチの作成

git checkout -b ***

# heroku コマンド

* heroku のバージョン確認

heroku version

* heroku へ ssh キーの追加

heroku keys:add

* heroku へのデプロイ

git push heroku master

git push heroku

* master へプッシュ

git push origin master

git push

# モデルの作成

* User クラスの作成（それぞれ string の name, email を保持）

rails generate scaffold User name:string email:string

* Micropost クラスの作成

rails generate scaffold Micropost content:text user_id:integer

* マイグレーション

rails db:migrate

* 元に戻す場合はこちら

rails db:rollback

* 最初のバージョンに戻したい場合はこちら

rails db:migrate VERSION=0

* heroku上のマイグレーション

heroku run rails db:migrate

* heroku のプロセススタート

heroku ps:scale web=1

* heroku のプロセスストップ

heroku ps:scale web=0

* controller の作成

rails generate controller StaticPages home help

* 上記を削除する場合はこちら

rails destroy controller StaticPages home help
