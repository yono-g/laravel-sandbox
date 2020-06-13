# Laravel sandbox

## 概要

+ Nginx 1.18
+ Postgresql 12.3
+ PHP 7.4
    - Laravel 7.x

## 開発環境構築手順

```sh
git clone REPOSITORY_URL
cd /path/to/laravel-sandbox
cp .env.example .env
./composer.sh install
docker-compose up -d

docker-compose exec app php artisan key:generate
docker-compose exec --user postgres db createdb sandbox
docker-compose exec app php artisan migrate

open localhost
```

## コンテナの使用例

```sh
# composerを使ってパッケージをインストールする:
./composer.sh require PACKAGE_NAME

# artisanコマンドを使ってtinkerを起動する:
docker-compose exec app php artisan tinker
```
