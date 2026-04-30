# Policy Learning

「観測→行動のマッピングをどう学ぶか」に関わる研究。VLA・Diffusion Policy・ACT・BC はすべてここに入る。アーキテクチャ選択 (LLM ベース / 拡散モデル / CVAE) や学習データの種類が主な差分軸。

---

## 論文インデックス

### Foundation Models / VLA

| 論文 | 著者 | 発表 | ポイント |
|---|---|---|---|
| [RT-2](https://arxiv.org/abs/2307.15818) | Google | CoRL 2023 | VLM → 行動トークン fine-tune の原点 |
| [OpenVLA](https://arxiv.org/abs/2406.09246) | Stanford | 2024 | 公開 VLA のデファクト。LoRA で新ロボット適応 |
| [π0](https://arxiv.org/abs/2410.24164) | Physical Intelligence | 2024 | PaliGemma + Flow Matching。手先タスク SOTA |
| [Octo](https://arxiv.org/abs/2405.12213) | Berkeley | RSS 2024 | マルチロボット汎用ポリシー |
| [HPT](https://arxiv.org/abs/2409.20537) | MIT | 2024 | 異種ロボット共有 Trunk |
| [RDT-1B](https://arxiv.org/abs/2410.07864) | Tsinghua | 2024 | 1B Diffusion Transformer、両腕操作用基盤 |
| [DeFI](https://arxiv.org/abs/2604.16391) | Zhang et al. | ICLR 2026 | 前向き/逆向きダイナミクス分離事前学習 |
| [ReFineVLA](https://arxiv.org/abs/2604.17800) | Vo et al. | 2026-04 | 推論根拠でVLAをfine-tune。SimplerEnv SOTA |
| [UniT](https://arxiv.org/abs/2604.19734) | XPeng Robotics | 2026-04 | 人間→ヒューマノイドゼロショット転移 |

### 行動表現・生成モデル

| 論文 | 著者 | 発表 | ポイント |
|---|---|---|---|
| [Diffusion Policy](https://arxiv.org/abs/2303.04137) | Columbia | RSS 2023 | DDPM による行動生成。マルチモーダル分布対応 |
| [ACT](https://arxiv.org/abs/2304.13705) | Stanford | RSS 2023 | Action Chunking + CVAE。精密手先作業の IL 基盤 |
| [3D Diffusion Policy](https://arxiv.org/abs/2403.03954) | PKU | RSS 2024 | 点群 + DP。視点変化に頑健 |
| [Consistency Policy](https://arxiv.org/abs/2405.07503) | CMU | RSS 2024 | DP を 10〜50x 高速化 |
| [Action Images](https://arxiv.org/abs/2604.06168) | Zhen et al. | 2026-04 | 行動をマルチビュー動画生成として定式化 |

### データ・模倣学習

| 論文 | 著者 | 発表 | ポイント |
|---|---|---|---|
| [ALOHA](https://arxiv.org/abs/2304.13705) | Stanford | RSS 2023 | 低コスト両腕ハードウェア標準 |
| [MimicGen](https://arxiv.org/abs/2310.17596) | NVIDIA | CoRL 2023 | 少数デモから大規模デモを自動生成 |
| [RoboAgent](https://arxiv.org/abs/2309.01918) | CMU | ICRA 2024 | MT-ACT + Semantic augmentation |
| [LIDEA](https://arxiv.org/abs/2604.10677) | SJTU | 2026-04 | 人間動画→ロボット IL。デモの 80% を代替 |

### VLA の評価・分析

| 論文 | 著者 | 発表 | ポイント |
|---|---|---|---|
| [VLA Survey](https://arxiv.org/abs/2604.23001) | Wang et al. | TMLR 2026 | データ基盤軸でのVLA研究体系サーベイ |
| [How VLAs Work](https://arxiv.org/abs/2604.21192) | Rasouli et al. | 2026-04 | BEHAVIOR1K で安全性・頑健性を体系評価 |

---

## 設計上のキートレードオフ

| 選択 | 候補A | 候補B | 差分 |
|---|---|---|---|
| 行動表現 | 離散トークン (RT-2, OpenVLA) | 連続生成 (π0, DP) | 離散は VLM に乗りやすい。連続は精密操作に強い |
| スケール | 大型 VLM ベース (7B+) | 軽量専用 (ACT, DP) | 大型は汎化力高い、軽量は推論速度有利 |
| データ | ロボットデモのみ | ウェブ知識活用 (VLA) | VLA はゼロショット汎化が強い |
| 事前学習 | 言語/画像から転移 | ロボットデータで学習 | 転移は汎化↑、専用学習は精度↑ |
