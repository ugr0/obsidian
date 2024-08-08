Amazon Simple Storage Service

# Amazon S3 標準
- S3標準のみ、データ取り出しに料金がかからない
- デフォルトで同一リージョン内の3箇所のAZへ自動的に複製される
- 耐久性はイレブンナイン

![[Pasted image 20230515233858.png]]

# 機能
## データの復元性と大規模災害対策
- [[オブジェクトロック機能]]
- バージョニング機能
	- 下の[[クロスリージョンレプリケーション]]の時は両方のリージョンでバージョニングを設定する必要がある
	- オブジェクトを削除すると削除マーカーと呼ばれるデータを持たないオブジェクトが最新のオブジェクトとなる
- [[S3レプリケーション]]


## セキュリティ対策
- アクセス制御
	- IAMポリシー
	- バケットポリシー
	- [[ACL]]
	- ブロックパブリックアクセス
- [[S3の暗号化]]

## ストレージ以外での用途
- Webサイトホスティング
- 署名付きURL

# コスト削減
- [Amazon S3 コストの見直しと削減 | AWS re:Post](https://repost.aws/ja/knowledge-center/s3-reduce-costs)
- マルチパートアップロード
	- 不完全で終了すると課金が上乗せ
- バージョニング
	- 昔のは消されないので注意
# S3パフォーマンス最適化
- プレフィックス名をランダムにする

## その他
- [[マルチパートアップロード]]
- [[Amazon S3 Transfer Acceleration]]
- S3イベント通知
	- [Amazon S3 イベント通知 - Amazon Simple Storage Service](https://docs.aws.amazon.com/ja_jp/AmazonS3/latest/userguide/EventNotifications.html)
 - S3オブジェクトLambda
	 - [S3 Object Lambda を使用したオブジェクトの変換 - Amazon Simple Storage Service](https://docs.aws.amazon.com/ja_jp/AmazonS3/latest/userguide/transforming-objects.html)
 - サーバーアクセスログ
	 - バケットに対するリクエストの詳細をログに残す
	 - [サーバーアクセスログを使用したリクエストのログ記録 - Amazon Simple Storage Service](https://docs.aws.amazon.com/ja_jp/AmazonS3/latest/userguide/ServerLogs.html)

# ストレージの種類
- 低冗長化ストレージ
	- 2箇所にレプリケーションされる
- 表
	- 下に行くほど安くなり、取り出し費用は多くなる
	- [[Amazon S3 Inteligent-Tiering]]だけは特別で、S3のアクセス頻度が変化するようなケースでは有用

| ストレージクラス名                                  | 耐久性        | 可用性 | 格納されるAZ | 取り出し費用 | 取り出し時間     |
| --------------------------------------------------- | ------------- | ------ | ------------ | ------------ | ---------------- |
| S3 Standard                                         | 99.999999999% | 99.99% | 3AZ以上      | なし         | ミリ秒           |
| [[Amazon S3 Inteligent-Tiering]]                    | 99.999999999% | 99.9%  | 3AZ以上      | 一部あり     | ミリ秒・分・時間 |
| [[Amazon S3 標準  低頻度アクセス(S3標準  IA)]]      | 99.999999999% | 99.9%  | 3AZ以上      | あり         | ミリ秒           |
| [[Amazon S3 1 ゾーン  低頻度アクセス(1ゾーン  IA)]] | 99.999999999% | 99.5%  | 1AZ          | あり         | ミリ秒           |
| [[Glacier Instant Retrieval]]                       | 99.999999999% | 99.9%  | 3AZ以上      | あり         | ミリ秒           |
| [[Glacier Flexible Retrieval]]                      | 99.999999999% | 99.99% | 3AZ以上      | あり         | 分・時間         |
| [[Glacier Deep Archive]]                            | 99.999999999% | 99.99% | 3AZ以上      | あり         | 時間                 |

# Tips
- オブジェクトはバケットからアクセス許可を継承しない。相互に独立している。
- データ転送料金
	- リージョンの外にデータを転送した場合のみ発生する(Cloud Frontについては対象外)

# 資料
- [バケットの制約と制限 - Amazon Simple Storage Service](https://docs.aws.amazon.com/ja_jp/AmazonS3/latest/userguide/BucketRestrictions.html)
- [Amazon S3 ライフサイクルを使用したオブジェクトの移行 - Amazon Simple Storage Service](https://docs.aws.amazon.com/ja_jp/AmazonS3/latest/userguide/lifecycle-transition-general-considerations.html)
