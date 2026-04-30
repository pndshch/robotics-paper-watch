# Foundations — 基礎論文ライブラリ (〜2025年)

週次ウォッチの比較基準となる論文群。新しい論文を読む際に「何と比べているか」を確認するための参照先。

---

## Policy Learning

### 行動表現・アーキテクチャ

| 論文 | 著者 | 発表 | 何が基準になっているか |
|---|---|---|---|
| [Diffusion Policy](https://arxiv.org/abs/2303.04137) | Chi et al. (Columbia) | RSS 2023 | DDPM による行動生成。マルチモーダル分布を扱える点が強み。多くの後継研究が "vs DP" で比較 |
| [ACT](https://arxiv.org/abs/2304.13705) | Zhao et al. (Stanford) | RSS 2023 | Action Chunking + CVAE。精密手先作業での IL 基盤。ALOHA と一緒に引用される |
| [3D Diffusion Policy (DP3)](https://arxiv.org/abs/2403.03954) | Ze et al. (PKU) | RSS 2024 | 点群 + DP。カメラ視点変化への頑健性で基準になる |
| [Consistency Policy](https://arxiv.org/abs/2405.07503) | Prasad et al. (CMU) | RSS 2024 | Diffusion Policy の高速版。1ステップ推論で実時間制御可能 |

### Foundation Models (大規模事前学習ポリシー)

| 論文 | 著者 | 発表 | 何が基準になっているか |
|---|---|---|---|
| [RT-2](https://arxiv.org/abs/2307.15818) | Zitkovich et al. (Google) | CoRL 2023 | VLM を行動トークンで fine-tune する VLA の原点。「ウェブ知識をロボットへ」というコンセプトの始祖 |
| [OpenVLA](https://arxiv.org/abs/2406.09246) | Kim et al. (Stanford) | arXiv 2024 | 公開 VLA のデファクトスタンダード。LoRA で新ロボットに適応可能 |
| [π0](https://arxiv.org/abs/2410.24164) | Black et al. (Physical Intelligence) | arXiv 2024 | PaliGemma + Flow Matching。複雑手先タスクでの VLA SOTA |
| [Octo](https://arxiv.org/abs/2405.12213) | Ghosh et al. (Berkeley) | RSS 2024 | マルチロボット汎用ポリシー。OXE データで事前学習 |
| [HPT](https://arxiv.org/abs/2409.20537) | Wang et al. (MIT) | arXiv 2024 | 異種ロボット共有 Trunk。Stem/Head 交換で新ロボットに適応 |
| [RDT-1B](https://arxiv.org/abs/2410.07864) | Liu et al. (Tsinghua) | arXiv 2024 | 1B パラメータ Diffusion Transformer。両腕操作用大規模基盤モデル |

### データ・模倣学習

| 論文 | 著者 | 発表 | 何が基準になっているか |
|---|---|---|---|
| [ALOHA](https://arxiv.org/abs/2304.13705) | Zhao et al. (Stanford) | RSS 2023 | 低コスト両腕ハードウェア。コスト・アクセシビリティの標準となった |
| [MimicGen](https://arxiv.org/abs/2310.17596) | Mandlekar et al. (NVIDIA) | CoRL 2023 | 少数デモから大規模デモを自動生成。シミュレーションデータ拡張の基準手法 |
| [RoboAgent](https://arxiv.org/abs/2309.01918) | Bharadhwaj et al. (CMU) | ICRA 2024 | MT-ACT + Semantic augmentation。少数デモ汎化の比較基準 |

---

## Reinforcement Learning

| 論文 | 著者 | 発表 | 何が基準になっているか |
|---|---|---|---|
| [Eureka](https://arxiv.org/abs/2310.12931) | Ma et al. (NVIDIA) | ICLR 2024 | LLM が報酬関数を自動設計。報酬設計の自動化研究の起点 |
| [DrEureka](https://arxiv.org/abs/2406.01967) | Ma et al. (NVIDIA) | RSS 2024 | DR パラメータ + 報酬を LLM が同時最適化。Sim-to-Real 自動化の基準 |
| [SERL](https://arxiv.org/abs/2401.16013) | Luo et al. (Berkeley) | ICRA 2024 | SAC + デモ初期化。実機 RL を数時間に短縮した基盤フレームワーク |
| [HIL-SERL](https://arxiv.org/abs/2410.21845) | Luo et al. (Berkeley) | arXiv 2024 | SERL にリアルタイム人間介入を追加。実機 RL の現時点の SOTA フレームワーク |

---

## World Model & Sim

| 論文 | 著者 | 発表 | 何が基準になっているか |
|---|---|---|---|
| [DreamerV3](https://arxiv.org/abs/2301.04104) | Hafner et al. (DeepMind) | arXiv 2023 | RSSM ベース。Model-based RL の多ドメイン SOTA |
| [UniSim](https://arxiv.org/abs/2310.06114) | Yang et al. (Berkeley) | ICLR 2024 | 行動条件付き動画生成でインタラクティブシミュレーター |

---

## Sensing & Perception

| 論文 | 著者 | 発表 | 何が基準になっているか |
|---|---|---|---|
| [Sparsh](https://arxiv.org/abs/2410.24090) | Higuera et al. (Meta) | CoRL 2024 | 触覚版 Foundation Model。複数センサ対応の自己教師あり事前学習 |
| [TacSL](https://arxiv.org/abs/2408.06506) | Qi et al. (NVIDIA) | arXiv 2024 | IsaacGym ベース触覚シミュレーション。触覚 Sim-to-Real の起点 |
| [UniTouch](https://arxiv.org/abs/2309.14972) | Yang et al. (Columbia) | CoRL 2023 | 視覚・触覚・音声の統合潜在空間。クロスモーダル触覚表現の基準 |
| [AnyGrasp](https://arxiv.org/abs/2212.08333) | Fang et al. (Tsinghua) | T-RO 2023 | GraspNet-1B で学習した汎用把持推定。把持のデファクトベースライン |
| [DP3](https://arxiv.org/abs/2403.03954) | Ze et al. (PKU) | RSS 2024 | 点群 + Diffusion Policy。3D 視覚の頑健性の基準 |
