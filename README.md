# robotics-paper-watch

ロボティクス関連の論文を週次でウォッチするリポジトリ。  
VLA・E2E・Diffusion Policy・Manipulation・RL・World Model・Tactile をカバー。

---

## トピックエリア

| トピック | 概要 |
|---|---|
| [VLA](topics/vla.md) | Vision-Language-Action モデル |
| [E2E](topics/e2e.md) | End-to-End ロボット学習・模倣学習 |
| [Diffusion Policy](topics/diffusion-policy.md) | 拡散モデルベースの行動生成 |
| [Manipulation](topics/manipulation.md) | ロボットマニピュレーション全般 |
| [Reinforcement Learning](topics/reinforcement-learning.md) | ロボティクス向け強化学習 |
| [World Model](topics/world-model.md) | 世界モデル・シミュレーション |
| [Tactile](topics/tactile.md) | 触覚センシング・触覚表現学習 |

---

## 週次ノート (最新順)

| 週 | 期間 | ハイライト |
|---|---|---|
| [2026-W18](weekly/2026-W18.md) | 2026-04-28〜 | キックオフ: 各トピックの重要論文を整理 |

---

## 使い方

### 論文を探すとき
- **最新トレンド** → [`weekly/`](weekly/) の最新ファイルを上から読む
- **トピックで絞る** → [`topics/`](topics/) の各ファイルのインデックスから

### 週次更新の流れ (Claude Code に依頼する場合)
```
「今週のロボティクス論文を調査して、robotics-paper-watch リポジトリに追記してください。
各トピック (VLA/E2E/Diffusion Policy/Manipulation/RL/World Model/Tactile) から
1〜2本ずつ arXiv で探し、weekly/ と topics/ を更新してください。」
```

### ノートのフォーマット
[`templates/weekly.md`](templates/weekly.md) を参照。各論文のメモは以下を意識:
- 何を解決したか (問題設定)
- アプローチの核心 (1〜2行)
- 既存研究との差分
- 気になる点・次に読む論文

---

## ディレクトリ構成

```
robotics-paper-watch/
├── README.md
├── weekly/               # 週次ノート (YYYY-WXX.md)
│   └── 2026-W18.md
├── topics/               # トピック別インデックス (論文の横断参照用)
│   ├── vla.md
│   ├── e2e.md
│   ├── diffusion-policy.md
│   ├── manipulation.md
│   ├── reinforcement-learning.md
│   ├── world-model.md
│   └── tactile.md
└── templates/
    └── weekly.md         # 週次ノートのテンプレート
```
