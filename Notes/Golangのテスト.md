- 関数名をTestから初め、引数に`*testing.T`を持つ関数が実行される

- テストの結果が失敗することを明示するには2種類の関数を使い分ける
	- `t.Fatal/t.Fatalf`
	- `t.Error/t.Errorf`

-　パッケージ名の指定の方法
	- テスト対象と同じパッケージ名称でテストコードを書く
		private関数もテストすることができる
	- テスト対象とは別のパッケージ名称でテストコードを書く
		privateな変数や関数にアクセスできないテストを書くことができるので、このパッケージの使用者と同じ実装をサンプルコードとして明示することができる。

- Goでは[[Table Driven Tests]]を推奨している。

- t.Skip / t.Skipf
  テストをスキップする

- setup / teardown

- t.Short
  t.SkipNow()というのをつけるとテストがスキップされる。

```
$ go test -short
```
	この時下のテストはスキップされる
```
func TestA(t *testing.T) {
	if testing.Short() {
		t.SkipNow()	
	}
	log.Println("TestA running")
}
```

- t.Parallel
  テストを並行に処理する
  [Go言語でのテストの並列化 〜t.Parallel()メソッドを理解する〜 | メルカリエンジニアリング](https://engineering.mercari.com/blog/entry/how_to_use_t_parallel/)


# ツール
- [dockertest のススメ](https://zenn.dev/shiguredo/articles/go-test-dockertest)
- [GoにおけるDBテスト dockertest vs testcontainers 比較してみた](https://zenn.dev/jy8752/articles/419ab77b2b6a61)