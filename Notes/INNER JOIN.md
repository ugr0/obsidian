内部結合。`JOIN`と`INNER JOIN`は同じ。

# 特徴
1. 右テーブルの行数に合わせて左テーブルの行数を複製する
   (これあってる？)
2. 結合相手がいない行は結合結果から消滅する。([[OUTER JOIN]](外部結合)では、条件に一致させた状態で結合してくれるのに加え、どちらかのテーブルに存在しないもの、NULLのものに関しても強制的に取得する。)

# 構文
```sql
SELECT * 
	FROM 結合元のテーブル名(左) 
	JOIN 結合先のテーブル名(右) 
	  ON 両テーブルの結合条件
```


# 参考記事
- [【INNER JOIN, LEFT JOIN , RIGHT JOIN】テーブル結合の挙動をまとめてみた【SQL】 - Qiita](https://qiita.com/ngron/items/db4947fb0551f21321c0)