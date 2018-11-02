# README

## RailsのDocker環境です

* Ruby version: 2.5
* Rails version: 5.1

## Dockerコマンド

※ 新規でrailsプロジェクトを作成するときは以下のコマンドを叩いてください
* docker-compose run web rails new . --force --database=mysql

* Railsイメージをビルドする
$ docker-compose build

# config/database.ymlのdefault内にある以下の項目を修正内容
password: password
host: db

# コンテナを実行するコマンド
※ -dオプションでデタッチで実行します
$ docker-compose up -d

# dbを作成するをコマンド
$ docker-compose run web bundle exec rake db:create