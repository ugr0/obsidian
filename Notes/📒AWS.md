# AWSを操作する3つの方法
- AWSマネジメントコンソール
- AWSコマンドラインインターフェイス(CLI)
- ソフトウェア開発キット(SDK)

# AWS設計のベストプラクティス11
[https://pages.awscloud.com/rs/112-TZM-766/images/AWS設計のベストプラクティスで最低限知っておくべき10のこと_20200617_rev.pdf](https://pages.awscloud.com/rs/112-TZM-766/images/AWS%E8%A8%AD%E8%A8%88%E3%81%AE%E3%83%98%E3%82%99%E3%82%B9%E3%83%88%E3%83%95%E3%82%9A%E3%83%A9%E3%82%AF%E3%83%86%E3%82%A3%E3%82%B9%E3%81%A6%E3%82%99%E6%9C%80%E4%BD%8E%E9%99%90%E7%9F%A5%E3%81%A3%E3%81%A6%E3%81%8A%E3%81%8F%E3%81%B8%E3%82%99%E3%81%8D10%E3%81%AE%E3%81%93%E3%81%A8_20200617_rev.pdf)
- スケーラビリティを確保する
- 環境を自動化する
- 使い捨て可能なリソースを使用する
- コンポーネントを疎結合にする
	- データは常にデータストアに格納し、処理側に持たせない(ステートレス)
- サーバーではなくサービスで設計する
- 適切なデータベースソリューションを選択する
- 単一障害点([[SPOF]])を排除する
- コストを最適化する
- キャッシュを使用する
- 全てのレイヤーでセキュリティを確保する
- 増加するデータの管理
	- [[データレイク]]がベストプラクティス
	- AWSにおけるデータレイク=[[Amazon S3]]

# AWSグローバルインフラストラクチャ
- [AWS グローバルインフラストラクチャ | AWS](https://aws.amazon.com/jp/about-aws/global-infrastructure/)
- エッジインフラ
	- [[AWS Local Zones]]
	- [[AWS WaveLength]]

# クラウドサービスの種類
- アンマネージドサービス
	  スケーリング、耐障害性、可用性を自分で管理
- [[AWS Managed Services]]
  スケーリング、耐障害性、可用性は一般的にサービスに組み込み済み

# カテゴリ別のサービス
- [[AWSのコンピューティング]]
- [[AWSのコンテナ]]
- [[AWSのストレージ]]
- [[AWSの移行と転送]]
- [[AWSのデータベース]]
- [[AWSのネットワーキングとコンテンツ配信]]
- [[AWSの開発者用ツール]]
- [[AWSのCustomer Enablement]]
- [[AWSのロボット工学]]
- [[AWSのブロックチェーン]]
- [[AWSの衛星]]
- [[AWSのQuantum Technologies]]
- [[AWSの管理とガバナンス]]
- [[AWSのメディアサービス]]
- [[AWSのMachine Learning]]
- [[AWSの分析]]
- [[AWSのセキュリティ・ID・コンプライアンス]]
- [[AWSのクラウド財務管理]]
- [[AWSのモバイル]]
- [[AWSのアプリケーション結合]]
- [[AWSのビジネスアプリケーション]]
- [[AWSのエンドユーザーコンピューティング]]
- [[AWSのIoT]]
- [[AWSのゲーム開発]]

# AWS エッジインフラストラクチャ
- [[AWS WaveLength]]
- [[AWS Local Zones]]

# 未整理
- [[VMware Cloud on AWS]]
- [[AWS Device Farm]]
- [[AWS AppSync]]
- [[AWS Compute Optimizer]]
- [[Amazon Elastic Transcoder]]

# プロビジョニングサービス

| AWSサービス                  | サーバー | AWSリソース |
| ---------------------------- | -------- | ----------- |
| [[AWS OpsWorks]]             | ○        | ×           |
| [[AWS System Manager]]       | ○        | ×           |
| [[AWS CloudFormation]]       | ×        | ○           |
| [[Amazon Elastic Beanstalk]] | ○        | ○           |

# Tips
- [[マルチアカウント戦略]]

# AWSのバッチ処理
- [AWSでバッチ処理を実装する際の選択肢とサービス比較](https://zenn.dev/faycute/articles/fb310e3ccd783f)

# AWS認定資格向けの資料
- [ホワイトペーパー | AWS](https://aws.amazon.com/jp/whitepapers/?whitepapers-main.sort-by=item.additionalFields.sortDate&whitepapers-main.sort-order=desc&awsf.whitepapers-content-type=*all&awsf.whitepapers-global-methodology=*all&awsf.whitepapers-tech-category=*all&awsf.whitepapers-industries=*all&awsf.whitepapers-business-category=*all)
	- アーキテクチャ、セキュリティ、エコノミクスなどのトピックを扱ったAWSの技術的なホワイトペーパー
- [AWS トレーニングと認定 – インストラクター主導形式の AWS クラウドトレーニングクラス | AWS](https://aws.amazon.com/jp/training/)
- [パートナー向けトレーニングと認定 - AWS パートナーネットワーク | AWS](https://aws.amazon.com/jp/partners/training/)
- [サービス別資料 | AWS クラウドサービス活用資料集](https://aws.amazon.com/jp/events/aws-event-resource/archive/?cards.sort-by=item.additionalFields.SortDate&cards.sort-order=desc&awsf.tech-category=*all)
  AWS Black Belt Online Seminar
- [AWS 初心者向け資料 | AWS クラウドサービス活用資料集](https://aws.amazon.com/jp/events/aws-event-resource/beginner/)
- [Self-paced digital training on AWS - AWS Skill Builder](https://explore.skillbuilder.aws/learn/external-ecommerce;view=none;redirectURL=)
- [ハンズオン資料 | AWS クラウドサービス活用資料集](https://aws.amazon.com/jp/events/aws-event-resource/hands-on/)

# アーキテクチャ
- [[モジュラーアーキテクチャ]]
- [[イベントソーシング]]
- [[CQRS]]
- [[サーキットブレーカー]]
- [[Sagaパターン]]
- [[サービスディスカバリ]]
- [[サービスメッシュ]]
- [[分散トレーシング]]
- [[疎結合アーキテクチャ]]

# AWSの資格勉強の例
- [インフラ素人の4年目アプリエンジニアが9カ月弱でAWS11冠するためにした７つのこと](https://zenn.dev/raku/articles/58c1dc8ac7fb30#(%E2%85%B0)%E6%AC%A1%E3%81%AE%E8%A9%A6%E9%A8%93%E6%97%A5%E3%82%92%E5%90%88%E6%A0%BC%E6%97%A5%E3%81%8B%E3%82%891%E3%82%AB%E6%9C%88%E4%BB%A5%E5%86%85%E3%81%AB%E3%82%B9%E3%82%B1%E3%82%B8%E3%83%A5%E3%83%BC%E3%83%AB%E3%81%99%E3%82%8B%EF%BC%88%E5%AF%BE%E8%B1%A1%EF%BC%9A%E5%85%A8%E8%A9%A6%E9%A8%93%EF%BC%89)
- [【最速】既婚子持ち社会人のクラウド初心者でも、1ヶ月半でAWS資格11冠制覇できる方法 - Qiita](https://qiita.com/mrpepper/items/64039b828c82e12ad35f)