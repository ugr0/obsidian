---
URL: https://www.php.net/manual/ja/mysqlinfo.concepts.buffering.php
Glasp URL: https://glasp.co/f5XC0CoKGYhSNqcjs12752ID2q02/p/XrC6lWWC4r1htvhMaa8G
Tags: []
Last updated: 2024-01-18
---
#### Highlights & Notes

> つまり、クエリの結果がすぐに MySQL サーバーから PHP に転送され、 PHP プロセスのメモリ内に結果を保持し続けるということです

>  バッファモードの弱点は、結果セットが大きくなると大量にメモリを消費するということです。 結果セットへの参照がなくなるか、結果セットを明示的に解放する (リクエストを終了すると、自動的に解放されます) まではメモリ上に残り続けます。


