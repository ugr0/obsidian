- KMSの暗号化を設定することで以降は透過的に暗号化状態になる
- コンソールから作成 -> デフォルトで暗号化される
- CLI -> 暗号化が有効にならない

# 暗号化の強制
- [[IAMポリシー]]の「condition」の「elasticfilesystem:Encrypted」を使う
- [[AWS Organizations]]の[[SCP]]により組織全体として暗号化を強制する