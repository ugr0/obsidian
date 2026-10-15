---
URL: https://amazon.com/dp/B0CW1KC9N8
Glasp URL: https://glasp.co/f5XC0CoKGYhSNqcjs12752ID2q02/kindle/B0CW1KC9N8
Author: 著者: 吉井 健文
Tags: []
Last updated: 2026-07-05
---
#### Highlights & Notes

> Pageファイルとして必要最低限な実装内容は、Reactコンポーネントを export default することです。

> App Routerでは、変更されたRoute Segmentのみが再レンダリングされます。

> SSRにおけるすべてのコンポーネントは ブラウザ／サーバー両方で 実行されるものでした。

> Server Component（RSC）」はサーバーサイドで のみ 実行されるコンポーネントです。

> 何も宣言しなければ、デフォルトですべてのコンポーネントがServer Componentとして扱われます。

> 一連のプロセスを「 ハイドレーション」

> 「ブラウザでも実行されるべきコンポーネント」というのは、多くのケースで小さな範囲に絞り込むことができます。

> App RouterではServer／Client Componentのように境界が存在することで、ブラウザに送るJavaScriptを必要最小限に抑えられ、パフォーマンスの向上が見込めます。

> 本来Client Componentでしか使用できない useState をimportしているためで、使用できない旨がエラーとして開発中の画面に表示され

> もし親コンポーネントで"use client" ディレクティブを宣言していたのなら（親がClient Componentなら）このコンポーネントでも"use client" を再宣言する必要は ありません。

> Component上におけるデータの取得は、以下のようなセキュリティおよびパフォーマンスの観点から、可能なかぎりServer Componentを使用することが推奨されています。

> データを取得できるのはPageファイルのみではありません。Layoutファイルや、それらの子となるServer Componentでもデータを取得できます。

> データの取得にともない考慮しなければならないのは、エラーハンドリングやローディング中の表示です。

> コンポーネントに直接 fetch 関数を書かず、この getPhotos 関数のような fetch 関数を使用したデータ取得関数を都度用意するようにしています。

> は「 何も指定しなければ、静的データ取得と扱われて結果はキャッシュされる」というもの

> デフォルトの設定は解除され、リクエストのたびにデータ取得が発生します。


