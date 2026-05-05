# CVPR2026 論文要旨 (Part 3)

### Molmo2: Open Weights and Data for Vision-Language Models with Video Understanding and Grounding
著者: Christopher Clark, Jieyu Zhang, Zixian Ma, Jae Sung Park, Rohun Tripathi, Sangho Lee, Reza Salehi, Jason Ren, Chris Dongjoo Kim, Yinuo Yang, Vincent Shao, Yue Yang, Weikai Huang, Ziqi Gao, Taira Anderson, Jianrui Zhang, Jitesh Jain, George Stoica, Ali Farhadi, Ranjay Krishna

<details>
<summary> 日本語要旨 </summary>

現在、最も強力なビデオ言語モデル（VLM）はプロプライエタリである。最も強力なオープンウェイトのモデルは、プロプライエタリなVLMから合成データを利用し効果的にそれらから蒸留するか、またはトレーニングデータやレシピを開示しない。その結果、オープンソースコミュニティは最先端のビデオ（および画像）言語モデルに改善するための基盤が欠けている。特に重要なことに、多くの下流アプリケーションは高レベルのビデオ理解だけでなく、ピクセル単位でのポイントドリブンまたはトラッキングを必要とする。さらに、プロプライエタリモデルでもこの能力が欠如している。私たちはMolmo2という新しいVLMファミリーを提示する。これはオープンソースモデルの中で最先端であり、シングルイメージ、マルチイメージ、ビデオタスクにおけるポイントドリブングラウンディングに優れた新機能を示している。私たちの主要な貢献は、7つの新しいビデオデータセットと2つのマルチイメージデータセットであり、これには高度に詳細なビデオキャプションを用いた事前学習用データセット、フリーフォームビデオQ&Aデータセット（微調整用）、複雑なクエリを持つ新しいオブジェクト追跡データセット、および革新的な新しいビデオポイントングデータセットが含まれる。これらはすべて閉じたVLMを使用せずに収集されたものである。また、効率的なパッキングとメッセージツリー符号化スキームを利用したこのデータのトレーニングレシピを提示し、ビジョントークンに対する双方向注意と新規トークン重み戦略がパフォーマンスを改善することを示す。私たちの最高峰8Bモデルは、短いビデオ、カウント、キャプショニングにおいて他のオープンウェイト・データモデルクラスを上回り、長時間ビデオでは競争力がある。ビデオグランディングにおいてMolmo2はより大きなプロプライエタリモデルを凌駕し、ビデオポイントングで32.9%（Molmo2）対17%（Gemini 2.5 Pro）という結果を示している。
</details>

<details>
<summary> 英語要旨 </summary>

Today’s strongest video-language models (VLMs) remain proprietary. The strongest open-weight models either rely on synthetic data from proprietary VLMs, effectively distilling from them, or do not disclose their training data or recipe. As a result, the open-source community lacks the foundations needed to improve on the state-of-the-art video (and image) language models. Crucially, many downstream applications require more than just high-level video understanding; they require grounding—either by pointing or by tracking in pixels. Even proprietary models lack this capability. We present Molmo2, a new family of VLMs that are state-of-the-art amongst open-source models and demonstrate exceptional new capabilities in point-driven grounding in single image, multi-image, and video tasks. Our key contribution is a collection of 7 new video datasets and 2 multi-image datasets, including a dataset of highly detailed video captions for pre-training, a free-form video Q&A dataset for fine-tuning, a new object tracking dataset with complex queries, and an innovative new video pointing dataset, all collected without the use of closed VLMs. We also present a training recipe for this data utilizing an efficient packing and message-tree encoding scheme and show bi-directional attention on vision tokens and a novel token-weight strategy improve performance. Our best-in-class 8B model outperforms others in the class of open weight and data models on short videos, counting, and captioning, and is competitive on long-videos. On video-grounding Molmo2 outperforms larger proprietary models, including 32.9% (Molmo2) vs 17% (Gemini 2.5 Pro) on video pointing.
</details>

---

### LongVideo-R1: Smart Navigation for Low-cost Long Video Understanding
著者: Jihao Qiu, Lingxi Xie, Xinyue Huo, Qi Tian, Qixiang Ye

<details>
<summary> 日本語要旨 </summary>

この論文では、低コンピューティング予算のもとでの長時間動画理解という重要かつ未だ十分に探求されていない課題に取り組んでいます。私たちは、効率的な動画コンテキストナビゲーションを実現し、徹底した検索の冗長性を避けるために、活発で推論能力を備えたマルチモーダル大規模言語モデル（MLLM）エージェント「LongVideo-R1」を提案します。LongVideo-R1の中核となるのは、高レベルのビジュアル手がかりを利用して次に処理するための最も情報量の多い動画クリップを推測する推論モジュールです。推論時には、エージェントは上位レベルのビジュアルサマリーからトラバースを開始し、徐々に焦点を絞り込みます。そして、クエリへの回答に必要な十分な知識が得られた時点で即座に探索プロセスを停止します。トレーニングを容易にするために、まずCGBenchというアノテーション付き動画コーパスから階層的な動画キャプションを抽出し、GPT-5を指導して33,000の高品質なチェーン・オブ・サウザルト・ウィズ・ツール（CoT-wt）経路を生成します。LongVideo-R1エージェントはQwen-3-8Bモデル上で二段階のパラダイムにより微調整されます：監督付き微調整（SFT）に続いて強化学習（RL）。ここで、RLは選択的かつ効率的なクリップナビゲーションを最大化するために特別に設計された報酬関数を使用します。複数の長時間動画ベンチマークでの実験は、QA精度と効率性の優れたトレードオフを享受するLongVideo-R1の有効性を検証しています。すべてのカスタマイズされたデータおよびソースコードは補足資料に提供され、公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

This paper addresses the critical and underexplored challenge of long video understanding with low computational budgets. We propose LongVideo-R1, an active, reasoning-equipped multimodal large language model (MLLM) agent designed for efficient video context navigation, avoiding the redundancy of exhaustive search. At the core of LongVideo-R1 lies a reasoning module that leverages high-level visual cues to infer the most informative video clip for subsequent processing. During inference, the agent initiates traversal from top-level visual summaries and iteratively refines its focus, immediately halting the exploration process upon acquiring sufficient knowledge to answer the query. To facilitate training, we first extract hierarchical video captions from CGBench, a video corpus with grounding annotations, and guide GPT-5 to generate 33K high-quality chain-of-thought-with-tool trajectories. The LongVideo-R1 agent is fine-tuned upon the Qwen-3-8B model through a two-stage paradigm: supervised fine-tuning (SFT) followed by reinforcement learning (RL), where RL employs a specifically designed reward function to maximize selective and efficient clip navigation. Experiments on multiple long video benchmarks validate the effectiveness of name, which enjoys superior tradeoff between QA accuracy and efficiency. All curated data and source code are provided in the supplementary material and will be made publicly available.
</details>

---

### Thinking in Uncertainty: Mitigating Hallucinations in MLRMs with Latent Entropy-Aware Decoding
著者: Zhongxing Xu, Zhonghua Wang, Zhe Qian, Dachuan Shi, feilong tang, Ming Hu, Shiyan Su, Xiaocheng Zou, Wei Feng, Dwarikanath Mahapatra, Yifan Peng, Mingquan Lin, Zongyuan Ge

<details>
<summary> 日本語要旨 </summary>

最近の多モーダル大規模推論モデル（MLRM）の進歩により、視覚的な質問応答のパフォーマンスが大幅に向上しました。しかし、私たちは移行語（例えば、「because」や「however」、「wait」など）がハロゲンと密接に関連しており、高エントロピー状態を示す傾向があることを観察しました。私たちは、適切な文脈的推論情報がトークンの確率分布から直接抽出できると主張します。スーパーポジション表現理論に触発され、私たちは潜在的なスーパーポジション推論を利用して複数の候補セマンティクスを統合し、潜在的な推論トラジェクトリーを維持することを提案します。仮説は、モデルが連続的な明示的推論に向かう可能性があり、高エントロピーの推論段階で密度のある文脈的手掛かりを十分に活用していないというものです。したがって、トークンの確率分布から豊富なセマンティック表現を構築することで、文脈的推論を強化することを提案します。この目的を達成するために、私たちはLatent Entropy-Aware Decoding（LEAD）を提示します。これは、セマンティックコンテキストを活用して信頼性のある推論を実現する効率的なプラグアンドプレイデコーディング戦略です。私たちの方法の核心は、エントロピーに気づいた推論モードスイッチングにあります。モデルは高エントロピー状態で確率重み付き連続埋め込みを使用し、エントロピーが減少すると離散トークン埋め込みに戻ります。さらに、モデルが視覚情報に焦点を当てるよう促すための事前知識ガイド付きビジュアルアンカー注入戦略を提案します。広範な実験は、LEADがさまざまなMLRMおよび複数のベンチマークでハロゲンを効果的に緩和することを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advancements in multimodal large reasoning models (MLRMs) have significantly improved performance in visual question answering. However, we observe that transition words (e.g., because, however, and wait) are closely associated with hallucinations and tend to exhibit high-entropy states. We argue that adequate contextual reasoning information can be directly extracted from the token probability distribution. Inspired by superposed representation theory, we propose leveraging latent superposed reasoning to integrate multiple candidate semantics and maintain latent reasoning trajectories. The hypothesis is that reliance on discrete textual inputs may drive the model toward sequential explicit reasoning, underutilizing dense contextual cues during high-entropy reasoning stages. Therefore, we propose constructing rich semantic representations from the token probability distributions to enhance in-context reasoning. With this goal, we present Latent Entropy-Aware Decoding (LEAD), an efficient plug-and-play decoding strategy that leverages semantic context to achieve reliable reasoning. The heart of our method lies in entropy-aware reasoning mode switching. The model employs probability-weighted continuous embeddings under high-entropy states and transitions back to discrete token embeddings as entropy decreases. Moreover, we propose a prior-guided visual anchor injection strategy that encourages the model to focus on visual information. Extensive experiments show that LEAD effectively mitigates hallucinations across various MLRMs on multiple benchmarks.
</details>

---

### Adversarial Style Optimization: Enhancing VLM Jailbreaks By GRPO-based Stylistic Triggers Optimization
著者: Bingjun Luo, Jialin Guo, Yue Yao, Xinpeng Ding

<details>
<summary> 日本語要旨 </summary>

多モーダル大規模言語モデル（MLLMs）は印象的な性能を達成していますが、その安全性の整合性は脱獄攻撃に対して依然として脆弱です。既存のコンテンツベースの脱獄攻撃はしばしば不一致であり、商用クローズソースMLLMsに対する攻撃成功率（ASR）が低く、非コンテンツベースの脆弱性を悪用していません。これまでの研究とは異なり、私たちは実証的にMLLMsがスタイリッシュ・インコンシステンシーを示すことを発見しました。つまり、理解能力から見ると、MLLMsは視覚的なスタイル（例えば、「鉛筆画」）に関わらずコンテンツを堅牢に理解できますが、安全性能の観点から見ると、これら特定のスタイリッシュなトリガーによって防御メカニズムが容易に回避され、有害な応答を引き起こします。この発見に基づいて、私たちは既存の視覚的脱獄攻撃を増幅するプラグアンドプレイ型の強化モジュールであるAdversarial Style Optimization（ASO）を提案します。ASOは画像編集モデルを微調整し、与えられた敵対的な画像に最適化されたスタイリッシュな修正を重ね合わせます。私たちはグループ相対政策最適化（GRPO）エージェントを適用し、構造的階層報酬関数によって導かれます。この関数は明示的な拒否の検出に使用されるログベースの信号と強力な裁判官モデルから得られた高精細度の意味評価を独自に組み合わせ、結果を重複しない異なる報酬階層にマッピングし、最も有効なスタイリッシュパラメータを選択します。広範囲の実験では、ASOがSOTA攻撃のASRを大幅に向上させることが示されました。GRPOエージェントは最適で直感的でないパラメータを自動的に発見し、スタイリッシュバイアスがMLLMsのレッドチーム向けの拡張可能かつモジュール化されたベクトルであることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Multimodal Large Language Models (MLLMs) have achieved impressive performance, but their safety alignment remains vulnerable to jailbreak attacks. Existing content-based jailbreaks are often inconsistent and show low attack success rates (ASR) against commercial closed-source MLLMs, failing to exploit non-content-based vulnerabilities. Unlike previous research, we empirically find that MLLMs exhibit a Stylistic Inconsistency between their comprehension ability and safety ability. That is, from the perspective of comprehension, MLLMs can robustly understand content regardless of visual style (e.g., "pencil sketch"). However, from the perspective of safety ability, their defense mechanisms can be easily bypassed by these specific stylistic triggers, leading to harmful responses. Based on this finding, we propose Adversarial Style Optimization (ASO), a plug-and-play enhancement module to amplify existing visual jailbreaks. ASO fine-tunes an image-editing model to superimpose an optimized stylistic modification onto a given adversarial image. We apply a Group Relative Policy Optimization (GRPO) agent, guided by a Structurally-Tiered Reward Function. This function uniquely combines a logit-based signal for detecting explicit refusals with a high-fidelity semantic evaluation from a powerful judge model, mapping outcomes to distinct, non-overlapping reward tiers to select the most potent stylistic parameters. Extensive experiments show that ASO significantly enhances the ASR of SOTA attacks. The GRPO agent automatically discovers optimal, non-intuitive parameters, demonstrating that stylistic biases are a scalable and modular vector for red-teaming MLLMs.
</details>

---

### DVGT: Visual Geometry Transformer for Autonomous Driving
著者: Sicheng Zuo, Zixun Xie, Wenzhao Zheng, Shaoqing Xu, Fang Li, Shengyin Jiang, Long Chen, Zhixin Yang, Jiwen Lu

<details>
<summary> 日本語要旨 </summary>

自動運転において、視覚入力から3Dシーンの幾何学を認識し再構築することは重要です。しかし、異なるシナリオやカメラ設定に適応できる密度の高い幾何学認識モデルが不足しています。このギャップを埋めるために、自動運転向けに特別に設計されたビジュアルジオメトリーテンショナー（DVGT）を提案します。これは、ポーズのないマルチビュー視覚入力のシーケンスからグローバルな密度3D点マップを再構築します。まず各画像から視覚特徴を抽出し、画像間で幾何学的関係を推測するために交互のインタービュー局所注意、クロスビュースペーシャル注意、クロスフレーム時間的注意を用います。最後に、複数のヘッドを使用して、最初のフレームのエゴ座標でグローバルな点マップと各フレームのエゴ姿勢をデコードします。私たちのDVGTは画像シーケンスから直接メトリックスケールの幾何学を予測し、外部センサーによるポストアライメントを不要とします。nuScenes、OpenScene、Waymo、KITTI、DDADなどの大規模な運転データセットの混合でトレーニングされたDVGTは、さまざまなシナリオにおいて他の幾何学予測モデルを大きく上回ります。
</details>

<details>
<summary> 英語要旨 </summary>

Perceiving and reconstructing 3D scene geometry from visual inputs is crucial for autonomous driving. However, it still lacks a driving-targeted dense geometry perception model that can adapt to different scenarios and camera configurations. To bridge this gap, we propose a Visual Geometry Transformer specifically designed for autonomous Driving (DVGT), which reconstructs a global dense 3D point map from a sequence of unposed multi-view visual inputs. We first extract visual features for each image and employ alternating intra-view local attention, cross-view spatial attention, and cross-frame temporal attention to infer geometric relations across images. Finally, we use multiple heads to decode a global point map in the ego coordinate of the first frame and the ego pose for each frame. Our DVGT directly predicts metric-scaled geometry from image sequences, eliminating the need for post-alignment with external sensors. Trained on a large mixture of driving datasets, including nuScenes, OpenScene, Waymo, KITTI, and DDAD, DVGT significantly outperforms the other geometry prediction models on various scenarios.
</details>

---

### FINER: MLLMs Hallucinate Under Fine-grained Negative Queries
著者: Rui Xiao, Sanghwan Kim, Yongqin Xian, Zeynep Akata, Stephan Alaniz

<details>
<summary> 日本語要旨 </summary>

多モーダル大規模言語モデル（MLLMs）は、特に細部にわたる質問で幻覚を引き起こす傾向があります。これまでの基準では、画像関連の粗い質問に焦点を当てており、この課題は十分に表現されていません。私たちは**FI**ne-grained **NE**gative que**R**ies（**FINER**）という新しい基準を導入します。これに加えて、**FINER-CompreCap**および**FINER-DOCCI**の2つのベンチマークも紹介します。FINERを使用して、複数のオブジェクト、属性、関係、そして「何」に関する質問という4つの設定で幻覚を分析しました。私たちのベンチマークは、細部の不一致が画像内に実際に存在する要素と共起した場合にMLLMsが幻覚を引き起こすことを明らかにしました。これに対処するために、FINERに触発されたデータでDirect Preference Optimization（DPO）を利用した**FINER-Tuning**を提案します。4つの先進的なMLLMsをFINER-Tuningで微調整することで、私たちのベンチマークにおける幻覚からInternVL3.5-14Bで最大24.2%の向上が見られました。また、8つの既存の幻覚スイートでのパフォーマンスも改善し、6つのベンチマークにわたる一般的な多様性能力を向上させました。ベンチマーク、トレーニングデータ、コードおよびモデルチェックポイントは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Multimodal large language models (MLLMs) struggle with hallucinations, particularly with fine-grained queries, a challenge underrepresented by existing benchmarks that focus on coarse image-related questions. We introduce **FI**ne-grained **NE**gative que**R**ies (**FINER**), alongside two benchmarks: **FINER-CompreCap** and **FINER-DOCCI**. Using FINER, we analyze hallucinations across four settings: multi-object, multi-attribute, multi-relation, and “what” questions. Our benchmarks reveal that MLLMs hallucinate when fine-grained mismatches co-occur with genuinely present elements in the image. To address this, we propose **FINER-Tuning**, leveraging Direct Preference Optimization (DPO) on FINER-inspired data. Finetuning four frontier MLLMs with FINER-Tuning yields up to 24.2% gains (InternVL3.5-14B) on hallucinations from our benchmarks, while simultaneously improving performance on eight existing hallucination suites, and enhancing general multimodal capabilities across six benchmarks. Benchmarks, training data, code and model checkpoints will be released.
</details>

---

### Omni-Supervised Motion Editing: Balancing Change and Invariance Through Positive-Negative Learning
著者: Zhenwu Shi, Jingyu Gong, Peiwei Wang, Xingzan Wang, Tianwen Qian, Wenxi Li, Yuan Fang, Jiao Xie, Lizhuang Ma, Shaohui Lin

<details>
<summary> 日本語要旨 </summary>

テキストベースの人間動作編集は、自然言語指示に基づいて既存の動作シーケンスを変更し、元の動作の一貫性を保つことを目的としています。既存の拡散ベースのアプローチはしばしばヒューリスティックな類似性手がかりや粗いグローバル条件付けに依存し、動作の歪みと最適でない意味合わせを引き起こします。主要な課題は変化（つまり、ターゲット領域を正確に編集する）と不変性（つまり、未編集部分を保持する）のバランスを取ることです。このような課題に対処するために、私たちはオムニ・サプライズド・ポジティブ・ネガティブ学習フレームワークであるOmniMEを提案します。私たちの方法は三つの補完的なコンポーネントを統合しています：（1）トランスフォーマ層間の粗いから細かい一貫性を強制するレトロスペクティブ特徴監督、（2）ソースとターゲットの類似性に基づく微妙な変動に焦点を当てる動作保持メカニズム、および（3）テキスト-動作対応を強化するトリプレットベースの意味合わせ。これらのコンポーネントは変化と不変性のバランスを取る統一された監督パラダイムを形成します。MotionFixおよびSTANCE調整データセットにおける広範な実験では、**OmniMEは編集のアラインメントにおいて最先端の性能を達成し**、私たちの統一学習フレームワークの有効性が確認されました。コードは受理後に公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Text-based human motion editing aims to modify existing motion sequences according to natural language instructions while maintaining the consistency of the original motion. Existing diffusion-based approaches often rely on heuristic similarity cues or coarse global conditioning, leading to motion distortion and suboptimal semantic alignment. The key challenge lies in balancing change (i.e. precisely editing target regions) and invariance (i.e. preserving unedited parts). To handle such challenge, we propose an Omni-Supervised Positive-Negative Learning framework, named OmniME. Our method integrates three complementary components: (1) retrospective feature supervision that enforces coarse-to-fine consistency across transformer layers,(2) motion preservation mechanism that focuses on subtle variations accoding to the source-target similarity, and (3) triplet-based semantic alignment that strengthens text-motion correspondence. Together, these components form a unified supervision paradigm that balances change and invariance. Extensive experiments on the MotionFix and STANCE Adjustment datasets demonstrate that **OmniME achieves state-of-the-art performance in editing alignment**, validating the effectiveness of our unified learning framework. The code will be made publicly available uppon acceptance.
</details>

---

### VisionDirector: Vision-Language Guided Closed-Loop Refinement for Generative Image Synthesis
著者: Meng Chu, Senqiao Yang, Haoxuan Che, Suiyun Zhang, Xichen Zhang, Shaozuo Yu, Haokun GUI, Zhefan Rao, Dandan Tu, Rui Liu, Jiaya Jia

<details>
<summary> 日本語要旨 </summary>

生成モデルは現在、写実的な画像を生成できますが、プロのデザイナーが発行する長くて多目標の指示に対してまだ苦労しています。このギャップを明らかにし、モデルの実際のパフォーマンスをより良く評価するために、私たちは2000タスクからなる新しいテストセットである**LGBench（ロングゴールベンチ）**を導入します。このテストセットは1000のT2Iと1000のI2Iタスクで構成され、指示の平均的な長さはグローバルレイアウト、ローカルオブジェクト配置、タイポグラフィー、ロゴの忠実度を含む18〜22の密接に結びついた目標で構成されています。私たちは最先端の商用APIでも目標の72％未満しか満たしておらず、ローカライズされた編集を頻繁に見逃すことが確認され、現在のパイプラインの脆弱性が明らかになりました。これに対処するために、トレーニング不要でビジョン言語監督を行う**VisionDirector**を提案します。このシステムは（i）長い指示から構造化された目標を抽出し、（ii）一発生成と段階的編集の間で動的に決定し、（iii）各編集後にマイクログリッドサンプリングとセマンティックな検証/ロールバックを実行し、（iv）目標レベルの報酬を記録します。さらに、計画者をGroup Relative Policy Optimizationで微調整することで、編集経路が短くなり（3.1対4.2ステップ）、より強いアライメントが得られます。VisionDirectorはGenEvalで新たな最高記録を達成し（全体で+7％）、ImgEditでも絶対値で+0.07の向上を示しながら、タイポグラフィー、複数オブジェクトシーン、姿勢編集において一貫した質的な改善を達成しました。コード、ベンチマーク、評価スクリプトは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Generative models can now produce photorealistic imagery, yet they still struggle with the long, multi-goal prompts that professional designers issue. To expose this gap and better evaluate models’ performance in real-world, we introduce Long Goal Bench(**LGBench**), a 2000-task suite (1000 T2I, 1000 I2I) whose average instruction contains 18---22 tightly coupled goals spanning global layout, local object placement, typography, and logo fidelity. We find even state-of-the-art commercial APIs satisfy fewer than 72\% of the goals and routinely miss localized edits, confirming the brittleness of current pipelines. To address this, we present **VisionDirector**, a training-free, vision-language supervisor that (i) extracts structured goals from long instructions, (ii) dynamically decides between one-shot generation and staged edits, (iii) runs micro-grid sampling plus semantic verification/rollback after every edit, and (iv) logs goal-level rewards. We further fine-tune the planner with Group Relative Policy Optimization, yielding shorter edit trajectories (3.1 vs.\ 4.2 steps) and stronger alignment. VisionDirector achieves new state of the art on GenEval (+7\% overall), and ImgEdit (+0.07 absolute) while producing consistent qualitative improvements on typography, multi-object scenes, and pose editing. The code, benchmark, and evaluation scripts will be released.
</details>

---

### AlcheMinT: Fine-grained Temporal Control for Multi-Reference Consistent Video Generation
著者: Sharath Girish, Viacheslav Ivanov, Tsai-Shien Chen, Hao Chen, Aliaksandr Siarohin, Sergey Tulyakov

<details>
<summary> 日本語要旨 </summary>

最近の大規模拡散モデルを用いた主題駆動型ビデオ生成技術は、ユーザー提供の主題に基づくパーソナライズされたコンテンツ合成を可能にしました。しかし、既存の方法では、主題の出現と消失に対する細かい時間制御が欠けており、これは構成ビデオ合成、ストーリーボード作成、コントロール可能なアニメーションなどの応用に不可欠です。私たちは、主題駆動型ビデオ生成における明示的なタイムスタンプ条件付けを導入する統一フレームワークであるAlcheMinTを提案します。私たちのアプローチでは、主題の識別に関連付けられた時間間隔のエンコードを可能にする新しい位置符号化メカニズムを導入しています。これは、予め学習されたビデオ生成モデルの位置符号化とシームレスに統合されています。さらに、主題記述テキストトークンを追加することで、視覚的なアイデンティティとビデオキャプションの間の結びつきを強化し、生成時の曖昧さを軽減します。トークンごとの連結により、AlcheMinTは追加のクロスアテンションモジュールを必要とせず、無視できるパラメータオーバーヘッドしか発生しません。私たちは、複数主題のアイデンティティ保持、ビデオの忠実度、時間的遵守を評価するベンチマークを確立しています。実験結果は、AlcheMinTが最先端のビデオパーソナライズ方法と同等の視覚品質を達成し、初めて複数主題生成における正確な時間制御を可能にすることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advances in subject-driven video generation with large diffusion models have enabled personalized content synthesis conditioned on user-provided subjects. However, existing methods lack fine-grained temporal control over subject appearance and disappearance, which are essential for applications such as compositional video synthesis, storyboarding, and controllable animation. We propose AlcheMinT, a unified framework that introduces explicit timestamps conditioning for subject-driven video generation. Our approach introduces a novel positional encoding mechanism that unlocks the encoding of temporal intervals, associated in our case with subject identities, while seamlessly integrating with the pretrained video generation model positional embeddings. Additionally, we incorporate subject-descriptive text tokens to strengthen binding between visual identity and video captions, mitigating ambiguity during generation. Through token-wise concatenation, AlcheMinT avoids any additional cross-attention modules and incurs negligible parameter overhead. We establish a benchmark evaluating multiple subject identity preservation, video fidelity, and temporal adherence. Experimental results demonstrate that AlcheMinT achieves visual quality matching state-of-the-art video personalization methods, while, for the first time, enabling precise temporal control over multi-subject generation within videos.
</details>

---

### Lightmover: Towards Precise and Efficient Control for Light Movement
著者: Gengze Zhou, Tianyu Wang, Soo Ye Kim, ZHIXIN SHU, Xin Yu, Yannick Hold-Geoffroy, Sumit Chaturvedi, Qi Wu, Zhe Lin, Scott Cohen

<details>
<summary> 日本語要旨 </summary>

私たちは、ビデオ拡散事前知識を活用してシーンの再レンダリングなしに物理的に妥当な照明変更を生成する単一画像での制御可能な光操作フレームワーク「LightMover」を提案します。私たちは、与えられた画像と光制御トークンに基づいて、光の位置、色、強度を調整し、それに伴う反射、影、フェローフを単一視点から同時に処理することで、光編集をビジュアルトークン空間でのシーケンス予測問題として定式化します。この空間的（移動）および外観（色、強度）制御の統一処理により、操作性と照明理解が向上します。さらに、空間情報を保持しつつ非空間属性をコンパクトにエンコードすることで制御シーケンス長を41％削減し、編集の忠実性を維持する適応的なトークンプルーニングメカニズムを導入します。私たちのフレームワークを訓練するために、光の位置、色、強度が変化してもシーン内容が元画像と一致したまま大量の画像ペアを生成できるスケーラブルなレンダリングパイプラインを構築します。私たちの手法は、光の位置、色、強度に対して正確かつ独立した制御を可能にし、さまざまなタスクで高いPSNRと強力な意味的一貫性（DINO、CLIP）を達成します。
</details>

<details>
<summary> 英語要旨 </summary>

We present LightMover, a framework for controllable light manipulation in single images that leverages video diffusion priors to produce physically plausible illumination changes without re-rendering the scene. We formulate light editing as a sequence-to-sequence prediction problem in visual token space: given an image and light-control tokens, the model adjusts light position, color, and intensity together with resulting reflections, shadows, and falloff from a single view. This unified treatment of spatial (movement) and appearance (color, intensity) controls improves both manipulation and illumination understanding. We further introduce an adaptive token-pruning mechanism that preserves spatially informative tokens while compactly encoding non-spatial attributes, reducing control sequence length by 41\% while maintaining editing fidelity. For training our framework, we construct a scalable rendering pipeline that can generate large numbers of image pairs across varied light positions, colors, and intensities while keeping the scene content consistent to the original image. \ours enables precise, independent control over light position, color, and intensity, and achieves high PSNR and strong semantic consistency (DINO, CLIP) across different tasks.
</details>

---

### Dynamics-Aware Preference Optimization for Vision-Language Models
著者: jusheng zhang, Kaitong Cai, Jing Yang, Jian Wang, Keze Wang

<details>
<summary> 日本語要旨 </summary>

視覚言語モデル（VLM）の好みに基づく微調整は、無意味な勾配を導入し最適化を歪め、キャリブレーションを低下させるため、不安定であることが知られています。本研究では、学習ダイナミクスの観点からこの問題を再検討し、「圧縮効果」と呼ばれる根本的な病理を特定します。これは、ほとんど無視できる損失にもかかわらず、容易な負例が大きく不整合な勾配を保持し続ける現象です。この問題に対処するため、私たちは「Cooling-Weighted Direct Preference Optimization（CW-DPO）」という2段階のフレームワークを提案します。これはまず整合性プロセスを滑らかにし、次に安定化させます。第1段階では、「ソフトな負例」を用いた制約付きSFT（シンプル・ファインチューニング）フェーズで過信した分布を正則化し、損失の地形を平坦にします。第2段階では、モデルの各トークンごとの対数確率の平均値に基づいて負例の勾配を適応的にスケーリングする「能力認識冷却重み」を導入します。これにより、無意味な更新を抑制しつつ、難しいオンポリシーの対比を強調します。このダイナミクスに配慮した重み付けは圧縮効果を効果的に軽減し、より滑らかな収束を可能にします。COCO、Flickr30k、NoCaps、MMMU、および MMBench1.1といった主流のベンチマークで行われた広範囲な実験では、CW-DPOが最先端の性能を達成しました。例えば、PPOに対して+3.4 CIDEr、MMMUで絶対精度+2.4%という改善を示し、キャリブレーションも向上させながら収束ステップ数を半分に削減しています。これは、滑らかにすることで冷却するというシンプルでありながら一般的な原理が堅牢なVLMの好みに基づく最適化において重要であることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Preference-based finetuning of vision-language models (VLMs) is notoriously unstable, as trivially wrong negatives inject uninformative gradients that distort optimization and degrade calibration. This work revisits this issue through the lens of learning dynamics and identifies a core pathology, the squeezing effect, where easy negatives retain large, misaligned gradients despite having negligible loss. To address this, we propose Cooling-Weighted Direct Preference Optimization (CW-DPO), a two-stage framework that first smooths and then stabilizes the alignment process. Stage 1 employs a constrained SFT phase with low-weight “gentle negatives’’ to regularize overconfident distributions and flatten the loss landscape. Stage 2 introduces a competence-aware cooling weight that adaptively scales negative gradients according to the model’s average per-token log-probability, suppressing uninformative updates while emphasizing hard, on-policy contrasts. This dynamics-aware weighting effectively mitigates the squeezing effect and enables smoother convergence. Extensive experiments on mainstream benchmarks—including COCO, Flickr30k, NoCaps, MMMU, and MMBench1.1—show that CW-DPO achieves state-of-the-art performance, for example +3.4 CIDEr over PPO and +2.4% absolute accuracy on MMMU, while improving calibration and halving convergence steps. This demonstrates that smoothing before cooling constitutes a simple yet general principle for robust VLM preference optimization.
</details>

---

### HTC-VLM: Disentangled Hybrid Token Compression for Vision-Language Models
著者: jusheng zhang, Xiaoyang Guo, Kaitong Cai, Qinhan Lyu, Yijia Fan, Wenhao Chai, Jian Wang, Keze Wang

<details>
<summary> 日本語要旨 </summary>

ビジョン言語モデル（VLM）はマルチモーダル推論を変革しましたが、LLMに数百の視覚パッチトークンを供給すると二次的な計算コストがかかり、メモリやコンテキストウィンドウに負担をかけます。従来のアプローチは継続的な圧縮が高レベルのセマンティクス（例えば、オブジェクトの識別）を希釈し、離散量子化が細部（例えば、テクスチャー）を失うというトレードオフに直面しています。私たちはこの問題に対処するために**HTC-VLM**を導入します。これはセマンティクスと外観を二重チャネルで分離し、ViTパッチを用いた細部の継続的な経路と、MGVQ量子化によるシンボリックアンカーを4トークンに投影した離散経路で構成されています。これらは580トークンのハイブリッドシーケンスとして融合し、分離注意マスクと`<voco>`ボトルネックを用いて1トークンに圧縮され、効率的で根拠のある表現が保証されます。HTC-VLMは7つのベンチマーク（GQA, VQAv2, MMBench, MME, POPE, SEED-Bench, ScienceQA-Image）において平均**87.2%**のパフォーマンスを維持し、580対1の圧縮比率で最先端の連続ベースライン（**81.0%**）を上回ります。注意分析によると、圧縮されたトークンは離散アンカーを優先し、そのセマンティックガイダンスが検証されています。私たちの作業は、ミニマリストなハイブリッドが効率と忠実性のジレンマを解決し、スケーラブルなVLMsの進展に寄与することを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Vision-language models (VLMs) have transformed multimodal reasoning, but feeding hundreds of visual patch tokens to LLMs incurs quadratic computational costs, straining memory and context windows. Traditional approaches face a trade-off: continuous compression dilutes high-level semantics like object identities, while discrete quantization loses granular details such as textures. We challenge this by introducing **HTC-VLM**, a hybrid framework that disentangles semantics and appearance through dual channels, i.e., a continuous pathway for fine-grained details via ViT patches and a discrete pathway for symbolic anchors using MGVQ quantization projected to four tokens. These are fused into a 580-token hybrid sequence and compressed to one token via a disentanglement attention mask and a `<voco>` bottleneck, ensuring efficient, grounded representations. HTC-VLM achieves an average performance retention of **87.2%** across seven benchmarks (GQA, VQAv2, MMBench, MME, POPE, SEED-Bench, ScienceQA-Image), outperforming the leading continuous baseline at **81.0%** with a 580-to-1 compression ratio. Attention analyses show the compressed token prioritizes the discrete anchor, validating its semantic guidance. Our work demonstrates that a minimalist hybrid can resolve the efficiency–fidelity dilemma, advancing scalable VLMs.
</details>

---

### PDCR: Perception-Decomposed Confidence Reward for Vision-Language Reasoning
著者: Hee Suk Yoon, Eunseop Yoon, Ji Woo Hong, SooHwan Eom, Gwanhyeong Koo, Mark A. Hasegawa-Johnson, Qi Dai, Chong Luo, Chang D. Yoo

<details>
<summary> 日本語要旨 </summary>

従来の強化学習における検証可能な報酬（RLVR）は、結果ベースの希薄な信号に依存してきました。最近の研究では、グラウンドトゥルースの答えへの自信の成長を報酬とすることで、コストのかかる外部モデルなしにステップレベルの指導を提供し、言語推論トレーニングを効果的に改善できることが示されています。これは単一モードのテキストに対して有効ですが、視覚言語（V-L）推論にこのグローバルな報酬を素朴に適用すると、タスクが希薄な視覚知覚と密度の高いテキスト的推論のヘテロジニアスな混合物であるため、最適ではありません。このグローバルな正規化は、主にテキストステップによって統計的に歪められることで、視覚ステップのトレーニング信号が混合物誘発の信号劣化を引き起こします。私たちは、この問題を解決するPerception-Decomposed Confidence Reward（PDCR）というフレームワークを提案します。これは、タスクのヘテロジニアスな性質に報酬構造を合わせることで解決します。PDCRはまず無監督のスキル分解を行い、視覚依存度を定量化するモデル内部のVisual Dependence Scoreを導入し、知覚と推論ステップを分離するクラスタリングアルゴリズムを適用します。これに基づき、PDCRは各スキルクラスタ内で自信の増加を正規化して分解された利点を計算します。このインタークラスタ正規化は、知覚と推論の両方に安定した適切なスケールの信号を提供します。私たちは、PDCRが素朴なグローバル報酬形式や希薄報酬ベースラインを上回り、主要なV-L推論ベンチマークで優れた性能を発揮することを示します。
</details>

<details>
<summary> 英語要旨 </summary>

Reinforcement Learning with Verifiable Rewards (RLVR) traditionally relies on a sparse, outcome-based signal. Recent work shows that providing a fine-grained, model-intrinsic signal—rewarding the confidence growth in the ground-truth answer—effectively improves language reasoning training by providing step-level guidance without costly external models. While effective for unimodal text, we find that naively applying this global reward to vision-language (V-L) reasoning is a suboptimal strategy, as the task is a heterogeneous mix of sparse visual perception and dense textual reasoning. This global normalization creates mixture-induced signal degradation, where the training signal for visual steps is statistically distorted by the predominant textual steps. We propose Perception-Decomposed Confidence Reward (PDCR), a framework that solves this by aligning the reward structure with the task's heterogeneous nature. PDCR first performs an unsupervised skill decomposition, introducing a model-internal Visual Dependence Score to quantify visual reliance and applying a clustering algorithm to separate perception and reasoning steps. Based on this, PDCR computes a decomposed advantage by normalizing confidence gains within each skill cluster. This intra-cluster normalization provides a stable, correctly-scaled signal for both perception and reasoning. We demonstrate that PDCR outperforms the naive, global-reward formulation and sparse-reward baselines on key V-L reasoning benchmarks.
</details>

---

### TINA: Text-Free Inversion Attack for Unlearned Text-to-Image Diffusion Models
著者: Qianlong Xiang, Miao Zhang, Haoyu Zhang, Kun Wang, Junhui Hou, Liqiang Nie

<details>
<summary> 日本語要旨 </summary>

テキストから画像への拡散モデルは驚異的な生成能力を示していますが、有害なコンテンツの作成を防ぐために概念消去技術が必要です。これにより、エラスター防御策とそれらを回避しようとする敵対的プローブの開発との間で動的な相互作用が生まれ、この共進化は消去方法の効果を段階的に向上させてきました。しかし、この敵対的共進化はテキスト中心の狭いパラダイムに収束し、概念とその関連する視覚知識が消去されたわけではなく残存していることを無視しています。この主張を裏付けるために、私たちは視覚的観点から調査し、DDIM逆転を利用して消去された概念の生成経路がまだ見つかるかどうかを探ります。しかし、このような視覚的生成経路を特定することは難しいです。なぜなら、標準のテキストガイド付きDDIM逆転が消去されたモデル内のテキスト中心の防御によって積極的に抑制されるからです。これに対処するため、私たちはTINA（Text-free INversion Attack）を導入します。これは、存在するテキスト中心の防御を回避するためにヌルテキスト条件下で動作し、視覚的なみのプロービングを強制する新しい手法です。さらに、TINAは標準逆転が通常のテキストガイダンスなしで蓄積される近似誤差を克服するための最適化手順を統合しています。私たちの実験では、TINAが最先端のアンラーニング処理を受けたモデルから消去された概念を成功裏に再生成することを示しました。TINAの成功は現在の方法が単に概念を隠すだけであることを証明しており、内部視覚知識に直接作用するパラダイムへの緊急の必要性を浮き彫りにしています。コードは受理後に公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Although text-to-image diffusion models exhibit remarkable generative power, concept erasure techniques are essential for their safe deployment to prevent the creation of harmful content. This has fostered a dynamic interplay between the development of erasure defenses and the adversarial probes designed to bypass them, and this co-evolution has progressively enhanced the efficacy of erasure methods. However, this adversarial co-evolution has converged on a narrow, text-centric paradigm that equates erasure with severing the text-to-image mapping, ignoring that the underlying visual knowledge related to undesired concepts still persist. To substantiate this claim, we investigate from a visual perspective, leveraging DDIM inversion to probe whether a generative pathway for the erased concept can still be found. However, identifying such a visual generative pathway is challenging because standard text-guided DDIM inversion is actively resisted by text-centric defenses within the erased model. To address this, we introduce TINA, a novel Text-free INversion Attack, which enforces this visual-only probe by operating under a null-text condition, thereby avoiding existing text-centric defenses. Moreover, TINA integrates an optimization procedure to overcome the accumulating approximation errors that arise when standard inversion operates without its usual textual guidance. Our experiments demonstrate that TINA successfully regenerates erased concepts from models treated with state-of-the-art unlearning. The success of TINA proves that current methods merely obscure concepts, highlighting an urgent need for paradigms that operate directly on internal visual knowledge. Code will be released upon acceptance.
</details>

---

### VGG-T$^3$: Offline Feed-Forward 3D Reconstruction at Scale
著者: Sven Elflein, Ruilong Li, Sérgio Agostinho, Žan Gojčič, Laura Leal-Taixe, Qunjie Zhou, Aljoša Ošep

<details>
<summary> 日本語要旨 </summary>

私たちは、オフラインのフィードフォワード手法における重要な制約を解決するスケーラブルな3D再構成モデルを提案します。これらの方法は、入力画像数に対して計算量とメモリ要件が二次的に増加するという問題があります。私たちのアプローチは、このボトルネックが可変長のキー・バリュー（KV）空間表現から生じることを鍵にしており、これをテスト時学習を通じて固定サイズのマルチレイヤーパーセプトロン（MLP）に凝縮します。VGG-T$^3$（$\mathbf{V}$isual $\mathbf{G}$eometry $\mathbf{G}$rounded $\mathbf{T}$est $\mathbf{T}$ime $\mathbf{T}$raining）は、入力ビュー数に対してオンラインモデルと同様に線形的にスケールし、$1k$画像コレクションの再構成においてソフトマックス注意を用いるベースラインに対して約11.6倍の高速化を達成します。これはわずか54秒で実現されます。私たちの方法が全体的なシーン集積能力を保持するため、得られる点マップ再構成誤差はVGGTと同等です。
</details>

<details>
<summary> 英語要旨 </summary>

We present a scalable 3D reconstruction model that addresses a critical limitation in offline feed-forward methods: their computational and memory requirements grow quadratically w.r.t. the number of input images. Our approach is built on the key insight that this bottleneck stems from the varying-length Key-Value (KV) space representation of scene geometry, which we distill into a fixed-size Multi-Layer Perceptron (MLP) via test-time training. VGG-T$^3$ ($\mathbf{V}$isual $\mathbf{G}$eometry $\mathbf{G}$rounded $\mathbf{T}$est $\mathbf{T}$ime $\mathbf{T}$raining) scales linearly w.r.t. the number of input views, similar to online models, and achieves a $11.6\times$ speed-up over baselines that rely on softmax attention for reconstructing a $1k$ image collection in just $54$ seconds. Because our method retains global scene aggregation capability, our resulting point map reconstruction error is comparable to VGGT.
</details>

---

### MuCo: Multi-turn Contrastive Learning for Multimodal Embedding Model
著者: Geonmo Gu, Byeongho Heo, Jaemyung Yu, Jaehui Hwang, Taekyung Kim, Sangmin Lee, HeeJae Jun, Yoohoon Kang, Sangdoo Yun, Dongyoon Han

<details>
<summary> 日本語要旨 </summary>

従来の多様なモーダル埋め込みモデルは、異なるモダリティ間でクエリとターゲットペアの表現を整合させるために対比学習を用いて構築されてきました。これらの手法は実証的な成功を収めていますが、通常「シングルターン」形式で構築されており、各クエリ-ターゲットペアが独立したデータポイントとして扱われます。このパラダイムは、各ペアに対する別々のフォワードパスを必要とし、同じコンテキストに関連する複数のクエリ間の潜在的な文脈関係を見落とすため、スケーリング時に計算効率が低下します。本研究では、対話型インスピレーションフレームワークであるマルチターン対比学習（MuCo）を導入し、このプロセスを再考しています。MuCoはMLLMsの会話的性質を活用し、単一の画像に関連する複数のクエリ-ターゲットペアを単一のフォワードパスで処理します。これにより、共有コンテキスト表現に条件付けられた複数のクエリとターゲット埋め込みを同時に抽出することが可能となり、効果的なバッチサイズを増加させ、全体的なトレーニング効率を向上させます。実験では、MuCoは新たに構築された5Mの多様なモダリティマルチターンデータセット（M3T）と共に使用し、MMEBおよびM-BEIRベンチマークで最先端の検索性能を達成する一方で、トレーニング効率と異なるモダリティ間の表現の整合性も大幅に向上しています。
</details>

<details>
<summary> 英語要旨 </summary>

Universal Multimodal embedding models built on Multimodal Large Language Models (MLLMs) have traditionally employed contrastive learning, which aligns representations of query-target pairs across different modalities. Yet, despite its empirical success, they are primarily built on a "single-turn" formulation where each query-target pair is treated as an independent data point. This paradigm leads to computational inefficiency when scaling, as it requires a separate forward pass for each pair and overlooks potential contextual relationships between multiple queries that can relate to the same context. In this work, we introduce Multi-Turn Contrastive Learning (MuCo), a dialogue-inspired framework that revisits this process. MuCo leverages the conversational nature of MLLMs to process multiple, related query-target pairs associated with a single image within a single forward pass. This allows us to extract a set of multiple query and target embeddings simultaneously, conditioned on a shared context representation, amplifying the effective batch size and overall training efficiency. Experiments exhibit MuCo with a newly curated 5M multimodal multi-turn dataset (M3T), which yields state-of-the-art retrieval performance on MMEB and M-BEIR benchmarks, while markedly enhancing both training efficiency and representation coherence across modalities.
</details>

---

### MeshFlow: Efficient Artistic Mesh Generation Via MeshVAE and Flow-based DiTs
著者: Weiyu Li, Antoine Toisoul, Tom Monnier, Roman Shapovalov, Rakesh Ranjan, Ping Tan, Andrea Vedaldi

<details>
<summary> 日本語要旨 </summary>

私たちは、アーティスト風の3Dメッシュを圧縮および生成する新しい方法であるMeshFlowを提案します。現在のメッシュジェネレータは、通常、次トークン予測として自動回帰（AR）手法を採用していますが、これはメッシュ接続性の離散的な性質により自然な選択です。しかし、推論コストがメッシュサイズの二乗に比例するため、スケーラビリティが悪いという問題があります。AR手法は頂点座標を離散化する必要があるため、量子化誤差が導入され、頂点の崩壊を引き起こす可能性があります。これらの課題に対処するため、連続的な頂点位置と離散的な接続性の両方を表現できるように、対比損失で監督された変分自己符号化器（VAE）を導入します。この隠れ空間は、従来のトークンベースのメッシュ表現よりも大幅にコンパクトです。次に、Rectified-Flow変換器に基づく3Dジェネレータを構築し、すべてのメッシュ頂点とエッジを並列で生成します。このモデルは、最速のARジェネレータよりも$26\times$高速にメッシュをサンプリングし、標準的なメッシュ生成指標において最先端の精度を達成します。
</details>

<details>
<summary> 英語要旨 </summary>

We present MeshFlow, a new method for compressing and generating artist-like 3D meshes. Current mesh generators often adopt Auto-Regressive (AR) next-token prediction, a natural choice given the discrete nature of mesh connectivity, which, however, scales poorly due to the inference cost being quadratic in mesh size. AR methods also require discretizing the vertex coordinates, which introduces quantization errors and can cause vertex collapse. To address these challenges, we introduce a Variational Autoencoder (VAE) that, supervised with a contrastive loss, represents both continuous vertex positions and discrete connectivity in a continuous latent space. This latent space is significantly more compact than prior token-based mesh representations. We then build a 3D generator based on a Rectified-Flow transformer, which generates all mesh vertices and edges in parallel. This model samples meshes $26\times$ faster than the fastest AR generator while also achieving state-of-the-art accuracy across standard mesh-generation metrics.
</details>

---

### FlexAvatar: Learning Complete 3D Head Avatars with Partial Supervision
著者: Tobias Kirschstein, Simon Giebenhain, Matthias Nießner

<details>
<summary> 日本語要旨 </summary>

私たちは、単一の画像から高品質で完全な3Dヘッドアバターを作成する方法としてFlexAvatarを紹介します。この課題の核心は、多視点データの限られた利用可能性と単眼トレーニングが不完全な3Dヘッド再構築をもたらす傾向にあります。この問題の根本原因は、単眼ビデオから学習する際に駆動信号とターゲット視点が絡み合っていることであると特定しました。これを解決するために、可変データソーストークン（バイアスシンク）を持つトランスフォーマベースの3Dポートレートアニメーションモデルを提案します。これにより、単眼および多視点データセットにわたる統一的なトレーニングが可能となります。この設計は、推論時に両方のデータソースの強みを活用します：単眼データからの強力な汎化能力と多視点監督からの完全な3D完全性。さらに、私たちのトレーニング手順は、アイデンティティ間の滑らかな補間と任意の入力観測数への柔軟なフィッティングを可能にする滑らかな潜在的アバタースペースをもたらします。単眼、少数ショット、および単眼アバター作成タスクでの広範な評価において、FlexAvatarの有効性を確認しました。多くの既存手法が視点外挿に苦戦していますが、FlexAvatarはリアルな顔のアニメーションを持つ完全な3Dヘッドアバターを生成します。
</details>

<details>
<summary> 英語要旨 </summary>

We introduce FlexAvatar, a method for creating high-quality and complete 3D head avatars from a single image. A core challenge lies in the limited availability of multi-view data and the tendency of monocular training to yield incomplete 3D head reconstructions. We identify the root cause of this issue as the entanglement between driving signal and target viewpoint when learning from monocular videos. To address this, we propose a transformer-based 3D portrait animation model with learnable data source tokens, so-called bias sinks, which enables unified training across monocular and multi-view datasets. This design leverages the strengths of both data sources during inference: strong generalization from monocular data and full 3D completeness from multi-view supervision. Furthermore, our training procedure yields a smooth latent avatar space that facilitates identity interpolation and flexible fitting to an arbitrary number of input observations. In extensive evaluations on single-view, few-shot, and monocular avatar creation tasks, we verify the efficacy of FlexAvatar. Many existing methods struggle with view extrapolation while FlexAvatar generates complete 3D head avatars with realistic facial animations.
</details>

---

### CompBench: Benchmarking Complex Instruction-guided Image Editing
著者: Bohan Jia, Wenxuan Huang, Yuntian Tang, Junbo Qiao, Jincheng Liao, Shaosheng Cao, Fei Zhao, Zhaopeng Feng, Zhouhong Gu, Zhenfei Yin, Lei Bai, Wanli Ouyang, Lin Chen, Fei Zhao, Zihan Wang, Yuan Xie, Shaohui Lin

<details>
<summary> 日本語要旨 </summary>

現実世界の応用がますます複雑なシーン操作を要求する中、既存の指示に基づく画像編集ベンチマークはタスクの複雑さを過度に単純化し、詳細で微細な指示が不足していることが多い。このギャップを埋めるために、私たちはCompBenchを導入する。これは複雑な指示に基づく画像編集のために特別に設計された大規模ベンチマークである。CompBenchは、微細な指示の従順性、空間的および文脈的推論を取り入れた挑戦的な編集シナリオを特徴とし、画像編集モデルの正確な操作能力を包括的に評価することができる。CompBenchを構築するために、私たちはカスタマイズされたタスクパイプラインを持つMLLM-人間協調フレームワークを提案する。さらに、編集意図を四つの主要な次元（位置、外観、動態、オブジェクト）に分離する指示解体戦略を提案し、これにより複雑な編集要件と指示がより密接に一致することを保証する。広範な評価は、CompBenchが現在の画像編集モデルの基本的な限界を明らかにし、次世代の指示に基づく画像編集システムの開発にとって重要な洞察を提供することを示している。
</details>

<details>
<summary> 英語要旨 </summary>

While real-world applications increasingly demand intricate scene manipulation, existing instruction-guided image editing benchmarks often oversimplify task complexity and lack comprehensive, fine-grained instructions. To bridge this gap, we introduce CompBench, a large-scale benchmark specifically designed for complex instruction-guided image editing. CompBench features challenging editing scenarios that incorporate fine-grained instruction following, spatial and contextual reasoning, thereby enabling comprehensive evaluation of image editing models' precise manipulation capabilities. To construct CompBench, We propose an MLLM-human collaborative framework with tailored task pipelines. Furthermore, we propose an instruction decoupling strategy that disentangles editing intents into four key dimensions: location, appearance, dynamics, and objects, ensuring closer alignment between instructions and complex editing requirements. Extensive evaluations reveal that CompBench exposes fundamental limitations of current image editing models and provides critical insights for the development of next-generation instruction-guided image editing systems.
</details>

---

### GlyphPrinter: Region-Grouped Direct Preference Optimization for Glyph-Accurate Visual Text Rendering
著者: Xincheng Shuai, Ziye Li, Henghui Ding, Dacheng Tao

<details>
<summary> 日本語要旨 </summary>

視覚的なテキストレンダリングにおいて正確なグリフを生成することは重要であるが、難しい。既存の方法は通常、高品質なシーンテキスト画像を大量に用いたトレーニングによってテキストレンダリングを向上させますが、グリフ変異の限定的なカバーや過度のスタイル化は特に複雑またはドメイン外の文字においてグリフの正確性を損なうことが多いです。一部の方法では強化学習を用いてこの問題を緩和しようとしますが、その報酬モデルは細かいグリフエラーに対して敏感でないテキスト認識システムに依存するため、誤ったグリフを含む画像でも高い報酬が与えられることがあります。Direct Preference Optimization（DPO）に触発されて、私たちは明示的な報酬モデルへの依存を排除する***GlyphPrinter***という好みに基づくテキストレンダリング方法を提案します。しかし、標準的なDPO目的関数は通常2つのサンプル間の全体的な好みしかモデル化しないため、グリフエラーが局所的に発生する視覚テキストレンダリングでは不十分です。この問題を解決するために、私たちは地域レベルのグリフ好みアノテーションを持つ***GlyphCorrector***データセットを構築し、アノテートされた領域におけるインター・インタラサンプルの好みを最適化する地域ベースの目的関数である***Region-Grouped DPO***（***R-GDPO***）を提案します。これによりグリフの正確性が大幅に向上します。さらに、制御可能なグリフ精度を持つ最適分布からサンプリングする***Regional Reward Guidance***という推論戦略を導入します。広範囲の実験により、提案されたGlyphPrinterがグリフの正確性で既存の方法を上回ることが示されており、スタイル化と精度のバランスも有利です。
</details>

<details>
<summary> 英語要旨 </summary>

Generating accurate glyphs for visual text rendering is essential yet challenging. Existing methods typically enhance text rendering by training on a large amount of high-quality scene text images, but the limited coverage of glyph variations and excessive stylization often compromise glyph accuracy, especially for complex or out-of-domain characters. Some methods leverage reinforcement learning to alleviate this issue, yet their reward models usually depend on text recognition systems that are insensitive to fine-grained glyph errors, so images with incorrect glyphs may still receive high rewards. Inspired by Direct Preference Optimization (DPO), we propose ***GlyphPrinter***, a preference-based text rendering method that eliminates reliance on explicit reward models. However, the standard DPO objective only models overall preference between two samples, which is insufficient for visual text rendering where glyph errors typically occur in localized regions. To address this issue, we construct the ***GlyphCorrector*** dataset with region-level glyph preference annotations and propose ***Region-Grouped DPO*** (***R-GDPO***), a region-based objective that optimizes inter- and intra-sample preferences over annotated regions, substantially enhancing glyph accuracy. Furthermore, we introduce ***Regional Reward Guidance***, an inference strategy that samples from an optimal distribution with controllable glyph accuracy. Extensive experiments demonstrate that the proposed GlyphPrinter outperforms existing methods in glyph accuracy while maintaining a favorable balance between stylization and precision.
</details>

---

### PSDesigner: Automated Graphic Design with A Human-Like Creative Workflow
著者: Xincheng Shuai, Song Tang, Yutong Huang, Henghui Ding, Dacheng Tao

<details>
<summary> 日本語要旨 </summary>

グラフィックデザインは、eコマースや広告などの分野で重要な役割を果たす創造的かつ革新的なプロセスです。しかし、ユーザーの意図を編集可能なデザインファイルに忠実に変換する自動化されたデザインシステムの開発は未解決の課題です。最近の研究では、強力なテキストから画像へのモデルやMLLMを活用してグラフィックデザインを支援するものがありますが、これらは通常プロフェッショナルなワークフローを簡略化し、結果として柔軟性や直感性に限界が生じています。この制約に対処するために、私たちは人間のデザイナーの創造的なワークフローを模倣する自動化されたグラフィックデザインシステムである***PSDesigner***を提案します。複数の専門コンポーネントに基づいて構築された***PSDesigner***は、ユーザーの指示に基づいて関連資産を収集し、デザインファイルを操作するためのツール呼び出しを自律的に推測して実行します。これには新しい資産の統合や劣った要素の洗練が含まれます。システムに強力なツール使用能力を与えるため、私たちは***CreativePSD***というデザインデータセットを構築しました。これは、多様なデザインシナリオや芸術スタイルにわたって操作トレースが付加された高品質のPSDデザインファイルを大量に含んでおり、モデルが専門家のデザイン手順を学習することを可能にします。広範な実験は、***PSDesigner***が多様なグラフィックデザインタスクで既存の方法を上回ることを示しており、非専門家でも簡単に生産品質のデザインを作成することが可能です。
</details>

<details>
<summary> 英語要旨 </summary>

Graphic design is a creative and innovative process that plays a crucial role in applications such as e-commerce and advertising. However, developing an automated design system that can faithfully translate user intentions into editable design files remains an open challenge. Although recent studies have leveraged powerful text-to-image models and MLLMs to assist graphic design, they typically simplify professional workflows, resulting in limited flexibility and intuitiveness. To address these limitations, we propose ***PSDesigner***, an automated graphic design system that emulates the creative workflow of human designers. Building upon multiple specialized components, ***PSDesigner*** collects theme-related assets based on user instructions, and autonomously infers and executes tool calls to manipulate design files, such as integrating new assets or refining inferior elements. To endow the system with strong tool-use capabilities, we construct a design dataset, ***CreativePSD***, which contains a large amount of high-quality PSD design files annotated with operation traces across a wide range of design scenarios and artistic styles, enabling models to learn expert design procedures. Extensive experiments demonstrate that ***PSDesigner*** outperforms existing methods across diverse graphic design tasks, empowering non-specialists to conveniently create production-quality designs.
</details>

---

### Unlocking Token Rewards Via Training-Free Reward Attribution
著者: WU Sitong, Haoru Tan, Bin Xia, Xichen Zhang, Jingyao Li, Shaofeng Zhang, Xiaojuan Qi, Bei Yu, Jiaya Jia

<details>
<summary> 日本語要旨 </summary>

この論文では、既存の深層報酬モデルからトークンレベルの報酬信号を抽出するために、非常に効率的で訓練不要な方法を提案します。私たちの核心的なアイデアは、全体のプロセス報酬を個々のトークンに帰属させることです。これは、各トークンが最終的なマクロスコピック報酬（例えば、プロセス報酬）に与える影響を推定することで行います。この影響は、トークンが意味的に空のトークンに置き換えられた場合の最終マクロスコピック報酬の変化として定義されます。この影響を素朴に計算することは計算上不可能であり、Nトークンシーケンスに対してPRMを通じてN回のフォワードパスが必要です。私たちは、非常に効率的な勾配ベースの推定器を提案することでこのボトルネックを克服します。具体的には、最初の順序のテイラー近似を使用し、影響計算をトークン埋め込みと空トークン埋め込みの差と報酬がトークン埋め込みに関してどう変化するかの勾配との内積に簡略化します。これにはフォワードパスとバックワードパスを1回ずつ行うだけで済みます。得られたトークンレベルの報酬により、標準的なRLアルゴリズムが追加の報酬モデル訓練を必要とせずに正確なクレジット割当てを行うことが可能になります。難解な推論ベンチマークでの実験では、私たちの方法がポリシーオプティマイゼーション効率を大幅に向上させ、LLMの推論能力の汎化性を強化することを示しています。私たちのP2Tは、Qwen2.5-VL-7B-InstructでMathVistaにおいて結果報酬より+4.9%、AIME24ではQwen2.5-Math-7Bで+11.5%向上し、約4倍の速さで収束します。私たちの結果は、微細な報酬形成の重要性を強調しており、既存のPRMからトークンレベルの監督を解放する簡単でプラグアンドプレイのソリューションを提供します。
</details>

<details>
<summary> 英語要旨 </summary>

In this paper, we propose an extremely efficient, training-free method to extract token-level reward signals directly from an existing deep reward model. Our core idea is to attribute the overall process reward to individual tokens by estimating each token's influence. This influence is defined as the change in the final macroscopic reward (e.g., the process reward) when a token is replaced with a semantically null token. Naively calculating this influence is computationally infeasible, requiring $N$ forward passes through the PRM for an $N$-token sequence. We overcome this bottleneck by proposing a highly efficient gradient-based estimator. Specifically, we use a first-order Taylor approximation, which simplifies the influence calculation to the inner product of the difference between the token embedding and the null token embedding, and the gradient of the reward with respect to the token embedding. This requires only a single forward and backward pass. The resulting token-level rewards enable standard RL algorithms to perform precise credit assignment without requiring additional reward model training. Experiments on challenging reasoning benchmarks demonstrate that our method substantially improves policy optimization efficiency and enhances the generalization of LLM reasoning capabilities. Our P2T outperforms the outcome reward by +4.9\% on MathVista for Qwen2.5-VL-7B-Instruct, and +11.5\% on AIME24 for Qwen2.5-Math-7B, while with a around 4$\times$ faster convergence. Our results underscore the importance of fine-grained reward shaping and provide a simple, plug-and-play solution to unlock token-level supervision from existing PRMs.
</details>

---

### Depth Peeling for High-Fidelity Gaussian-Enhanced Surfel Rendering
著者: Keyang Ye, Hongzhi Wu, Kun Zhou

<details>
<summary> 日本語要旨 </summary>

新しい視点合成は、NeRFsや3D Gaussian Splatting（3DGS）によって大きく進歩しており、正確な色のブレンドを行うためにボリューメトリックサンプルまたは原始体を順序付ける必要があります。最近のGaussian-Enhanced Surfels（GES）はソートフリーで高性能なレンダリングを可能にしますが、アーティファクトや非効率的な再構成といった問題があります。これらの制限に対処するために、私たちはDP-GESという新しい表現を提案します。この表現は不透明なサーフェルズに半透明の境界を追加し、Depth Peelingを利用してピクセルごとの正確な順序付けを行います。この設計により、ソートフリーで正しいトランスミッションモジュレーションを持つガウス分布スプラッティングが可能となり、アーティファクトの除去とポッピングアーティファクトの効果的な排除を実現し、完全に微分可能な統合最適化を促進します。広範囲のシーンでの詳細な実験は、私たちの方法が優れた再構成品質を達成し、最先端技術と比較して有利に競争することを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Novel view synthesis has been significantly advanced by NeRFs and 3D Gaussian Splatting (3DGS), which require ordering volumetric samples or primitives for correct color blending. While the recent Gaussian-Enhanced Surfels (GES) enable high-performance, sort-free rendering, they suffer from aliasing artifacts and suboptimal reconstruction. To address these limitations, we propose DP-GES, a novel representation that augments opaque surfels with semi-transparent boundaries and leverages Depth Peeling to establish accurate per-pixel ordering. This design enables sort-free Gaussian splatting with correct transmittance modulation, effectively eliminating aliasing and popping artifacts while facilitating a fully differentiable joint optimization. Extensive experiments demonstrate that our method achieves superior reconstruction quality and compares favorably against state-of-the-art techniques across a wide range of scenes.
</details>

---

### InfiniDepth: Arbitrary-Resolution and Fine-Grained Depth Estimation with Neural Implicit Fields
著者: Hao Yu, Haotong Lin, Jiawei Wang, Jiaxin Li, Yida Wang, Xueyang Zhang, Yue Wang, Xiaowei Zhou, Ruizhen Hu, Sida Peng

<details>
<summary> 日本語要旨 </summary>

既存の深度推定手法は、画像グリッド上での離散的な深度予測に限定されています。このような表現形式は、任意の出力解像度へのスケーラビリティを制限し、幾何学的詳細の回復を妨げます。本論文では、深度をニューラル暗黙フィールドとして表現するInfiniDepthを提案します。簡潔で効果的なローカル暗黙デコーダーにより、連続した2D座標で深度をクエリすることが可能となり、任意解像度および細部までの精密な深度推定を実現します。我々の手法の能力をより良く評価するために、5つの異なるゲームから収集した高品質な4K合成ベンチマークを用意しました。これは多様なシーンで豊かな幾何学的および外観詳細を含んでいます。広範囲の実験により、InfiniDepthが相対深度推定とメトリック深度推定の両方のタスクにおいて合成および現実世界のベンチマークで最先端の性能を達成していることが示されました。特に、細部領域で優れた結果を出しています。また、大きな視点シフト下での新観点合成タスクにも寄与し、穴やアーティファクトが少ない高品質な結果を生成します。コードとデータは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Existing depth estimation methods are fundamentally limited to predicting depth on discrete image grids. Such representations restrict their scalability to arbitrary output resolutions and hinder the geometric detail recovery. This paper introduces InfiniDepth, which represents depth as neural implicit fields. Through a simple yet effective local implicit decoder, we can query depth at continuous 2D coordinates, enabling arbitrary-resolution and fine-grained depth estimation. To better assess our method's capabilities, we curate a high-quality 4K synthetic benchmark from five different games, spanning diverse scenes with rich geometric and appearance details. Extensive experiments demonstrate that InfiniDepth achieves state-of-the-art performance on both synthetic and real-world benchmarks across relative and metric depth estimation tasks, particularly excelling in fine-detail regions. It also benefits the task of novel view synthesis under large viewpoint shifts, producing high-quality results with fewer holes and artifacts. Code and data will be made publicly available.
</details>

---

### Unlocking Strong Supervision: A Data-Centric Study of General-Purpose Audio Pre-Training Methods
著者: Xuanru Zhou, Yiwen Shao, Wei-Cheng Tseng, Dong Yu

<details>
<summary> 日本語要旨 </summary>

現在のオーディオ事前学習は、広範なオーディオ理解タスクに対する統一された表現を学ぶことを目指していますが、弱くノイズの多いラベルや規模が限られていることに依存しており、その結果、分断されて基本的なボトルネックに直面しています。ビジョン領域の基礎事前学習のブループリントから教訓を得て、オーディオ分野はまず大規模で強力な監督フレームワークを確立する必要があると主張します。私たちは、高品質のキャプションを生成するために最先端のキャプショナーを活用し、スピーチ、音楽、環境音を統合する初のユニファイド・タグ・システム（UTS）を導入した新たなデータ中心のパイプラインを紹介します。その後、強力なソースデータに対して異なる事前学習目的の体系的比較研究を行います。実験結果からは、データの品質とカバー範囲がパフォーマンスの主要なドライバーであること、そして目的選択が下流タスクの専門化を決定することが示唆されます。
</details>

<details>
<summary> 英語要旨 </summary>

Current audio pre-training seeks to learn unified representations for broad audio understanding tasks, but it remains fragmented and is fundamentally bottlenecked by its reliance on weak, noisy, and scale-limited labels. Drawing lessons from vision's foundational pre-training blueprint, we argue that the audio field must first establish its own large-scale, strong supervision framework. We introduce a new data-centric pipeline that leverages a high-fidelity captioner to create SOTA-quality captions and the first Unified Tag System (UTS) that bridges speech, music, and environmental sounds. We then conduct a systematic comparative study of different pre-training objectives on these strong source data. Our experiments suggest that data quality and coverage are the primary drivers of performance, while the choice of objective dictates downstream task specialization.
</details>

---

### From Failure to Feedback: Group Revision Unlocks Hard Cases in Object-Level Grounding
著者: Yuyuan Liu, Yiping Ji, Anjie Le, Jiayuan Zhu, Jiazhen Pan, Can Peng, Jiajun Deng, Fengbei Liu, Junde Wu

<details>
<summary> 日本語要旨 </summary>

大規模ビジョン言語モデルの微調整において、強化学習を用いる手法が、オブジェクトレベルのグラウンディング能力向上の有望なアプローチとして浮上しています。しかし、既存の方法は主にGRPO（Group Reward Policy Optimization）を基盤とし、報酬を応答レベルで割り当てるため、難易度の高いシナリオでは全候補応答が失敗した場合に学習信号が極端に少なくなってしまいます。本研究では、この問題を解決するためにグループ修正最適化パラダイムを提案します。これはサンプリングされた初期応答から始まり、改善されたグラウンディング結果を探索するための一連の修正候補を生成します。報酬形成に触発され、各候補が初期試行に対してどれだけ改善したかを定量化し、それを情報豊かな形成信号に変換する統合プロセスを導入します。これらの信号は報酬の洗練と利点の調整の両方に使用され、高品質な修正の影響力を増幅させます。私たちの方法は、GRPOベースの既存モデルと比較して、参照および推論セグメンテーション（REC）やカウント評価基準において一貫した向上を達成しました。コードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Finetuning Large Vision-Language Models with reinforcement learning has emerged as a promising approach to enhance their capability in object-level grounding. However, existing methods, mainly based on GRPO, assign rewards at the response level. Such sparse reward leads to minimal learning signals when all candidate responses are failed in challenging scenarios. In this work, we propose a group-revision optimisation paradigm that enhances learning on hard cases. It begins with a sampled initial response and generates a set of revised candidates to explore improved grounding outcomes. Inspired by reward shaping, we introduce a consolidation process that quantifies each candidate’s improvement over the initial attempt and converts it into informative shaping signals. These signals are used to both refine the reward and modulate the advantage, amplifying the influence of high-quality revisions. Our method achieves consistent gains across referring and reasoning segmentation, REC, and counting benchmarks compared with prior GRPO-based models. Code will be released.
</details>

---

### LATTICE: Democratize High-Fidelity 3D Generation at Scale
著者: Zeqiang Lai, Yunfei Zhao, Zibo Zhao, Haolin Liu, Qingxiang Lin, Jingwei Huang, Chunchao Guo, Xiangyu Yue

<details>
<summary> 日本語要旨 </summary>

私たちは、3次元と2次元の生成モデル間の品質とスケーラビリティのギャップを埋める新しいフレームワークであるLATTICEを紹介します。2次元画像合成は固定された空間グリッドと確立されたトランスフォーマーアーキテクチャの恩恵を受けていますが、3次元生成は基本的により難しいです。これは、詳細な幾何学的表面と空間構造をゼロから予測する必要があるためです。この課題は、既存の3次元表現の計算複雑性や構造化されたスケーラブルな3次元アセットエンコード方式の不足によってさらに増幅されます。これに対処するため、我々はVoxSetという半構造化表現を提案します。この表現は3次元アセットを粗いボクセルグリッドに固定されたコンパクトなラテントベクトルの集合に圧縮し、効率的で位置認識可能な生成を可能にします。VoxSetは以前のVecSet手法のシンプルさと圧縮利点を保持しつつ、ラテント空間に明示的な構造を導入し、位置埋め込みが生成をガイドすることを可能にし、強力なトークンレベルのテスト時スケーリングを実現します。この表現に基づき、LATTICEは2段階のパイプラインを採用しています：まず、希薄なボクセル化された幾何学的アンカーを生成し、次に再確認された流れトランスフォーマーを使用して詳細な幾何学を生み出します。我々の方法は核としてシンプルですが、任意解像度のデコード、低コストのトレーニング、柔軟な推論スキームをサポートし、さまざまな側面で最先端のパフォーマンスを達成し、スケーラブルかつ高品質な3次元アセット作成への大きな一歩を提供します。
</details>

<details>
<summary> 英語要旨 </summary>

We present LATTICE, a new framework for high-fidelity 3D asset generation that bridges the quality and scalability gap between 3D and 2D generative models. While 2D image synthesis benefits from fixed spatial grids and well-established transformer architectures, 3D generation remains fundamentally more challenging due to the need to predict both spatial structure and detailed geometric surfaces from scratch. These challenges are exacerbated by the computational complexity of existing 3D representations and the lack of structured and scalable 3D asset encoding schemes. To address this, we propose VoxSet, a semi-structured representation that compresses 3D assets into a compact set of latent vectors anchored to a coarse voxel grid, enabling efficient and position-aware generation. VoxSet retains the simplicity and compression advantages of prior VecSet methods while introducing explicit structure into the latent space, allowing positional embeddings to guide generation and enabling strong token-level test-time scaling. Built upon this representation, LATTICE adopts a two-stage pipeline: first generating a sparse voxelized geometry anchor, then producing detailed geometry using a recitified flow transformer. Our method is simple at its core, but supports arbitrary resolution decoding, low-cost training, and flexible inference schemes, achieving state-of-the-art performance on various aspects, and offering a significant step toward scalable, high-quality 3D asset creation.
</details>

---

### Neighbor GRPO: Contrastive ODE Policy Optimization Aligns Flow Models
著者: Dailan He, Guanlin Feng, Xingtong Ge, Yazhe Niu, Yi Zhang, Bingqi Ma, Guanglu Song, Yu Liu, Hongsheng Li

<details>
<summary> 日本語要旨 </summary>

グループ相対政策最適化（GRPO）は、画像およびビデオ生成モデルを人間の好みに合わせるために有望な結果を示しています。しかし、その決定論的サンプリングパラダイムのために現代の流れマッチングモデルへの適用は困難です。現在の方法では、確率性を導入するために通常微分方程式（ODE）を確率微分方程式（SDE）に変換しますが、このSDEベースのGRPOは効率的なクレジット割り当てと少ステップサンプリング用の高次ソルバーとの互換性の問題を抱えています。本論文では、まず既存のSDEベースGRPO方法を距離最適化の観点から再解釈し、その基盤メカニズムが対照的な学習の一形態であることを明らかにします。この洞察に基づき、SDEを完全に回避する新たな整合化アルゴリズムであるNeighbor GRPOを提案します。Neighbor GRPOは、ODEの初期ノイズ条件を操作して多様な候補軌道を生成し、ソフトマックス距離に基づく代理ジャンプ政策を用いてモデルを最適化します。この距離ベースの目的とポリシーグラディエント最適化との間に理論的な関連性を確立し、我々のアプローチをGRPOフレームワークに厳密に統合します。この方法は決定論的ODEサンプリングの利点である効率性と高次ソルバーとの互換性を完全に保持しています。さらに、計算効率向上のため対称アンカーサンプリングを導入し、報酬平坦化問題に対処するためグループごとのクォーシノルム再重み付けを行います。広範な実験では、Neighbor GRPOがSDEベースの対抗馬よりもトレーニングコスト、収束速度、生成品質において顕著に優れていることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Group Relative Policy Optimization (GRPO) has shown promise in aligning image and video generative models with human preferences. However, applying it to modern flow matching models is challenging because of its deterministic sampling paradigm. Current methods address this issue by converting Ordinary Differential Equations (ODEs) to Stochastic Differential Equations (SDEs), which introduce stochasticity. However, this SDE-based GRPO suffers from issues of inefficient credit assignment and incompatibility with high-order solvers for fewer-step sampling. In this paper, we first reinterpret existing SDE-based GRPO methods from a distance optimization perspective, revealing their underlying mechanism as a form of contrastive learning. Based on this insight, we propose Neighbor GRPO, a novel alignment algorithm that completely bypasses the need for SDEs. Neighbor GRPO generates a diverse set of candidate trajectories by perturbing the initial noise conditions of the ODE and optimizes the model using a softmax distance-based surrogate leaping policy. We establish a theoretical connection between this distance-based objective and policy gradient optimization, rigorously integrating our approach into the GRPO framework. Our method fully preserves the advantages of deterministic ODE sampling, including efficiency and compatibility with high-order solvers. We further introduce symmetric anchor sampling for computational efficiency and group-wise quasi-norm reweighting to address reward flattening. Extensive experiments demonstrate that Neighbor GRPO significantly outperforms SDE-based counterparts in terms of training cost, convergence speed, and generation quality.
</details>

---

### High-Fidelity Diffusion Face Swapping with ID-Constrained Facial Conditioning
著者: Dailan He, Xiahong Wang, Shulun Wang, Hao Shao, Bingqi Ma, Guanglu Song, Yu Liu, Hongsheng Li

<details>
<summary> 日本語要旨 </summary>

顔の入れ替えは、ターゲットの属性（ポーズや表情など）を保持しつつ、ソースの顔のアイデンティティをターゲットにシームレスに転送することを目指します。生成能力が優れていることで知られる拡散モデルは、最近、顔の入れ替えの品質向上において有望な結果を示しています。本論文では、拡散ベースの顔の入れ替えにおける2つの主要な課題に取り組みます：アイデンティティよりもターゲット属性を優先することと、アイデンティティと属性条件付けの間の固有の対立です。これらの問題に対処するために、まずアイデンティティの保持を確実にし、その後属性の整合性を細かく調整することで達成される分離条件注入を通じて顔の入れ替え用のアイデンティティ制約付き属性チューニングフレームワークを導入します。さらに、ポストトレーニングの洗練段階でアイデンティティと敵対的損失を組み込むことで忠実度を向上させます。提案するアイデンティティ制約付き拡散ベースの顔入れ替えモデルは、質的および量的評価の両方で既存の方法を上回り、優れたアイデンティティの類似性と属性の一貫性を示し、高忠実度な顔入れ替えにおいて新たな最先端のパフォーマンスを達成しています。
</details>

<details>
<summary> 英語要旨 </summary>

Face swapping aims to seamlessly transfer a source facial identity onto a target while preserving target attributes such as pose and expression. Diffusion models, known for their superior generative capabilities, have recently shown promise in advancing face-swapping quality. This paper addresses two key challenges in diffusion-based face swapping: the prioritized preservation of identity over target attributes and the inherent conflict between identity and attribute conditioning. To tackle these issues, we introduce an identity-constrained attribute-tuning framework for face swapping that first ensures identity preservation and then fine-tunes for attribute alignment, achieved through a decoupled condition injection. We further enhance fidelity by incorporating identity and adversarial losses in a post-training refinement stage. Our proposed identity-constrained diffusion-based face-swapping model outperforms existing methods in both qualitative and quantitative evaluations, demonstrating superior identity similarity and attribute consistency, achieving a new state-of-the-art performance in high-fidelity face swapping.
</details>

---

### MotionEdit: Benchmarking and Learning Motion-Centric Image Editing
著者: Yixin Wan, Lei Ke, Wenhao Yu, Kai-Wei Chang, Dong Yu

<details>
<summary> 日本語要旨 </summary>

私たちは、**MotionEdit**という新しいデータセットを紹介します。これは動作中心の画像編集タスクに焦点を当てており、主題の行動や相互作用を変更しつつ、アイデンティティ、構造、物理的な妥当性を保持するものです。既存の画像編集データセットは静的な外観の変化に焦点を当てたり、希薄で低品質な動作編集しか含まないことが多いですが、MotionEditは連続したビデオから抽出・検証されたリアルな動作変換を示す高品質の画像ペアを提供します。この新しいタスクは科学的にも挑戦的であり、フレーム制御ビデオ合成やアニメーションなどの下流応用に実際的に重要です。モデルパフォーマンスをこの新しいタスクで評価するため、**MotionEdit-Bench**というベンチマークを導入します。これは動作中心の編集に挑戦し、生成的、識別的、嗜好に基づくメトリックでモデルパフォーマンスを測定するものです。ベンチマーク結果は、動作編集が既存の最先端の拡散ベースの編集モデルにとって依然として高度な課題であることを示しています。このギャップを埋めるため、私たちは**MotionNFT**（動作指向の負の意識FineTuning）を提案します。これは入力画像とモデル編集画像間の動作流れが実際の動作にどれだけ一致するかに基づいて動作整合性報酬を計算し、正確な動作変換に向かってモデルを導くポストトレーニングフレームワークです。FLUX.1 KontextおよびQwen-Image-Editでの広範な実験は、MotionNFTが動作編集タスクにおける基本モデルの編集品質と動作忠実度を一貫して向上させつつ、一般的な編集能力を損なわずにその効果を示しています。
</details>

<details>
<summary> 英語要旨 </summary>

We introduce **MotionEdit**, a novel dataset for motion-centric image editing—the task of modifying subject actions and interactions while preserving identity, structure, and physical plausibility. Unlike existing image editing datasets that focus on static appearance changes or contain only sparse, low-quality motion edits, MotionEdit provides high-fidelity image pairs depicting realistic motion transformations extracted and verified from continuous videos. This new task is not only scientifically challenging but also practically significant, powering downstream applications such as frame-controlled video synthesis and animation. To evaluate model performance on the novel task, we introduce **MotionEdit-Bench**, a benchmark that challenges models on motion-centric edits and measures model performance with generative, discriminative, and preference-based metrics. Benchmark results reveal that motion editing remains highly challenging for existing state-of-the-art diffusion-based editing models. To address this gap, we propose **MotionNFT** (Motion-guided Negative-aware FineTuning), a post-training framework that computes motion alignment rewards based on how well the motion flow between input and model-edited images matches the ground-truth motion, guiding models toward accurate motion transformations. Extensive experiments on FLUX.1 Kontext and Qwen-Image-Edit show that MotionNFT consistently improves editing quality and motion fidelity of both base models on the motion editing task without sacrificing general editing ability, demonstrating its effectiveness.
</details>

---

### VLM-3R: Vision-Language Models Augmented with Instruction-Aligned 3D Reconstruction
著者: Zhiwen Fan, Jian Zhang, Renjie Li, Junge Zhang, Runjin Chen, Hezhen Hu, Kevin Wang, Peihao Wang, Huaizhi Qu, Shijie Zhou, Dilin Wang, Zhicheng Yan, Hongyu Xu, Justin Theiss, Tianlong Chen, Jiachen Li, Zhengzhong Tu, Zhangyang Wang, Rakesh Ranjan

<details>
<summary> 日本語要旨 </summary>

大規模マルチモーダルモデル（LMMs）の2次元画像や動画への急速な進展は、人間に近い視覚空間的知性を目指して3Dシーンへの拡張に関する興味を引き起こしました。しかし、モデル設計やデータ取得の両面で人間と同等の深い空間理解を達成することは依然として課題です。既存の方法では、外部の深度センサーによる幾何学的キャプチャや3Dマップの事前構築用のオフ・ザ・シェルフアルゴリズムに依存することが多く、これはスケーラビリティを制限します。本研究では、3D再構成指示調整とスケーラブルなトレーニングデータのキュレーション、新しい時間的推論のベンチマークを組み合わせたVision-Language Models（VLM-3R）フレームワークを紹介します。具体的には、VLM-3Rは単眼動画フレームを処理し、シーンコンテキスト（空間トークン）とカメラの動き（ビュートークン）を表す暗黙の3Dトークンを導出する幾何学エンコーダを使用します。同時に、200,000以上の3D再構成指示調整の質問応答ペアを持つスケーラブルなデータ作成パイプラインを構築しています。時間的推論を評価するために、進化する空間関係に焦点を当てた5つの異なるタスクで138,600以上の質問応答ペアを含むVision-Spatial-Temporal Intelligenceベンチマーク（VSTI-Bench）も導入しています。広範囲にわたる実験では、VLM-3Rが堅牢な視覚空間的推論をサポートし、時間的3Dコンテキストの変化の理解を向上させ、単眼による3D空間支援と具現化された推論を可能にすることが示されています。
</details>

<details>
<summary> 英語要旨 </summary>

The rapid advancement of Large Multimodal Models (LMMs) for 2D images and videos has sparked interest in extending these models to 3D scenes, with the goal of human-like visual-spatial intelligence. However, achieving deep spatial understanding comparable to human capabilities remains challenging for both model design and data acquisition. Existing methods often rely on external depth sensors for geometry capture or off-the-shelf algorithms for pre-constructing 3D maps, which limits their scalability. In this work, we introduce VLM-3R, a framework for Vision-Language Models that couples 3D reconstructive instruction tuning with scalable training data curation and a new benchmark for temporal reasoning. Specifically, VLM-3R processes monocular video frames with a geometry encoder that derives implicit 3D tokens representing scene context (spatial tokens) and camera motion (view tokens). In parallel, we build a scalable data creation pipeline with over 200K 3D reconstructive instruction-tuning question-answer pairs. To evaluate temporal reasoning, we further introduce the Vision-Spatial-Temporal Intelligence benchmark (VSTI-Bench), which contains over 138.6K question-answer pairs across five distinct tasks focused on evolving spatial relationships. Extensive experiments show that VLM-3R supports robust visual-spatial reasoning and improves the understanding of temporal 3D context changes, enabling monocular 3D spatial assistance and embodied reasoning.
</details>

---

### PhysSkin: Real-Time and Generalizable Physics-Based Animation Via Self-Supervised Neural Skinning
著者: Yuanhang Lei, Tao Cheng, Xingxuan Li, Boming Zhao, Siyuan Huang, Ruizhen Hu, Peter Yichen Chen, Hujun Bao, Zhaopeng Cui

<details>
<summary> 日本語要旨 </summary>

多様な3D形状や離散化に対して一般化可能なリアルタイムの物理ベースのアニメーションを実現することは、基本的な課題であり続けています。私たちはこの課題に取り組むための物理情報を用いたフレームワーク「PhysSkin」を紹介します。Linear Blend Skinningの精神に基づき、ハンドル変換で定義されるサブスペースの座標から全空間の変形まで昇格させる連続的なスキニングフィールドを基底関数として学習します。多様な3D形状にわたって良好に一般化し、メッシュフリーで離散化非依存かつ物理的に整合性のあるスキニングフィールドを生成するために、PhysSkinは新しいニューラルスキニングフィールドオートエンコーダーを採用しています。このオートエンコーダーはトランスフォーマベースのエンコーダとクロスアテンショントリップレディケータで構成されています。さらに、オン・ザ・フライのスキニングフィールド正規化と衝突認識勾配修正を取り入れた新しい物理情報を用いた自己監督学習戦略も開発しています。これによりエネルギー最小化、空間滑らかさ、直交性制約の効果的なバランスが可能となります。PhysSkinは一般化可能なニューラルスキニングで優れたパフォーマンスを示し、リアルタイムの物理ベースのアニメーションを実現します。
</details>

<details>
<summary> 英語要旨 </summary>

Achieving real-time physics-based animation that generalizes across diverse 3D shapes and discretizations remains a fundamental challenge. We introduce PhysSkin, a physics-informed framework that addresses this challenge. In the spirit of Linear Blend Skinning, we learn continuous skinning fields as basis functions lifting motion subspace coordinates to full-space deformation, with subspace defined by handle transformations. To generate mesh-free, discretization-agnostic, and physically consistent skinning fields that generalize well across diverse 3D shapes, PhysSkin employs a new neural skinning fields autoencoder which consists of a transformer-based encoder and a cross-attention decoder. Furthermore, we also develop a novel physics-informed self-supervised learning strategy that incorporates on-the-fly skinning-field normalization and conflict-aware gradient correction, enabling effective balancing of energy minimization, spatial smoothness, and orthogonality constraints. PhysSkin shows outstanding performance on generalizable neural skinning and enables real-time physics-based animation.
</details>

---

### SAGE: Scalable Agentic 3D Scene Generation for Embodied AI
著者: Hongchi Xia, Xuan Li, Max Li, Qianli Ma, Jiashu Xu, Ming-Yu Liu, Yin Cui, Tsung-Yi Lin, Wei-Chiu Ma, Shenlong Wang, Shuran Song, Fangyin Wei

<details>
<summary> 日本語要旨 </summary>

現実世界でのデータ収集は、具現化エージェントにとって高コストかつ危険なため、スケーラブルでリアルでシミュレーション用の3D環境が求められています。しかし、既存のシーン生成システムは多くの場合、ルールベースまたはタスク固有のパイプラインに依存しており、アーティファクトや物理的に不正なシーンを生み出すことがあります。私たちは、ユーザー指定の具現化タスク（例えば、「皿を取ってテーブルの上に置く」）を与えるだけで、意図を理解し自動的にシミュレーション用環境を大規模に生成するアゲンティックフレームワーク「SAGE」を提案します。エージェントはレイアウトとオブジェクト構成のための複数のジェネレーターと、セマンティックな妥当性、視覚的リアリズム、物理的安定性を評価する批評家を組み合わせています。反復的な推論と適応的ツール選択により、エージェントはシーンを自己改善し、ユーザーの意図と物理的妥当性が満たされるまで続けます。結果として得られる環境はリアルで多様であり、現代のシミュレーターで直接ポリシートレーニングに使用可能です。このデータだけでトレーニングされたポリシーは明確なスケーリング傾向を示し、未見のオブジェクトやレイアウトに一般化することができ、具現化AIにおけるシミュレーション駆動型スケーリングの可能性を示しています。3Dシーン生成コードとアクション生成コードをリリースし、さらなる研究を促進します。
</details>

<details>
<summary> 英語要旨 </summary>

Real-world data collection for embodied agents remains costly and unsafe, calling for scalable, realistic, and simulator-ready 3D environments. However, existing scene-generation systems often rely on rule-based or task-specific pipelines, yielding artifacts and physically invalid scenes. We present SAGE, an agentic framework that, given a user-specified embodied task (e.g., “pick up a bowl and place it on the table”), understands the intent and automatically generates simulation-ready environments at scale. The agent couples multiple generators for layout and object composition with critics that evaluate semantic plausibility, visual realism, and physical stability. Through iterative reasoning and adaptive tool selection, it self-refines the scenes until meeting user intent and physical validity. The resulting environments are realistic, diverse, and directly deployable in modern simulators for policy training. Policies trained purely on this data exhibit clear scaling trends and generalize to unseen objects and layouts, demonstrating the promise of simulation-driven scaling for Embodied AI. We will release both 3D scene and action generation code to foster further research.
</details>

---

### SAM 3D: 3Dfy Anything in Images
著者: Xingyu Chen, Fu-Jen Chu, Pierre Gleize, Kevin Liang, Alexander Sax, Hao Tang, Weiyao Wang, Michelle Guo, Thibaut Hardin, Xiang Li, Aohan Lin, Jia-Wei Liu, Ziqi Ma, Anushka Sagar, Bowen Song, Xiaodong Wang, Jianing &quot;Jed&quot; Yang, Bowen Zhang, Piotr Dollár, Georgia Gkioxari, Matt Feiszli, Jitendra Malik

<details>
<summary> 日本語要旨 </summary>

私たちは、単一の画像から幾何学的形状、テクスチャー、レイアウトを予測するビジュアルに基づく3Dオブジェクト再構築用の生成モデルであるSAM 3Dを紹介します。SAM 3Dは自然画像において優れた性能を発揮し、こうした画像では遮蔽やシーンの混雑が一般的であり、視覚認識の手掛かりとしてコンテキストから得られる情報がより重要になります。この成果を実現するために、オブジェクトの形状、テクスチャー、姿勢をアノテーションする人間とモデルを組み合わせたパイプラインを採用し、これまでにない規模でビジュアルに基づく3D再構築データを提供しています。このデータから学習するために、合成的な事前学習と実世界の整列を組み合わせた現代的なマルチステージトレーニングフレームワークを採用し、「3Dデータの壁」を突破しています。最近の研究に対して顕著な進歩を遂げ、実世界のオブジェクトやシーンにおける人間の好みテストで少なくとも5:1の勝率を得ています。私たちはコードとモデル重み、オンラインデモ、野外での3Dオブジェクト再構築に対する新しい挑戦的なベンチマークを公開します。
</details>

<details>
<summary> 英語要旨 </summary>

We present SAM 3D, a generative model for visually grounded 3D object reconstruction, predicting geometry, texture, and layout from a single image. SAM 3D excels in natural images, where occlusion and scene clutter are common and visual recognition cues from context play a larger role. We achieve this with a human- and model-in-the-loop pipeline for annotating object shape, texture, and pose, providing visually grounded 3D reconstruction data at unprecedented scale. We learn from this data in a modern, multi-stage training framework that combines synthetic pretraining with real-world alignment, breaking the 3D "data barrier". We obtain significant gains over recent work, with at least a $5:1$ win rate in human preference tests on real-world objects and scenes. We will release our code and model weights, an online demo, and a new challenging benchmark for in-the-wild 3D object reconstruction.
</details>

---

### Learning to Generate Highly Dynamic Videos Using Synthetic Motion Data
著者: Wonjoon Jin, Jiyun Won, Janghyeok Han, Qi Dai, Chong Luo, Seung-Hwan Baek, Sunghyun Cho

<details>
<summary> 日本語要旨 </summary>

最近の進歩にもかかわらず、ビデオ拡散モデルは依然として高度な動的運動を含むリアルなビデオの合成や微細な運動制御が必要な場面で苦戦しています。この中心的な限界は、一般的に使用されるトレーニングデータセットにそのような例が不足していることにあります。これに対処するために、私たちは合成運動データを利用したビデオ合成フレームワークであるDynaVidを導入します。このアプローチは、光流として表現され、コンピュータグラフィックスパイプラインを使用してレンダリングされます。この方法には二つの主要な利点があります。第一に、合成運動は実データから得ることが難しい多様な運動パターンや正確な制御信号を提供します。第二に、レンダリングされたビデオのように人工的な外観を持たず、レンダリングされた光流は運動のみをエンコードし、外観から分離されているため、モデルが合成ビデオの不自然な見た目を再現することを防ぎます。この考えに基づき、DynaVidは二段階生成フレームワークを採用しています：まず運動ジェネレータが運動を合成し、その後、運動ガイド付きビデオジェネレータがその運動に条件付けられたビデオフレームを生成します。この分離された形式は、モデルが合成データからダイナミックな運動パターンを学びつつ、リアル世界のビデオから視覚的なリアリズムを保持することを可能にします。私たちは特に既存のデータセットが限られている活発な人間運動生成や極端なカメラ運動制御という二つの挑戦的なシナリオで、このフレームワークを検証しました。広範な実験により、DynaVidがダイナミック運動生成およびカメラ運動制御のリアリズムと制御可能性を向上させることが示されました。コードとデータセットは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Despite recent progress, video diffusion models still struggle to synthesize realistic videos involving highly dynamic motions or requiring fine-grained motion controllability. A central limitation lies in the scarcity of such examples in commonly used training datasets. To address this, we introduce DynaVid, a video synthesis framework that leverages synthetic motion data in training, which is represented as optical flow and rendered using computer graphics pipelines. This approach offers two key advantages. First, synthetic motion offers diverse motion patterns and precise control signals that are difficult to obtain from real data. Second, unlike rendered videos with artificial appearances, rendered optical flow encodes only motion and is decoupled from appearance, thereby preventing models from reproducing the unnatural look of synthetic videos. Building on this idea, DynaVid adopts a two-stage generation framework: a motion generator first synthesizes motion, and then a motion-guided video generator produces video frames conditioned on that motion. This decoupled formulation enables the model to learn dynamic motion patterns from synthetic data while preserving visual realism from real-world videos. We validate our framework on two challenging scenarios, vigorous human motion generation and extreme camera motion control, where existing datasets are particularly limited. Extensive experiments demonstrate that DynaVid improves the realism and controllability in dynamic motion generation and camera motion control. Codes and datasets will be publicly available.
</details>

---

### ShotDirector: Directorially Controllable Multi-Shot Video Generation with Cinematographic Transitions
著者: Xiaoxue Wu, Xinyuan Chen, Yaohui Wang, Yu Qiao

<details>
<summary> 日本語要旨 </summary>

ショットトランジションは、全体のナラティブ表現やビジュアルストーリーテリングにおける演出デザインを決定するため、マルチショット動画生成において重要な役割を果たします。しかし、最近の進歩は主にショット間の低レベルの視覚的一貫性に焦点を当てており、トランジションがどのように設計されるかや映像言語がどのようにして一貫したナラティブ表現に寄与するかを無視しています。これはしばしば意図的な編集パターンなしで単なる連続ショット変更につながります。この制限に対処するため、私たちはShotDirectorという効率的なフレームワークを提案します。これはパラメータレベルのカメラコントロールと階層編集パターンに対応したプロンプティングを統合しています。具体的には、6-DoFポーズや内部設定を取り入れたカメラ制御モジュールを採用し、正確なカメラ情報の注入を可能にします。さらに、プロフェッショナル編集パターンに対応した階層的プロンプトを導入するために、ショット認識マスクメカニズムが使用されており、ショットコンテンツの細かい制御が可能です。この設計により、私たちのフレームワークはパラメータレベルの条件と高次元のセマンティックガイダンスを効果的に組み合わせ、映画のようなコントロール可能なショットトランジションを実現しています。訓練と評価を容易にするために、私たちは映画のような編集パターンの優先事項を捉えるShotWeaver40Kデータセットを構築し、コントロール可能なマルチショット動画生成用の評価メトリクスセットを開発しています。広範囲にわたる実験は、私たちのフレームワークの効果を示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Shot transitions play a pivotal role in multi-shot video generation, as they determine the overall narrative expression and the directorial design of visual storytelling. However, recent progress has primarily focused on low-level visual consistency across shots, neglecting how transitions are designed and how cinematographic language contributes to coherent narrative expression. This often leads to mere sequential shot changes without intentional film-editing patterns. To address this limitation, we propose ShotDirector, an efficient framework that integrates parameter-level camera control and hierarchical editing-pattern-aware prompting. Specifically, we adopt a camera control module that incorporates 6-DoF poses and intrinsic settings to enable precise camera information injection. In addition, a shot-aware mask mechanism is employed to introduce hierarchical prompts aware of professional editing patterns, allowing fine-grained control over shot content. Through this design, our framework effectively combines parameter-level conditions with high-level semantic guidance, achieving film-like controllable shot transitions. To facilitate training and evaluation, we construct ShotWeaver40K, a dataset that captures the priors of film-like editing patterns, and develop a set of evaluation metrics for controllable multi-shot video generation. Extensive experiments demonstrate the effectiveness of our framework.
</details>

---

### Learning to Adapt: Self-Improving Web Agent Via Cognitive-Aware Exploration
著者: Weile Chen, Bingchen Miao, Qifan Yu, Wendong Bu, Guoming Wang, Wenqiao Zhang, Shengyu Zhang, Juncheng Li, Siliang Tang

<details>
<summary> 日本語要旨 </summary>

最近のマルチモーダル大規模言語モデル（MLLMs）の進歩により、ウェブエージェント分野で有望な進展が見られています。しかし、既存のウェブエージェントはしばしば手作業で設計された実行パイプラインや高価な専門家経路に依存しており、複雑かつ動的な環境への適応性が制限されています。これらの課題に対処するため、私たちは**SCALE**（**S**elf-**C**ognitive-**A**ware **L**earning and **E**xploration）を提案します。これは、環境探索を通じて自らの限界を発見し認知的な境界を拡張するために、*selector*、*predictor*、および*judger*という三つの役割を活用します。さらに、グローバル計画を促進しエージェントが局所的な探索の罠に陥ることを防ぐためのグラフ探索戦略である**SCALE-Hop**を提案します。学習をさらに支援するため、私たちは19の実際のウェブサイトから収集した大規模なデータセット**SCALE-20k**を構築しました。このデータセットは、多様なタスク種類とSCALEの探索トレースから生成された構造化されたデモンストレーションを含んでいます。実験結果によると、私たちのアプローチはさまざまなウェブ環境における複数のMLLMsのパフォーマンスと汎用性を大幅に向上させています。私たちのフレームワークは、本当に自律的で適応可能なウェブエージェントを構築するための拡張性と汎用性のあるソリューションを提供します。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advances in Multimodal Large Language Models (MLLMs) have led to promising progress in web agents. However, existing web agents often rely on handcrafted execution pipelines or expensive expert trajectories, limiting their adaptability to complex, dynamic environments. To address these challenges, we propose **SCALE** (**S**elf-**C**ognitive-**A**ware **L**earning and **E**xploration), which leverages three advertise roles——*selector*, *predictor*, and *judger* to autonomously discover their limitations and expand its cognitive boundaries through the environment exploration. Moreover, we propose **SCALE-Hop**, a graph exploration strategy that facilitates global planning and helps agents avoid local exploration traps. To further support learning, we construct **SCALE-20k**, a large-scale dataset collected from 19 real-world websites, containing diverse task types and structured demonstrations generated from SCALE’s exploration traces. Experimental results show that our approach significantly improves the performance and generalization of multiple MLLMs in various web environments. Our framework offers a scalable and generalizable solution for building truly autonomous and adaptive web agents.
</details>

---

### VisMem: Latent Vision Memory Unlocks Potential of Vision-Language Models
著者: Xinlei Yu, Chengming Xu, Guibin Zhang, Zhangquan Chen, Yudong Zhang, Yongbo He, Peng-Tao Jiang, Jiangning Zhang, Xiaobin Hu, Shuicheng Yan

<details>
<summary> 日本語要旨 </summary>

ビジョン言語モデル（VLMs）は顕著な成功を収めているものの、多くの複雑な視覚タスクにおけるパフォーマンスは、「視覚処理のボトルネック」によってしばしば制限されます。これは、長期的な生成中に視覚証拠からのアンカリングを失い、文脈化された視覚経験に欠ける傾向があることを指します。人間の認知メモリ理論に触発されており、これは短期的な視覚支配型記憶と長期的な意味支配型記憶を区別しています。私たちは、動的な潜在的視覚メモリを備えることでVLMsに認知的に整合したフレームワークであるVisMemを提案します。これは、細部までの感覚保持を可能にする短期モジュールと抽象的意味の蓄積を可能にする長期モジュールから構成されています。これらのメモリは推論中にシームレスに呼び出され、VLMsが思考と生成の間で感覚的な忠実性と意味的一貫性を維持することを可能にします。理解、推論、および生成のための多様なベンチマークにわたる広範な実験は、VisMemが基本的なモデルに対して平均で11.8%のパフォーマンス向上を達成し、すべての競合他社を凌駕することを示しています。これは潜在空間メモリ強化における新たなパラダイムを確立します。ソースコードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Despite the remarkable success of Vision-Language Models (VLMs), their performance on a range of complex visual tasks is often hindered by a "visual processing bottleneck": a propensity to lose grounding in visual evidence and exhibit a deficit in contextualized visual experience during prolonged generation. Drawing inspiration from human cognitive memory theory, which distinguishes short-term visually-dominant memory and long-term semantically-dominant memory, we propose VisMem, a cognitively-aligned framework that equips VLMs with dynamic latent vision memories, a short-term module for fine-grained perceptual retention and a long-term module for abstract semantic consolidation. These memories are seamlessly invoked during inference, allowing VLMs to maintain both perceptual fidelity and semantic consistency across thinking and generation. Extensive experiments across diverse benchmarks for understanding, reasoning, and generation reveal that VisMem delivers a significant average performance boost of 11.8% relative to the vanilla model and outperforms all counterparts, establishing a new paradigm for latent-space memory enhancement. The source code will be made publicly available.
</details>

---

### Diff4Splat: Repurposing Video Diffusion Models for Dynamic Scene Generation
著者: Panwang Pan, Chenguo Lin, Chenxin Li, Jingjing Zhao, Yuchen Lin, Haopeng Li, yunlong lin, Kairun Wen, Yixuan Yuan, Yadong Mu

<details>
<summary> 日本語要旨 </summary>

私たちは、単一の画像から動的シーンを生成するフィードフォワードフレームワークであるDiff4Splatを紹介します。この方法は、大規模な4Dデータセットから学習された幾何学的および動きの制約と、ビデオ拡散モデルの強力な生成事前知識を統合します。単一の画像、カメラトラジェクトリ、そして任意のテキストプロンプトが与えられた場合、私たちのモデルは変形可能な3Dガウスフィールドによって表現される動的シーンを直接予測します。このアプローチは単一パスで外観、幾何学、および動きを捉え、テスト時の最適化や後処理を不要にします。私たちのフレームワークの中核にあるビデオラテントトランスフォーマーは既存のビデオ拡散モデルを強化し、それらが空間時間的依存性を共同でモデリングし、時間を通じて3Dガウスプリミティブを予測することを可能にします。外観の忠実度、幾何学的精度、動きの一貫性をターゲットにした目標で監督されたDiff4Splatは、30秒以内に高品質な動的シーンを生成します。私たちは、ビデオ生成、新視点合成、幾何学抽出の分野でDiff4Splatの有効性を示し、これらの領域で最適化ベースの方法と同等またはそれ以上に動的シーン合成を行いながら、大幅に効率的であることを示します。
</details>

<details>
<summary> 英語要旨 </summary>

We introduce Diff4Splat, a feed-forward framework for dynamic scene generation from a single image. Our method synergizes the powerful generative priors of video diffusion models with geometric and motion constraints learned from a large-scale 4D dataset. Given a single image, a camera trajectory, and an optional text prompt, our model directly predicts a dynamic scene represented by a deformable 3D Gaussian field. This approach captures appearance, geometry, and motion in a single pass, eliminating the need for test-time optimization or post-hoc processing. At the core of our framework is a video latent transformer that enhances existing video diffusion models, enabling them to jointly model spatio-temporal dependencies and predict 3D Gaussian Primitives over time. Supervised by objectives targeting appearance fidelity, geometric accuracy, and motion consistency, Diff4Splat generates high-fidelity dynamic scenes within 30 seconds. We demonstrate the effectiveness of Diff4Splat across video generation, novel view synthesis, and geometry extraction, where it matches or surpasses optimization-based methods for dynamic scene synthesis while being significantly more efficient.
</details>

---

### ID-Crafter: VLM-Grounded Online RL for Compositional Multi-Subject Video Generation
著者: Panwang Pan, Jingjing Zhao, Yuchen Lin, Chenguo Lin, Chenxin Li, Hengyu Liu, Tingting Shen, Yadong Mu

<details>
<summary> 日本語要旨 </summary>

高品質なビデオ合成においては顕著な進歩が達成されていますが、現在のパラダイムでは多数の主体からのアイデンティティ情報を効果的に統合することがしばしば困難です。これにより、セマンティックな衝突やアイデンティティおよび相互作用の保存性能が低下し、制御可能性や適用範囲が限定されます。この問題に対処するため、我々は複数主体ビデオ生成において優れたアイデンティティ保存とセマンティックな一貫性を実現するフレームワーク「ID-Crafter」を提案します。ID-Crafterは以下の三つの主要コンポーネントを統合しています：（i）アイデンティティ保存に特化した階層的注意メカニズムで、内部主体レベル、間主体レベル、クロスモーダルレベルで徐々に特徴を集約する；（ii）事前学習済みのビジョン言語モデル（VLM）によって動機付けられたセマンティック理解モジュールで、微細なガイダンスを提供し複雑な間主体関係を捉える；および（iii）重要な概念に対してさらにモデルを洗練するためのオンライン強化学習フェーズ。また、堅牢なトレーニングと評価を促進する新しいデータセットも構築しています。広範囲にわたる実験は、ID-Crafterが複数主体ビデオ生成のベンチマークで新たな最先端性能を確立し、アイデンティティ保存、時間的一貫性、全体的なビデオ品質において優れていることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Significant progress has been achieved in high-fidelity video synthesis, yet current paradigms often fall short in effectively integrating identity information from multiple subjects. This leads to semantic conflicts and suboptimal performance in preserving identities and interactions, limiting controllability and applicability. To tackle this issue, we introduce ID-Crafter, a framework for multi-subject video generation that achieves superior identity preservation and semantic coherence. ID-Crafter integrates three key components: (i) a hierarchical identity-preserving attention mechanism that progressively aggregates features at intra-subject, inter-subject, and cross-modal levels; (ii) a semantic understanding module powered by a pretrained Vision-Language Model (VLM) to provide fine-grained guidance and capture complex inter-subject relationships; and (iii) an online reinforcement learning phase to further refine the model for critical concepts. Furthermore, we construct a new dataset to facilitate robust training and evaluation. Extensive experiments demonstrate that ID-Crafter establishes new state-of-the-art performance on multi-subject video generation benchmarks, excelling in identity preservation, temporal consistency, and overall video quality.
</details>

---

### GaussianDWM: Driving World Model Using Language-aligned 3D Gaussians for Scene Understanding and Multi-modal Generation
著者: Tianchen Deng, Xuefeng Chen, Yi Chen, Qu Chen, Yuyao Xu, Lijin Yang, Le Xu, Yu Zhang, Bo Zhang, Wuxiong.Huang Wuxiong.Huang, Hesheng Wang

<details>
<summary> 日本語要旨 </summary>

生成モデルの進化に伴い、ドライビング・ワールド・モデル（DWMs）は急速に発展しています。しかし、既存のDWMsは3次元シーン理解能力を欠き、入力データに条件付けられたコンテンツのみ生成でき、運転環境の解釈や推論ができません。また、現在のアプローチでは点群やBEV特徴を用いて3次元空間情報を表現しますが、これらはテキスト情報と基礎となる3Dシーンとの正確な整合性を欠いています。これらの制限に対処するため、私たちは3次元ガウスシーン表現に基づく新しい統一的なDWMフレームワークを提案します。このフレームワークは3次元シーン理解とマルチモーダルシーン生成の両方を可能にし、さらに理解および生成タスクに対するコンテキスト豊かな強化も実現します。私たちのアプローチは各ガウス原始体に豊富な言語特徴を埋め込み、テキスト情報と3Dシーンを直接整合させることで早期モダリティの整合性を達成します。また、冗長な3次元情報を除去し、正確かつコンパクトな3次元トークンをテキスト理解に注入するためのタスク認識型言語ガイド付きトークンサンプリング戦略も設計しました。さらに、私たちはビジョン・ランゲージモデルで捉えた情報を高レベルの言語条件と低レベルの画像条件と組み合わせてマルチモーダル生成プロセスを共同で指導する新しい二重条件マルチモーダル生成モデルも設計しました。nuScenes、OmniDrive-nuScenes、NuInteractの各データセットにおける包括的な研究を通じて、私たちのフレームワークの有効性を検証しました。私たちの方法は最先端のパフォーマンスを達成しています。コードはGitHubで公開します。
</details>

<details>
<summary> 英語要旨 </summary>

Driving World Models (DWMs) have been developing rapidly with the advances of generative models. However, existing DWMs lack 3D scene understanding capabilities and can only generate content conditioned on input data, without the ability to interpret or reason about the driving environment. Moreover, current approaches represent 3D spatial information with point cloud or BEV features do not accurately align textual information with the underlying 3D scene. To address these limitations, we propose a novel unified DWM framework based on 3D Gaussian scene representation, which enables both 3D scene understanding and multi-modal scene generation, while also enabling contextual enrichment for understanding and generation tasks. Our approach directly aligns textual information with the 3D scene by embedding rich linguistic features into each Gaussian primitive, thereby achieving early modality alignment. In addition, we design a novel task-aware language-guided token sampling strategy that removes redundant 3D information and injects accurate and compact 3D tokens into textual understanding. Furthermore, we design a dual-condition multi-modal generation model, where the information captured by our vision-language model is leveraged as a high-level language condition in combination with a low-level image condition, jointly guiding the multi-modal generation process. We conduct comprehensive studies on the nuScenes, OmniDrive-nuScenes, and NuInteract datasets to validate the effectiveness of our framework. Our method achieves state-of-the-art performance. We will release the code publicly on GitHub.
</details>

---

### G$^2$VLM: Geometry Grounded Vision Language Model with Unified 3D Reconstruction and Spatial Reasoning
著者: Wenbo hu, JINGLI LIN, Yilin Long, Yunlong Ran, Lihan Jiang, Yifan Wang, Chenming Zhu, Runsen Xu, Tai Wang, Jiangmiao Pang

<details>
<summary> 日本語要旨 </summary>

ビジョン言語モデル（VLMs）は、空間理解や推論タスクにおいて依然として頑健性が欠けており、パフォーマンスが低いです。このギャップの原因は、2D画像から3D空間を再構築できる視覚幾何学的な学習過程が欠如していることにあると考えます。私たちは、空間理解の二つの基本的側面を結び付ける幾何学的に根拠のあるビジョン言語モデルであるG$^2$VLMを提案します。これは、3D空間再構築と空間理解です。G$^2$VLMは、学習された3D視覚幾何学的特徴を直接に活用して3D属性の予測を行い、インコンテキスト学習と交錯推論を通じて空間推理タスクを強化します。私たちの統一設計は、多視点画像や動画データで豊富にトレーニングしつつ、通常は収集が困難なアノテーションから得られる3D視覚的事前知識の利点を同時に活用することで、空間理解において高度にスケーラブルです。実験結果は、G$^2$VLMが両方のタスクに優れた能力を示し、フィードフォワード3D再構築モデルと同等の成果を達成する一方で、空間理解や推論タスクではより良いまたは競争力のある結果を示しています。意味的に強力なVLMと低レベル3Dビジョンタスクを統一することで、G$^2$VLMがコミュニティのための強固な基準として機能し、将来的には3Dシーン編集などのさらなる応用を解放することを期待します。
</details>

<details>
<summary> 英語要旨 </summary>

Vision-Language Models (VLMs) still lack robustness in spatial intelligence, demonstrating poor performance on spatial understanding and reasoning tasks. We attribute this gap to the absence of a visual geometry learning process capable of reconstructing 3D space from 2D images. We present G$^2$VLM, a geometry grounded vision-language model that bridges two fundamental aspects of spatial intelligence: spatial 3D reconstruction and spatial understanding. G$^2$VLM natively leverages learned 3D visual geometry features to directly predict 3D attributes and enhance spatial reasoning tasks via in-context learning and interleaved reasoning. Our unified design is highly scalable for spatial understanding: it trains on abundant multi-view image and video data, while simultaneously leveraging the benefits of 3D visual priors that are typically only derived from hard-to-collect annotations. Experimental results demonstrate G$^2$VLM is proficient in both tasks, achieving comparable results to state-of-the-art feed-forward 3D reconstruction models and achieving better or competitive results across spatial understanding and reasoning tasks. By unifying a semantically strong VLM with low-level 3D vision tasks, we hope G$^2$VLM can serve as a strong baseline for the community and unlock more future applications, such as 3D scene editing.
</details>

---

### SoccerMaster: A Vision Foundation Model for Soccer Understanding
著者: Haolin Yang, Jiayuan Rao, Haoning Wu, Weidi Xie

<details>
<summary> 日本語要旨 </summary>

最近、サッカーの理解はそのドメイン固有の複雑さとユニークな課題により、研究関心が高まっています。しかし、これまでの研究では通常、タスク特化型の専門家モデルを使用しており、それらはリソース集約的であり、ゲーム全体の視点を妨げています。本論文では、多様なサッカーのビジュアル理解タスクを単一モデルで処理可能にする統合フレームワークを提案することを目指しています。具体的には、以下の貢献を行っています：(i) サッカー特化のビジョンファウンデーションモデルである**SoccerMaster**を初めて提示し、監督付きマルチタスク事前学習により単一フレームワーク内で包括的な理解タスクを統合します；(ii) 複数の既存サッカー動画データセットを集約し、**SoccerFactory**と呼ばれる自動化されたデータキュレーションパイプラインを開発して、スケーラブルなマルチタスクトレーニングアノテーションを生成します；そして(iii) SoccerMasterが多様な下流タスクにおいて一貫してタスク特化型の専門家モデルを上回ることを示す広範な実験を行い、その幅広さと優位性を強調します。データ、コード、およびモデルは研究コミュニティに公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Soccer understanding has recently garnered growing research interest due to its domain-specific complexity and unique challenges. However, prior works typically rely on task-specific expert models, which are resource-intensive and hinder a holistic view of the game. This paper aims to propose a unified framework that enables a single model to handle diverse soccer visual understanding tasks, spanning both fine-grained perception (e.g., athlete detection) and semantic reasoning (e.g., event classification). Concretely, we make the following contributions in this paper:(i) we present **SoccerMaster**, the first soccer-specific vision foundation model that unifies comprehensive understanding tasks within a single framework via **supervised multi-task pretraining**;(ii) we consolidate multiple existing soccer video datasets and develop an automated data curation pipeline, termed as **SoccerFactory**, to produce scalable multi-task training annotations;and (iii) we conduct extensive experiments demonstrating that SoccerMaster consistently outperforms task-specific expert models across diverse downstream tasks, underscoring its breadth and superiority. The data, code, and model will be publicly available to the research community.
</details>

---

### STARFlow-V: End-to-End Video Generative Modeling with Autoregressive Normalizing Flows
著者: Jiatao Gu, Ying Shen, Tianrong Chen, Laurent Dinh, Yuyang Wang, Miguel Ángel Bautista, David Berthelot, Joshua Susskind, Shuangfei Zhai

<details>
<summary> 日本語要旨 </summary>

正規化流（NF）は連続データのための端から端まで確率ベースの生成モデルであり、最近画像生成において励みとなる進展を遂げています。しかし、ビデオ生成領域ではスペーシャルタイム複雑性や計算コストが大幅に高く、最先端のシステムはほぼ全て拡散ベースのモデルに依存しています。本研究ではこの設計空間を再検討し、STARFlow-Vという正規化流ベースのビデオジェネレーターを提示します。これは端から端までの学習、堅牢な因果予測、およびネイティブ確率推定といった大きな利点を持っています。最近提案されたSTARFlowに基づき、STARFlow-Vはグローバル・ローカルアーキテクチャーを採用し、スペーシャルタイム潜在空間で動作します。このアーキテクチャーでは因果依存関係をグローバルな潜在空間に制限しつつ、フレーム内の豊かな局所的相互作用を保持します。これにより、標準的な自己回帰拡散モデル生成で一般的な欠点である時間経過に伴う誤差蓄積が緩和されます。さらに、流れスコアマッチングを提案し、これによりモデルは自己回帰的な方法でビデオ生成の一貫性を向上するための軽量因果除去器を備えることができます。サンプリング効率を改善するため、STARFlow-Vはビデオに配慮したジャコビ反復法スキームを採用し、内部更新を並列化可能な反復として再定義しますが、因果性を維持します。可逆構造のおかげで、同じモデルはテキストからビデオ、画像からビデオ、そしてビデオからビデオ生成タスクにもネイティブに対応可能です。実験的に、STARFlow-Vは拡散ベースのベンチマークと比較して強力な視覚的忠実性と時間的一貫性を達成し、実用的なサンプリングスループットでこれらを示します。これらの結果は、私たちが知る限りでは初めての証拠であり、NFが高品質な自己回帰ビデオ生成に対応可能であることを示しており、世界モデル構築のための有望な研究方向性を確立します。
</details>

<details>
<summary> 英語要旨 </summary>

Normalizing flows (NFs) are end-to-end likelihood-based generative models for continuous data, and have recently regained attention with encouraging progress on image generation. Yet in the video generation domain, where spatiotemporal complexity and computational cost are substantially higher, state-of-the-art systems almost exclusively rely on diffusion-based models. In this work, we revisit this design space by presenting STARFlow-V, a normalizing flow-based video generator with substantial benefits such as end-to-end learning, robust causal prediction and native likelihood estimation. Building upon the recently proposed STARFlow, STARFlow-V operates in the spatiotemporal latent space with a global-local architecture which restricts causal dependencies to a global latent space while preserving rich local within-frame interactions. This eases error accumulation over time, a common pitfall of standard autoregressive diffusion model generation. Additionally, we propose flow-score matching, which equips the model with a light-weight causal denoiser to improve the video generation consistency in an autoregressive fashion. To improve the sampling efficiency, STARFlow-V employs a video-aware Jacobi iteration scheme that recasts inner updates as parallelizable iterations without breaking causality. Thanks to the invertible structure, the same model can natively support text-to-video, image-to-video as well as video-to-video generation tasks. Empirically, STARFlow-V achieves strong visual fidelity and temporal consistency with practical sampling throughput relative to diffusion-based baselines. These results present the first evidence, to our knowledge, that NFs are capable of high-quality autoregressive video generation, establishing them as a promising research direction for building world models.
</details>

---

### LongVT: Incentivizing Thinking with Long Videos Via Native Tool Calling
著者: Zuhao Yang, Sudong Wang, Kaichen Zhang, Keming Wu, Sicong Leng, Yifan Zhang, Bo Li, Chengwei Qin, Shijian Lu, Xingxuan Li, Lidong Bing

<details>
<summary> 日本語要旨 </summary>

大規模マルチモーダルモデル（LMMs）は、テキストによるChain-of-Thoughtを用いたビデオ推論で大きな可能性を示しています。しかし、特に証拠が希薄かつ時間的に散在する長尺の動画処理時には、幻覚に対して脆弱です。人間が長いビデオを理解する方法—まず全体をスキャンし、その後詳細なために関連クリップを検討することに着想を得て、「長尺動画での思考」を促すエンドツーエンドのエージェントフレームワーク「LongVT」を提案します。具体的には、LMMsが持つ固有の時間的な位置づけ能力をビデオクロッピングツールとして活用し、特定の動画クリップにズームインし、より細かいフレームを再サンプルします。このグローバルからローカルへの推論ループは、取得した視覚的証拠に基づいて答えが確立されるまで続きます。長尺動画推論用の細かな質問応答データが乏しいため、トレーニングと評価を促進する「VideoSIAH」というデータセットを編纂し公開します。私たちのトレーニングデータセットには、ツール統合冷スタート監督細かい調整用247.9Kサンプル、エージェント強化学習用1.7Kサンプル、エージェント強化細かい調整用15.4Kサンプルが含まれます。評価ベンチマークには、半自動データパイプラインと人間の介入による検証を通じて注意深く確認された1,280のQAペアが含まれます。精密に設計された3段階のトレーニング戦略と広範な実験的検証を通じて、LongVTは4つの挑戦的な長尺動画理解および推論ベンチマークにわたって強力な既存のベースラインを一貫して上回ります。
</details>

<details>
<summary> 英語要旨 </summary>

Large multimodal models (LMMs) have shown great potential in video reasoning with textual Chain-of-Thought. However, they remain vulnerable to hallucination, especially when processing long-form videos where evidence is sparse and temporally dispersed. Inspired by how humans comprehend long videos—by first skimming globally and then examining relevant clips for details—we introduce LongVT, an end-to-end agentic framework that sparks "Thinking with Long Videos" via interleaved Multimodal Chain-of-Tool-Thought. Specifically, we exploit LMMs’ inherent temporal grounding ability as a native video cropping tool to zoom in on specific video clips and resample finer-grained frames. This global-to-local reasoning loop continues until answers are grounded in retrieved visual evidence. Given the scarcity of fine-grained question-answering data for long-video reasoning, we curated and will release a data suite named VideoSIAH to facilitate both training and evaluation. Our training dataset consists of 247.9K samples for tool-integrated cold-start supervised fine-tuning, 1.7K samples for agentic reinforcement learning, and 15.4K samples for agentic reinforcement fine-tuning. Our evaluation benchmark contains 1,280 QA pairs carefully verified through a semi-automatic data pipeline with human-in-the-loop validation. With a meticulously designed three-stage training strategy and extensive empirical validations, LongVT consistently outperforms strong existing baselines across four challenging long-video understanding and reasoning benchmarks.
</details>

---

### Synthetic Object Compositions for Scalable and Accurate Learning in Detection, Segmentation, and Grounding
著者: Weikai Huang, Jieyu Zhang, Taoyang jia, Chenhao Zheng, Ziqi Gao, Jae Sung Park, Ranjay Krishna

<details>
<summary> 日本語要旨 </summary>

視覚的なグループ化—インスタンスセグメンテーション、ビジュアルグラウンディング、オブジェクト検出のようなタスクを通じて操作されることで—ロボットの知覚から写真編集に至るまでの応用が可能です。これらはコンピュータビジョンにおける基本的な問題であり、大規模かつ細心の注意を払ってアノテーションされたデータセットによって支えられています。その影響力にもかかわらず、これらのデータセットは構築が高価でカバレッジに偏りがあり、スケーリングが難しいです。合成データセットは有望な代替手段を提供しますが、柔軟性、精度、構成的多様性の面で苦戦しています。私たちは**Synthetic Object Compositions (SOC)**という正確かつスケーラブルなデータ合成パイプラインを導入します。これは3次元幾何学的レイアウトの拡張とカメラ構成の拡張による生成調和とマスク面積加重ブレンディングを通じて、新しい画像に高品質な合成オブジェクトセグメントを組み立てることで実現されます。これにより正確かつ多様なマスク、ボックス、および参照表現が得られます。私たちの合成画像**100K枚**だけを用いてトレーニングしたモデルは、実際の大規模なデータセット（GRIT 20M、V3Det 200K）や他の合成パイプライン（Copy-Paste、X-Paste、SynGround、SegGen）を上回る**+24–36%**の性能向上を達成しました。これによりLVISで**+10.9 AP**、gRefCOCOで**+8.4 $N_{\text{Acc}}$**が得られます。一般的なオープンボキャブラリー設定を超えて、SOCは異なる用途に対する制御可能なデータセット構築を可能にし、低データおよびクローズドボキャブラリーのシナリオでのパフォーマンス向上も実現します。LVISとCOCOに合成オブジェクトセグメントを追加することで、異なる実データ規模にわたって強力な性能が得られ、特に極めて限定された実データ条件下ではさらなる改善が見られます。これには**1% COCO**のデータ設定での**+6.59 AP**も含まれます。また、この制御可能性により、私たちが提案する微細属性識別を必要とする診断グラウンディングタスクである**intra-class referring**のための標的データ生成も可能になります。
</details>

<details>
<summary> 英語要旨 </summary>

Visual grouping—operationalized through tasks such as instance segmentation, visual grounding, and object detection—enables applications ranging from robotic perception to photo editing. These fundamental problems in computer vision are powered by large-scale, painstakingly annotated datasets. Despite their impact, these datasets are costly to build, biased in coverage, and difficult to scale. Synthetic datasets offer a promising alternative but struggle with flexibility, accuracy, and compositional diversity. We introduce **Synthetic Object Compositions (SOC)**, an accurate and scalable data synthesis pipeline via a novel object-centric composition strategy. It composes high-quality synthetic object segments into new images using 3D geometric layout augmentation and camera configuration augmentation with generative harmonization and mask-area-weighted blending, yielding accurate and diverse masks, boxes, and referring expressions. Models trained on just **100K** of our synthetic images outperform those trained on larger real datasets (GRIT 20M, V3Det 200K) and synthetic pipelines (Copy-Paste, X-Paste, SynGround, SegGen) by **+24–36%**—achieving **+10.9 AP** on LVIS and **+8.4 $N_{\text{Acc}}$** on gRefCOCO. Beyond the general open-vocabulary setup, SOC also enables controllable dataset construction for different use cases and boosts performance in both low-data and closed-vocabulary scenarios. Augmenting LVIS and COCO with synthetic object segments delivers strong performance across different real-data scales and yields even greater improvements under extremely limited real-data conditions, including **+6.59 AP** on a **1% COCO** data setup. Furthermore, this controllability enables targeted data generation for **intra-class referring**, a diagnostic grounding task we propose that requires fine-grained attribute discrimination.
</details>

---

### VideoNet: A Large-Scale Dataset for Domain-Specific Action Recognition
著者: Tanush Yadav, Reza Salehi, Jae Sung Park, Vivek Ramanujan, Hannaneh Hajishirzi, Yejin Choi, Ali Farhadi, Rohun Tripathi, Ranjay Krishna

<details>
<summary> 日本語要旨 </summary>

ビデオは行動の豊かな微細さを捉えます。大規模なビデオ言語モデルは長いビデオの理解に進歩していますが、ドメイン特化型で細部まで分かれた動作の微妙な運動を識別する能力は明確ではありません。現在のベンチマークはドメイン非依存的に細部まで分かれた行動を評価しており、このタスクでモデルを評価することが難しい状況です。このギャップを埋めるために、私たちはドメイン特化型の細部まで分かれた行動理解をビデオモデルで評価するための包括的なベンチマーク\dataset を導入します。このベンチマークは38のドメインにわたる1,087の異なる行動をカバーしており、岩登りから縫合まで含まれています。私たちの評価では、現在のビデオモデルがゼロショットシナリオでこれらの行動を認識する際に顕著な困難に直面していることが示されました。次に、このタスクでのモデルパフォーマンスを向上させる方法を検討します。そのために、160Kの細部まで分かれたドメイン特化型行動のクリップからなるトレーニングデータセットを収集しました。このデータで4Bモデルを事後学習することにより、私たちのベンチマーク上ですべてのGeminiモデルおよびGPT-4o を超える結果を得ました。次に、フィーチャーショット評価を行い、最も高性能なモデルであるGPT-5 がフィーチャーショット評価設定では苦戦していることを示しました。3つのインコンテキスト例を与えられた場合、モデルと人間のパフォーマンスの差が広がり、人間の正解率は13%向上する一方で、モデルはわずか3%しか改善しません。これはビデオ言語モデルが現在効果的なフィーチャーショートラーナーではないことを示唆しており、テキストのみの対応物と異なります。さらに、これらのモデルのフィーチャーショート学習能力を向上させることで追加の改善が得られる可能性があります。
</details>

<details>
<summary> 英語要旨 </summary>

Videos capture a rich array of subtleties in actions. While large video language models have advanced in understanding long videos, their ability to discern nuanced motions in domain-specific, fine-grained actions remains unclear. Current benchmarks evaluate for fine-grained actions in a domain agnostic manner, making to hard to evaluate models on this task. To address this gap, we introduce \dataset, a comprehensive benchmark aimed at evaluating the domain-specific, fine-grained action understanding of video models. This benchmark covers $1,087$ distinct actions spanning $38$ domains, from bouldering to suturing. Our evaluations demonstrate that current video models encounter significant difficulties in recognizing these actions in a zero-shot scenario. We then examine how to improve model performance on this task. To this end, we collect a training dataset of 160K clips of fine-grained, domain-specific actions. Post-training a 4B model on this data, we surpass all Gemini models and GPT-4o on our benchmark. Next, we evaluate few-shot evaluation and demonstrate that even the best-performing model, GPT-5, struggles in a few-shot evaluation setting. When given three in-context examples, the gap between model and human performance widens, with human accuracy improving by 13% while models only improve by 3%. This suggests that video language models are currently not effective few-shot learners--unlike their text-only counterparts and further gains may be elicited from improving these models' few-short learning capabilities.
</details>

---

### UniGen-1.5: Enhancing Image Generation and Editing Through Reward Unification in RL
著者: Rui Tian, Mingfei Gao, Haiming Gang, Jiasen Lu, Zhe Gan, Yinfei Yang, Zuxuan Wu, Afshin Dehghan

<details>
<summary> 日本語要旨 </summary>

私たちは、高度な画像理解、生成、編集を行う統一的多モーダル大規模言語モデル（MLLM）であるUniGen-1.5を紹介します。UniGenの基に立ち、モデルアーキテクチャとトレーニングパイプラインを総合的に強化し、画像理解および生成能力を強化しつつ、強力な画像編集機能を開放します。特に、共有報酬モデルを用いて画像生成と画像編集の両方を改善する統一的リインフォースメントラーニング（RL）戦略を提案しています。さらに、画像編集パフォーマンスを向上させるために、編集指示の理解を大幅に改善する軽量なEdit Instruction Alignmentステージを提案します。これはRLトレーニングの成功に不可欠です。実験結果では、UniGen-1.5が競争力のある理解と生成パフォーマンスを示しています。具体的には、UniGen-1.5はGenEvalおよびImgEditベンチマークでそれぞれ0.89および4.31の総合スコアを達成し、BAGELなどの最先端モデルを上回り、GPT-Image-1のようなプロプライエタリモデルと同等のパフォーマンスに到達しています。
</details>

<details>
<summary> 英語要旨 </summary>

We present UniGen-1.5, a unified multimodal large language model (MLLM) for advanced image understanding, generation and editing. Building upon UniGen, we comprehensively enhance the model architecture and training pipeline to strengthen the image understanding and generation capabilities while unlocking strong image editing ability. Especially, we propose a unified Reinforcement Learning (RL) strategy that improves both image generation and image editing jointly via shared reward models. To further enhance image editing performance, we propose a light Edit Instruction Alignment stage that significantly improves the editing instruction comprehension that is essential for the success of the RL training. Experimental results show that UniGen-1.5 demonstrates competitive understanding and generation performance. Specifically, UniGen-1.5 achieves 0.89 and 4.31 overall scores on GenEval and ImgEdit benchmarks that surpass the state-of-the-art models such as BAGEL and reaching performance comparable to proprietary models such as GPT-Image-1.
</details>

---

### Learning from Itself: Mining Internal Knowledge from Vision Language Models for Continual Learning
著者: Yizheng Gong, Siyue Yu, Waleed Al-Nuaimy, Jimin Xiao

<details>
<summary> 日本語要旨 </summary>

ビジョン言語モデルのCLIPはゼロショット認識に優れていますが、継続的学習において2つの重要な問題に直面しています：（1）事前学習キャプションと事後学習クラス名の間の厳しい分布ギャップ、および（2）ビジョンオンリーとデュアルエンコーダーアプローチの性能不一致—ビジョンオンリー手法は細部にわたるタスクで20%高い精度を達成する一方、CLIPは自然画像で優位です。これらの課題に対処するために、私たちはCLIPの内部知識を探索して学習する「Learning from Itself（LfI）」を提案します。まず、学習可能なトークンを最適化してCLIPの対比的損失を最小化し、事前学習と微調整の分布ギャップを埋める補助的な訓練信号を生成することで、外部モデルを必要とせずに問題（1）を解決します。次に、CLIPのテキストエンコーダーと一時的なビジョン分類器間の知識転送を動的に重み付けする適応的相互教師学習を導入し、それぞれのインスタント性能に基づいて強い枝がより多く教え、弱い枝がより多く学ぶことで問題（2）に対処します。推論時には、両方の枝から識別力を吸収した元のCLIPアーキテクチャのみが使用されます。LfIは複数の継続的学習ベンチマークで最先端の結果を達成し、CLIPが新たなタスクを効果的に自己教育することで継続的に学び続ける能力を示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Vision-language models like CLIP excel at zero-shot recognition but struggle with continual learning due to two critical issues: (1) severe distribution gap between pretraining captions and post-training class names, and (2) performance mismatch between vision-only and dual-encoder approaches—vision-only methods achieve 20% higher accuracy on fine-grained tasks while CLIP dominates on natural images. We propose Learning from Itself (LfI), which mines CLIP's internal knowledge to address both challenges. First, we generate pseudo-captions by optimizing learnable tokens to minimize CLIP's contrastive loss, creating auxiliary training signals that bridge the pretraining-finetuning distribution gap without external models. Second, we introduce adaptive mutual distillation that dynamically weights knowledge transfer between CLIP's text encoder and a temporary vision classifier based on their instantaneous performance—stronger branches teach more, weaker ones learn more. At inference, only the original CLIP architecture is used, having absorbed discriminative knowledge from both branches. LfI achieves state-of-the-art results across multiple continual learning benchmarks, demonstrating that CLIP can effectively teach itself to continually learn new tasks.
</details>

---

### BiGMINT: Biologically-guided Hierarchical Multimodal Integration for Modeling Multiple Compound Activities in Drug Discovery
著者: Pushpak Pati, Bo Li, Abbas Khan, Tomé Albuquerque, Steffen Jaensch, Amina Mollaysa, Walid Hassan, Samantha J Allen, Joke Reumers, Helai Mohammad, Scott Oloff, Tommaso Mansi, Rui Liao, Dmytro Lituiev, Zhoubing Xu

<details>
<summary> 日本語要旨 </summary>

薬剤探索において、化合物活性モデリングは重要であり、正確な *in silico* 予測が高価で時間のかかるターゲット特異的実験試験への依存を大幅に削減することができます。化合物活性モデリングのための従来の機械学習アプローチは、通常、化学プロテオミクス中心の分子データまたは表現型中心の画像スクリーンに依存しており、補完的な生物学的シグナルを捉える能力が限られています。多様モーダルアプローチは有望ですが、分子メカニズムと細胞応答の相互作用をしばしば捉えきれません。本論文では、化学プロテオミクスデータと高コンテンツ画像（HCI）データを階層的に統合する生物学的ガイド付き多様モーダルフレームワーク **BiGMINT** を紹介します。これは、化学プロテオミクスによる表現型集約、タスク認識のクロスモーダル融合、およびタンパク質間相互作用事前情報を導入して活性をモデリングします。私たちの大規模な自社データセット（U2OS と iNeuron からの99K および 40K 化合物–HCI ペア）において、**BiGMINT** は最良の単一モーダルおよび多様モーダル手法と比較して、平均 AUCROC を最大で10.0% と4.2% 向上させ、高性能タスクカバレッジを最大で103% と56% 増加させました。詳細な分析により、これらの向上はモーダル補完性から生じており、タンパク質間事前情報が難しい活性のモデリングを強化することが示されました。論文受理時にコードを公開して再現性を保証します。
</details>

<details>
<summary> 英語要旨 </summary>

Compound activity modeling is critical for drug discovery, where accurate *in silico* predictions can significantly reduce reliance on expensive, time‑consuming target-specific experimental assays. Traditional machine learning approaches for compound activity modeling typically rely on either chemoproteomics-centric molecular data or phenotype-centric imaging screens, limiting their ability to capture complementary biological signals. While multimodal approaches show promise, they often fail to capture the interplay between molecular mechanisms and cellular responses. In this paper, we present **BiGMINT**, a **Bi**ologically **G**uided **M**ultimodal framework that hierarchically **INT**egrates chemoproteomic and high-content imaging (HCI) data, introducing chemoproteomics-guided phenotypic aggregation, task-aware cross-modal fusion, and protein–protein interaction priors for modeling activities. On two large-scale in-house datasets, with 99K and 40K compound–HCI pairs from U2OS and iNeuron, **BiGMINT** improves mean AUCROC by up to 10.0% and 4.2%, and high-performing task coverage by up to 103% and 56% over best unimodal and multimodal methods. Thorough analysis revealed mechanistic insights, showing these gains stem from modality complementarity, and protein–protein priors enhance modeling of challenging activities. Code will be released for reproducibility on acceptance of the paper.
</details>

---

### MedCLIPSeg: Probabilistic Vision-Language Adaptation for Data-Efficient and Generalizable Medical Image Segmentation
著者: Taha Koleilat, Hojat Asgariandehkordi, Omid Nejatimanzari, Berardino Barile, Yiming Xiao, Hassan Rivaz

<details>
<summary> 日本語要旨 </summary>

医用画像セグメンテーションは、トレーニングに必要な限られたアノテーション、曖昧な解剖学的特徴、ドメインシフトのために依然として課題が残っています。CLIPのようなビジョン・ランゲージモデルは強力なクロスモーダル表現を提供しますが、そのテキストガイド付き医用画像セグメンテーションへの潜在能力は未だ十分に探求されていません。私たちは、CLIPを適応させることで堅牢性、データ効率性、不確実性認識を持つ医用画像セグメンテーションのための新しいフレームワークMedCLIPSegを提案します。私たちのアプローチは、パッチレベルのCLIP埋め込みを確率的なクロスモーダル注意を通じて活用し、画像とテキストトークン間で双方向の相互作用を可能にし、予測不確実性の明示的なモデリングを行います。また、柔軟なパッチレベルの対照的損失と組み合わせることで、多様なテキストプロンプトにわたってより微細な意味学習を促進し、MedCLIPSegはデータ効率性とドメイン一般化能力の向上を実現します。6つの臓器と5つの画像モダリティにまたがる16のデータセットで行った広範な実験では、MedCLIPSegは精度、効率性、堅牢性の面で既存手法を上回り、セグメンテーション結果の局所的信頼性を強調する解釈可能な不確実性マップを提供します。この研究は、テキスト駆動型医用画像セグメンテーションにおける確率的ビジョン・ランゲージモデリングの可能性を示しています。コードとテキストプロンプトは受理後に公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Medical image segmentation remains challenging due to limited annotations for training, ambiguous anatomical features, and domain shifts. While vision-language models such as CLIP offer strong cross-modal representations, their potential for dense, text-guided medical image segmentation remains underexplored. We present MedCLIPSeg, a novel framework that adapts CLIP for robust, data-efficient, and uncertainty-aware medical image segmentation. Our approach leverages patch-level CLIP embeddings through probabilistic cross-modal attention, enabling bidirectional interaction between image and text tokens and explicit modeling of predictive uncertainty. Together with a soft patch-level contrastive loss that encourages more nuanced semantic learning across diverse textual prompts, MedCLIPSeg effectively improves data efficiency and domain generalizability. Extensive experiments across 16 datasets spanning five imaging modalities and six organs demonstrate that MedCLIPSeg outperforms prior methods in accuracy, efficiency, and robustness, while providing interpretable uncertainty maps that highlight local reliability of segmentation results. This work demonstrates the potential of probabilistic vision-language modeling for text-driven medical image segmentation. Code and text prompts will be made publicly available upon acceptance.
</details>

---

### FAVE: A Structured Benchmark for Fine-Grained Audio-Visual Temporal Evaluation in Multimodal LLMs
著者: Weiheng Lu, An Yu, Jian Li, Zhenfei Zhang, Felix X. Ye, Ming-Ching Chang

<details>
<summary> 日本語要旨 </summary>

オーディオビジュアル大規模言語モデル（AVLLM）は、視覚的および聴覚的コンテンツの理解において顕著な進歩を遂げています。しかし、オーディオとビジュアルストリーム間の微細な時間関係を捉える能力は十分に評価されていません。これに対処するため、私たちはFAVE（Fine-grained Audio-Visual Temporal Evaluation）という包括的なベンチマークを導入します。このベンチマークは、時間認識の三つの核心次元を対象にしています：クロスモーダル時間整合（FAVE-align）、イベント時間関係（FAVE-low）、詳細な瞬間キャプション（FAVE-high）。FAVEを構築するため、私たちはショット境界検出、自動キャプショニング、GPT支援による洗練を統合したスケーラブルなアノテーションパイプラインを提案します。これにより、時間的に根拠のある高品質なデータが生成されます。オープンソースおよびクローズドソースの両方の12の最先端マルチモーダルLLMで広範囲にわたる実験を行った結果、特にジョイントオーディオビジュアルタスクにおいて、マルチモーダル統合、時間関係とタイムスタンプのローカライゼーションにおける重要な限界が明らかになりました。これらの発見は、AVLLMが実世界のビデオコンテンツを理解するためにより良い時間モデリングが必要であることを強調しています。FAVEは、時間的に意識したマルチモーダルシステムの進歩を促す厳格な試験場として機能し、受理され次第公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Audio-visual large language models (AVLLMs) have made significant strides in understanding visual and auditory content. However, their ability to capture fine-grained temporal relationships between audio and visual streams remains insufficiently evaluated. To address this, we introduce FAVE (Fine-grained Audio-Visual Temporal Evaluation), a comprehensive benchmark targeting three core dimensions of temporal perception: cross-modal temporal alignment (FAVE-align), event temporal relationship (FAVE-low), and detailed moment captioning (FAVE-high). To construct FAVE, we propose a scalable annotation pipeline that integrates shot boundary detection, automated captioning, and GPT-assisted refinement to produce temporally grounded, high-quality data. Extensive experiments on twelve state-of-the-art multimodal LLMs, both open-source and closed-source, reveal key limitations in multimodal integration, temporal relationship and timestamp localization, especially for joint audio-visual tasks. These findings highlight the need for better temporal modeling to improve AVLLMs' understanding of real-world video content. FAVE serves as a rigorous testbed for advancing temporally aware multimodal systems, and will be publicly released upon acceptance.
</details>

---

### SpatialStack: Layered Geometry-Semantic Fusion for 3D VLM Spatial Reasoning
著者: Jian Zhang, Shijie Zhou, Bangya LIU, Achuta Kadambi, Zhiwen Fan

<details>
<summary> 日本語要旨 </summary>

大規模なビジョン言語モデル（VLM）は、具現化されたAIシステムや物理的AIシステムにとって不可欠な3D空間推論の信頼性をまだ確保できていません。この制限は、細部にわたる3D幾何学や空間関係を捉えられないことから生じます。最近の取り組みでは多視点幾何学トランスフォーマーをVLMに導入しましたが、通常はビジョンエンコーダーと幾何学エンコーダーから深層特徴のみを融合させ、豊富な階層信号を捨てることで空間理解における基本的なボトルネックを生じさせます。この問題を克服するために、私たちはSpatialStackを提案します。これは、ビジョン、幾何学、言語表現をモデル階層全体で逐次的に整列させる一般的な階層融合フレームワークです。従来の遅い段階でのビジョン-幾何学融合を超えて、SpatialStackは言語バックボーンと同期しながら多層幾何学的特徴を積み重ねることにより、局所的な幾何学的精度と全体的な文脈セマンティクスの両方を捉えることができます。このフレームワークに基づいて、私たちはVLM-SpatialStackというモデルを開発しました。これは複数の3D空間推論ベンチマークで最先端の性能を達成しています。広範な実験とアブレーションにより、私たちの多層融合戦略が3D理解を一貫して向上させ、多様な空間推論タスクにわたって堅牢に汎化することが示されており、SpatialStackは次世代のマルチモーダル物理AIシステムにおけるビジョン-言語-幾何学統合の効果的で拡張可能な設計パラダイムとして確立されています。
</details>

<details>
<summary> 英語要旨 </summary>

Large vision-language models (VLMs) still struggle with reliable 3D spatial reasoning, a core capability for embodied and physical AI systems. This limitation arises from their inability to capture fine-grained 3D geometry and spatial relationships. While recent efforts have introduced multi-view geometry transformers into VLMs, they typically fuse only the deep-layer features from vision and geometry encoders, discarding rich hierarchical signals and creating a fundamental bottleneck for spatial understanding. To overcome this, we propose SpatialStack, a general hierarchical fusion framework that progressively aligns vision, geometry, and language representations across the model hierarchy. Moving beyond conventional late-stage vision-geometry fusion, SpatialStack stacks and synchronizes multi-level geometric features with the language backbone, enabling the model to capture both local geometric precision and global contextual semantics. Building upon this framework, we develop VLM-SpatialStack, a model that achieves state-of-the-art performance on multiple 3D spatial reasoning benchmarks. Extensive experiments and ablations demonstrate that our multi-level fusion strategy consistently enhances 3D understanding and generalizes robustly across diverse spatial reasoning tasks, establishing SpatialStack as an effective and extensible design paradigm for vision-language-geometry integration in next-generation multimodal physcial AI systems.
</details>

---

### P-Flow: Prompting Visual Effects Generation
著者: Rui Zhao, Mike Zheng Shou

<details>
<summary> 日本語要旨 </summary>

最近の動画生成モデルにおける進歩は、テキストプロンプトに従う能力を大幅に向上させました。しかし、時間的に進化し、外観駆動型の現象であるダイナミックビジュアルエフェクト（例えば、物体の圧縮や爆発など）のカスタマイズは未だ十分に探求されていません。動作のカスタマイズや制御に関する以前の研究は、主に対象物またはカメラの低レベルな動きに焦点を当てており、これらは明示的な制御信号（例えば、運動軌道）でガイドすることが可能です。対照的に、ダイナミックビジュアルエフェクトはテキストプロンプトを用いた制御により自然に適しています。しかし、これらの効果を正確に指定する単一のプロンプトを作成することは、複雑な時間的推論や時間をかけた反復的な改善が必要であるため、人間にとって困難で時間がかかります。この課題に対処するために、私たちはP-Flowという新しいトレーニングフリーのフレームワークを提案します。これは、動画生成におけるダイナミックビジュアルエフェクトのカスタマイズを行う際に、基礎となるモデルを変更することなく実現します。P-Flowは視覚言語モデルのセマンティックおよび時間的推論能力を活用し、参照動画のビジュアルエフェクトと生成された出力の不一致に基づいてプロンプトを最適化します。反復的な改善を通じて、プロンプトは新しいシーンで望ましいダイナミックエフェクトをより良く誘発するように進化します。実験では、P-Flowが高品質かつ多様なビジュアルエフェクトのカスタマイズを達成し、テキストから動画および画像から動画生成の両方のタスクで他のモデルを上回ることが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advancements in video generation models have significantly improved their ability to follow text prompts. However, the customization of dynamic visual effects, defined as temporally evolving and appearance-driven visual phenomena like object crushing or explosion, remains underexplored. Prior works on motion customization or control mainly focus on low-level motions of the subject or camera, which can be guided using explicit control signals such as motion trajectories. In contrast, dynamic visual effects involve higher-level semantics that are more naturally suited for control via text prompts. However, it is hard and time-consuming for humans to craft a single prompt that accurately specifies these effects, as they require complex temporal reasoning and iterative refinement over time. To address this challenge, we propose P-Flow, a novel training-free framework for customizing dynamic visual effects in video generation without modifying the underlying model. By leveraging the semantic and temporal reasoning capabilities of vision-language models, P-Flow performs test-time prompt optimization, refining prompts based on the discrepancy between the visual effects of the reference video and the generated output. Through iterative refinement, the prompts evolve to better induce the desired dynamic effect in novel scenes. Experiments demonstrate that P-Flow achieves high-fidelity and diverse visual effect customization and outperforms other models on both text-to-video and image-to-video generation tasks.
</details>

---

### TeamHOI: Learning A Unified Policy for Cooperative Human-Object Interactions with Any Team Size
著者: Stefan Lionar, Gim Hee Lee

<details>
<summary> 日本語要旨 </summary>

物理ベースの人間型ロボット制御は、単一エージェントのリアルで高性能な動作を可能にする点で顕著な進歩を遂げていますが、協調的な人物-オブジェクト相互作用（HOI）への拡張は依然として困難です。私たちはTeamHOIというフレームワークを提案します。これにより、任意の数の協力エージェント間で協調的なHOIを処理するための単一の分散型ポリシーが可能になります。各エージェントはローカル観測を用いて動作し、チームメイトトークンを持つTransformerベースのポリシーネットワークを通じて他のチームメイトに注意を払うことで、可変サイズのチーム間でスケーラブルな調整が可能です。協調的HOIデータの不足を解決しつつ動作リアリズムを維持するために、私たちはさらにマスク付き敵対的運動事前知識（AMP）戦略を導入します。これは単一人間の参考動作を使用しつつ、トレーニング中にオブジェクトと接触する身体部位をマスキングします。マスクされた領域はタスク報酬を通じて導かれ、多様で物理的に妥当な協調動作が生成されます。TeamHOIは2から8の人間型エージェントと異なるオブジェクト幾何学を含む難易度の高い協力的運搬タスクで評価します。最後に、安定した運搬を促進するために、チームサイズおよび形状非依存の形成報酬を設計します。TeamHOIは単一ポリシーで多様な配置にわたる統合的な協力を示し、高い成功率を達成しています。
</details>

<details>
<summary> 英語要旨 </summary>

Physics-based humanoid control has achieved remarkable progress in enabling realistic and high-performing single-agent behaviors, yet extending these capabilities to cooperative human-object interaction (HOI) remains challenging. We present TeamHOI, a framework that enables a single decentralized policy to handle cooperative HOIs across any number of cooperating agents. Each agent operates using local observations while attending to other teammates through a Transformer-based policy network with teammate tokens, allowing scalable coordination across variable team sizes. To enforce motion realism while addressing the scarcity of cooperative HOI data, we further introduce a masked Adversarial Motion Prior (AMP) strategy that uses single-human reference motions while masking object-interacting body parts during training. The masked regions are then guided through task rewards to produce diverse and physically plausible cooperative behaviors. We evaluate TeamHOI on a challenging cooperative carrying task involving two to eight humanoid agents and varied object geometries. Finally, to promote stable carrying, we design a team-size- and shape-agnostic formation reward. TeamHOI achieves high success rates and demonstrates coherent cooperation across diverse configurations with a single policy.
</details>

---

### Ego-STAR: Spatiotemporal Hints for Egocentric Video Understanding
著者: Arsha Nagrani, Jasper Uijlings, Shyamal Buch, Tobias Weyand, Sudheendra Vijayanarasimhan, Bo Hu, Ramin Mehran, David A. Ross, Cordelia Schmid

<details>
<summary> 日本語要旨 </summary>

ビデオ推論モデルは、エゴセントリックおよびエンバディッドエージェントの重要な構成要素です。しかし、これらのモデルを評価するための標準的なベンチマークは、出力（例えば質問への答え）のみを評価し、中間推論ステップの評価を行わず、多くがテキストドメインでの回答に限定されています。私たちは、エゴセントリックな視覚的推論を評価するためのベンチマークとしてEgoSTARを導入します。最近の高品質なビデオデータソース（エゴセントリックおよびエンバディッド設定で記録されたもの）に、挑戦的な多ステップマルチモーダル質問と時間空間密度の高い人手による推論トレースを追加しました。ベンチマーク実験では、最先端のモデルでも人間のパフォーマンスとの大きなギャップがあることが示されています。このギャップを詳細に調査するために、各推論トレースに質問を解決するために必要な興味の対象物を注釈しました。これらの対象物については時間空間マスクアノテーションも提供しています。広範囲な評価を通じて、フロンティアモデルが「どこで」、「いつ」見るべきかのヒントによって促された場合、パフォーマンスが大幅に向上することを特定しました。EgoSTARは公開され、エゴセントリック推論の進歩を促進します。
</details>

<details>
<summary> 英語要旨 </summary>

Video reasoning models are a core component of egocentric and embodied agents. However, standard benchmarks for assessing models provide only evaluation of the output (e.g., the answer to a question), without evaluation of intermediate reasoning steps, and most provide answers only in the text domain. We introduce EgoSTAR, a benchmark for evaluating complex egocentric visual reasoning. We extend recent high-quality video data sources recorded from egocentric / embodied settings with a set of challenging, multi-step multimodal questions and spatiotemporally-dense human-annotated reasoning traces. Benchmarking experiments show that state-of-the-art models still have a large gap to human performance. To investigate this gap in detail, we annotate each reasoning trace in the dataset with the objects of interest required to solve the question, for which we also have spatio-temporal mask annotations. Through extensive evaluations, we identify that if frontier models are prompted with hints of `where' and `when' to look, we can get substantial improvements in performance. EgoSTAR will be released publicly to foster progress in egocentric reasoning.
</details>

---

### UniRain: Unified Image Deraining with RAG-based Dataset Distillation and Multi-objective Reweighted Optimization
著者: Qianfeng Yang, Qiyuan Guan, Xiang Chen, Jiyu Jin, Guiyue Jin, Jiangxin Dong

<details>
<summary> 日本語要旨 </summary>

雨除去の分野では大きな進歩が遂げられていますが、多くの既存手法は特定の種類の雨による劣化に対して開発されており、多様な実世界の雨天シーンに一般化できないことがあります。したがって、異なる種類の雨による劣化をユニバーサルフレームワーク内で効果的にモデリングすることは、実世界の画像除雨において重要です。本論文では、昼夜問わず雨ストライプや雨滴によって劣化した画像を復元できる有効な統一的な画像除雨フレームワーク「UniRain」を提案します。統一モデルの汎用性をさらに向上させるため、すべての公開されている除雨データセットから高品質なトレーニングサンプルを選択することでより良い混合トレーニングが可能になる知的リトリーバル強化生成（RAG）ベースのデータセット縮小パイプラインを構築しました。さらに、多目的再重み付け最適化戦略をシンメトリックなモジュール・オブ・エキスパーツ（MoE）アーキテクチャに組み込むことで、多様なシーンにわたる一貫した性能の向上と堅牢性を図りました。広範な実験により、私たちが提案するベンチマークおよび複数の公開データセットで最先端モデルに対して一貫して有利に機能することを示しました。コードとデータセットは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Despite significant progress has been made in image deraining, we note that most existing methods are often developed for only specific types of rain degradation and fail to generalize across diverse real-world rainy scenes. How to effectively model different rain degradations within a universal framework is important for real-world image deraining. In this paper, we propose UniRain, an effective unified image deraining framework capable of restoring images degraded by rain streak and raindrop under both daytime and nighttime conditions. To better enhance unified model generalization, we construct an intelligent retrieval augmented generation (RAG)-based dataset distillation pipeline that selects high-quality training samples from all public deraining datasets for better mixed training. Furthermore, we incorporate a simple yet effective multi-objective reweighted optimization strategy into the asymmetric mixture-of-experts (MoE) architecture to facilitate consistent performance and improve robustness across diverse scenes. Extensive experiments show that our framework performs consistently favorably against the state-of-the-art models on both our proposed benchmarks and multiple public datasets. Code and dataset will be available.
</details>

---

### Interact2Ar: Full-Body Human-Human Interaction Generation Via Autoregressive Diffusion Models
著者: Pablo Ruiz-Ponce, Sergio Escalera, Jose Garcia-Rodriguez, Jiankang Deng, Rolandos Alexandros Potamias

<details>
<summary> 日本語要旨 </summary>

リアルな人間同士の相互作用を生成することは、高品質な個々の身体や手の動きだけでなく、すべての参加者間の一貫した調整も必要とする困難なタスクです。利用可能なデータの制約と学習の複雑性が増すことにより、従来の方法は手の動きを無視する傾向があり、相互作用のリアリズムや表現力を限定しています。さらに、現在の拡散ベースのアプローチは全体の動作シーケンスを同時に生成するため、人間の相互作用の反応的で適応的な性質を捉える能力が制限されています。これらの制約に対処するために、私たちはInteract2Arを導入します。これは、フルボディの人間同士の相互作用を生成する初のエンドツーエンドのテキスト条件付き自己回帰拡散モデルです。Interact2Arは専用の並列ブランチを通じて詳細な手の運動学を組み込むことで、高精度なフルボディ生成が可能になります。さらに、私たちは新しいメモリ技術を備えた自己回帰パイプラインを導入し、効率的な大きなコンテキストウィンドウを使用して人間の相互作用に固有の変動性への適応を促進します。私たちのモデルの適応性は、時間的な動作構成、リアルタイムでの障害への適応、および対話型から多人数シナリオへの拡張を含む一連の下流アプリケーションを可能にします。生成された動作を検証するために、フルボディ相互作用を評価するために特別に設計された堅牢な評価者と拡張メトリクスのセットを導入します。定量的および定性的実験を通じて、Interact2Arの最先端のパフォーマンスを示します。
</details>

<details>
<summary> 英語要旨 </summary>

Generating realistic human-human interactions is a challenging task that requires not only high-quality individual body and hand motions, but also coherent coordination among all interactants. Due to limitations in available data and increased learning complexity, previous methods tend to ignore hand motions, limiting the realism and expressivity of the interactions. Additionally, current diffusion-based approaches generate entire motion sequences simultaneously, limiting their ability to capture the reactive and adaptive nature of human interactions. To address these limitations, we introduce Interact2Ar, the first end-to-end text-conditioned autoregressive diffusion model for generating full-body, human-human interactions. Interact2Ar incorporates detailed hand kinematics through dedicated parallel branches, enabling high-fidelity full-body generation. Furthermore, we introduce an autoregressive pipeline coupled with a novel memory technique that facilitates adaptation to the inherent variability of human interactions using efficient large context windows. The adaptability of our model enables a series of downstream applications, including temporal motion composition, real-time adaptation to disturbances, and extension beyond dyadic to multi-person scenarios. To validate the generated motions, we introduce a set of robust evaluators and extended metrics designed specifically for assessing full-body interactions. Through quantitative and qualitative experiments, we demonstrate the state-of-the-art performance of Interact2Ar.
</details>

---

### SwiftVLA: Unlocking Spatiotemporal Dynamics for Lightweight VLA Models at Minimal Overhead
著者: Chaojun Ni, Chen Cheng, Xiaofeng Wang, Zheng Zhu, Wenzhao Zheng, Boyuan Wang, Tianrun Chen, Guosheng Zhao, Haoyun Li, Zhehao Dong, Qiang Zhang, Yun Ye, Yang Wang, Guan Huang, Wenjun Mei

<details>
<summary> 日本語要旨 </summary>

ビジョン・ランゲージ・アクション（VLA）モデルは、事前学習済みのビジョン・ランゲージ・モデル（VLMs）を基に構築されており、大きな可能性を示していますが、そのパラメータ数の多さから実用的ではありません。この問題を軽減するために、軽量VLMの使用が探求されましたが、これは空間時間的推論能力を犠牲にします。3D入力を組み込むことで改善できるという方法もありますが、通常は大規模なVLMを用いて3Dと2Dの入力を融合し、依然として時間的理解に欠けています。そこで、我々はSwiftVLAと呼ばれるアーキテクチャを提案します。これはコンパクトなモデルに4Dの理解能力を強化しつつ設計効率を維持するものです。具体的に、我々のアプローチでは、2D画像から段階的に4D特徴を抽出する事前学習済みの4D視覚幾何トランスフォーマーと、時間キャッシュが特徴です。次に、VLMが2D画像と4D特徴の両方を活用する能力を強化するために、\textit{Fusion Tokens}（学習可能なトークン）を導入します。これらは将来予測目的で訓練され、アクション生成のための統一表現を生成するように設計されています。最後に、4D入力をランダムにVLMへマスクし、そのマスクされた特徴を再構成するようにVLAを訓練するマスク・アンド・リコンストラクト戦略を導入します。この自己再構築目的は効果的な4D表現の学習を促進し、インフェレンス時に4Dブランチを削除してもパフォーマンスの低下が最小限であることを可能にします。実際およびシミュレートされた環境での広範な実験では、SwiftVLAは軽量ベースラインを上回り、最大7倍大きいVLAsと競合することが示されました。エッジデバイスにおいては、SwiftVLAは\(\pi_0\)より18倍高速でありながら、メモリフットプリントを12倍削減して同等のパフォーマンスを達成します。
</details>

<details>
<summary> 英語要旨 </summary>

Vision–Language–Action (VLA) models built on pretrained Vision–Language Models (VLMs) show strong potential but are limited in practicality due to their large parameter counts. To mitigate this issue, using a lightweight VLM has been explored, but it compromises spatiotemporal reasoning. Although some methods suggest that incorporating additional 3D inputs can help, they usually rely on large VLMs to fuse 3D and 2D inputs and still lack temporal understanding. Therefore, we propose SwiftVLA, an architecture that enhances a compact model with 4D understanding while preserving design efficiency. Specifically, our approach features a pretrained 4D visual geometry transformer with a temporal cache that incrementally extracts 4D features from 2D images. Then, to enhance the VLM’s ability to exploit both 2D images and 4D features, we introduce \textit{Fusion Tokens}, a set of learnable tokens trained with a future prediction objective to generate unified representations for action generation. Finally, we introduce a mask-and-reconstruct strategy that randomly masks 4D inputs to the VLM and trains the VLA to reconstruct the masked features. This self-reconstruction objective helps learn effective 4D representations, allowing the 4D branch to be dropped at inference with minimal performance loss. Extensive experiments in real and simulated environments show that SwiftVLA outperforms lightweight baselines and rivals VLAs up to $7\times$ larger. On edge devices, SwiftVLA achieves comparable performance while being $18\times$ faster than the $\pi_0$ and reducing the memory footprint by $12\times$.
</details>

---

### ShowUI-π: Flow-based Generative Models As GUI Dexterous Hands
著者: Siyuan Hu, Kevin Qinghong Lin, Mike Zheng Shou

<details>
<summary> 日本語要旨 </summary>

人間のような自動化をロボティクスやデジタル環境で実現するためには、器用な操作が可能な知能エージェントの構築が不可欠です。しかし、既存のGUIエージェントは離散的なクリック予測（x, y）に依存しており、これによって自由形式で閉ループの軌道（例えば、進捗バーをドラッグすること）が制限されています。これらは連続的なリアルタイムの認識と調整を必要とします。本研究では、初めてのフローベースの生成モデルであるShowUI-πをGUI器用手として開発しました。以下の設計が特徴です：(i) 統一された離散的・連続的アクション、離散的なクリックと連続的なドラッグを共有モデル内で統合し、多様なインタラクションモードに柔軟に適応可能にします；(ii) ドラッグのアクション生成のためのフローベース方式、連続的な視覚観察からインクリメンタルなカーソル調整を軽量なアクション専門家によって予測し、滑らかで安定した軌道を確保します；(iii) ドラッグ用のトレーニングデータとベンチマーク、私たちはPowerPointやAdobe Premiere Proなど5つのドメインにわたって20,000本のドラッグ軌道を手動で収集・合成し、GUIエージェントのドラッグ能力を評価する包括的なオンラインおよびオフライン評価プロトコルを備えたScreenDragベンチマークを導入します。実験結果によると、独自のGUIエージェントは依然としてScreenDragで苦戦しています（例：Operatorスコア13.27、最高のGemini-2.5-CUAが22.18）。対照的に、ShowUI-πは450Mパラメータしか使用せずに26.98を達成し、タスクの難しさと私たちのアプローチの有効性を強調しています。この作業がデジタル世界でのGUIエージェントの人間のような器用な制御に向けて進展することを期待します。
</details>

<details>
<summary> 英語要旨 </summary>

Building intelligent agents capable of dexterous manipulation is essential for achieving human-like automation in both robotics and digital environments. However, existing GUI agents rely on discrete click predictions (x,y), which prohibits free-form, closed-loop trajectories (e.g. dragging a progress bar) that require continuous, on-the-fly perception and adjustment. In this work, we develop ShowUI-π, the first flow-based generative model as GUI dexterous hand, featuring the following designs:(i) Unified Discrete–Continuous Actions, integrating discrete clicks and continuous drags within a shared model, enabling flexible adaptation across diverse interaction modes;(ii) Flow-based Action Generation for drag modeling, which predicts incremental cursor adjustments from continuous visual observations via a lightweight action expert, ensuring smooth and stable trajectories;(iii) Drag Training data and Benchmark, where we manually collect and synthesize 20K drag trajectories across five domains (e.g. PowerPoint, Adobe Premiere Pro), and introduce ScreenDrag, a benchmark with comprehensive online and offline evaluation protocols for assessing GUI agents’ drag capabilities. Our experiments show that proprietary GUI agents still struggle on ScreenDrag (e.g. Operator scores 13.27, and the best Gemini-2.5-CUA reaches 22.18). In contrast, ShowUI-π achieves 26.98 with only 450M parameters, underscoring both the difficulty of the task and the effectiveness of our approach. We hope this work advances GUI agents toward human-like dexterous control in digital world.
</details>

---

### StreamDiT: Real-Time Streaming Text-to-Video Generation
著者: Akio Kodaira, Tingbo Hou, Ji Hou, Markos Georgopoulos, Felix Juefei-Xu, Masayoshi Tomizuka, Yue Zhao

<details>
<summary> 日本語要旨 </summary>

最近、トランスフォーマーをベースとした拡散モデルを数十億パラメータにスケールアップすることで、テキストからビデオ（T2V）生成の分野で大きな進歩が達成されました。これにより高品質なビデオを生成可能になりました。しかし、既存モデルは通常、オフラインで短いクリップのみを生成するため、インタラクティブやリアルタイムアプリケーションへの適用が制限されています。本論文ではこれらの課題に対処し、ストリーミングビデオ生成モデルであるStreamDiTを提案します。StreamDiTのトレーニングは移動バッファを追加することでフロー一致に基づいています。さらに、コンテンツの一貫性と視覚品質を向上させるために、異なる分割スキームのバッファフレームを用いた混合トレーニングを設計しました。StreamDiTモデリングは時間埋め込みとウィンドウ注意が変動するadaLN DiTに基づいています。提案方法の実践のため、4Bパラメータを持つStreamDiTモデルをトレーニングしました。また、StreamDiT専用に設計されたマルチステップ蒸留法も提案します。選択した分割スキームの各セグメントでサンプリング蒸留を行います。蒸留後、関数評価回数（NFEs）はバッファ内のチャンク数にまで減少します。最終的に、我々の蒸留モデルは1つのGPU上でリアルタイムパフォーマンスを16 FPSで達成し、512p解像度でビデオストリームを生成可能です。本手法を定量的指標と人間評価によって評価します。我々のモデルは、例えばストリーミング生成、インタラクティブ生成、ビデオからビデオへの変換などのリアルタイムアプリケーションを可能にします。
</details>

<details>
<summary> 英語要旨 </summary>

Recently, great progress has been achieved in text-to-video (T2V) generation by scaling transformer-based diffusion models to billions of parameters, which can generate high-quality videos. However, existing models typically produce only short clips offline, restricting their use cases in interactive and real-time applications. This paper addresses these challenges by proposing StreamDiT, a streaming video generation model. StreamDiT training is based on flow matching by adding a moving buffer. We design mixed training with different partitioning schemes of buffered frames to boost both content consistency and visual quality. StreamDiT modeling is based on adaLN DiT with varying time embedding and window attention. To practice the proposed method, we train a StreamDiT model with 4B parameters. In addition, we propose a multistep distillation method tailored for StreamDiT. Sampling distillation is performed in each segment of a chosen partitioning scheme. After distillation, the total number of function evaluations (NFEs) is reduced to the number of chunks in a buffer. Finally, our distilled model reaches real-time performance at 16 FPS on one GPU, which can generate video streams at 512p resolution. We evaluate our method through both quantitative metrics and human evaluation. Our model enables real-time applications, e.g. streaming generation, interactive generation, and video-to-video.
</details>

---

### EditMGT: Unleashing Potentials of Masked Generative Transformers in Image Editing
著者: Wei Chow, Linfeng Li, Lingdong Kong, Zefeng Li, Qi Xu, Hang Song, Tian Ye, Xian Wang, Jinbin Bai, Shilin Xu, Xiangtai Li, Junting Pan, Shaoteng Liu, Ran Zhou, Tianshu Yang, Songhua Liu

<details>
<summary> 日本語要旨 </summary>

最近の拡散モデル（DMs）は画像編集タスクにおいて卓越した視覚品質を達成しています。しかし、DMsのグローバルなノイズ除去ダイナミクスは、局所的な編集対象と全画像コンテキストを本質的に混同し、非ターゲット領域で意図しない変更が生じる原因となっています。この論文では、DMsを超えて注目を移し、マスク付き生成トランスフォーマー（MGTs）を代替アプローチとしてこの課題に取り組むことを提案します。複数のマスクされたトークンを予測することで全体的な洗練ではなく、MGTsは局所化されたデコーディングパラダイムを示し、非関連領域を明示的に保持しながら編集プロセス中の能力を備えています。この洞察に基づき、私たちは最初のMGTベースの画像編集フレームワークであるEditMGTを紹介します。まず、MGTのクロスアテンションマップが編集関連領域を局所化するための情報豊富なローカライゼーション信号を提供し、これらのマップを洗練して微細かつ正確な局所化を達成する多層アテンション統合スキームを考案します。これらの適応的ローカライゼーション結果に基づき、低アテンション領域でトークンフリッピングを制限することで誤った編集を抑制し、意図したターゲット領域に修正を限定しながら周辺の非ターゲット領域の完全性を保持する地域ホールドサンプリングを導入します。EditMGTをトレーニングするために、1024ピクセル以上の高解像度画像を含む7つの多様な編集カテゴリーにわたるCrisp-2Mデータセットを構築します。追加パラメータを導入せず、事前学習済みのテキストから画像へのMGTをアテンション注入によって画像編集モデルに適応させます。4つの標準的なベンチマークで行った広範な実験は、1B未満のパラメータであるにもかかわらず、私たちのモデルが画像類似性の最先端のパフォーマンスを達成し、より速い編集を可能にすることを示しています。さらに、スタイル変更およびスタイル転送タスクでそれぞれ3.6%および17.6%の改善を達成し、比較可能または優れた編集品質を提供します。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advances in diffusion models (DMs) have achieved exceptional visual quality in image editing tasks. However, the global denoising dynamics of DMs inherently conflate local editing targets with the full-image context, leading to unintended modifications in non-target regions. In this paper, we shift our attention beyond DMs and turn to Masked Generative Transformers (MGTs) as an alternative approach to tackle this challenge. By predicting multiple masked tokens rather than holistic refinement, MGTs exhibit a localized decoding paradigm that endows them with the inherent capacity to explicitly preserve non-relevant regions during the editing process. Building upon this insight, we introduce the first MGT-based image editing framework, termed EditMGT. We first demonstrate that MGT's cross-attention maps provide informative localization signals for localizing edit-relevant regions and devise a multi-layer attention consolidation scheme that refines these maps to achieve fine-grained and precise localization. On top of these adaptive localization results, we introduce region-hold sampling, which restricts token flipping within low-attention areas to suppress spurious edits, thereby confining modifications to the intended target regions and preserving the integrity of surrounding non-target areas. To train EditMGT, we construct Crisp-2M, a high-resolution (>1024) dataset spanning seven diverse editing categories. Without introducing additional parameters, we adapt a pre-trained text-to-image MGT into an image editing model through attention injection. Extensive experiments across four standard benchmarks demonstrate that, with fewer than 1B parameters, our model achieves state-of-the-art image similarity performance while enabling faster editing. Moreover, it delivers comparable or superior editing quality, with improvements of 3.6% and 17.6% on style change and style transfer tasks, respectively.
</details>

---

### Generative Video Motion Editing with 3D Point Tracks
著者: Yao-Chih Lee, Zhoutong Zhang, Gabriel Huang, Jui-Hsien Wang, Joon-Young Lee, Jia-Bin Huang, Eli Shechtman, Zhengqi Li

<details>
<summary> 日本語要旨 </summary>

ビデオのナラティブにおいて、カメラと物体の動きは中心的な役割を果たします。しかし、これらの捉えられた動きを正確に編集することは、特に複雑な物体運動がある場合に大きな課題です。現在のモーション制御型画像からビデオへ（I2V）のアプローチでは、一貫したビデオ編集のための全体的なコンテキストが不足していることが多く、ビデオからビデオへ（V2V）の方法は視点変更や基本的な物体移動を提供しますが、細かい物体運動に対する制御は限られています。私たちは、カメラと物体の動きを共同で編集可能にするトラック条件付きV2Vフレームワークを提案します。これを実現するために、ソースビデオとそれに対応する3D点トラック（ソースおよびターゲットの動きを表す）で条件付けられたビデオ生成モデルを用いています。これらの3Dトラックは、豊かなコンテキストを新しい動きに転送しつつスペースタイム的一貫性を保持するための希薄な対応関係を確立します。重要なことに、3Dトラックは2Dトラックに比べて明示的な深度手がかりを提供し、モデルが正確な動き編集のために深度順序を解決し、遮蔽を処理することを可能にします。合成および実際のデータで2段階でトレーニングされた私たちのモデルは、カメラ/物体の共同操作、動き転送、非剛性変形を含む多様な動き編集をサポートし、ビデオ編集における新たなクリエイティブな可能性を解放します。
</details>

<details>
<summary> 英語要旨 </summary>

Camera and object motions are central to a video's narrative. However, precisely editing these captured motions remains a significant challenge, especially under complex object movements. Current motion-controlled image-to-video (I2V) approaches often lack full-scene context for consistent video editing, while video-to-video (V2V) methods provide viewpoint changes or basic object translation, but offer limited control over fine-grained object motion. We present a track-conditioned V2V framework that enables joint editing of camera and object motion. We achieve this by conditioning a video generation model on a source video and paired 3D point tracks representing source and target motions. These 3D tracks establish sparse correspondences that transfer rich context from the source video to new motions while preserving spatiotemporal coherence. Crucially, compared to 2D tracks, 3D tracks provide explicit depth cues, allowing the model to resolve depth order and handle occlusions for precise motion editing. Trained in two stages on synthetic and real data, our model supports diverse motion edits, including joint camera/object manipulation, motion transfer, and non-rigid deformation, unlocking new creative potential in video editing.
</details>

---

### Enhancing Vision Language Models for 4D Perception
著者: Seokju Cho, Abhishek Badki, Hang Su, Jindong Jiang, Ziyao Zeng, Seungryong Kim, Sifei Liu, Orazio Gallo

<details>
<summary> 日本語要旨 </summary>

最近の進歩にもかかわらず、ビジョン言語モデル（VLMs）は依然として世界のダイナミクスを理解することに苦労しています。私たちは、3D運動について推論する能力が困難であるだけでなく、2つの要因によってさらに複雑化されていることを指摘します。第一に、VLMsは運動をその2D画像への射影を通じて間接的に観察しています。第二に、既存のデータセットではオブジェクトとカメラの運動が分離されていません。これらに対処するために、私たちは特にシーン理解における運動関連に焦点を当てたQA生成パイプラインを提示します。カメラとオブジェクトの運動が絡み合うことに特に注意し、従来の方法で追跡するだけでなく、固定参照系（True-Motion Tracking）と呼ばれる新しい方法を用いています。これは運動の直感的な説明を提供します。このパイプラインから、大規模な400Kトレーニングサンプルと2.2Kサンプルのベンチマークを生成しました。既存のモデルを私たちのデータセットでトレーニングすることにより、外部ベンチマークでのパフォーマンス向上が得られ、私たちの方法の有効性が検証されました。
</details>

<details>
<summary> 英語要旨 </summary>

Despite recent advances, Vision Language Models (VLMs) still struggle to grasp the dynamics of the world. We note that the ability to reason about 3D motion, challenging in itself, is further complicated by two factors. First, VLMs observe motion indirectly via its projection on 2D images. Second, existing datasets fail to disentangle object and camera motion. To address these, we present a QA generation pipeline that focuses on motion-related scene understanding. We take particular care of the entanglement of camera and object motion by casting tracking in both the traditional way and in a novel, fixed reference system, dubbed True-Motion Tracking, which provides an intuitive description of motion. From this pipeline, we generate large-scale 400K training samples and a 2.2K-sample benchmark. Training existing models on our dataset yields performance improvements on an external benchmark, validating the effectiveness of our method.
</details>

---

### Region-Adaptive Sampling for Diffusion Transformers
著者: Ziming Liu, Yifan Yang, Chengruidong Zhang, Yiqi Zhang, Lili Qiu, Yang You, Yuqing Yang

<details>
<summary> 日本語要旨 </summary>

拡散モデル（DMs）は、さまざまな分野で生成タスクの最先端として位置づけられていますが、その実行速度を制限する連続的な前方伝播に依存しています。これまでの加速方法は主にサンプリングステップの削減や中間結果の再利用に焦点を当てていました。Diffusion Transformers（DiTs）が可変トークン数を扱う柔軟性を活かし、モデルのフォーカスに基づいて画像領域ごとに異なる更新比率を動的に割り当てる訓練不要のサンプリング戦略であるRASを提案します。私たちの主な観察は、各ステップでDiTsが意味的に重要な領域に集中しており、これらの領域は連続するステップ間で強い連続性を示すということです。この特徴を活用し、RASはフォーカスされた領域だけを更新し、他の領域ではキャッシュされたノイズを再利用します。フォーカスは前ステップの出力から決定されます。Stable Diffusion 3およびLumina-Next-T2Iで評価した結果、RASはそれぞれ最大2.36倍と2.51倍の速度向上を達成しましたが、品質の低下は最小限に抑えられています。これは、リアルタイム生成においてより効率的な拡散トランスフォーマーへの実用的な一歩を示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Diffusion models (DMs) have become the state-of-the-art for generative tasks across domains, but their reliance on sequential forward passes limits real-time performance. Prior acceleration methods mainly reduce sampling steps or reuse intermediate results. Leveraging the flexibility of Diffusion Transformers (DiTs) to handle variable token counts, we propose RAS, a training-free sampling strategy that dynamically assigns different update ratios to image regions based on model focus. Our key observation is that at each step, DiTs concentrate on semantically meaningful areas, and these regions exhibit strong continuity across consecutive steps. Exploiting this, RAS updates only focused regions while reusing cached noise for others, with focus determined from the previous step’s output. Evaluated on Stable Diffusion 3 and Lumina-Next-T2I, RAS achieves up to 2.36× and 2.51× speedups, respectively, with minimal quality loss. This demonstrates a practical step toward more efficient diffusion transformers for real-time generation.
</details>

---

### Exploring Visual Pretraining for Learning Language Intelligence
著者: Zhonghan Zhao, Yiming Zhang, Wenwei Zhang, Haiteng Zhao, Xingguang Wei, Zhangwei Gao, Kuikun Liu, Yuzhe Gu, Size Wu, Haian Huang, Jianfei Gao, haijun Lv, Demin Song, Yunhua Zhou, Qipeng Guo, Gaoang Wang, Kai Chen

<details>
<summary> 日本語要旨 </summary>

最も基本的な事前学習パラダイムは通常、モダリティ固有のモデルをそれぞれのデータセットで訓練しますが、「表象が最終的にデータとモデルのスケールに応じて異なるモダリティ間で整合する」というプラトン的表象仮説は、興味深い可能性を示唆しています。つまり、大規模言語モデル（LLM）が視覚コーパスでの事前学習によってテキストで訓練されたモデルと同等の性能を達成し、テキストスケーリングのボトルネックを打破するためのデータソースを拡大し、より包括的なコーパス理解のために豊かな視覚的手がかりを活用できるということです。本論文は、この示唆の実現可能性を初めて示す試みとして、「マスク付き自己回帰事前学習による言語知能の学習（MAPLE）」というLLM向けの新しい視覚事前学習パラダイムを導入します。これは、原始的なドキュメント画像を利用して言語知能を向上させるものです。MAPLEは、マスク付き自己回帰モデルと様々なLLMバックボーンを統合するために普遍的であり、LLMsがマスクされた領域の仮説を生成するよう促します。これは、マスクされていない領域に基づいています。私たちは数学的推論のドメインでMAPLEを検証し、テキストのみの事前学習と比較して最大40.2％の平均精度向上を示す4つの数学的推論ベンチマークで一貫して優れていることを示します。さらなる分析では、視覚事前学習されたLLMsがドキュメントビジュアルとテキストを整合させ、レイアウトや構造的手がかりを活用する共有ラテンスペースを学ぶことを示し、これはより強力な言語モデルへの実現可能で拡張性のある道筋を支持しています。
</details>

<details>
<summary> 英語要旨 </summary>

While the most fundamental pretraining paradigm typically trains modality-specific models on their respective datasets, the Platonic Representation Hypothesis that representations eventually align across modalities as data and model scale suggests an intriguing possibility: large language models (LLMs) could be pretrained on visual corpora to reach parity with text-pretrained models, thereby expanding data sources to break the text-scaling bottlenecks, and leveraging richer visual cues for more comprehensive corpus understanding. This paper makes the first attempt to demonstrate the feasibility of this implication by introducing Masked Autoregressive Pretraining for Learning language intelligencE (MAPLE), a novel visual pretraining paradigm for LLMs that leverages raw document images to improve language intelligence. MAPLE is universal to integrate masked auto-regressive models with various LLM backbones, where the LLMs are incentivized to generate latent hypotheses for the masked regions based on the unmasked regions. We verify MAPLE in the domain of math reasoning with multiple LLM backbones and show that MAPLE consistently surpasses text-only pretraining relatively by at most 40.2\% on average accuracy across four math reasoning benchmarks. Further analyses show that visually pretrained LLMs learn a shared latent space that aligns document visuals with text and exploits layout and structural cues, supporting visual pretraining as a feasible and scalable route to stronger language models.
</details>

---

### CineScene: Implicit 3D As Effective Scene Representation for Cinematic Video Generation
著者: Kaiyi Huang, Yukun Huang, Yu Li, Jianhong Bai, Xintao Wang, Zinan Lin, Xuefei Ning, Jiwen Yu, Yu Wang, Xihui Liu

<details>
<summary> 日本語要旨 </summary>

映画のようなビデオ制作には、シーンと主題の構成やカメラの動きをコントロールする必要がありますが、実写撮影は物理的なセットを建設する必要があるため高価です。この問題に対処するために、私たちは分離されたシーンコンテキストを持つ映画のようなビデオ生成タスクを導入します：静的環境の複数の画像が与えられた場合、目標は動的な主題を特徴とする高品質なビデオをシーンの一貫性を保ちつつユーザー指定のカメラ軌道に従って生成することです。私たちは、暗黙的な3D認識シーン表現を活用した映画のようなビデオ生成フレームワークであるCineSceneを提示します。私たちの主要な革新は、3D認識機能を暗黙的に注入する新しいコンテキスト条件付けメカニズムです：シーン画像をVGGTを通じて視覚表現にエンコードした後、CineSceneは事前学習済みのテキストからビデオ生成モデルへ追加のコンテキスト連結を行い、空間的な優先順位を注入し、一貫したシーンと動的主題を持つカメラ制御ビデオ合成を可能にします。モデルの堅牢性をさらに向上させるために、トレーニング中の入力シーン画像に対する簡単で効果的なランダムシャッフリング戦略を導入します。トレーニングデータ不足に対処するため、私たちはUnreal Engine 5を使用して静的シーンを表すパノラマ画像とそのカメラ軌道を含む動的主題のあるなしでペアになったビデオを持つシーン分離データセットを構築します。実験結果は、CineSceneが大きなカメラ移動を処理し、多様な環境に一般化することでシーン一貫性のある映画のようなビデオ生成において最先端のパフォーマンスを達成していることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Cinematic video production requires control over scene-subject composition and camera movement, but live-action shooting remains costly due to the need for constructing physical sets. To address this, we introduce the task of cinematic video generation with decoupled scene context: given multiple images of a static environment, the goal is to synthesize high-quality videos featuring dynamic subject while preserving the underlying scene consistency and following a user-specified camera trajectory. We present CineScene, a framework that leverages implicit 3D-aware scene representation for cinematic video generation. Our key innovation is a novel context conditioning mechanism that injects 3D-aware features in an implicit way: By encoding scene images into visual representations through VGGT, CineScene injects spatial priors into a pretrained text-to-video generation model by additional context concatenation, enabling camera-controlled video synthesis with consistent scenes and dynamic subjects. To further enhance the model's robustness, we introduce a simple yet effective random-shuffling strategy for the input scene images during training. To address the lack of training data, we construct a scene-decoupled dataset with Unreal Engine 5, containing paired videos of scenes with and without dynamic subjects, panoramic images representing the underlying static scene, along with their camera trajectories. Experiments show that CineScene achieves state-of-the-art performance in scene-consistent cinematic video generation, handling large camera movements and demonstrating generalization across diverse environments.
</details>

---

### SO-Bench: A Structural Output Evaluation of Multimodal LLM
著者: Di Feng, Kaixin Ma, Feng Nan, Haofeng Chen, Bohan Zhai, David Griffiths, Mingfei Gao, Zhe Gan, Eshan Verma, Yinfei Yang, Zhifeng Chen, Afshin Dehghan

<details>
<summary> 日本語要旨 </summary>

多モーダル大規模言語モデル（MLLMs）は、出力が正確であるだけでなく、事前に定義されたデータスキーマに準拠する必要のある実世界のエージェント設定でますます展開されています。テキスト領域における構造化生成に関しては最近進歩が見られますが、視覚入力を基にしたスキーマに基づく情報抽出と推論を体系的に評価するベンチマークはまだ存在しません。本研究では、私たちが慎重に設計したSO-BENCHベンチマークを用いてMLLMsの視覚的な構造出力能力を包括的に調査します。UI画面、自然画像、文書、グラフという4つの視覚領域をカバーし、SO-BENCHは6,500以上の多様なJSONスキーマと1,800以上の人間によって品質が確認された画像–スキーマペアから構築されています。オープンソースおよび最先端のプロプライエタリモデルを対象としたベンチマーク実験では、正確でスキーマに準拠した出力を予測する際の持続的なギャップが明らかになり、より良い多様モーダル構造化推論の必要性が浮き彫りにされました。ベンチマークを超えて、私たちはさらにトレーニング実験を行い、モデルの構造出力能力を大幅に向上させました。このベンチマークをコミュニティと共有する計画です。
</details>

<details>
<summary> 英語要旨 </summary>

Multimodal large language models (MLLMs) are increasingly deployed in real-world, agentic settings where outputs must not only be correct, but also conform to pre-defined data schemas. Despite recent progress in structured generation in textual domain, there is still no benchmark that systematically evaluates schema-grounded information extraction and reasoning over visual inputs. In this work, we conduct a comprehensive study of visual structural output capabilities for MLLMs with our carefully designed SO-BENCH benchmark. Covering four visual domains, including UI screens, natural images, documents, and charts, SO-BENCH is built from over 6.5K diverse JSON schemas and 1.8K curated image–schema pairs with human-verified quality. Benchmarking experiments on open-sourced andfrontier proprietary models reveal persistent gaps in predicting accurate, schema compliant outputs, highlighting the need for better multimodal structured reasoning. Beyond benchmarking, we further conduct training experiments to largely improve the model’s structured output capability. We plan to make the benchmark available to the community.
</details>

---

### Mind The Gap: Transferring Labels to Align Object Detection Datasets
著者: Mikhail Kennerley, Angelica I Aviles-Rivero, Carola-Bibiane Schönlieb, Robby T. Tan

<details>
<summary> 日本語要旨 </summary>

複数の物体検出データセットを組み合わせることは、モデルの汎化性能向上への道筋を提供しますが、クラスの意味やバウンディングボックスアノテーションにおける不整合によって妨げられます。これらの問題に対処する方法は、共有されたラベル分類法を仮定し、空間的な不整合のみに対応するものや、手動での再ラベリングが必要となるもの、または固定されたターゲットラベルスペースに適さない統一ラベル空間を生成するものがあります。私たちは、多様なソースデータセットからのアノテーションをターゲットデータセットのラベルスペースに系統的に投影するラベル転送フレームワークであるLabel-Aligned Transfer（LAT）を提案します。LATは、まずソースデータセットごとに特化した検出器をトレーニングし、それらから生成されたプシュードラベルを地上真アノテーションと組み合わせることで開始します。この際、二段階の検出器における領域提案ネットワークをPrivileged Proposal Generator（PPG）が置き換えます。さらに、プシュードラベルのノイズを軽減し、領域特徴を洗練するために、Semantic Feature Fusion（SFF）モジュールが信頼度重み付きの注意メカニズムを用いてオーバーラップする提案からクラス意識のあるコンテキストと特徴を注入します。このパイプラインは、データセット固有のアノテーションの詳細性を保持しつつ、異種データセット間で多対一のラベルスペース転送を可能にし、下流検出器のトレーニングに適した意味的および空間的に整合された表現を生成します。LATはこのようにしてクラスレベルの不一致とバウンディングボックスの不整合の両方を、共有ラベルスペースや手動再アノテーションに依存せずに同時に解決します。複数のベンチマークでLATは検出性能の一貫した向上を示し、基準となる手法に対して最大+8.4 APの改善を達成しています。
</details>

<details>
<summary> 英語要旨 </summary>

Combining multiple object detection datasets offers a path to improved model generalisation but is hindered by inconsistencies in class semantics and bounding box annotations.cSome methods to address this assume shared label taxonomies and address only spatial inconsistencies; others require manual relabelling, or produce a unified label space, which may be unsuitable when a fixed target label space is required. We propose Label-Aligned Transfer (LAT), a label transfer framework that systematically projects annotations from diverse source datasets into the label space of a target dataset. LAT begins by training dataset-specific detectors to generate pseudo-labels, which are then combined with ground-truth annotations via a Privileged Proposal Generator (PPG) that replaces the region proposal network in two-stage detectors. To further refine region features and address pseudo-label noise, a Semantic Feature Fusion (SFF) module injects class-aware context and features from overlapping proposals using a confidence-weighted attention mechanism. This pipeline preserves dataset-specific annotation granularity while enabling many-to-one label space transfer across heterogeneous datasets, resulting in a semantically and spatially aligned representation suitable for training a downstream detector. LAT thus jointly addresses both class-level misalignments and bounding box inconsistencies without relying on shared label spaces or manual re-annotation. Across multiple benchmarks, LAT demonstrates consistent improvements in detection performance, achieving gains of up to +8.4 AP over baseline methods.
</details>

---

### EffectMaker: Unifying Reasoning and Generation for Customized Visual Effect Creation
著者: Shiyuan Yang, Ruihuang Li, Jiale Tao, Shuai Shao, qinglin lu, Jing Liao

<details>
<summary> 日本語要旨 </summary>

ビジュアルエフェクト（VFX）は、動画コンテンツの表現力と創造性を高めるために不可欠ですが、通常、専門知識と高額な制作パイプラインが必要です。既存のAIGCシステムは、効果固有のデータの希少性や超自然的またはスタイリッシュな効果をモデル化する固有の難しさにより、VFX生成において大きな課題に直面しています。さらに、これらのアプローチは通常、各効果ごとの微調整を必要とし、スケーラビリティや未知のVFXへの一般化能力が大幅に制限されます。本研究では、参照ベースのVFXカスタマイズを可能にする統合的な推論・生成フレームワークであるEffectMakerを提案します。EffectMakerは、高度な言語モデルを用いて効果の意味を解釈し、ターゲットとする対象への適応を考慮しながら推論を行います。また、Diffusion Transformerは参照動画から微細な視覚的手掛かりをインコンテキスト学習によって捉えます。これらの2つの要素は、効果ごとの微調整なしで正確で制御可能かつ効果一貫性のある合成を実現するための意味論的・視覚的デュアルパスガイダンスメカニズムを形成します。さらに、100,000本の動画と2,000種類のVFXカテゴリーを含む最大かつ高品質な合成データセットであるEffectDataを構築し、一般化能力とスケーラビリティを向上させます。実験結果は、EffectMakerが最先端のベースラインに比べて優れた視覚品質と効果一貫性を達成しており、カスタマイズされたVFX生成のためのスケーラブルで柔軟なパラダイムを提供することを示しています。コードとデータは受理後に公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Visual effects (VFX) are essential for enhancing the expressiveness and creativity of video content, yet producing high-quality effects typically requires expert knowledge and costly production pipelines. Existing AIGC systems face significant challenges in VFX generation due to the scarcity of effect-specific data and the inherent difficulty of modeling supernatural or stylized effects. Moreover, these approaches often require per-effect fine-tuning, which severely limits their scalability and generalization to novel VFX. In this work, we present EffectMaker, a unified reasoning–generation framework that enables reference-based VFX customization. EffectMaker employs a multimodal large language model to interpret high-level effect semantics and reason about their adaptation to a target subject, while a diffusion transformer leverages in-context learning to capture fine-grained visual cues from reference videos. These two components form a semantic–visual dual-path guidance mechanism that enables accurate, controllable, and effect-consistent synthesis without per-effect fine-tuning. Furthermore, we construct EffectData, a largest and high-quality synthetic dataset containing 100K videos across 2K VFX categories, to enhance generalization and scalability. Experiments show that EffectMaker achieves superior visual quality and effect consistency over state-of-the-art baselines, offering a scalable and flexible paradigm for customized VFX generation. Code and data will be released upon acceptance.
</details>

---

### ConsistCompose: Unified Multimodal Layout Control for Image Composition
著者: Xuanke Shi, Boxuan Li, Xiaoyang Han, Zhongang Cai, Lei Yang, Quan Wang, Dahua Lin

<details>
<summary> 日本語要旨 </summary>

視覚理解と画像生成を組み合わせた統一的なマルチモーダルモデルは急速に進化していますが、多くのシステムは依然として視覚的アンカリング（言語を画像領域に合わせること）に焦点を当てており、その生成対応であるレイアウト制御可能な多インスタンス生成のための言語埋め込みレイアウトグラウンデッドジェネレーション（LELG）は未だ十分に探求されておらず、正確な構成制御を限定しています。私たちは、レイアウト座標を直接言語プロンプトに埋め込むことで、単一の生成インターフェース内でレイアウト制御可能な多インスタンス画像生成を可能にする統一的マルチモーダルフレームワーク「ConsistCompose」を提案します。さらに、レイアウトと識別情報の注釈（2.6Mのテキストガイド付きおよび0.8Mの画像ガイド付きデータペア）を持つ3.4Mの多インスタンス生成用データセット「ConsistCompose3M」を構築し、レイアウト条件付きジェネレーションに対する大規模な監督を提供します。このフレームワーク内で、LELGはインスタンス-座標バインディングプロンプトと座標認識可能なクラシファイアーフリーガイダンスを通じて実現され、言語的レイアウト手がかりをタスク固有の枝分かれなしに正確な空間制御に変換します。COCO-PositionとMS-Benchでの実験では、ConsistComposeはレイアウト制御ベースラインを大幅に上回る空間精度を達成しつつ、識別忠実性を保持し競争力のある一般的なマルチモーダル理解を維持しており、レイアウト制御可能なマルチモーダル画像生成のための統一されたパラダイムを確立します。
</details>

<details>
<summary> 英語要旨 </summary>

Unified multimodal models that couple visual understanding with image generation have advanced rapidly, yet most systems still focus on visual grounding—aligning language with image regions—while their generative counterpart, linguistic-embedded layout-grounded generation(LELG) for layout-controllable multi-instance generation, remains underexplored and limits precise compositional control. We present ConsistCompose, a unified multimodal framework that embeds layout coordinates directly into language prompts, enabling layout-controlled multi-instance image generation from Interleaved Image-Text within a single generative interface. We further construct ConsistCompose3M, a 3.4M multi-instance generation dataset with layout and identity annotations (2.6M text-guided and 0.8M image-guided data pairs) that provides large-scale supervision for layout-conditioned generation. Within this framework, LELG is instantiated through instance–coordinate binding prompts and coordinate-aware classifier-free guidance, which translate linguistic layout cues into precise spatial control without task-specific branches. Experiments on COCO-Position and MS-Bench show that ConsistCompose substantially improves spatial accuracy over layout-controlled baselines while preserving identity fidelity and competitive general multimodal understanding, establishing a unified paradigm for layout-controllable multimodal image generation.
</details>

---

### CountGD++: Generalized Prompting for Open-World Counting
著者: Niki Amini-Naieni, Andrew Zisserman

<details>
<summary> 日本語要旨 </summary>

画像や動画内のオブジェクトを自動で数える方法の柔軟性と精度は、オブジェクトがどのように指定されるかに制限されています。既存の手法では、ユーザーがテキストや視覚的な例を用いて対象オブジェクトを説明できますが、視覚的な例は画像内で手動によってアノテーションされる必要があり、何を数えないかを指定する方法はありません。これらのギャップに対処するため、私たちはターゲットオブジェクトの指定方法を拡張する新しい機能を導入します。具体的には、何を数えないかをテキストや視覚的な例で説明できるようプロンプトを拡張し、「偽の代表例」を導入して推論時の視覚的な例のアノテーションを自動化し、カウントモデルを自然画像および合成外部画像からの視覚的な例を受け入れるように拡張します。また、新しいカウントモデルであるCountGD++をLLMのビジョン専門エージェントとして使用します。これらの貢献は、マルチモーダルなオープンワールドカウントのプロンプトの柔軟性を拡大し、複数のデータセットにわたる精度、効率、一般化能力の顕著な改善につながります。
</details>

<details>
<summary> 英語要旨 </summary>

The flexibility and accuracy of methods for automatically counting objects in images and videos are limited by the way the object can be specified. While existing methods allow users to describe the target object with text and visual examples, the visual examples must be manually annotated inside the image, and there is no way to specify what not to count. To address these gaps, we introduce novel capabilities that expand how the target object can be specified. Specifically, we extend the prompt to enable what not to count to be described with text and/or visual examples, introduce the concept of `pseudo-exemplars' that automate the annotation of visual examples at inference, and extend counting models to accept visual examples from both natural and synthetic external images. We also use our new counting model, CountGD++, as a vision expert agent for an LLM. Together, these contributions expand the prompt flexibility of multi-modal open-world counting and lead to significant improvements in accuracy, efficiency, and generalization across multiple datasets.
</details>

---

### CoMo: Learning Continuous Latent Motion from Internet Videos for Scalable Robot Learning
著者: Jiange Yang, tom tomlinson, Haoyi Zhu, Mingyu Liu, Kaijing Ma, Yating Wang, Gangshan Wu, Tong He, Limin Wang

<details>
<summary> 日本語要旨 </summary>

インターネット動画からの教師なし学習による潜在的な運動の把握は、汎用ロボットを開発する上で重要です。既存の離散法では、小さなコードブックサイズを使用したベクトル量子化によって、静的背景情報の過剰抽出に起因するショートカット学習問題を軽減しています。しかし、これらは情報損失が生じやすく、より複雑で細かいダイナミクスの捉えに苦労します。また、離散的な潜在運動と連続的なロボットアクションの分布間には本質的なギャップがあり、統一されたポリシーの共同学習を妨げています。私たちは、インターネットスケールの動画からより正確な連続的潜在運動を学習することを目指すCoMoを提案します。CoMoは、ショートカット学習の難易度を高めるために初期段階での時系列差分（Td）メカニズムを採用し、運動手がかりを明示的に強化します。また、連続的な潜在運動がより意味のある前景情報を捉えられるようにするため、時系列対比学習（Tcn）スキームも提案しています。具体的には、正のペアは小さな未来フレームの時間オフセットを持つ運動表現から構築され、負のペアは直接的に時系列方向を反転させて形成されます。提案されたTdとTcnは協調して働き、潜在運動が前景により集中し、運動手がかりを強化することを効果的に保証します。重要なことに、CoMoは強力なゼロショット一般化能力を示し、未見の動画に対して有効な仮想アクションラベルを生成することができます。また、ロボットアクションとビデオ潜在運動の共通連続分布も統一ポリシーの共同学習に大いに貢献します。広範なシミュレーションおよび実世界の実験では、CoMo仮想アクションラベルと共同でトレーニングされたポリシーが拡散型および自己回帰型アーキテクチャを用いても優れた性能を達成しています。
</details>

<details>
<summary> 英語要旨 </summary>

Unsupervised learning of latent motion from Internet videos is crucial for building generalist robots. Existing discrete methods generally mitigate the shortcut learning problem caused by extracting excessive static background information through vector quantization with a small codebook size. However, they suffer from information loss and struggle to capture more complex and fine-grained dynamics. Moreover, there is an inherent gap between the distribution of discrete latent motion and continuous robot action, which hinders the joint learning of a unified policy. We propose CoMo, which aims to learn more precise continuous latent motion from internet-scale videos. CoMo employs an early temporal difference (Td) mechanism to increase the difficulty of shortcut learning and explicitly enhance motion cues. Additionally, to ensure that continuous latent motion better captures meaningful foreground information, we further propose a temporal contrastive learning (Tcn) scheme. Specifically, positive pairs are constructed from motion representations with a small future frame temporal offset, while negative pairs are formed by directly reversing the temporal direction. The proposed Td and Tcn work synergistically and effectively ensure that the latent motion focuses better on the foreground and reinforces motion cues. Critically, CoMo exhibits strong zero-shot generalization, enabling it to generate effective pseudo action labels for unseen videos. The shared continuous distribution of robot action and video latent motion also significantly benefits the joint learning of unified policy. Extensive simulated and real-world experiments show that policies co-trained with CoMo pseudo action labels achieve superior performance with both diffusion and autoregressive architectures.
</details>

---

### Exploring Spatial Intelligence from A Generative Perspective
著者: Muzhi Zhu, Shunyao Jiang, Huanyi Zheng, Zekai Luo, Hao Zhong, Anzhou Li, Kaijun Wang, Jintao Rong, Yang Liu, Hao Chen, Tao Lin, Chunhua Shen

<details>
<summary> 日本語要旨 </summary>

多モーダル大規模言語モデルにおいて、空間知性は不可欠ですが、現在の評価基準は主に理解の側面からしか評価していません。現代の生成型または統合的な多モーダルモデルが、3D空間制約を尊重し操作しながら画像生成を行う能力である「生成型空間知性（GSI）」を持っているかどうか、またそのような能力が測定や改善され得るかどうかを問います。私たちは、空間に基づく画像編集を通じてGSIを量的に評価するための最初のベンチマークである「GSI-Bench」を導入します。これは2つの補完的なコンポーネントから構成されます：3D優先ガイド生成とフィルタリングパイプラインによって構築された高品質な実世界データセット「GSI-Real」と、制御可能な空間操作および完全自動ラベリングを備えた大規模合成ベンチマーク「GSI-Syn」です。統一された評価プロトコルと共に、GSI-Benchはスケーラブルでモデル非依存の空間遵守度および編集忠実性の評価を可能にします。実験結果は、統合的な多モーダルモデルをGSI-Synで微調整することが、合成タスクおよび実世界タスクの両方で顕著な向上をもたらし、驚くべきことに下流の空間理解能力も改善されることを示しています。これは生成型トレーニングが具体的に空間推論を強化できる初めての明確な証拠を提供し、多モーダルモデルにおける空間知性の進展への新たな道筋を築いています。
</details>

<details>
<summary> 英語要旨 </summary>

Spatial intelligence is essential for multimodal large language models, yet current benchmarks largely assess it only from an understanding perspective. We ask whether modern generative or unified multimodal models also possess generative spatial intelligence (GSI)—the ability to respect and manipulate 3D spatial constraints during image generation—and whether such capability can be measured or improved. We introduce GSI-Bench, the first benchmark designed to quantify GSI through spatially grounded image editing. It consists of two complementary components: GSI-Real, a high-quality real-world dataset built via a 3D-prior-guided generation and filtering pipeline, and GSI-Syn, a large-scale synthetic benchmark with controllable spatial operations and fully automated labeling. Together with a unified evaluation protocol, GSI-Bench enables scalable, model-agnostic assessment of spatial compliance and editing fidelity. Experiments show that fine-tuning unified multimodal models on GSI-Syn yields substantial gains on both synthetic and real tasks and, strikingly, also improves downstream spatial understanding. This provides the first clear evidence that generative training can tangibly strengthen spatial reasoning—establishing a new pathway for advancing spatial intelligence in multimodal models.
</details>

---

### Match-and-Fuse: Consistent Generation from Unstructured Image Sets
著者: Kate Feingold, Omri Kaduri, Tali Dekel

<details>
<summary> 日本語要旨 </summary>

私たちは、Match-and-Fuseを紹介します。これは、一貫した制御された生成が可能な無構造画像セットのゼロショートトレーニングフリー手法です。この方法では、共通の視覚要素を持ちつつも、視点、撮影時刻、周囲の内容が異なる画像コレクションを生成します。既存の方法は個々の画像や密にサンプリングされた動画で操作するのとは対照的に、私たちのフレームワークはセット間の生成を行います：ソースセットとユーザープロンプトが与えられると、共有コンテンツの横断的一貫性を保持した新しいセットを生成します。私たちの鍵となるアイデアは、このタスクをグラフとしてモデル化することであり、各ノードが画像に対応し、各エッジが画像ペアの共同生成をトリガーします。この形式では、すべてのペアごとの生成を統一されたフレームワークにまとめ、その局所的な一貫性を強制しつつ、全セットでのグローバルな一致を達成します。これは、マスクや手動監督を必要とせず、密な入力対応によってガイドされた画像ペア間の内部特徴の融合により実現されます。また、この方法はテキストから画像モデルで発生する傾向を利用し、複数のビューが単一のキャンバスを共有する際に一貫した生成を促進します。Match-and-Fuseは、一貫性と視覚品質で最先端を達成し、画像コレクションからのコンテンツ作成の新たな可能性を解き放ちます。
</details>

<details>
<summary> 英語要旨 </summary>

We present Match-and-Fuse - a zero-short, training-free method for consistent controlled generation of unstructured image sets -- collections that share a common visual element, yet differ in viewpoint, time of capture, and surrounding content. Unlike existing methods that operate on individual images or densely sampled videos, our framework performs set-to-set generation: given a source set and user prompts, it produces a new set that preserves cross-image consistency of shared content. Our key idea is to model the task as a graph, where each node corresponds to an image and each edge triggers a joint generation of image pairs. This formulation consolidates all pairwise generations into a unified framework, enforcing their local consistency while achieving global coherence across the entire set. This is achieved by fusing internal features across image pairs, guided by dense input correspondences, without requiring masks or manual supervision. This also allows us to leverage an emergent prior in text‑to‑image models that encourages coherent generation when multiple views share a single canvas. Match-and-Fuse achieves state-of-the-art consistency and visual quality, and unlocks new capabilities for content creation from image collections.
</details>

---

### Recovering Physically Plausible Human-Object Interactions from Monocular Videos
著者: Dingbang Huang, Etienne Vouga, Qixing Huang, Georgios Pavlakos

<details>
<summary> 日本語要旨 </summary>

この論文では、単眼動画から物理的に妥当な人間-オブジェクト相互作用（HOI）を再構築する方法を提案します。既存の運動学ベースのアプローチは視覚的に妥当な動きを生成できますが、物体の貫通や浮遊といった物理的な不整合が生じることがあります。これらの問題を克服するために、運動学推定から始まり、その後物理シミュレータで相互作用を再現する強化学習（RL）ポリシーによって精度を向上させる物理ガイド付きの再構築フレームワークを導入します。運動学推定は通常ノイズが多いため、単純なRLトレーニングでは失敗することがあります。そのため、最も情報量の高く信頼性のある運動学再構築フレームを自動的に特定する二重自己更新メカニズムを持つ適応サンプリング戦略を提案します。このプロセスは段階的に再構築の品質を向上させ、物理的に一貫したHOIシーケンスを生成します。私たちは2つの標準的なベンチマークでこのアプローチを示し、最先端手法と比較して物理的妥当性メトリックにおいて明確な改善を達成しました。
</details>

<details>
<summary> 英語要旨 </summary>

In this paper, we present a method to reconstruct physically plausible human-object interactions (HOI) from monocular videos. While existing kinematic-based approaches produce visually plausible motion, they often result in physical artifacts such as interpenetration and object floating. To overcome these issues, we introduce a physics-guided reconstruction framework that begins with a kinematic estimate and then refines it through a reinforcement learning (RL) policy trained to reproduce the interaction in a physics simulator. Because kinematic estimates are typically noisy, naive RL training can fail. Therefore, we propose an adaptive sampling strategy with a dual self-updating mechanism that automatically identifies the frames with the most informative and reliable kinematic reconstruction. Our process progressively improves reconstruction quality and yields physically consistent HOI sequences. We demonstrate our approach on two standard benchmarks and achieve clear improvements in physical plausibility metrics over state-of-the-art methods.
</details>

---

### StableMaterials: Enhancing Diversity in Material Generation Via Semi-Supervised Learning
著者: Giuseppe Vecchio

<details>
<summary> 日本語要旨 </summary>

私たちは、セミ・教師あり学習とラテントディファレンシャルモデル（LDMs）を統合した新しいアプローチである**StableMaterials**を紹介します。この方法は、既存の大規模画像生成モデルから知識を抽出するために敵対的学習を用い、注釈付きデータへの依存を最小限に抑えつつ生成の多様性を向上させます。この転移アプローチは、SDXLモデルからの画像テクスチャーの分布と生成された材料の分布を一致させることで、初期トレーニングデータセットに存在しない新しい材料の生成を可能にします。また、サンプルの視覚品質を向上させ高解像度の生成を実現するために、拡散ベースのリファイナーモデルを使用しています。最後に、わずか4ステップで迅速な生成が可能となるラテント一貫性モデルを転移し、通常は少ない拡散ステップで見られる視覚的アーティファクトを除去する新しいタイリング技術を提案します。StableMaterialsのアーキテクチャとトレーニングプロセス、既存のLDMフレームワーク内でのセミ・教師あり学習の統合について詳述します。最先端手法との比較評価では、StableMaterialsの有効性が示され、コンピュータグラフィックスをはじめとする様々な分野での応用可能性が強調されています。StableMaterialsは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

We introduce **StableMaterials**, a novel approach for generating photorealistic physical-based rendering (PBR) materials that integrate semi-supervised learning with Latent Diffusion Models (LDMs). Our method employs adversarial training to distill knowledge from existing large-scale image generation models, minimizing the reliance on annotated data and enhancing the diversity in generation. This distillation approach aligns the distribution of the generated materials with that of image textures from an SDXL model, enabling the generation of novel materials that are not present in the initial training dataset. Furthermore, we employ a diffusion-based refiner model to improve the visual quality of the samples and achieve high-resolution generation. Finally, we distill a latent consistency model for fast generation in just four steps and propose a new tileability technique that removes visual artifacts typically associated with fewer diffusion steps. We detail the architecture and training process of StableMaterials, the integration of semi-supervised training within existing LDM frameworks. Comparative evaluations with state-of-the-art methods show the effectiveness of StableMaterials, highlighting its potential applications in computer graphics and beyond. StableMaterials will be made publicly available.
</details>

---

### Confusion-Aware Spectral Regularizer for Long-Tailed Recognition
著者: Ziquan Zhu, Gaojie Jin, Hanruo Zhu, Si-Yuan Lu, Yunxiao Zhang, ZEYU FU, Ronghui Mu, Guoqiang Zhang, Zhao Sun, Xia Yuhang, Jiaxing Shang, Xiang Li, Lu Liu, Tianjin Huang

<details>
<summary> 日本語要旨 </summary>

長尾分類は、実際のデータが非常に不均衡な分布を持ち、少数のヘッドクラスが支配し多くのテールクラスが限られたサンプルしか含まないことから長年の課題であり続けています。この不均衡は特徴学習をヘッドカテゴリに偏らせ、希少クラスでの大幅な劣化を引き起こします。最近の研究では再サンプリング、再重み付け、分離学習戦略が提案されていますが、最も代表度の低いクラスにおける改善は全体的な精度と比較して依然として限定的です。本研究では、特に悪化したクラスの一般化を明示的に重視する混乱中心の観点から長尾認識に取り組みます。まず、クラス固有のエラー分析の新しい理論フレームワークを確立し、最悪クラスのエラーが周波数重み付けされた混乱行列のスペクトルノルムとモデル依存の複雑さ項によって狭く上限されることを示します。この洞察に基づき、訓練中に混乱行列のスペクトルノルムを最小化し、間クラスの混乱を減少させテールクラスの一般化を強化するConfusion-Aware Spectral Regularizer（CAR）を提案します。安定かつ効率的な最適化を可能にするため、CARは異分布行列の可微分代替とEMAベースの混乱推定器を組み込み、ミニバッチ間で滑らかで低変動な推定値を維持します。ImageNet-LT、CIFAR100-LT、iNaturalistデータセットにわたる複数の長尾基準における広範な実験は、CARが最悪クラス精度と全体的パフォーマンスを大幅に改善することを示しています。ConCutMix拡張と組み合わせると、CARはトレーニングからゼロ（$2.37\% \sim 4.83\%$）および事前学習からの微調整設定（$2.42\% \sim 4.17\%$）において、既存の最先端長尾学習手法を一貫して上回ります。
</details>

<details>
<summary> 英語要旨 </summary>

Long-tailed image classification remains a long-standing challenge, as real-world data typically follow highly imbalanced distributions where a few head classes dominate and many tail classes contain only limited samples. This imbalance biases feature learning toward head categories and leads to significant degradation on rare classes. Although recent studies have proposed re-sampling, re-weighting, and decoupled learning strategies, the improvement on the most underrepresented classes still remains marginal compared with overall accuracy. In this work, we present a confusion-centric perspective for long-tailed recognition that explicitly focuses on worst-class generalization. We first establish a new theoretical framework of class-specific error analysis, which shows that the worst-class error can be tightly upper-bounded by the spectral norm of the frequency-weighted confusion matrix and a model-dependent complexity term. Guided by this insight, we propose the Confusion-Aware Spectral Regularizer (CAR) that minimizes the spectral norm of the confusion matrix during training to reduce inter-class confusion and enhance tail-class generalization. To enable stable and efficient optimization, CAR integrates a Differentiable Confusion Matrix Surrogate and an EMA-based Confusion Estimator to maintain smooth and low-variance estimates across mini-batches. Extensive experiments across multiple long-tailed benchmarks demonstrates that CAR substantially improves both worst-class accuracy and overall performance. When combined with ConCutMix augmentation, CAR consistently surpasses exisiting state-of-the-art long-tailed learning methods under both the training-from-scratch setting (by $2.37\% \sim 4.83\%$) and the fine-tuning-from-pretrained setting (by $2.42\% \sim 4.17\%$) across ImageNet-LT, CIFAR100-LT, and iNaturalist datasets.
</details>

---

### VideoFusion: A Spatio-Temporal Collaborative Network for Multi-modal Video Fusion
著者: Linfeng Tang, Yeda Wang, Meiqi Gong, Zizhuo Li, Yuxin Deng, Xunpeng Yi, Chunyu Li, Han Xu, HAO ZHANG, Jiayi Ma

<details>
<summary> 日本語要旨 </summary>

ビデオは実際の取得シナリオにより適合し、貴重な時間的手がかりを持っています。しかし、既存のマルチセンサーフュージョン研究は主に複数の画像から補完的なコンテキストを統合することに焦点を当てており、ビデオではありません。これは主に2つの理由によるものです：1) 大規模なマルチセンサービデオデータセットが不足しているため、ビデオフュージョン研究が制限されており、2) 空間的および時間的依存関係を統一した枠組みで同時にモデル化することの固有の難しさです。本論文はこれらのジレンマに対して積極的に補償します。まず、我々はM3SVDを構築しました。これは220の時間的に同期された空間的に登録された赤外線可視ビデオからなるベンチマークデータセットで、153,797フレームを含み、ビデオフュージョンコミュニティのデータギャップを埋めています。次に、VideoFusionという多モーダルビデオフュージョンモデルを提案します。これはクロスモーダル補完性と時間的ダイナミクスを最大限に活用して、マルチモーダル入力から空間的および時間的に一貫したビデオを生成します。具体的には、1) クロスモーダル情報の相互作用と強化のための差分強化モジュールが開発され、2) 完全なモダリティガイド付きフュージョン戦略が適応的にマルチモーダル特徴を統合するために使用され、3) バイタイムラル共注意メカニズムが前後の時間的コンテキストを動的に集約してクロスフレーム特徴表現を強化します。広範な実験は、VideoFusionが画像指向のフュージョンパラダイムよりもシーケンスで優れており、効果的に時間的不整合と干渉を軽減することを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Compared to images, videos better align with real-world acquisition scenarios and possess valuable temporal cues. However, existing multi-sensor fusion research predominantly integrates complementary context from multiple images rather than videos. This primarily stems from two factors: 1) the scarcity of large-scale multi-sensor video datasets, limiting research in video fusion, and 2) the inherent difficulty of jointly modeling spatial and temporal dependencies in a unified framework. This paper proactively compensates for the dilemmas. First, we construct M3SVD, a benchmark dataset with 220 temporally synchronized and spatially registered infrared-visible videos comprising 153,797 frames, filling the data gap for the video fusion community. Secondly, we propose VideoFusion, a multi-modal video fusion model that fully exploits cross-modal complementarity and temporal dynamics to generate spatio-temporally coherent videos from multi-modal inputs. Specifically, 1) a differential reinforcement module is developed for cross-modal information interaction and enhancement, 2) a complete modality-guided fusion strategy is employed to adaptively integrate multi-modal features, and 3) a bi-temporal co-attention mechanism is devised to dynamically aggregate forward-backward temporal contexts to reinforce cross-frame feature representations. Extensive experiments reveal that VideoFusion outperforms existing image-oriented fusion paradigms in sequences, effectively mitigating temporal inconsistency and interference.
</details>

---

### AnchorFlow: Training-Free 3D Editing Via Latent Anchor-Aligned Flows
著者: Zhenglin Zhou, Fan Ma, Chengzhuo Gui, Xiaobo Xia, Hehe Fan, Yi Yang, Tat-seng Chua

<details>
<summary> 日本語要旨 </summary>

モデルの微調整を行わずに、人間の指示に基づいて3D形状を変更することを目的としたトレーニングフリーな3Dエディティングは、3Dコンテンツ作成において重要な役割を果たします。しかし、既存のアプローチでは、しばしば強力で幾何学的に安定した編集が難しいという問題があります。これは主に、拡散サンプリング中のタイムステップ依存性ノイズによって導入される不一致な潜在的アンカーに起因しています。この制限を克服するため、我々は潜在的アンカーの一貫性という原則に基づいてAnchorFlowを導入します。具体的には、AnchorFlowはソースおよびターゲットトラジェクトリ間で共有されるグローバルな潜在的アンカーを確立し、緩和されたアンカー整列損失とアンカーに沿った更新規則を用いて一貫性を強制します。この設計により、エディティングプロセス全体で変換が安定し、意味的に忠実であることが保証されます。潜在的参照空間を安定化することで、AnchorFlowはより顕著なセマンティック変更を可能にします。さらに、AnchorFlowはマスクフリーです。マスクの監督がない中でも、幾何学的忠実性を効果的に保持します。Eval3DEditベンチマークでの実験結果では、AnchorFlowは多様な編集タイプにわたって意味的に整合し、構造的に頑健な編集を一貫して提供することが示されました。コードおよびモデルは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Training-free 3D editing aims to modify 3D shapes based on human instructions without model finetuning. It plays a crucial role in 3D content creation. However, existing approaches often struggle to produce strong or geometrically stable edits, largely due to inconsistent latent anchors introduced by timestep-dependent noise during diffusion sampling. To address these limitations, we introduce AnchorFlow, which is built upon the principle of latent anchor consistency. Specifically, AnchorFlow establishes a global latent anchor shared between the source and target trajectories, and enforces coherence using a relaxed anchor-alignment loss together with an anchor-aligned update rule. This design ensures that transformations remain stable and semantically faithful throughout the editing process. By stabilizing the latent reference space, AnchorFlow enables more pronounced semantic modifications. Moreover, AnchorFlow is mask-free. Without mask supervision, it effectively preserves geometric fidelity. Experiments on the Eval3DEdit benchmark show that AnchorFlow consistently delivers semantically aligned and structurally robust edits across diverse editing types. The code and models will be made publicly available.
</details>

---

### Large-scale Codec Avatars: The Unreasonable Effectiveness of Large-scale Avatar Pretraining
著者: Junxuan Li, Rawal Khirodkar, Egor Zakharov, Jihyun Lee, Zhaoen Su, Yuan Dong, Julieta Martinez, Kai Li, Qingyang Tan, Takaaki Shiratori, Matthew Hu, Peihong Guo, Xuhua Huang, Zhongshi Jiang, LINGCHEN YANG, Ariyan Zarei, Marco Pesavento, Yichen Xu, Chengan He, He Wen, Giljoo Nam, Teng Deng, Wyatt Borsos, Anjali Thakrar, Jean-Charles Bazin, Rinat Abdrashitov, Carsten Stoll, Ginés Hidalgo, James Booth, Lucy Wang, Xiaowen Ma, Yu Rong, Sairanjith Thalanki, Chen Cao, Christian Häne, Abhishek Kar, Sofien Bouaziz, Jason Saragih, Yaser Sheikh, Shunsuke Saito

<details>
<summary> 日本語要旨 </summary>

高品質な3Dアバターモデリングは、忠実度と汎用性の間で重要なトレードオフに直面しています。一方で、マルチビュースタジオデータを使用することで、表情やポーズの精密制御が可能な人物モデリングは高忠実度ですが、スケールの限界とスタジオ環境と現実世界とのドメインギャップにより、現実的なデータへの汎用性は制約されます。他方で、最近の大規模アバターモデルは数百万の野外サンプルを使用してトレーニングされ、広範囲の身元に対する汎用性が期待されていますが、結果として得られるアバターは3Dの不確定性により低品質です。これを解決するために、私たちはLarge-Scale Codec Avatars（LCA）を提案します。これは、世界規模の人口に対してフィードフォワード方式で一般化可能な高忠実度かつ全身3Dアバターモデルであり、効率的な推論を可能にします。大言語モデルやビジョン基礎モデルの成功に触発され、初めてスケールでの3Dアバターモデリングに対するプレ/ポストトレーニングパラダイムを提示します：1Mの野外動画で事前学習し、外観と幾何学に関する広範な優先順位を学び、その後高品質なキュレーションデータでポストトレーニングして表現力と忠実度を向上させます。LCAは髪型、服装、人口統計にわたって一般化し、細部まで精密な顔の表情制御や指レベルの可動制御を提供しつつ、強いアイデンティティ保持性を維持します。特に、リライト可能性と制約されていない入力へのゆるやかな衣服サポートへの出現一般化、およびスタイル化された画像に対するゼロショットでの堅牢性を観察していますが、これは直接的な監督が存在しない状況です。
</details>

<details>
<summary> 英語要旨 </summary>

High-quality 3D avatar modeling faces a critical trade-off between fidelity and generalization. On the one hand, multi-view studio data enables high-fidelity modeling of humans with precise control over expressions and poses, but it struggles to generalize to real-world data due to limited scale and the domain gap between the studio environment and the real world. On the other hand, recent large-scale avatar models trained on millions of in-the-wild samples show promise for generalization across a wide range of identities, yet the resulting avatars are often of low-quality due to inherent 3D ambiguities. To address this, we present Large-Scale Codec Avatars (LCA), a high-fidelity, full-body 3D avatar model that generalizes to world-scale populations in a feedforward manner, enabling efficient inference. Inspired by the success of large language models and vision foundation models, we present, for the first time, a pre/post-training paradigm for 3D avatar modeling at scale: we pretrain on 1M in-the-wild videos to learn broad priors over appearance and geometry, then post-train on high-quality curated data to enhance expressivity and fidelity. LCA generalizes across hair styles, clothing, and demographics while providing precise, fine-grained facial expressions and finger-level articulation control, with strong identity preservation. Notably, we observe emergent generalization to relightability and loose garment support to unconstrained inputs, and zero-shot robustness to stylized imagery, despite the absence of direct supervision.
</details>

---

### Streaming Video Instruction Tuning
著者: Jiaer Xia, Peixian Chen, Mengdan Zhang, Xing Sun, Kaiyang Zhou

<details>
<summary> 日本語要旨 </summary>

私たちは、一般的な対話型アシスタントとして機能するリアルタイムストリーミングビデオLLMであるStreamoを紹介します。既存のオンラインビデオモデルが質問応答やキャプショニングに限定されているのとは異なり、Streamoはリアルタイムナレーション、アクション理解、イベントキャプショニング、時間的イベントグラウンディング、時制に敏感な質問応答を含むストリーミングビデオタスクの広範囲にわたるパフォーマンスを行います。このような多様性を実現するため、私たちはストリーミングビデオ理解に特化した大規模な指示従属型データセットであるStreamo-Instruct-465Kを構築しました。このデータセットは多様な時間的コンテキストとマルチタスクの監督をカバーしており、異種ストリーミングタスクにわたる統一トレーニングを可能にします。指示従属型データセットでエンドツーエンドにトレーニングした後、Streamoは効率的なパイプラインを通じて強力な時間的推論能力、応答性の高い対話機能、さまざまなストリーミングベンチマークにわたる広範な一般化能力を示します。包括的な実験結果は、Streamoがオフラインビデオ認識モデルとリアルタイムマルチモーダルアシスタントの間にギャップを埋め、連続的なビデオストリームでの統一された知能あるビデオ理解への一歩を示しています。
</details>

<details>
<summary> 英語要旨 </summary>

We present Streamo, a real-time streaming video LLM that serves as a general-purpose interactive assistant. Unlike existing online video models that focus narrowly on question answering or captioning, Streamo performs a broad spectrum of streaming video tasks, including real-time narration, action understanding, event captioning, temporal event grounding, and time-sensitive question answering. To develop such versatility, we construct Streamo-Instruct-465K, a large-scale instruction-following dataset tailored for streaming video understanding. The dataset covers diverse temporal contexts and multi-task supervision, enabling unified training across heterogeneous streaming tasks. After training end-to-end on the instruction-following dataset through a streamlined pipeline, Streamo exhibits strong temporal reasoning, responsive interaction, and broad generalization across a variety of streaming benchmarks. Extensive experiments show that Streamo bridges the gap between offline video perception models and real-time multimodal assistants, making a step toward unified, intelligent video understanding in continuous video streams.
</details>

---

### The Image As Its Own Reward: Reinforcement Learning with Adversarial Reward for Image Generation
著者: Weijia Mao, Hao Chen, Zhenheng Yang, Mike Zheng Shou

<details>
<summary> 日本語要旨 </summary>

画像生成における強化学習（RL）では、信頼性の高い報酬関数が不可欠です。現在の多くのRLアプローチは、人間の好みを近似するためにスカラー報酬を出力する事前学習済みの嗜好モデルに依存しています。しかし、これらの報酬はしばしば人間の知覚を捉えることができず、報酬ハッキングに対して脆弱です。つまり、高いスコアが必ずしも良質な画像を意味しないのです。これに対処するために、我々は**Adv-GRPO**というRLフレームワークを導入します。このフレームワークでは、報酬モデルと生成器が反復的に更新される敵対的な報酬を使用しています。報酬モデルは参照画像を正のサンプルとして用いて監督学習され、大幅にハッキングから逃れることができます。KL正則化がパラメータ更新を制約するのとは異なり、我々の学習した報酬はその視覚的出力を通じて直接生成器を導くため、画質の高い画像が得られます。また、既存の報酬関数を最適化することで報酬ハッキングを軽減できるものの、その固有のバイアスは残ります。例えば、PickScoreは画像品質を低下させる可能性があり、OCRに基づく報酬は美的忠実度を減少させることが多いです。これに対処するために、我々は**画像自体を報酬として取り入れます**。参照画像やビジョンファウンデーションモデル（例えばDINO）を用いて豊かな視覚的報酬を提供します。これらの密な視覚信号は単一のスカラーではなく、画質、美学、タスク固有のメトリックにわたって一貫した向上をもたらします。最後に、参照サンプルとファウンデーションモデル報酬を組み合わせることで分布転送と柔軟なスタイルカスタマイズが可能になります。人間評価では、我々の方法はFlow-GRPOやSD3を上回り、画質および美学でそれぞれ70.0%と72.4%の勝率を達成しました。コードとモデルは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

A reliable reward function is essential for reinforcement learning (RL) in image generation. Most current RL approaches depend on pre-trained preference models that output scalar rewards to approximate human preferences. However, these rewards often fail to capture human perception and are vulnerable to reward hacking, where higher scores do not correspond to better images. To address this, we introduce **Adv-GRPO**, an RL framework with an adversarial reward that iteratively updates both the reward model and the generator. The reward model is supervised using reference images as positive samples and can largely avoid being hacked. Unlike KL regularization that constrains parameter updates, our learned reward directly guides the generator through its visual outputs, leading to higher-quality images. Moreover, while optimizing existing reward functions can alleviate reward hacking, their inherent biases remain. For instance, PickScore may degrade image quality, whereas OCR-based rewards often reduce aesthetic fidelity. To address this, we take **the image itself as a reward**, using reference images and vision foundation models (e.g., DINO) to provide rich visual rewards. These dense visual signals, instead of a single scalar, lead to consistent gains across image quality, aesthetics, and task-specific metrics. Finally, we show that combining reference samples with foundation-model rewards enables distribution transfer and flexible style customization. In human evaluation, our method outperforms Flow-GRPO and SD3, achieving 70.0% and 72.4% win rates in image quality and aesthetics, respectively. Code and models will be released.
</details>

---

### Cubic Discrete Diffusion: Discrete Visual Generation on High-Dimensional Representation Tokens
著者: Yuqing Wang, Chuofan Ma, Zhijie Lin, Yao Teng, Lijun Yu, Shuai Wang, Jiaming Han, Jiashi Feng, Yi Jiang, Xihui Liu

<details>
<summary> 日本語要旨 </summary>

視覚生成における離散トークンの使用は、言語モデルと共有される統一的なトークン予測パラダイムを可能にし、シームレスなマルチモーダルアーキテクチャを約束するため、大きな注目を集めています。しかし、現在の離散生成手法は通常8〜32次元の低次元VAEトークンに限定されており、理解に不可欠な意味的豊かさを犠牲にしています。高次元事前学習表現（768〜1024次元）はこのギャップを埋める可能性がありますが、その離散生成は基本的な課題を抱えています。本論文では、高次元表現のための初めての離散生成モデルであるCubic Discrete Diffusion（CubiD）を提案します。空間位置を原子的に扱うのではなく、CubiDは高次元離散表現全体で細かいマスキングを行います—任意の次元および位置が部分観測からマスクされ予測可能です。これにより、モデルは注意機構を通じて空間内外での豊かな相関を学習することができ、$O(hwd)$ の非効率的な順次生成問題を $T \ll hwd$ における $O(T)$ の並列反復へと変換します。ImageNet-256では、CubiDは900Mから3.7Bパラメータまでの強力なスケーリング挙動を示し、離散生成において最先端の成果を達成しています。重要なことに、これらの離散化されたトークンが元の表現能力を保持することを検証し、同じ離散トークンが理解および生成タスクの両方で効果的に使用可能であることを示しています。この研究が統一マルチモーダルアーキテクチャに向けた将来の研究へのインスピレーションとなることを願っています。
</details>

<details>
<summary> 英語要旨 </summary>

Visual generation with discrete tokens has gained significant attention as it enables a unified token prediction paradigm shared with language models, promising seamless multimodal architectures. However, current discrete generation methods remain limited to low-dimensional VAE tokens (typically 8-32 dims), sacrificing the semantic richness essential for understanding. While high-dimensional pretrained representations (768-1024 dims) could bridge this gap, their discrete generation poses fundamental challenges. In this paper, we present Cubic Discrete Diffusion (CubiD), the first discrete generation model for high-dimensional representations. Instead of treating spatial positions atomically, CubiD performs fine-grained masking throughout the high-dimensional discrete representation—any dimension at any position can be masked and predicted from partial observations. This enables the model to learn rich correlations both within and across spatial positions through attention, transforming an intractable $O(hwd)$ sequential generation problem into $O(T)$ parallel iterations where $T \ll hwd$. On ImageNet-256, CubiD achieves state-of-the-art discrete generation with strong scaling behavior from 900M to 3.7B parameters. Crucially, we validate that these discretized tokens preserve original representation capabilities, demonstrating that the same discrete tokens can effectively serve both understanding and generation tasks. We hope this work will inspire future research toward unified multimodal architectures.
</details>

---

### MoEActok: A MoE-based Action Tokenizer for Vision-Language-Action Models
著者: Chunpu Xu, Zhixuan Liang, Tianshuo Yang, Chi-Min Chan, Yang Xiao, Jessie Wang, Xiaokang Yang, Yao Mu

<details>
<summary> 日本語要旨 </summary>

最近の視覚言語行動（VLA）モデルに関する研究は、連続制御信号を離散トークンに変換し、LLM/VLMのトレーニングパラダイムと整合させるアクショントークナイザーの探索で大きな進歩を遂げています。これらの手法は通常、複数の異なるスキルが含まれる全体の操作経路に対して単一のトークナイザーを訓練し、そのため難解な最適化のトレードオフを引き起こします。この問題に対処するために、私たちはスキル認識型の離散表現をVLAモデルに生成するために混合専門家（MoE）量子化器を用いる新しいアクショントークナイザー、MoEActokを提案します。MoEActokは、各専門家が特定のスキルに特化するクラスタリング駆動型のMoE VQ-VAEメカニズムを使用しています。主要なコンポーネントとしては：(a) k-meansクラスタリングを用いたアクション・スキル分離戦略で、類似したスキルを持つクラスターを整列させることによりアクションチャンクをグループ化する；(b) スキル条件付きコンテキストをVLAモデルに補完し、スキルの根拠を改善するスキル認識型トレーニングパラダイム；および(c) 共有エンコーダー表現を専門化された量子化用のスキル特異的な潜在空間に投影し、その後多様な量子化された表現を共通の空間に調和させて共有デコーダーによる一貫した再構成が可能とするアダプターです。私たちはMoEActokベースのVLAモデルをRoboTwinおよびSimpler-Envシミュレータで複数の既存のアクショントークナイザーベースラインと比較し、さらに3つの実世界タスクでゼロショットトランスファを評価します。シミュレートされた環境および実世界の設定の両方において、MoEActokベースのVLAは既存の離散トークン化手法を大きく上回ります。
</details>

<details>
<summary> 英語要旨 </summary>

Recent works on vision-language-action (VLA) models have made great progress in exploring action tokenizers that convert continuous control signals into discrete tokens to align with LLM/VLM training paradigms. These approaches typically train a single tokenizer over entire manipulation trajectories, which often comprise multiple distinct skills and thus pose a challenging optimization trade-off. To address this issue, we introduce MoEActok, a novel action tokenizer that employs a mixture-of-experts (MoE) quantizer to produce skill-aware discrete representations for VLA models. MoEActok utilizes a clustering-driven MoE VQ-VAE mechanism in which each expert specializes in a particular skill. The key components are: (a) an action-skill decoupling strategy that uses k-means clustering to group action chunks, aligning clusters having similar skills; (b) a skill-aware training paradigm that augments VLA models with skill-conditioned context, improving skill grounding; and (c) an adapter that projects shared encoder representations into skill-specific latent spaces for specialized quantization, and subsequently harmonize the heterogeneous quantized representations back into a unified space for coherent reconstruction by the shared decoder. We evaluate MoEActok-based VLA models against multiple prior action tokenizer baselines in the RoboTwin and Simpler-Env simulators, and further assess zero-shot transfer on three real-world tasks. Across both simulated and real-world settings, MoEActok-based VLA substantially outperforms existing discrete tokenization methods.
</details>

---

### Unified Camera Positional Encoding for Controlled Video Generation
著者: Cheng Zhang, Boying Li, Meng Wei, Yan-Pei Cao, Camilo Cruz Gambardella, Dinh Phung, Jianfei Cai

<details>
<summary> 日本語要旨 </summary>

トランスフォーマーは、自動運転やエンボディAIの世界モデルにおける3次元認識、ビデオ生成、そしてカメラ幾何学を理解することが重要な分野で普遍的なバックボーンとして台頭しています。しかし、既存のカメラエンコーディング方法はしばしば単純化されたピンホール仮定に依存し、実際のカメラで見られる多様な内部パラメータやレンズ歪みに対する汎用性を制限しています。私たちは**相対的光線エンコーディング**という幾何学的一貫性のある表現を導入し、6自由度の姿勢、内部パラメータ、レンズ歪みを含む完全なカメラ情報を統合します。その能力を多様な制御要求下で評価するために、テキストからビデオ生成のカメラ制御をテストベッドタスクとして採用しました。この設定では、ピッチとロールを**絶対方向エンコーディング**で効果的な2つの要素として特定し、初期カメラ姿勢の完全制御を可能にします。これらの設計は**UCPE（統一カメラ位置エンコーディング）**を形成し、トレーニング可能なパラメータが1%未満である軽量空間注意アダプターを介して事前学習済みのビデオDiffusionトランスフォーマーに統合され、最先端のカメラ制御性と視覚的忠実度が達成されます。多様なカメラ動作やレンズタイプを網羅する大規模ビデオデータセットを構築し、体系的なトレーニングと評価を容易にします。広範囲の実験はUCPEがカメラ制御可能なビデオ生成での効果を確認し、将来のマルチビュー、ビデオ、3Dタスクにおけるトランスフォーマーの一般的なカメラ表現としての潜在性を浮き彫りにします。
</details>

<details>
<summary> 英語要旨 </summary>

Transformers have emerged as a universal backbone across 3D perception, video generation, and world models for autonomous driving and embodied AI, where understanding camera geometry is essential for grounding visual observations in three-dimensional space. However, existing camera encoding methods often rely on simplified pinhole assumptions, restricting generalization across the diverse intrinsics and lens distortions in real-world cameras. We introduce **Relative Ray Encoding**, a geometry-consistent representation that unifies complete camera information, including 6-DoF poses, intrinsics, and lens distortions. To evaluate its capability under diverse controllability demands, we adopt camera-controlled text-to-video generation as a testbed task. Within this setting, we further identify pitch and roll as two components effective for **Absolute Orientation Encoding**, enabling full control over the initial camera orientation. Together, these designs form **UCPE (Unified Camera Positional Encoding)**, which integrates into a pretrained video Diffusion Transformer through a lightweight spatial attention adapter, adding **less than 1% trainable parameters** while achieving state-of-the-art camera controllability and visual fidelity. To facilitate systematic training and evaluation, we construct a large video dataset covering a wide range of camera motions and lens types. Extensive experiments validate the effectiveness of UCPE in camera-controllable video generation and highlight its potential as a general camera representation for Transformers across future multi-view, video, and 3D tasks.
</details>

---

### Think Visually, Reason Textually: Vision-Language Synergy in Abstract Reasoning
著者: Beichen Zhang, Yuhang Zang, Xiaoyi Dong, Yuhang Cao, Haodong Duan, Dahua Lin, Jiaqi Wang

<details>
<summary> 日本語要旨 </summary>

最小限の例からの抽象的推論は、GPT-5やGrok 4などの先進的な基盤モデルにとって未解決の重要な問題であり続けています。これらのモデルは依然として構造化された変換規則を少数の例から推測することができず、人間の知能の重要な特徴です。人工一般知能（AGI）用の抽象化および推論コーパス（ARC-AGI）は、この能力を厳密に評価するためのテストベッドを提供し、概念的な規則誘導と新しいタスクへの転移を要求します。既存の多くの方法はARC-AGIを純粋にテキスト推論のタスクとして扱っており、人間がこのようなパズルを解決する際に視覚的抽象化に大きく依存していることを見落としています。しかし、私たちのパイロット実験は矛盾を明らかにしました：ARC-AGIグリッドを単純に画像としてレンダリングすると、規則の実行が不正確であるためパフォーマンスが低下します。これにより、私たちの中心的な仮説が生まれました：視覚と言語は異なる推論段階で補完的な強みを持っています：視覚は全体的なパターン抽象化と検証をサポートし、一方で言語は記号的なルールの形成と正確な実行に特化しています。この洞察に基づき、私たちは2つの協力戦略を導入します：（1）視覚-言語シナジー推論（VLSR）、これはARC-AGIをモダリティに合わせたサブタスクに分解するものであり；（2）モダリティ切り替え自己訂正（MSSC）、これは視覚を用いてテキストベースの推論を検証し、内在的なエラー修正を行います。広範囲にわたる実験では、私たちのアプローチが多様なフラッグシップモデルと複数のARC-AGIタスクでテキストのみの基準値を最大4.33％上回ることを示しています。私たちの発見は、視覚的抽象化と言語的推論を統合することが、将来の基盤モデルにおける一般化可能で人間らしい知能を達成するための重要なステップであることを示唆しています。
</details>

<details>
<summary> 英語要旨 </summary>

Abstract reasoning from minimal examples remains a core unsolved problem for frontier foundation models such as GPT-5 and Grok 4. These models still fail to infer structured transformation rules from a handful of examples, which is a key hallmark of human intelligence. The Abstraction and Reasoning Corpus for Artificial General Intelligence (ARC-AGI) provides a rigorous testbed for this capability, demanding conceptual rule induction and transfer to novel tasks. Most existing methods treat ARC-AGI as a purely textual reasoning task, overlooking the fact that humans rely heavily on visual abstraction when solving such puzzles. However, our pilot experiments reveal a paradox: naively rendering ARC-AGI grids as images degrades performance due to imprecise rule execution. This leads to our central hypothesis that vision and language possess complementary strengths across distinct reasoning stages:vision supports global pattern abstraction and verification, whereas language specializes in symbolic rule formulation and precise execution. Building on this insight, we introduce two synergistic strategies:(1) Vision-Language Synergy Reasoning (VLSR), which decomposes ARC-AGI into modality-aligned subtasks; and(2) Modality-Switch Self-Correction (MSSC), which leverages vision to verify text-based reasoning for intrinsic error correction. Extensive experiments demonstrate that our approach yields up to a 4.33\% improvement over text-only baselines across diverse flagship models and multiple ARC-AGI tasks. Our findings suggest that unifying visual abstraction with linguistic reasoning is a crucial step toward achieving generalizable, human-like intelligence in future foundation models.
</details>

---

### WarpTracker: Tracking By Warping Instead of Correlation
著者: Zihang Lai, Eldar Insafutdinov, Edgar Sucar, Andrea Vedaldi

<details>
<summary> 日本語要旨 </summary>

コンピュータビジョンにおける密な点追跡は基本的な問題であり、動画解析からロボット操作まで幅広い応用がある。最先端のトラッカーは通常、フレーム間で特徴をマッチングするためにコスト体積を利用しているが、このアプローチは空間分解能に対して二次的な複雑性を伴うため、スケーラビリティと効率が制限されてしまう。本稿では、コスト体積の代わりにワーピングを利用する新しい密な点トラッカーであるWarpTrackerを提案する。最近の光流推定技術の進歩に触発された当アプローチは、現在の推定値に基づきターゲットフレームからクエリフレームへ特徴をワープすることで、トラック推定を反復的に洗練していく。さらに、すべてのトラックに対して共同スペース時間的推論を行うトランスフォーマーアーキテクチャと組み合わせることで、特徴相関計算なしに長距離対応を確立している。我々の設計はシンプルであり、標準的な密な点追跡ベンチマーク（TAP-Vid-DAVIS, TAP-Vid-Kinetics, Robo-TAP）において最先端の性能を達成している。驚くべきことに、このモデルは光流推定でも優れた結果を示し、Sintel, KITTI, Springベンチマークでは専門的な方法を時に上回っている。これらの結果から、ワーピングベースのアーキテクチャが密な点追跡と光流推定を統一する可能性を示唆している。
</details>

<details>
<summary> 英語要旨 </summary>

Dense point tracking is a fundamental problem in computer vision, with applications ranging from video analysis to robotic manipulation. State-of-the-art trackers typically rely on cost volumes to match features across frames, but this approach incurs quadratic complexity in spatial resolution, limiting its scalability and efficiency. In this paper, we propose WarpTracker, a novel dense point tracker that eschews cost volumes in favor of warping. Inspired by recent advances in optical flow, our approach iteratively refines track estimates by warping features from the target frame to the query frame based on the current estimate. Combined with a transformer architecture that performs joint spatiotemporal reasoning across all tracks, our design established long-range correspondences without computing feature correlation. Our model is simple and achieves state-of-the-art performance on standard dense point tracking benchmarks, including TAP-Vid-DAVIS, TAP-Vid-Kinetics, and Robo-TAP. Remarkably, the model also excels at optical flow, sometimes outperforming specialized methods on the Sintel, KITTI, and Spring benchmarks. These results suggest that warping-based architectures can unify dense point tracking and optical flow estimation.
</details>

---

### Latent Action Pretraining Meets Pose Estimation
著者: Zhengqing Wang, Saurabh Nair, Prajwal Chidananda, Pujith Kachana, Samuel Li, Matthew Brown, Yasutaka Furukawa

<details>
<summary> 日本語要旨 </summary>

この論文では、自己監督学習の観点からカメラ姿勢推定を再考し、3Dアノテーションによる完全な監督学習という現在のトレンドに対するスケーラブルな代替手段として逆動力学学習を用いた事前学習に焦点を当てます。具体的には、大規模な運転ビデオからGenieのように潜在的なアクション表現を学ぶために逆動力学および前向き動力学モデルを使用します。私たちの考え方は単純でありながら効果的です。既存の手法では、潜在的なアクションをそのままの形で世界モデルのアクション条件付けやポリシーネットワーク内のロボットアクションパラメータのプロキシとして使用します。私たちの手法は、潜在的なアクション特徴をカメラ姿勢推定器への入力として再利用し、限られた数の高品質3Dアノテーションで微調整することにより、正確かつ汎化可能な姿勢予測を実現しつつ、フィードフォワード効率性を維持します。運転評価基準での広範な実験により、LA-Poseはラベル付きデータの使用量が桁違いに少なくても最先端手法と競合し、場合によってはそれを上回る性能を示すことがわかりました。具体的には、WaymoおよびPandaSet評価基準で、LA-Poseは最近のフィードフォワード手法よりも10%以上高い姿勢精度を達成しています。この研究が逆動力学自己監督学習における姿勢推定の可能性を示す初めての試みであると考えます。
</details>

<details>
<summary> 英語要旨 </summary>

This paper revisits camera pose estimation through the lens of self-supervised pretraining, focusing on inverse-dynamics pretraining as a scalable alternative to the current trend of fully supervised training with 3D annotations. Concretely, we employ inverse- and forward-dynamics models to learn latent action representations, similar to Genie from large-scale driving videos. Our idea is simple yet effective. Existing methods use latent actions in their original capacity, that is, as action conditioning of world-models or as proxies of robot action parameters in policy networks. Our method, dubbed LA-Pose, repurposes the latent action features as inputs to a camera pose estimator, finetuned on a limited set of high-quality 3D annotations. This formulation enables accurate and generalizable pose prediction while maintaining feed-forward efficiency. Extensive experiments on driving benchmarks show that LA-Pose achieves competitive and even superior performance to state-of-the-art methods while using orders of magnitude less labeled data. Concretely, on the Waymo and PandaSet benchmarks, LA-Pose achieves over 10% higher pose accuracy than recent feed-forward methods. To our knowledge, this work is the first to demonstrate the power of inverse-dynamics self-supervised learning for pose estimation.
</details>

---

### CycleManip: Enabling Cycle-based Manipulation Via Effective History Perception and Understanding
著者: Yi-Lin Wei, Haoran Liao, Yuhao Lin, Pengyue Wang, Zhizhao Liang, Guiliang Liu, Wei-Shi Zheng

<details>
<summary> 日本語要旨 </summary>

この論文では、ロボット操作における重要であるが十分に探求されていないタスクである「サイクルベースの操作」を調査します。これは、ロボットが期待される終了時間内に周期的または反復的なアクションを実行する必要があるタスクです。このようなタスクは日常生活で重要であり、例えば瓶を振ったり釘を打つことに当てはまります。しかし、これまでの研究ではほとんど探求されておらず、二つの主な課題があります：1) 模倣方法はしばしば期待される終了時間内にタスクを完了できないことが多く、これは歴史的データの効果的な活用が不十分であるためです；2) 十分なデータや自動評価ツールを備えた基準が存在しないことにより、この領域で有効な解決策の開発が阻害されています。これらの課題に対処するために、まず私たちは追加モデルや階層構造、または大きな計算オーバーヘッドを必要とせずにエンドツーエンドの模倣方式でサイクルベースのタスク操作を達成するための「CycleManipフレームワーク」を提案します。その核心的な洞察は、コスト意識のあるサンプリング戦略によって効果的な歴史認識を強化し、マルチタスク学習によって歴史的理解を向上させることです。次に、私たちはサイクルベースのタスク操作基準を導入します。これは多様なサイクルベースのタスクを提供し、自動評価方法も含んでいます。シミュレーションおよび実世界の設定における広範囲な実験は、私たちの手法がサイクルベースのタスク操作において高い成功率を達成していることを示しています。結果はまた、一般的な操作への強力な適応性能や、ビジョン言語行動（VLA）モデルなどの模倣ポリシーに対するプラグアンドプレイ機能を示しています。さらに、結果は私たちのアプローチがバイアームグリッパーや繊細な手、人間型ロボットといった多様なロボットプラットフォームに適用可能であることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

In this paper, we explore an important yet underexplored task in robot manipulation: cycle-based manipulation, where robots need to perform cyclic or repetitive actions with an expected terminal time. These tasks are crucial in daily life, such as shaking a bottle or knocking a nail. However, few prior works have explored this task, leading to two main challenges: 1) the imitation methods often fail to complete these tasks within the expected terminal time due to the ineffective utilization of history; 2) the absence of a benchmark with sufficient data and automatic evaluation tools hinders development of effective solutions in this area. To address these challenges, we firstly propose the CycleManip framework to achieve cycle-based task manipulation in a end-to-end imitation manner without requiring any extra models, hierarchical structure or significant computational overhead. The core insight is to enhance effective history perception by a cost-aware sampling strategy and to improve historical understanding by multi-task learning. Secondly, we introduce a cycle-based task manipulation benchmark, which provides diverse cycle-based tasks, and an automatic evaluation method. Extensive experiments conducted in both simulation and real-world settings demonstrate that our method achieves high success rates in cycle-based task manipulation. The results further show strong adaptation performance in general manipulation, and the plug-and-play ability on imitation policies such as Vision-Language-Action (VLA) models. Moreover, the results show that our approach can be applied across diverse robotic platforms, including bi-arm grippers, dexterous hands, and humanoid robots.
</details>

---

### WildPose: A Unified Framework for Robust Pose Estimation in The Wild
著者: Jianhao Zheng, Liyuan Zhu, Zihan Zhu, Iro Armeni

<details>
<summary> 日本語要旨 </summary>

動的環境におけるカメラ姿勢推定は、ほとんどの視覚SLAMやSfM手法が静的な環境からの入力を前提としているため、重要な課題です。最近では動的に対応する方法も存在しますが、それらはしばしば統一されておらず、セマンティックベースのアプローチは脆弱であり、シーケンスごとの最適化手法は短いシーケンスに失敗し、他の学習済みモデルは静的なシーンでは悪い性能を示すことがあります。私たちは、動的環境で堅牢である一方で、静的および低自己運動のデータセットにおいて最先端のパフォーマンスを維持する統一されたモノクロポーズ推定フレームワークであるWildposeを提案します。私たちの主な洞察は、現代3Dビジョンにおける2つの強力なパラダイムを結び付けることです：フィードフォワードモデルの豊かな知覚前処理部分と、異なるiableバンドル調整（BA）によるエンド・トゥ・エンド最適化。これを実現するために、異なるiable BAパイプラインを2つの方法で強化します。まず、凍結された事前学習済みMASt3R特徴バックボーンとその後の層を静的および動的データの多様なカリキュラムで訓練する新しい3D認識更新演算子を導入します。次に、同じ凍結されたバックボーンから得られる豊かなマルチレベルの3D認識特徴を活用した高容量動作マスク検出器を提案します。広範囲にわたる実験では、Wildposeが動的（Wild-SLAM、Bonn）、静的（TUM、7-Scenes）、および低自己運動（Sintel）のデータセットを含む多様なベンチマークにわたって一貫して先行研究を上回ることが示されています。
</details>

<details>
<summary> 英語要旨 </summary>

Estimating camera pose in dynamic environments is a critical challenge, as most visual SLAM and SfM methods assume inputs from static environments. While recent dynamic-aware methods exist, they are often not unified: semantic-based approaches are brittle, per-sequence optimization methods fail on short sequences, and other learned models sometimes perform badly on static-only scenes. We present Wildpose, a unified monocular pose estimation framework that is robust in dynamic environments while maintaining state-of-the-art performance on static and low-ego-motion datasets. Our key insight is to connect the two powerful paradigms in modern 3D vision: the rich perceptual frontend of feed-forward models and the end-to-end optimization of differentiable bundle adjustment (BA). We achieve this by enhancing the differentiable BA pipeline in two ways. First, we introduce a new 3D-aware update operator by integrating a frozen, pre-trained MASt3R feature backbone and training the operator's subsequent layers on a diverse curriculum of static and dynamic data. Second, we propose a high-capacity motion mask detector that leverages rich, multi-level 3D-aware features from the same frozen backbone. Extensive experiments show Wildpose consistently outperforms prior methods across a wide variety of benchmarks, including dynamic (Wild-SLAM, Bonn), static (TUM, 7-Scenes), and low-ego-motion (Sintel) datasets.
</details>

---

### Radiance Meshes for Volumetric Reconstruction
著者: Alexander Mai, Trevor Hedstrom, George Kopanas, Janne Kontkanen, Falko Kuester, Jonathan T. Barron

<details>
<summary> 日本語要旨 </summary>

私たちは、定数密度のテトラヘドロンセルを持つ放射場を表現するために、デラウナイ三次元格子化法で生成される「Radiance Meshes」を紹介します。ヴォロノイ図とは異なり、デラウナイ三次元格子化法は既存のハードウェアがネイティブにサポートするシンプルな三角形を生成します。このため、私たちのモデルは、ラスタライゼーションとレイトレーシングの両方を用いて正確かつ高速な体積レンダリングが可能です。また、新しいラスタライゼーション手法を導入し、同等のプリミティブ数と解像度を仮定した場合において、これまでの放射場表現よりも高速なレンダリングスピードを実現します。デラウナイ頂点位置の最適化はトポロジー上の不連続性（エッジフリップ）を引き起こしますが、これに対処するためにZip-NeRFスタイルのバックボーンを使用し、トポロジー変化時でも滑らかに変化する場を表現できるようにしています。私たちのレンダリング方法は体積レンダリング方程式を正確に評価し、標準的な消費者向けハードウェア上で高品質なリアルタイムビュー合成が可能です。また、私たちのテトラヘドラルメッシュは、魚眼レンズ歪み、物理ベースシミュレーション、編集、メッシュ抽出など、さまざまな興味深い応用に適しています。
</details>

<details>
<summary> 英語要旨 </summary>

We introduce Radiance Meshes for representing radiance fields with constant density tetrahedral cells produced with a Delaunay tetrahedralization. Unlike a Voronoi diagram, a Delaunay tetrahedralization yields simple triangles that are natively supported by existing hardware. As such, our model is able to perform exact and fast volume rendering using both rasterization and ray-tracing. We introduce a new rasterization method that achieve faster rendering speeds than all prior radiance field representations (assuming an equivalent number of primitives and resolution) across a variety of platforms. Optimizing the positions of Delaunay vertices introduces topological discontinuities (edge flips). To solve this, we use a Zip-NeRF-style backbone which allows us to express a smoothly varying field even when the topology changes. Our rendering method exactly evaluates the volume rendering equation and enables high quality, real-time view synthesis on standard consumer hardware. Our tetrahedral meshes also lend themselves to a variety of exciting applications including fisheye lens distortion, physics-based simulation, editing, and mesh extraction.
</details>

---

### Spatiotemporal Pyramid Flow Matching for Climate Emulation
著者: Jeremy Irvin, Jiaqi Han, Zikui Wang, Abdulaziz Alharbi, Yufei Zhao, Nomin-Erdene Bayarsaikhan, Daniele Visioni, Andrew Y. Ng, Duncan Watson-Parris

<details>
<summary> 日本語要旨 </summary>

生成モデルは、地球の変化する気候を模倣する方法を変革する可能性があります。従来の生成アプローチは天候スケールの自己回帰に依存していますが、これは長期的な気候予測において本質的に遅く、非定常的な外力下で安定した展開を示すことがまだありません。ここでは、スペースタイムピラミッドフロー（SPF）と呼ばれる新しい流量マッチングアプローチのクラスを紹介します。これは空間的および時間的スケールにわたってデータを階層的にモデル化します。カスケードビデオモデルからインスピレーションを得て、SPFは生成軌道を空間時間ピラミッドに分割し、空間解像度を徐々に増加させることで計算を削減し、各ステージを関連するタイムスケールと結合して、ピラミッド内の任意の時間レベルで直接サンプリングが可能になります。この設計は、それぞれのステージを指定された物理的外力（例えば温室効果ガスやエアロゾル）に条件付けることで、複数の時間スケールで効率的かつ並列な気候模倣を可能にします。ClimateBenchでは、SPFは年次および月次スケールで強力な流量マッチングベースラインや事前学習済みモデルを上回り、特に粗い時間レベルでの高速サンプリングを提供します。SPFをスケールするために、私たちはClimateSuiteを構築しました。これは現在までに最大の地球システムシミュレーションコレクションであり、10の気候モデルと初めて気候介入のシミュレーションを含む33,000以上のシミュレーション年から構成されています。拡張されたSPFモデルは、異なる気候モデルにわたる保持アウトシナリオで良好な汎化を示すことが分かりました。これらの結果から、SPFとClimateSuiteは、時間スケールおよび現実的な将来シナリオにわたる正確で効率的な確率的気候模倣の基盤を提供します。データとコードは[レビュー用に匿名化]で公開されています。
</details>

<details>
<summary> 英語要旨 </summary>

Generative models have the potential to transform the way we emulate Earth’s changing climate. Previous generative approaches rely on weather-scale autoregression for climate emulation, but this is inherently slow for long climate horizons and has yet to demonstrate stable rollouts under nonstationary forcings. Here, we introduce Spatiotemporal Pyramid Flows (SPF), a new class of flow matching approaches that model data hierarchically across spatial and temporal scales. Inspired by cascaded video models, SPF partitions the generative trajectory into a spatiotemporal pyramid, progressively increasing spatial resolution to reduce computation and coupling each stage with an associated timescale to enable direct sampling at any temporal level in the pyramid. This design, together with conditioning each stage on prescribed physical forcings (e.g., greenhouse gases or aerosols), enables efficient, parallel climate emulation at multiple timescales. On ClimateBench, SPF outperforms strong flow matching baselines and pre-trained models at yearly and monthly timescales while offering fast sampling, especially at coarser temporal levels. To scale SPF, we curate ClimateSuite, the largest collection of Earth system simulations to date, comprising over 33,000 simulation-years across ten climate models and the first dataset to include simulations of climate interventions. We find that the scaled SPF model demonstrates good generalization to held-out scenarios across climate models. Together, SPF and ClimateSuite provide a foundation for accurate, efficient, probabilistic climate emulation across temporal scales and realistic future scenarios. Data and code is publicly available at [anonymized for review].
</details>

---

### 3D-LATTE: Latent Space 3D Editing from Textual Instructions
著者: Maria Parelli, Michael Oechsle, Michael Niemeyer, Federico Tombari, Andreas Geiger

<details>
<summary> 日本語要旨 </summary>

最近のテキスト/画像ベースの3Dアセット生成におけるマルチビュー拡散モデルの成功にもかかわらず、3Dアセットの指示に基づく編集は驚くほど生成モデルの品質に遅れをとっています。その主な理由は、最近の2次元事前知識を使用した手法が視点間で一貫性のない編集信号を引き起こすためです。2D事前知識蒸留方法やマルチビュー編集戦略を超えて、私たちはネイティブ3D拡散モデルの潜在空間内で動作するトレーニングフリーな編集手法を提案します。これにより、直接的に3D幾何学を操作することが可能です。ソースオブジェクトから生成された3D注意マップを混合して編集の合成を導くことで、幾何学に配慮した正則化ガイダンス、フーリエ領域でのスペクトル変調戦略、3D強化のための洗練ステップと組み合わせることにより、私たちの手法は以前の3D編集方法を上回り、さまざまな形状や意味的操作において高品質で正確な編集を可能にします。コードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Despite the recent success of multi-view diffusion models for text/image-based 3D asset generation, instruction-based editing of 3D assets lacks surprisingly far behind the quality of generation models. The main reason is that recent approaches using 2D priors suffer from view-inconsistent editing signals. Going beyond 2D prior distillation methods and multi-view editing strategies, we propose a training-free editing method that operates within the latent space of a native 3D diffusion model, allowing us to directly manipulate 3D geometry. We guide the edit synthesis by blending 3D attention maps from the generation with the source object. Coupled with geometry-aware regularization guidance, a spectral modulation strategy in the Fourier domain and a refinement step for 3D enhancement, our method outperforms previous 3D editing methods enabling high-fidelity and precise edits across a wide range of shapes and semantic manipulations. Code will be publicly released.
</details>

---

### VideoITG: Multimodal Video Understanding with Instructed Temporal Grounding
著者: Shihao Wang, Guo Chen, De-An Huang, Zhiqi Li, Minghan LI, Guilin Liu, Jan Kautz, Jose M. Alvarez, Lei Zhang, Zhiding Yu

<details>
<summary> 日本語要旨 </summary>

ビデオ大規模言語モデル（Video-LLMs）は、マルチモーダル理解および推論タスクにおいて顕著な可能性を示していますが、ビデオから最も情報量の高いフレームを効率的に選択する方法は依然として重要な課題です。既存の手法では、インターフレーム冗長性を減少させるか、無監督イベントローカライゼーションを用いてフレームサンプリングを最適化しようとしています。しかし、これらのアプローチは複雑な指示に従ったタスクや正確な時系列モデリングが求められるシナリオで不十分であり、セマンティックアライメントおよび時系列推論の両方で限定的な性能を示しています。これらの課題に対処するために、私たちはユーザー指示に基づいてフレームサンプリング戦略を適応的にカスタマイズすることを目的とした「ビデオITG（Instructed Temporal Grounding for Videos）」フレームワークを導入します。具体的には、指示条件付きキャプションの生成、関連するビデオセグメントの取得、および効率的な監督を可能にする重要フレームの選択を自動化する「VidThinker」パイプラインを設計しました。VidThinkerを使用して、500,000件の時系列グランディングアノテーションを含む40,000本のビデオからなるVideoITG-40Kデータセットを構築しました。私たちのプラグアンドプレイ型VideoITGモデルは、Video-LLMsの視覚言語アラインメントおよび推論能力を活用して差別的なフレーム選択を行います。VideoITGは、マルチモーダルビデオ理解評価基準において一貫して性能を向上させ、その有効性と潜在力を示しました。
</details>

<details>
<summary> 英語要旨 </summary>

While Video Large Language Models (Video-LLMs) have shown significant potential in multimodal understanding and reasoning tasks, how to efficiently select the most informative frames from videos remains a critical challenge. Existing methods attempt to optimize frame sampling by reducing inter-frame redundancy or employing unsupervised event localization. However, these approaches often fall short in handling complex instruction-following tasks and scenarios that demand precise temporal modeling, resulting in limited performance in both semantic alignment and temporal reasoning. To address the above challenges, we introduce Instructed Temporal Grounding for Videos (VideoITG), a framework aiming to adaptively customize frame sampling strategies based on user instructions. Specifically, we design the VidThinker pipeline, which automates annotation by generating instruction-conditioned captions, retrieving relevant video segments, and selecting key frames to enable efficient supervision. Using VidThinker, we build the VideoITG-40K dataset with 40K videos and 500K temporal grounding annotations. Our plug-and-play VideoITG model leverages Video-LLMs’ visual-language alignment and reasoning for discriminative frame selection. VideoITG consistently boosts the performance on multiple multimodal video understanding benchmarks, demonstrating its effectiveness and potential.
</details>

---

### PromptStereo: Zero-Shot Stereo Matching Via Structure and Motion Prompts
著者: Xianqi Wang, Hao Yang, Hangtian Wang, JunDa Cheng, Gangwei Xu, Min Lin, Xin Yang

<details>
<summary> 日本語要旨 </summary>

現代のステレオマッチング手法は、モノクル深度ファウンデーションモデルを活用することで、優れたゼロショット一般化性能を達成しています。しかし、既存の多くの方法は、コストボリューム構築や不整合初期化において頑健な特徴を抽出することに主眼を置いています。一方で、ゼロショット一般化にも重要な反復精緻化段階は未だ十分に探求されていません。ある方法ではモノクル深度事前情報を反復の指針として扱いますが、通常のGRUベースアーキテクチャはその表現能力が限られているためにこれを十分に活用することが難しいです。本論文では、モノクル深度ファウンデーションモデルのデコーダーに基づく新しい反復精緻化モジュールであるプロンプト再帰単位（PRU）を提案します。モノクル構造とステレオ運動手がかりをデコーダーにプロンプトとして統合することで、PRUはモノクル深度ファウンデーションモデルの潜在表現に絶対ステレオスケール情報を豊かにしつつ、その固有のモノクル深度事前情報を保持します。実験では、私たちのPromptStereoが複数のデータセットで最先端のゼロショット一般化性能を達成し、かつ同等または高速な推論スピードを維持することを示しています。私たちの発見は、プロンプトによる指導的反復精緻化がゼロショットステレオマッチングにおける有望な方向性であることを強調しています。
</details>

<details>
<summary> 英語要旨 </summary>

Modern stereo matching methods have leveraged monocular depth foundation models to achieve superior zero-shot generalization performance. However, most existing methods primarily focus on extracting robust features for cost volume construction or disparity initialization. At the same time, the iterative refinement stage, which is also crucial for zero-shot generalization, remains underexplored. Some methods treat monocular depth priors as guidance for iteration, but conventional GRU-based architectures struggle to exploit them due to the limited representation capacity. In this paper, we propose Prompt Recurrent Unit (PRU), a novel iterative refinement module based on the decoder of monocular depth foundation models. By integrating monocular structure and stereo motion cues as prompts into the decoder, PRU enriches the latent representations of monocular depth foundation models with absolute stereo-scale information while preserving their inherent monocular depth priors. Experiments demonstrate that our PromptStereo achieves state-of-the-art zero-shot generalization performance across multiple datasets, while maintaining comparable or faster inference speed. Our findings highlight prompt-guided iterative refinement as a promising direction for zero-shot stereo matching.
</details>

---

### Toward Low-Cost Yet Effective Temporal Learning for UAV Tracking
著者: chaocan xue, Qihua Liang, Bineng Zhong, Yanting Zu, Yuanliang Xue, Haiying Xia, Shuxiang Song

<details>
<summary> 日本語要旨 </summary>

トラッキングコミュニティにおいて、時間情報の利用は常に開かれた議題でした。しかし、既存のトラッカーは徐々により多くの入力やパラメータを使用して時間的学習を行う傾向があり、これがリソース制約のある無人航空機（UAV）での展開を妨げています。さらに重要なことは、性能向上が時間的学習そのものから得られたものか、それとも増加した入力やパラメータから得られたものかが不明確である点です。本研究では、性能向上と計算コストを同時に考慮したバランスの取れた視点から時間的学習コンポーネントを設計することを提唱します。この目的を達成するため、新しい評価指標である「精度/浮動小数点演算（PPF）」を導入します。PPFは時間的学習コンポーネントによって得られたトラッキング精度の向上を、FLOPsあたりで定量化し、これらのコンポーネント間の公平かつ効率意識のある比較を可能にし、より効率的な設計へと導きます。この指標に基づいて、文脈関係を効率的にモデル化する低コストで効果的な時間的学習（LETL）アプローチを提案します。このアプローチはビデオストリーム内の代表的な外観トークンを連続して伝播・統合し、相対的に低い計算コストでターゲットの変化するパターンを効率的に捕捉します。LETLアプローチを既存のワンストリームフレームワークに統合し、堅牢なUAVトラッキング用のシンプルかつ効果的なトラッカーであるLETrackを構築します。複数の航空追跡データセットにおける広範な実験結果は、我々のLETrackの優位性を示し、提案されたLETLアプローチがより高いPPFスコアを達成しており、他の時間的学習戦略を上回っていることを示します。
</details>

<details>
<summary> 英語要旨 </summary>

The utilization of temporal information has always been an open topic in the tracking community. However, existing trackers tend to employ more and more inputs or parameters for temporal learning, hindering their deployment in resource-constrained unmanned aerial vehicles (UAVs). More importantly, this raises ambiguity whether the performance gains come from the temporal learning itself, or come from the increased inputs and parameters. In this study, we advocate designing temporal learning components from a more balanced perspective that jointly considers performance gains and computational costs. To achieve this goal, we introduce a new evaluation metric, i.e., precision per FLOPs (PPF). The PPF is introduced to quantify the tracking precision gains achieved by temporal learning components per unit of FLOPs, thus enabling fair and efficiency-aware comparisons among these components and driving them toward more efficient designs. Based on this metric, we propose a low-cost yet effective temporal learning (LETL) approach to efficiently model contextual relationships. This approach continuously propagates and merges representative appearance tokens in video streams, allowing the tracker to efficiently capture the changing patterns of targets with relatively low computational costs. We integrate the LETL approach into existing one-stream frameworks, thereby building a simple yet effective tracker, namely LETrack, for robust UAV tracking. Extensive experimental results on multiple aerial tracking datasets demonstrate the superiority of our LETrack, and show that the proposed LETL approach achieves higher PPF scores, outperforming other temporal learning strategies.
</details>

---

### Virtual Full-stack Scanning of Brain MRI Via Imputing Any Quantised Code
著者: Yicheng Wu, Tao Song, Zhonghua Wu, Jin Ye, Zongyuan Ge, Wenjia Bai, Zhaolin Chen, Jianfei Cai

<details>
<summary> 日本語要旨 </summary>

磁気共鳴画像法（MRI）は、さまざまな取得モダリティを用いて解剖学に関する広範な情報を提供する強力で多様性のある画像技術です。しかし、臨床フローでは、スキャン時間やコスト制約のためにすべての関連モダリティを収集することは現実的ではありません。仮想全層スキャニングは、利用可能ながら不完全な取得から欠落しているMRIモダリティを補間し、コスト効率の良い方法でデータの完全性と臨床的有用性を向上させようとします。既存の補間手法はしばしばグローバル条件付けやモダリティ固有の設計に依存しており、これが患者集団や画像プロトコルをまたいで一般化することを制限します。これらの制約に対処するために、私たちはCodeBrainという統一フレームワークを提案し、「任意から任意」の補間タスクを領域レベルでの完全層コード予測問題として再定式化します。CodeBrainは2段階のパイプラインを採用しています：（1）完全なMRIモダリティセットを領域レベルでスカラー量子化コードにエンコードし、これらのコードとモダリティ非依存の共通特徴をデコードすることで高忠実度の画像再構成が可能なコンパクト表現を学習します；（2）不完全なモダリティからフルスタックコードマップを予測するために、多様な補間シナリオに対応するグレーディングベースの設計で投影エンコーダーをトレーニングします。IXIおよびBraTS 2023という2つの公開脳MRIデータセットでの広範な実験は、CodeBrainが最先端の手法を一貫して上回り、統一された脳MRI補間の新しいベンチマークを確立し、仮想全層スキャニングを可能にすることを示しています。コードはリリースされます。
</details>

<details>
<summary> 英語要旨 </summary>

Magnetic resonance imaging (MRI) is a powerful and versatile imaging technique, offering a wide spectrum of information about the anatomy by employing different acquisition modalities. However, in the clinical workflow, it is impractical to collect all relevant modalities due to the scan time and cost constraints. Virtual full-stack scanning aims to impute missing MRI modalities from available but incomplete acquisitions, offering a cost-efficient solution to enhance data completeness and clinical usability. Existing imputation methods often depend on global conditioning or modality-specific designs, which limit their generalisability across patient cohorts and imaging protocols. To address these limitations, we propose CodeBrain, a unified framework that reformulates various ``any-to-any'' imputation tasks as a region-level full-stack code prediction problem. CodeBrain adopts a two-stage pipeline: (1) it learns the compact representation of a complete MRI modality set by encoding it into scalar-quantised codes at the region level, enabling high-fidelity image reconstruction after decoding these codes along with modality-agnostic common features; (2) it trains a projection encoder to predict the full-stack code map from incomplete modalities via a grading-based design for diverse imputation scenarios. Extensive experiments on two public brain MRI datasets, i.e., IXI and BraTS 2023, demonstrate that CodeBrain consistently outperforms state-of-the-art methods, establishing a new benchmark for unified brain MRI imputation and enabling virtual full-stack scanning. Code will be released.
</details>

---

### Hypergraph-State Collaborative Reasoning for Multi-Object Tracking
著者: Zikai Song, Junqing Yu, Yi-Ping Phoebe Chen, Wei Yang, Xinchao Wang

<details>
<summary> 日本語要旨 </summary>

マルチオブジェクト追跡（MOT）において、動作推論はターゲットをフレーム間で一貫して関連付けることを可能にする基盤です。しかし、既存の動作推定手法は2つの主要な制約に直面しています：（1）ノイズや確率的予測によって引き起こされる不安定性、および（2）視覚的手がかりが消失した際の遮蔽下での脆弱性。これらの問題を克服するために、私たちは複数の相関オブジェクト間の共同推論を通じて動作推定を向上させる協調的推論フレームワークを提案します。類似した運動状態を持つオブジェクトがお互いに制約し、補正し合うことで、私たちのフレームワークはノイズの多い軌跡を安定化させ、ターゲットが遮蔽されている場合でも妥当な動作連続性を推測します。この概念を実現するために、私たちはハイパーハイパーグラフ計算とステート空間モデル（SSM）を統合したアーキテクチャであるHyperSSMを設計しました。これは統一された空間・時間的推論のためです。ハイパーハイパーグラフモジュールは動的なハイパーエッジを通じて空間運動相関を捉え、SSMは構造化された状態遷移によって時間的滑らかさを強制します。この協調設計により、空間の合意と時間的一貫性の同時最適化が可能となり、堅牢で安定した動作推定が実現されます。MOT17、MOT20、DanceTrack、およびSportsMOTを含む4つの主流かつ多様なベンチマークにわたる広範囲な実験は、さまざまな運動パターンとシーンの複雑性をカバーしており、私たちのアプローチが幅広い追跡シナリオで最先端の性能を達成することを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Motion reasoning serves as the cornerstone of multi-object tracking (MOT), as it enables consistent association of targets across frames. However, existing motion estimation approaches face two major limitations: (1) instability caused by noisy or probabilistic predictions, and (2) vulnerability under occlusion, where trajectories often fragment once visual cues disappear. To overcome these issues, we propose a collaborative reasoning framework that enhances motion estimation through joint inference among multiple correlated objects. By allowing objects with similar motion states to mutually constrain and refine each other, our framework stabilizes noisy trajectories and infers plausible motion continuity even when target is occluded. To realize this concept, we design HyperSSM, an architecture that integrates Hypergraph computation and a State Space Model (SSM) for unified spatial–temporal reasoning. The Hypergraph module captures spatial motion correlations through dynamic hyperedges, while the SSM enforces temporal smoothness via structured state transitions. This synergistic design enables simultaneous optimization of spatial consensus and temporal coherence, resulting in robust and stable motion estimation. Extensive experiments on four mainstream and diverse benchmarks(MOT17, MOT20, DanceTrack, and SportsMOT) covering various motion patterns and scene complexities, demonstrate that our approach achieves state-of-the-art performance across a wide range of tracking scenarios.
</details>

---

### Thinking with Video: Video Generation As A Promising Multimodal Reasoning Paradigm
著者: Jingqi Tong, Yurong Mou, Hangcheng Li, Mingzhe Li, Yongzhuo Yang, Ming Zhang, Qiguang Chen, Tianyi Liang, Xiaomeng Hu, Yining Zheng, Xinchi Chen, Jun Zhao, Xuanjing Huang, Xipeng Qiu

<details>
<summary> 日本語要旨 </summary>

テキストと「イメージを用いた思考」のパラダイムは、大規模言語モデル（LLMs）およびビジョン・ランゲージ・モデル（VLMs）の推論能力を大幅に向上させます。しかし、これらのパラダイムには固有の限界があります。(1) 画像は単一の瞬間しか捉えず、動的なプロセスや連続した変化を表現できません。また、(2) テキストとビジョンを異なるモダリティとして分離することが、統一されたマルチモーダル理解や生成を妨げています。したがって、「動画を用いた思考」という新しいパラダイムを提案します。これは、Sora-2のような動画生成モデルを活用して、動画フレームをマルチモーダル推論の統一された媒体として使用するものです。この探求を支援するために、「Video Thinking Benchmark（VideoThinkBench）」を開発しました。これは、(1) ビジョン中心のタスク（例：Eyeballing Puzzles）、および(2) テキスト中心のタスク（例：GSM8KやMMMUのサブセット）を含む二つのタスクカテゴリーから成ります。VideoThinkBenchでの評価により、Sora-2が有能な推論者であることが確立されました。ビジョン中心のタスクでは、Sora-2は最先端（SOTA）VLMsと一般的に同等であり、GPT5を10%上回ってEyeballing Puzzlesで優れています。テキスト中心のタスクでは、MATHで92%、MMMUで69.2%の正答率を達成しています。さらに、これらの能力の源泉を体系的に分析しました。また、自己整合性とインコンテキスト学習がSora-2のパフォーマンス向上に寄与することも見つけました。要約すると、私たちの発見は動画生成モデルが統一されたマルチモーダル理解および生成モデルとしての可能性を示し、「Thinking with Video」を統一されたマルチモーダル推論パラダイムと位置付けています。
</details>

<details>
<summary> 英語要旨 </summary>

Thinking with Text and "Thinking with Images" paradigm significantly improve the reasoning ability of large language models (LLMs) and Vision Language Models (VLMs). However, these paradigms have inherent limitations. (1) Images capture only single moments and fail to represent dynamic processes or continuous changes, and (2) The separation of text and vision as distinct modalities, hindering unified multimodal understanding and generation. Therefore, we propose "Thinking with Video", a new paradigm that leverages video generation models such as Sora-2 to use video frames as a unified medium for multimodal reasoning. To support this exploration, we developed the Video Thinking Benchmark (VideoThinkBench), which encompasses two task categories: (1) vision-centric tasks (e.g., Eyeballing Puzzles), and (2) text-centric tasks (e.g., subsets of GSM8K, MMMU). Our evaluation on VideoThinkBench establishes Sora-2 as a capable reasoner. On vision-centric tasks, Sora-2 is generally comparable to state-of-the-art (SOTA) VLMs, and even surpassing GPT5 by 10% on eyeballing puzzles. On text-centric tasks, Sora-2 achieves 92% accuracy on MATH, and 69.2% accuracy on MMMU. Furthermore, we systematically analyse the source of these abilities. We also find that self-consistency and in-context learning can improve Sora-2’s performance. In summary, our findings demonstrate that the video generation model is the potential unified multimodal understanding and generation model, positioning "Thinking with Video" as a unified multimodal reasoning paradigm.
</details>

---

