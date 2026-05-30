# CVPR 2026 チュートリアル一覧

> **会場:** Colorado Convention Center, Denver, Colorado, USA  
> **開催日:** 2026年6月3日（火）・6月4日（水）

---

## 目次

| # | チュートリアル名 | 日時 | 会場 |
|---|---|---|---|
| 1 | [All You Need To Know About Self-Driving](#tutorial-1) | Jun 04, 9:00 AM (終日) | Room 301/302 |
| 2 | [Building GenAI based Simulation Environment for End-to-End Autonomous Driving](#tutorial-2) | Jun 03, 1:30 PM | Room 201 |
| 3 | [From Perception to Simulation: The Emergence of World Models in Multi-modal Reasoning](#tutorial-3) | Jun 03, 2:00 PM | Room 301/302 |
| 4 | [Monte Carlo Physical Simulation](#tutorial-4) | Jun 03, 1:00 PM | Room 702 |
| 5 | [Foundations and Frontiers of Watermarking](#tutorial-5) | Jun 04, 1:00 PM | Mile High 2B |
| 6 | [Principled Interpretability in Vision Models](#tutorial-6) | Jun 03, 1:00 PM | Mile High 3C |
| 7 | [Towards Safe Multi-Modal Learning: Evolving Threats and Safety Solutions](#tutorial-7) | Jun 03, 8:00 AM | Mile High 3C |
| 8 | [Extending Computer Vision to Hidden Objects: Millimeter-Wave Imaging](#tutorial-8) | Jun 04, 8:00 AM | Room 702 |
| 9 | [Tom Builds, Tom Breaks: Hands-On Attacks and Defenses for Vision-Language Systems](#tutorial-9) | Jun 03, 8:00 AM | Mile High 2B |
| 10 | [Edge AI in Action: Mastering On-Device Inference](#tutorial-10) | Jun 03, 8:00 AM | Room 702 |
| 11 | [From Perception to Action: Building Efficient and Deployable Robot Intelligence Pipelines](#tutorial-11) | Jun 04, 1:00 PM | Room 702 |
| 12 | [The Road to Convergence: Evolution of Unified Multimodal Models](#tutorial-12) | Jun 04, 1:00 PM | Room 201 |
| 13 | [Computer Vision at Scale: Multi-Camera Tracking for Checkout-Free Retail](#tutorial-13) | Jun 04, 8:00 AM | Room 203 |
| 14 | [Analytic Understanding of Diffusion Models](#tutorial-14) | Jun 04, 8:30 AM (終日) | Mile High 3C |
| 15 | [3D Human Mesh Modeling and Recovery from RGB and LiDAR](#tutorial-15) | Jun 03, 1:30 PM | Mile High 2B |
| 16 | [Accelerated Diffusion Models: From Theory to Interactive World Models](#tutorial-16) | Jun 03, 9:00 AM | Room 201 |
| 17 | [The Full Stack of Physical AI](#tutorial-17) | Jun 04, 8:00 AM | Mile High 2B |
| 18 | [The Principles of Diffusion Models: Real-Time Continuous & Discrete Diffusion](#tutorial-18) | Jun 03, 8:00 AM | Room 301/302 |
| 19 | [Recent Advances in AI for Medical Imaging](#tutorial-19) | Jun 04, 8:00 AM | Room 201 |

---

<a id="tutorial-1"></a>
## 1. All You Need To Know About Self-Driving

- **日時:** 2026年6月4日（水）9:00 AM〜（終日）
- **会場:** Room 301/302
- **登壇者:** Raquel Urtasun, Abbas Sadat, Sivabalan Manivasagam, Jingkang Wang, Ioan Andrei Barsan (Waabi)
- **リンク:** https://waabi.ai/cvpr-2026#tutorial

**概要:**

Waabiチームによる自動運転システムの全側面を網羅する終日チュートリアル。ハードウェア・センサーから始まり、知覚・運動予測・計画・制御・ML開発・シミュレーション・V2V通信・マッピング・自己位置推定まで、自動運転に関わるすべての技術領域を体系的に解説する。Physical AIの最前線に立つWaabiの研究・開発チームが講師を務める実践的な内容。

**スケジュール:**

| トピック | 内容 |
|----------|------|
| ハードウェア・センサー | センサー構成と特性 |
| 知覚（Perception） | 物体検出・セマンティック理解 |
| 運動予測（Motion Forecasting） | 他車両・歩行者の動き予測 |
| 計画・制御（Planning & Control） | 経路計画と車両制御 |
| ML開発 | 機械学習パイプライン |
| シミュレーション | 仮想環境でのテスト |
| V2V通信 | 車両間通信 |
| マッピング・自己位置推定 | 地図作成と位置特定 |

> ⚠️ 各トピックの詳細時刻は未公開。終日（Full-day）形式。

---

<a id="tutorial-2"></a>
## 2. Building GenAI based Simulation Environment for End-to-End Autonomous Driving

- **日時:** 2026年6月3日（火）1:30〜4:00 PM MDT
- **会場:** Room 201
- **登壇者:** Henry Liu (Univ. of Michigan), Howie Sun (Laplace Intelligence), Žan Gojčič (NVIDIA), Jun Gao (Univ. of Michigan & NVIDIA), Xintao Yan (HKU)
- **リンク:** https://cvpr2026-tutorial-genai-av-sim.github.io/

**概要:**

自動運転の安全検証に不可欠なシミュレーション環境の構築を、生成AIの観点から解説する半日チュートリアル。従来型シミュレータの限界（センサー特性や挙動の多様性の欠如）を指摘し、TeraSim・NVIDIA NuRec・Cosmosなどのオープンソースツールを用いた生成型シミュレーションの最前線を紹介する。シーン再構成から生成合成・安全評価まで一貫したパイプラインを提示し、研究者・実務者双方に具体的な出発点を提供する。

**スケジュール:**

| 時間 (MDT) | トピック | 登壇者 |
|------------|----------|--------|
| 1:30–2:00 PM | 自動運転の20年と残された課題 | Henry Liu（Univ. of Michigan） |
| 2:00–2:30 PM | TeraSim入門：自動運転の未知の危険シナリオを発見する生成型シミュレーション | Howie Sun（Laplace Intelligence） |
| 2:30–3:00 PM | 自動運転クローズドループシミュレーションのための生成的シーン再構成 | Žan Gojčič（NVIDIA） |
| 3:00–3:30 PM | 自動運転向け生成型ワールドシミュレータの最近の進展 | Jun Gao（Univ. of Michigan & NVIDIA） |
| 3:30–4:00 PM | 長期的AVシミュレーションに向けて：構造化自己回帰ワールドモデリングと検索ベース評価 | Xintao Yan（The Univ. of Hong Kong） |

---

<a id="tutorial-3"></a>
## 3. From Perception to Simulation: The Emergence of World Models in Multi-modal Reasoning

- **日時:** 2026年6月3日（火）14:00〜17:25
- **会場:** Room 301/302
- **登壇者:** Yujun Cai, Jianfei Cai (NTU), Yiwei Wang, Ming-Hsuan Yang (UC Merced)
- **リンク:** https://wangywust.github.io/cvpr-tutorial-world-model/

**概要:**

マルチモーダル推論におけるワールドモデルの台頭を、知覚・生成・シミュレーション・物理整合性の観点から体系的に論じるチュートリアル。「Chain-of-Thought」から「Chain-of-State」へのパラダイムシフトを基軸に、ビデオ生成・3D再構成・物理シミュレーション・具現化エージェントへの応用を幅広くカバーする。Genie 3・Cosmos 3・VideoPhy等の最新研究を招待講演で紹介し、今後の研究方向を展望する。

**スケジュール:**

| 時間 | トピック | 登壇者 |
|------|----------|--------|
| 14:00–14:10 | オープニング：動機と概要 | Yujun Cai |
| 14:10–14:40 | Chain-of-ThoughtからChain-of-Stateへ：有能なモデルが世界を予測しなければならない理由 | Dan Kondratyuk |
| 14:40–15:10 | Genie 3：インタラクティブなフォトリアルな世界の生成 | Hang Qi |
| 15:10–15:50 | 物理整合性のある効率的なビジュアルワールドモデルに向けて | Jianfei Cai |
| 15:50–16:20 | VideoPhy：ビデオ生成における物理常識評価 | Kai-Wei Chang |
| 16:20–16:50 | Cosmos 3：Physical AI向けオムニワールド基盤モデル | Ming-Yu Liu |
| 16:50–17:25 | ワールドモデルに向けて：ジオメトリ・ビュー合成・視覚推論 | Ming-Hsuan Yang |

---

<a id="tutorial-4"></a>
## 4. Monte Carlo Physical Simulation

- **日時:** 2026年6月3日（火）1:00 PM
- **会場:** Room 702
- **登壇者:** Rohan Sawhney, Bailey Miller, Ioannis Gkioulekas, Keenan Crane
- **リンク:** https://rohan-sawhney.github.io/mcgp-resources/

**概要:**

偏微分方程式（PDE）のためのグリッドフリーなモンテカルロ法（Walk on Spheres; WoS）を中心に、物理シミュレーションへの応用を解説するコース。従来の有限要素法に対して体積メッシュを不要とするWoSの優位性を示し、モンテカルロレンダリングの知見をPDEソルバーに応用する新手法を紹介する。SIGGRAPH 2025およびSGP 2024でも同様のコースを実施しており、スライドや参考文献が充実している。

**スケジュール:**

| トピック | 内容 |
|----------|------|
| モンテカルロ法の基礎 | サンプル生成・分散削減 |
| Walk on Spheres（WoS） | アルゴリズムと一般化 |
| 境界条件への拡張 | Neumann/Robin条件（Walk on Stars, Walkin' Robin） |
| 空間変化係数を持つPDE | 応用と実装 |
| オープンソースツール | Zombie / FCPW ライブラリ |

> ⚠️ CVPR 2026固有の詳細タイムテーブルは未公開。リソースページのみ公開中。

---

<a id="tutorial-5"></a>
## 5. Foundations and Frontiers of Watermarking: Algorithms, Multimodal Extensions, Benchmarks, and Authenticity Frameworks

- **日時:** 2026年6月4日（水）1:00–5:00 PM
- **会場:** Mile High 2B
- **登壇者:** Vishal Asnani (Adobe Research), Shruti Agarwal (Adobe Research), Benedetta Tondi (Univ. of Siena), Pierre Fernandez (Meta FAIR), Furong Huang (Univ. of Maryland)
- **リンク:** https://vishal3477.github.io/watermarking-cvpr2026/

**概要:**

生成AIの台頭により再び重要性を増す不可視電子透かしについて、古典的信号処理理論から最先端のディープラーニング手法・マルチモーダル拡張・堅牢性評価・産業展開まで、体系的に解説する半日チュートリアル。画像・動画・音声・3D（NeRF・Gaussian Splats）への応用、生成透かしパラダイム（モデルファインチューニング・ノイズ空間手法）を網羅する。コンテンツ真正性・AIトレーサビリティを支えるプロヴェナンスエコシステムの実装例も紹介する。

**スケジュール:**

| 時間 | トピック | 登壇者 |
|------|----------|--------|
| 1:00–1:05 PM | はじめに・動機付け | Vishal Asnani（Adobe Research） |
| 1:05–1:45 PM | 実世界の真正性システム：デプロイ済みシステムのデモと検証可能なプロヴェナンス | Shruti Agarwal（Adobe Research） |
| 1:45–2:25 PM | マルチモーダル＆生成透かし：エンコーダ・デコーダ手法の音声/動画/3D拡張と生成透かしパラダイム | Pierre Fernandez（Meta FAIR） |
| 2:25–2:40 PM | ☕ コーヒーブレイク | — |
| 2:40–3:20 PM | ディープラーニング以前と以後の透かし技術：古典的基礎理論（スペクトラム拡散・量化ベース手法）とその現代的応用 | Benedetta Tondi（Univ. of Siena） |
| 3:20–3:30 PM | 短休憩 | — |
| 3:30–4:10 PM | ベンチマーキング＆堅牢性評価：攻撃分類・評価指標・標準化ストレステスト | Furong Huang（Univ. of Maryland） |
| 4:10–4:50 PM | GenAI透かし＆アトリビューション：生成モデルへの透かし埋め込みの統一フレームワーク | Vishal Asnani（Adobe Research） |
| 4:50–5:00 PM | 総括・Q&A | 全登壇者 |

---

<a id="tutorial-6"></a>
## 6. Principled Interpretability in Vision Models: From Mechanistic Understanding to Interpretable Models by Design

- **日時:** 2026年6月3日（火）1:00–5:00 PM
- **会場:** Mile High 3C
- **登壇者:** Tsui-Wei (Lily) Weng, Tuomas Oikarinen（UC San Diego）
- **リンク:** https://lilywenglab.github.io/cvpr2026-principled-interpretability-tutorial/

**概要:**

ハイステークスな応用への深層学習の普及に伴い、モデルの信頼性確保に不可欠な解釈可能性（Interpretability）を体系的に解説するチュートリアル。事後的なメカニズム的解釈（ニューロン・レイヤー・回路レベルの分析）と、設計段階から解釈可能なモデル（Concept Bottleneck Models等）の両アプローチを統一的に論じる。評価プロトコルの標準化・信頼性評価・デバッグ・安全性監査への実践的応用も扱う。

**スケジュール:**

| パート | トピック |
|--------|----------|
| Part 1 | イントロダクション＆背景 |
| Part 2 | 事後的モデルレベルの解釈可能性 |
| Part 3 | 忠実性・信頼性の評価 |
| Part 4 | 設計段階から解釈可能なDNNモデル |
| Part 5 | 応用・デモ・技術Q&A |

> ⚠️ 各パートの詳細時刻はページ上で「近日公開（Stay tuned）」とされており未公表。

---

<a id="tutorial-7"></a>
## 7. Towards Safe Multi-Modal Learning: Evolving Threats and Safety Solutions

- **日時:** 2026年6月3日（火）8:00 AM
- **会場:** Mile High 3C
- **登壇者:** Xi Li（Univ. of Alabama at Birmingham）, Manling Li（Northwestern Univ.）, Muchao Ye（Univ. of Iowa）
- **リンク:** https://sites.google.com/view/cvpr26-safe-mm-learnig/home

**概要:**

マルチモーダル学習における安全上の脅威とその対策を体系的に解説するチュートリアル。テキスト・画像・音声・動画を統合する大規模マルチモーダルモデルが持つ固有のリスク（モダリティ統合の侵害・モダリティミスアライメント・複合的脆弱性）を分類・整理し、単一モダリティシステムから継承された従来の安全前提がどのように崩れるかを論じる。敵対的攻撃・データポイズニング・ジェイルブレイク・幻覚（ハルシネーション）を包括的に扱い、信頼できるマルチモーダルAIへの道筋を示す。

**スケジュール:**

| パート | トピック | 時間 |
|--------|----------|------|
| Part 1 | イントロダクション＆背景（マルチモーダル学習の独自性・安全課題の整理） | 20分 |
| Part 2 | 新興のマルチモーダル安全脅威（モダリティ統合の侵害・ミスアライメント・複合リスク） | 50分 |
| — | 休憩 | 10分 |
| Part 3 | 進化するマルチモーダル安全状況（従来の安全前提の崩壊） | 20分 |
| — | 休憩 | 10分 |
| Part 4 | 安全なマルチモーダル学習の最新動向（教師あり安全ファインチューニング・嗜好ベース最適化・学習不要手法） | 50分 |
| Part 5 | 結論（オープンチャレンジ・将来方向） | 10分 |
| Q&A | 質疑応答 | 20分 |

---

<a id="tutorial-8"></a>
## 8. Extending Computer Vision to Hidden Objects: A Tutorial on Millimeter-Wave Imaging and Reconstruction of Occluded Scenes

- **日時:** 2026年6月4日（水）8:00 AM
- **会場:** Room 702
- **登壇者:** Mingmin Zhao（Univ. of Pennsylvania）, Laura Dodds（MIT）, Hailan Shanbhag（EPFL）
- **リンク:** https://cvpr-mmwave-tutorial.github.io/

**概要:**

5G/6G/次世代WiFiに使われるミリ波（mmWave）信号を用いて、段ボール・布・霧などの遮蔽物越しの隠れた物体を検出・3D再構成する技術を紹介するチュートリアル。可視光や他の透過モダリティ（X線・超音波）との違いを解説した上で、古典的なmmWaveイメージング手法と最先端のディープラーニングベース手法を体系的に教える。自動運転・ロボット工学・物流など幅広い応用分野を扱い、mmWave研究を始める研究者向けのデータセット・ベンチマーク・ツールも紹介する。

**スケジュール:**

| 時間 | トピック |
|------|----------|
| 8:00–8:15 AM | イントロダクション |
| 8:15–9:15 AM | ミリ波信号の基礎：可視光との違い・応用事例・古典的イメージング手法とその限界 |
| 9:15–10:00 AM | 高度な透過物体3D再構成：法線推定を用いた遮蔽物越し物体の3D再構成と補完 |
| 10:00–10:15 AM | ☕ コーヒーブレイク |
| 10:15–11:00 AM | 視界不良環境における視覚品質シーン理解：mmWaveによるLiDAR相当シーン再構成と自動運転への応用 |
| 11:00–11:45 AM | ミリ波研究のはじめ方：既存データセット・ツール・オープン問題のツアー＋ハンズオンデモ |

---

<a id="tutorial-9"></a>
## 9. Tom Builds, Tom Breaks: Hands-On Attacks and Defenses for Vision-Language Systems

- **日時:** 2026年6月3日（火）8:00 AM
- **会場:** Mile High 2B
- **登壇者:** Pavan Reddy
- **リンク:** https://portfolio.pavanreddy.ai/talks-and-workshops/cvpr-tutorial-2026/content

**概要:**

Vision-Language Systems（VLMs）に対する攻撃手法とその防御策を、実践的なハンズオン形式で学ぶチュートリアル。「Tom Builds, Tom Breaks」というタイトルは構築（防御側）と破壊（攻撃側）の双方の視点を持つことを示唆しており、参加者が直接攻撃・防御を体験できる構成。

**スケジュール:**

> ⚠️ ページがJavaScriptレンダリング必須のSPAのため詳細取得不可。

---

<a id="tutorial-10"></a>
## 10. Edge AI in Action: Mastering On-Device Inference

- **日時:** 2026年6月3日（火）8:00 AM
- **会場:** Room 702
- **登壇者:** Fabricio Batista Narcizo（Jabra / ITU）, Elizabete Munzlinger（Jabra / ITU）, Sai Narsi Reddy Donthi Reddy（Jabra）, Shan Ahmed Shaffi（Jabra）
- **リンク:** https://www.fabricionarcizo.com/cvpr2026-edge-ai-in-action/

**概要:**

スマートフォン・カメラ・ドローン・ウェアラブル等のエッジデバイスにAIモデルを直接デプロイするEdge AIの実践的チュートリアル。Qualcomm SnapdragonとNVIDIA Jetsonという代表的な2つのエッジAIプラットフォームを対象に、モデル最適化・変換・推論の実装手順をハンズオン形式で解説する。ONNX・TensorRT・Qualcomm SNPE・Qualcomm AI Runtime SDK等のツールを用い、物体検出と大規模言語モデル（LLM）の応用例を通じてエッジAIパイプライン全体を体験できる。

**スケジュール:**

| モジュール | トピック |
|------------|----------|
| モジュール1 | エッジAIプラットフォームとハードウェアアクセラレーションの入門：クラウドAIとの比較・レイテンシ/プライバシ/消費電力のトレードオフ・実世界応用例 |
| モジュール2 | Qualcomm Snapdragonへの最適化＆デプロイ：モデル変換パイプライン・SNPE/Qualcomm AI Runtime SDKを用いた推論最適化・ベンチマーク |
| モジュール3 | エッジAIモデルのパフォーマンス分析＆ベンチマーキング：QNN runtimeによるデバイス上プロファイリング（HTP/DSP/GPU/CPU）・量化評価・分析ダッシュボード |
| モジュール4 | NVIDIA Jetsonへの最適化＆デプロイ：Jetsonエコシステム・モデル量化・TensorRT SDKを用いたリアルタイム推論 |

> ⚠️ 各モジュールの詳細時刻は未公開。

---

<a id="tutorial-11"></a>
## 11. From Perception to Action: Building Efficient and Deployable Robot Intelligence Pipelines with Open-Source Edge AI Toolkits

- **日時:** 2026年6月4日（水）1:00 PM
- **会場:** Room 702
- **登壇者:** Samet Akcay, Zhuo Wu, Michael Paulitsch, Ashutosh Kumar, Tao Xiong, Adrian Boguszewski, Sameer Sheorey, Benjamin Ummenhofer
- **リンク:** https://github.com/zhuo-yoyowz/cvpr-2026/

**概要:**

ロボットによるテーブルトップ操作を題材に、「論文から実機ロボットへ」のギャップを埋めることを目的とした完全オープンソースのエンドツーエンドワークフローを教えるチュートリアル。テレオペレーションによるデータ収集から始まり、Transformer・拡散ベースのビジュモータポリシーの学習、3D物体デジタル化によるシミュレーションスケーリング、そしてエッジデバイスへのリアルタイムデプロイまでをカバーする。最終的にLeRobotスタイルアームを使ったライブデモで締めくくる実践的な内容。

**スケジュール:**

| モジュール | トピック |
|------------|----------|
| Intro | 体現的ロボット操作とテーブルトップタスクの紹介 |
| Module 1 | オープンソースツールによるテレオペレーションデータ収集とビジュモータポリシー学習 |
| Module 2 | 3D再構成・ニューラル物体クローニングによるシミュレーション用アセット生成 |
| Module 3 | モデル変換・最適化・エッジハードウェアへのリアルタイムデプロイ |
| Module 4 | 手頃なロボットアーム上でのエンドツーエンド知覚→行動パイプライン（ライブデモ） |

> ⚠️ 具体的な時刻付きスケジュールは未公開（アウトラインのみ）。

---

<a id="tutorial-12"></a>
## 12. The Road to Convergence: Evolution of Unified Multimodal Models

- **日時:** 2026年6月4日（水）1:00 PM
- **会場:** Room 201
- **登壇者:** Jindong Wang (William & Mary), Hao Chen (DeepMind), Jiakui Hu (Peking Univ.), Zhaolong Su (William & Mary), Sharon Li (UW–Madison)
- **リンク:** https://rollingsu.github.io/umm-tutorial.github.io/#

**概要:**

統合マルチモーダルモデル（UMM）のアーキテクチャ設計・表現学習・学習ダイナミクス・評価を体系的に解説するチュートリアル。「どうモデル化するか」「どう表現するか」「どう学習するか」という3つの根本的な問いを軸に構成される。自己回帰・拡散・ハイブリッドアプローチのトレードオフ分析、連続・離散トークナイザの比較、DPO/GRPOなどの後学習アライメント手法まで幅広くカバーする。ロボティクスや自動運転への応用と、統一コードベースの実演も含む。

**スケジュール:**

| セッション | 時間 | トピック |
|------------|------|----------|
| Session 1 | 30分 | Introduction & Motivation — UMMの中核的動機・定義、理解と生成の相互強化 |
| Session 2 | 45分 | Modeling Architectures — 外部専門家統合・モジュール型・エンドツーエンド統合の分類学 |
| Session 3 | 45分 | The Unified Tokenizer Challenge — 連続表現 vs 離散トークン化、カスケード・デュアルブランチ設計 |
| Session 4 | 45分 | Training Recipes & Data — インターリーブデータセット構築・事前学習目標・DPO/GRPOアライメント |
| Session 5 | 30分 | Evaluation, Applications & Future Directions — ベンチマーク・ロボティクス・自動運転応用・オープン課題 |
| Session 6 | 15分 | Unified Codebase & Integration — 統合マルチモーダルコードベースの実践的ウォークスルー |

---

<a id="tutorial-13"></a>
## 13. Computer Vision at Scale: Multi-Camera Tracking, Calibration, and Event Detection for Checkout-Free Retail

- **日時:** 2026年6月4日（水）8:00 AM（3.5時間）
- **会場:** Room 203
- **登壇者:** Hareesh Kolluru (Motive), Motilal Agarwal (Zippin), Tanmay Bangalore (Meta)
- **リンク:** https://checkout-free-tutorial-cvpr26.github.io/

**概要:**

レジなし小売という現実の大規模コンピュータビジョンシステムを題材に、マルチカメラキャリブレーション・リアルタイムトラッキング・構造化イベント検出という3つの基盤技術を学術・産業横断的に解説するチュートリアル。インフラ制約（帯域幅・レイテンシ・エッジコンピューティング）がアルゴリズム設計にどう影響するかを中心テーマとして据える。自動運転・スマートシティ・スポーツ分析などに直接転用できる汎用的な手法として提示。ライブデモでオンラインキャリブレーション・マルチオブジェクトトラッキングを実演する。

**スケジュール:**

| 時間 | トピック | 登壇者 |
|------|----------|--------|
| 15分 | Introduction & Multi-Camera Vision at Scale — 産業規模のインフラ制約・ライブデモセットアップ紹介 | 全員 |
| 60分 | Automatic Multi-Camera Calibration — SuperPoint/LoFTR/バンドル調整、SIFT/ORB/SfM、オンライン改良・障害検知 ▶ ライブデモ | Agarwal |
| 15分 | Break — 参加者デモ体験 | — |
| 45分 | Real-Time Multi-Camera Tracking — 整数計画法によるグローバル最適化、グラフ定式化、非同期データ・遮蔽対応 ▶ ライブデモ | Kolluru |
| 45分 | Structured Event Inference & Reliability — 手・棚インタラクション、マルチカメラ統合、エッジコンピューティング ▶ ライブデモ | Bangalore + 全員 |
| 30分 | Interactive Q&A & Hands-on Demo — 参加者がライブシステムを操作 | 全員 |

---

<a id="tutorial-14"></a>
## 14. Analytic Understanding of Diffusion Models

- **日時:** 2026年6月4日（水）8:30 AM–5:00 PM（終日）
- **会場:** Mile High 3C
- **登壇者:** Artem Lukoianov, Chenyang Yuan, Christopher Scarvelis, Mason Kamb（+ 招待講演者1名 TBA）
- **リンク:** https://analytic-diffusion.github.io/

**概要:**

拡散モデルの学習目標には「訓練データだけを再現する完全記憶の閉形式解が存在する」というパラドックスがある。このチュートリアルは、それにもかかわらずなぜ深層拡散モデルが汎化するのかを「解析的拡散モデル」の視点から探求する。スコアスムージング・ニューラルアーキテクチャの帰納バイアス・学習ダイナミクス・データ幾何など、最適デノイジングのレンズを通じた理論的理解を構築する。講義とJupyterノートブックを組み合わせた実践的な終日チュートリアル。

**スケジュール:**

| 時間 | トピック | 登壇者 |
|------|----------|--------|
| 8:30–8:45 | Welcome & Introduction — チュートリアル概要・拡散入門・記法説明 | 全員 |
| 8:45–9:30 | Hands-on: 拡散モデルのパラドックス — 閉形式スコアデノイザ・最適サンプリング・記憶・訓練集合安定性の実験 | Chenyang Yuan |
| 9:30–9:45 | Break | — |
| 9:45–10:45 | Fundamentals of Diffusion Models — 順・逆過程・スコアマッチング・デノイジング目標 | Chenyang Yuan |
| 10:45–11:00 | Break | — |
| 11:00–12:00 | Score Smoothing & Effective Linear Structures — アンダーフィットとスコアスムージングの関係、線形モデルとの接続 | Christopher Scarvelis |
| 12:00–13:30 | Lunch | — |
| 13:30–14:30 | Wiener Filters & Analytical Denoisers + Hands-on — データ共分散・Wienerフィルタ・局所性・PCAベースデノイザ | Artem Lukoianov |
| 14:30–15:00 | Guidance & Analytical Models — 畳み込み帰納バイアス・等変性・アーキテクチャが訓練集合を超える創造性を可能にする仕組み | Mason Kamb |
| 15:00–15:15 | Break | — |
| 15:15–16:15 | Invited Talk — 招待講演者（TBA） | TBA |
| 16:15–16:30 | Break | — |
| 16:30–17:00 | Open Questions & Discussion — オープン課題パネルディスカッション・Q&A | 全員 |

---

<a id="tutorial-15"></a>
## 15. 3D Human Mesh Modeling and Recovery from RGB and LiDAR

- **日時:** 2026年6月3日（火）1:30 PM
- **会場:** Mile High 2B
- **登壇者:** Romain Brégier, István Sárándi, Salma Galaaoui, Fabien Baradel, Nermin Samet, David Picard
- **リンク:** https://human-mesh-tutorial.github.io/

**概要:**

人体メッシュモデリングとリカバリ（HMR）の現状を体系的に解説する半日チュートリアル。パラメトリック人体モデル（SMPL・SMPL-X・MHR・Anny等）の設計思想から始まり、RGBカメラからの3D HMR、さらに困難な屋外環境でのLiDARからのHMRまでをステップバイステップでカバーする。AR/VR・スポーツ分析・自動運転・ヒューマンロボットインタラクションなど幅広い下流アプリケーションを念頭に置いた内容。

**スケジュール:**

| 時間 | トピック | 登壇者 |
|------|----------|--------|
| 13:30–14:30 | パラメトリック人体メッシュモデルの理解 — 骨格アニメーション・スキニング・統計的形状モデリング・SMPL/SMPL-X/STAR/MHR/Anny/SOMAの概観 | Romain Brégier |
| 14:30–15:30 | RGBからの3D人体メッシュリカバリ — 単人物・多人物・映像・ワールド空間・マルチビュー（HMR2.0・SMPLer-X・NLF等）・ライブデモ | István Sárándi |
| 15:30–15:45 | ☕ コーヒーブレイク | — |
| 15:45–16:45 | LiDARからの3D人体姿勢・形状推定 — 屋外安全クリティカルシナリオ・LiDAR固有の課題・データセット・メトリクス・コード例・デモ | Salma Galaaoui |

---

<a id="tutorial-16"></a>
## 16. Accelerated Diffusion Models: From Theory to Interactive World Models

- **日時:** 2026年6月3日（火）9:00 AM–12:00 PM
- **会場:** Room 201
- **登壇者:** Julius Berner (NVIDIA), Weili Nie (Meta), Arash Vahdat (NVIDIA)
- **リンク:** https://cvpr26-tutorial-fastgen.github.io/

**概要:**

拡散モデル・フローベース手法のリアルタイムインタラクティブ応用に向けた高速化手法を体系的に教えるチュートリアル（半日）。反復サンプリングの計算コストがリアルタイムデプロイの障壁になっているという問題意識のもと、オープンソースのFastGenライブラリを活用しながら、一般的なサンプリング高速化・蒸留ベースの少ステップサンプラー学習・動画および対話的ワールドモデルへの応用という3つの主要分野をカバーする。

**スケジュール:**

| 時間 | トピック | 登壇者 |
|------|----------|--------|
| 9:00–9:50 AM | General Paradigms to Accelerating Diffusion Models — 高度な微分方程式ソルバー・低次元潜在拡散・改良ノイズプロセス・アーキテクチャベース高速化 | Arash Vahdat |
| 9:50–10:00 AM | Break | — |
| 10:00–10:50 AM | Accelerating Diffusion Models with Step Distillation — 軌道ベース蒸留（Consistency Models・Flow Maps）と分布蒸留（Adversarial蒸留・Variational Score蒸留） | Julius Berner |
| 10:50–11:00 AM | Break | — |
| 11:00–11:50 AM | From Images to Interactive World Models — リアルタイムサンプリング・長期コンテキストメモリ・ブロック単位因果生成（CausVid・Self-Forcing・APT2） | Weili Nie |

---

<a id="tutorial-17"></a>
## 17. The Full Stack of Physical AI: Simulation, Foundation Models, and Edge Deployment for Next-Generation Robotics Applications

- **日時:** 2026年6月4日（水）8:00 AM（半日）
- **会場:** Mile High 2B
- **登壇者:** Raymond Lo, Johnny Núñez, Chitoku Yato, Spencer Huang, Mitesh Patel（全員 NVIDIA）
- **リンク:** https://johnnynunez-nv.github.io/physical-ai-cvpr2026/

**概要:**

自律ロボット・自動運転車などのPhysical AIアプリケーション実現に向けたフルスタック（シミュレーション → 基盤モデル → エッジデプロイ）を解説するNVIDIA主催の半日チュートリアル。Isaac Sim/Isaac Lab/MJWarp/Newtonによるシミュレーション、GR00T・ACTなどのVLAモデル（Vision-Language-Action）、NVIDIA Jetson Thorへのリアルタイムデプロイという3本柱で構成される。参加者はエンドツーエンドのロボティクスパイプライン（データ収集→モデル学習→実機デプロイ）を体験できる。

**スケジュール:**

| 時間 | トピック | 登壇者 |
|------|----------|--------|
| 9:00–9:15 | Opening Remarks — Physical AI概要とモチベーション | Johnny Núñez |
| 9:15–10:15 | Talk 1: Simulation — Isaac Sim, Isaac Lab, MJWarp, Newton（環境構築・データ生成・ポリシー検証・Sim-to-Real） | Mitesh Patel |
| 10:15–11:15 | Talk 2: Foundation Models — GR00T と Physical AI基盤モデル（知覚・言語・行動の接続） | Yuqi Xie |
| 11:15–11:30 | ☕ コーヒーブレイク | — |
| 11:30–12:30 | Talk 3: Edge Deployment — Jetson Thor へのデプロイ（モデル最適化・リアルタイム推論・ハードウェア対応） | Johnny Núñez |
| 12:30–13:00 | Panel Discussion + Q&A | 全員 |

---

<a id="tutorial-18"></a>
## 18. The Principles of Diffusion Models: Real-Time Continuous & Discrete Diffusion

- **日時:** 2026年6月3日（火）8:00 AM
- **会場:** Room 301/302
- **登壇者:** Chieh-Hsin (Jesse) Lai (Sony AI), Subham Sahoo, Dongjun Kim, Yang Song, Yuki Mitsufuji (Sony), Stefano Ermon (Stanford)
- **リンク:** https://sites.google.com/view/cvpr26-principles-of-diffusion/home

**概要:**

連続データと離散データにまたがる高速拡散ベース生成を扱う実践的チュートリアル。第1部では連続拡散を変分・スコアベース・フローベースの3つの視点から統一し、DMD蒸留・Consistency Models・MeanFlowなど最新の高速サンプリング手法を解説する。第2部では離散拡散の理論的基盤として「Diffusion Duality」（離散と連続の拡散過程の双対性）を紹介し、Discrete Consistency Distillationによる少ステップ生成を実演する。ライブデモを交えた実践重視の内容。

**スケジュール:**

| 時間 | セクション | 内容 | 担当 |
|------|------------|------|------|
| 8:00–8:05 AM | 開始 | チュートリアル開始・イントロダクション | — |
| 8:05–9:35 AM | Part 1: Continuous Diffusion | ① 連続拡散の概観（VAE/DDPM、Score SDE、Flow Matching）② 分布ベース蒸留（DMD）▶ ライブデモ ③ フローマップモデル（CM・CTM・MeanFlow）▶ ライブデモ ④ 音声・映像生成とコンテンツ保護 | Chieh-Hsin Lai / Yuki Mitsufuji |
| 9:35–9:50 AM | Break | — | — |
| 9:50–11:30 AM | Part 2: Discrete Diffusion | ① 離散拡散の概観（Uniform-state拡散・順逆過程） ② ライブデモ: 画像生成 ③ 自己蒸留による高速化（Diffusion Duality・Discrete Consistency Distillation） ④ ライブデモ: Discrete Consistency Distillation | Subham Sahoo |

---

<a id="tutorial-19"></a>
## 19. Recent Advances in AI for Medical Imaging: Progress, Challenges, and Future Directions

- **日時:** 2026年6月4日（水）8:00 AM
- **会場:** Room 201
- **登壇者:** Jiaqi Wang (Auburn Univ.), Peirong Liu (Johns Hopkins), Can Zhao (NVIDIA), Yufan He (NVIDIA), Jeya Maria Jose Valanarasu (Microsoft Research), Sharon Xiaolei Huang (Penn State)
- **リンク:** https://sites.google.com/view/cvpr26aiformedical/home

**概要:**

医療画像AIの最新動向（MRI・CT・X線・超音波・デジタル病理など）を包括的に解説するチュートリアル。深層学習・基盤モデル・マルチモーダル統合・生成モデルがもたらした進歩を整理しつつ、汎化性・解釈可能性・データ異質性・プライバシー・実臨床展開という課題にも正面から向き合う。物理インフォームド学習・プライバシー保護連合学習・オープンソース医療基盤モデルという3つのパラダイムを中心に据え、次世代医療画像AIの方向性を展望する。

**スケジュール:**

| パート | 時間目安 | トピック | 登壇者 |
|--------|----------|----------|--------|
| Part 1 | 5分 | Introduction & Background | — |
| Part 2 | 60分 | Interpretable AI for Medical Image Understanding and Discovery — 集団規模の実データからのがん発見のためのマルチモーダルAI・物理駆動学習 | Jeya Maria Jose Valanarasu, Peirong Liu |
| Part 3 | 60分 | Open-source Foundation Models for Medical Imaging | TBD |
| — | 15分 | ☕ コーヒーブレイク | — |
| Part 4 | 60分 | Collaborative and Privacy Preserving AI for Medical Imaging — プライバシー保護動画データ共有 | Sharon Xiaolei Huang |
| Part 5 | 45分 | Future Work & Panel Discussion | 全員 |
| Part 6 | — | Sponsorship Talk & Lottery（スポンサー: Arith AI） | — |

---

## 統計サマリー

| 項目 | 値 |
|------|-----|
| チュートリアル総数 | **19件** |
| 6月3日（火）開催 | 10件 |
| 6月4日（水）開催 | 9件 |
| 終日開催 | 3件（#1, #14, 他） |
| 半日午前 | 7件 |
| 半日午後 | 9件 |
| 拡散モデル関連 | 4件（#14, #16, #18, #4） |
| 自動運転関連 | 2件（#1, #2） |
| ロボティクス/Physical AI | 3件（#11, #17, #3） |
| 安全性・セキュリティ | 3件（#5, #7, #9） |
| エッジAI/デプロイ | 2件（#10, #11） |
