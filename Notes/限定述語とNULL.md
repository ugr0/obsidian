# 限定述語とNULL
限定述語はSQLのALLやANYのこと。ANYは、INと同値なのであまり使われない。ALLは比較的よく使われる。

```sql
SELECT *
	FROM Class_A
  WHERE age < ALL ( SELECT age
						FROM Class_B
					  WHERE city = '東京');
```
上のSQLの場合は、
`Class_Bテーブルのcityが東京のレコードのageの全てよりも低いageのレコードをClass_Aテーブルから取る`SQLだが、Class_BテーブルのageがNULLだった場合に、意図しない挙動(何も選択しない)挙動になる。

- サブクエリを実行し、年齢のリストを取得
```sql
SELECT *
	FROM Class_A
  WHERE age < ALL ( 22, 23, NULL) ;
```
- ALL述語をANDで同値変換
```sql
SELECT *
	FROM Class_A
  WHERE (age < 22) AND (age < 23) AND (age < NULL);
```
- NULLに < を適用するとunknownになる
```sql
SELECT *
	FROM Class_A
  WHERE (age < 22) AND (age < 23) AND unknown;
```
- ANDにunknownがあるので、結果がtrueにならない。
```sql
SELECT *
	FROM Class_A
  WHERE false または unknown;
```