# Sensing & Perception

ロボットが何をどう知覚するか。触覚センサ・3D 視覚・マルチモーダル表現学習。「ポリシーに何を入力するか」を決める研究群。

---

## 論文インデックス

### 触覚センサ・ハードウェア

| 論文 | 著者 | 発表 | ポイント |
|---|---|---|---|
| [FingerEye](https://arxiv.org/abs/2604.20689) | NUS | 2026-04 | 双眼カメラ + 変形リングで接触前後を連続センシング |
| [TAMEn](https://arxiv.org/abs/2604.07335) | Wu et al. | 2026-04 | 指先触覚 + 魚眼カメラ搭載操作エンジン。OSS公開 |
| [HANDFUL](https://arxiv.org/abs/2604.25126) | USC | 2026-04 | LEAP Hand で把握後の二次操作。触覚 × 多指 |

### 触覚表現学習・Foundation Model

| 論文 | 著者 | 発表 | ポイント |
|---|---|---|---|
| [Sparsh](https://arxiv.org/abs/2410.24090) | Meta FAIR | CoRL 2024 | 複数センサ対応の自己教師あり触覚事前学習 |
| [TacViT](https://arxiv.org/abs/2604.00744) | Bristol | 2026-04 | ViT ベース触覚認識。未知センサへの汎化 |
| [UniTouch](https://arxiv.org/abs/2309.14972) | Columbia | CoRL 2023 | 視覚・触覚・音声の統合潜在空間 |

### 触覚シミュレーション

| 論文 | 著者 | 発表 | ポイント |
|---|---|---|---|
| [TacSL](https://arxiv.org/abs/2408.06506) | NVIDIA | 2024 | IsaacGym ベース。触覚 Sim-to-Real の起点 |
| [ETac](https://arxiv.org/abs/2604.20295) | Xu et al. | 2026-04 | データ駆動で弾性体近似。869 FPS で RL に使える |

### 触覚データセット

| 論文 | 著者 | 発表 | ポイント |
|---|---|---|---|
| [VTouch++](https://arxiv.org/abs/2604.20444) | Hua et al. | 2026-04 | 視触覚 × 両腕操作データセット。300+ タスク |

### 3D 視覚・把持

| 論文 | 著者 | 発表 | ポイント |
|---|---|---|---|
| [AnyGrasp](https://arxiv.org/abs/2212.08333) | Tsinghua | T-RO 2023 | GraspNet-1B で学習した汎用把持推定 |
| [3D Diffusion Policy](https://arxiv.org/abs/2403.03954) | PKU | RSS 2024 | 点群入力で視点変化に頑健なポリシー |

---

## 触覚センサの種類と特徴

| センサ | タイプ | 特徴 | 関連論文 |
|---|---|---|---|
| GelSight / GelSight Wedge | 光学 | 高解像度・研究用標準 | TacSL |
| DIGIT (Meta) | 光学・小型 | 軽量・安価。Sparsh と相性良い | Sparsh |
| TacTip (Bristol) | ソフトバンパー | 皮膚変形を光学計測 | TacViT |
| LEAP Hand | 多指ハンド | 安価・OSS。触覚センサ搭載可 | HANDFUL |
| FingerEye (NUS) | 双眼カメラ型 | 接触前後の連続センシング | FingerEye |

---

## 触覚研究の現状と課題

**整ってきたもの:**
- センサの選択肢 (光学・ソフト・圧力など)
- Foundation Model アプローチ (Sparsh, TacViT)
- 高速シミュレーション (ETac: 869 FPS)

**まだ課題:**
- Sim-to-Real ギャップ (センサ画像の再現精度)
- VLA との統合 (触覚トークンをどう VLA に入れるか)
- 両腕 × 触覚の協調制御 (VTouch++ がデータを提供しはじめた)
