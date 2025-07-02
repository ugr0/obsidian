# npmのキャッシュ
- [CI/CDでnpm ciする際は \~/.npm をキャッシュしよう | DevelopersIO](https://dev.classmethod.jp/articles/cicd-npm-ci-cache/)
- [npm install と npm ci って結局どう使うの？2023年版 - Mitsuyuki.Shiiba](https://bufferings.hatenablog.com/entry/2023/03/15/215044)
- [npm installとnpm ciの動作確認を簡単にやっておいた - Mitsuyuki.Shiiba](https://bufferings.hatenablog.com/entry/2023/03/21/145023)
- npm ciはnode_modulesを消してからlockファイルをもとにインストールを行うので、安全。
- cacheを使用する時は、.npmフォルダが作られるのでそれをキャッシュするとそのフォルダからnode_modulesフォルダへのコピーにより、単純にインストールする分のネットワーク通信時間が短縮される。しかし実際にはそこまで時間は変わらない。(3/4程度)
	- pnpmによりその辺が改善されているみたい。