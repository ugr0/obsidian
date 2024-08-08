- GitHub Container Registry は、GitHub Packages に新たに追加された機能という位置づけ

| 従来の Packages | GitHub Container Registry |  |
| ---- | ---- | ---- |
| イメージの保存先 | リポジトリに紐づく | organization やユーザーアカウントに紐づく |
| 権限 | リポジトリの権限と同じ | イメージごとに設定できる |
| 認証なしでの public イメージの pull | 不可能 | 可能 |
| ドメイン | docker.pkg.github.com  <br>/OWNER/REPOSITORY/IMAGE_NAME | ghcr.io/OWNER/IMAGE_NAME |

- [GitHub Container Registry(ghcr.io)にDockerイメージをpushする手順 - Qiita](https://qiita.com/zembutsu/items/1effae6c39ceae3c3d0a)
- [GitHub Container Registry 入門 - 生産性向上ブログ](https://www.kaizenprogrammer.com/entry/2020/09/03/060236)
