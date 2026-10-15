---
URL: https://cloud.google.com/blog/ja/topics/developers-practitioners/using-google-cloud-service-account-impersonation-your-terraform-code
Glasp URL: https://glasp.co/f5XC0CoKGYhSNqcjs12752ID2q02/p/26b238423c97d003803a
Tags: []
Last updated: 2025-10-07
---
#### Highlights & Notes

> まず、Terraform コードの実行に使用するサービス アカウントをプロジェクトに用意する必要があります。このサービス アカウントには、コードで参照されるリソースを作成する権限が必要です。次に、自分のユーザー アカウントにサービス アカウント トークン作成者の IAM ロールを付与する必要があります。このロールを使用すると、サービス アカウントの権限を借用して API とリソースにアクセスできます。

> 設定が完了すると、現在のターミナル セッションで実行される Terraform コードには、自分のアカウントではなくサービス アカウントの認証情報が使用されます。

> Terraform コードで作成されるすべてのリソースに対して 1 つのサービス アカウントしか使用できないという制限もあります


