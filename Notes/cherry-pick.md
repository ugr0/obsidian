- [Git - git-cherry-pick Documentation](https://git-scm.com/docs/git-cherry-pick)
- [cherry-pick 運用の地獄から這い上がった話をしよう](https://zenn.dev/noraworld/articles/cherry-pick-operation#%E3%81%AF%E3%81%98%E3%82%81%E3%81%AB)

# マージコミットをcherry-pickする記事
- [git翻訳後記(1) - cherry-pick - ブログのおんがえし](https://ongaeshi.hatenablog.com/entry/20100404/1270374998) 
- `git cherry-pick -m 1 コミットハッシュ`
	- マージコミットは、そのコミットの親が複数（マージ元、マージ先）あるので、そのままでは適用できない。
	- 適用するときにどちらの親を選ぶか、それを指定するのが`-m`オプション。親コミットを選択して、親コミットとマージコミットの差分を適用する。
	- `-m`オプションは数値を指定する。値は1から始まるが、その値は`git log`の`Merge`ヘッダの表示順に対応する。

# Points to remember
- git cherry-pick <commit-hash>  to cherry-pick a commit from another branch