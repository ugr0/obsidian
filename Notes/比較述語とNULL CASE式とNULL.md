# 比較述語とNULL CASE式とNULL
```sql
CASE col_1
	WHEN 1    THEN 'o'
	WHEN NULL THEN 'x'
END
```
このCASE式は絶対にxを返さない。なぜなら`col_1 = NULL`が`unknown`になるからで、WHERE句の時と同じように、trueの場合のみが有効。

正しくは、下のように、検索CASE式を使って書く必要がある。
```sql
CASE
	WHEN col_1 = 1   THEN 'o'
	WHEN col_1 = IS NULL THEN 'x'
END
```