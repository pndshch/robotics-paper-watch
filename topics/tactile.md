# Tactile (触覚センシング・触覚表現学習)

触覚センサからの情報活用。把持安定性・材質判定・精密操作への応用。

---

## 論文インデックス

| 論文 | 著者 | 発表 | ポイント | 週次ノート |
|---|---|---|---|---|
| [Sparsh](https://arxiv.org/abs/2410.24090) | Higuera et al. (Meta) | CoRL 2024 | 触覚版 foundation model。複数センサ対応の自己教師あり事前学習 | [W18](../weekly/2026-W18.md) |
| [TacSL](https://arxiv.org/abs/2408.06506) | Qi et al. (NVIDIA) | arXiv 2024-08 | IsaacGym ベース触覚シミュレーション。Sim-to-Real 対応 | [W18](../weekly/2026-W18.md) |
| [UniTouch](https://arxiv.org/abs/2309.14972) | Yang et al. (Columbia) | CoRL 2023 | 視覚・触覚・音声の統合表現空間 | [W18](../weekly/2026-W18.md) |

---

## 代表的なセンサ

| センサ | 開発元 | 特徴 |
|---|---|---|
| GelSight / GelSight Wedge | MIT | 高解像度触覚画像。研究用標準 |
| DIGIT | Meta FAIR | 小型・安価。Sparsh と相性良い |
| Tactip | Bristol | ソフトバンパー型 |
| F/T Sensor (ATI 等) | 各社 | 力・トルク計測の基本センサ |

---

## トレンド・まとめ

- **Foundation Model 化:** Sparsh が示すように、大規模事前学習 + downstream fine-tune が触覚にも波及
- **Sim-to-Real:** TacSL のように触覚をシミュレーションで学習して実機転移する方向が発展中
- **マルチモーダル統合:** UniTouch のように視触覚・音を統合した表現学習が活発
- **VLA との統合:** 視覚・言語・触覚を一体で扱う VLA はまだ少ない。次のフロンティア

## 関連

- [Manipulation](manipulation.md): 把持安定性・精密操作に触覚が直接貢献
- [VLA](vla.md): 触覚トークンを VLA に統合する研究が今後増える予想
