- オンプレミスとAWSの間を[[IPSec]]および[[VPN]]接続するサービス
- [[AWS Direct Connect]]よりもスループットや品質が低下するが、比較的低コストで短期間で導入できる。
	- Direct Connectを主回線として、Site-to-Site VPNを障害発生時の回線とする方法もある

- [冗長な Site-to-Site VPN 接続を使用してフェイルオーバーを提供する - AWS Site-to-Site VPN](https://docs.aws.amazon.com/ja_jp/vpn/latest/s2svpn/vpn-redundant-connection.html)