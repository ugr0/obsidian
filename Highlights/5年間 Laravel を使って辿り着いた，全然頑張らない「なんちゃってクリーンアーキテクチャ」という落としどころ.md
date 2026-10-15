---
URL: https://zenn.dev/mpyw/articles/ce7d09eb6d8117
Glasp URL: https://glasp.co/f5XC0CoKGYhSNqcjs12752ID2q02/p/AvoB2GlKhwd52FhIkn3g
Tags: []
Last updated: 2023-07-11
---
#### Highlights & Notes

>  HTTP に依存している例外があるため， HTTP 非依存の例外を定義してモデルで使用し，これをコントローラで変換することにします。

> コントローラ側での処理を隠蔽するために書いています。

> Eloquent Model に対する操作単位でメソッドに切り出して，判定ロジックをコントローラの外に出すことができます。

> 逆に言えば HTTP がデータベースレイヤに強く依存した実装となっており，柔軟性を大きく損なうもの

> すべてのメソッドの実装は誰も把握できないレベル

> 結果的にRepository に条件の組み立て方 1 つごとに 1 メソッド用意することで， Repository クラスが肥大化してしまうことが懸念されます。

> 単一責務な Service は UseCase と呼ぶほうがしっくり来る


