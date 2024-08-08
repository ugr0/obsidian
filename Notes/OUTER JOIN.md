[[INNER JOIN]](内部結合)のように条件に一致させた状態で結合してくれるのに加え、**どちらかのテーブルに存在しないもの、NULLのものに関しても強制的に取得**する。

# LEFT JOIN( = LEFT OUTER JOIN)
左外部結合。左のテーブルは全て表示する。左テーブルを基準に右テーブルにないものは、全ての値をNULLとして表示する。
```sql
SELECT * 
	FROM users 
	LEFT JOIN posts 
	ON users.id = posts.user_id
```

| id  | name   | id   | body  | user_id |
| --- | ------ | ---- | ----- | ------- |
| 3   | hanako | 1    | Hello | 3       |
| 1   | taro   | 2    | Hi    | 1       |
| 2   | jiro   | 3    | Good  | 2       |
| 4   | saito  | NULL | NULL  | NULL    |

# RIGHT JOIN( = RIGHT OUTER JOIN)
右外部結合。LEFT JOINの逆。
```sql
SELECT * 
	FROM users 
	RIGHT JOIN posts 
	ON users.id = posts.user_id
```

| id   | name   | id  | body  | user_id |
| ---- | ------ | --- | ----- | ------- |
| 1    | taro   | 2   | Hi    | 1       |
| 2    | jiro   | 3   | Good  | 2       |
| 3    | hanako | 1   | Hello | 3       |
| NULL | NULL   | 4   | Sorry | 4       |

# FULL JOIN( = FULL OUTER JOIN)
完全外部結合。左右の全テーブルを全て表示させる。
```sql
SELECT * 
	FROM users 
	FULL JOIN posts 
	ON users.id = posts.user_id
```
