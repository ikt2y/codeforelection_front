## Code for 選挙プロジェクトへようこそ

Code for 選挙プロジェクトは、2017年衆議院選挙候補者のオープンなデータベースを作り、候補者の政策及び過去の実績を中立的に参照できるサイトを制作することを目的としています。

## プロジェクトについて

[こちらの Github リポジトリ](https://github.com/codeforjapan/codeforelection)を参照下さい。

## インストール方法

dockerのインストールすると簡単にセットアップすることが可能です。

```bash
docker-compose build
docker-compose up -d db
docker-compose run --rm app bundle exec rails db:setup
docker-compose up
```


候補者データのインポートは、docker-compose upでサーバを立ち上げた状態で、下記のコマンドを実行することで可能です。

```bash
docker-compose exec app bundle exec rake graydb:import
```

その後、ブラウザから http://localhost:3000 にアクセスして下さい。
