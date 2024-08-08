# 指定日からのマージコミットを抽出する
```
$ git log --since=2020-01-01 --merges --pretty=format:"%s" | grep "Merge" | sort | uniq
```
- [【Git】指定日からのマージコミットを抽出する #Git - Qiita](https://qiita.com/K-Shuuun/items/38d54665cd45ba3b9b7f)