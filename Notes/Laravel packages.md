# スターターキット
- [[Laravel Breeze]]
- [[Laravel Jetstream]]
- [[Laravel Sail]]

# ローカル環境
- [Laravel Herd](https://herd.laravel.com/)
- [[Laravel Homestead]]
- [[Laravel Valet]]

# 静的解析
- laravel-ide-helper
	- [GitHub - barryvdh/laravel-ide-helper: Laravel IDE Helper](https://github.com/barryvdh/laravel-ide-helper)
	- IDE保管用のヘルパーファイルを生成する
- php_codesniffer
	- [GitHub - squizlabs/PHP_CodeSniffer: PHP_CodeSniffer tokenizes PHP files and detects violations of a defined set of coding standards.](https://github.com/squizlabs/PHP_CodeSniffer)
	- コードの構文チェック・自動修正を行うことができる
- larastan(phpstan)
	- [GitHub - nunomaduro/larastan: ⚗️ Adds code analysis to Laravel improving developer productivity and code quality.](https://github.com/nunomaduro/larastan)
	- Laravelのコードの静的解析を行うことができる
	- 参考リンク
		- [PHPStan の使い方 - LAZE SOFTWARE](https://lazesoftware.com/ja/blog/210906/)
- phive
	[Phive](https://phar.io/)はPHPのための便利ツールをPharファイル単位でインストールできるツールです。このツールも`composer require --dev`では依存性が混ざる問題を防ぐ問題を避けられます。

# E2E
- [[Laravel Dusk]]

# タスク実行
- [[Laravel Envoy]]

# 認証
- [[Laravel Fortify]]
- [[Laravel Sanctum]]
- [[Laravel Precognition]]
- [[Laravel Socialite]]
## OAuth2
- [[Laravel Passport]]

# ルーティング
- [[Laravel Folio]]

# キュー
- [[Laravel Horizon]]

# パフォーマンス
- [[Laravel Octane]]
## 非同期
- Swoole
	- [Swooleを使う前に知っておきたい基礎の基礎 - Qiita](https://qiita.com/prograti/items/e29210300232e4a3d8b7)

# 機能フラグ
- [[Laravel Pennant]]

# モニタリング・監視・debug
- [[Laravel Pulse]]
- [[Laravel Telescope]]
- laravel-debugbar
	- [GitHub - barryvdh/laravel-debugbar: Laravel Debugbar (Integrates PHP Debug Bar)](https://github.com/barryvdh/laravel-debugbar)
	- デバッグ情報をブラウザで確認できる
- clockwork
	- [GitHub - itsgoingd/clockwork: Clockwork - php dev tools in your browser - server-side component](https://github.com/itsgoingd/clockwork)
	- デバッグサポート用

# 全文検索
- [[Laravel Scout]]

# DB
- dbal
	- [GitHub - doctrine/dbal: Doctrine Database Abstraction Layer](https://github.com/doctrine/dbal)
- iseed
	- [GitHub - orangehill/iseed: Laravel Inverse Seed Generator](https://github.com/orangehill/iseed)
	- 実際にDBに入っているデータからseederファイルを逆生成できる
