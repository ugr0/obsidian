- ネットワークレイヤーとトランスポートレイヤー (レイヤー 3 と 4)、およびアプリケーションレイヤー (レイヤー 7) の AWS のリソースのために、「Distributed Denial of Service (DDoS) 攻撃」に対する保護を提供します
- 自動的に適用される無料のStandardと有償のAdvancedの2種類ある。
- [[AWS Shield Standard]]
- AWS Shield Advanced
	- 対象リソースのトラフィックを分析し、正常パターンを定義したベースラインを作る。
	- [[アノマリー型検知]]を行う
	- DDos対策チーム(SRT)のサポートを365日24時間受けられる
	- DDoSによってオートスケールしてスケールアップした利用料の増加分に対しては調整リクエストを出すことができる
	- 追加料金なしで[[AWS WAF]]を利用可能


- [AWS Shield の仕組み - AWS WAF、AWS Firewall Manager、および AWS Shield Advanced](https://docs.aws.amazon.com/ja_jp/waf/latest/developerguide/ddos-overview.html#ddos-advanced)