---
URL: https://dev.classmethod.jp/articles/iam-and-presigned-url/
Glasp URL: https://glasp.co/f5XC0CoKGYhSNqcjs12752ID2q02/p/0Khf68IUO3Dk3sMnNaLb
Tags: []
Last updated: 2023-12-10
---
#### Highlights & Notes

> アクセスは「署名付き URL を生成した IAM エンティティ」によるものとして扱われる

> AWS CLI では、ダウンロード用のみ、署名付き URL の発行に対応してます。

> 署名付き URL の生成に権限は必要ない

> リソースベースポリシー

> リクエストを実行した時点

> 通常は署名付き URL の作成とほぼ同時にリクエストが行われるが、URL の作成だけされてリクエストが保留された状態

> Authorizationヘッダーに署名を含めるクエリ文字列に署名を含める

> 「ロールを引き受けたセッション」で生成できる URL の有効期限は IAM ユーザーのそれと比べて短いという仕様

> リクエストが実行された時点の権限構成が評価される

> 認可はリクエストを実行した時点の権限構成をもとに行われる


