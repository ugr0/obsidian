- AWSのAPI利用状況に関するログを記録することができる
- デフォルトでOnになっているが、永続的に使いたい場合は明示的にOnと設定する。
- ログファイルは[[Amazon S3]]に保存される
- ログファイルの暗号化
	- [AWS KMS キーによる CloudTrail ログファイルの暗号化 (SSE-KMS) - AWS CloudTrail](https://docs.aws.amazon.com/ja_jp/awscloudtrail/latest/userguide/encrypting-cloudtrail-log-files-with-aws-kms.html)
- 過去90日間のサービスに対する操作を表示する
- [CloudTrail ログファイルの整合性の検証 - AWS CloudTrail](https://docs.aws.amazon.com/ja_jp/awscloudtrail/latest/userguide/cloudtrail-log-file-validation-intro.html)
	- 有効にすることで、S3バケットに配信された後に変更されたか、修正されたか、削除されたかを簡単に検出できる
- [[Amazon SNS]]と結合することで、特定の操作をしたときにEメールなどで通知できる

![[Pasted image 20230516094308.png]]