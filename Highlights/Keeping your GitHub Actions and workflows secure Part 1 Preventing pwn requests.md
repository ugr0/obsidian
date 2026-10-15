---
URL: https://securitylab.github.com/research/github-actions-preventing-pwn-requests/
Glasp URL: https://glasp.co/f5XC0CoKGYhSNqcjs12752ID2q02/p/2qLPJDkdruC1KiogcRIc
Tags: []
Last updated: 2023-12-14
---
#### Highlights & Notes

> PR のターゲット リポジトリのコンテキストで実行されます。これは、標準のチェックアウト アクションがターゲット リポジトリを使用して、ユーザーが指定したコードが誤って使用されることを防ぐことを意味します

> 新しい PR が送信されるときに、プロジェクトのビルドが中断されないこと、機能のリグレッションが導入されないこと、およびテストが合格していることを確認するのが CI/CD の一般的な慣例です。

> PR のコードを注意深く調べずに、ローカル マシン上で信頼できないソースから PR をチェックアウトして構築してはいけないのはこのためです。

> Npm パッケージにはカスタム preinstall および postinstall スクリプトが含まれている可能性があるため、攻撃者が新しいパッケージのリファレンス。最新のビルド オーケストレーションは、複数のコード インジェクション ポイントを必要とするほど複雑です。npm install

> 信頼できないコードの構築が必要で、PR を更新するための書き込み権限も必要なシナリオを可能にする新しいトリガー workflow_run が導入されました。たとえばコードカバレッジ結果やその他のテスト結果。


