# UUIDv1

-   `time_low`: 
-   `time_mid`: 
-   `time_hi_and_version`: 
-   `clk_seq_hi_res`: 
-   `clk_seq_low`: 
-   `node`: 
-   `node`: 
```
 0                   1                   2                   3
 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                          time_low                             |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|       time_mid                |         time_hi_and_version   |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|clk_seq_hi_res |  clk_seq_low  |         node (0-1)            |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                         node (2-5)                            |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
```
# UUIDv4

# UUIDv7
[UUID v6, v7, v8 : タイムスタンプでソートできる新しい UUID のドラフト仕様 - kakakakakku blog](https://kakakakakku.hatenablog.com/entry/2022/10/31/082041)

**UUID v7** はよく使われる Unix Time (32 bit) にミリ秒を追加した 48 bit を使う

例
- 018422b2-4843-7a62-935b-b4e65649de3e
- 018422b2-5013-7f02-830f-2563ce4533df
- 018422b2-57e8-79b2-8b59-d6926217a9dc

UUID v7 のフィールド構成も 128 bit 長で以下の通り．より詳細な表現はドラフト仕様を参照で！なお，ID の中に**「バージョン情報」**も含まれるため，3 ブロック目の1文字目は必ず `7` になる．

-   `unix_ts_ms`: タイムスタンプ情報 48 bit
-   `ver`: バージョン情報 4 bit
-   `rand_a`: 乱数 12 bit
-   `var`: variant 2 bit
-   `rand_b`: 乱数 62 bit
```
0                   1                   2                   3
 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                           unix_ts_ms                          |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|          unix_ts_ms           |  ver  |       rand_a          |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|var|                        rand_b                             |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                            rand_b                             |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
```
[UUIDv7 in MySQL - Itsacon's Log](https://www.itsacon.net/miscellaneous/uuidv7-in-mysql/)

# ULID

# Compact UUID
- [UUIDを少し短くするUUIDShortener - 24/7 twenty-four seven](https://blog.kishikawakatsumi.com/entry/20131031/1383235295)


# 参考
- [A Universally Unique IDentifier (UUID) URN Namespace](https://www.ietf.org/archive/id/draft-ietf-uuidrev-rfc4122bis-00.html)