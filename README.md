# 環境構築
本アプリは次のようにして環境構築を行います。
- 本アプリのリポジトリからURLを取得する
- 次のコマンドを実行する
```
git clone <本リポジトリのURL>
```
- クローンしたディレクトリに移動
- 次のコマンドを実行してコンテナを起動する
```
docker-compose up -d
```
- 以下のコマンドでwebコンテナ内に入り、DB作成
```
docker-compose exec web bash
rails db:create
rails db:migrate
exit
```

- コンテナを再起動させる
```
docker-compose up
```

- ブラウザでlocalhost:3000にアクセスする
- アプリを終了したい場合はCtr+Cを押す