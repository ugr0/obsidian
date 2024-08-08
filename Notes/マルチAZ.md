- 利用する基本的なサービス
	- [[Amazon VPC]]
	- [[ELB]]
	- [[Amazon EC2]] + [[Amazon EBS]]
	- [[Amazon EC2]] + [[Amazon RDS]]


![[Pasted image 20230719010444.png]]
![[Pasted image 20230719010618.png]]

# マルチAZ DB Cluster
あらかじめWriterとは別のAZにアクティブなReaderのインスタンスを配置し、 フェイルオーバー時はReaderをWriterを素早く昇格させることで、フェイルオーバーの高速化を図っている