---
URL: https://zenn.dev/shunsuke_suzuki/articles/secure-github-actions-by-pull-request-target
Glasp URL: https://glasp.co/f5XC0CoKGYhSNqcjs12752ID2q02/p/4cjPlvSSvOI5ziDnNeb7
Tags: []
Last updated: 2023-12-14
---
#### Highlights & Notes

> pull request の base branch の最新コミットで workflow が実行されるため、 Pull Request で workflow を改竄することが出来ません。

> そのため default branch の CI でのみ強い権限を付与し、 Pull Request の CI では弱い権限しか付与しないということが可能です。

> Pull Request を作成すると改竄前の workflow の定義に基づいて workflow が実行されるはずです。また Pull Request で workflow file を削除しても workflow は実行されます。これが pull_request event との大きな違いです。


