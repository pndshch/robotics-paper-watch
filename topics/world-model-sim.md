# World Model & Sim

環境ダイナミクスのモデリング。計画・合成データ生成・Sim-to-Real インフラに使われる。「何が次に起こるか」を学ぶという意味でポリシー学習とは目的が異なる。

---

## 論文インデックス

### 世界モデル (学習)

| 論文 | 著者 | 発表 | ポイント |
|---|---|---|---|
| [DreamerV3](https://arxiv.org/abs/2301.04104) | DeepMind | 2023 | RSSM。Model-based RL の多ドメイン SOTA |
| [UniSim](https://arxiv.org/abs/2310.06114) | Berkeley | ICLR 2024 | 行動条件付き動画生成でインタラクティブシミュ |

### 世界モデル (応用・実用化)

| 論文 | 著者 | 発表 | ポイント |
|---|---|---|---|
| [Hi-WM](https://arxiv.org/abs/2604.21741) | Li et al. | 2026-04 | 世界モデル内で人間介入。ポスト学習に活用 |
| [Cortex 2.0](https://arxiv.org/abs/2604.20246) | Aida et al. | 2026-04 | 産業ロボット向け。候補生成→スコアリング→実行 |
| [ViVa](https://arxiv.org/abs/2604.08168) | Lv et al. | 2026-04 | 動画生成モデルを RL の価値推定に転用 |

### シミュレーション・データ生成

| 論文 | 著者 | 発表 | ポイント |
|---|---|---|---|
| [MimicGen](https://arxiv.org/abs/2310.17596) | NVIDIA | CoRL 2023 | 少数デモ → 自動大規模データ生成 |
| [TacSL](https://arxiv.org/abs/2408.06506) | NVIDIA | 2024 | IsaacGym ベース触覚シミュ |
| [ETac](https://arxiv.org/abs/2604.20295) | Xu et al. | 2026-04 | 触覚シミュ 869 FPS。RL との統合が現実的な速度 |

---

## 用途別の整理

| 用途 | 代表論文 | 何に使うか |
|---|---|---|
| Model-based RL | DreamerV3 | 潜在空間でのロールアウトで方策学習 |
| データ生成 | MimicGen | 実環境でのデータ収集を代替 |
| 計画 | Cortex 2.0 | 実行前に候補を生成・評価 |
| ポスト学習 | Hi-WM | 学習済みポリシーを安全に改善 |
| Sim2Real | TacSL, ETac | 触覚など実機コストの高いセンサを Sim で事前学習 |
