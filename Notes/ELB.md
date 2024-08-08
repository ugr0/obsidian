- Elastic Load Balancing
![[Pasted image 20230516091332.png]]
![[Pasted image 20230516091658.png]]
![[Pasted image 20230717175507.png]]

# ELBのコンポーネント
- [[ロードバランサー]]
- [[リスナー]]
- [[ターゲットグループ]]

# Contents
- [[ELBの種類]]

# 特徴
- VPC間でロードバランサーを適用させるには[[Amazon Route 53]]を使う。
- [[DNSラウンドロビン]]で各AZ内のELBに振り分け
- ELB自体が高可用性のマネージドサービスなので単一障害点([[SPOF]])にならない。
	- 自動スケーリングする
- セキュリティ機能
	- SSL復号の機能を備えている
	- [[ACM]]と連携し、SSL復号をELBが担うことで、バックエンドインスタンスの負荷軽減や、証明書の一元管理が可能となる
- ヘルスチェック機能
	- 同一リージョン内のターゲットに対して可能
	- [[スティッキーセッション]]
	- [[Connection Draining]]
- [[クロスゾーン負荷分散]]
- 外部ELB(Internet-facing)
	- ELB自体がパブリックサブネットに配置されている。
	- バックエンドインスタンスをパブリックサブネットに配置する必要がないので、セキュリティを高めることができる
- 内部ELB(Internal)
	- VPC内や、オンプレミス環境からのみ利用できる
- 複数値ヘッダー
	- [ターゲットとしての Lambda 関数 - Elastic Load Balancing](https://docs.aws.amazon.com/ja_jp/elasticloadbalancing/latest/application/lambda-functions.html#multi-value-headers)
 - 監視
	 - アクセスログ
		 - デフォルトでオフになっている

![[Pasted image 20230719001150.png]]
![[Pasted image 20230719002827.png]]
![[Pasted image 20230719003734.png]]