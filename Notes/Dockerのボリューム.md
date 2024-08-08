ボリュームとは、Docker コンテナーにおいて生成され利用されるデータを、永続的に保持する目的で利用される仕組みです。 [バインドマウント](https://matsuand.github.io/docs.docker.jp.onthefly/storage/bind-mounts/) はホストマシン OS のディレクトリ構造に依存しますが、ボリュームは完全に Docker によって管理されます。 ボリュームにはバインド[[マウント]]に比べて、以下のように優れた点があります。

-   ボリュームはバインドマウントよりも、バックアップや移行が容易です。
-   ボリュームは Docker CLI コマンドや Docker API を利用して管理することができます。
-   ボリュームは Linux と Windows 上のコンテナーにおいて動作します。
-   ボリュームは複数コンテナー間にて安全に共有できます。
-   ボリュームドライバーを用いると、リモートホスト上、あるいはクラウドプロバイダー上のボリュームに保存できるようになります。保存の際にはボリューム内データを暗号化することができ、その他にも種々の機能を利用することができます。
-   ボリュームを新たに生成すると、その内容はコンテナーがあらかじめ用意していた内容になります。
-   Docker Desktop 上のボリュームは、Mac や Windows ホストからのバインドマウントに比べて、より高い性能を実現します。

# 参考資料
- [ボリュームの利用 | Docker ドキュメント](https://matsuand.github.io/docs.docker.jp.onthefly/storage/volumes/)
- [Fetching Title#k7mp](https://karuta-kayituka.hatenablog.com/entry/2019/05/04/114056)