## 区間DPとは
- `dp[i][j]` = 区間`[i, j)`の最適解、みたいなDPをするやつ 
- 区間DPのよくある方針として`dp[L][R]`を`dp[L+1][R]`と`dp[L][R-1]`を使って更新する方針がある
## 参考記事
- [区間DP - 個人的な競プロメモ](https://scrapbox.io/pocala-kyopro/%E5%8C%BA%E9%96%93DP)
- [競技プログラミングにおける区間DP問題まとめ - はまやんはまやんはまやん](https://blog.hamayanhamayan.com/entry/2017/02/27/152226)