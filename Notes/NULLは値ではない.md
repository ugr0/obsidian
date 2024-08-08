なぜ「＝NULL」ではなく、「IS NULL」と書く必要があるのか。
	- NULLに比較述語を適用した結果は、常にunknownになる。
	- RDBにおいて、NULLは値ではないことに注意。
- 以下の式は全部unknownになる。
```
1 = NULL
2 > NULL
3 < NULL
4 <> NULL
NULL = NULL
NULL > NULL
NULL < NULL
NULL <> NULL
```
- NULLは「そこに値がない」ことを示すただの視覚的マーク、目印。

真理値unknownとは別に、NULLの一種のUNKNOWNがあるので注意。

```sql
unknown = unknown -- true(真理値の比較)

UNKNOWN = UNKNOWN -- false(NULL = NULL)
```
