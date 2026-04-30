# E2E / Imitation Learning (End-to-End ロボット学習)

センサ入力から行動出力まで一貫して学習するアプローチ。模倣学習・行動クローニングを中心に扱う。

---

## 論文インデックス

| 論文 | 著者 | 発表 | ポイント | 週次ノート |
|---|---|---|---|---|
| [ACT](https://arxiv.org/abs/2304.13705) | Zhao et al. (Stanford) | RSS 2023 | Action Chunking + CVAE。精密手先作業での模倣学習基盤 | [W18](../weekly/2026-W18.md) |
| [ALOHA](https://arxiv.org/abs/2304.13705) | Zhao et al. (Stanford) | RSS 2023 | 安価ハードウェアで両腕マニピュレーション | [W18](../weekly/2026-W18.md) |
| [HPT](https://arxiv.org/abs/2409.20537) | Wang et al. (MIT) | arXiv 2024-09 | 異種ロボット共有 Trunk。Stem/Head 交換で適応 | [W18](../weekly/2026-W18.md) |
| [RoboAgent](https://arxiv.org/abs/2309.01918) | Bharadhwaj et al. (CMU) | ICRA 2024 | MT-ACT + Semantic augmentation。18 デモで 38 タスク汎化 | [W18](../weekly/2026-W18.md) |

---

## トレンド・まとめ

- **Action Chunking:** ACT を起点に「N ステップ先を一括予測」が主流手法のひとつに
- **スケーリング:** 多ロボット・多タスクデータの統合 (HPT, Octo) が焦点
- **データ効率:** 少数デモから汎化する手法 (RoboAgent, MimicGen) が実用上重要
- **ハードウェア:** ALOHA 系の低コスト両腕セットアップが普及し研究の民主化が進む
