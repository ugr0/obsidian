Relational DataBase Management System。[[RDB]]を管理するシステム。


## RDBの作成時刻や更新時刻について
[RDBの作成時刻や更新時刻用カラムに関するプラクティス | おそらくはそれさえも平凡な日々](https://songmu.jp/riji/entry/2019-10-21-created_at-update_at.html)

## RDBMSの内部動作を知る方法
PLANコマンドを実行する。

# データ型
TIMESTAMPとDATETIME
- 時間がTIMESTAMPはUTCに統一してくれる。
- TIMESTAMPは、2038年問題がある。
- [Postgres と MySQL における id, created_at, updated_at に関するベストプラクティス](https://zenn.dev/mpyw/articles/rdb-ids-and-timestamps-best-practices)