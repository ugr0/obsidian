# 特徴
- ローテーション
	- [AWS Secrets Managerシークレットのローテーション - AWS Secrets Manager](https://docs.aws.amazon.com/ja_jp/secretsmanager/latest/userguide/rotating-secrets.html#rotate-secrets_how)
- シークレットを暗号化して管理しており、[[AWS KMS]]が使われている。デフォルトでKMSを使っているので、あまり意識されないが、カスタマー管理CMKを利用する場合はユーザーが指定したキーを利用できる。この場合は料金かかる。
- API呼び出しにはサービスクォーターが設けられている

# 参考
- [AWS Secrets Manager の概要 - AWS Secrets Manager](https://docs.aws.amazon.com/ja_jp/secretsmanager/latest/userguide/intro.html)