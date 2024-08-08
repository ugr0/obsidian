環境変数の優先度は以下の順になる。
1. Compose ファイル
2. シェル環境変数
3. 環境変数ファイル
4. Dockerfile
5. 変数が定義されていない

# Contents
- [[COMPOSE_FILE]]

# 参考
- [Compose 内の環境変数 — Docker-docs-ja 20.10 ドキュメント](https://docs.docker.jp/compose/environment-variables.html#:~:text=%E8%A4%87%E6%95%B0%E3%81%AE%E3%83%95%E3%82%A1%E3%82%A4%E3%83%AB%E3%81%A7%E5%90%8C%E3%81%98%E7%92%B0%E5%A2%83%E5%A4%89%E6%95%B0%E3%81%8C%E3%81%82%E3%82%8B%E5%A0%B4%E5%90%88%E3%80%81Compose%20%E3%81%AF%E4%BD%BF%E7%94%A8%E3%81%99%E3%82%8B%E5%80%A4%E3%82%92%E9%81%B8%E3%81%B6%E3%81%9F%E3%82%81%E3%80%81%E4%BB%A5%E4%B8%8B%E3%81%AE%E5%84%AA%E5%85%88%E5%BA%A6%E3%81%A7%E4%BD%BF%E3%81%84%E3%81%BE%E3%81%99%E3%80%82)
- [ファイルでデフォルトの環境変数を設定 — Docker-docs-ja 20.10 ドキュメント](https://docs.docker.jp/compose/env-file.html)
- [Compose CLI 環境変数 — Docker-docs-ja 20.10 ドキュメント](https://docs.docker.jp/compose/reference/envvars.html#compose-file)