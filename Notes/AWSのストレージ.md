## オブジェクトストレージ
- [[Amazon S3]]
## ブロックストレージ
- [[Amazon EBS]]
## その他
- [[AWS Storage Gateway]]
- [[Amazon EFS]]
- [[インスタンスストア]]
- [[Amazon FSx]]
	- [[FSx for Lustre]]
	- [[FSx for OpenZFS]]
	- [[FSx for NetApp ONTAP]]
- [[AWS Snow Family]]
- [[AWS Transfer Family]]
- [[AWS Backup]]

|機能・特徴|EBS|EFS|FSx for Windows|
|---|---|---|---|
|接続|単一EC2インスタンスに接続|複数EC2インスタンスから同時接続可能|複数EC2インスタンスから同時接続可能|
|接続可能台数|1|数千（大規模なファイルシステムをサポート）|数千（大規模なファイルシステムをサポート）|
|利用方法|ブロックストレージとして使用|ネットワークファイルシステムとして使用|ネットワークファイルシステムとして使用|
|データ永続性|ボリュームにデータが永続的に保持|ファイルシステムにデータが永続的に保持|ファイルシステムにデータが永続的に保持|
|耐久性|単一EBSボリュームの場合は99.8％の可用性|11x9（99.999999999％）の耐久性|99.9％の可用性|
|拡張性|ボリュームサイズを拡張可能|自動スケーリングで容量が自動的に拡張|自動スケーリングで容量が自動的に拡張|
|パフォーマンス|ボリュームタイプによって異なる|ファイルシステムサイズによってスループットがスケール|Windowsのネイティブファイルサービスで高パフォーマンス|
|データ暗号化|サポートされている|サポートされている|サポートされている|