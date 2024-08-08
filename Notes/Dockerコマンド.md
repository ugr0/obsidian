# コンテナの作成・起動

```
$ docker-compose up -d
// 初回のimgae構築時は時間がかかる（5〜10分）
// バックグラウンドで起動する場合は-dオプション
// うまくいかない時はまずdocker for macの「Restart Docker」(dockerの再起動)を行う
```

# キャッシュを使用しせずにimageをbuild

```
$ docker-compose build --no-cache
```

# ログを見る場合（バックグラウンドでコンテナを起動している場合）

```
$ docker-compose logs
```

# binding.pryを使える状態でサーバーを起動

```
$ docker-compose up -d
// バックグラウンドで起動

$ docker-compose ps
// Railsが動いているコンテナのIDもしくはコンテナ名を調べる

$ docker attach コンテナのIDもしくはコンテナ名_1
// コマンド実行後は何も起こらないがアクセスするとログが流れてくるようになる
// attachすると、binding.pryが記述している場所に来るとデバッグモードが起動する
```

# ローカルからコンテナに対してコマンドを実行する

```
$ docker-compose run {サービス名(コンテナ)} {実行したいコマンド}
// コンテナを新しく作って実行するコマンド
// runの後ろに--rmをつけるとコンテナを停止した段階でコマンド実行プロセスを削除するような挙動も可能 
 
$ docker-compose exec {サービス名(コンテナ)} {実行したいコマンド}
// 起動しているコンテナに対して実行するコマンド（新しくコンテナを作りなおさず実行）   
```

# webコンテナの中に入る

```
$ docker-compose exec web /bin/bash
// dbコンテナに入る場合はwebをdbに変更
```

# コンテナを停止

```
Ctrl+C
```

or

```
$ docker-compose stop
```

# コンテナとネットワークを停止+削除

```
$ docker-compose down
```

# コンテナとネットワークに加えてvolumeも削除

```
docker-compose down -v
```

# dcoker上に存在する全てのdocker imageを削除する

```
$ docker rmi $(docker images -q)

// docker imagesコマンドはローカルのホスト上にあるイメージの一覧を表示するコマンド。
```

# そのプロジェクトのdocker imageを全削除する

```
$ docker-compose down --rmi all
```

# そのプロジェクトのイメージもvolumeも全削除

```
docker-compose down --rmi all -v
```

# 起動中のコンテナの一覧を見る

```
$ docker-compose ps
```

# ユーザが作成した全てのネットワークを一覧表示

```
$ docker network ls

// Docker エンジンの daemon が把握している全てのネットワーク一覧を表示
```

# ネットワークの情報を表示

```
$ docker network inspect [オプション] ネットワーク [ネットワーク..]
```

コンテナのIDを指定することでコンテナのIPアドレスや所属するネットワークのIPアドレスも見れる

```
$ docker container ls
$ docker container inspect {containerのID}
```

# マウントの確認

```
$ docker inspect $(docker-compose ps -q <コンテナ名>)
```

# imageの一覧を確認

```
$ docker images
```

# 未使用のvolumeを一括削除

```
$ docker volume prune
```

# 未使用のimageを一括削除

```
$ docker image prune
```

# 未使用のcontainerを一括削除

```
$ docker container prune
```

# 未使用のnetworkを一括削除

```
$ docker network prune
```

# 参考資料
- [Docker CLI (docker) — Docker-docs-ja 20.10 ドキュメント](https://docs.docker.jp/engine/reference/commandline/toc.html)
- [Dockerでのローカル開発環境構築の入門 - Qiita](https://qiita.com/Dai_Kentaro/items/de26054e8cf1e019a667)