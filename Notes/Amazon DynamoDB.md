- NoSQLデータベースサービス
- ms単位の一貫したレイテンシーを提供できる
- 1日に10兆件以上のリクエストを処理することができる
- 毎秒2000万件を超えるリクエストをサポートする

![[Pasted image 20230516000907.png]]
![[Pasted image 20230516000929.png]]

- 自動的にデータが3箇所のAZに保存される
- 結果整合性モデル
	- 結果整合性は、処理は高速だが最新の結果が反映されていないことがある
	- 強力な整合性は、確実に最新のデータにアクセスできるが、応答は結果整合性よりも遅くなる
	- 2つのAZに正常に書き込みが完了した時点で、正常に書き込みが完了したという判断になっているので、そのもう一つのAZのを読み取ると最新のデータが取れない状況が生まれる。
- 強力な整合性のある読み取り
	- [読み込み整合性 - Amazon DynamoDB](https://docs.aws.amazon.com/ja_jp/amazondynamodb/latest/developerguide/HowItWorks.ReadConsistency.html)
- ポイントインタイムリカバリ
	- 過去35日間の任意の時点にデータを戻すことができる
- 課金
	- キャパシティモード
		- オンデマンド
		- プロビジョニング済み
- TTLを使用して、項目を期限切れにする設定ができる
	- [DynamoDB の有効期限 (TTL) を使用して項目を期限切れにする - Amazon DynamoDB](https://docs.aws.amazon.com/ja_jp/amazondynamodb/latest/developerguide/TTL.html)

# セカンダリインデックス
[セカンダリインデックスを使用したデータアクセス性の向上 - Amazon DynamoDB](https://docs.aws.amazon.com/ja_jp/amazondynamodb/latest/developerguide/SecondaryIndexes.html)
[DynamoDBのキー・インデックスについてまとめてみた #DynamoDB - Qiita](https://qiita.com/shibataka000/items/e3f3792201d6fcc397fd)

- [[LSI]]
- [[GSI]]


# 資料
- [特徴 - Amazon DynamoDB | AWS](https://aws.amazon.com/jp/dynamodb/features/#Performance_at_scale)
- [DynamoDBにまつわるサーバレス失敗談とその対処法 - ログミーTech](https://logmi.jp/tech/articles/321337)