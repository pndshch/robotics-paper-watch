# World Model (世界モデル)

環境の遷移・物理を学習する生成モデル。Model-based RL や合成データ生成に使われる。

---

## 論文インデックス

| 論文 | 著者 | 発表 | ポイント | 週次ノート |
|---|---|---|---|---|
| [DreamerV3](https://arxiv.org/abs/2301.04104) | Hafner et al. (DeepMind) | arXiv 2023 | RSSM ベース。単一アルゴリズムで多ドメイン SOTA | [W18](../weekly/2026-W18.md) |
| [UniSim](https://arxiv.org/abs/2310.06114) | Yang et al. (Berkeley) | ICLR 2024 | 行動条件付き動画生成でインタラクティブシミュレーター | [W18](../weekly/2026-W18.md) |
| [SWIM](https://arxiv.org/abs/2311.02673) | Hu et al. (Wayve) | arXiv 2023 | 自動運転向け大規模世界モデル | [W18](../weekly/2026-W18.md) |

---

## トレンド・まとめ

- **潜在 vs ピクセル:** DreamerV3 が潜在空間で世界モデル学習。UniSim はピクセル動画生成
- **スケーリング:** 大規模動画生成 (Sora 的アプローチ) で高品質シミュレーションへ
- **ロボット応用:** UniSim のように行動条件付きで「ロボットの行動→次の観測」を生成する方向が有望
- **RL との接続:** DreamerV3 は Model-based RL の SOTA。潜在空間の想像上のロールアウトで学習

## 関連

- [RL](reinforcement-learning.md): Model-based RL (DreamerV3) はここの延長
- [VLA](vla.md): UniSim のような行動条件付き世界モデルは VLA の評価環境としても使える
