- Amazon CloudWatch は、AWSリソースと、AWSで実行されているアプリケーションをリアルタイムでモニターリングします
- CloudWatch を使用して[[メトリクス]]を収集し、追跡できます
- EC2のOSレベル以上で発生する情報は、標準メトリクスとしてはストリーミングされない
 - ダッシュボードの共有
	 - [CloudWatch ダッシュボードの共有 - Amazon CloudWatch](https://docs.aws.amazon.com/ja_jp/AmazonCloudWatch/latest/monitoring/cloudwatch-dashboard-sharing.html)

# 関連サービス
- [[Amazon CloudWatch Logs]]
- [[CloudWatch Alarm]]
- [[CloudWatch Events]]
- [[CloudWatch EC2メトリクス]]

# EC2のメトリクス
- 標準[[メトリクス]]

| メトリクス     | 説明                                                           |
| -------------- | -------------------------------------------------------------- |
| CPUUtilization | CPU使用率                                                      |
| DiskReadOps    | インスタンスストアボリュームからの読み取り回数(指定された期間) |
| DiskReadBytes  | インスタンスストアボリュームから読み取られたバイト数           |
| NetworkIn      | 全てのネットワークインターフェイスから受信されたバイト数                                                               |

- カスタムメトリクス([[CloudWatchエージェント]]を導入することで収集可能)
	- メモリ使用率
	- ディスク使用率
	- スワップ使用率

# 参考
- [Amazon CloudWatch とは - Amazon CloudWatch](https://docs.aws.amazon.com/ja_jp/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html)