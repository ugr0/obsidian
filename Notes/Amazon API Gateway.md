- APIの作成、配布、保守、監視、保護を簡単に行えるサービス
- 特定のリージョンにAPIがデプロイされ、その際のAPIのホスト名のことをAPIエンドポイントという。
- 料金は、「API呼び出し数」と「使用したキャッシュ量」に基づいている

| エンドポイント名              | トラフィックの発信元                        | 使用可能なAPI      |
| ----------------------------- | ------------------------------------------- | ------------------ |
| リージョンAPIエンドポイント   | API Gatewayと同一リージョン内のクライアント | HTTP API, REST API |
| エッジ最適化APIエンドポイント | 地理的に分散されたクライアント              | REST API           |
| プライベートAPIエンドポイント | VPC内のクライアント                         | REST API           |


- [API キャッシュを有効にして応答性を強化する - Amazon API Gateway](https://docs.aws.amazon.com/ja_jp/apigateway/latest/developerguide/api-gateway-caching.html)
- APIの使用をユーザーに応じて、使用量を分けれる
	- [API キーを使用した使用量プランの作成と使用 - Amazon API Gateway](https://docs.aws.amazon.com/ja_jp/apigateway/latest/developerguide/api-gateway-api-usage-plans.html)