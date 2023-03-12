# docker-laravel-handson
https://qiita.com/ucan-lab/items/56c9dc3cf2e6762672f4

## 使用技術
- php: 8.1-fpm-buster
- composer: 2.2
- nginx: 1.20-alpine
- mysql/mysql-server: 8.0
- Laravel: 9.x

## 初期セットアップ
1. git clone git@github.com:isamuyonekawa/docker-laravel-handson.git
2. cd docker-laravel-handson
3. docker compose up -d
4. http://localhost:8080/
5. docker compose exec app bash
6. chmod -R 777 storage bootstrap/cache
7. composer install
8. cp .env.example .env
9. php artisan key:generate
10. php artisan storage:link
11. http://localhost:8080/
12. php artisan migrate

## コマンド
- コンテナ削除
docker compose down
- コンテナ状態確認
docker compose ps
- コンテナ、イメージ、ボリューム、ネットワーク、未定義コンテナ、全てを一括消去するコマンド
docker compose down --rmi all --volumes --remove-orphans