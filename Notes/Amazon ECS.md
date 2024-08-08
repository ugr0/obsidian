- コンテナ管理を行う、マネージドサービス。

# ECS環境の構築
- クラスター作成
- タスク定義
	- Dockerイメージの格納先
	- メモリの使用量の制限
	- ネットワーク
	- ストレージ
	- ヘルスチェック
- [[ELB]]設定
- サービス設定
	- クラスター上で起動するコンテナ数
	- 起動するコンテナの最大数


# Auto Scaling
- [サービスの自動スケーリング - Amazon Elastic Container Service](https://docs.aws.amazon.com/ja_jp/AmazonECS/latest/developerguide/service-auto-scaling.html)
- [[ターゲット追跡スケーリングポリシー]]
- [[ステップスケーリングポリシー]]
- [[スケジュールに基づくスケーリング]]


# Contents
- [サービスの負荷分散 - Amazon Elastic Container Service](https://docs.aws.amazon.com/ja_jp/AmazonECS/latest/developerguide/service-load-balancing.html)