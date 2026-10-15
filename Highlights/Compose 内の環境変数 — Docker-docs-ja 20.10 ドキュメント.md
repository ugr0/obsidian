---
URL: https://docs.docker.jp/compose/environment-variables.html
Glasp URL: https://glasp.co/f5XC0CoKGYhSNqcjs12752ID2q02/p/T77RwckFQqLZKlL2gh6R
Tags: []
Last updated: 2023-06-21
---
#### Highlights & Notes

> 複数の環境変数がある場合、デフォルトでは .env というファイル名で展開したい変数を記述できます。

> ${POSTGRES_VERSION}

> 環境変数の値が無い場合は、 Compose は空の文字列を投入します。

> $変数 と ${変数} 構文をサポートしています。

> 設定上で文字列としてのドル記号が必要な場合は、 $$ （二重ドル記号）を使います。

> docker compose コマンドを実行する現在の作業ディレクトリとみなします

> それぞれの .env ファイル内で指定された値よりも、シェル上の値が優先されます。


