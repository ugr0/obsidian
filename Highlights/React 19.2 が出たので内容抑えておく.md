---
URL: https://zenn.dev/noda_k/articles/d9d63a18cdbe84
Glasp URL: https://glasp.co/f5XC0CoKGYhSNqcjs12752ID2q02/p/710dd0a7d1c79cdbb047
Tags: []
Last updated: 2025-10-09
---
#### Highlights & Notes

> <Activity> は、UIを部分的に可視／非可視モードで制御しつつ、状態や DOM の内容を保持できるようにするためのラッパーコンポーネント

> 当然useEffectの処理が再度実行されますのでもしthemeの変更に依存したくない場合はLintの警告を無視して依存配列を[roomId]のようにしていました。このような記述は非推奨でありバグの原因となります。

> useEffectEvent（onConnected）の中では最新の値を読む一方で、useEffectの依存は必要最小限に保てることです！

> Partial Pre-renderingはページの中ですぐ表示したい静的な部分と個別ユーザーやリクエスト依存の動的領域を“同じルート”内で両立させる戦略

> 動的部分は後からレンダを再開（resume）して埋め込みます。


