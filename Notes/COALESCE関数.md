coalesceは、与えられた引数のうち、NULLでない最初の引数を返してくれる関数。
```sql
SELECT COALESCE('山田', '鈴木', '田中'); /* => '山田' */ 
SELECT COALESCE(NULL, '鈴木', NULL); /* => '鈴木' */ 
SELECT COALESCE(NULL, NULL, '田中'); /* => '田中' */ 
SELECT COALESCE(数値型の列, 0); /* 数値型の列の出力 NULLが格納されている場合は0を返す */
```
# 参考資料
- [SQL関数coalesceの使い方と読み方 | ⬢ Appirits spirits](https://spirits.appirits.com/doruby/8666/)
- [【SQL】COALESCEで値が「NULL」だった場合に別の値を返す - Qiita](https://qiita.com/yuta_sawamura/items/0c007c8e3ca07168c992)