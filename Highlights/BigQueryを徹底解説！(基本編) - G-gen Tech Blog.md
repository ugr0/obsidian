---
URL: https://blog.g-gen.co.jp/entry/bigquery-explained-basics
Glasp URL: https://glasp.co/f5XC0CoKGYhSNqcjs12752ID2q02/p/a4824229443a886ec6fc
Tags: []
Last updated: 2024-09-18
---
#### Highlights & Notes

> コンピュート処理を行うワーカーはコンテナ群で形成されており (裏では Borg と呼ばれる技術が使われています)、ユーザーによるジョブ投入に応じて自動的にスケーリングします。

> BigQuery にロードすることなくそのままクエリできたり

> BigQuery には、Amazon Web Services (AWS) の Amazon S3 や Microsoft Azure の Azure Blob Storage など、他のクラウドサービスのデータを取り込むための機能も備わっています。

> データセット (後述) ごとに Logical Storage 課金か Physical Storage 課金（Compressed Storage とも呼称）かを選択することができます。

> Logical Storage 課金を選択すると、圧縮前の額面データサイズに課金されます。Physical Storage 課金だと、圧縮後の実データサイズに対して課金されます。

> 格納してすぐのデータは Active Storage の単価で課金されます。その後、90 日間連続で変更がされなかったデータは Long-term Storage という扱いになり、より安価な単価で課金されます。

> オンデマンドの場合、BigQuery が1ヶ月にスキャンしたデータサイズに応じて料金が決定します。

> BigQuery Editions では、利用したスロットの量に応じて課金されます。スロットとは、BigQuery がクエリの実行に使う CPU のリソース量を図るための単位

> テーブルをグルーピングするための論理的な入れ物です。


