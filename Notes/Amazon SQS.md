非同期で処理を行いたい場合に使う。

# 特徴
- 標準キューではメッセージの順番が保証されない
	- 同一メッセージが重複して配信される可能性があること
- FIFOキューはメッセージを順番に配信できるが性能が若干劣る
- 可視性タイムアウトを設定すると処理の重複を防止できる
	- デフォルトで30秒。最小0秒, 最大12時間

# ロングポーリング
- キューがからの場合にメッセージを取得できるまで待ち時間を設定することでメッセージ取得要求の数を減らすことができる
- [Amazon SQS ショートポーリングとロングポーリング - Amazon Simple Queue Service](https://docs.aws.amazon.com/ja_jp/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-short-and-long-polling.html)