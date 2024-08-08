# BrowserTest
`/tests/Browser`配下にテストを配置する。

実際にブラウザを使って画面にリクエスト、  
ボタンをクリック、  
マウスホバー、  
フォーム送信などの操作をするテストをコードで実行できる。

FeatureTestにさらに  
・複数HTTPリクエストの遷移  
・画面操作時のJsの動作  
のような観点を加えてテストできるイメージ。

Unit、FeatureはPHPUnitで動作するテストなのに対し、  
BrowserTestは`laravel/dusk`というパッケージを使ったテスト。