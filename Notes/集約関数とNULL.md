# 集約関数とNULL
```sql
SELECT *
	FROM Class_A
  WHERE age < ( SELECT AVG(age)
				  FROM Class_B
			     WHERE city = '東京');
```
この場合で東京の生徒がいない場合は、AVG関数はNULLを返す。SUM関数なども同様。