---
URL: https://docs.github.com/ja/actions/using-workflows/caching-dependencies-to-speed-up-workflows
Glasp URL: https://glasp.co/f5XC0CoKGYhSNqcjs12752ID2q02/p/llnQHowBArfRtgCxzz9I
Tags: []
Last updated: 2023-06-16
---
#### Highlights & Notes

> pull request でトリガーされたワークフロー実行によってキャッシュが作成される場合、そのキャッシュは merge ref (refs/pull/.../merge) に対して作成されます。 このため、このキャッシュのスコープは制限され、pull request の再実行によってのみ復元できます。 ベース ブランチ、またはそのベース ブランチを対象とする他の pull request では、復元できません。

> オプション 代替の復元キーを含んだ文字列。各復元キーは新しい行に配置されます。 key に対するキャッシュ ヒットが発生しない場合は、キャッシュを検索して復元するために、これらの復元キーが指定された順序で使用されます。

> pull request に対してワークフロー実行がトリガーされた場合は、ベース ブランチで作成されたキャッシュを復元することもできます (フォークされたリポジトリのベース ブランチも含む)。

> 7日間以上アクセスされていないキャッシュエントリを削除します。 保存できるキャッシュの数に制限はありませんが、リポジトリ内のすべてのキャッシュの合計サイズは制限されています (最大 10 GB)。


