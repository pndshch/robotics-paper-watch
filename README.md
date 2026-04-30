# robotics-paper-watch

ロボティクス関連の論文を週次でウォッチするリポジトリ。

---

## ナビゲーション

| 何を見たいか | 見る場所 |
|---|---|
| 今週の最新論文 | [weekly/](weekly/) の最新ファイル |
| 今月の論文まとめ | [monthly/](monthly/) の最新ファイル |
| 2023〜2024年の基礎論文 | [foundations.md](foundations.md) |
| トピック別インデックス | [topics/](topics/) |

---

## 週次ノート (最新順)

| 週 | 期間 | ハイライト |
|---|---|---|
| [2026-W18](weekly/2026-W18.md) | 2026-04-21〜04-30 | HANDFUL, VLA Survey, Hi-WM, FingerEye, ETac ほか |

## 月次ノート

| 月 | 論文数 | ハイライト |
|---|---|---|
| [2026-04](monthly/2026-04.md) | 19本 | VLA評価研究の充実、触覚シミュの高速化、ヒューマノイド量産期 |

---

## トピック別インデックス

4カテゴリで分類する。タスクドメイン (manipulation / locomotion / etc.) は各論文のタグで管理する。

| カテゴリ | 何をカバーするか |
|---|---|
| [Policy Learning](topics/policy-learning.md) | 観測→行動のマッピングをどう学ぶか。VLA・BC・Diffusion Policy・Flow Matching・ACT など、学習パラダイムや行動表現の選択に関わる研究すべて |
| [Reinforcement Learning](topics/reinforcement-learning.md) | 報酬信号で環境と相互作用しながら学ぶ研究。報酬設計・Sim-to-Real・オンライン適応 |
| [World Model & Sim](topics/world-model-sim.md) | 環境ダイナミクスのモデリング。計画・合成データ生成・シミュレーション・Sim2Real インフラ |
| [Sensing & Perception](topics/sensing-perception.md) | ロボットが何をどう知覚するか。触覚センサ・3D視覚・マルチモーダル表現学習 |

> **なぜこの4分類か**
> 「VLA」「E2E」「Diffusion Policy」「Manipulation」を別カテゴリにしていたが、VLA・Diffusion Policy・ACT はすべて Policy Learning の異なるアーキテクチャ選択に過ぎない。Manipulation はタスクドメインであり、研究カテゴリではない。意味のある軸で分類し直した。

---

## 週次更新の依頼フォーマット

```
「今週のロボティクス論文を調査して、robotics-paper-watch リポジトリに追記してください。
arXiv の cs.RO / cs.LG を中心に、以下のトピックで新着論文を探してください:
Policy Learning (VLA/IL/DP), RL, World Model/Sim, Sensing/Tactile

weekly/YYYY-WXX.md を新規作成し、monthly/YYYY-MM.md に追記、
関連する topics/ も更新して push してください。」
```
