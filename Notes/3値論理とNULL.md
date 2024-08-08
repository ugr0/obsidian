[SQL](SQL.md)は3値論理(true, false, unknown)が採用されている。それは、NULLをRDBに採用しているから。

# 要点
1. [NULLは値ではない](NULL%E3%81%AF%E5%80%A4%E3%81%A7%E3%81%AF%E3%81%AA%E3%81%84.md)
2. 値ではないので、述語もまともに適用できない。
3. 無理やり適用するとunknownが生じる。
4. unknownが論理演算に紛れ込むと、SQLが直感に反する動作をする。
5. これに対処するには、段階的なステップに分けてSQLの動作を追うことが有効。

# Contents
- [3値論理の真理値表](3%E5%80%A4%E8%AB%96%E7%90%86%E3%81%AE%E7%9C%9F%E7%90%86%E5%80%A4%E8%A1%A8.md)
- [比較述語とNULL 排中律が成立しない](比較述語とNULL%20排中律が成立しない.md)
- [比較述語とNULL CASE式とNULL](%E6%AF%94%E8%BC%83%E8%BF%B0%E8%AA%9E%E3%81%A8NULL%20CASE%E5%BC%8F%E3%81%A8NULL.md)
- [NOT INとNOT EXISTSは同値ではない](NOT%20INとNOT%20EXISTSは同値ではない.md)
- [限定述語とNULL](%E9%99%90%E5%AE%9A%E8%BF%B0%E8%AA%9E%E3%81%A8NULL.md)
- [限定述語と極値関数は同値ではない](%E9%99%90%E5%AE%9A%E8%BF%B0%E8%AA%9E%E3%81%A8%E6%A5%B5%E5%80%A4%E9%96%A2%E6%95%B0%E3%81%AF%E5%90%8C%E5%80%A4%E3%81%A7%E3%81%AF%E3%81%AA%E3%81%84.md)
- [集約関数とNULL](%E9%9B%86%E7%B4%84%E9%96%A2%E6%95%B0%E3%81%A8NULL.md)

# 参考資料
-  [📚達人に学ぶSQL徹底指南書第２版](%F0%9F%93%9A%E9%81%94%E4%BA%BA%E3%81%AB%E5%AD%A6%E3%81%B6SQL%E5%BE%B9%E5%BA%95%E6%8C%87%E5%8D%97%E6%9B%B8%E7%AC%AC%EF%BC%92%E7%89%88.md)
- [3値論理とNULL (1/3)|CodeZine（コードジン）](https://codezine.jp/article/detail/532)