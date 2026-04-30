# Reinforcement Learning

報酬信号で環境と相互作用しながら学ぶ研究。報酬設計・Sim-to-Real・オンライン適応が主な課題。IL との主な違いは「デモ不要・報酬設計必要・実機時間コスト」。

---

## 論文インデックス

### 報酬設計の自動化

| 論文 | 著者 | 発表 | ポイント |
|---|---|---|---|
| [Eureka](https://arxiv.org/abs/2310.12931) | NVIDIA | ICLR 2024 | LLM が報酬関数を自動設計・反復改善 |
| [DrEureka](https://arxiv.org/abs/2406.01967) | NVIDIA | RSS 2024 | LLM が DR パラメータ + 報酬を同時最適化 |

### 実機 RL・サンプル効率

| 論文 | 著者 | 発表 | ポイント |
|---|---|---|---|
| [SERL](https://arxiv.org/abs/2401.16013) | Berkeley | ICRA 2024 | SAC + デモ初期化で実機 RL を 1〜3 時間に |
| [HIL-SERL](https://arxiv.org/abs/2410.21845) | Berkeley | 2024 | SERL にリアルタイム人間介入を追加 |
| [Jump-Start RL + VLA](https://arxiv.org/abs/2604.13733) | Moroncelli et al. | 2026-04 | VLA で PPO 初期化。インタラクション 50% 削減 |

### RL × 動画・世界モデル

| 論文 | 著者 | 発表 | ポイント |
|---|---|---|---|
| [DreamerV3](https://arxiv.org/abs/2301.04104) | DeepMind | 2023 | RSSM ベース Model-based RL の多ドメイン SOTA |
| [ViVa](https://arxiv.org/abs/2604.08168) | Lv et al. | 2026-04 | 事前学習済み動画生成モデルを価値推定に転用 |

### ヒューマノイド・Locomotion

| 論文 | 著者 | 発表 | ポイント |
|---|---|---|---|
| [Multi-Gait Humanoid](https://arxiv.org/abs/2604.19102) | Wu et al. | 2026-04 | 選択的 AMP で 5 種の歩容を単一 RL フレームワークで |
| [Whole-Body Humanoid Locomotion](https://arxiv.org/abs/2604.17335) | ETH × Peng | 2026-04 | Diffusion で参照動作生成 + RL 追跡。複雑地形対応 |

---

## IL との比較軸

| 観点 | RL | IL (Policy Learning) |
|---|---|---|
| 学習信号 | 報酬 (設計必要) | デモ (収集必要) |
| 実機コスト | 高 (何時間も必要) | 低〜中 (少数デモで済む) |
| 汎化性 | タスク内で最適化 | デモ分布に依存 |
| 組み合わせ | SERL = IL で初期化 + RL で改善 | — |
