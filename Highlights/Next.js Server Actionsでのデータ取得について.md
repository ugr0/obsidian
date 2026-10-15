---
URL: https://zenn.dev/akky1991/articles/e1bcbfff77488d
Glasp URL: https://glasp.co/f5XC0CoKGYhSNqcjs12752ID2q02/p/d4d872fb336cc74fcbbf
Tags: []
Last updated: 2025-11-05
---
#### Highlights & Notes

> Server Actionsは魅力的な機能ですが、データ取得という特定の用途においては、その仕組みや設計思想に起因するいくつかの側面を慎重に評価する必要があります。

> POSTリクエストが基本であるため、GETリクエストに対する標準的なHTTPキャッシュ（ブラウザ、CDN）は機能しません。

> クライアントからServer Actionを呼び出す際には、必ずクライアント・サーバー間のネットワーク通信が発生します。

> Server Actionsは主にミューテーションのために設計されており、「アクション」という名称もそれを反映しています。

> データ取得ロジックをServer Actionsに強く依存させると、Next.js/React環境以外での再利用が難しくなり、技術的なロックインを招く可能性があります。


