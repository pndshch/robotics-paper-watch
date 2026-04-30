# Reinforcement Learning (ロボティクス向け強化学習)

実機・シミュレーションでの RL。報酬設計・サンプル効率・Sim-to-Real が主な課題。

---

## 論文インデックス

| 論文 | 著者 | 発表 | ポイント | 週次ノート |
|---|---|---|---|---|
| [Eureka](https://arxiv.org/abs/2310.12931) | Ma et al. (NVIDIA) | ICLR 2024 | LLM (GPT-4) が報酬関数を自動設計・改善 | [W18](../weekly/2026-W18.md) |
| [DrEureka](https://arxiv.org/abs/2406.01967) | Ma et al. (NVIDIA) | RSS 2024 | LLM が DR パラメータと報酬を同時最適化 | [W18](../weekly/2026-W18.md) |
| [SERL](https://arxiv.org/abs/2401.16013) | Luo et al. (Berkeley) | ICRA 2024 | SAC + デモ初期化で実機 RL を 1〜3 時間に短縮 | [W18](../weekly/2026-W18.md) |
| [HIL-SERL](https://arxiv.org/abs/2410.21845) | Luo et al. (Berkeley) | arXiv 2024-10 | RL ループへのリアルタイム人間介入 | [W18](../weekly/2026-W18.md) |

---

## トレンド・まとめ

- **報酬設計の自動化:** Eureka → DrEureka で LLM が報酬と DR を書く時代に
- **実機 RL の現実化:** SERL / HIL-SERL で実機での RL が数時間で完了するようになった
- **Sim-to-Real:** DR + LLM の組み合わせが有望。DrEureka がその先端
- **IL との融合:** SERL のようにデモで RL を初期化する hybrid アプローチが主流

## 関連

- [World Model](world-model.md): Model-based RL (DreamerV3) はここと接続
