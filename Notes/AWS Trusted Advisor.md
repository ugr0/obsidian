お客様が AWS のベストプラクティスをフォローするためのレコメンデーションを提供いたします。Trusted Advisor は、チェックを使ってお客様のアカウントを評価します。これらのチェックは、お客様の AWS インフラストラクチャを最適化し、セキュリティとパフォーマンスを向上し、コストを削減し、サービスをモニタリングします。そしてレコメンデーションに従って、サービスやリソースを最適化することができます。

- コストの最適化
	- 使用率の低いリソースのコスト最適化チェック
		- Amazon RDS Idle DB Instances
		- Idle Load Balancers
		- Low Utilization Amazon EC2 Instances
		- Unassociated Elastic IP Addresses
		- Underutlized Amazon EBS Volumes
		- 使用率の低いAmazon Redshift クラスタ
	- リザーブドインスタンス、Saving Plansに対する最適化チェック
		- Amazon EC2 Reserved Instances Lease Expiration
		- Amazon EC2リザーブドインスタンスの最適化、Amazon ElastiCacheリザーブドノードの最適化、 Amazon OpenSearch Serviceリザーブドインスタンスの最適化, Amazon Redshiftリザーブドノードの最適化、およびAmazon Relational Database Serviceのリザーブドインスタンスの最適化
		- Saving Plans
- パフォーマンス
- セキュリティ
- 耐障害性
- サービスクォータ


- 通知はメールのみ。SNSなどのプッシュ通知をするためには、設定をしてTrusted Advisorの変更を監視する必要がある


![[Pasted image 20230516094418.png]]

# 資料
- [AWS Trusted Advisor](https://aws.amazon.com/jp/premiumsupport/technology/trusted-advisor/)
- [AWS Trusted Advisor チェックリファレンス - AWS Support](https://docs.aws.amazon.com/ja_jp/awssupport/latest/user/trusted-advisor-check-reference.html)
- [AWS Trusted Advisor メトリクスをモニタリングする Amazon CloudWatch アラームを作成する - AWS Support](https://docs.aws.amazon.com/ja_jp/awssupport/latest/user/cloudwatch-metrics-ta.html#trusted-advisor-metrics-dimensions)