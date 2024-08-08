- 使用するすべての AWS リソース (Amazon EC2 インスタンスや Amazon RDS DB インスタンスなど) を記述するテンプレートを作成すれば、CloudFormation がお客様に代わってこれらのリソースの[[プロビジョニング]]や設定を受け持つ
- テンプレート
	- CloudFormationの設定ファイルを指し、このファイルに[[プロビジョニング]]したいAWSリソースを記述する
- スタック
	- テンプレートに従ってCloudFormationでプロビジョニングされるAWSリソースの集合をさす
	- [DeletionPolicy 属性 - AWS CloudFormation](https://docs.aws.amazon.com/ja_jp/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html)
		- stackを消してもリソースを消せないようにする -> Retain
		- snapshopを残す -> Snapshot
- 変更セット
	- スタックを更新する必要がある場合は、変更の実装前に実行中のリソースに与える影響を理解することで、安心してスタックを更新できます
	- [変更セットを使用したスタックの更新 - AWS CloudFormation](https://docs.aws.amazon.com/ja_jp/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-changesets.html)
 - ドリフト
	 - コンソールから手作業で変更した時に生じるテンプレートとの差分
 - [[AWS CloudFormation StackSets]]

# 資料
- [AWS CloudFormation の概要 - AWS CloudFormation](https://docs.aws.amazon.com/ja_jp/AWSCloudFormation/latest/UserGuide/Welcome.html)