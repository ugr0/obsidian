Amazon Elastic Compute Cloud

# 特徴
- 従量課金制
- [[AMI]]を使用
- インスタンスタイプ
	- t2.microだとtがファミリー, 2が世代, microがサイズ
		- d->内蔵ストレージがある
		- n->ネットワークを強化
		- a->AMDのCPUを搭載
	- NW帯域幅が決まっている
	- EC2インスタンスファミリー
- [[EC2 インスタンスフリート]]
- [[Amazon EC2 Dedicated Host]]
 - 自動復旧
- [[EC2インスタンスファミリー]]

![[Pasted image 20230716215839.png]]

- [[Amazon EC2 Auto Scaling]]
- [[インスタンスユーザーデータ]]
- [[インスタンスメタデータ]]
- [[AWS Systems Manager Session Manager]]
- [[EC2 Image Builder]]
- [[ELB]]
- [[VM Export]]
- [[VM Import]]


# EC2インスタンス最適化
 - [[プレイスメントグループ]]
 - EC2の料金
	- 従量型
		- [[オンデマンドインスタンス]]
	- 予約型
		- [[リザーブドインスタンス]]
		- Savings Plans
	- [[オンデマンドキャパシティ予約]]
	- 入札型
		- [[スポットインスタンス]]
	- 専有型
		- [[ハードウェア専用インスタンス]]
		- Dedicated Hosts

# Cases
- [[Amazon S3]]と[[AWS CodeDeploy]]でEC2インスタンスにデプロイ
	- [Amazon S3 CodeDeploy へのリビジョンをプッシュする (EC2/オンプレミスのデプロイのみ) - AWS CodeDeploy](https://docs.aws.amazon.com/ja_jp/codedeploy/latest/userguide/application-revisions-push.html)