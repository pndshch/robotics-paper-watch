# VLA (Vision-Language-Action Models)

大規模言語/視覚モデルをロボット行動生成に応用する研究領域。

---

## 論文インデックス

| 論文 | 著者 | 発表 | ポイント | 週次ノート |
|---|---|---|---|---|
| [RT-2](https://arxiv.org/abs/2307.15818) | Zitkovich et al. (Google) | CoRL 2023 | VLM を行動トークンで fine-tune した VLA の原点 | [W18](../weekly/2026-W18.md) |
| [OpenVLA](https://arxiv.org/abs/2406.09246) | Kim et al. (Stanford) | arXiv 2024-06 | フル公開 VLA。LoRA fine-tune で新ロボットに適応 | [W18](../weekly/2026-W18.md) |
| [π0](https://arxiv.org/abs/2410.24164) | Black et al. (Physical Intelligence) | arXiv 2024-10 | PaliGemma + flow matching。複雑手先タスクで SOTA | [W18](../weekly/2026-W18.md) |
| [Octo](https://arxiv.org/abs/2405.12213) | Ghosh et al. (Berkeley) | RSS 2024 | マルチロボット汎用ポリシー。OXE データで学習 | [W18](../weekly/2026-W18.md) |
| [GR-1](https://arxiv.org/abs/2312.13139) | Wu et al. | ICLR 2024 | 動画生成事前学習をロボット制御に転用 | [W18](../weekly/2026-W18.md) |

---

## トレンド・まとめ

- **スケーリング:** RT-2 → OpenVLA → π0 と規模が拡大。VLM の pre-training が行動汎化に効く
- **行動表現:** 離散トークン化 (RT-2, OpenVLA) vs 連続フロー (π0) の 2 流派
- **オープン化:** OpenVLA・Octo により再現実験が容易になった
- **次の課題:** 長時間タスク・触覚統合・リアルタイム性能
