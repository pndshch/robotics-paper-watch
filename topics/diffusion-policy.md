# Diffusion Policy (拡散モデルベース行動生成)

行動生成にノイズ除去拡散モデルを使うアプローチ。マルチモーダルな行動分布を扱える。

---

## 論文インデックス

| 論文 | 著者 | 発表 | ポイント | 週次ノート |
|---|---|---|---|---|
| [Diffusion Policy](https://arxiv.org/abs/2303.04137) | Chi et al. (Columbia) | RSS 2023 | ロボット行動生成への DDPM 導入。基盤論文 | [W18](../weekly/2026-W18.md) |
| [3D Diffusion Policy (DP3)](https://arxiv.org/abs/2403.03954) | Ze et al. (PKU) | RSS 2024 | 点群観測 + Diffusion Policy。カメラ視点変化に頑健 | [W18](../weekly/2026-W18.md) |
| [Consistency Policy](https://arxiv.org/abs/2405.07503) | Prasad et al. (CMU) | RSS 2024 | Consistency Distillation で 10〜50x 高速推論 | [W18](../weekly/2026-W18.md) |
| [RDT-1B](https://arxiv.org/abs/2410.07864) | Liu et al. (Tsinghua) | arXiv 2024-10 | 1B パラメータ Diffusion Transformer。両腕操作用基盤モデル | [W18](../weekly/2026-W18.md) |

---

## トレンド・まとめ

- **品質 vs 速度:** Diffusion Policy は精度が高いが推論が遅い。Consistency Policy など高速化手法が活発
- **3D 観測:** DP3 が示すように点群入力で汎化性が大幅向上
- **スケーリング:** RDT-1B のように大規模化する方向と、軽量高速化する方向が並行
- **Flow Matching との関係:** π0 は Flow Matching で類似の効果を達成。収束も速い傾向

## 関連

- [VLA → π0](vla.md): Flow Matching ベースの VLA と比較するとアーキテクチャの選択肢が見えやすい
