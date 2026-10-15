---
URL: https://docs.docker.jp/compose/extends.html
Glasp URL: https://glasp.co/f5XC0CoKGYhSNqcjs12752ID2q02/p/uGY6K8VDFHsLwBShQaNz
Tags: []
Last updated: 2023-06-21
---
#### Highlights & Notes

> デフォルトでは、 Compose は２つのファイルを読み込みます。１つは docker-compose.yml で、もう１つはオプションで docker-compose.override.yml ファイルです。

> extends キーワードは、共通の設定を異なるファイル間で共有できます。また、全く異なるプロジェクトでさえも共有できます。

> 複数のサービスが共通の設定を持つ場合、個々のサービスを拡張するのが便利です。

> Compose はオリジナルのサービスにある設定情報を、ローカルの設定情報へとコピーします

> 単一の値を持つ場合、古い値を新しい値で置き換えます。

> 複数の値を持つオプション では、Compose は両方の値を連結します。

> Compose はローカルで定義した値を優先しながら、全体を「 統合merge 」します。 environment と labels では、環境変数の値やラベル名で明示された値が使われます。

> コンテナ内にマウントするパスを使う場合に 統合merge されます。


