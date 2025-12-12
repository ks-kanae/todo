# laravel-docker-template

# Todoアプリ
```
こちらのアプリは、タスク管理が簡単にできるアプリです。タスクをTodoとして任意の名前で作成でき、作成したTodo名の更新や削除が簡単にできます。
環境構築の詳細を以下に記載しております。
尚、Docker環境を使用しております。
```

## 環境構築

#### リポジトリをクローン

```
cd (保存したいディレクトリを指定)

git clone git@github.com:ks-kanae/todo.git

```

#### Laravelのビルド

```
cd todo

docker-compose up -d --build

code .

```

#### Laravel パッケージのダウンロード

```
docker-compose exec php bash
```

```
composer install
```

#### .env ファイルの作成

```
cp .env.example .env
```

#### .env ファイルの修正

```
DB_CONNECTION=mysql
- DB_HOST=127.0.0.1
+ DB_HOST=mysql
DB_PORT=3306
- DB_DATABASE=laravel
- DB_USERNAME=root
- DB_PASSWORD=
+ DB_DATABASE=laravel_db
+ DB_USERNAME=laravel_user
+ DB_PASSWORD=laravel_pass
```

#### キー生成

```
php artisan key:generate
```

#### マイグレーション・シーディングを実行

```
php artisan migrate
```

## 使用技術（実行環境）

フレームワーク：Laravel

言語：php:8.1-fpm

Webサーバー：Nginx 1.21.1

データベース：MySQL 8.0.36

## ER図

![ER図](xxxx.drawio.png)

## URL

アプリケーション：http://localhost

管理画面：◯◯◯◯◯ ◯◯◯◯ ◯◯◯◯

phpMyAdmin：http://localhost:8080
