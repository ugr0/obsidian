- Command and Query Responsibility Segregation
- コマンドクエリ責務分離

今まで１つのアプリケーションでまとめて扱っていた処理を、データを登録する処理(コマンド)とデータを参照する処理(クエリ)の役割を分離することにより、アクセスパターンやユースケースの違いに対応できる。

アクセスパターンがそれぞれ違うので、それぞれの要件に合ったデータベースを選択できる。

それぞれの要件に合ったデータベースを選択するので、データベース間のデータ連携(もしくは変換)を非同期に行う仕組みも必要。

# 参考
- [CQRS パターン - Azure Architecture Center | Microsoft Learn](https://learn.microsoft.com/ja-jp/azure/architecture/patterns/cqrs)
- [[📚良いコード／悪いコードで学ぶ設計入門(ミノ駆動本)]]