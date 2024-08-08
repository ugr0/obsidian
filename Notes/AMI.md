- Amazon マシンイメージ

# 分類
- Amazon EBS-Backed
	- EBSがOSのルート領域として利用される
	- EC2インスタンスを停止してもデータは残る(不揮発性)
- Instance Store-Backed
	- インスタンスストアがルート領域に利用される
	- インスタンスストアはEC2インスタンスを停止するとデータが削除される（揮発性j)

# Case
- 共有
	- [特定の AWS アカウントとの AMI の共有 - Amazon Elastic Compute Cloud](https://docs.aws.amazon.com/ja_jp/AWSEC2/latest/UserGuide/sharingamis-explicit.html)