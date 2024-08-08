Amazon Elastic Block Store

- EC2インスタンスのボリュームとして使用
- 「AZ内」でレプリケート
- [[EBSのボリュームタイプ]]
- ボリュームタイムの変更が可能
- 容量の変更が可能
- [[EBS最適化インスタンス]]
- 高い耐久性のスナップショット
	- 自動的にS3に保管される
	- 初回はフルバックアップで、それ以降は増分
- [[EBSボリュームの暗号化]]
- 永続的ストレージ
- [[EBS-Backedインスタンス]]
- [[インスタンスストア]]と比較される
- [[EBS高速スナップショット復元(FSR)]]

![[Pasted image 20230515234815.png]]
![[Pasted image 20230716221627.png]]
![[Pasted image 20230716221606.png]]
![[Pasted image 20230717160432.png]]
![[Pasted image 20230716221842.png]]
![[Pasted image 20230716221858.png]]
![[Pasted image 20230716222059.png]]
![[Pasted image 20230717161039.png]]
![[Pasted image 20230717161110.png]]

# Snapshot
![[Pasted image 20230717161145.png]]
![[Pasted image 20230717161210.png]]
![[Pasted image 20230717161322.png]]
![[Pasted image 20230717161645.png]]
![[Pasted image 20230717162649.png]]

![[Pasted image 20230717162856.png]]

# 参考
- [Amazon EBS 最適化インスタンスを使用する - Amazon Elastic Compute Cloud](https://docs.aws.amazon.com/ja_jp/AWSEC2/latest/UserGuide/ebs-optimized.html)