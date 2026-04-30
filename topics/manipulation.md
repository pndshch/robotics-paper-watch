# Robot Manipulation (ロボットマニピュレーション)

把持・操作・組み立てなど、ロボットが物体を操る技術全般。

---

## 論文インデックス

| 論文 | 著者 | 発表 | ポイント | 週次ノート |
|---|---|---|---|---|
| [MimicGen](https://arxiv.org/abs/2310.17596) | Mandlekar et al. (NVIDIA) | CoRL 2023 | 少数デモから大規模デモを自動生成するデータ拡張 | [W18](../weekly/2026-W18.md) |
| [RoboAgent](https://arxiv.org/abs/2309.01918) | Bharadhwaj et al. (CMU) | ICRA 2024 | MT-ACT + Semantic augmentation で少数デモ汎化 | [W18](../weekly/2026-W18.md) |
| [AnyGrasp](https://arxiv.org/abs/2212.08333) | Fang et al. (Tsinghua) | T-RO 2023 | GraspNet-1B で学習した汎用把持姿勢推定 | [W18](../weekly/2026-W18.md) |
| [ACT / ALOHA](https://arxiv.org/abs/2304.13705) | Zhao et al. (Stanford) | RSS 2023 | 精密両腕マニピュレーションの模倣学習 | [W18](../weekly/2026-W18.md) |

---

## トレンド・まとめ

- **データスケール:** MimicGen 等の自動データ生成でシミュレーションデータが爆増
- **Sim-to-Real:** シミュレーションからの転移が中心課題。Diffusion Policy や RL がブリッジ
- **両腕・器用性:** ALOHA 系の低コスト両腕セットアップで器用な操作研究が活発化
- **把持の汎化:** AnyGrasp のように大規模データで事前学習した把持推定器が実用化

## サブトピック

- **Grasping:** AnyGrasp, GraspNet
- **Bimanual:** ALOHA, RDT-1B, ACT
- **Data Generation:** MimicGen
- **Dexterous Hand:** π0, 後続論文を追う
