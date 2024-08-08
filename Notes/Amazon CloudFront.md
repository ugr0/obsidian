- 静的データおよび動的データを高速に配信するための[[CDN]]サービス。
	- AWSで唯一のCDNサービス
- CloudFront は[[オリジン]]からウェブコンテンツを取得し、世界中のエッジサーバーネットワークを経由してビューワーにウェブコンテンツを供給する。
	- オリジンにはオンプレミス環境も指定できる
	- 同じドメイン名でURLのパスに応じてオリジンサーバーを指定できる
- コンテンツを配信するときは[[ディストリビューション]]を作成する

# 機能
- SSLによる通信の暗号化
	- REST APIエンドポイントのみ
- 署名付きURL
- カスタムエラーページ
- 地域制限(地理的ブロッキング)
- ストリーミング配信
- フィールドレベル暗号化
- [[Amazon CloudFront Origin Shieid]]
- [[OAI]]
- [[CloudFrontの通信の暗号化の設定]]
- [[CloudFront キャッシュの最適化と可用性]]

# 静的Webサイトを公開する
- アクセスが[[OAI]]で制限されたオリジンとして、REST APIエンドポイントを使用する
- パブリックアクセスを許可して、Webサイトエンドポイントをオリジンとして使用する
- アクセスがRefererヘッダーで制限されたオリジンとして、Webサイトエンドポイントを使用する

# Contents
- オリジングループを使用して、プライマリバケットとスタンバイバケット間でフェイルオーバー処理を設定することができる。（単に両方のバケットをオリジンに追加するだけではできない)
	- [CloudFront オリジンフェイルオーバーによる高可用性の最適化 - Amazon CloudFront](https://docs.aws.amazon.com/ja_jp/AmazonCloudFront/latest/DeveloperGuide/high_availability_origin_failover.html)
 - [CloudFront ディストリビューションでのさまざまなオリジンの使用 - Amazon CloudFront](https://docs.aws.amazon.com/ja_jp/AmazonCloudFront/latest/DeveloperGuide/DownloadDistS3AndCustomOrigins.html)

# 資料
- [Amazon CloudFront とは何ですか? - Amazon CloudFront](https://docs.aws.amazon.com/ja_jp/AmazonCloudFront/latest/DeveloperGuide/Introduction.html)