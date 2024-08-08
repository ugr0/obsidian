`EXPLAIN`を使って、JOIN時にどちらのテーブルが駆動表でどちらのテーブルが内部表になっているか調べることができる。

また、実行計画を立てるために、テーブルの統計情報から概算値を見積もってrowsを見せてくれる。

```
mysql> EXPLAIN SELECT * FROM t1, t2 WHERE t1.c1 = 1 AND t1.c2 = t2.c3\G
```

