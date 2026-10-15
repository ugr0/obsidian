---
URL: https://zenn.dev/sasakiki/articles/3c903edaea1817
Glasp URL: https://glasp.co/f5XC0CoKGYhSNqcjs12752ID2q02/p/c5af3a65a268f011774f
Tags: []
Last updated: 2024-10-31
---
#### Highlights & Notes

> 操作の順番を決める際に、Terraformは暗黙的または明示的なリソースの関連性のみを考慮します。

> Terraformのmoduleは1階層のディレクトリからのみなり、ネストされたディレクトリは別のmoduleとして扱われます。

> 常にひとつのRootモジュールのコンテクスト内で実行されます。

> それぞれのリソースブロックが1つ以上のインフラのオブジェクトを表しています。

> ローカル名はTerraformモジュール内でそのリソースがどこからきたものかを参照する際に使用されますが、モジュールの外には影響がありません。

> stateはterraformの構成ファイルと実際に作成されたリソースを紐づけ、metadatをトラッキングして、大きいインフラリソースのパフォーマンスの改善に利用されます。


