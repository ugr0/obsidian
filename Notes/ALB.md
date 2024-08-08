- Application Load Balancer

# 機能
- リージョン内でのみトラフィックを分散できる
- スティッキーセッション
	- ロードバランサーがユーザーのセッションを特定のターゲットにバインドするように設定でき、これにより、ユーザーのセッション中のすべてのリクエストが同じターゲットに送信される
	- [Application Load Balancer のスティッキーセッション - Elastic Load Balancing](https://docs.aws.amazon.com/ja_jp/elasticloadbalancing/latest/application/sticky-sessions.html)
	- [Application Load Balancer の CloudWatch メトリクス - Elastic Load Balancing](https://docs.aws.amazon.com/ja_jp/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html#load-balancer-metrics-alb)

![[Pasted image 20230717175940.png]]

- リスナー
- ルール
- ターゲット
	- [[Amazon EC2]]
	- [[Amazon ECS]]
	- [[AWS Lambda]]
	- IP
- ターゲットグループ

![[Pasted image 20230719000932.png]]
![[Pasted image 20230719000953.png]]
![[Pasted image 20230719001104.png]]