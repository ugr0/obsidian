- Amazon EC2インスタンス向けのスケーラブルなネットワークファイルストレージ
- 複数のEC2インスタンスやECSコンテナなどで共有利用できるファイルストレージサービス
	- 同時ファイルアクセスが可能
- Linuxインスタンスのみで機能する
- バックアップは[[AWS Backup]]と連携して行う

# モード
- 既存のではモードは変えられないので、[[AWS DataSync]]などを使って新しいインスタンスを作る必要がある
- スループットモード
	- バーストスループット
	- プロビジョンドスループット
- [Amazon EFS パフォーマンス - Amazon Elastic File System](https://docs.aws.amazon.com/ja_jp/efs/latest/ug/performance.html#performancemodes)


# 高可用性
- 複数のAZに冗長化してデータを保管する

# 耐障害性
- AZ障害が生じた場合でも自動でフェイルオーバーされる([[フォールトトレランス]])

- [[EFSの暗号化]]
# 自動スケーリング
- マネージド型
- ストレージ容量やパフォーマンスを自動でスケーリングする

# 標準的なファイルシステム
- [[NFS]]によってアクセス

# ストレージクラス
- 標準
- 標準 - 低頻度アクセス(Standard - Infrequent Access)
	- 標準より低コスト
	- データの読み取りに対して課金
	- 長期保管やバックアップに適している
- 1ゾーン
	- 低コスト
- 1ゾーン - 低頻度アクセス (One Zone - Infrequent Access)
	- 標準 - 低頻度よりもさらに安価

# 資料
- [Amazon Elastic File System とは - Amazon Elastic File System](https://docs.aws.amazon.com/ja_jp/efs/latest/ug/whatisefs.html)