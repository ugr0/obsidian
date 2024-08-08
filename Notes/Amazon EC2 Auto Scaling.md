- Amazon EC2 Auto Scaling は、アプリケーションの負荷を処理するために適切な数の Amazon EC2 インスタンスを利用できるようにします。
- Auto Scaling グループと呼ばれる EC2 インスタンスの集合を作成します。
- 複数のリージョンにインスタンスを含めることはできない。
- 同じリージョンの複数のAZにならインスタンスを含めることができる。

# 簡易スケーリングポリシー
- ステップスケーリングおよび簡易スケーリングでは、スケーリングプロセスを呼び出す CloudWatch アラームのスケーリングメトリクスとしきい値を選択
- [Amazon EC2 Auto Scaling のステップおよび簡易スケーリングポリシー - Amazon EC2 Auto Scaling](https://docs.aws.amazon.com/ja_jp/autoscaling/ec2/userguide/as-scaling-simple-step.html)

# ウォームプール
- インスタンスが大量のデータをディスクに書き込む必要があるなど、起動時間が非常に長いアプリケーションのレイテンシーを低減できる
- [Amazon EC2 Auto Scaling のウォームプール - Amazon EC2 Auto Scaling](https://docs.aws.amazon.com/ja_jp/autoscaling/ec2/userguide/ec2-auto-scaling-warm-pools.html)
- [EC2 AutoScaling WarmPool速度検証 | TECH BLOG | NRI Digital](https://www.nri-digital.jp/tech/20210608-5037/#:~:text=%E5%88%9D%E6%9C%9F%E5%8C%96%E6%B8%88%E3%81%BF%E3%81%AEEC2%E3%82%A4%E3%83%B3%E3%82%B9%E3%82%BF%E3%83%B3%E3%82%B9%E3%82%92%E8%A8%AD%E5%AE%9A%E6%95%B0%E5%88%86Pool%E3%81%AB%E4%BF%9D%E6%8C%81%E3%81%97%E3%81%A6%E3%81%8A%E3%81%8D%E3%80%81%E8%BF%85%E9%80%9F%E3%81%AB%E3%82%B9%E3%82%B1%E3%83%BC%E3%83%AA%E3%83%B3%E3%82%B0%E3%82%92%E5%AE%8C%E4%BA%86%E3%81%99%E3%82%8B%E3%81%93%E3%81%A8%E3%81%8C%E3%81%A7%E3%81%8D%E3%81%BE%E3%81%99%E3%80%82)

# スケールイン

# クールダウン
- Auto Scalingが連続で実行されないようにAuto Scalingの待ち時間を設定する機能

# ライフサイクルフック
- Auto ScalingによるEC2インスタンスの起動または終了を一時的に待機させて、指定したアクションを実行する

# 資料
- [Amazon EC2 Auto Scaling とは - Amazon EC2 Auto Scaling](https://docs.aws.amazon.com/ja_jp/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html)
- [アベイラビリティーゾーンを追加および削除する - Amazon EC2 Auto Scaling](https://docs.aws.amazon.com/ja_jp/autoscaling/ec2/userguide/as-add-availability-zone.html)