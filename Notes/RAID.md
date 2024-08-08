Redundant Array of Independent Disksの略。独立したディスクの冗長配列という意味。
(Redundant Array of Inexpensive Disksの略とも言われており、この場合だと安いディスクの冗長配列という意味。)

- 複数のディスクを束ねて仮想的に１つのストレージとする技術。
- 単位でまとめられたディスクをRAIDグループという。
- 基本的には、複数のディスクに同じデータを書き込んで冗長化することで、そのうちの一本が壊れても残りのディ数が生きていればデータを保全できるようにするというもの。
- システムの信頼性（可用性）だけではなく、性能向上も改善できる。(ディスクI/Oを分散する)

# RAIDの種類
- [RAID0](RAID0.md)
- [RAID1](RAID1.md)
- [RAID5](RAID5.md)
- [RAID10](RAID10.md)
- [RAID6](RAID6.md)