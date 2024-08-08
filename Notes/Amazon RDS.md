Amazon Relational Database Service
![[Pasted image 20230516000403.png]]

- [[マルチAZ]]
- [[リードレプリカ]]
- [[RDSの暗号化]]
- RDSのパフォーマンス最適化
	- [[RDS Performance Insights]]
- バックアップ
	- 最大35日間
	- デフォルト7日間
	- スナップショット
		- 共有スナップショットのコピー
			- 暗号化されている場合は、KMS暗号キーへのアクセス権限が必要になる
- ストレージタイプ
	- 汎用 SSD - 汎用 SSD ボリュームは、中規模の DB インスタンスで実行しているさまざまなワークロードに対応できるコスト効率の高いストレージとして使用できます。汎用ストレージは、開発およびテスト環境に適しています。
	    
	    ストレージサイズの範囲を含む汎用 SSD ストレージの詳細については、「[汎用 SSD ストレージ](https://docs.aws.amazon.com/ja_jp/AmazonRDS/latest/UserGuide/CHAP_Storage.html#Concepts.Storage.GeneralSSD)」を参照してください。
    
	- プロビジョンド IOPS SSD - プロビジョンド IOPS ストレージは、低 I/O レイテンシーおよび一貫した I/O スループットが必要となる I/O 負荷の高いワークロード (特にデータベースワークロード) のニーズを満たすように設計されています。プロビジョンド IOPS ストレージは本稼働環境に最適です。
	    
	    ストレージサイズの範囲を含むプロビジョンド IOPS ストレージの詳細については、「[プロビジョンド IOPS SSD ストレージ](https://docs.aws.amazon.com/ja_jp/AmazonRDS/latest/UserGuide/CHAP_Storage.html#USER_PIOPS)」を参照してください。
    
	- マグネティック - また、Amazon RDS は下位互換性のためにマグネティックストレージをサポートしています。新しいストレージが必要な場合には、汎用 SSD またはプロビジョンド IOPS SSD の使用が推奨されます。マグネティックストレージでの DB インスタンスのストレージ量の上限は、他のストレージタイプより少なくなります。詳細については、「[マグネティックストレージ](https://docs.aws.amazon.com/ja_jp/AmazonRDS/latest/UserGuide/CHAP_Storage.html#CHAP_Storage.Magnetic)」を参照してください。

|                    | 可用性 | スループット増 | レイテンシ |
| ------------------ | ------ | -------------- | ---------- |
| スケールアップ     | -      | ○              | -          |
| Multi AZ           | ○      | -              | -          |
| リードレプリカ     | -      | ○              | -          |
| プロビジョンドIOPS | -      | ○              | ○          |

![[Pasted image 20230719010510.png]]