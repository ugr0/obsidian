---
URL: https://docs.aws.amazon.com/ja_jp/AmazonRDS/latest/UserGuide/MySQL.Concepts.LocalTimeZone.html
Glasp URL: https://glasp.co/f5XC0CoKGYhSNqcjs12752ID2q02/p/9a6a14a6ce25ea021ea4
Tags: []
Last updated: 2024-08-08
---
#### Highlights & Notes

> デフォルトでは、MySQL DB インスタンスのタイムゾーンは協定世界時 (UTC) です

> パラメータグループの time_zone パラメータを設定すると、そのパラメータグループを使用しているすべての DB インスタンスとリードレプリカは、新しいローカルタイムゾーンを使用するように変更されます。

> DB インスタンスとそのリードレプリカには異なるローカルタイムゾーンを設定できます。そのためには、DB インスタンスとレプリカに異なるパラメータグループを使用し、各パラメータグループの time_zone パラメータを異なるローカルタイムゾーンに設定します。

> DB スナップショットから DB インスタンスを復元すると、ローカルタイムゾーンが UTC に設定されます。


