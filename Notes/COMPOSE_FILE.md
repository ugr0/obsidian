# COMPOSE_FILEの挙動

```bash
COMPOSE_FILE=docker-compose.yml:docker-compose.prod.yml
```

みたいなのを書くと、両方の設定が適用となる。競合したところは古い方が優先される。

# 参考
- [Compose 設定をファイルとプロジェクト間で共有 — Docker-docs-ja 20.10 ドキュメント](https://docs.docker.jp/compose/extends.html)
- [docker-compose.ymlが環境別に複数ある場合はCOMPOSE_FILEを定義しておくと幸せになれる](https://suin.io/535)