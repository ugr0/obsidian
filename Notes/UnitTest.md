`/tests/Unit`配下にテストを配置する。  
一番粒度の細かいテスト。

Service、Model、Middleware、Policyなど、  
自分で作ったクラス１つ１つと対応するように  
テストクラス（ファイル）を１つ１つ作る。

その対象クラスのメソッド１つ１つの動作を検証するための  
テストケースをコードに書いていく。

Controllerクラスのテストは  
UnitTestではなくFeatureTestとするほうがしっくりくる。