# サポートページ
- [『達人に学ぶ SQL徹底指南書』サポートページ](https://mickindex.sakura.ne.jp/database/db_support_sinan.html#LocalLink-p1_1)

# [[CASE式]]の演習問題
## 1-1 複数列の最大値

自分の解答(○)
```sql
SELECT key,
	CASE WHEN x > y THEN x
	ELSE y END AS greatest
  FROM Greatests
```

自分の解答(?)
```sql
SELECT key,
	CASE WHEN x > y THEN
		(CASE x > z THEN x
		 ELSE z END)
	ELSE (CASE y > z THEN y
		  ELSE z END) END AS greatest
FROM Greatests;
```

### 本の解答
```sql
SELECT key,
	CASE WHEN (CASE WHEN x < y THEN y 
				ELSE x END) < z THEN z
	ELSE (CASE WHEN x < y THEN y 
			ELSE x ENDREATEST(x, y), z) AS greatest
	FROM Greatests;
```

## 1-2 合計と再掲を表頭に出力する行列変換

### 本の解答
```sql
SELECT sex,
	SUM(population) as total,
	SUM(CASE WHEN pref_name = '徳島' THEN population
		ELSE 0 END)	AS col_1 -> tokushima,
	SUM(CASE WHEN pref_name = '香川' THEN population
		ELSE 0 END)	AS col_2 -> kagawa,
	SUM(CASE WHEN pref_name = '愛媛' THEN population
		ELSE 0 END)	AS col_3 -> ehime,
	SUM(CASE WHEN pref_name = '高知' THEN population
		ELSE 0 END)	AS col_4 -> kouchi,
	SUM(CASE WHEN pref_name IN ('徳島', '香川', '愛媛', '高知')
			THEN population
		ELSE 0 END) as saikei
 FROM PopTbl2
 GROUP BY sex
```

## 1-3 ORDER BYでソート列を作る

### 本の解答
```sql
SELECT key
  FROM Greatests
  ORDER BY CASE key
		WHEN 'B' THEN 1
		WHEN 'A' THEN 2
		WHEN 'D' THEN 3
		WHEN 'C' THEN 4
		ELSE NULL END;
```

ソート列を結果に表示したい場合
```sql
SELECT key, 
	CASE key
		WHEN 'B' THEN 1
		WHEN 'A' THEN 2
		WHEN 'D' THEN 3
		WHEN 'C' THEN 4
		ELSE NULL END AS sort_col
	FROM Greatest
  ORDER BY sort_col;
```
問題点
- ソート用の列を設計時の時に作ればそもそもこんなのしなくていい
- SQLはあくまでも、データの検索をするのであって、データの見た目の整形はホスト言語ですればいい

# [[ウィンドウ関数]]の演習問題
## 2-1 ウィンドウ関数の結果予想 その1

### 自分の解答
各行に、全体のload_valの合計値が加わる。
partition byもorder byもないから？

### 解答
↑正解

## 2-2 ウィンドウ関数の結果予想 その2
### 自分の解答
serverごとの合計が各行に加わる。
partition byで集合を指定しているから?

### 解答
↑正解

# [[自己結合の使い方]]の演習問題
## 3-1 重複組合せ
### 自分の解答(○)
```sql
SELECT P1.name AS name_1, P2.name AS name_2
	FROM Products P1 INNER JOIN Products P2
	ON P1.name <= P2.name
```

## 3-2 ウィンドウ関数で重複削除
### 自分の解答(X)
```sql
DELETE FROM Product P1
	WHERE EXISTS( SELECT MAX() -- この辺なんか書きたい...
					FROM Product P2
				)
```

### 解答
(name, price)で一意になっていないのをカウントするテーブルを作って、カウントが1(一意)かそうじゃないかを見る。
```sql
-- (name, price)のパーティションに一意な連番を振ったテーブルを作成
CREATE TABLE Products_NoRedundant
AS
SELECT ROW_NUMBER() 
		OVER(PARTITION BY name, price
					ORDER BY name) AS row_num,
	   name, price
	FROM Products;
```
※ ROW_NUMBER(): パーティション毎に1~の連番を振る関数。

```sql
-- 連番が1以外のレコードを削除
DELETE FROM Products_NoRedundant
	WHERE row_num > 1;
```

# [3値論理とNULL](3%E5%80%A4%E8%AB%96%E7%90%86%E3%81%A8NULL.md)の演習問題
## 4-1 ODERY BY句によるソート結果でのNULL
TODO
## 4-2 NULLと文字列の連結
TODO
## 4-3 COALESCE関数
[COALESCE関数](COALESCE%E9%96%A2%E6%95%B0.md)

# [[EXISTS述語]]の演習問題
## 5-1 配列テーブル-行持ちの場合
### 自分の解答(x)
```sql
SELECT DISTINCT key 
	FROM ArrayTbl2 t1
	WHERE EXISTS(
		SELECT *
			FROM ArrayTbl2 t2
			WHERE 
		)
```

### 解答
- NULLを評価して、バグる可能性があることを思い出す。
```sql
SELECT DISTINCT key
	FROM ArrayTbl2 A1
	WHERE NOT EXISTS (SELECT *
		FROM ArrayTbl2 A2
		WHERE A1.key = A2.key
			AND (A2.val <> 1 OR A2.val IS NULL));
```
最後のA2.val IS NULLがないと、NOT EXISTSがtrueに評価される。
別解は本を参照。

## 5-2 ALL述語による全称量子化
### 自分の解答(x)
```sql
SELECT *
	FROM Projects P1
	WHERE ALL (SELECT )	
```

### 解答
全ての行について○がついたプロジェクトを選択する
```sql
SELECT *
  FROM Projects P1
  WHERE '○' = ALL 
		(SELECT CASE WHEN step_nbr <= 1
					AND status = '完了' THEN '○'
					 WHEN step_nbr > 1
					AND status = '待機' THEN '○'
					ELSE 'x' END
			FROM Projects P2
			WHERE P1.project_id = P2.project_id);
```

## 5-3 素数を求める
TODO