- **Mirror Source** – 特定の VPC 内にある AWS ネットワークリソースで、トラフィックの送信元として使用できます。VPC トラフィックミラーリングは、ミラー送信元として Elastic Network Interface (ENI) を使用できます。

- **Mirror Target** – ミラーリングの対象となるトラフィックの送信先として [ENI](https://aws.amazon.com/blogs/aws/new-elastic-network-interfaces-in-the-virtual-private-cloud/) または [Network Load Balancer](https://aws.amazon.com/blogs/aws/new-network-load-balancer-effortless-scaling-to-millions-of-requests-per-second/) を使用できます。送信先はミラー送信元と同一の AWS アカウント内であることも、上記で説明したとおり、集中型 VPC モデルを活用して別のアカウントに置くこともできます。

- **Mirror Filter** – 捕捉 (承認) またはスキップ (拒否) するインバウンドまたはアウトバウンド (送信元に対して) のトラフィックの仕様。フィルターはプロトコル、送信元と送信先のポートの範囲、送信元と送信先の CIDR ブロックを指定できます。ルールは採番され、特定のミラーセッションの範囲内の順序で処理されます。

- **Traffic Mirror Session** – フィルターを使用するミラー送信元とミラー送信先間の接続。セッションは採番され、順番に評価されて、最初の一致 (承認または拒否) がパケットの処理を決定するために使用されます。指定されたパケットは、最大で 1 つの送信先へ送信されます。

- [最新 – VPC トラフィックミラーリング – ネットワークトラフィックを捉えて検査する | Amazon Web Services ブログ](https://aws.amazon.com/jp/blogs/news/new-vpc-traffic-mirroring/)