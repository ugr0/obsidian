---
URL: https://zenn.dev/soundtricker/articles/fa27c919ad3630
Glasp URL: https://glasp.co/f5XC0CoKGYhSNqcjs12752ID2q02/p/be4f33407139409ee809
Tags: []
Last updated: 2025-10-08
---
#### Highlights & Notes

> 最近ではInfrastructure Manager(Infra Manager)というサービスも提供されており、Terraformの実行や履歴、Stateファイル[2]の管理もGoogle Cloud上でできるようになり

> 「(複数の)開発者が開発中に触りたい部分はTerraformで管理しない(別の手段で管理する)」が今のところ良い指針です。

> 開発者が自身のブランチ中で追加/修正/削除することが多く上記の例のようなことが発生しやすいため、CIによるデプロイなどでterraformでは管理しないようにしています。

> Cloud TasksのQueueやCloud Scheculerをyamlで管理していて、CD時にrakeタスクやpythonのfabなどを利用してGoogle Cloud側との差分を見てデプロイしています。

> Cloud Runに設定する環境変数も以下のようなyamlを作成してデプロイ時に展開&Cloud Runへ設定するようにしています。(yamlからコマンドライン引数に変換するパーサを書いてる 値がsm://で始まっていたらそれをsecret keyにsecret managerから環境変数へ設定するようなオプション設定をする)

> 上ではルートProjectと書いていますが、複数のProjectにまたがって何かしたい時に利用するProjectです。

> staging Project IDにはランダムサフィックスを付けておいたほうが良いです。(productionは任意) これはProject IDが他と被らないようにするためというのもありますが、開発状況によりstagingの増減をするシーンが多々有り、作り直ししたときに同じProject IDのProjectが作れないということを避けるためです。

> Terraformではtf stateファイルの置き場(Terraform Backend)として、 Cloud Storageが選択できるため、Google Cloudで利用する場合はCloud Storageにしておくのがいい

> 上記の様に複数のプロジェクトを同一バケットで扱う場合は、prefix を指定して Project 毎にディレクトリを指定します。

> 使用するバケットは オブジェクトバージョニング を有効にすることをお勧めします。純粋にバージョン管理的な意味合いもありますが、様々な事情で、terraform state rmコマンドなどで、stateファイルを操作したいことがあります。その際に操作ミスなので下手にstateの状態が正しくない状態になってしまった時にオブジェクトバージョニングを有効にしておけば、操作前の状態にstateファイルを戻すことができます。

> Terraform実行用のサービスアカウント作成し、Terraformの実行はそのサービスアカウント経由で実行することが望ましいです。

> セキュリティ観点で、サービスアカウントキーファイルを利用することは非推奨です。

> Terraformのコードは、可読性と一貫性を保つために、公式ドキュメントで推奨されているスタイルガイドに従ってフォーマットする必要があります。

> Github ActionsでGoogle Cloudの認証を行う場合は google-github-actions/auth Actionsを利用します。ここで認証したサービスアカウントから任意のサービスアカウントへ権限借用する場合は、google-github-actions/auth の delegates に権限借用を行いたいサービスアカントを設定する必要があります。この設定がないと権限借用ができないというエラーになります(エラーメッセージは忘れました)

> iam_policyとiam_bindingについては、Terraform上で管理してないIAMポリシーは、全て削除されるということです。


