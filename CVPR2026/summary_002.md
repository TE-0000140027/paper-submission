# CVPR2026 論文要旨 (Part 2)

### Scaling Parallel Sequence Models to Vision Foundation Models
著者: Yitong Jiang, Collin McCarthy, Hongjun Wang, Hanrong Ye, Qi Dou, Tianfan Xue, Jinwei Gu, Jan Kautz, Danny Yin, Pavlo Molchanov, Sifei Liu

<details>
<summary> 日本語要旨 </summary>

自己注意の二次的複雑性により、ビジョンファウンデーションモデルのスケーリングは制約されています。線形時間で動作する一般化空間伝播ネットワーク（GSPN）など、サブ二次的注意の代替手段である線形注意変種や状態空間モデルは、画像を1Dトークンシーケンスに直列化することで空間的一貫性と効率性を損なうものの、モデル複雑性を削減します。GSPNは2次元グリッド上で直接文脈を伝播させることにより線形時間で動作し、位置埋め込みを排除しますが、GPUスケーリングの限界に達しています。バッチやチャネルの増加はSM並列性を飽和させ、スキャンを直列化し、ラグタイムを引き起こします。私たちはCompact GSPN（C-GSPN）を導入しました。これは伝播空間を圧縮して精度を保持しつつ、伝播のラグタイムをほぼ10倍削減するViTブロックです。効率性をさらに向上させるために軽量投影とCUDAカーネルの統合を行います。大規模な事前学習を可能にするため、レイヤーごとの監督とエンド・ツー・エンドの整列を組み合わせた二段階クロスオペレーター転移戦略を採用します。代表的な1K構成（バッチ32、C=1152）では、C-GSPNは最大で2倍の高速化を達成し、ゼロショット精度を維持しつつセグメンテーションを+2.1%改善します。広範な実験と分解により、提案された圧縮と二段階転移が強力な転移のために重要であり、かつ計算を大幅に削減することが示されています。これにより、初めてサブ二次的演算子がファウンデーションスケール（CLIPスタイル）のビジョン事前学習に拡張されました。
</details>

<details>
<summary> 英語要旨 </summary>

Scaling vision foundation models is constrained by the quadratic complexity of self-attention. Although subquadratic attention alternatives like linear attention variants and state-space models successfully reduce the model complexity, they typically serialize images into 1D token sequences, compromising spatial coherence and efficiency. Generalized Spatial Propagation Networks (GSPN) offer a linear-time alternative that propagates context directly on the 2D grid via line-scan propagation and removes positional embeddings, yet the original design hits GPU-scaling limits: growing batch/channels saturate SM concurrency, serializing scans, and spiking latency. We introduce Compact GSPN (C-GSPN), a ViT block that compresses the propagation space to preserve accuracy while cutting propagation latency by nearly 10×. We further improve efficiency with lightweight projections and fused CUDA kernels. To enable large-scale pretraining, we adopta two-stage cross-operator distillation strategy that combines layer-wise supervision with end-to-end alignment. In a representative 1K configuration (batch 32, C=1152), C-GSPN achieves up to 2× speedup, maintains competitive zero-shot accuracy, and improves segmentation by +2.1%. Extensive experiments and ablations show that the proposed compression and two-stage distillation are criticalfor strong transfer while substantially reducing compute, enabling the first extension of a subquadratic operator to foundation-scale (CLIP-style) vision pretraining.
</details>

---

### Paper2Figure: A Multi-Agent Collaborative System for Figure Generation Towards Academic Research Paper
著者: Siwei Han, Haonian Ji, Siyang Xin, Juanquan Shi, Shi Qiu, Xinyu Ye, Peng Xia, Jiaqi Liu, Zhaorun Chen, Yiyang Zhou, Linjie Li, Lijuan Wang, Huaxiu Yao

<details>
<summary> 日本語要旨 </summary>

研究論文のために明確で正確な図を自動生成することは依然として難しい課題です。これには意味理解、精密構造、視覚的美学が必要です。既存のアプローチでは忠実性と品質のバランスを取ることが難しく、大言語モデル（LLM）に基づくコードベースの方法（例：SVG, Mermaid）は構造化されていますが硬直的であり、画像生成モデル（例：GPT-Image-1, Nano Banana）は編集しにくく、しばしば不正確な図を生成します。私たちは、論文から図を生成するための二重マルチエージェントシステムとインタラクティブウェブプラットフォームであるPaper2Figureを提案します。生成エージェントはテキストを私たちが設計したFigScript言語に変換し、図の意味、スタイル、レイアウトをエンコードします。ウェブシステムはこのFigScriptを初期画像にレンダリングし、Refinementエージェントが反復的に問題を特定してFigScriptを論理、整列、美学、およびテキストの正確性を改善するために修正します。重要なことに、ユーザーは直感的なウェブインターフェースを通じて結果をさらに洗練できるため、最終出力に対して完全な制御が可能です。Paper2Figureの評価のために、100の学術図とペアになった説明から成るPaper2Figure Benchを導入します。実験では、Paper2Figureが人間の調整なしで完全自動生成時に最先端ベースラインよりも正確性を12%、美しさを13.5%、完成度を17.0%向上させることを示しています。自動生成とインタラクティブ編集の組み合わせにより、Paper2FigureはAI支援と研究者の制御の間のギャップを埋め、高品質な学術図作成のための実用的な解決策を提供します。
</details>

<details>
<summary> 英語要旨 </summary>

Automatically generating clear and accurate figures for research papers remains challenging, as it requires semantic understanding, precise structure, and visual aesthetics. Existing approaches struggle to balance fidelity and quality: large language model (LLM) code-based methods (e.g., SVG, Mermaid) are structured but inflexible, while image-generation models (e.g., GPT-Image-1, Nano Banana) produce hard-to-edit and often inaccurate figures. We present Paper2Figure, a dual multi-agent system with an interactive web platform for paper-to-figure generation. Generation Agents convert text into our designed FigScript language, encoding figure semantics, styles and layout. The web system renders the FigScript into an initial image, which Refinement Agents iteratively analyze to locate issues and revise the FigScript for improved logic, alignment, aesthetics and text accuracy. Crucially, users can further refine results through an intuitive web interface, ensuring full control over the final output. To evaluate Paper2Figure, we introduce Paper2Figure Bench, a benchmark comprising 100 academic figures with paired descriptions. Experiments demonstrate that Paper2Figure markedly improves accuracy by 12%, beauty by 13.5%, and completeness by 17.0% over state-of-the-art baselines in fully automatic generation without human adjustment. By combining automated generation with interactive edit, Paper2Figure bridges the gap between AI assistance and researcher control, offering a practical solution for high-quality academic figure creation.
</details>

---

### Real-Time Generation of Streamable Talking Portrait Video with Reference-Guided Deep Compression VAEs
著者: Sicheng Xu, Yu Deng, Shoukang Hu, Yichuan Wang, Yizhong Zhang, Zhan Chen, Jiaolong Yang, Baining Guo

<details>
<summary> 日本語要旨 </summary>

ビデオ拡散モデルはポートレート動画生成において大きな進歩を遂げましたが、その高い計算要求はインタラクティブアプリケーションでの使用を制限しています。本研究では、音声入力と参照画像に条件付けられたストリーミング可能なトークポートレートビデオ生成のフレームワークを提案します。このフレームワークはストリーミングシナリオに特化して設計され、深層的な潜在変数圧縮用の因果ビデオVAEと自己回帰潜在変数ノイズ除去モデルを備えています。私たちの因果VAEは、参照画像の可変数をガイダンスとして統合し、動的情報に焦点を当てることで静的な外観ではなく圧縮効率と再構成品質を向上させます。また、私たちは残差自己符号化パラダイムを拡張し、VAEにおける空間時間因果性の処理を改善しています。ジェネレータはRectified Flow Transformerアーキテクチャに基づいており、ビデオ潜在変数をブロックごとに自己回帰的な方法で生成します。私たちの手法により、リアルタイムで高品質なトークポートレート動画が生成可能となり、ベースラインモデルよりもはるかに速いスピードを達成しています。さらに、包括的な実験では、リアリズム、生き生き感、ビデオ品質の面で大規模モデルと同等またはそれ以上の性能を示していることが確認されました。
</details>

<details>
<summary> 英語要旨 </summary>

Video diffusion models have significantly advanced portrait video generation, yet their high computational demands limit their use in interactive applications. This work presents a framework for streamable talking portrait video generation conditioned on speech audio and reference images. Designed meticulously for streaming scenarios, it features a causal video VAE for deep latent compression and an auto-regressive latent denoising model. Our causal VAE integrates a variable number of reference images as guidance, allowing the network to focus on dynamic information rather than static appearance, thereby enhancing compression efficacy and reconstruction quality. Additionally, we extend the residual auto-encoding paradigm to improve spatial-temporal causality handling in our VAE. The generator is based on a Rectified Flow Transformer architecture and produces video latents in a blockwise auto-regressive manner. Our method enables the real-time generation of high-quality talking portrait videos, achieving speeds significantly faster than baseline models. Furthermore, comprehensive experiments demonstrate that it is on par with or even outperforms these large models in realism, vividness, and video quality.
</details>

---

### From Where Things Are to What They Are For: Benchmarking Spatial–Functional Intelligence in Multimodal LLMs
著者: Le Zhang, Jihan Yang, Soundarya Krishnan, Jimit Majmudar, Xiou Ge, Prasoon Puri, Prathamesh Saraf, Shruti Bhargava, Dhivya Piraviperumal, Yinan Ling, Cindy Pan, Hong Yu, Aishwarya Agrawal, Bo-Hsiang Tseng

<details>
<summary> 日本語要旨 </summary>

人間レベルのエージェンシー知性は、低次元の幾何学的認識を超えて進化し、物事がどこにあるかを知ることから、それらが何のためであるかを理解する段階へと移行します。既存のベンチマークは多様なモーダルLLM（大規模言語モデル）の基礎的な幾何学的認識能力を効果的に評価しますが、地に足のついた知性に不可欠な高次の認知能力を探ることはできません。このギャップを埋めるために、私たちは空間機能的知性ベンチマーク（SFI-Bench）を導入します。これは多様な視点からの室内ビデオスキャンから得られた1500以上の専門家によって注釈された質問を含む動画ベースのベンチマークです。SFI-Benchは、高度な推論の2つの補完的次元を体系的に評価することを目的としています：1）構造化された空間的推論、複雑なレイアウトを理解し、一貫した空間表現を形成する能力、および2）機能的推論、オブジェクトの利用可能性と文脈依存の有用性を推測する能力です。そのタスクには条件付きカウント、マルチホップ関係推論、機能的ペアリング、知識に基づくトラブルシューティングが含まれ、これらはモデルの認識、記憶、および推論を統合する能力に直接挑戦します。私たちの実験では、現在の多様なLLMが空間的記憶と機能的・外部知識を統合することで一貫して苦労していることが明らかになり、重要なボトルネックが浮き彫りにされました。SFI-Benchは、より高度な認知能力を持ち、真に地に足のついた多様なエージェントへと進化するための重要なツールを提供します。
</details>

<details>
<summary> 英語要旨 </summary>

Human level agentic intelligence transcends low-level geometric perception, evolving from knowing where things are to understanding what they are for. While existing benchmarks effectively evaluate this foundational geometric perception capabilites of multimodal LLMs, they fall short of probing the higher-order cognitive abilities essential for grounded intelligence. To bridge this gap, we introduce the Spatial-Functional Intelligence Benchmark (SFI-Bench), a video-based benchmark with over 1500 expert-annotated questions derived from diverse, egocentric indoor video scans. SFI-Bench is designed to systematically evaluate two complementary dimensions of advanced reasoning: 1) Structured Spatial Reasoning, understanding complex layouts and forming coherent spatial representations, and 2) Functional Reasoning, inferring object affordances and context-dependent utility. Its tasks, including conditional counting, multi-hop relational reasoning, functional pairing, and knowledge-grounded troubleshooting, directly challenge a model's ability to integrate perception, memory, and inference. Our experiments reveal that current MLLMs consistently struggle to integrate spatial memory with functional and external knowledge, highlighting a critical bottleneck. SFI-Bench thus provides an essential tool for measuring and driving progress towards more cognitively capable and truly grounded multimodal agents.
</details>

---

### MimiCAT: Mimic with Correspondence-Aware Cascade-Transformer for Category-Free 3D Pose Transfer
著者: Zenghao Chai, Chen Tang, Yongkang Wong, Xulei Yang, Mohan Kankanhalli

<details>
<summary> 日本語要旨 </summary>

3Dポーズ転送は、ソースメッシュのポーズスタイルを対象キャラクターに移行させつつ、対象の幾何学的特性とソースのポーズ特徴を保持することを目指します。既存の方法は主に構造が類似したキャラクターに限定されており、カテゴリフリーな設定（例えばヒューマノイドのポーズを四足動物に転送すること）への一般化が困難です。異なるキャラクタータイプ間で見られる構造的および変換の多様性が、不一致な領域や低品質な転送を引き起こす主要な課題です。これに対処するため、まず数百種類の異なるキャラクターにわたる100万スケールのポーズデータセットを構築します。さらに、カテゴリフリー3Dポーズ転送用にMimiCATというカスケードトランスフォーマーモデルを提案します。MimiCATは厳密な一対一の対応マッピングに依存することなく、セマンティックキーポイントラベルを利用して柔軟な多対多マッチングを可能にする新しいソフトコレスポンデンスを学習します。その後、ポーズ転送は条件付き生成プロセスとして定式化され、ソースの変換がソフトコレスポンデンスマッチングによって対象へ投影され、形状条件付き表現を用いてさらに洗練されます。広範な定性的および定量的実験は、MimiCATが異なるキャラクター間で妥当なポーズを転送し、ヒューマノイド-ヒューマノイドのような狭いカテゴリ転送に限定された既存手法を大幅に上回ることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

3D pose transfer aims to transfer the pose-style of a source mesh to a target character while preserving both the target's geometry and the source's pose characteristic. Existing methods are largely restricted to characters with similar structures and fail to generalize to category-free settings (e.g., transferring a humanoid's pose to a quadruped). The key challenge lies in the structural and transformation diversity inherent in distinct character types, which often leads to mismatched regions and poor transfer quality. To address these issues, we first construct a million-scale pose dataset across hundreds of distinct characters. We further propose MimiCAT, a cascade-transformer model designed for category-free 3D pose transfer. Instead of relying on strict one-to-one correspondence mappings, MimiCAT leverages semantic keypoint labels to learn a novel soft correspondence that enables flexible many-to-many matching across characters. The pose transfer is then formulated as a conditional generation process, in which the source transformations are first projected onto the target through soft correspondence matching and subsequently refined using shape-conditioned representations. Extensive qualitative and quantitative experiments demonstrate that MimiCAT transfers plausible poses across different characters, significantly outperforming prior methods that are limited to narrow category transfer (e.g., humanoid-to-humanoid).
</details>

---

### Vista4D: Video Reshooting with 4D Point Clouds
著者: Kuan Heng Lin, Zhizheng Liu, Pablo Salamanca, Yash Kant, Ryan Burgert, Yuancheng Xu, Koichi Namekata, Yiwei Zhao, Bolei Zhou, Micah Goldblum, Paul Debevec, Ning Yu

<details>
<summary> 日本語要旨 </summary>

私たちは、入力ビデオとターゲットカメラを4次元ポイントクラウドに基づいて配置する堅牢で柔軟な動画再撮影フレームワーク **Vista4D** を提案します。具体的には、入力ビデオが与えられた場合、私たちの方法は異なるカメラトラジェクションと視点から同じダイナミクスを持つシーンを再構成します。既存の動画再撮影手法は、実世界の動的ビデオにおける深度推定アーティファクトに苦しみ、また挑戦的な新しいトラジェクションでコンテンツの外観を保持したり正確なカメラ制御を維持することができません。私たちは静止画像セグメンテーションと4D再構成による4次元基盤のポイントクラウド表現を構築し、見えたコンテンツを明示的に保持し豊富なカメラ信号を提供します。また、実世界推論時のポイントクラウドアーティファクトに対する堅牢性を向上させるために、再構成されたマルチビュー動的データで学習します。私たちの結果は、多種多様なビデオとカメラパスにおいて4次元一貫性、カメラ制御、視覚品質が最先端のベースラインを上回ることを示しています。さらに、私たちの方法は動的シーン拡張や4Dシーン再構成などの実世界アプリケーションへも一般化します。結果は補足資料にあるビデオで最適にご覧いただけます。
</details>

<details>
<summary> 英語要旨 </summary>

We present **Vista4D**, a robust and flexible video reshooting framework that grounds the input video and target cameras in a 4D point cloud. Specifically, given an input video, our method re-synthesizes the scene with the same dynamics from a different camera trajectory and viewpoint. Existing video reshooting methods often struggle with depth estimation artifacts of real-world dynamic videos, while also failing to preserve content appearance and maintain precise camera control for challenging new trajectories. We build a 4D-grounded point cloud representation with static pixel segmentation and 4D reconstruction to explicitly preserve seen content and provide rich camera signals, and we train with reconstructed multiview dynamic data for robustness against point cloud artifacts during real-world inference. Our results demonstrate improved 4D consistency, camera control, and visual quality compared to state-of-the-art baselines under a variety of videos and camera paths. Moreover, our method generalizes to real-world applications such as dynamic scene expansion and 4D scene recomposition. Results are best viewed as videos in the Supplement.
</details>

---

### OpenMMReasoner: Pushing The Frontiers in Multimodal Reasoning with An Open and General Recipe
著者: Kaichen Zhang, Keming Wu, Zuhao Yang, Bo Li, Kairui Hu, Bin Wang, Xingxuan Li, Lidong Bing

<details>
<summary> 日本語要旨 </summary>

最近の推論言語モデルの進歩は、その能力をマルチモーダル領域に拡張することへの関心を高めています。しかし、視覚的およびビデオ推論における顕著な進歩にもかかわらず、透明性や再現可能性に欠けるデータのキュレーションとトレーニングパイプラインがスケーラブルな研究の大きな障壁となっています。本研究では、マルチモーダル推論を対象とした完全に透明な二段階のレシピであるOpenMMReasonerを紹介します。このレシピは、監督付き微調整（SFT）および強化学習（RL）から構成されています。SFTステージでは、厳密なステップバイステップの検証を行った874kサンプルのデータセットを構築し、推論能力の強固な基盤を提供します。その後のRLステージでは、多様なドメインにわたる74kサンプルのデータセットを活用してこれらの能力をさらに磨き上げ、安定化し、より堅牢で効率的な学習プロセスを実現します。広範囲な評価では、私たちのトレーニングレシピが強力なベースラインを上回るだけでなく、データ品質とトレーニング設計がマルチモーダル推論パフォーマンスに与える重要な役割を浮き彫りにしています。特筆すべきことに、私たちの方法はQwen2.5-VL-7B-Instructベースラインに対し9.5%の改善を達成し、9つのマルチモーダル推論ベンチマークでその実績を確立しています。これは、将来の大規模なマルチモーダル推論研究における堅固な経験的基盤を形成します。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advancements in reasoning language models have fueled growing interest in extending such capabilities to multimodal domains. However, despite notable progress in visual and video reasoning, the lack of transparent and reproducible data curation and training pipelines remains a major barrier to scalable research. In this work, we introduce OpenMMReasoner, a fully transparent two-stage recipe for multimodal reasoning spanning supervised fine-tuning (SFT) and reinforcement learning (RL). In the SFT stage, we construct an 874k-sample cold-start dataset with rigorous step-by-step validation, providing a strong foundation for reasoning capabilities. The subsequent RL stage leverages a 74k-sample dataset across diverse domains to further sharpen and stabilize these abilities, resulting in a more robust and efficient learning process. Extensive evaluations demonstrate that our training recipe not only surpasses strong baselines but also highlights the critical role of data quality and training design in shaping multimodal reasoning performance. Notably, our method achieves a 9.5\% improvement over the Qwen2.5-VL-7B-Instruct baseline across nine multimodal reasoning benchmarks, establishing a solid empirical foundation for future large-scale multimodal reasoning research.
</details>

---

### Transition Matching Distillation for Fast Video Generation
著者: Weili Nie, Julius Berner, Nanye Ma, Chao Liu, Saining Xie, Arash Vahdat

<details>
<summary> 日本語要旨 </summary>

大規模なビデオ拡散モデルとフローモデルは、高品質のビデオ生成において顕著な成功を収めていますが、その効率的でないマルチステップサンプリングプロセスのため、リアルタイムインタラクティブアプリケーションへの応用は限られています。本研究では、効率的なフェイズ生成器にビデオ拡散モデルを蒸留するための新しいフレームワークであるTransition Matching Distillation（TMD）を提案します。TMDの中心的なアイデアは、各トランジションが軽量な条件付きフローとしてモデル化された少数ステップの確率遷移プロセスに、拡散モデルのマルチステップ除雑トレジャリを一致させることです。効率的な蒸留を可能にするために、元の拡散バックボーンを以下の2つのコンポーネントに分解します：（1）主要なバックボーンであり、初期層の大部分から構成され、各外側トランジションステップで意味的表現を抽出するもの；および（2）フローヘッドであり、最後の数層からなり、これらの表現を活用して複数の内側フローアップデートを実行します。予め学習されたビデオフローモデルが与えられた場合、まずモデルにフローヘッドを導入し、それを条件付きフロー図として適応させます。次に、各トランジションステップでのフローヘッド展開を伴う学習モデルに対して分布マッチング蒸留を適用します。Wan2.1 1.3Bおよび14Bのテキストからビデオへのモデルを蒸留する広範な実験により、TMDが生成速度と視覚品質の間で柔軟かつ強力なトレードオフを提供することが示されました。特に、TMDは同等の推論コスト下で既存の蒸留モデルを視覚的忠実性およびプロンプト遵守の面で上回ります。
</details>

<details>
<summary> 英語要旨 </summary>

Large video diffusion and flow models have achieved remarkable success in high-quality video generation, but their use in real-time interactive applications remains limited due to their inefficient multi-step sampling process. In this work, we present Transition Matching Distillation (TMD), a novel framework for distilling video diffusion models into efficient few-step generators. The central idea of TMD is to match the multi-step denoising trajectory of a diffusion model with a few-step probability transition process, where each transition is modeled as a lightweight conditional flow. To enable efficient distillation, we decompose the original diffusion backbone into two components: (1) a main backbone, comprising the majority of early layers, that extracts semantic representations at each outer transition step; and (2) a flow head, consisting of the last few layers, that leverages these representations to perform multiple inner flow updates. Given a pretrained video flow model, we first introduce a flow head to the model, and adapt it into a conditional flow map. We then apply distribution matching distillation to the student model with flow head rollout in each transition step. Extensive experiments on distilling Wan2.1 1.3B and 14B text-to-video models demonstrate that TMD provides a flexible and strong trade-off between generation speed and visual quality. In particular, TMD outperforms existing distilled models under comparable inference costs in terms of visual fidelity and prompt adherence.
</details>

---

### EVATok: Adaptive Length Video Tokenization for Efficient Visual Autoregressive Generation
著者: Tianwei Xiong, Jun Hao Liew, Zilong Huang, Zhijie Lin, Jiashi Feng, Xihui Liu

<details>
<summary> 日本語要旨 </summary>

自己回帰型（AR）ビデオ生成モデルは、ピクセルを離散的なトークンシーケンスに圧縮するビデオトークナイザーに依存しています。これらのトークンシーケンスの長さは、再構成品質と下流生成の計算コストをバランスさせるために重要です。従来のビデオトークナイザーは、異なる動画の時間的ブロックに均一なトークン割り当てを適用し、しばしば単純で静的または繰り返しのあるセグメントにトークンが無駄になり、動的または複雑なセグメントが不十分にサービスされます。この非効率性を解決するために、私たちは**EVATok**というフレームワークを導入しました。これは**E**fficient **V**ideo **A**daptive **Tok**enizers（効率的なビデオ適応トークナイザー）を生成するものです。このフレームワークは、各動画に対して最適なトークン割り当てを推定し、品質とコストのトレードオフを最大化します。また、これらの最適な割り当てを迅速に予測するための軽量ルーターを開発し、ルーターが予測した割り当てに基づいて動画をエンコードする適応トークナイザーを訓練します。EVATokは、ビデオ再構成と下流AR生成の効率性および全体的な品質に大幅な改善をもたらすことを示しました。私たちの進化した訓練レシピがビデオセマンティックエンコーダーを統合することで強化され、EVATokはUCF-101において優れた再構成能力と最先端のクラスから動画生成を達成しました。これは、従来の最先端技術であるLARPや固定長ベースラインと比較してトークン使用量が少なくとも24.4％削減されています。
</details>

<details>
<summary> 英語要旨 </summary>

Autoregressive (AR) video generative models rely on video tokenizers that compress pixels into discrete token sequences. The length of these token sequences is crucial for balancing reconstruction quality against downstream generation computational cost. Traditional video tokenizers apply a uniform token assignment across temporal blocks of different videos, often wasting tokens on simple, static, or repetitive segments while underserving dynamic or complex ones. To address this inefficiency, we introduce **EVATok**, a framework to produce **E**fficient **V**ideo **A**daptive **Tok**enizers. Our framework estimates optimal token assignments for each video to achieve the best quality-cost trade-off, develops lightweight routers for fast prediction of these optimal assignments, and trains adaptive tokenizers that encode videos based on the assignments predicted by routers. We demonstrate that EVATok delivers substantial improvements in efficiency and overall quality for video reconstruction and downstream AR generation. Enhanced by our advanced training recipe that integrates video semantic encoders, EVATok achieves superior reconstruction and state-of-the-art class-to-video generation on UCF-101, with at least 24.4\% savings in average token usage compared to the prior state-of-the-art LARP and our fixed-length baseline.
</details>

---

### WiseEdit: Benchmarking Cognition- and Creativity-Informed Image Editing
著者: Kaihang Pan, Weile Chen, Haiyi Qiu, Qifan Yu, Wendong Bu, zehan wang, Yun Zhu, Juncheng Li, Siliang Tang

<details>
<summary> 日本語要旨 </summary>

最近の画像編集モデルは、認知や創造性に基づいた高度な能力を備えており、それらを支援しています。しかし、既存のベンチマークは評価範囲が狭すぎ、これらの先進的な能力を包括的に評価することに失敗しています。この問題に対処するため、私たちはWiseEditを導入します。これは認知や創造性に基づいた画像編集の包括的な評価のための知識集約型ベンチマークであり、深いタスクの深さと広範な知識の幅を特徴としています。人間の認知創造に例えると、WiseEditは画像編集を三段階に分解します：Awareness（意識）、Interpretation（解釈）、Imagination（想像力）。それぞれのステップに対応するタスクがあり、モデルがその特定のステップで完了することを難しくしています。また、WiseEditはいずれの三つのステップも容易に終わらせることができない複雑なタスクも含んでいます。さらに、WiseEditは三種類の基本的な知識を取り入れています：宣言的知識、手続き的知識、メタ認知知識です。最終的に、WiseEditは1,220のテストケースから構成され、SoTA画像編集モデルが知識に基づく認知推論や創造的な構成能力において持つ限界を客観的に明らかにします。
</details>

<details>
<summary> 英語要旨 </summary>

Recent image editing models boast next-level intelligent capabilities, facilitating cognition- and creativity-informed image editing. Yet, existing benchmarks provide too narrow a scope for evaluation, failing to holistically assess these advanced abilities. To address this, we introduce WiseEdit, a knowledge-intensive benchmark for comprehensive evaluation of cognition- and creativity-informed image editing, featuring deep task depth and broad knowledge breadth. Drawing an analogy to human cognitive creation, WiseEdit decomposes image editing into three cascaded steps—Awareness, Interpretation, and Imagination—each corresponding to a task that poses a challenge for models to complete at the specific step. It also encompasses complex tasks, where none of the three steps can be finished easily. Furthermore, WiseEdit incorporates three fundamental types of knowledge: Declarative, Procedural, and Metacognitive knowledge. Ultimately, WiseEdit comprises 1,220 test cases, objectively revealing the limitations of SoTA image editing models in knowledge-based cognitive reasoning and creative composition capabilities.
</details>

---

### BinaryAttention: One-Bit Attention for Vision and Diffusion Transformers
著者: Chaodong XIAO, Zhengqiang ZHANG, Lei Zhang

<details>
<summary> 日本語要旨 </summary>

トランスフォーマーは広範囲で顕著な成功を収めていますが、その注意モジュールの計算複雑性はビジョンタスクにおける主要なボトルネックとなっています。既存の方法では、効率と精度をバランスさせるために8ビットまたは4ビットの量子化が主に用いられています。本論文では理論的根拠を示し、注意の二値化が重要な類似関係を保持することを指摘し、高速かつ正確な1ビット注意の有効な方法であるBinaryAttentionを提案します。具体的には、クエリーとキーの符号のみを保持して注意を計算し、浮動小数点のドット積をビット単位の演算に置き換えることで、計算コストを大幅に削減します。1ビット量子化下での固有の情報損失を補うために学習可能なバイアスを導入し、エンドツーエンドの加速を実現します。注意の精度を保つために量子化認識訓練と自己教師付き技術を採用し、量子化誤差を軽減しながら符号一致した類似性を確保します。BinaryAttentionはA100 GPU上でFlashAttention2の約2倍速いことが示されています。ビジョントランスフォーマーおよびディフュージョントランスフォーマーのベンチマークにおける広範な実験では、BinaryAttentionが全精度注意と同等またはそれを超えることを示し、その有効性を検証しています。本研究はビジョンタスクにおける低ビットトランスフォーマーの最前線を押し進める、高度に効率的かつ有効な全精度注意への代替手段を提供します。コードとモデルは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Transformers have achieved widespread and remarkable success, while the computational complexity of their attention modules remains a major bottleneck for vision tasks. Existing methods mainly employ 8-bit or 4-bit quantization to balance efficiency and accuracy. In this paper, with theoretical justification, we indicate that binarization of attention preserves the essential similarity relationships, and propose BinaryAttention, an effective method for fast and accurate 1-bit attention. Specifically, we retain only the sign of queries and keys in computing the attention, and replace the floating dot products with bit-wise operations, significantly reducing the computational cost. We mitigate the inherent information loss under 1-bit quantization by incorporating a learnable bias, and enable end-to-end acceleration. To maintain the accuracy of attention, we adopt quantization-aware training and self-distillation techniques, mitigating quantization errors while ensuring sign-aligned similarity. BinaryAttention is more than 2$\times$ faster than FlashAttention2 on A100 GPUs. Extensive experiments on vision transformer and diffusion transformer benchmarks demonstrate that BinaryAttention matches or even exceeds full-precision attention, validating its effectiveness. Our work provides a highly efficient and effective alternative to full-precision attention, pushing the frontier of low-bit transformers for vision tasks. The codes and models will be made publicly available.
</details>

---

### ViT$^3$: Unlocking Test-Time Training in Vision
著者: Dongchen Han, Yining Li, Tianyu Li, Zixuan Cao, Ziming Wang, Jun Song, YuCheng YuCheng, Bo Zheng, Gao Huang

<details>
<summary> 日本語要旨 </summary>

最近、効率的なシーケンスモデリングの有望な方向としてテストタイムトレーニング（TTT）が注目されています。TTTは注意操作をオンライン学習問題として再定式化し、キー・バリューペアからテスト時にコンパクトな内部モデルを構築します。この再定式化により、豊かで柔軟な設計空間が開かれつつ、線形の計算複雑性が達成されます。しかし、強力な視覚的TTTデザインを構築することは依然として課題です：内部モジュールや内部トレーニングの基本的な選択について、包括的な理解や実用的なガイドラインが不足しています。この重要なギャップを埋めるために、本論文では視覚シーケンスモデリングのTTT設計に関する体系的な実験研究を提示します。一連の実験と分析から、効果的な視覚的TTTのための6つの実践的洞察が導き出され、設計原則が確立され、将来の改善への道筋が明らかにされます。これらの成果はVision Test-Time Training（ViT$^3$）モデルとして結実し、純粋なTTTアーキテクチャで線形複雑性と並列計算を達成します。ViT$^3$は画像分類、画像生成、物体検出、セマンティックセグメンテーションなど多様な視覚タスクで評価されました。結果は、ViT$^3$がMambaや線形注意のバリエーションなどの先進的な線形複雑性モデルと一貫して匹敵またはそれを上回り、最適化されたビジョントランスフォーマーとのギャップを効果的に埋めることを示しました。この研究とViT$^3$ベースラインが将来の視覚TTTモデルの開発を促進することを期待しています。コードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Test-Time Training (TTT) has recently emerged as a promising direction for efficient sequence modeling. TTT reformulates attention operation as an online learning problem, constructing a compact inner model from key–value pairs at test time. This reformulation opens a rich and flexible design space while achieving linear computational complexity. However, crafting a powerful visual TTT design remains challenging: fundamental choices for the inner module and inner training lack comprehensive understanding and practical guidelines. To bridge this critical gap, in this paper, we present a systematic empirical study of TTT designs for visual sequence modeling. From a series of experiments and analyses, we distill six practical insights that establish design principles for effective visual TTT and illuminate paths for future improvement. These findings culminate in the Vision Test-Time Training (ViT$^3$) model, a pure TTT architecture that achieves linear complexity and parallelizable computation. We evaluate ViT$^3$ across diverse visual tasks, including image classification, image generation, object detection, and semantic segmentation. Results show that ViT$^3$ consistently matches or outperforms advanced linear-complexity models (e.g., Mamba and linear attention variants) and effectively narrows the gap to highly optimized vision Transformers. We hope this study and the ViT$^3$ baseline can facilitate future work on visual TTT models. Code will be released.
</details>

---

### PinPoint: Evaluation of Composed Image Retrieval with Explicit Negatives, Multi-Image Queries, and Paraphrase Testing
著者: Rohan Mahadev, Joyce Yuan, Patrick Poirson, David Xue, Hao-Yu Wu, Dmitry Kislyuk

<details>
<summary> 日本語要旨 </summary>

合成画像検索（CIR）は大きな進歩を遂げていますが、現在のベンチマークは単一の正解に限定され、誤検出回避、堅牢性、および複数画像推論の評価に必要な注釈が不足しています。私たちは、実際の世界で使用可能な包括的なベンチマーク **PinPoint** を提案します。これは23のクエリカテゴリーにわたる7,846のクエリと329Kの関連判断を含んでいます。PinPoint は以下の点で分野を進展させます：(1) 複数の正解（平均9.1件/クエリ） (2) 明示的な難しいネガティブ例、(3) クエリごとに6つの指示文のパラフレーズを提供して堅牢性テスト、(4) 複数画像構成のサポート（クエリの13.4％）、および (5) 公平性評価のための人口統計メタデータ。私たちの分析によると、20以上の方法を含む4つの主要なパラダイムで、3つの重大な欠点が明らかになりました：最良の手法はmAP@10 28.5％を達成していますが、難しいネガティブ例（関連性のない結果）を9％の頻度で取得します。最良のモデルも、パラフレーズ間で25.1％のパフォーマンス変動を示し、現在のCIR技術における大きな改善ポテンシャルがあることを示しています。複数画像クエリは、異なる方法で40〜70％悪化します。これらの新たに明らかにされた問題を克服するために、私たちは既存システムに適用可能なトレーニングフリーの再ランキング方法を提案します。この方法はオフ・ザ・シェルフのMLLM（多言語大規模モデル）に基づいています。これにより、既存の手法とのギャップを埋めることができます。私たちはすべての画像、クエリ、注釈、検索インデックス、およびベンチマークコードを含む完全なデータセットを公開します。
</details>

<details>
<summary> 英語要旨 </summary>

Composed Image Retrieval (CIR) has made significant progress, yet current benchmarks are limited to single ground-truth answers and lack the annotations needed to evaluate false positive avoidance, robustness and multi-image reasoning. We present \textbf{PinPoint}, a comprehensive real world benchmark with 7,846 queries and 329K relevance judgments across 23 query categories. PinPoint advances the field by providing: (1) multiple correct answers (averaging 9.1 per query) (2) explicit hard negatives, (3) six instruction paraphrases per query for robustness testing, (4) multi-image composition support (13.4\% of queries), and (5) demographic metadata for fairness evaluation. Based on our analysis of 20+ methods across 4 different major paradigms, we uncover three significant drawbacks: The best methods while achieving mAP@10 of 28.5\%, still retrieves irrelevant results (hard negatives) 9\% of the time. The best models also exhibit 25.1\% performance variation across paraphrases, indicating significant potential for enhancing current CIR techniques. Multi-image queries performs 40 to 70\% worse across different methods. To overcome these new issues uncovered by our evaluation framework, we propose a training-free reranking method based on an off-the-shelf MLLM that can be applied to any existing system to bridge the gap. We release the complete dataset, including all images, queries, annotations, retrieval index, and benchmarking code.
</details>

---

### DNF-SR: Dual-Input and Negative-Aware Feature Fine-Tuning for Real-World Image Super-Resolution
著者: Shuhao Han, Wenjie Liao, Haotian Fan, Hang Dong, Rui Zhang, Chun-Le Guo, Chongyi Li

<details>
<summary> 日本語要旨 </summary>

ディフュージョンモデルの強力な生成的事前知識を活用することで、リアル世界画像超解像（Real-ISR）手法は印象的な性能を示しています。効率的なReal-ISRを達成するために、最近のいくつかの研究では一段階ディフュージョンベースモデルを設計しました。しかし、LR画像を直接ディフュージョンモデルに供給すると、モデルの元々の入力との分布的なギャップが生じます。この分布的ギャップを減少させるための直接的なアプローチは、LRラテンスにノイズを導入することです。しかし、直接ノイズを追加すると、LR画像のコンテンツが必然的に損なわれます。本研究では、リアルISR用の**DNF‑SR**、すなわち**D**ual‑inputと**N**egative‑aware **F**eature fine-tuning方法を提案します。具体的には、元のLR画像とノイズ付きLR入力を連結し、ディフュージョンベースの画像編集モデルに供給する**ダブルインプット戦略**を使用します。これにより、高精細な一段階超解像と改善された知覚およびコンテンツの一貫性が確保されます。また、ノイズ付きLR入力に存在するノイズは出力にランダム性と多様性を導入します。この特性を利用し、出力品質を向上させるための後期トレーニング最適化方法であるNegative-aware Feature Fine-Tuning（NF²T）を提案します。NF$^2$Tは複数の出力を正と負のサブセットに分類し、画像空間および特徴空間の両方で暗黙的なポリシー改善方向を定義することで、最適化の安定性をさらに高めます。広範囲の実験結果はDNF-SRが他の方法を上回ることを示しています。コードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Benefiting from the powerful generative priors of diffusion models, diffusion-based real-world image super-resolution (Real-ISR) methods have demonstrated impressive performance. To achieve efficient Real-ISR, several recent works have designed one-step diffusion-based models. Howerver, unmediatedly feeding LR into a diffusion model creates a distributional gap with the model's original input. A straightforward approach to reduce the distribution gap is to introduce noise to the LR latents. However, directly adding noise inevitably corrupts the content of the LR images. In this study, we propose \textbf{DNF‑SR}, a \textbf{D}ual‑input and \textbf{N}egative‑aware \textbf{F}eature fine‑tuning method for Real-ISR. Specifically, we use a \textbf{dual-input} strategy that concatenates the original LR image with the noisy LR input and feeds them into a diffusion-based image editing model, ensuring both high-fidelity one-step super-resolution and improved perceptual and content consistency. Additionally, the noise present in the noisy LR input introduces randomness and diversity into the outputs. We exploit this property and propose a post-training optimization method, Negative-aware Feature Fine-Tuning (NF²T), which guides the model toward producing higher-quality results. NF$^2$T classifies multiple outputs into positive and negative subsets and then defines implicit policy improvement directions in both the image and feature spaces, thereby further enhancing the stability of the optimization. Extensive experiments show that DNF-SR outperforms other methods. Code will be released.
</details>

---

### MiniCPM-V 4.5: Cooking Efficient MLLMs Via Architecture, Data, and Training Recipe
著者: Tianyu Yu, Zefan Wang, Chongyi Wang, Fuwei Huang, Wenshuo Ma, Zhihui He, Tianchi Cai, Weize Chen, Yuxiang Huang, Ranchi Zhao, Bokai Xu, Junbo Cui, Yingjing Xu, Liqing Ruan, Luoyuan Zhang, Hanyu Liu, Jingkun Tang, Hongyuan Liu, Qining Guo, Wenhao Hu, Bingxiang He, Jie Zhou, Jie Cai, Ji Qi, Zonghao Guo, Chi Chen, Guoyang Zeng, Yuxuan Li, Ganqu Cui, Ning Ding, Xu Han, Yuan Yao, Zhiyuan Liu, Maosong Sun

<details>
<summary> 日本語要旨 </summary>

多モーダル大規模言語モデル（MLLMs）は急速に進化し、AI開発の最前線を代表しています。しかし、そのトレーニングと推論効率がアクセス性や拡張性を向上させるための主要なボトルネックとして浮上しています。これらの課題に対処するため、高い効率と優れたパフォーマンスを実現する8BパラメーターのモデルであるMiniCPM-V 4.5を提案します。モデルアーキテクチャ、データ戦略、トレーニング方法における3つの主要な改善点を紹介します：画像とビデオの高度にコンパクトなエンコード用の統一された3D-Resamplerモデルアーキテクチャ、重いデータエンジニアリングなしでドキュメント知識とテキスト認識に対する統一学習パラダイム、そして短期および長期の推論モードの両方での熟達度を持つハイブリッド強化学習戦略。OpenCompass評価における包括的な実験結果は、MiniCPM-V 4.5が広く使用されているプロプライエタリモデルであるGPT-4o-latestや、より大きなオープンソースモデルであるQwen2.5-VL 72Bを上回っていることを示しています。特に、優れたパフォーマンスは顕著な効率性で達成されています。例えば、広く採用されているVideoMMEベンチマークでは、MiniCPM-V 4.5が30B未満のサイズのモデルの中で最先端のパフォーマンスを達成し、Qwen2.5-VL 7BのGPUメモリコスト46.7％および推論時間8.7％で実現しています。
</details>

<details>
<summary> 英語要旨 </summary>

Multimodal Large Language Models (MLLMs) are undergoing rapid progress and represent the frontier of AI development. However, their training and inference efficiency have emerged as a core bottleneck in making MLLMs more accessible and scalable. To address the challenges, we present MiniCPM-V 4.5, an 8B parameter model designed for high efficiency and strong performance. We introduce three core improvements in model architecture, data strategy and training method: a unified 3D-Resampler model architecture for highly compact encoding over images and videos, a unified learning paradigm for document knowledge and text recognition without heavy data engineering, and a hybrid reinforcement learning strategy for proficiency in both short and long reasoning modes. Comprehensive experimental results in OpenCompass evaluation show that MiniCPM-V 4.5 surpasses widely used proprietary models such as GPT-4o-latest, and significantly larger open-source models such as Qwen2.5-VL 72B. Notably, the strong performance is achieved with remarkable efficiency. For example, on the widely adopted VideoMME benchmark, MiniCPM-V 4.5 achieves state-of-the-art performance among models under 30B size, using just 46.7\% GPU memory cost and 8.7\% inference time of Qwen2.5-VL 7B.
</details>

---

### Self-Consistency for LLM-based Motion Trajectory Generation and Verification
著者: Jiaju Ma, R. Kenny Jones, Jiajun Wu, Maneesh Agrawala

<details>
<summary> 日本語要旨 </summary>

自己整合性は、軽量で非監督的な方法で言語モデルの自然言語推理タスクにおけるパフォーマンスを向上させる効果的な技術として証明されています。本研究では、この自己整合性を視覚領域に適応する方法を検討します。具体的には、言語モデル（LLM）が生成した動きのグラフィックストラジェクトリの生成と検証を考えます。例えば、「円を螺旋状のパスで移動させる」というプロンプトに対して、まず多様な動きのストラジェクトリをLLMからサンプリングし、その後クラスタリングを通じて一貫したストラジェクトリ群を特定します。私たちの重要な洞察は、プロンプトに関連する形状ファミリーを、変換群（例えば剛体、類似、アフィン）とペアになったプロトタイプストラジェクトリとしてモデル化することです。この場合、2つのストラジェクトリは、変換群が許す歪みの下で一方を他方に変形できるならば、一貫性があると考えられます。私たちは、候補となる変換群間の階層的関係を用いて自動的に形状ファミリーを回復するアルゴリズムを提案します。このアプローチは、LLMベースのストラジェクトリ生成の精度を4～6％向上させます。また、私たちは方法論を拡張し、検証にも対応できるようにしました。これにより、VLMベースラインと比較して11％の精度向上が観測されました。
</details>

<details>
<summary> 英語要旨 </summary>

Self-consistency has proven to be an effective technique for improving LLM performance on natural language reasoning tasks in a lightweight, unsupervised manner. In this work, we study how to adapt self-consistency to visual domains; specifically, we consider the generation and verification of LLM-produced motion graphics trajectories. Given a prompt (e.g., ``Move the circle in a spiral path''), we first sample diverse motion trajectories from an LLM, and then identify groups of consistent trajectories via clustering. Our key insight is to model the family of shapes associated with a prompt as a prototype trajectory paired with a group of geometric transformations (e.g., rigid, similarity, affine). Two trajectories can then be considered consistent if one can be transformed into the other under the warps allowable by the transformation group. We propose an algorithm that automatically recovers a shape family, using hierarchical relationships between a set of candidate transformation groups. Our approach improves the accuracy of LLM-based trajectory generation by 4–6\%. We further extend our method to support verification, observing 11\% precision gains over VLM baselines.
</details>

---

### UnityVideo: Unified Multi-Modal Multi-Task Learning for Enhancing World-Aware Video Generation
著者: Jiehui Huang, Yuechen Zhang, Xu He, Yuan Gao, Zhi Cen, Bin Xia, Yan Zhou, Xin Tao, Pengfei Wan, Jiaya Jia

<details>
<summary> 日本語要旨 </summary>

最近のビデオ生成モデルは印象的な合成能力を示していますが、シングルモダリティ条件付けによって制約されており、包括的な世界理解が限られています。これは十分でないクロスモーダル相互作用と、包括的な世界知識表現のための限定的なモダリティ多様性に起因しています。この制約を解決するために、私たちは複数のモダリティ（セグメンテーションマスク、人間骨格、DensePose、光流、深度マップ）とトレーニングパラダイムを共同で学習する世界認識ビデオ生成のための統一フレームワーク「UnityVideo」を導入します。私たちのアプローチは、2つの主要なコンポーネントで構成されています：（1）異種トレーニングパラダイムを統一する動的ノイジング、および（2）モジュールパラメータと文脈学習による統一処理を可能にするモダリティスイッチャーとインコンテキストラーナー。私たちは、1,300万サンプルの大規模な統一データセットを提供します。共同最適化により、UnityVideoは収束速度を加速し、未見データへのゼロショット一般化能力を顕著に向上させます。私たちは、UnityVideoがビデオ品質と一貫性を向上させ、物理世界の制約との整合性も改善していることを示します。コードとモデルはリリースされます。詳細な結果は補足資料でご覧いただけます。
</details>

<details>
<summary> 英語要旨 </summary>

Recent video generation models demonstrate impressive synthesis capabilities but remain limited by single-modality conditioning, constraining their holistic world understanding. This stems from insufficient cross-modal interaction and limited modal diversity for comprehensive world knowledge representation. To address these limitations, we introduce UnityVideo, a unified framework for world-aware video generation that jointly learns across multiple modalities—segmentation masks, human skeletons, DensePose, optical flow, and depth maps—and training paradigms. Our approach features two core components: (1) dynamic noising to unify heterogeneous training paradigms, and (2) a modality switcher with an in-context learner that enables unified processing via modular parameters and contextual learning. We contribute a large-scale unified dataset with 1.3M samples. Through joint optimization, UnityVideo accelerates convergence and significantly enhances zero-shot generalization to unseen data. We demonstrate that UnityVideo achieves superior video quality, consistency, and improved alignment with physical world constraints. Code and models will be released. More results can be viewed in the supplementary.
</details>

---

### ArchSym: Detecting 3D-Grounded Architectural Symmetries in The Wild
著者: Hanyu Chen, Ruojin Cai, Steve Marschner, Noah Snavely

<details>
<summary> 日本語要旨 </summary>

コンピュータビジョンにおける対称性検出は基本的な問題であり、対称性は下流タスクの強力な事前情報として機能します。しかし、既存の学習ベースの方法は、主にオブジェクト中心または合成データセットで訓練および評価されているため、実世界のシーンに一般化することができません。さらに、モノクロ入力の固有のスケール曖昧性は3D平面を局在化する問題を不適切なものにし、多くの既存の研究では平面の方向のみを予測しています。本論文では、これらの制限に対処するために、単一の野外RGB画像から*3Dグラウンドされた反射的対称性*を検出する最初のフレームワークを提示します。これは建築ランドマークに焦点を当てています。私たちは2つの重要な革新を紹介します：(1) 画像間のクロスビューマッチングを活用してSfM再構成から大規模な建築対称性データセットであるArchSymを自動的にキュレートする、スケーラブルなデータアノテーションパイプライン；そしてそのデータセットに基づいて(2) 予測されたシーンジオメトリに対して相対的に定義された符号付き距離マップとしてパラメータ化される3Dで対称性を正確に局在化する単一ビューの対称性検出器。私たちは、ジオメトリベースの代替手法と比較して私たちの対称性アノテーションパイプラインを検証し、新しいベンチマークでの最先端のベースラインに対して私たちの対称性検出器が大幅に優れていることを示します。
</details>

<details>
<summary> 英語要旨 </summary>

Symmetry detection is a fundamental problem in computer vision, and symmetries serve as powerful priors for downstream tasks. However, existing learning-based methods for detecting 3D symmetries from single images have been almost exclusively trained and evaluated on object-centric or synthetic datasets, and thus fail to generalize to real-world scenes. Furthermore, due to the inherent scale ambiguity of monocular inputs, which makes localizing the 3D plane an ill-posed problem, many existing works only predict the plane's orientation. In this paper, we address these limitations by presenting the first framework for detecting *3D-grounded reflectional symmetries* from single, in-the-wild RGB images, focusing on architectural landmarks. We introduce two key innovations: (1) a scalable data annotation pipeline to automatically curate a large-scale dataset of architectural symmetries, ArchSym, from SfM reconstructions by leveraging cross-view image matching; and building on the dataset, (2) a single-view symmetry detector that accurately localizes symmetries in 3D by parameterizing them as signed distance maps defined relative to predicted scene geometry. We validate our symmetry annotation pipeline against geometry-based alternatives and demonstrate that our symmetry detector significantly outperforms state-of-the-art baselines on our new benchmark.
</details>

---

### Learning 3D Representations for Spatial Intelligence from Unposed Multi-View Images
著者: bo zhou, Qiuxia Lai, Zeren Sun, Xiangbo Shu, Yazhou Yao, Wenguan Wang

<details>
<summary> 日本語要旨 </summary>

堅牢な3次元表現学習は、空間知性の感覚的基盤を形成し、シーン理解やエンボディAIにおける下流タスクを可能にします。しかし、ポーズされていないマルチビュー画像から直接そのような表現を学習することは依然として困難です。最近の自己教師付け手法は幾何学、外観、意味をフィードフォワード方式で統一しようと試みていますが、しばしば弱い幾何学誘導、限定された外観の詳細、および幾何学と意味の不整合に苦しんでいます。私たちはこれらの制限を克服するためにフィードフォワードフレームワーク$\textbf{\textit{UniSplat}}$を導入します。このフレームワークは三つの補完的なコンポーネントで構成されています。まず、エンコーダーにおける幾何学誘導を強化する$\textit{dual-masking strategy}$（デュアルマスキング戦略）を提案します。エンコーダーとデコーダーのトークンを両方マスクし、幾何学情報が豊富な領域に向けてデコーダーのマスクを設定することで、モデルは不完全な視覚的手掛かりから構造情報を推測させ、ポーズされていない入力でも幾何学に対応した表現が得られるようにします。次に、外観と意味の不整合を軽減するために$\textit{coarse-to-fine Gaussian splatting strategy}$（粗いから細かいガウス分布スプラッティング戦略）を開発し、放射場を逐次的に洗練します。最後に、幾何学と意味の一貫性を強制するために$\textit{pose-conditioned recalibration mechanism}$（ポーズ条件付き再調整メカニズム）を導入し、複数ヘッドの出力を推定されたカメラパラメータを用いて画像平面に再投影した予測3次元点と意味マップを対応するRGBおよび意味予測と整合させ、クロスタスクの一貫性を確保し幾何学と意味の不一致を解決します。これらのコンポーネントが組み合わされることで、ポーズされていないスパースビュー入力に対しても堅牢であり、多様なタスクに一般化する統一的な3次元表現が得られ、空間知性の感覚的基盤を築きます。
</details>

<details>
<summary> 英語要旨 </summary>

Robust 3D representation learning forms the perceptual foundation of spatial intelligence, enabling downstream tasks in scene understanding and embodied AI. However, learning such representations directly from unposed multi-view images remains challenging. Recent self-supervised methods attempt to unify geometry, appearance, and semantics in a feed-forward manner, but they often suffer from weak geometry induction, limited appearance detail, and inconsistencies between geometry and semantics. We introduce $\textbf{\textit{UniSplat}}$, a feed-forward framework designed to address these limitations through three complementary components. First, we propose a $\textit{dual-masking strategy}$ that strengthens geometry induction in the encoder. By masking both encoder and decoder tokens, and targeting decoder masks toward geometry-rich regions, the model is forced to infer structural information from incomplete visual cues, yielding geometry-aware representations even under unposed inputs. Second, we develop a $\textit{coarse-to-fine Gaussian splatting strategy}$ that reduces appearance-semantics inconsistencies by progressively refining the radiance field. Finally, to enforce geometric–semantic consistency, we introduce a $\textit{pose-conditioned recalibration mechanism}$ that interrelates the outputs of multiple heads by reprojecting predicted 3D point and semantic maps into the image plane using estimated camera parameters, and aligning them with corresponding RGB and semantic predictions to ensure cross-task consistency and resolving geometry–semantic mismatches. Together, these components yield unified 3D representations that are robust to unposed, sparse-view inputs and generalize across diverse tasks, laying a perceptual foundation for spatial intelligence.
</details>

---

### InterPrior: A Scalable Motion Prior for Physics-Based Human-Object Interactions
著者: Sirui Xu, Samuel Schulter, Morteza Ziyadi, Xialin He, Xiaohan Fei, Yu-Xiong Wang, Liangyan Gui

<details>
<summary> 日本語要旨 </summary>

人間は、明示的な全身運動のレベルで物体との全身相互作用をほとんど計画しません。高次の意図、例えばアフォーダンスが目標を定義する一方で、バランス、接触、操作の調整は、基礎となる物理的および運動学的優先順位から自然に生じます。このような優先順位を拡張することが、ヒューマノイドが多様な文脈でロコマニピュレーションスキルを組み合わせて一般化し、物理的に整合した全身調整を維持する鍵となります。このために、我々はInterPriorという拡張可能なフレームワークを導入します。これは、大規模な模倣学習の事前トレーニングと強化学習による後処理を通じて、つまり相互作用運動優先順位として統一された制御ポリシーを学習します。InterPriorは最初に完全参照の模倣専門家から多様な、目標条件付き変分政策を抽出し、マルチモーダルおよび部分的に指定された目標手がかりから運動を再構築します。ターゲットとした多様性プロセスは、データ拡張と物理的な乱れの組み合わせによって、異なる接触およびオブジェクト条件への露出を広げ、訓練データを超えて一般化する運動優先順位を生み出します。大規模な人間と物体の相互作用の膨大な構成空間に対処するため、強化学習による微調整が未見の目標能力を向上させ、失敗した掴みからの回復を可能にします。結果として得られるポリシーは再利用可能な運動優先順位として機能し、新たな行動、特に未見のオブジェクトとの相互作用を吸収することができます。また、ユーザーインタラクティブ制御や異なるエンフォッシュメントにおけるその効果も示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Humans rarely plan whole-body interactions with objects at the level of explicit whole-body movements. High-level intentions, such as affordance, define the goal, while coordinated balance, contact, and manipulation can emerge naturally from underlying physical and motor priors. Scaling such priors is key to enabling humanoids to compose and generalize loco-manipulation skills across diverse contexts while maintaining physically coherent whole-body coordination. To this end, we introduce InterPrior, a scalable framework that learns a unified control policy, i.e., interaction motion prior through large-scale imitation pretraining and post-training by reinforcement learning. InterPrior first distills a full-reference imitation expert into a versatile, goal-conditioned variational policy that reconstructs motion from multi-modal and partially specified goal cues. A targeted diversity process, combining data augmentation and physical perturbations, broadens exposure to varied contact and object conditions, producing a motion prior that generalizes beyond the training data. To address the vast configuration space of large-scale human-object interaction, a reinforcement learning finetuning enhances unseen goal competence, enabling recovery from unsuccessful grasp. The resulting policy acts as a reusable motion prior that can absorb new behaviors, including interactions with unseen objects. We also show its effectiveness in user-interactive control and across different embodiments.
</details>

---

### LAMP: Localization Aware Multi-camera People Tracking in Metric 3D World
著者: Nan Yang, Julian Straub, Fan Zhang, Richard Newcombe, Jakob Engel, Lingni Ma

<details>
<summary> 日本語要旨 </summary>

エゴセントリックなマルチカメラデバイスからの3D人間動作追跡は、厳しい自己運動や部分的可視性または遮蔽によって挑戦されています。既存の方法は通常、静止またはゆっくりと移動するカメラで記録されたモノクルビデオ向けに設計されており、マルチビュー、キャリブレーション済みかつローカライズされた入力を容易に活用することができません。これにより、動的エゴセントリックな記録では簡単に失敗する可能性のある脆弱な方法となっています。私たちは、観察者とターゲットの運動を早期に分離することでこの問題を解決する新しい簡潔なフレームワーク「LAMP（**L**ocalization **A**ware **M**ulti-camera **P**eople Tracking）」を提案します。LAMPは、2段階のプロセスを導入しています：まず、デバイスの既知の6自由度ポーズとキャリブレーションを利用し、一定の時間窓内で全てのカメラから検出された2Dボディキーポイントを統一した3D世界座標系に変換します。次に、エンド・トゥ・エンドで学習されたTransformerモデルが、このスパースタイムライクな世界座標のレイクラウドに直接3D人間動作を適合させます。この「リフト・アンド・フィット」アプローチは、自然な世界空間での人間動作に対する優先順位を学習し活用することを可能にし、また複数の非同期的かつ部分的観測および移動カメラから情報を柔軟に統合するための優雅なフレームワークを提供します。LAMPは単眼ベンチマークで最先端の成果を達成し、特にエゴセントリックなマルチカメラ設定において基準となる手法を大幅に上回っています。
</details>

<details>
<summary> 英語要旨 </summary>

Tracking 3D human motion from egocentric, multi-camera devices is challenged by severe egomotion and partial visibility or occlusions. Existing methods are designed for monocular video often recorded from static or slowly-moving cameras and cannot easily leverage multi-view, calibrated and localized input. This makes them brittle and prone to fail on dynamic egocentric captures. We propose LAMP ($\textbf{L}$ocalization $\textbf{A}$ware $\textbf{M}$ulti-camera $\textbf{P}$eople Tracking): a novel, simple framework to solve this via early disentanglement of observer and target motion. LAMP introduces a two-step process: First, we leverage the device's known 6-DoF pose and calibration to convert detected 2D body keypoints from all cameras over a temporal window into a unified 3D world reference frame. Second, an end-to-end-trained Transformer model fits 3D human motion directly to this spatio-temporal ray cloud in world coordinates. This "lift-then-fit" approach allows to learn and leverage a natural prior over world-space human motion, as well as providing an elegant framework to flexibly incorporate information from multiple, temporally asynchronous, partially observing, and moving cameras. LAMP achieves state-of-the-art results on monocular benchmarks, while significantly outperforming baselines for our targeted egocentric multi-camera setting.
</details>

---

### LocateAnything3D: Vision-Language 3D Detection with Chain-of-Sight
著者: Yunze Man, Shihao Wang, Guowen Zhang, Johan Bjorck, Liangyan Gui, Linxi Fan, Jan Kautz, Yu-Xiong Wang, Zhiding Yu

<details>
<summary> 日本語要旨 </summary>

世界で行動するためには、モデルが見たものを名前付けて3次元空間で自分の位置を知る必要があります。現在のビジョン言語モデル（VLM）はオープンエンドな2D記述とグラウンディングに優れていますが、多物体3D検出はまだVLMのツールボックスからほとんど欠けています。私たちは「LocateAnything3D」というVLM固有のレシピを提案します。これにより、3D検出を次トークン予測問題として扱うことができます。その鍵は、人々が画像から推論する方法を反映した短く明示的な「Chain-of-Sight（CoS）」シーケンスです：2Dで物体を見つけ、次に距離、サイズ、姿勢を推測します。デコーダーはまず視覚的なチェインオブサイトとして2D検出を発生させ、その後簡単から難しいカリキュラムで3Dボックスを予測します：物体間では、近くから遠くへの順序が初期の曖昧さを軽減しエゴセントリックな有用性に合致します；各物体内では、カメラ中心からの距離、寸法、回転の因数分解が安定性と学習可能性で情報をランク付けします。このVLM固有のインターフェースは専用ヘッドなしにオープンバレットリストおよびビジュアルプロンプティング能力を保持します。挑戦的なOmni3Dベンチマークで、私たちのモデルは49.89 APという最先端の結果を達成し、基準が与えられた場合でも前回の最高値より+15.51の絶対的な改善を示します。また、保持されたカテゴリに対してゼロショットで一般化し、強力なキャリブレーションと堅牢性を発揮します。3D検出を規律ある次トークン問題に変えることで、「LocateAnything3D」はモデルが3Dで知覚するための実用的な基盤を提供します。
</details>

<details>
<summary> 英語要旨 </summary>

To act in the world, a model must name what it sees and know where it is in 3D. Today's vision-language models excel at open-ended 2D description and grounding, yet multi-object 3D detection remains largely missing from the VLM toolbox. We present LocateAnything3D, a VLM-native recipe that casts 3D detection as a next-token prediction problem. The key is a short, explicit Chain-of-Sight (CoS) sequence that mirrors how people reason from images: find an object in 2D, then infer its distance, size, and pose. The decoder first emits 2D detections as a visual chain-of-thought, then predicts 3D boxes under an easy-to-hard curriculum: across objects, a near-to-far order reduces early ambiguity and matches ego-centric utility; within each object, a center-from-camera, dimensions, and rotation factorization ranks information by stability and learnability. This VLM-native interface preserves open-vocabulary and visual-prompting capability without specialized heads. On the challenging Omni3D benchmark, our model achieves state-of-the-art results, with 49.89 AP, surpassing the previous best by +15.51 absolute improvement even when baseline is given ground-truth 2D boxes. It also generalizes zero-shot to held-out categories with strong calibration and robustness. By turning 3D detection into a disciplined next-token problem, LocateAnything3D offers a practical foundation for models to perceive in 3D.
</details>

---

### Differences That Matter: Auditing Models for Capability Gap Discovery and Rectification
著者: Qihao Liu, Chengzhi Mao, Yaojie Liu, Alan L. Yuille, Wen-Sheng Chu

<details>
<summary> 日本語要旨 </summary>

従来の多モーダルLLM（MLLM）の評価方法は解釈可能性に欠け、モデル間の重要な能力ギャップを完全に明らかにすることがしばしば不十分です。これに対処するために、私たちは**AuditDM**という自動化フレームワークを導入しました。このフレームワークは、MLLMの逸脱を監査することで失敗モードを発見し、修正します。AuditDMは強化学習を用いてMLLMを監査人として微調整し、ターゲットモデル間の不一致を最大化する難問や対事実画像を生成します。訓練された後、監査人は多様で解釈可能な例示を明らかにし、これがモデルの弱点を明らかにし、修正用のアノテーションフリーデータとして役立ちます。Gemma-3やPaliGemma-2のようなSoTAモデルに適用すると、AuditDMは20を超える異なる失敗タイプを発見します。これらの発見で微調整することで、すべてのモデルが16のベンチマークにわたって一貫して改善され、3Bモデルが28Bの対抗馬を超えることも可能になります。私たちの結果は、データスケーリングが減少するリターンに達した場合、ターゲットモデル監査が効果的な診断および改善の道を提供することを示唆しています。
</details>

<details>
<summary> 英語要旨 </summary>

Conventional evaluation methods for multimodal LLMs (MLLMs) lack interpretability and are often insufficient to fully disclose significant capability gaps across models. To address this, we introduce **AuditDM**, an automated framework that actively discovers and rectifies MLLM failure modes by auditing their divergence. AuditDM fine-tunes an MLLM as an auditor via reinforcement learning to generate challenging questions and counterfactual images that maximize disagreement among target models. Once trained, the auditor uncovers diverse, interpretable exemplars that reveal model weaknesses and serve as annotation-free data for rectification. When applied to SoTA models like Gemma-3 and PaliGemma-2, AuditDM discovers more than 20 distinct failure types. Fine-tuning on these discoveries consistently improves all models across 16 benchmarks, and enables a 3B model to surpass its 28B counterpart. Our results suggest that as data scaling hits diminishing returns, targeted model auditing offers an effective path to model diagnosis and improvement.
</details>

---

### PhyOceanCast: Global Ocean Forecasting with Physics-Informed Diffusion
著者: Qixiu Li, Xiang Zhu, Xiaoyong Li, Xiaolong Xu

<details>
<summary> 日本語要旨 </summary>

海洋ダイナミクスは、世界的な気候パターンや極端な天候イベントを駆動し、これにより正確な空間時間予測が気候監視および海洋運用にとって不可欠です。従来のグローバルオーシャンフォレキャスティングシステム（GOFSs）は高精度な予測を提供しますが、計算コストが高く、増加する歴史データを十分に活用できていません。最近の深層学習モデルは顕著な成功を収めましたが、依然として三つの基本的な課題に直面しています：（1）方程式の状態関係による強い物理的結合にもかかわらず海洋変数を均質化すること、（2）球形幾何学を無視し、高緯度での重大な歪みを引き起こすこと、および（3）多スケール時間ダイナミクスをモデル化することに苦労していることです。私たちはこれらの制限を克服する物理情報を考慮した拡散モデル、PhyOceanCastを紹介します。その二つの主要な革新点は次の通りです。第一に、球形トポロジーを保持しつつ異種エンコーディングとk-hop制約付き注意機構を用いて変数間相互作用を可能にする球形グラフ注意ネットワークの多スケール海洋結合（SGAN-MOC）です。第二に、運動拡散制約を持つ複数スケールで海洋ダイナミクスを分解する物理情報付きウェーブレット時間的一貫性（PWTC）モジュールです。PhyOceanCastは、温度、塩分、速度場を含む145の海洋変数と36の深さレベルに加えて海面高を予測します。広範な実験が拡散、トランスフォーマー、ハイブリッドベースラインを上回る優れた性能を示し、グローバルオーシャン標準変数予測の新たなパラダイムを約束します。コードは補足資料で利用可能です。
</details>

<details>
<summary> 英語要旨 </summary>

Ocean dynamics drive global climate patterns and extreme weather events, making accurate spatiotemporal forecasting essential for climate monitoring and marine operations. Traditional Global Ocean Forecasting Systems (GOFSs) offer high accuracy predictions, yet remain computationally expensive and fail to fully leverage growing historical data. Recent deep learning models have achieved notable success, but still face three fundamental challenges: (1) they homogenize ocean variables despite strong physical coupling via equation-of-state relationships; (2) they neglect spherical geometry, resulting in severe distortions at high latitudes; and (3) they struggle to model multi-scale temporal dynamics. We introduce PhyOceanCast, a physics-informed diffusion model that overcomes these limitations through two key innovations. First, the Spherical Graph Attention Network for Multi-scale Ocean Coupling (SGAN-MOC) preserves spherical topology while enabling cross-variable interactions via heterogeneous encoding and k-hop-constrained attention. Second, the Physics-Informed Wavelet Temporal Coherence (PWTC) module that decomposes ocean dynamics across multiple scales with advection-diffusion constraints. PhyOceanCast forecasts 145 ocean variables, including temperature, salinity, and velocity fields, across 36 depth levels plus sea surface height. Extensive experiments demonstrate superior performance over diffusion, transformer, and hybrid baselines, promising a new paradigm for global ocean canonical variable forecasting. Code is available at supplementary materials.
</details>

---

### ORBIT: Benchmarking SfM in The Wild with 360° Video
著者: Sara Sabour, Richard Tucker, Marcus A. Brubaker, Saurabh Saxena, Junhwa Hur, Andrea Tagliasacchi, Deqing Sun, David J. Fleet, Richard Szeliski, Noah Snavely

<details>
<summary> 日本語要旨 </summary>

構造から運動（SfM）は3D認識の基盤であるが、複雑な映像における挑戦的なカメラモーションやダイナミックシーンでは、現在の方法がしばしば失敗する。この問題をさらに悪化させているのは、信頼できる基準データが欠如しており、実際の進捗状況を測定したり、改善が最も必要な箇所を特定することが難しい点である。このギャップに対処するため、私たちはカメラ姿勢推定の評価用新しい基準を導入する。重要な洞察は、オンライン360°パノラマビデオをデータソースとして活用し、挑戦的なクリップを構築しつつも堅牢な基準軌道回復を可能にすることである。これらのパノラマビデオは、ブレや動き、ダイナミックオブジェクトによって影響を受けた部分でもカメラ運動追跡のための豊かな視覚的コンテキストを提供する。360°ビデオ全体でカメラ運動を追跡し、特定の部分を切り出して再投影することで、私たちの基準であるORBIT（100本の映像クリップからなる多様なコレクション）を生成する。実験結果は、COLMAPや他の最先端SfM手法が私たちの基準でカメラ位置を正確に推定することに苦労していることを示し、これは将来の研究における挑戦的かつ未解決の問題領域であることを示唆している。その結果、ORBITは本当に難易度が高く、実世界のSfM問題における研究者たちが有意義に競争し、進捗を測定できる貴重なテストベッドとして機能する。
</details>

<details>
<summary> 英語要旨 </summary>

Structure-from-Motion (SfM) is a cornerstone of 3D perception, yet current methods often fail when applied to complex videos involving challenging camera motions or dynamic scenes. Compounding the problem, the field lacks reliable ground-truth benchmarks for such difficult scenarios, making it hard to gauge real-world progress, or pinpoint where improvements are most needed. To address this gap, we introduce a new benchmark for evaluating camera pose estimation. Our key insight is to leverage online panoramic 360° as a source of data from which to construct challenging clips, while still enabling robust ground-truth trajectory recovery. The panoramic nature of these videos provides richer visual context for tracking camera motion, even when parts of the view are affected by blur, motion, or dynamic objects. By tracking camera motion across full 360° videos, we crop and reproject selected portions to generate perspective-view clips that serve as our benchmark---ORBIT---a diverse collection of 100 video clips. Experiments show that COLMAP and other state-of-the-art SfM methods struggle to accurately estimate camera positions on our benchmark, indicating that it remains a challenging and open problem space for future research. As a result, ORBIT provides a valuable testbed where researchers can meaningfully compete and measure progress on truly challenging, real-world SfM problems.
</details>

---

### AGENTSAFE: Benchmarking The Safety of Embodied Agents on Hazardous Instructions
著者: Zonghao Ying, Le Wang, Yisong Xiao, Jiakai Wang, Yuqing Ma, Jinyang Guo, Zhenfei Yin, Mingchuan Zhang, Aishan Liu, Xianglong Liu

<details>
<summary> 日本語要旨 </summary>

ビジョン言語モデル（VLM）の統合が、人間中心の環境で動作可能な新世代のエンバディッドエージェントを推進しています。しかし、展開が拡大するにつれて、これらのシステムは特に危険な指示を実行する際に増加する安全リスクに直面します。現在の安全評価ベンチマークは限定的です：それらは狭い範囲の危険しかカバーせず、主に最終結果に焦点を当て、エージェントの完全な知覚-計画-実行プロセスを無視し、重要な障害モードを見えにくくしています。したがって、私たちはSAFEという名前のベンチマークを提案します。これは、危険な指示に対するエンバディッドVLMエージェントの安全性を体系的に評価するものです。SAFEは三つのコンポーネントから構成されています：SAFE-THOR、高レベルのVLM出力を低レベルのエンバディッド制御にマッピングする汎用アダプターを備えた拡張可能な敵対的シミュレーションサンドボックスで、多様なエージェントワークフローの統合をサポート；SAFE-VERSE、アイザック・アシモフの三法則に触発されたリスク認識タスクセットで、45の敵対的シナリオ、1,350の危険なタスク、9,900の指示を含み、人間、環境、エージェントへのリスクをカバー；そしてSAFE-DIAGNOSE、知覚、計画、実行にわたるエージェントパフォーマンスを測定する多層的かつ細分化された評価プロトコルです。私たちはSAFEを9つの最先端VLMと2つのエンバディッドエージェントワークフローに適用し、危険認識から安全な計画および実行への翻訳における体系的な失敗を明らかにします。私たちの発見は現在の安全整合性の基本的な限界を示し、より安全なエンバディッドインテリジェンスの開発における包括的で多段階評価の必要性を証明しています。
</details>

<details>
<summary> 英語要旨 </summary>

The integration of vision-language models (VLMs) is driving a new generation of embodied agents capable of operating in human-centered environments. However, as deployment expands, these systems face growing safety risks, particularly when executing hazardous instructions. Current safety evaluation benchmarks remain limited: they cover only narrow scopes of hazards and focus primarily on final outcomes, neglecting the agent's full perception-planning-execution process and thereby obscuring critical failure modes. Therefore, we present SAFE, a benchmark for systematically assessing the safety of embodied VLM agents on hazardous instructions. SAFE comprises three components: SAFE-THOR, an extensible adversarial simulation sandbox with a universal adapter that maps high-level VLM outputs to low-level embodied controls, supporting diverse agent workflow integration; SAFE-VERSE, a risk-aware task suite inspired by Asimov's Three Laws of Robotics, comprising 45 adversarial scenarios, 1,350 hazardous tasks, and 9,900 instructions that span risks to humans, environments, and agents; and SAFE-DIAGNOSE, a multi-level and fine-grained evaluation protocol measuring agent performance across perception, planning, and execution. Applying SAFE to nine state-of-the-art VLMs and two embodied agent workflows, we uncover systematic failures in translating hazard recognition into safe planning and execution. Our findings reveal fundamental limitations in current safety alignment and demonstrate the necessity of a comprehensive, multi-stage evaluation for developing safer embodied intelligence.
</details>

---

### CTCal: Rethinking Text-to-Image Diffusion Models Via Cross-Timestep Self-Calibration
著者: Xiefan Guo, Xinzhu Ma, Haiyu Zhang, Di Huang

<details>
<summary> 日本語要旨 </summary>

最近のテキストから画像への合成技術は、主に拡散ベースのモデルによって推進されていますが、テキストプロンプトと生成された画像の正確な整列を達成することは依然として大きな課題です。この困難さは主に従来の拡散損失の限界から生じており、これは細部までのテキスト画像対応をモデリングするための暗黙的な監督しか提供しません。本論文では、拡散モデル内における正確なテキスト画像整列がtimestepが増加するにつれてますます困難になるという観察に基づいたCross-Timestep Self-Calibration（CTCal）を導入します。CTCalは、より少ないノイズで形成された信頼性の高いテキスト画像整列（すなわちクロスアテンションマップ）を利用して、より多くのノイズがある大きなtimestepにおける表現学習を校正し、トレーニング中に明示的な監督を提供します。さらに、CTCalと拡散損失の調和的な統合を達成するためにtimestep-aware adaptive weightingを提案しています。CTCalはモデル非依存であり、既存のテキストから画像への拡散モデル（例えばStable Diffusion 2.1）や流れベースアプローチ（例えばStable Diffusion 3）に容易に統合することができます。T2I-Compbench++およびGenEvalベンチマークを用いた広範な実験は、提案されたCTCalの有効性と汎用性を示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advancements in text-to-image synthesis have been largely propelled by diffusion-based models, yet achieving precise alignment between text prompts and generated images remains a persistent challenge. We find that this difficulty arises primarily from the limitations of conventional diffusion loss, which provides only implicit supervision for modeling fine-grained text-image correspondence. In this paper, we introduce Cross-Timestep Self-Calibration (CTCal), founded on the supporting observation that establishing accurate text-image alignment within diffusion models becomes progressively more difficult as the timestep increases. CTCal leverages the reliable text-image alignment (i.e., cross-attention maps) formed at smaller timesteps with less noise to calibrate the representation learning at larger timesteps with more noise, thereby providing explicit supervision during training. We further propose a timestep-aware adaptive weighting to achieve a harmonious integration of CTCal and diffusion loss. CTCal is model-agnostic and can be seamlessly integrated into existing text-to-image diffusion models, encompassing both diffusion-based (e.g., Stable Diffusion 2.1) and flow-based approaches (e.g., Stable Diffusion 3). Extensive experiments on T2I-Compbench++ and GenEval benchmarks demonstrate the effectiveness and generalizability of the proposed CTCal.
</details>

---

### BulletTime: Decoupled Control of Time and Camera Pose for Video Generation
著者: Yiming Wang, Qihang Zhang, Shengqu Cai, Tong Wu, Jan Ackermann, Zhengfei Kuang, Yang Zheng, Frano Rajič, Siyu Tang, Gordon Wetzstein

<details>
<summary> 日本語要旨 </summary>

新たに登場したビデオ拡散モデルは高い視覚的忠実度を達成していますが、シーンダイナミクスとカメラの動きを基本的に結びつけてしまうため、正確な空間および時間制御能力が限られています。私たちは、シーンダイナミクスとカメラポーズを明示的に分離することで、両者の細かい操作を可能にする4Dコントローラブルビデオ拡散フレームワークを提案します。このフレームワークは連続したワールドタイムシーケンスとカメラトラジェクトリを条件付き入力として取り込み、注意層における4D位置埋め込みと特徴の適応正規化を通じてビデオ拡散モデルに注入します。このモデルをトレーニングするために、時間的変動とカメラの変動が独立してパラメータ化されたユニークなデータセットを作成しました（このデータセットは公開予定です）。実験結果によると、私たちのモデルは多様なタイミングパターンやカメラトラジェクトリにわたって堅牢な現実世界4D制御を達成し、生成品質を維持しつつ、コントローラビリティの面で先行研究を上回ることが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

Emerging video diffusion models achieve high visual fidelity but fundamentally couple scene dynamics with camera motion, limiting their ability to provide precise spatial and temporal control. We introduce a 4D-controllable video diffusion framework that explicitly decouples scene dynamics from camera pose, enabling fine-grained manipulation of both scene dynamics and camera viewpoint. Our framework takes continuous world-time sequences and camera trajectories as conditioning inputs, injecting them into the video diffusion model through a 4D positional embedding in the attention layer and adaptive normalizations for feature modulation. To train this model, we curate a unique dataset in which temporal and camera variations are independently parameterized; this dataset will be made public. Experiments show that our model achieves robust real-world 4D control across diverse timing patterns and camera trajectories, while preserving high generation quality and outperforming prior work in controllability.
</details>

---

### LitePT: Lighter Yet Stronger Point Transformer
著者: Yuanwen Yue, Damien Robert, Jianyuan Wang, Sunghwan Hong, Jan D. Wegner, Christian Rupprecht, Konrad Schindler

<details>
<summary> 日本語要旨 </summary>

現代の3D点群処理用ニューラルアーキテクチャには畳み込み層と注意ブロックが含まれていますが、それらをどのように組み合わせるか最適な方法は明確ではありません。私たちは3D点群ネットワーク内の異なる計算ブロックの役割を分析し、次の直感的な挙動を見出しました：初期層で高解像度においては、低レベルの幾何学情報を抽出するために畳み込みが適しており、その一方で注意メカニズムは利益をもたらさず高コストです；また、深層で低解像度の場合、注意はより効率的に高レベルのセマンティクスと文脈を捉えます。この設計原則に基づき、初期段階では畳み込みを使用し、深層では注意に切り替える新たな改良された3D点群バックボーンを提案します。冗長な畳み込み層を廃棄する際の空間配置情報の損失を避けるため、訓練不要の新しい3D位置エンコーディングであるPointROPEを導入します。結果として得られたLitePTモデルは、パラメータ数が最先端のPoint Transformer V3の約3.6倍少なく、2倍速く動作し、2倍少ないメモリを使用しながらも、さまざまなタスクやデータセットでそれに匹敵するか、またはそれを上回る性能を発揮します。
</details>

<details>
<summary> 英語要旨 </summary>

Modern neural architectures for 3D point cloud processing contain both convolutional layers and attention blocks, but the best way to assemble them remains unclear. We analyse the role of different computational blocks in 3D point cloud networks and find an intuitive behaviour: convolution is adequate to extract low-level geometry at high-resolution in early layers, where attention is expensive without bringing any benefits; attention captures high-level semantics and context in low-resolution, deep layers more efficiently. Guided by this design principle, we propose a new, improved 3D point cloud backbone that employs convolutions in early stages and switches to attention for deeper layers. To avoid the loss of spatial layout information when discarding redundant convolution layers, we introduce a novel, training-free 3D positional encoding, PointROPE. The resulting LitePT model has 3.6× fewer parameters, runs 2× faster, and uses 2× less memory than the state-of-the-art Point Transformer V3, but nonetheless matches or even outperforms it on a range of tasks and datasets.
</details>

---

### Global Prior Meets Local Consistency: Dual-Memory Augmented Vision-Language-Action Model for Efficient Robotic Manipulation
著者: Zaijing Li, Bing Hu, Rui Shao, Gongwei Chen, Dongmei Jiang, Pengwei Xie, Jianye Hao, Liqiang Nie

<details>
<summary> 日本語要旨 </summary>

階層的ビジョン・ランゲージ・アクション（VLA）モデルは、ロボット操作の分野で急速に主流となっています。これらは通常、認識および理解のためのビジョン・ランゲージバックボーンと、アクション生成のための生成的ポリシーから構成されています。しかし、そのパフォーマンスはアクション生成プロセスによって次第に制約されるようになりました。(i) 低い推論効率。等方性ノイズ事前分布とターゲットアクション分布の間の顕著な分布的ギャップが、デノイジングステップを増加させ、実行不可能なサンプルの発生率を高めます。(ii) 劣った堅牢性。既存のポリシーは現在の観測にのみ条件付けられており、歴史的なシーケンスの制約を無視し、タスク進行と時間的一貫性への認識が欠如しています。これらの問題に対処するために、私たちはグローバル・プリオリメモリ（GPM）およびローカル・コンシステンシー・メモリ（LCM）を備えたデュアルメモリVLAフレームワークであるOptimusVLAを導入します。GPMは、セマンティックに類似した軌道から取得されたタスクレベルのプリオリでガウシアンノイズを置き換えることで、生成パスを短縮し、関数評価回数（NFE）を削減します。LCMは実行されたアクションシーケンスを動的にモデル化してタスク進行を推定し、学習された一貫性制約を注入することで軌道の時間的連続性と滑らかさを強制します。3つのシミュレーションベンチマークにおいて、OptimusVLAは強力なベースラインを一貫して上回ります：LIBEROで98.6％の平均成功率を達成し、CALVINでは$\pi_{0}$より13.5％改善し、RoboTwin 2.0 Hardで38％の平均成功率を達成します。リアルワールド評価においては、一般化と長期間スイートで最高位を獲得し、それぞれ$\pi_{0}$より42.9％と52.4％を上回ります。また、2.9倍の推論速度向上も実現しています。
</details>

<details>
<summary> 英語要旨 </summary>

Hierarchical Vision–Language–Action (VLA) models have rapidly become a dominant paradigm for robotic manipulation. It typically comprising a Vision–Language backbone for perception and understanding, together with a generative policy for action generation. However, its performance is increasingly bottlenecked by the action generation proceess. (i) Low inference efficiency. A pronounced distributional gap between isotropic noise priors and target action distributions, which increases denoising steps and the incidence of infeasible samples. (ii) Poor robustness. Existing policies condition solely on the current observation, neglecting the constraint of history sequence and thus lacking awareness of task progress and temporal consistency. To address these issues, we introduce OptimusVLA, a dual-memory VLA framework with Global Prior Memory (GPM) and Local Consistency Memory (LCM). GPM replaces Gaussian noise with task-level priors retrieved from semantically similar trajectories, thereby shortening the generative path and reducing the umber of function evaluations (NFE). LCM dynamically models executed action sequence to infer task progress and injects a learned consistency constraint that enforces temporal coherence and smoothness of trajectory. Across three simulation benchmarks, OptimusVLA consistently outperforms strong baselines: it achieves 98.6\% average success rate on LIBERO, improves over $\pi_{0}$ by 13.5\% on CALVIN, and attains 38\% average success rate on RoboTwin 2.0 Hard. In Real-World evaluation, OptimusVLA ranks best on Generalization and Long-horizon suites, surpassing $\pi_{0}$ by 42.9\% and 52.4\%, respectively, while delivering 2.9× inference speedup.
</details>

---

### Seeing Through The Noise: Improving Infrared Small Target Detection and Segmentation from Noise Suppression Perspective
著者: Maoxun Yuan, Duanni Meng, Ziteng Xi, Tianyi Zhao, Shiji Zhao, Yimian Dai, Xingxing Wei

<details>
<summary> 日本語要旨 </summary>

赤外線小目標の検出とセグメンテーション（IRSTDS）は、防衛および民間応用において重要でありながらも困難な課題です。これは、ターゲットの暗く形のない外観と背景の混乱が激しいためです。最近のCNNベースの方法は有望な結果を達成していますが、それらは騒音の影響を軽減するために特徴表現を強化することだけに焦点を当てており、これが誤報率の増加問題を引き起こしています。本論文では、周波数領域から問題を分析し、騒音抑制の観点からパフォーマンスを向上させるために新しいノイズ抑制特徴ピラミッドネットワーク（NS-FPN）を提案します。このNS-FPNは、低周波数ガイド付き特徴浄化（LFP）モジュールと螺旋認識特徴サンプリング（SFS）モジュールを元のFPN構造に統合しています。LFPモジュールは高周波成分を浄化することで騒音特徴を抑制し、騒音干渉なしで特徴強化を実現します。一方、SFSモジュールは螺旋サンプリングを採用して特徴融合過程においてターゲット関連の特徴を統合します。私たちのNS-FPNは軽量で効果的に設計され、既存のIRSTDSフレームワークに容易に組み込むことができます。IRSTD-1kおよびNUAA-SIRSTデータセットを用いた広範な実験では、私たちの方法が誤報を大幅に削減し、IRSTDSタスクにおいて優れた性能を達成することを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Infrared small target detection and segmentation (IRSTDS) is a critical yet challenging task in defense and civilian applications, owing to the dim, shapeless appearance of targets and severe background clutter. Recent CNN-based methods have achieved promising target perception results, but they only focus on enhancing feature representation to offset the impact of noise, which results in the increased false alarm problem. In this paper, through analyzing the problem from the frequency domain, we pioneer in improving performance from noise suppression perspective and propose a novel noise-suppression feature pyramid network (NS-FPN), which integrates a low-frequency guided feature purification (LFP) module and a spiral-aware feature sampling (SFS) module into the original FPN structure. The LFP module suppresses the noise features by purifying high-frequency components to achieve feature enhancement devoid of noise interference, while the SFS module further adopts spiral sampling to fuse target-relevant features in feature fusion process. Our NS-FPN is designed to be lightweight yet effective and can be easily plugged into existing IRSTDS frameworks. Extensive experiments on the IRSTD-1k and NUAA-SIRST datasets demonstrate that our method significantly reduces false alarms and achieves superior performance on IRSTDS task.
</details>

---

### General Process Reward Modeling for Robotic Reinforcement Learning
著者: Huajie Tan, Sixiang Chen, Yijie Xu, Zixiao Wang, Cheng Chi, Yuheng Ji, Yaoxu Lyu, Zhongxia Zhao, Xiansheng Chen, Peterson Co, Shaoxuan Xie, Guocai Yao, Pengwei Wang, Zhongyuan Wang, Shanghang Zhang

<details>
<summary> 日本語要旨 </summary>

ロボット工学における強化学習（RL）の適用において最大の障壁は、効果的な報酬関数の設計です。最近では学習型プロセス報酬モデル（PRMs）が有望な方向性として注目されていますが、二つの基本的な制約によってしばしば妨げられます。一つは、その報酬モデルがステップ認識を欠き、単眼視点に依存しているため、微細な操作の進捗評価が信頼性に欠けることです。もう一つは、報酬形成手法が理論的に不十分であり、しばしば意味の罠を引き起こし、ポリシー最適化を誤導することです。これらに対処するため、我々は多視点入力から一般的なステップ認識型プロセス報酬モデルを学習する新しい方法であるRobo-Dopamineを導入します。その中核には、3,400時間以上の大規模データセットで訓練された一般的な報酬モデル（GRM）があります。これはステップごとの報酬離散化を用いて構造理解を強化し、多視点報酬融合によって知覚的制約を克服します。Robo-Dopamineを基に、我々はポリシー不変型報酬形成法を用いる堅牢なポリシー学習フレームワークであるDopamine-RLを提案します。これにより、エージェントは最適ポリシーを変えずに密な報酬を活用して効率的に自己改善することが可能となり、根本的に意味の罠を回避します。10個のシミュレーションタスクおよび8つの実世界タスクで広範囲にわたる実験が我々のアプローチを検証しています。GRMは報酬評価において最先端の精度を達成し、GRMに基づくDopamine-RLはポリシー学習効率を大幅に向上させます。例えば、GRMが単一の専門家軌道からワンショットで新しいタスクに適応されると、その結果得られた報酬モデルはDopamine-RLを用いてポリシーを150回のオンラインロールアウト（実際のロボット相互作用で約1時間）で95％の成功率まで改善させ、タスク間で強力な汎化性能を維持します。
</details>

<details>
<summary> 英語要旨 </summary>

The primary obstacle for applying reinforcement learning (RL) to real-world robotics is the design of effective reward functions. While recently learning-based Process Reward Models (PRMs) are a promising direction, they are often hindered by two fundamental limitations: their reward models lack step-aware understanding and rely on single-view perception, leading to unreliable assessments of fine-grained manipulation progress; and their reward shaping procedures are theoretically unsound, often inducing a semantic trap that misguides policy optimization. To address these, we introduce Robo-Dopamine, a novel reward modeling method for learning a general-purpose, step-aware process reward model from multi-view inputs. At its core is our General Reward Model (GRM), trained on a vast 3,400+ hour dataset, which leverages Step-wise Reward Discretization for structural understanding and Multi-Perspective Reward Fusion to overcome perceptual limitations. Building upon Robo-Dopamine, we propose Dopamine-RL, a robust policy learning framework that employs a theoretically-sound Policy-Invariant Reward Shaping method, which enables the agent to leverage dense rewards for efficient self-improvement without altering the optimal policy, thereby fundamentally avoiding the semantic trap. Extensive experiments across 10 simulated and 8 real-world tasks validate our approach. {GRM achieves state-of-the-art accuracy in reward assessment}, and {Dopamine-RL built on GRM significantly improves policy learning efficiency}. For instance, after {GRM} is adapted to a new task in a one-shot manner from a single expert trajectory, the resulting reward model enables Dopamine-RL to improve the policy from near-zero to 95\% success with only 150 online rollouts (approximately 1 hour of real robot interaction), while retaining strong generalization across tasks.
</details>

---

### Action-Sketcher: From Reasoning to Action Via Visual Sketches for Robotic Manipulation
著者: Huajie Tan, Peterson Co, Yijie Xu, Shanyu Rong, Yuheng Ji, Cheng Chi, Xiansheng Chen, Zhongxia Zhao, Pengwei Wang, Zhongyuan Wang, Shanghang Zhang

<details>
<summary> 日本語要旨 </summary>

長期的な目標を持つ、複雑で動的な環境におけるロボットの操作は、実際の展開においてますます重要となっています。これには、複雑なレイアウト内での空間的な曖昧さの解消や、動的な相互作用下での時間的な回復力が必要です。しかし、既存のエンドツーエンドおよび階層型のビジョン・ランゲージ・アクション（VLA）ポリシーは、しばしばテキストのみの手がかりに依存し、計画意図を潜在的なものとして保持するため、散らかったまたは不完全に指定されたシーンでの\textit{参照的な根拠付け}が妨げられ、長期目標の効果的な\textit{タスク分解}が閉ループ相互作用によって阻害され、行動選択の理由を隠蔽することで\textit{因果説明}が制限されます。これらの問題に対処するために、まず私たちは**Visual Sketch**を導入します。これは、ロボットの現在のビュー上に点、箱、矢印、タイプされた関係を描画して空間的意図を外部化し、言語とシーンの幾何学を結びつけ、高次の推論と低次の制御の間に人間が確認できる橋渡しを提供する軽量な視覚的中間物です。**Visual Sketch**を基にして、私たちはVLAフレームワークである**Action-Sketcher**を提示します。これは適応型トークンゲート戦略によって調整されるサイクリックな\textit{See $\rightarrow$ Think $\rightarrow$ Sketch $\rightarrow$ Act}ワークフローで動作し、推論のトリガー、スケッチの修正、アクション発行をサポートすることにより、反応的な修正と人間との相互作用を可能にしつつ、リアルタイムでのアクション予測を維持します。スケーラブルなトレーニングと評価を可能にするために、私たちは交錯した画像、テキスト、\textit{Visual Sketch}の指導、およびアクションシーケンスを含む230万サンプルのコーパスを編纂し、\textit{Action-Sketcher}は交錯したシーケンス整列によるモダリティ統一、言語からスケッチへの一貫性による正確な言語的根拠付け、およびスケッチからアクションへの強化学習を補完した模倣学習を組み合わせたマルチステージカリキュラムレシピでトレーニングします。散らかった机上や複数オブジェクトタスクにおけるシミュレーションと実際のロボットを用いた実験では、長期目標達成率が向上し、動的なシーン変化への強靭性が増し、編集可能なスケッチと段階ごとの計画による解釈性が高まったことを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Long-horizon, open-world robotic manipulation is increasingly important for real-world deployment, requiring spatial disambiguation in complex layouts and temporal resilience under dynamic interaction. However, existing end-to-end and hierarchical Vision–Language–Action (VLA) policies often rely on text-only cues while keeping plan intent latent, which undermines \textit{referential grounding} in cluttered or underspecified scenes, impedes effective \textit{task decomposition} of long-horizon goals with close-loop interaction, and limits \textit{causal explanation} by obscuring the rationale behind action choices. To address these issues, we first introduce \textbf{Visual Sketch}, a lightweight visual intermediate that renders points, boxes, arrows, and typed relations on the robot’s current views to externalize spatial intent, bind language to scene geometry, and provide a human-verifiable bridge between high-level reasoning and low-level control. Building on \textit{Visual Sketch}, we present \textbf{Action-Sketcher}, a VLA framework that operates in a cyclic \textit{See $\rightarrow$ Think $\rightarrow$ Sketch $\rightarrow$ Act} workflow coordinated by adaptive token-gated strategy for reasoning triggers, sketch revision, and action issuance, thereby supporting reactive corrections and human interaction while preserving real-time action prediction. To enable scalable training and evaluation, we curate a 2.3M-sample corpus with interleaved images, text, \textit{Visual Sketch} supervision, and action sequences, and train \textit{Action-Sketcher} with a multi-stage curriculum recipe that combines interleaved sequence alignment for modality unification, language-to-sketch consistency for precise linguistic grounding, and imitation learning augmented with sketch-to-action reinforcement for robustness. Experiments on cluttered tabletops and multi-object tasks, in simulation and on real robots, show improved long-horizon success, stronger robustness to dynamic scene changes, and enhanced interpretability via editable sketches and step-wise plans.
</details>

---

### Fast-FoundationStereo: Real-Time Zero-Shot Stereo Matching
著者: Bowen Wen, Shaurya Dewan, Stan Birchfield

<details>
<summary> 日本語要旨 </summary>

ステレオファウンデーションモデルは強力なゼロショット一般化能力を持っていますが、リアルタイムアプリケーションにおいて計算コストが高すぎます。効率的なステレオアーキテクチャは、速度のために堅牢性を犠牲にし、費用のかかるドメインごとの微調整が必要です。このギャップを埋めるために、我々は初めて強力なゼロショット一般化能力をリアルタイムフレームレートで達成するFast-FoundationStereoというアーキテクチャファミリーを提案します。我々は、分割統治型の加速戦略を採用しており、その主要な3つのコンポーネントは次の通りです：(1) ハイブリッドバックボーンを効率的な単一学生に圧縮するための知識蒸留；(2) 潜在時間予算内で最適なコストフィルターデザインを自動発見するブロックワイズニューラルアーキテクチャ検索により、探索の複雑さを指数関数的に削減；(3) イテレーティブリファインメントモジュール内の冗長性を排除するための構造化プルーニング。また、我々は1.4Mの野外ステレオペアを補完し、知識蒸留を促進する自動偽ラベリングパイプラインを導入します。結果として得られたモデルは、FoundationStereoの約10倍速く実行できながら、そのゼロショット精度に近い性能を発揮し、リアルタイム手法の中で新たな最先端を確立します。
</details>

<details>
<summary> 英語要旨 </summary>

Stereo foundation models achieve strong zero-shotgeneralization but remain computationally prohibitive forreal-time applications. Efficient stereo architectures, on the other hand, sacrificerobustness for speed and require costly per-domain fine-tuning. To bridge this gap, we present Fast-FoundationStereo, a family of architectures that achieve, for the first time, strong zero-shot generalization at real-time frame rate. We employ a divide-and-conquer acceleration strategy with three components: (1) knowledge distillation to compress the hybrid backbone into a single efficient student; (2) blockwise neural architecture search for automatically discovering optimal cost filtering designs under latency budgets, reducing search complexity exponentially; and (3) structured pruning for eliminating redundancy in the iterative refinement module. Furthermore, we introduce an automatic pseudo-labeling pipeline used to curate 1.4M in-the-wild stereo pairs to supplement synthetic training data and facilitate knowledge distillation. The resulting model can run over 10× faster than FoundationStereo while closely matching its zero-shot accuracy, thus establishing a new state-of-the-art among real-time methods.
</details>

---

### PV-Ground: Text-Guided Point-Voxel Interaction for 3D Visual Grounding
著者: Junpeng Shang, Feifei Shao, Jun Xiao, Lin Li, Hongwei Wang, Dongfang Ma

<details>
<summary> 日本語要旨 </summary>

3次元視覚的なアンカリング（VG）は、自由形式のテキスト記述に基づいて3次元シーン内のターゲットオブジェクトをローカライズすることを目指しています。既存の3D VGモデルは主に点群特徴抽出のためにポイントベースのバックボーンを使用しています。このような方法では、入力点群の積極的なダウンサンプリングが必要であり、正確なローカライズに不可欠な微細な空間的詳細を犠牲にします。本論文では、効果的なテキストガイド付きポイント-ボクセル特徴相互作用に基づく新しい3D VGアーキテクチャであるPV-Groundを提案します。私たちの方法は、両方のボクセルとキーポイントの補完的な強みを活かしています：高解像度の空間詳細を保持するためにボクセルベースの特徴抽出バックボーンを使用し、テキストクエリと効率的で深い相互作用を可能にするためにこれらの特徴を集約するコンパクトなキーポイントを利用します。さらに、私たちはテキストガイド付きキーポイントサンプリングモジュールを提案し、キーポイント分布をテキストで記述されたオブジェクト周辺に適応的に集中させることで、タスク固有の特徴集約を可能にし、モデルパフォーマンスを大幅に向上させます。広範な定性的および定量的実験が私たちの提案方法の優位性を示しています。私たちの方法は、ScanReferデータセットで5.1％、ReferIt3Dデータセットで5.6％のパフォーマンス向上を達成し、セグメンテーションタスクでも4％以上の改善を実現しています。コードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

3D visual grounding (VG) aims to localize target objects in 3D scenes based on free-form textual descriptions. Existing 3D VG models predominantly employ point-based backbones for point cloud feature extraction. Such methods require aggressive downsampling of the input point cloud, which sacrifices the fine-grained spatial details crucial for precise localization. This paper proposes PV-Ground, a novel 3D VG architecture based on effective text-guided point-voxel feature interaction. Our method leverages the complementary strengths of both voxels and keypoints: it employs a voxel-based feature extraction backbone to preserve high-resolution spatial details, while utilizing compact keypoints to aggregate these features for efficient, deep interaction with the textual query. Furthermore, we propose a text-guided keypoint sampling module to adaptively concentrate the keypoint distribution around the text-described object, enabling task-specific feature aggregation and significantly boosts model performance. Extensive qualitative and quantitative experiments demonstrate the superiority of our proposed method. Our method achieves a performance improvement of 5.1\% on the ScanRefer dataset and 5.6\% on the ReferIt3D dataset, while also achieves over 4\% improvement in the segmentation task. The code will be made publicly available.
</details>

---

### GeoMMBench and GeoMMAgent: Toward Expert-Level Multimodal Intelligence in Geoscience and Remote Sensing
著者: Aoran Xiao, Shihao Cheng, Yonghao Xu, Yexian Ren, Hongruixuan Chen, Naoto Yokoya

<details>
<summary> 日本語要旨 </summary>

最近のマルチモーダル大規模言語モデル（MLLM）の進歩は、ドメイン指向AIの発展を加速させていますが、地球科学や遠隔センシング（RS）におけるその開発は、広範な専門知識、異質なセンサーモダリティ、タスクの断片化されたスペクトルといった特有の課題によって制約されています。これらのギャップを埋めるために、私たちはGeoMMBenchを導入します。これは、多様なRS分野、センサー、タスクをカバーする包括的なマルチモーダル質問応答基準であり、以前の基準よりも広範かつ厳格な評価が可能です。GeoMMBenchを使用して、36のオープンソースおよびプロプライエタリー大規模言語モデル（LLM）を評価し、専門知識、感覚的な根拠付け、推論といった地理空間解釈において専門家レベルが必要とされる能力の系統的な欠陥を明らかにしました。評価に留まらず、私たちはGeoMMAgentを提案します。これは、ドメイン特化型RSモデルやツールを戦略的に統合することで検索、知覚、推論を行うマルチエージェントフレームワークです。広範な実験結果は、GeoMMAgentが単独のLLMよりも大幅に優れていることを示し、複雑な地球科学やRSの課題に動的に対処するためにツール強化エージェントが重要であることを強調しています。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advances in multimodal large language models (MLLMs) have accelerated progress in domain-oriented AI, yet their development in geoscience and remote sensing (RS) remains constrained by distinctive challenges: wide-ranging disciplinary knowledge, heterogeneous sensor modalities, and a fragmented spectrum of tasks. To bridge these gaps, we introduce GeoMMBench, a comprehensive multimodal question-answering benchmark covering diverse RS disciplines, sensors, and tasks, enabling broader and more rigorous evaluation than prior benchmarks. Using GeoMMBench, we assess 36 open-source and proprietary large language models (LLMs), uncovering systematic deficiencies in domain knowledge, perceptual grounding, and reasoning—capabilities essential for expert-level geospatial interpretation. Beyond evaluation, we propose GeoMMAgent, a multi-agent framework that strategically integrates retrieval, perception, and reasoning through domain-specific RS models and tools. Extensive experimental results demonstrate that GeoMMAgent significantly outperforms standalone LLMs, underscoring the importance of tool-augmented agents for dynamically tackling complex geoscience and RS challenges.
</details>

---

### UniLS: End-to-End Audio-Driven Avatars for Unified Listening and Speaking
著者: Xuangeng Chu, Ruicong Liu, Yifei Huang, Yun Liu, YICHEN PENG, Bo Zheng

<details>
<summary> 日本語要旨 </summary>

リアルな会話型アバターを生成するには、単独のスピーカーではなく、発話と聴取の動的かつ相互作用的なプロセスをモデル化する必要があります。しかし、リスナーをモデル化することは特に困難です：直接音駆動型のトレーニングでは失敗し、硬直した静的な聴取動作が生じます。この失敗は基本的な不均衡から生じています：スピーカーの動きは発話音声に強く駆動される一方で、リスナーの動きは主に内部の動作優先順位に従い、外部の発話によってほんのわずかに導かれます。この課題が多くの方法をスピーチ生成のみに集中させる原因となりました。共同生成の唯一の以前の試みは、追加のスピーカーの動きを用いてリスナーを生成するものでしたが、この設計はエンドツーエンドではなく、リアルタイム適用性を妨げます。この制限に対処するために、私たちはUniLSを提案します。これは、ダブルトラックオーディオのみで駆動される統一的なスピーチ・リスニング表現を生成する初めてのエンドツーエンドフレームワークです。私たちの方法は、革新的な2段階トレーニングパラダイムを導入します。第1ステージでは、オーディオフリーの自己回帰ジェネレータを用いて内部動作優先順位を学習し、自然な顔の動きの即興的ダイナミクスを捉えます。第2ステージでは、ダブルトラックオーディオを導入し、ジェネレータを外部発話の手がかりに基づいて学習した動作優先順位を調整するように微調整します。広範な評価では、UniLSはスピーチ精度で最先端の成果を達成しています。さらに重要なことに、リスニングメトリクスで44.1%の改善を実現し、より多様で自然な聴取表現を生成します。これにより硬直問題が効果的に緩和され、インタラクティブデジタルヒューマン用の実用的かつ高精度なオーディオ駆動ソリューションを提供します。
</details>

<details>
<summary> 英語要旨 </summary>

Generating lifelike conversational avatars requires modeling not just isolated speakers, but the dynamic, reciprocal interaction of speaking and listening. However, modeling the listener is exceptionally challenging: direct audio-driven training fails, producing stiff, static listening motions. This failure stems from a fundamental imbalance: the speaker's motion is strongly driven by speech audio, while the listener's motion primarily follows an internal motion prior and is only loosely guided by external speech. This challenge has led most methods to focus on speak-only generation. The only prior attempt at joint generation relies on extra speaker's motion to produce the listener. This design is not end-to-end, thereby hindering the real-time applicability. To address this limitation, we present UniLS, the first end-to-end framework for generating unified speak-listen expressions, driven by only dual-track audio. Our method introduces a novel two-stage training paradigm. Stage 1 first learns the internal motion prior by training an audio-free autoregressive generator, capturing the spontaneous dynamics of natural facial motion. Stage 2 then introduces the dual-track audio, fine-tuning the generator to modulate the learned motion prior based on external speech cues. Extensive evaluations show UniLS achieves state-of-the-art speaking accuracy. More importantly, it delivers up to 44.1% improvement in listening metrics, generating significantly more diverse and natural listening expressions. This effectively mitigates the stiffness problem and provides a practical, high-fidelity audio-driven solution for interactive digital humans.
</details>

---

### Plan, Imagine, Then Act: Steering Your VLA with Efficient Visually Grounded Planning
著者: Zhuoyang Zhang, Shang Yang, Qinghao Hu, Luke Huang, James Hou, Yufei Sun, Yao Lu, Song Han

<details>
<summary> 日本語要旨 </summary>

ビジョン・ランゲージ・アクション（VLA）モデルは、特にオープンワールド環境での抽象的な言語指示を具体的かつ実行可能なアクションに変換するという難しいタスクを担っています。私たちは、\textit{Visually Grounded Planning}（視覚的に根拠のある計画）を提案します。これは、想像された将来の観測とサブタスクの説明を用いてVLAを段階的にガイドする一般的で効率的な高レベルプランナーです。想像された将来の観測があることで、VLAは高次元の意味論的推論よりもビジュオモーター推論に集中することが可能となり、精度と汎化性能が向上します。私たちのプランナーは、現在の視覚入力および言語指示から高品質な640×480の将来の観測を予測する非常に効率的な先見の明画像生成モジュールと、タスクについて推論し、両方のジェネレーターおよびVLA用のサブタスク説明を生成するビジョン・ランゲージコンポーネントから構成されます。重要なことに、最先端のVLAsは、視覚入力を単純に強化するだけで、アーキテクチャーの変更なしに私たちのプランナーをシームレスに統合することが可能です。先見の明ジェネレーターは、約1000万件のマルチタスク、クロスエンボディサンプルで事前学習されており、堅牢なエンボディ動力学を学習し、強固な実世界汎化性能を達成します。私たちは、11の多様かつ複数ステップの実世界タスクからなるベンチマークでフレームワークを評価しました。平均成功率は87.4％という結果を示し、これは$\pi_0$ベースライン（46.5％）に対して+40.9％の絶対的な改善、およびテキストサブタスクガイダンスで強化された$\pi_0$（57.1％）に対して+30.3％の絶対的な改善を示しました。
</details>

<details>
<summary> 英語要旨 </summary>

Vision-Language-Action (VLA) models convert abstract language instructions into concrete, executable actions, a task that is especially challenging in open-world environments. We present \textit{Visually Grounded Planning}, a general and efficient high-level planner that guides a VLA step-by-step using imagined future observations and subtask descriptions. With an imagined future observation, the VLA can focus on visuomotor inference rather than high-level semantic reasoning, leading to improved accuracy and generalization. Our planner comprises a highly efficient foresight image-generation module that predicts a high-quality 640×480 future observation from the current visual input and language instruction within only 0.33 s on an H100 GPU, together with a vision–language component that reasons over the task and produces subtask descriptions for both the generator and the VLA. Importantly, state-of-the-art VLAs can integrate our planner seamlessly by simply augmenting their visual inputs, without any architectural modification. The foresight generator is pretrained on approximately 10 million multi-task, cross-embodiment samples, enabling it to learn robust embodied dynamics and achieve strong real-world generalization. We evaluate our framework on a benchmark consists of 11 diverse, multi-step real-world tasks. It achieves an average success rate of 87.4\%, demonstrating a +40.9\% absolute improvement over the $\pi_0$ baseline (46.5\%) and a +30.3\% absolute improvement over $\pi_0$ augmented with textual subtask guidance (57.1\%).
</details>

---

### Granulon: Awakening Pixel-Level Visual Encoders with Adaptive Multi-Granularity Semantics for MLLM
著者: Junyuan Mao, Qiankun Li, Linghao Meng, Zhicheng He, Xinliang Zhou, Kun Wang, Yang Liu, Yueming Jin

<details>
<summary> 日本語要旨 </summary>

最近のマルチモーダル大規模言語モデル（MLLM）は、主にCLIPベースのビジュアルエンコーダーを利用しており、これらはグローバルなセマンティックな整合性に重点を置いていますが、細部までの視覚的理解に苦労しています。一方、DINOv3は強力なピクセルレベルの知覚能力を提供しますが、粗いグラニュラリティのセマンティック抽象化が欠けており、多重グラニュラリティに基づく推論が限定されます。このギャップを埋めるために、私たちはDINOv3ベースの新しいMLLMであるGranulonを提案します。これは適応的なグラニュラリティ拡張を備えています。Granulonは、テキスト条件付きのグラニュラリティコントローラーを導入し、これによりテキスト入力のセマンティックスコープに応じて視覚的抽象化レベルが動的に調整されます。また、適応型トークン集約モジュールを導入し、これはグラニュラリティガイド付きのプーリングと関係性に基づくクラスタリングを行い、コンパクトでセマンティックに豊かな視覚的トークンを生成します。この設計により、単一のフォワードパス内で「ピクセルから細部への粗い」推論が統合されます。広範かつ解釈可能な実験は、Granulonが正確性を30%向上させ、ハックションを20%削減することを示しており、同一の設定下ですべてのビジュアルエンコーダーを凌駕します。コードは補足資料にあります。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advances in multimodal large language models largely rely on CLIP-based visual encoders, which emphasize global semantic alignment but struggle with fine-grained visual understanding. In contrast, DINOv3 provides strong pixel-level perception yet lacks coarse-grained semantic abstraction, leading to limited multi-granularity reasoning. To address this gap, we propose Granulon, a novel DINOv3-based MLLM with adaptive granularity augmentation. Granulon introduces a text-conditioned granularity Controller that dynamically adjusts the visual abstraction level according to the semantic scope of the textual input, and an Adaptive Token Aggregation module that performs granularity-guided pooling and relation-aware clustering to produce compact, semantically rich visual tokens. This design enables unified "pixel-to-fine-to-coarse" reasoning within a single forward pass. Extensive and interpretable experiments demonstrate that Granulon improves accuracy by 30% and reduces hallucination by 20%, outperforming all visual encoders under identical settings. Code is available at the Supplementary.
</details>

---

### Dual Ascent Diffusion for Inverse Problems
著者: Minseo Kim, Axel Levy, Gordon Wetzstein

<details>
<summary> 日本語要旨 </summary>

逆問題は、天体物理学から医用画像診断に至るまで多くの分野で基本的なものです。新たに登場した拡散モデルは、これらの問題を解決する強力な事前情報を提供します。しかし、既存の最大事後確率（MAP）や事後分布サンプリングアプローチは、異なる計算的近似に依存しており、不正確または非最適なサンプルを生じさせます。この問題に対処するために、私たちは拡散モデル事前情報を用いてMAP問題を解く新しいアプローチとして、二重昇降最適化フレームワークを導入します。このフレームワークは、画像復元問題における様々な指標での画質が向上し、高い測定ノイズレベルに対してもより頑健であり、速く、また観測をより忠実に表現する解を推定します。
</details>

<details>
<summary> 英語要旨 </summary>

Ill-posed inverse problems are fundamental in many domains, ranging from astrophysics to medical imaging. Emerging diffusion models provide a powerful prior for solving these problems. Existing maximum-a-posteriori (MAP) or posterior sampling approaches, however, rely on different computational approximations, leading to inaccurate or suboptimal samples. To address this issue, we introduce a new approach to solving MAP problems with diffusion model priors using a dual ascent optimization framework. Our framework achieves better image quality as measured by various metrics for image restoration problems, it is more robust to high levels of measurement noise, it is faster, and it estimates solutions that represent the observations more faithfully than the state of the art.
</details>

---

### Flow4DGS-SLAM: Optical Flow-Guided 4D Gaussian Splatting SLAM
著者: Yunsong Wang, Gim Hee Lee

<details>
<summary> 日本語要旨 </summary>

動的環境の処理は、視覚的な同時位置推定と地図作成（SLAM）における重要な研究課題です。最近の研究では、3Dガウススプラッティング（3DGS）をSLAMと組み合わせて、堅牢なカメラ姿勢推定と写実的なレンダリングを達成しています。しかし、効率的に静的および動的領域の両方を再構築することは依然として課題です。本研究では、光流によって導かれる動的3DGS SLAMの効率的なフレームワークを提案します。入力深度と事前の光流を使用して、まずカメラエゴモーションモデルに適合させて光流を分解することで、カテゴリー非依存の動きマスク生成戦略を提案します。このモジュールは動的および静的なガウシアンを分離し、同時に光流に基づくカメラ姿勢初期化を提供します。キーフレームでのその時間中心を明示的にモデル化することで、動的3DGSのトレーニング速度を向上させます。これらの中心は3次元シーンフローの事前情報を用いて伝播され、適応的な挿入戦略によって動的に初期化されます。また、時間的不透明度と回転をガウス混合モデル（GMM）でモデル化し、複雑なダイナミクスを適応的に学習します。実験結果は、追跡、動的再構築、トレーニング効率の分野で我々の最先端の性能を示しています。論文が受理された際にコードを公開します。
</details>

<details>
<summary> 英語要旨 </summary>

Handling the dynamic environments is a significant research challenge in Visual Simultaneous Localization and Mapping (SLAM). Recent research combines 3D Gaussian Splatting (3DGS) with SLAM to achieve both robust camera pose estimation and photorealistic renderings. However, using SLAM to efficiently reconstruct both static and dynamic regions remains challenging. In this work, we propose an efficient framework for dynamic 3DGS SLAM guided by optical flow. Using the input depth and prior optical flow, we first propose a category-agnostic motion mask generation strategy by fitting a camera ego-motion model to decompose the optical flow. This module separates dynamic and static Gaussians and simultaneously provides flow-guided camera pose initialization. We boost the training speed of dynamic 3DGS by explicitly modeling their temporal centers at keyframes. These centers are propagated using 3D scene flow priors and are dynamically initialized with an adaptive insertion strategy. Alongside this, we model the temporal opacity and rotation using a Gaussian Mixture Model (GMM) to adaptively learn the complex dynamics. The empirical results demonstrate our state-of-the-art performance in tracking, dynamic reconstruction, and training efficiency. Our code will be made publicly available upon paper acceptance.
</details>

---

### Multimodal RewardBench 2: Evaluating Omni Reward Models for Interleaved Text and Image
著者: Yushi Hu, Reyhane Askari, Melissa Hall, Emily Dinan, Luke Zettlemoyer, Marjan Ghazvininejad

<details>
<summary> 日本語要旨 </summary>

大規模言語モデル（LLM）のトレーニングには報酬モデル（RMs）が不可欠ですが、画像とテキストシーケンスを交互に扱うオムニモデルに対してはまだ十分に探求されていません。私たちはMultimodal RewardBench 2（MMRB2）を導入し、これは多様な理解と（交互の）生成における報酬モデルの包括的なベンチマークとして初めて登場します。MMRB2は4つのタスクをカバーしています：テキストから画像へ、画像編集、交互生成、および多様な推論（「画像で考える」）、それぞれのタスクに対し23モデルとエージェントを含む21のソースタスクから1,000組の専門家アノテーションされた好みペアを提供します。MMRB2は以下のように設計されています：（1）実用的でありながら挑戦的なプロンプト、（2）最先端のモデルとエージェントからの応答、および（3）強い人間専門家コンセンサスを持つ好みペアで、これらは集合フィルタリング戦略によってキュレーションされています。MMRB2を使用して、各サブタスクの既存の裁判官を研究しました。これには多様なLLM-as-a-judgeと人間の好みでトレーニングされたモデルが含まれます。GPT-5やGemini-2.5-Proのようなトップ裁判官は66～75％の精度に達し、これは人間の>90％と比較され、一般的に使用されるGPT-4o（59％の精度）を上回ります。最も優れたパフォーマンスを発揮するオープンソースモデルQwen3-VL-32Bは、Gemini-2.5-Flash（64％）と同様の精度を達成します。また、MMRB2のパフォーマンスが下流タスクの成功と強く相関していることも示しました。さらに詳細な分析を行うことで、報酬モデルを改善するための重要な領域を明らかにしました。
</details>

<details>
<summary> 英語要旨 </summary>

Reward models (RMs) are essential for training large language models (LLMs), but remain underexplored for omni models that handle interleaved image and text sequences. We introduce Multimodal RewardBench 2 (MMRB2), the first comprehensive benchmark for reward models on multimodal understanding and (interleaved) generation. MMRB2 spans four tasks: text-to-image, image editing, interleaved generation, and multimodal reasoning (“thinking-with-images”), providing 1,000 expert-annotated preference pairs per task from 23 models and agents across 21 source tasks. MMRB2 is designed with: (1) practical but challenging prompts; (2) responses from state-of-the-art models, and agents; and (3) preference pairs with strong human-expert consensus, curated via an ensemble filtering strategy. Using MMRB2, we study existing judges for each subtask, including multimodal LLM-as-a-judge and models trained with human preferences. Top judges like GPT-5 and Gemini-2.5-Pro reach 66–75% accuracy, compared to >90% for humans, and outperform the commonly used GPT-4o (59% accuracy). The best performing open-source model Qwen3-VL-32B achieves similar accuracies as Gemini-2.5-Flash (64%). We also show that MMRB2 performance strongly correlates with downstream task success, and conduct an in-depth analysis that shows key areas to improve the reward models going forward.
</details>

---

### HumanNOVA: Photorealistic, Universal and Rapid 3D Human Avatar Modeling from A Single Image
著者: Hezhen Hu, Wangbo Zhao, Lanqing Guo, Hanwen Jiang, Jonathan Liu, Zhiwen Fan, Kai Wang, Zhangyang Wang, Georgios Pavlakos

<details>
<summary> 日本語要旨 </summary>

本論文では、単一のRGB画像から生成されるリアルな3D人間アバターモデルであるHumanNOVAを紹介します。このモデルは汎用性が高く、かつ迅速に動作します。フォトリアリズムと一般化の両立は、多様な高品質3D人間データの不足により困難です。この問題を解決するため、2つの戦略に基づくスケーラブルなデータ生成パイプラインを構築しました。第一の戦略は既存のリグ付きアセットを利用し、日常生活で見られる広範囲のポーズでアニメーション化することです。第二の戦略は既存のマルチカメラによる人間のキャプチャを利用し、フィッティングを通じてトレーニング用の多様なビューを生成することです。これらの戦略により、データ量および多様性が大幅に向上し、100,000アセットまでスケールアップすることが可能になりました。アーキテクチャについては、HumanNOVAはトークン条件付きのフィードフォワード型アバターモデリングフレームワークを採用しており、1秒未満での高速推論が可能であり、テスト時の最適化は不要です。入力画像と詳細な幾何学や外観を持たない単純化された人間メッシュ（SMPL）からモデルは両方の入力をコンパクトなトークン表現にエンコードします。これらのトークンは条件付き信号として機能し、クロスアテンションを通じて融合され、トライプレーンベースの3Dアバターレプリゼンテーションが構築されます。多数のベンチマークにおける広範な実験は、私たちのアプローチの優位性を定量的・定性的に示し、さまざまな入力画像条件下での堅牢性も確認しています。
</details>

<details>
<summary> 英語要旨 </summary>

In this paper, we present HumanNOVA, a photorealistic, universal, and rapid model for generating 3D human avatars from a single RGB image. Achieving both photorealism and generalization is challenging due to the scarcity of diverse, high-quality 3D human data. To address this, we build a scalable data generation pipeline that follows two strategies. The first one is to leverage existing rigged assets and animate them with extensive poses from daily life. The second strategy is to utilize existing multi-camera captures of humans and employ fitting to generate more diverse views for training. These two strategies enable us to scale up to 100k assets, significantly enhancing both the quantity and the diversity of data for robust model training. In terms of the architecture, HumanNOVA adopts a feed-forward, token-conditioned avatar modeling framework that allows fast inference in less than one second and requires no test-time optimization. Given an input image and an estimated simplified human mesh (SMPL) without detailed geometry or appearance, the model first encodes both inputs into compact token representations. These tokens then act as conditioning signals and are fused through cross-attention to construct a triplane-based 3D avatar representation. Extensive experiments on multiple benchmarks demonstrate the superiority of our approach, both quantitatively and qualitatively, as well as its robustness under diverse input image conditions.
</details>

---

### Mesh4D: 4D Mesh Reconstruction and Tracking from Monocular Video
著者: Zeren Jiang, Chuanxia Zheng, Iro Laina, Diane Larlus, Andrea Vedaldi

<details>
<summary> 日本語要旨 </summary>

私たちは、単眼ビデオからの動的な対象のモノリシック4Dメッシュ再構築用にMesh4Dというフィードフォワードモデルを提案します。このモデルは、対象の完全な3D形状および動きを変形場として再構築します。私たちの主要な貢献は、全アニメーションシーケンスを一度でエンコードするコンパクトなラテント空間です。このラテント空間は、訓練中に教師データの骨格構造によって導かれる自己符号化器によって学習されます。これにより、可能な変形に対する強い事前情報が提供されます。重要なことに、推論時には骨格情報を必要としません。エンコーダーはスペースタイム注意機構を用いており、対象の全体的な変形のより安定した表現を得ることができます。この表現に基づき、入力ビデオおよび最初のフレームから再構築されたメッシュに条件付けられたラテント拡散モデルを訓練します。このモデルは全アニメーションを一発で予測します。Mesh4Dの評価は、再構築および新視点合成のベンチマークにおいて行われ、正確な3D形状と変形を回復する点で既存手法を上回りました。
</details>

<details>
<summary> 英語要旨 </summary>

We propose Mesh4D, a feed-forward model for monocular 4D mesh reconstruction. Given a monocular video of a dynamic object, our model reconstructs the object’s complete 3D shape and motion, represented as a deformation field. Our key contribution is a compact latent space that encodes the entire animation sequence in a single pass. This latent space is learned by an autoencoder that, during training, is guided by the skeletal structure of the training objects, providing strong priors on plausible deformations. Crucially, skeletal information is not required at inference time. The encoder employs spatio-temporal attention, yielding a more stable representation of the object’s overall deformation. Building on this representation, we train a latent diffusion model that, conditioned on the input video and the mesh reconstructed from the first frame, predicts the full animation in one shot. We evaluate Mesh4D on reconstruction and novel view synthesis benchmarks, outperforming prior methods in recovering accurate 3D shape and deformation.
</details>

---

### DiP: Taming Diffusion Models in Pixel Space
著者: Zhennan Chen, junwei zhu, Xu Chen, Jiangning Zhang, Xiaobin Hu, Hanzhen Zhao, Chengjie Wang, Jian Yang, Ying Tai

<details>
<summary> 日本語要旨 </summary>

拡散モデルは、生成品質と計算効率の間で基本的なトレードオフに直面しています。潜在空間拡散モデル（LDMs）は効率的な解決策を提供しますが、情報損失やエンド・ツー・エンドのトレーニング不足といった問題に直面しています。一方で、既存のピクセル空間モデルはVAEを回避しますが、高解像度合成では計算コストが大きすぎます。このジレンマを解決するために、私たちは効率的なピクセル空間拡散フレームワークであるDiPを提案します。DiPは生成プロセスをグローバルとローカルの2段階に分離します：Diffusion Transformer（DiT）バックボーンが大きなパッチ上で効率的にグローバル構造を構築し、一方で軽量なPatch Detailer Headは文脈特徴を活用して細部の詳細を復元します。この協調設計により、VAEに依存せずLDMsと同等の計算効率を達成します。DiPは以前の方法に比べて最大10倍速い推論スピードでありながら、パラメータ数をわずか0.3％増加させるだけで、ImageNet 256×256において1.90のFIDスコアを達成します。
</details>

<details>
<summary> 英語要旨 </summary>

Diffusion models face a fundamental trade-off between generation quality and computational efficiency. Latent Diffusion Models (LDMs) offer an efficient solution but suffer from potential information loss and non-end-to-end training. In contrast, existing pixel space models bypass VAEs but are computationally prohibitive for high-resolution synthesis. To resolve this dilemma, we propose DiP, an efficient pixel space diffusion framework. DiP decouples generation into a global and a local stage: a Diffusion Transformer (DiT) backbone operates on large patches for efficient global structure construction, while a co-trained lightweight Patch Detailer Head leverages contextual features to restore fine-grained local details. This synergistic design achieves computational efficiency comparable to LDMs without relying on a VAE. DiP is accomplished with up to 10$\times$ faster inference speeds than previous method while increasing the total number of parameters by only 0.3\%, and achieves an 1.90 FID score on ImageNet 256$\times$256.
</details>

---

### OmniDocLayout: Towards Diverse Document Layout Generation Via Coarse-to-Fine LLM Learning
著者: Hengrui Kang, Zhuangcheng Gu, Zhiyuan Zhao, Zichen Wen, Bin Wang, Weijia Li, Conghui He

<details>
<summary> 日本語要旨 </summary>

ドキュメントAIは急速に進化し、注目を集めています。しかし、多くの努力が文書レイアウト分析（DLA）に向けられている一方で、その生成的な対応であるレイアウト生成は未だ十分に探求されていません。従来のグラフィックレイアウトデザインや部屋のレイアウト計画と異なり、文書レイアウト生成は通常、ページあたりの要素数が多く、構造的にも多様性と複雑さを示します。現在の主な障害は、多様な文書レイアウトの不足です：既存の研究ではマンハッタンスタイルの学術論文が支配的であり、新聞や雑誌といったオープンワールドジャンルは極端に代表されていません。このギャップを埋めるために、私たちはOmniDocLayout-1Mをキュレーションしました。これは多様な文書レイアウトの初の百万規模データセットであり、6つの一般的なドキュメントタイプをカバーし、複数のソースから収集された現代的なレイアウトを含んでいます。また、既存の方法が複雑な領域で苦戦し、長いシーケンスを整然と配置することにしばしば失敗するため、私たちはOmniDocLayout-LLMという0.5Bモデルを導入します。これは設計された二段階のCoarse-to-Fine学習パラダイムを持っています：1）我々のデータセットから粗いカテゴリ定義で普遍的なレイアウト原則を学ぶ、2）少数の細かく注釈付きサンプルを用いて特定のドメインに知識を転移する。広範囲の実験は、私たちのアプローチがM$^6$Docデータセットの複数のドメインで強力な性能を達成し、既存のレイアウト生成専門家および最新の一般的なLLMsを大幅に上回ることを示しています。私たちのコード、データセット、モデルは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Document AI has advanced rapidly and is attracting increasing attention. Yet, while most efforts have focused on document layout analysis (DLA), its generative counterpart, layout generation, remains underexplored. Distinct from traditional graphic layout design and room layout planning, document layout generation typically involves a larger number of elements per page and exhibits greater structural diversity and complexity. Currently, a major obstacle lies in the scarcity of diverse document layouts: academic papers with Manhattan-style structures dominate existing studies, while open-world genres such as newspapers and magazines remain severely underrepresented. To address this gap, we curate OmniDocLayout-1M, the first million-scale dataset of diverse document layouts, covering six common document types and comprising contemporary layouts collected from multiple sources. Moreover, since existing methods struggle in complex domains and often fail to arrange long sequences coherently, we introduce OmniDocLayout-LLM, a 0.5B model with designed two-stage Coarse-to-Fine learning paradigm: 1) learning universal layout principles from our dataset with coarse category definitions, and 2) transferring the knowledge to a specific domain with few fine-grained annotated samples. Extensive experiments demonstrate that our approach achieves strong performance on multiple domains in M$^6$Doc dataset, substantially surpassing both existing layout generation experts and several latest general-purpose LLMs. Our code, dataset, and models will be publicly released.
</details>

---

### JarvisEvo: Towards A Self-Evolving Photo Editing Agent with Synergistic Editor-Evaluator Optimization
著者: yunlong lin, Linqing Wang, Kunjie Lin, Zixu Lin, Kaixiong Gong, Wenbo Li, Bin Lin, Zhenxi Li, Shiyi Zhang, Yuyang Peng, Wenxun Dai, Xinghao Ding, Chunyu Wang, qinglin lu

<details>
<summary> 日本語要旨 </summary>

エージェントベースの編集モデルは、インタラクティブな体験、処理品質、創造的な柔軟性を大幅に向上させてきました。しかし、2つの重要な課題が残っています：（1）指示ハロゲン化—テキストのみのチェーン・オブ・シンク（CoT）推論は、固有の情報ボトルネックにより事実誤りを完全に防ぐことができません；（2）リワードハッキング—動的なポリシー最適化は静的なリワードモデルに対して行われ、エージェントが報酬関数の欠陥を悪用することを可能にします。これらの問題に対処するために、私たちは専門家人間デザイナーを模倣し、反復的な編集、適切なツールの選択、結果の評価、および自己の意思決定についての反省を通じて成果を洗練する統一された画像編集エージェントであるJarvisEvoを提案します。JarvisEvoは3つの主要な利点を提供します：（1）指示に従うことと編集品質を向上させるインターレイド型マルチモーダルチェーン・オブ・シンク（iMCoT）推論メカニズム；（2）外部リワードなしでの自己改善を可能にし、効果的にリワードハッキングを緩和するシナジスティック・エディター–イベーテーター政策最適化（SEPO）フレームワーク；および（3）Adobe LightroomとQwen-Image-Editツールのシームレスな統合による保存型および生成型編集のサポート。ArtEdit-Benchでは、JarvisEvoが平均18.95%向上し、保存型編集メトリクスでNano-Bananaを上回りました。これには、ピクセルレベルのコンテンツ忠実度で44.96%という大幅な改善が含まれますが、生成型編集タスクでも競争力のあるパフォーマンスを維持しています。
</details>

<details>
<summary> 英語要旨 </summary>

Agent-based editing models have substantially advanced interactive experiences, processing quality, and creative flexibility. However, two critical challenges persist: (1) instruction hallucination—text-only chain-of-thought (CoT) reasoning cannot fully prevent factual errors due to inherent information bottlenecks; (2) reward hacking—dynamic policy optimization against static reward models allows agents to exploit flaws in reward functions. To address these issues, we propose JarvisEvo, a unified image editing agent that emulates an expert human designer by iteratively editing, selecting appropriate tools, evaluating results, and reflecting on its own decisions to refine outcomes. JarvisEvo offers three key advantages: (1) an interleaved multimodal chain-of-thought (iMCoT) reasoning mechanism that enhances instruction following and editing quality; (2) a synergistic editor–evaluator policy optimization (SEPO) framework that enables self-improvement without external rewards, effectively mitigating reward hacking; and (3) support for both preservative and generative editing through seamless integration of Adobe Lightroom and Qwen-Image-Edit tools. On ArtEdit-Bench, JarvisEvo outperforms Nano-Banana by an average of 18.95% on preservative editing metrics, including a substantial 44.96% improvement in pixel-level content fidelity, while maintaining competitive performance in generative editing tasks.
</details>

---

### FlexiVideo: Variation-Aware Temporal Dynamics Modeling for Efficient Video Understanding
著者: Da Peng, Xuesong Yang, Zonghao Guo, Yichen Zhang, Chi Chen, Yidan Zhang, Yuan Yao, Fang Wan, Wei Ke, Maosong Sun

<details>
<summary> 日本語要旨 </summary>

自然な動画は、高ダイナミックなシーンの移行を伴うセグメントと低ダイナミックな視覚的変化が支配するセグメントによって異質な時間的ダイナミクスを示します。しかし、ほとんどのMLLM（マルチタスク・ラーニング・ランゲージ・モデル）ではすべてのフレームを同様に扱うことが一般的であり、これにより冗長な視覚エンコードが発生し、大きな計算オーバーヘッドが生じます。最新のトップモデルであるQwen2.5-VLは固定の2フレームエンコーディングスキームを採用していますが、私たちのパイロット実験では、高ダイナミックなフレームペアにおいて視覚的混乱問題に直面することが示されました。この問題を解決するために、私たちはFlexiVideoを提案します。これは、時間的ダイナミクスを視覚変動を利用してモデル化する効率的なMLLMです。FlexiVideoはまず適応的な時間セグメンテーションモジュールを使用してフレーム間の差異を推定し、連続したフレームを微細な視覚変化を持つシーンセグメントにグループ化します。次に、ダイナミカルスパースタイムエンティングモジュールがシーンレベルのエンコード用の時間ウィンドウを調整します。構造化された時間的組織内でシーンレベルの視覚表現を再構築することにより、私たちのアプローチはダイナミクスをより効果的にモデル化し、エンコード負荷を削減しつつ微細な視覚変動を保持します。広範囲の実験では、FlexiVideo-3Bが6つの一般的なビデオベンチマークでQwen2.5-VL-3Bを一貫して上回ることが示されました。特に、MotionBenchで10FPSで評価した場合、FlexiVideo-3BはQwen2.5-VL-3Bに比べて視覚トークンを43.5%削減しつつ1.3%のパフォーマンス向上を達成し、効率と有効性の間で大幅に優れたバランスを実現しています。コードとチェックポイントは近日中にリリースされます。
</details>

<details>
<summary> 英語要旨 </summary>

Natural videos exhibit heterogeneous temporal dynamics, with certain segments undergoing high-dynamic scene transitions and others dominated by low-dynamic visual changes. However, treating all frames identically, a common practice in most MLLMs, leads to redundant visual encoding, which results in significant computational overhead. The recent state-of-the-art model, i.e., Qwen2.5-VL, adopts a fixed two-frame encoding scheme, but our pilot experiments indicate that it encounters a visual confusion problem under high-dynamic frame pairs. To address this issue, we propose FlexiVideo, an efficient MLLM that models temporal dynamics leveraging visual variation. FlexiVideo first employs an adaptive temporal segmentation module to estimate inter-frame differences, grouping consecutive frames into scene segments with subtle visual changes. Subsequently, a dynamical spatio-temporal embedding module adjusts the temporal window for scene-level encoding. By restructuring scene-level visual representations within a structured temporal organization, our approach models dynamics more effectively and reduces the encoding burden while preserving fine-grained visual variations. Extensive experiments show that FlexiVideo-3B consistently outperforms Qwen2.5-VL-3B across 6 general video benchmarks. Notably, when evaluated on MotionBench at 10 FPS, FlexiVideo-3B reduces visual tokens by 43.5% compared with Qwen2.5-VL-3B while achieving a 1.3% performance gain, striking a significantly better balance between efficiency and effectiveness. Code and checkpoints will be released soon.
</details>

---

### CHIRP Dataset: Towards Long-term, Individual-level, Behavioural Monitoring of Bird Populations in The Wild
著者: Alex Hoi Hang Chan, Neha Singhal, Onur Kocahan, Andrea Meltzer, Saverio Lubrano, Miya Warrington, Michael Griesser, Fumihiro Kano, Hemal Naik

<details>
<summary> 日本語要旨 </summary>

個体動物の長期的な行動監視は、特に保全生物学や進化生物学において、異なる時間スケールで発生する行動変化を研究するために重要です。コンピュータビジョン手法は生物多様性の監視に有益であることが示されていますが、野生集団における自動化された行動監視は依然として課題です。これは、個体動物から生物学的に意味のある測定を抽出するために必要なコンピュータビジョンタスクの範囲をカバーしたデータセットが不足していることに起因します。本研究では、そのようなデータセット（CHIRP）と野生鳥類の個体再識別のための新しい方法（CORVID）を紹介します。CHIRP（Combining beHaviour, Individual Re-identification and Postures）データセットは、スウェーデン・ラップランドで研究されている野生のシベリアジャイアントバケツカラーの長期集団から収集され、再識別（re-id）、行動認識、2Dキーポイント推定、物体検出、インスタンスセグメンテーションをサポートしています。従来のタスク固有のベンチマークに加えて、生物学的に関連する指標（摂食率、共起率）を用いたアプリケーション固有のベンチマークを導入し、実際の使用例でモデルのパフォーマンスを評価します。最後に、色付き脚環のセグメンテーションと分類に基づく鳥類の個体識別のための新しいパイプライン（CORVID）を紹介します。これは、広く使用されている視覚的な個体識別手法です。CORVIDは検出された色環の組み合わせをデータベースとマッチングすることで確率に基づくID追跡方法を提供します。アプリケーション固有のベンチマークを用いて、CORVIDが最先端のre-id手法を上回ることを示します。本研究がコンピュータビジョン研究と生物学的応用の間に橋渡しするための、倫理的承認された生物学的研究から実際のデータセットをキュレートするためのコミュニティへの青写真となることを願っています。
</details>

<details>
<summary> 英語要旨 </summary>

Long-term behavioural monitoring of individual animals is crucial for studying behavioural changes that occurs over different time scales, especially for conservation and evolutionary biology. Computer vision methods have proven to benefit biodiversity monitoring, but automated behaviour monitoring in wild populations remains challenging. This stems from the lack of datasets that cover a range of computer vision tasks necessary to extract biologically meaningful measurements of individual animals. Here, we introduce such a dataset (CHIRP) with a new method (CORVID) for individual re-identification of wild birds. The CHIRP (Combining beHaviour, Individual Re-identification and Postures) dataset is curated from a long-term population of wild Siberian jays studied in Swedish Lapland, supporting re-identification (re-id), action recognition, 2D keypoint estimation, object detection, and instance segmentation. In addition to traditional task-specific benchmarking, we introduce application-specific benchmarking with biologically relevant metrics (feeding rates, co-occurrence rates) to evaluate the performance of models in real-world use cases. Finally, we present CORVID (COlouR-based Video re-ID), a novel pipeline for individual identification of birds based on the segmentation and classification of coloured leg rings, a widespread approach for visual identification of individual birds. CORVID offers a probability-based id tracking method by matching the detected combination of colour rings with a database. We use application-specific benchmarking to show that CORVID outperforms state of the art re-id methods. We hope this work offers the community a blueprint for curating real-world datasets from ethically approved biological studies to bridge the gap between computer vision research and biological applications.
</details>

---

### Zero-Shot Reconstruction of Animatable 3D Avatars with Cloth Dynamics from A Single Image
著者: Joohyun Kwon, Geonhee Sim, Gyeongsik Moon

<details>
<summary> 日本語要旨 </summary>

既存の単一画像に基づく3Dヒューマンアバター生成手法は、主に剛体ジョイント変換を利用しており、リアルな衣服動態のモデリングが制限されています。本論文では、単一画像から運動依存型の衣服動態を持つアニメーション可能な3Dヒューマンアバターを再構築するゼロショットフレームワークである「DynaAvatar」を提案します。大規模多人数運動データセットでトレーニングされたDynaAvatarは、Transformerベースのフィードフォワードアーキテクチャを用いて、被験者特有の最適化なしにダイナミック3Dガウス変形を直接予測します。動的キャプチャが不足している問題を克服するため、静的から動的への知識転移戦略を導入しました：大規模な静的キャプチャで事前学習されたTransformerが強力な幾何学的および外観優先情報を提供し、動作依存変形に効率的に適応するために軽量LoRA微調整で動的キャプチャ上で行われます。さらに、レンダリング空間内の衣服動態に対して信頼性のある動き方向幾何学的手がかりを提供する光流–ガイド付き目的関数である「DynaFlow loss」を提案します。最後に、既存の動的キャプチャデータセットにおける欠落またはノイズのあるSMPL-Xフィッティングを再アノテーションしました。これらの公開されている多くの動的キャプチャデータセットには、高品質な3Dアバター再構築モデルのトレーニングに適さない不完全または信頼性の低いフィッティングが含まれています。実験結果は、DynaAvatarが視覚的に豊かで汎用性のあるアニメーションを生成し、既存手法を上回っていることを示しています。コード、予測モデル、再アノテーションはリリースされます。
</details>

<details>
<summary> 英語要旨 </summary>

Existing single-image 3D human avatar methods primarily rely on rigid joint transformations, limiting their ability to model realistic cloth dynamics. We present DynaAvatar, a zero-shot framework that reconstructs animatable 3D human avatars with motion-dependent cloth dynamics from a single image. Trained on large-scale multi-person motion datasets, DynaAvatar employs a Transformer-based feed-forward architecture that directly predicts dynamic 3D Gaussian deformations without subject-specific optimization. To overcome the scarcity of dynamic captures, we introduce a static-to-dynamic knowledge transfer strategy: a Transformer pretrained on large-scale static captures provides strong geometric and appearance priors, which are efficiently adapted to motion-dependent deformations through lightweight LoRA fine-tuning on dynamic captures. We further propose the DynaFlow loss, an optical flow–guided objective that provides reliable motion-direction geometric cues for cloth dynamics in rendered space. Finally, we reannotate the missing or noisy SMPL-X fittings in existing dynamic capture datasets, as most public dynamic capture datasets contain incomplete or unreliable fittings that are unsuitable for training high-quality 3D avatar reconstruction models. Experiments demonstrate that DynaAvatar produces visually rich and generalizable animations, outperforming prior methods. Code, pretrained models, and reannotations will be released.
</details>

---

### R2G：A Multi-View Circuit Graph Benchmark Suite from RTL to GDSII
著者: ZEWEI ZHOU, Jiajun Zou, Jiajia Zhang, Ao Yang, Ruichao He, Haozheng Zhou, Ao Liu, Jiawei Liu, Leilei Jin, Shan Shen, Daying Sun

<details>
<summary> 日本語要旨 </summary>

電子設計自動化（EDA）における機械学習の進展は、後期物理設計段階で同じ回路を一貫して表現するオープンなマルチビュー・グラフデータセットが不足していることによって制約されています。私たちは、DEFファイルをタイプ付きで異種の情報保存型回路グラフに変換し、配置および配線におけるノードレベルおよびエッジレベルのタスクをサポートする標準化されたベンチマークとフレームワークであるR2G（RTL-to-GDSII）を提示します。R2Gは情報平等性を持つ5つの段階認識ビューを提供し、ローダー、統一された分割、ドメイン固有の指標、再現可能なベースラインを含みます。これによりクロスビュー比較が公平に行えると同時に表現からモデリングを分離することができます。系統的な研究において古典的なGNN（GIN、GAT、GatedGCN）を用いた実験では、ビューの選択がパフォーマンスに強く影響し、段階や監督によって変動すること、デコーダヘッドの深さ（3〜4層）が精度と安定性を向上させることを示します。これらの発見はビューのセマンティクスを目的およびメッセージ伝達に結びつけ、実践的なガイダンスを提供します。EDAのセマンティクスとグラフ学習を橋渡しすることで、R2Gは大規模データセットとエンドツーエンドパイプラインをリリースし、原則に基づいた表現設計のオープンなテストベッドを作成します。データセット、ローダー、評価スクリプトはGitHubで公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Progress in machine learning for electronic design automation (EDA) is constrained by the lack of open, multi-view graph datasets that coherently represent the same circuits across late physical-design stages. We present R2G (RTL-to-GDSII), a standardized benchmark and framework that converts DEF files into typed, heterogeneous, information-preserving circuit graphs and supports node- and edge-level tasks in placement and routing. R2G provides five stage-aware views with information parity and includes loaders, unified splits, domain-specific metrics, and reproducible baselines—enabling fair cross-view comparison and isolating representation from modeling. In systematic studies with classic GNNs (GIN, GAT, GatedGCN), we show that view choice strongly affects performance, varies with stage and supervision, and that decoder-head depth (3--4 layers) improves accuracy and stability; these findings connect view semantics to objectives and message passing and offer practical guidance. By bridging EDA semantics and graph learning, R2G releases large-scale datasets and an end-to-end pipeline, creating an open testbed for principled representation design. Datasets, loaders, and evaluation scripts will be released on GitHub.
</details>

---

### MakeAnything: Harnessing Diffusion Transformers for Multi-Domain Procedural Sequence Generation
著者: Yiren Song, Cheng Liu, Mike Zheng Shou

<details>
<summary> 日本語要旨 </summary>

人間の知能の特徴の一つは、構造化された多段階プロセスを通じて複雑なアーティファクトを作成する能力です。AIによる手順的チュートリアルの生成は長年の目標でありますが、以下の3つの主要な障壁に直面しています：（1）多タスク手順データセットの不足、（2）各ステップ間の論理的連続性と視覚的一貫性を保つこと、および（3）複数のドメインにわたる汎用化。これらの課題に対処するため、私たちは21タスクをカバーし、24,000以上の手順的シーケンスを含むマルチドメインデータセットを提案します。この基盤の上で、拡散変換器（DIT）に基づくフレームワーク「MakeAnything」を導入し、DITのコンテキスト内能力を活用して一貫した手順的シーケンスを生成するために微調整を利用します。また、画像生成における非対称低ランク適応（LoRA）を導入し、エンコーダーのパラメータを固定しつつデコーダ層を適応的に調整することで、汎用化能力とタスク特有の性能のバランスを取ります。さらに、ReCraftモデルは空間時間的一貫性制約を通じて画像からプロセス生成を可能にし、静止画像を妥当な作成シーケンスに分解できるようにします。広範囲の実験により、MakeAnythingが既存手法を上回り、手順生成タスクにおける新たなパフォーマンス基準を設定することを示しました。
</details>

<details>
<summary> 英語要旨 </summary>

A hallmark of human intelligence is the ability to create complex artifacts through structured multi-step processes. Generating procedural tutorials with AI is a longstanding but challenging goal, facing three key obstacles: (1) scarcity of multi-task procedural datasets, (2) maintaining logical continuity and visual consistency between steps, and (3) generalizing across multiple domains. To address these challenges, we propose a multi-domain dataset covering 21 tasks with over 24,000 procedural sequences. Building upon this foundation, we introduce MakeAnything, a framework based on the diffusion transformer (DIT), which leverages fine-tuning to activate the in-context capabilities of DIT for generating consistent procedural sequences. We introduce asymmetric low-rank adaptation (LoRA) for image generation, which balances generalization capabilities and task-specific performance by freezing encoder parameters while adaptively tuning decoder layers. Additionally, our ReCraft model enables image-to-process generation through spatiotemporal consistency constraints, allowing static images to be decomposed into plausible creation sequences. Extensive experiments demonstrate that MakeAnything surpasses existing methods, setting new performance benchmarks for procedural generation tasks.
</details>

---

### OpenVision 2: A Family of Generative Pretrained Visual Encoders for Multimodal Learning
著者: Yanqing Liu, Xianhang li, Letian Zhang, Zirui Wang, Zeyu Zheng, Yuyin Zhou, Cihang Xie

<details>
<summary> 日本語要旨 </summary>

この論文では、OpenVisionのアーキテクチャと損失設計を簡素化し、そのトレーニング効率を向上させる方法について述べています。CapPaやAIMv2などの先行するビジョン言語事前学習作業およびLLaVAのような現代的なマルチモーダル設計に続き、我々の変更はシンプルです：テキストエンコーダー（したがって対比損失）を削除し、純粋に生成的なトレーニング信号としてキャプショニング損失のみを保持します。この新バージョンをOpenVision 2と名付けました。初期結果は有望です：この簡素化にもかかわらず、OpenVision 2は元のモデルのパフォーマンスと競合しつつ、広範なマルチモーダルベンチマークで優れた結果を示しました。また、トレーニング時間やメモリ消費量も大幅に削減されています。例えば、ViT-L/14ではトレーニング時間が約1.5倍（83時間から57時間）、メモリ使用量が約1.8倍（24.5GBから13.8GB）削減され、最大バッチサイズも2,000から8,000に増加しました。この優れたトレーニング効率は、OpenVisionで使用されている最大のビジョンエンコーダーを超えてスケールアップすることも可能にします（1億パラメータ以上）。我々はこの軽量かつ生成的なみのパラダイムが、マルチモーダルファウンデーションモデルにおける将来のビジョンエンコーダー開発にとって魅力的であると強く信じています。
</details>

<details>
<summary> 英語要旨 </summary>

This paper provides a simplification on OpenVision's architecture and loss design for enhancing its training efficiency. Following the prior vision-language pretraining works CapPa and AIMv2, as well as modern multimodal designs like LLaVA, our changes are straightforward: we remove the text encoder (and therefore the contrastive loss), retaining only the captioning loss as a purely generative training signal. We name this new version OpenVision 2. The initial results are promising: despite this simplification, OpenVision 2 competitively matches the original model's performance on a broad set of multimodal benchmarks while substantially cutting both training time and memory consumption. For example, with ViT-L/14, it reduces training time by about 1.5x (from 83h to 57h), and memory usage by about 1.8x (from 24.5GB to 13.8GB, equivalently allowing the maximum batch size to grow from 2k to 8k). This superior training efficiency also allows us to scale far beyond the largest vision encoder used in OpenVision, reaching more than 1 billion parameters. We hold a strong belief that this lightweight, generative-only paradigm is compelling for future vision encoder development in multimodal foundation models.
</details>

---

### Uncertainty-driven 3D Gaussian Splatting Active Mapping Via Anisotropic Visibility Field
著者: Shangjie Xue, Jesse Dill, Dhruv Ahuja, Frank Dellaert, Panagiotis Tsiotras, Danfei Xu

<details>
<summary> 日本語要旨 </summary>

私たちは、3DGSにおける不確実性の定量化とアクティブマッピングを行う新しいフレームワークであるGaussian Splatting Anisotropic Visibility Field（GAVIS）を提案します。私たちの主な洞察は、トレーニングビューから見えていない領域が3DGSによって信頼性の低い予測をもたらすということです。これに対処するために、トレーニングビューに関して各粒子の異方性可視性を定義し、球面調和関数で表現される3DGS内の可視性フィールドを定量化するための原理的かつ効率的な方法を導入します。得られた可視性フィールドは、不確実性に配慮したベイズネットワーク–ベースの体積レンダリングプロセスに統合され、合成ビューに対するリアルタイム（200 FPS）不確実性の定量化を可能にします。さらに、この形式に基づいて最大情報利得フレームワーク内でアクティブマッピングが行われます。多様な環境における広範囲の実験では、GAVISが精度と効率の両方で従来の手法を一貫してかつ顕著に上回っていることが示されました。さらに、スタンドアローン使用だけでなく、私たちの方法は既存の手法のパフォーマンス向上を後付けで適用することも可能です。
</details>

<details>
<summary> 英語要旨 </summary>

We present Gaussian Splatting Anisotropic Visibility Field (GAVIS), a novel framework for uncertainty quantification and active mapping in 3DGS. Our key insight is that regions unseen from the training views yield unreliable predictions from the 3DGS. To address this, we introduce a principled and efficient method for quantifying the visibility field in 3DGS, defined as the anisotropic visibility of each particle with respect to the training views, and represented using spherical harmonics. The resulting visibility field is integrated into a Bayesian Network–based uncertainty-aware volume rendering process, enabling real-time (200 FPS) uncertainty quantification for synthesized views. Active mapping is further performed within a maximum information gain framework building on this formulation. Extensive experiments across diverse environments demonstrate that GAVIS consistently and significantly outperforms prior approaches in both accuracy and efficiency. Moreover, beyond standalone use, our method can be applied post-hoc to improve the performance of existing approaches.
</details>

---

### Intrinsic Image Fusion for Multi-View 3D Material Reconstruction
著者: Peter Kocsis, Lukas Höllein, Matthias Nießner

<details>
<summary> 日本語要旨 </summary>

私たちは、多視点画像から高品質な物理ベースの材料を再構築する方法として「Intrinsic Image Fusion」を紹介します。材料の再構築は非常に制約が少なく、通常は費用がかかりノイズの多いパストレーシングを必要とする分析-合成法に依存しています。最適化をより制約付けるために、単一視点の事前知識を再構築プロセスに組み込みます。私たちは、各ビューごとに複数でありながらしばしば不整合な候補分解を生成する拡散ベースの材料推定器を利用します。この不整合を減少させるため、予測結果に明示的な低次元パラメトリック関数を適合させます。その後、最も一貫した予測と最も信頼性の高いビューからの予測を融合するために、柔軟な視点ごとの予測選択と信頼度ベースの多視点内部セットを用いた堅牢な最適化フレームワークを提案します。これにより、一貫したパラメトリック材料空間へと融合されます。最後に、低次元パラメータのために逆パストレーシングを用いて最適化します。私たちの結果は、シンセティックおよびリアルなシーンでの材料分離において、状態・オブ・ザ・アートの方法を上回り、高品質な再照明に適した鮮明かつクリーンな再構築を生み出します。
</details>

<details>
<summary> 英語要旨 </summary>

We introduce Intrinsic Image Fusion, a method that reconstructs high-quality physically based materials from multi-view images. Material reconstruction is highly underconstrained and typically relies on analysis-by-synthesis, which requires expensive and noisy path tracing. To better constrain the optimization, we incorporate single-view priors into the reconstruction process. We leverage a diffusion-based material estimator that produces multiple, but often inconsistent, candidate decompositions per view. To reduce the inconsistency, we fit an explicit low-dimensional parametric function to the predictions. We then propose a robust optimization framework using soft per-view prediction selection together with confidence-based soft multi-view inlier set to fuse the most consistent predictions of the most confident views into a consistent parametric material space. Finally, we use inverse path tracing to optimize for the low-dimensional parameters. Our results outperform state-of-the-art methods in material disentanglement on both synthetic and real scenes, producing sharp and clean reconstructions suitable for high-quality relighting.
</details>

---

### Efficient Hybrid SE(3)-Equivariant Visuomotor Flow Policy Via Spherical Harmonics for Robot Manipulation
著者: Qinglun Zhang, Shen Cheng, Tian Dan, Haoqiang Fan, Guanghui Liu, Shuaicheng Liu

<details>
<summary> 日本語要旨 </summary>

既存の等変換手法はデータ効率を向上させる一方で、高い計算コスト、単一モダリティ入力への依存性、および高速サンプリング方法と組み合わせた際の不安定性に悩まされています。本研究では、これら重要な制約を克服する新しいフレームワークであるE3Flowを提案します。E3Flowは効率的な修正流と安定した多様モダリティ等変換学習を初めて統合することに成功し、これらの課題を克服しています。我々のフレームワークは球面調和関数表現を基盤とし、厳密なSO(3)等変換性を保証します。また、点群と画像から構成されるハイブリッドビジュアルモダリティを動的に融合することで球面調和特徴に豊富な視覚情報を注入するための新しい不変特徴強化モジュール（FEM）を導入します。E3FlowはMimicGenベンチマークから8つの操作タスクとさらに4つの実世界実験でその有効性を検証しました。シミュレーション結果では、E3Flowが最先端の球面拡散ポリシー（SDP）に対して平均成功率で3.12%の改善を達成しつつ、同時に7倍の推論速度向上を実現しました。E3Flowはロボットポリシーラーニングにおけるパフォーマンス、効率性、データ効率の新たで非常に有効なトレードオフを示しています。コードとビデオは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

While existing equivariant methods enhance data efficiency, they suffer from high computational intensity, reliance on single-modality inputs, and instability when combined with fast-sampling methods. In this work, we propose E3Flow, a novel framework that addresses the critical limitations of equivariant diffusion policies. E3Flow overcomes these challenges, successfully unifying efficient rectified flow with stable, multi-modal equivariant learning for the first time. Our framework is built upon spherical harmonic representations to ensure rigorous SO(3) equivariance. We introduce a novel invariant Feature Enhancement Module (FEM) that dynamically fuses hybrid visual modalities (point clouds and images), injecting rich visual cues into the spherical harmonic features. We evaluate E3Flow on 8 manipulation tasks from the MimicGen benchmark and further conduct 4 real-world experiments to validate its effectiveness in physical environments. Simulation results show that E3Flow achieves a 3.12\% improvement in average success rate over the state-of-the-art Spherical Diffusion Policy (SDP) while simultaneously delivering a 7$\times$ inference speedup. E3Flow thus demonstrates a new and highly effective trade-off between performance, efficiency, and data efficiency for robotic policy learning. Code and videos will be released.
</details>

---

### OmniGen2: Towards Instruction-Aligned Multimodal Generation
著者: Chenyuan Wu, Jiahao Wang, PengFei Zheng, Ruiran Yan, Shitao Xiao, Xin Luo, Yueze Wang, Wanli Li, Xiyan Jiang, Yexin Liu, Junjie Zhou, Ziyi Xia, Ze Liu, Chaofan Li, Haoge Deng, Kun Luo, Bo Zhang, Jiajun Zhang, Dong Liu, Defu Lian, Xinlong Wang, Zhongyuan Wang, Tiejun Huang, Zheng Liu

<details>
<summary> 日本語要旨 </summary>

マルチモーダル生成モデルは、さまざまなモダリティの指示を処理し、画像生成タスクにおいて優れた性能を発揮します。しかし、複雑な実世界シナリオでの堅牢性は限定的であり、これは一般化された指示の整合性が不十分であるためです。私たちは、\textbf{OmniGen2}という複雑かつ詳細な指示に従うことを目的とした統一型マルチモーダルジェネレーターを導入します。私たちの主要な貢献は、まず強力で世界知識に基づいた基盤モデルを構築し、その後進行的なマルチタスク指示調整戦略を用いてそれを整合させる二段階の設計です。この基盤モデルは、柔軟なマルチモーダル生成に対応するための分離されたデコード機能と、学習効率を向上させる新しい位置エンコーディングスキームを備えた洗練されたアーキテクチャを特徴としています。私たちは大規模なデータ構築パイプラインを用いてこのモデルを実世界の知識に基づかせました。この基盤の上で、進行的な強化学習に基づく整合プロセスを提案します。このフェーズでは、トレーニングタスクと報酬信号を慎重にスケジュールし、クロストラックの知識転移を促進することで、モデルの指示従属能力を大幅に向上させます。私たちのモデルは標準的なベンチマークおよび専用のインコンテキスト生成ベンチマーク\textbf{OmniContext}で競争力のある性能を示します。私たちは、将来の研究におけるより高度な指示整合型ジェネレーティブモデルの構築を促進するために、モデル、コード、ベンチマーク、トレーニングデータセットを公開します。
</details>

<details>
<summary> 英語要旨 </summary>

Multimodal generative models can process instructions in various modalities and demonstrate outstanding performance across a wide range of image generation tasks. However, their robustness in complex real-world scenarios remains limited due to insufficient generalized instruction alignment. We introduces \textbf{OmniGen2}, a unified multimodal generator designed to follow complex, fine-grained instructions. Our core contribution is a two-stage design that first builds a strong, world-knowledge-grounded foundation model and then aligns it using a progressive, multi-task instruction tuning strategy. The foundation model features a streamlined architecture with decoupled decoding for versatile multimodal generation and a novel positional encoding scheme to improve learning efficiency. We ground this model in real-world knowledge using large-scale data construction pipelines. Building on this foundation, we propose a progressive, reinforcement-based alignment process. This phase carefully schedules training tasks and reward signals to foster cross-task knowledge transfer, significantly improving the model's instruction-following capabilities. Our models demonstrate competitive performance on standard benchmarks and our dedicated in-context generation benchmark, \textbf{OmniContext}. We will release our models, code, benchmark, and training datasets to catalyze future research in building more capable and instruction aligned generative models.
</details>

---

### Taming Generative Diffusion Model for Task-Oriented Infrared Imaging
著者: Tengyu Ma, Zhilong Dai, Yubo Diao, Guanming An, Long Ma, Jinyuan Liu, Risheng Liu

<details>
<summary> 日本語要旨 </summary>

赤外線（IR）画像は、厳しい環境下での知覚に欠かせないものですが、現実世界のデータはしばしば動的に結合した劣化によって汚染され、視覚品質と下流の意味理解の両方を損ないます。拡散モデルが強力な生成事前分布を提供する一方で、既存のアプローチはこの状況に適していません。その遅い多段階サンプリング、IR物理学と整合しないRGB駆動統計への依存、およびすべてのモデルパラメータを高コストで微調整する必要性が、動的なIR知覚には実用的ではありません。私たちは、IR修復を単一ステップ生成過程として再定式化する統一拡散フレームワークを提示します。その核心のアイデアは、劣化した入力を拡散軌道における特定の中間潜在状態と関連付けることであり、これによりモデルが単一かつ直接的な逆ステップを通じてクリーン画像を再構築することが可能になります。物理的現実性はさらに強化され、赤外線特有のスペクトル正則化を導入し、熱放射の特徴的エネルギー分布を保持します。動的IR知覚の多様で急速に変わる要求に対応するため、タスク認識型低ランク適応メカニズムをさらに開発しました。このメカニズムは軽量なプロンプティングハイパーネットワークを使用してコンパクトな変調パラメータを生成し、全体のネットワークを再訓練することなく迅速かつスケーラブルな適応能力を促進します。包括的な評価により、私たちのフレームワークが最先端の復元性能を達成し、信頼できる意味構造を維持し、多様なタスクと条件にわたって効果的に一般化する迅速な適応をサポートしていることが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

Infrared (IR) imaging is indispensable for perception in adverse environments, yet real-world data is often corrupted by dynamically coupled degradations that impair both visual quality and downstream semantic understanding. Although diffusion models offer powerful generative priors, existing approaches remain ill-suited to this setting. Their slow multi-step sampling, reliance on RGB-driven statistics misaligned with IR physics, and the necessity for costly fine-tuning of all model parameters render them impractical for dynamic IR perception. We present a unified diffusion framework that re-formulates IR restoration as a single-step generative process. The core idea is to associate each degraded input with a specific intermediate latent state in the diffusion trajectory, enabling the model to reconstruct the clean image via a single, direct reverse step. Physical realism is further reinforced through an IR-specific spectral regularization that preserves the characteristic energy distribution of thermal emissions. Addressing the diverse and rapidly shifting demands of dynamic IR perception, we further develop a task-aware low-rank adaptation mechanism. This mechanism employs a lightweight prompting hypernetwork to generate compact modulation parameters, facilitating rapid and scalable adaptation ability without retraining the entire network. Comprehensive evaluations demonstrate that our framework attains state-of-the-art restoration performance, preserves reliable semantic structures, and supports rapid adaptation that generalizes effectively across diverse tasks and conditions.
</details>

---

### ReasonMap: Towards Fine-Grained Visual Reasoning from Transit Maps
著者: Sicheng Feng, Song Wang, Shuyi Ouyang, Lingdong Kong, Zikai Song, Jianke Zhu, Huan Wang, Xinchao Wang

<details>
<summary> 日本語要旨 </summary>

多モーダル大規模言語モデル（MLLMs）は、セマンティックシーン理解とテキスト画像の整合性において顕著な進歩を示し、数学や論理を含むより複雑なタスクでのパフォーマンスが向上しています。しかし、細部までの視覚的理解と空間推論を必要とするタスクにおけるその能力は未だ十分に探求されていません。このギャップを埋めるため、我々はこれらの能力を評価するために特別に設計された新しいベンチマークであるReasonMapを導入します。ReasonMapは30都市の高解像度交通地図を含み、2種類の質問と3つのテンプレートにわたる1,008の質問応答ペアを提供しています。さらに、回答の正確性と品質を適切に評価する二段階の評価パイプラインを設計しました。16の人気MLLMsの包括的な評価では、意外な傾向が明らかになります：オープンソースモデルでは基本バリアントがその推論チューンされた対応物を上回る一方で、クローズドソースモデルでは逆の傾向が観察されます。さらなる分析により、ビジュアルマスキング設定下でも強力なパフォーマンスは直接的な視覚的根拠を必要とし、言語の優先事項だけに依存することはできないことが確認されました。さらに、強化ファインチューニングを用いたトレーニングベースラインを確立し、将来の探求の参考点を提供します。このベンチマーク研究が視覚的推論に新たな洞察をもたらし、オープンソースとクローズドソースモデルの間のギャップを調査する手助けとなることを期待しています。コードとデータサンプルは補足資料にあります。
</details>

<details>
<summary> 英語要旨 </summary>

Multimodal large language models (MLLMs) have demonstrated significant progress in semantic scene understanding and text-image alignment, with reasoning variants enhancing performance on more complex tasks involving mathematics and logic. However, their proficiency in tasks requiring both fine-grained visual understanding and spatial reasoning remains underexplored. To bridge this gap, we introduce ReasonMap, a novel benchmark specifically designed to evaluate these capabilities. ReasonMap encompasses high-resolution transit maps from 30 cities and includes 1,008 question-answer pairs spanning two question types and three templates. Furthermore, we design a two-level evaluation pipeline that properly assesses answer correctness and quality. Our comprehensive evaluation of 16 popular MLLMs reveals a counterintuitive pattern: among open-source models, base variants outperform their reasoning-tuned counterparts, whereas the opposite trend is observed in closed-source models. Further analysis under the visual-masking setting confirms that strong performance necessitates direct visual grounding, rather than relying solely on language priors. We further establish a training baseline with reinforcement fine-tuning, providing a reference for future exploration. We hope this benchmark study offers new insights into visual reasoning and helps investigate the gap between open- and closed-source models. Code and data samples are in the Supplementary.
</details>

---

### Beyond Ground-Truth: Leveraging Image Quality Priors for Real-World Image Restoration
著者: Fengyang Xiao, Peng Hu, Lei Xu, XingE Guo, Guanyi Qin, Yuqi Shen, Chengyu Fang, Rihan Zhang, Chunming He, Sina Farsiu

<details>
<summary> 日本語要旨 </summary>

現実世界の画像復元は、制御されていない条件下で撮影された劣化した低品質（LQ）入力から高品質（HQ）画像を復元することを目指しています。既存の方法は通常、グラウンドトゥルース（GT）による監督を前提とし、GTが完璧な参考品質を提供すると仮定します。しかし、GTにも一貫性のない知覚的忠実度を持つ画像が含まれており、モデルはトレーニングデータの平均品質レベルに収束する可能性があります。これにより、達成可能な最高の知覚的品質を実現できません。この問題に対処するために、我々は新しいフレームワークである**IQPIR**を提案します。これは、事前学習されたNo-Reference Image Quality Assessment（NR-IQA）モデルから抽出した画像品質優先度（IQP）を導入し、復元プロセスを明示的に知覚的に最適な出力に向けてガイドします。我々のアプローチは、以下の3つの重要なメカニズムを通じてIQPと学習されたコードブック優先度をシナジー的に統合します：(1) **品質条件付きトランスフォーマー**、ここではNR-IQAから導出されたスコアが予測表現を最大の知覚的品質に向けて誘導する条件信号として機能します。この設計は既存の復元アーキテクチャに対応し、構造変更なしでプラグアンドプレイの強化を提供します；(2) **デュアルブランチコードブック構造**、これは一般的な特徴とHQ固有の特徴を分離し、両方の一般的な構造情報と品質に敏感な属性を包括的に表現します；そして(3) **連続隠れ空間でよく観察される過剰最適化効果を軽減する**ための**離散表現ベースの品質最適化戦略**。実世界画像復元における広範な実験は、我々の方法がカットエッジ技術を超えただけでなく、既存の方法向けの汎用的な品質ガイド付き強化戦略としても機能することを示しています。コードはリリースされます。
</details>

<details>
<summary> 英語要旨 </summary>

Real-world image restoration aims to restore high-quality (HQ) images from degraded low-quality (LQ) inputs captured under uncontrolled conditions. Existing methods typically depend on ground-truth (GT) supervision, assuming that GT provides perfect reference quality. However, GT can still contain images with inconsistent perceptual fidelity, causing models to converge to the average quality level of the training data rather than achieving the highest perceptual quality attainable. To address these problems, we propose a novel framework, termed \textbf{IQPIR}, that introduces an Image Quality Prior (IQP)—extracted from pre-trained No-Reference Image Quality Assessment (NR-IQA) models—to guide the restoration process toward perceptually optimal outputs explicitly. Our approach synergistically integrates IQP with a learned codebook prior through three key mechanisms:(1) a \textbf{quality-conditioned Transformer}, where NR-IQA-derived scores serve as conditioning signals to steer the predicted representation toward maximal perceptual quality. This design provides a plug-and-play enhancement compatible with existing restoration architectures without structural modification; and(2) a \textbf{dual-branch codebook structure}, which disentangles common and HQ-specific features, ensuring a comprehensive representation of both generic structural information and quality-sensitive attributes; and (3) {a \textbf{discrete representation-based quality optimization strategy}, which mitigates over-optimization effects commonly observed in continuous latent spaces.}Extensive experiments on real-world image restoration demonstrate that our method not only surpasses cutting-edge methods but also serves as a generalizable quality-guided enhancement strategy for existing methods. The code will be released.
</details>

---

### Learning to Assist: Physics-Grounded Human-Human Control Via Multi-Agent Reinforcement Learning
著者: Yuto Shibata, Kashu Yamazaki, Lalit Jayanti, Yoshimitsu Aoki, Mariko Isogawa, Katerina Fragkiadaki

<details>
<summary> 日本語要旨 </summary>

ヒューマノイドロボティクスは、日常のサービスや介護アプリケーションを変革する強い可能性を持っています。最近の一般的な運動追跡技術（GMT）の進歩により、仮想キャラクターやヒューマノイドロボットが広範囲の人間の動作を再現できるようになりましたが、これらの挙動は依然として孤立し非対話的です。一方、支援シナリオでは、進化するパートナーの姿勢やダイナミクスへの継続的な認識と迅速な適応が求められます。本論文では、密接に相互作用し力を交換する人間同士の動作シーケンスの模倣を多エージェント強化学習問題として定式化します。支持者（アシスタント）と受取人の両方に対し、パートナー認識ポリシーを物理シミュレータ上で共同訓練し、支援動作参照を追跡します。この問題を解決可能にするために、単一人間の運動追跡コントローラから優先事項を転送するパートナーポリシー初期化スキームを導入し、探索を大幅に改善します。さらに、アシスタントの参照動作を受取人のリアルタイム姿勢に適応させるダイナミックな参照再ターゲティングと、物理的に意味のある支援を促進する接触促進報酬を提案します。私たちは、AssistMimicが確立されたベンチマークで成功裏に支援相互作用動作を追跡できる初めての方法であることを示し、物理的に根拠のあるかつ社会的認識を持ったヒューマノイド制御における多エージェントRL形式の利点を実証します。コードは受理後に公開いたします。
</details>

<details>
<summary> 英語要旨 </summary>

Humanoid robotics has strong potential to transform daily service and caregiving applications. Although recent advances in general motion tracking within physics engines (GMT) have enabled virtual characters and humanoid robots to reproduce a broad range of human motions, these behaviors remain largely isolated and non-interactive. Assistive scenarios, by contrast, require continuous awareness of a human partner and rapid adaptation to their evolving posture and dynamics. In this paper, we formulate the imitation of closely interacting, force-exchanging human–human motion sequences as a multi-agent reinforcement learning problem. We jointly train partner-aware policies for both the supporter (assistant) and the recipient in a physics simulator to track assistive motion references. To make this problem tractable, we introduce a partner policies initialization scheme that transfers priors from single-human motion-tracking controllers, greatly improving exploration. We further propose dynamic reference retargeting and contact-promoting reward, which adapt the assistant’s reference motion to the recipient’s real-time pose and encourage physically meaningful support. We show that AssistMimic is the first method capable of successfully tracking assistive interaction motions on established benchmarks, demonstrating the benefits of a multi-agent RL formulation for physically grounded and socially aware humanoid control. We will make our code available upon acceptance.
</details>

---

### FlashLips: 100-FPS Mask-Free Latent Lip-Sync Using Reconstruction Instead of Diffusion or GANs
著者: Andreas Zinonos, Michał Stypułkowski, Antoni Bigata Casademunt, Stavros Petridis, Maja Pantic, Nikita Drobyshev

<details>
<summary> 日本語要旨 </summary>

私たちは、リアルタイム性能を100 FPS以上で単一GPU上で達成し、より大きな最先端モデルと同等の視覚品質を維持しつつ、マスクフリーのリップシンクシステム「FlashLips」を提案します。このシステムは2段階構成であり、リップ制御とレンダリングを分離しています。第1段階では、参照アイデンティティ、マスクされたターゲットフレーム、低次元のリップポーズベクトルを用いて画像を再構成するコンパクトな1ステップのラテント空間エディターです。このエディターは再構成損失だけで純粋に訓練され、GANや拡散モデルを使用しません。明示的なマスクを推論時に除去するために自己監督学習を用います：ターゲット画像の口元変更バリアントを生成し、これらが偽のグラウンドトゥルースとして細かい調整のためのファインチューニングに使用されます。このプロセスはネットワークにリップ部分への編集を局所化させつつ、他の部分を保持することを教えます。第2段階では、音声からリップポーズベクトルを予測するためにフローマッチング目的で訓練されたオーディオ・トゥ・ポーズ変換器です。これらの段階が組み合わさり、決定論的な再構成と堅牢な音声制御を統合したシンプルで安定したパイプラインを形成し、高い知覚品質とリアルタイムより速いスピードを提供します。
</details>

<details>
<summary> 英語要旨 </summary>

We present FlashLips, a two-stage, mask-free lip-sync system that decouples lips control from rendering and achieves real-time performance running at over 100 FPS on a single GPU, while matching the visual quality of larger state-of-the-art models. Stage 1 is a compact, one-step latent-space editor that reconstructs an image using a reference identity, a masked target frame, and a low-dimensional lips-pose vector, trained purely with reconstruction losses - no GANs or diffusion. To remove explicit masks at inference, we use self-supervision: we generate mouth-altered variants of the target image, that serve as pseudo ground truth for fine-tuning, teaching the network to localize edits to the lips while preserving the rest. Stage 2 is an audio-to-pose transformer trained with a flow-matching objective to predict lips-poses vectors from speech. Together, these stages form a simple and stable pipeline that combines deterministic reconstruction with robust audio control, delivering high perceptual quality and faster-than-real-time speed.
</details>

---

### WEAVE: Unleashing and Benchmarking The In-context Interleaved Comprehension and Generation
著者: Wei Chow, Jiachun Pan, Yongyuan Liang, Mingze Zhou, Xue Song, Liyu Jia, Saining Zhang, Siliang Tang, Juncheng Li, Fengda Zhang, Weijia Wu, Hanwang Zhang, Tat-seng Chua

<details>
<summary> 日本語要旨 </summary>

最近の統一多様モーダルモデル（UMMs）の進歩により、視覚的理解と生成が大きく前進しました。しかし、現在のデータセットや基準は主に単一ターンのインタラクションを対象としており、実際の画像作成や編集の多ターンで文脈依存的な性質を捉えていません。このギャップに対処するため、我々はWEAVEを提案します。これは、コンテキスト内で交互に行われる異種モーダルの理解と生成のための最初のスイートです。このスイートは2つの補完的な部分から構成されています。WEAVE-100kは、370,000以上のダイアログターンと500,000枚の画像を含む$100$Kの交互サンプルで構成される大規模なデータセットです。これにより、歴史的コンテキストに基づく推論が必要な理解、編集、生成タスクをカバーしています。WEAVEBenchは、480枚の画像に基づく100のタスクを含む人間によって注釈付けされたベンチマークであり、元の画像と編集指示の組み合わせに基づいて参考画像も評価するハイブリッドVLMジャッジフレームワークを特徴としています。これは、多ターン生成、視覚的記憶、および多様な領域にわたる世界知識推論能力を評価します。実験では、WEAVE-100kでのトレーニングが視覚的理解、画像編集、および理解生成協調機能を可能にすることを示しています。さらに、UMMsが発生的な視覚記憶能力を開発するのを助けます。一方で、WEAVEBenchでの広範な評価は、多ターンで文脈認識型画像生成と編集における現在のアプローチの持続的な限界と課題を明らかにします。我々はWEAVEが多様モーダルコミュニティにおけるコンテキスト内で交互に行われる理解と生成の研究の視点と基盤を提供するものと考えています。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advances in unified multimodal models (UMMs) have enabled impressive progress in visual comprehension and generation. However, existing datasets and benchmarks focus primarily on single-turn interactions, failing to capture the multi-turn, context-dependent nature of real-world image creation and editing. To address this gap, we present WEAVE, the first suite for in-context interleaved cross-modality comprehension and generation. Our suite consists of two complementary parts. WEAVE-100k is a large-scale dataset of $100$K interleaved samples spanning over $370$K dialogue turns and $500$K images, covering comprehension, editing, and generation tasks that require reasoning over historical context. WEAVEBench is a human-annotated benchmark with $100$ tasks based on $480$ images, featuring a hybrid VLM judger evaluation framework based on both the reference image and the combination of the original image with editing instructions that assesses models' abilities in multi-turn generation, visual memory, and world-knowledge reasoning across diverse domains. Experiments demonstrate that training on WEAVE-100k enables vision comprehension, image editing, and comprehension-generation collaboration capabilities. Furthermore, it facilitates UMMs to develop emergent visual-memory capabilities, while extensive evaluations on WEAVEBench expose the persistent limitations and challenges of current approaches in multi-turn, context-aware image generation and editing. We believe WEAVE provides a view and foundation for studying in-context interleaved comprehension and generation for multi-modal community.
</details>

---

### Machine Mental Imagery: Empower Multimodal Reasoning with Latent Visual Tokens
著者: Zeyuan Yang, Xueyang Yu, Delin Chen, Maohao Shen, Chuang Gan

<details>
<summary> 日本語要旨 </summary>

ビジョン言語モデル（VLMs）はマルチモーダル理解に優れていますが、テキストのみでのデコードを強いられるため、視覚的な想像力を必要とするタスクではパフォーマンスが制限されます。最近の試みはVLMsに明示的な画像を生成させようとしていますが、重い画像生成の事前学習がしばしば推論能力を妨げています。人間が視覚的な手掛かりを内部で構築し操作する方法に触発され、VLMsが明示的な画像を生成せずとも交錯したマルチモーダルの軌跡を通じて推理できるかどうかを調査します。このために、「Mirage」と名付けられた機械的な精神イメージフレームワークを提案し、VLMのデコードに通常のテキストと共に潜在的な視覚トークンを追加します。具体的には、モデルが「視覚的に考える」ことを選択するたびに、その隠れ状態を次のトークンとして再構成し、ピクセルレベルで画像を生成せずにマルチモーダルの軌跡を続けます。まずは潜在的なトークンを実際の画像埋め込みからの蒸留を通じて監督し、その後テキストのみでの監督に切り替えてタスク目標と密接に一致するように潜在的な軌跡を整合させます。次いで強化学習の段階がマルチモーダル推理能力をさらに向上させます。多様なベンチマークでの実験は、\Model が明示的な画像生成なしに強力なマルチモーダル推理を解放することを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Vision-language models (VLMs) excel at multimodal understanding, yet their text-only decoding forces them to verbalize visual reasoning, limiting performance on tasks that demand visual imagination. Recent attempts train VLMs to render explicit images, but the heavy image-generation pre-training often hinders the reasoning ability. Inspired by the way humans reason with mental imagery—the internal construction and manipulation of visual cues—we investigate whether VLMs can reason through interleaved multimodal trajectories without producing explicit images. To this end, we present a Machine Mental Imagery framework, dubbed as “Mirage”, which augments VLM decoding with latent visual tokens alongside ordinary text. Concretely, whenever the model chooses to “think visually”, it recasts its hidden states as next tokens, thereby continuing a multimodal trajectory without generating pixel-level images. Begin by supervising the latent tokens through distillation from ground-truth image embeddings, we then switch to text-only supervision to make the latent trajectory align tightly with the task objective. A subsequent reinforcement learning stage further enhances the multimodal reasoning capability. Experiments on diverse benchmarks demonstrate that \Model unlocks stronger multimodal reasoning without explicit image generation.
</details>

---

### PhyCritic: Multimodal Critic Models for Physical AI
著者: Tianyi Xiong, Shihao Wang, Guilin Liu, Yi Dong, Ming Li, Heng Huang, Jan Kautz, Zhiding Yu

<details>
<summary> 日本語要旨 </summary>

大規模マルチモーダルモデルの急速な発展に伴い、信頼性の高い審査員および批評家モデルは、オープンエンド評価と好みの整合性を提供するために不可欠であり、ペアワイズな好み、数値スコア、説明的正当化を通じて生成された応答を評価します。しかし、現在の批評家は主にキャプショニングや画像質問応答など一般的な視覚領域で訓練されており、知覚、因果推論、計画を含む物理AIタスクはほとんど探求されていません。私たちは、物理AIに最適化されたマルチモーダル批評家モデルであるPhyCriticを紹介します。これは二段階のRLVRパイプラインを通じて最適化されます：物理的に向けられた知覚と推論を強化する物理スキルウォームアップステージ、その後自己参照批評家の微調整が行われ、批評家は判断前に候補応答を審査するために内部参照として自身の予測を生成し、判断の安定性と物理的正確さを向上させます。物理および一般目的マルチモーダル審査基準にわたり、PhyCriticはオープンソースベースラインに比べて顕著な性能向上を達成し、ポリシーモデルとして適用されることで物理的に根拠のあるタスクにおける知覚と推論がさらに改善されます。
</details>

<details>
<summary> 英語要旨 </summary>

With the rapid development of large multimodal models, reliable judge and critic models have become essential for open-ended evaluation and preference alignment, providing pairwise preferences, numerical scores, and explanatory justifications for assessing model-generated responses. However, existing critics are primarily trained in general visual domains such as captioning or image question answering, leaving physical AI tasks involving perception, causal reasoning, and planning largely underexplored. We introduce PhyCritic, a multimodal critic model optimized for physical AI through a two-stage RLVR pipeline: a physical skill warmup stage that enhances physically oriented perception and reasoning, followed by self-referential critic finetuning, where the critic generates its own prediction as an internal reference before judging candidate responses, improving judgment stability and physical correctness. Across both physical and general-purpose multimodal judge benchmarks, PhyCritic achieves strong performance gains over open-source baselines and, when applied as a policy model, further improves perception and reasoning in physically grounded tasks.
</details>

---

### Unified Multimodal Models As Auto-Encoders
著者: Zhiyuan Yan, Kaiqing Lin, Zongjian Li, Junyan Ye, Hui Han, Haochen Wang, Zhendong Wang, Bin Lin, Li Hao, Xinyan Xiao, Jingdong Wang, Haifeng Wang, Li Yuan

<details>
<summary> 日本語要旨 </summary>

画像からテキスト（I2T）理解とテキストから画像（T2I）生成は、基本的で重要ながらも伝統的に分離されているマルチモーダルタスクです。それらの内在的なつながりにもかかわらず、既存のアプローチは通常独立して最適化され、相互強化の機会を逃しています。本論文では、これらのタスクが共有されたオートエンコーダーの観点からつながることができると主張します。この中でテキストは中間的な潜在表現として機能し、2方向を結ぶ役割を果たします — 画像をテキストセマンティクスにエンコードする（I2T）と、テキストを画像にデコードする（T2I）。私たちの重要な洞察は、「もしエンコーダーが本当に画像を理解しているならば、それはすべての必須構造を捉えるべきであり、デコーダーがテキストを本当に理解しているならば、その構造を忠実に復元するべきだ」ということです。この原則に基づき、我々は強化学習に基づくポストトレーニング手法であるUnified-GRPOを提案します。これは再構成報酬を通じて両モジュールを共同最適化し、入力と生成画像の間のセマンティックな一貫性を最大化します。この再構成目的の下で、エンコーダーは入力画像から可能な限り正確かつ包括的なセマンティック情報を抽出して再構成品質を最大化するよう促されます。一方、デコーダーはエンコーダーの事前条件に基づいて生成されることで同時に最適化され、自己進化的な改善が可能になります。実験的には、テキストを中間表現として使用し、再構成強化学習パラダイムの下でトレーニングすることがI2TおよびT2Iの両方に効果的であることがわかりました。I2Tモジュールは細部までの視覚認識（小物認識、グラウンディングなど）を強化し、その密な埋め込みや言語事前知識が反対にT2Iの忠実度と複雑な指示に従う能力を向上させる豊かなセマンティックシグナルを提供します。これらの結果は、再構成強化学習がオートエンコーディングフレームワーク内で相互に補完的なクロスモーダルシナジーを確立することを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Image-to-text (I2T) understanding and text-to-image (T2I) generation are two fundamental, important yet traditionally isolated multimodal tasks. Despite their intrinsic connection, existing approaches typically optimize them independently, missing the opportunity for mutual enhancement. In this paper, we argue that both tasks can be connected under a shared Auto-Encoder perspective, where text serves as the intermediate latent representation, bridging the two directions — encoding images into textual semantics (I2T) and decoding text back into images (T2I). Our key insight is that *if the encoder truly "understands" the image, it should capture all essential structure, and if the decoder truly "understands" the text, it should recover that structure faithfully.* Building upon this principle, we propose Unified-GRPO, a post-training method based on reinforcement learning that jointly optimizes both modules through reconstructive rewards, maximizing the semantic consistency between the input and the generated images. Under this reconstruction objective, the encoder is encouraged to extract as much accurate and comprehensive semantic information from the input image to maximize reconstruction quality, while the decoder is simultaneously optimized to generate conditioned on the encoder's prior, enabling a self-evolving improvement. Empirically, we find that using text as the intermediate representation and training under a reconstructive RL paradigm effectively benefits both I2T and T2I. The I2T module gains stronger fine-grained visual perception, such as small-object recognition, grounding, etc, while its dense embeddings and language priors, in turn, provide richer semantic signals that improve T2I fidelity and complex instruction following. These results demonstrate that the reconstructive RL establishes a mutually reinforcing cross-modal synergy within the auto-encoding framework.
</details>

---

### Adaptive Depth Lightweight RGB-T Tracking with Holistic Token Routing
著者: Tian Ding, Hongtao Yang, Liangtao Shi, Jun Li, Xiantao Hu, Jian Yang, Ying Tai

<details>
<summary> 日本語要旨 </summary>

夜間のシーン、眩しさ、霧、部分的な遮蔽において失敗することがあります。最近のアーキテクチャは深層融合や大規模なパラメータ数を強調し、これによりFLOPsと帯域幅が増加しています。この計算負荷はリアルタイム性能を制約し、高エンドGPUを超えたスケーラビリティを限定します。精度と効率のバランスを取るために、適応型早期終了（AEE）を提案します：バックボーンにいつでもヘッドを追加し、それらを信頼性が確認された最初の層でインフェレンスを停止する早期終了ポリシーとペアリングします。これにより冗長な計算をスキップします。クロスモーダル相互作用のために、包括的トークンガイドインタラクション（HTGI）モジュールを設計しました。ここでは各モダリティがコンパクトなセットの包括的状態トークンに圧縮され、レイヤーごとの整列なしで他のモダリティのモデリングストリームに注入されます。これにより非常に低コストでターゲット情報交換が可能になります。RGB-Tベンチマークでは、軽量トラッカーは大幅に遅延を削減しつつ競争力のある精度を維持します；LasHeRでは70.2%の精度と56.3%の成功率を達成し、GPUで148.3 FPS、CPUで50.2 FPS、エッジデバイスで28.7 FPSで動作します。
</details>

<details>
<summary> 英語要旨 </summary>

fails under night scenes, glare, fog, and partial occlusion. Despite notable accuracy gains, recent architectures emphasize deep fusion and large parameter counts, driving up FLOPs and bandwidth. This computational burden constrains real-time performance and limits scalability beyond high-end GPUs. To balance accuracy and efficiency, we propose Adaptive Early-Exit (AEE): we augment the backbone with anytime heads and pair them with a confidence-calibrated early-exit policy that halts inference at the earliest reliable layer, skipping redundant computation. For cross-modal interaction, we design a Holistic-Token-Guided Interaction (HTGI) module, where each modality is compressed into a compact set of holistic state tokens and injected into the other modality’s modeling stream without layer-wise alignment, enabling targeted information exchange at extremely low cost. On RGB-T benchmarks, the lightweight tracker substantially reduces latency while maintaining competitive accuracy; on LasHeR, it achieves 70.2% precision and 56.3% success, running at 148.3 FPS on GPU, 50.2 FPS on CPU, and 28.7 FPS on an edge device.
</details>

---

### TR2M: Transferring Monocular Relative Depth to Metric Depth with Language Descriptions and Dual-Level Scale-Oriented Contrast
著者: Beilei Cui, Yiming Huang, Long Bai, Hongliang Ren

<details>
<summary> 日本語要旨 </summary>

本研究では、相対深度をメトリック深度に転送するための汎用化可能なフレームワークを提案します。現在の単眼深度推定手法は主にメトリック深度推定（MMDE）と相対深度推定（MRDE）に分類されます。MMDEはメトリックスケールで深度を推定しますが、特定のドメインに限られることが多いです。一方、MRDEは異なるドメインに対してよく汎化するものの、不確かなスケールが下流アプリケーションを妨げます。このため、スケールの不確実性を解消し、相対深度をメトリック深度に転送するフレームワークを構築することを目指します。従来の手法は言語入力を用いて2つの要因を推定して再スケーリングを行っていましたが、我々のアプローチであるTR2Mはテキスト記述と画像の両方を入力とし、ピクセルレベルで相対深度をメトリック深度に転送するために2つの再スケーリングマップを推定します。異なるモダリティからの特徴はクロスモダリティアテンションモジュールで結合され、より良いスケール情報のキャプチャが可能になります。また、信頼性のある仮想メトリック深度を構築しフィルタリングする戦略を設計して、より包括的な監督を実現します。さらに、深度分布をガイダンスとして使用し、モデルがスケール分布に沿った固有の知識を学習するよう強制するための二重レベルスケール指向対比的学習も開発しています。TR2Mは少数のトレーニング可能なパラメーターを用いて、さまざまなドメインのデータセットでトレーニングされます。実験結果は、TR2Mが既存のデータセットにおける優れた性能だけでなく、5つの未見のデータセットに対する強力なゼロショット能力も示しています。我々は大規模なメトリック深度モデルや多量のトレーニングデータを必要とせず、言語支援によるピクセル単位での相対深度からメトリック深度への転送に大きな可能性があることを示します。コードは受理後に公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

This work presents a generalizable framework to transfer relative depth to metric depth. Current monocular depth estimation methods are mainly divided into metric depth estimation (MMDE) and relative depth estimation (MRDE). MMDEs estimate depth in metric scale but are often limited to a specific domain. MRDEs generalize well across different domains, but with uncertain scales which hinders downstream applications. To this end, we aim to build up a framework to solve scale uncertainty and transfer relative depth to metric depth. Previous methods used language as input and estimated two factors for conducting rescaling. Our approach, TR2M, utilizes both text description and image as inputs and estimates two rescale maps to transfer relative depth to metric depth at pixel level. Features from two modalities are fused with a cross-modality attention module to better capture scale information. A strategy is designed to construct and filter confident pseudo metric depth for more comprehensive supervision. We also develop dual-level scale-oriented contrastive learning to utilize depth distribution as guidance to enforce the model learning about intrinsic knowledge aligning with the scale distribution. TR2M only exploits a small number of trainable parameters to train on datasets in various domains and experiments not only demonstrate TR2M’s great performance in seen datasets but also reveal superior zero-shot capabilities on five unseen datasets. We show the huge potential in pixel-wise transferring relative depth to metric depth with language assistance instead of large-size metric depth models with large amounts of training data. Code will be public available upon acceptance.
</details>

---

### Flowception: Temporally Expansive Flow Matching for Video Generation
著者: Tariq Berrada, John Nguyen, Karteek Alahari, Jakob Verbeek, Ricky T. Q. Chen

<details>
<summary> 日本語要旨 </summary>

私たちは、新しい非自己回帰型かつ可変長のビデオ生成フレームワークであるFlowceptionを提案します。Flowceptionは、離散的なフレーム挿入と連続的なフレームノイズ除去を交互に行う確率パスを学習します。自己回帰手法と比較して、Flowceptionはサンプリング時のフレーム挿入メカニズムが長期的なコンテキストを効率的に圧縮するため、エラーの累積/ドリフトを軽減します。全シーケンスフローと比較して、私たちの方法は訓練時のFLOPsを3倍削減し、また局所的な注意機構にも適応しやすく、ビデオの長さをその内容と共に学習することが可能です。定量的実験結果は、自己回帰および全シーケンスベースラインに対してFVDおよびVBenchメトリクスの改善を示し、これは質的な結果でさらに検証されています。最後に、Flowceptionはフレームの挿入とノイズ除去をシーケンス内で学習することで、画像からビデオ生成やビデオインターポレーションなど異なるタスクを無縫に統合します。
</details>

<details>
<summary> 英語要旨 </summary>

We present Flowception, a novel non-autoregressive and variable-length video generation framework. Flowception learns a probability path that interleaves discrete frame insertions with continuous frame denoising. Compared to autoregressive methods, Flowception alleviates error accumulation/drift as the frame insertion mechanism during sampling serves as an efficient compression mechanism to handle long-term context. Compared to full-sequence flows, our method reduces FLOPs for training three-fold, while also being more amenable to local attention variants, and allowing to learn the length of videos jointly with their content. Quantitative experimental results show improved FVD and VBench metrics over autoregressive and full-sequence baselines, which is further validated with qualitative results. Finally, by learning to insert and denoise frames in a sequence, Flowception seamlessly integrates different tasks such as image-to-video generation and video interpolation.
</details>

---

### MERLIN: Building Low-SNR Robust Multimodal LLMs for Electromagnetic Signals
著者: Junyu Shen, Zhendong She, Chenghanyu Zhang, Yuchuang Sun, Luqing Luo, Dingwei Tan, Zonghao Guo, Bo Guo, Zehua Han, Wupeng Xie, Yaxin Mu, Peng Zhang, Pei Pei Li, Fengxiang Wang, Yangang Sun, Maosong Sun

<details>
<summary> 日本語要旨 </summary>

マルチモーダル大規模言語モデル（MLLMs）のパラダイムは、電磁（EM）領域を進化させるための有望な設計図を提供します。しかし、現在のアプローチはしばしばネイティブMLLMパラダイムから逸脱し、タスク特化型またはパイプラインアーキテクチャを使用しており、これによってモデルの性能と汎用性に基本的な制限が生じます。EM領域でMLLMのポテンシャルを完全に実現するためには、3つの主要な課題を克服する必要があります：（1）\textbf{データ}。MLLMsの事前学習に使用されるEM信号と記述的テキストアノテーションのペアを持つ高品質なデータセットの不足；（2）\textbf{基準}。EM信号からテキストへのタスクでモデルのパフォーマンスを体系的に評価・比較するための包括的な基準の欠如；（3）\textbf{モデル}。信号対雑音比（SNR）が低い環境での重要な信号特徴が隠れることによって生じる、モデルの脆弱性。これらの課題に対処するために、EM領域におけるMLLMsの基盤を確立するための三つの貢献を紹介します。まず、データ不足を克服するために、100,000以上のEM信号-テキストペアから成る大規模なデータセットであるEM-100kを構築しリリースします。次に、厳格かつ標準化された評価を可能にするために、知覚から推論まで多岐にわたるダウンストリームタスクを特徴とする最も包括的な基準であるEM-Benchを提案します。最後に、モデルの中核的な課題に取り組むために、MERLINという新しいトレーニングフレームワークを提示します。これは低レベルの信号表現を高レベルのセマンティックテキストに整合させるだけでなく、挑戦的な低-SNR環境でのモデルの堅牢性とパフォーマンスを明示的に向上させるよう設計されています。包括的な実験が私たちの方法を検証し、MERLINがEM-Benchで最先端であり、低-SNR環境で顕著な堅牢性を示していることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

The paradigm of Multimodal Large Language Models (MLLMs) offers a promising blueprint for advancing the electromagnetic (EM) domain. However, prevailing approaches often deviate from the native MLLM paradigm, instead using task-specific or pipelined architectures that lead to fundamental limitations in model performance and generalization. Fully realizing the MLLM potential in EM domain requires overcoming three main challenges: (1) \textbf{Data.} The scarcity of high-quality datasets with paired EM signals and descriptive text annotations used for MLLMs pre-training; (2) \textbf{Benchmark.} The absence of comprehensive benchmarks to systematically evaluate and compare the performance of models on EM signal-to-text tasks; (3) \textbf{Model.} A critical fragility in low Signal-to-Noise Ratio (SNR) environments, where critical signal features can be obscured, leading to significant performance degradation. To address these challenges, we introduce a tripartite contribution to establish a foundation for MLLMs in the EM domain. First, to overcome data scarcity, we construct and release EM-100k, a large-scale dataset comprising over 100,000 EM signal-text pairs. Second, to enable rigorous and standardized evaluation, we propose EM-Bench, the most comprehensive benchmark featuring diverse downstream tasks spanning from perception to reasoning. Finally, to tackle the core modeling challenge, we present MERLIN, a novel training framework designed not only to align low-level signal representations with high-level semantic text, but also to explicitly enhance model robustness and performance in challenging low-SNR environments. Comprehensive experiments validate our method, showing that MERLIN is state-of-the-art in the EM-Bench and exhibits remarkable robustness in low-SNR settings.
</details>

---

### SAMTok: Representing Any Mask with Two Words
著者: yikang zhou, Tao Zhang, Dengxian Gong, Yuanzheng Wu, Ye Tian, Haochen Wang, Haobo Yuan, Jiacong Wang, Lu Qi, Hao Fei, Shunping Ji, Anran Wang, Zhuochen Wang, Yujing Wang, Cheng CHEN, Xiangtai Li

<details>
<summary> 日本語要旨 </summary>

ピクセル単位の能力は、インタラクティブな知的システムを構築するために不可欠です。しかし、ピクセル単位のマルチモーダルLLM（MLLMs）は、複雑な領域レベルエンコーダー、専門的なセグメンテーションデコーダー、および互換性のないトレーニング目標によりスケールが難しいままです。これらの課題を解決するために、私たちはSAMTokというディスクリートマスクトークナイザーを提案します。このツールは任意の領域マスクを2つの特別なテキストトークンに変換し、これらのトークンから高い忠実度でマスクを再構築します。マスクを新たな言語として扱うことで、SAMTokはQwenVLシリーズのような基本的なMLLMsが標準的な次トークン予測と簡単な強化学習を通じてピクセル単位の能力を学ぶことを可能にします。これはアーキテクチャの変更や専門的な損失設計を必要としません。SAMTokはSAM2に基づき、マスクエンコーダーと残差ベクトル量子化器を用いて209Mの多様なマスクでトレーニングされ、ディスクリートでコンパクトかつ情報豊富なトークンを生成します。5MのSAMTok形式のマスク理解と生成データサンプルにより、QwenVL-SAMTokは領域キャプショニング、VQA、グラウンドされた会話、参照セグメンテーション、シーングラフ解析、およびマルチラウンドインタラクティブセグメンテーションにおいて最先端または比較可能な結果を達成します。さらに、テキスト回答一致報酬というものを導入し、マスク生成の効率的な強化学習を可能にし、GRESおよびGCGベンチマークで顕著な改善を達成します。私たちの結果は、MLLMsに強力なピクセル単位の能力を与えるためのシンプルかつスケーラブルなパラダイムを示しています。コードとモデルは利用可能になります。
</details>

<details>
<summary> 英語要旨 </summary>

Pixel-wise capabilities are essential for building interactive intelligent systems. However pixel-wise multi-modal LLMs (MLLMs) remain difficult to scale due to complex region-level encoders, specialized segmentation decoders, and incompatible training objectives. To solve these challenges, we present SAMTok, a discrete mask tokenizer that converts any region mask into two textual special tokens and reconstructs masks from these tokens with high fidelity. By treating masks as a new language, SAMTok enables base MLLMs (such as the QwenVL series) to learn pixel-wise capabilities through standard next-token prediction and simple reinforcement learning, without architectural modifications and specialized loss design. SAMTok builds on SAM2 and is trained on 209M diverse masks using a mask encoder and residual vector quantizer to produce discrete, compact, and information-rich tokens. With 5M SAMTok formatted mask understanding and generation data samples, QwenVL-SAMTok attains state-of-the-art or comparable results on region captioning, region VQA, grounded conversation, referring segmentation, scene graph parsing, and multi-round interactive segmentation. We further introduce a textual answer-matching reward that enables efficient reinforcement learning for mask generation, delivering substantial improvements on GRES and GCG benchmarks. Our results demonstrate a simple and scalable paradigm for equipping MLLMs with strong pixel-wise capabilities. Code and models will be available.
</details>

---

### V-DPM: Video Reconstruction with Dynamic Point Maps
著者: Edgar Sucar, Eldar Insafutdinov, Zihang Lai, Andrea Vedaldi

<details>
<summary> 日本語要旨 </summary>

新しい強力な3次元表現であるDUSt3Rの不変点マップは、3D形状とカメラパラメータをエンコードすることにより、フィードフォワード3D再構成を大きく進展させました。これらの点マップは静的シーンを仮定していますが、動的ポイントマップ（DPMs）はこの概念を動的な3Dコンテンツに拡張し、3Dシーンの動きも表現します。しかし、これまでのところDPMsは画像ペアに限定されており、DUSt3R同様、2つ以上のビューが関与する場合に最適化を通じた後処理が必要です。私たちはDPMsが動画に適用されるときにはるかに意味があると主張し、これを示すためにV-DPMを導入します。まず、動画に対してDPMsを設定する方法を示し、その表現力の最適化、ニューラル予測の容易さ、および事前学習モデルの再利用を可能にします。次に、これらのアイデアを最近の3D再構成のステート・オブ・ザ・アーツであるVGGTの上に実装します。VGGTは静的シーンでトレーニングされていますが、わずかな合成データだけで効果的なV-DPM予測子として適応させることが可能であることを示します。これにより、動的環境下での3Dおよび4D再構成においてステート・オブ・ザ・アーツを達成します。特に、VGGTの最近の動的拡張であるP3とは異なり、DPMsはシーン内の各点の完全な3D動きだけでなく、動的深度も再構成します。
</details>

<details>
<summary> 英語要旨 </summary>

New, powerful 3D representations such as DUSt3R’s invariant point maps, which encode 3D shape and camera parameters, have significantly advanced feed-forward 3D reconstruction. While point maps assume static scenes, Dynamic Point Maps (DPMs) extend the concept to dynamic 3D content, also representing 3D scene motion. However, DPMs have so far been limited to image pairs and, like DUSt3R, require post-processing via optimization when more than two views are involved. We argue that DPMs are far more meaningful when applied to videos and introduce V-DPM to demonstrate this. First, we show how to set up DPMs for videos to optimize their representational power, ease of neural prediction, and reuse of pre-trained models. Second, we implement these ideas on top of VGGT, a recent state-of-the-art 3D reconstructor. Although VGGT was trained on static scenes, we show that a small amount of synthetic data suffices to adapt it into an effective V-DPM predictor. This yields state-of-the-art 3D and 4D reconstruction in dynamic settings. In particular, unlike recent dynamic extensions of VGGT such as P3, DPMs reconstruct not only dynamic depth but also the full 3D motion of every point in the scene.
</details>

---

### HoneyBee: Data Recipes for Vision-Language Reasoners
著者: Hritik Bansal, Devendra Singh Sachan, Kai-Wei Chang, Aditya Grover, Gargi Ghosh, Wen-tau Yih, Ramakanth Pasunuru

<details>
<summary> 日本語要旨 </summary>

最近の視覚言語モデル（VLM）は推論タスクにおいて非常に効果的であることが示されています。しかし、高性能なVL推論トレーニングデータセットの構築原理はまだ十分に理解されていません。本研究では、トレーニングおよび評価設定を慎重に制御しながら、複数のデータキュレーションアプローチを導入し、その影響をVL推論能力について研究します。コンテキスト（画像と質問ペア）のソース効果を分析し、ターゲットデータ介入を実装し、画像、質問、チェーンオブシンク（CoT）解決策のスケーリングを探求します。私たちの発見は次のように示しています：(a) コンテキストソース戦略がVLMパフォーマンスに大きな影響を与える、(b) 画像キャプションからの補助信号やテキストのみの推論の含有が顕著な向上をもたらす、そして(c) データ次元（例：画像ごとのユニークな質問数および画像-質問ペアごとのユニークなCoT数）をスケーリングすることで推論能力が一貫して向上する。これらの洞察に基づき、私たちは350K画像-質問ペアから成る2.5M例を含む大規模かつ高品質なCoT推論データセットであるHoneyBeeを導入します。HoneyBeeでトレーニングされたVLMは、モデルサイズに関わらず最先端のモデルを上回ります。例えば、3Bパラメーターを持つHoneyBeeでトレーニングされたVLMはMathVerseでSOTAモデルおよび基本モデルに対してそれぞれ7.8%と24.8%の向上を示します。さらに、精度を犠牲にすることなくデコーディングコストを73％削減するテスト時スケーリング戦略を提案します。全体として、この作業はVL推論データセットキュレーション研究における改善された戦略を提示します。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advances in vision-language models (VLMs) have made them highly effective at reasoning tasks. However, the principles underlying the construction of performant VL reasoning training datasets remain poorly understood. In this work, we introduce several data curation approaches and study their impacts on VL reasoning capabilities by carefully controlling training and evaluation setups. We analyze the effects of context (image and question pair) sources, implement targeted data interventions, and explore scaling up images, questions, and chain-of-thought (CoT) solutions. Our findings reveal that (a) context source strategies significantly affect VLM performance, (b) interventions such as auxiliary signals from image captions and the inclusion of text-only reasoning yield substantial gains, and (c) scaling all data dimensions (e.g., unique questions per image and unique CoTs per image-question pair) consistently improves reasoning capability. Motivated by these insights, we introduce HoneyBee, a large-scale, high-quality CoT reasoning dataset with 2.5M examples consisting 350K image-question pairs. VLMs trained with HoneyBee outperform state-of-the-art models across model sizes. For instance, a HoneyBee-trained VLM with 3B parameters outperforms the SOTA model and the base model by 7.8% and 24.8%, respectively, on MathVerse. Furthermore, we propose a test-time scaling strategy that reduces decoding cost by 73% without sacrificing accuracy. Overall, this work presents improved strategies for VL reasoning dataset curation research.
</details>

---

### Spherical Leech Quantization for Visual Tokenization and Generation
著者: Yue Zhao, Hanwen Jiang, Zhenlin Xu, Chutong Yang, Ehsan Adeli, Philipp Krähenbühl

<details>
<summary> 日本語要旨 </summary>

パラメータの効率性と大規模なコードブックへのスケーラビリティにより、ルックアップフリー量子化は多くの注目を集めています。本論文では、格子符号理論を通じた異なる非パラメトリック量子化方法の統一的な形式化を提示します。格子コードの幾何学は、特定の既存のルックアップフリー量子化バリエーション（例えばBSQ）で自己符号器をトレーニングする際に補助的な損失項が必要である理由を説明します。さらに進んで、ランダム格子、一般化フィボナッチ格子、最密球面パック格子といった可能性のある候補を探求します。その中でも、高対称性と超球上での均等な分布により、トレーニング手順の簡素化と再構成-圧縮トレードオフの改善をもたらすLeech格子ベースの量子化方法、すなわち球面Leech量子化（$\Lambda_{24}$-SQ）が優れていることが分かりました。画像トークン化および圧縮タスクにおいて、この量子化アプローチはすべての指標でBSQ（最良の既存技術）を上回る再構成品質を達成し、わずかに少ないビット数で実現します。この改善は、最先端の自己回帰画像生成フレームワークにも拡張されます。
</details>

<details>
<summary> 英語要旨 </summary>

Lookup-free quantization has received much attention due to its efficiency on parameters and scalability to a large codebook. In this paper, we present a unified formulation of different non-parametric quantization methods through the lens of lattice coding. The geometry of lattice codes explains the necessity of auxiliary loss terms when training auto-encoders with certain existing lookup-free quantization variants such as BSQ. As a step forward, we explore a few possible candidates, including random lattices, generalized Fibonacci lattices, and densest sphere packing lattices. Among all, we find the Leech lattice-based quantization method, which is dubbed as Spherical Leech Quantization ($\Lambda_{24}$-SQ), leads to both a simplified training recipe and an improved reconstruction-compression tradeoff thanks to its high symmetry and even distribution on the hypersphere. In image tokenization and compression tasks, this quantization approach achieves better reconstruction quality across all metrics than BSQ, the best prior art, while consuming slightly fewer bits. The improvement also extends to state-of-the-art auto-regressive image generation frameworks.
</details>

---

### ThinkGen: Generalized Thinking for Visual Generation
著者: Siyu Jiao, Yiheng Lin, Yujie Zhong, Qi She, Wei zhou, Xiaohan Lan, Zilong Huang, Fei Yu, Yingchen Yu, Yunqing Zhao, Yao Zhao, Yunchao Wei

<details>
<summary> 日本語要旨 </summary>

最近のマルチモーダル大規模言語モデル（MLLM）の進歩は、連鎖的思考（CoT）推論が複雑な理解タスクに対して体系的なソリューションを可能にすることを示しています。しかし、その生成タスクへの拡張はまだ初期段階であり、一般化や適応が困難なシナリオ特有のメカニズムに制限されています。本研究では、MLLMのCoT推論を様々な生成シナリオで明示的に活用する初めての思考駆動型視覚生成フレームワーク「ThinkGen」を提案します。ThinkGenは、予め学習されたMLLMとDiffusion Transformer（DiT）からなる分離アーキテクチャを採用し、MLLMがユーザーの意図に基づいてカスタマイズされた指示を生成し、DiTはこれらの指示に従って高品質な画像を生成します。さらに、MLLMとDiTモジュール間で交互に強化学習を行う分離可能GRPOベースのトレーニングパラダイム（SepGRPO）を提案しています。この柔軟な設計により、多様なデータセットでの共同学習が可能となり、幅広い生成シナリオにおける効果的なCoT推論を促進します。包括的な実験では、ThinkGenが多数の生成ベンチマークで堅牢かつ最先端の性能を達成することを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Recent progress in Multimodal Large Language Models (MLLMs) demonstrates that Chain-of-Thought (CoT) reasoning enables systematic solutions to complex understanding tasks. However, its extension to generation tasks remains nascent and limited by scenario-specific mechanisms that hinder generalization and adaptation. In this work, we present ThinkGen, the first think-driven visual generation framework that explicitly leverages MLLM's CoT reasoning in various generation scenarios. ThinkGen employs a decoupled architecture comprising a pretrained MLLM and a Diffusion Transformer (DiT), wherein the MLLM generates tailored instructions based on user intent, and DiT produces high-quality images guided by these instructions. We further propose a separable GRPO-based training paradigm (SepGRPO), alternating reinforcement learning between the MLLM and DiT modules. This flexible design enables joint training across diverse datasets, facilitating effective CoT reasoning for a wide range of generative scenarios. Extensive experiments demonstrate that ThinkGen achieves robust, state-of-the-art performance across multiple generation benchmarks.
</details>

---

### UniVerse: Empower Unified Generation with Reasoning and Knowledge
著者: Kaiyue Sun, Weiyang Jin, Chengqi Duan, Rongyao Fang, Xian Liu, Yuwei Niu, Chunwei Wang, Aoxue Li, Xihui Liu

<details>
<summary> 日本語要旨 </summary>

現在のテキスト・トゥ・イメージ（T2I）生成モデルは、複雑な推論や専門知識を必要とするプロンプトに対してしばしば苦戦し、暗黙のユーザー意図を正確に解釈できません。このギャップを埋めるために、我々は**T2I-Reason**という大規模なデータセットを導入します。これは、推論や知識を備えた統一的多様モデル（UMMs）のテキスト・トゥ・イメージ生成を強化することを目的としています。このデータセットには、120,000対のテキスト三重奏と画像が含まれています。テキスト三重奏は、(1) 推論や知識を必要とする暗黙のプロンプトであり、その基本的な意味を解読するために; (2) ステップバイステップの分析を提供し、暗黙のプロンプトの意味を解決する推論チェーン; および(3) T2I生成用に準備された明確で直接的な視覚的説明である明示的プロンプトから構成されています。T2I-Reasonは綿密に構築されており、65,000サンプルが推論専用であり、特に算術推論、空間属性関係の推論、帰納的推論（原因から結果へ）、そして演繹的推論（結果から原因へ）を対象としています。一方、55,000サンプルは専門知識が必要であり、これには多様な分野、空間時間概念、エンティティの知識が含まれます。我々のデータセットの有効性を確認するために、統一的多様モデルであるBagelをこのデータセット上でトレーニングしました。T2I生成の推論能力を評価する複数のベンチマークにおいて、我々のモデルは構成と推論の両方において顕著で一貫した改善を達成しました。これは、中間的な推論チェーンへの明示的なトレーニングがより賢い統一生成モデルに向けた重要なステップであることを確認しています。
</details>

<details>
<summary> 英語要旨 </summary>

Current text-to-image (T2I) generation models often struggle with prompts that require complex reasoning or specialized knowledge, failing to accurately interpret implicit user intent. To bridge this gap, we introduce \textbf{T2I-Reason}, a large-scale dataset designed to empower text-to-image generation in unified multimodal models (UMMs) with reasoning and knowledge. The dataset contains 120k pairs of text triplet and image. The text triplet consists of (1) an implicit prompt, which requires reasoning or knowledge to decipher its underlying meaning; (2) a reasoning chain, which provides a step-by-step analysis to resolve the implicit prompt's meaning; and (3) an explicit prompt, a clear and straightforward visual description prepared for T2I generation. T2I-Reason is meticulously constructed: 65k samples are dedicated to reasoning, specifically targeting arithmetic reasoning, spatial-attribute relationship reasoning, deductive reasoning (cause to effect), and abductive reasoning (effect to cause). While 55k samples necessitate specialized knowledge, which covers multiple disciplines, spatial-temporal concepts, and entity knowledge. To validate the effectiveness of our dataset, we train a unified multimodal model, Bagel, on our dataset. Results across multiple benchmarks that evaluate the reasoning capabilities of T2I generation demonstrate that our model achieves significant and consistent improvements on both composition and reasoning, confirming that explicit training on intermediate reasoning chains is a pivotal step towards more intelligent unified generative models.
</details>

---

### TrajTok: Learning Trajectory Tokens Enables Better Video Understanding
著者: Chenhao Zheng, Jieyu Zhang, Jianing Zhang, Weikai Huang, Ashutosh Kumar, Quan Kong, Oncel Tuzel, Chun-Liang Li, Ranjay Krishna

<details>
<summary> 日本語要旨 </summary>

ビデオモデルにおけるトークン化は、通常パッチファイケーションを介して行われますが、これにより過剰で冗長な数のトークンが生成されます。このことはビデオの効率性およびスケーラビリティを大幅に制限します。最近の軌道ベースのトークナイザーは、ビデオの長さとトークン数を分離することで有望な解決策を提供していますが、これらは遅くてタスクに依存しない複雑な外部セグメンテーションおよび追跡パイプラインに依存しています。私たちはTrajTokを提案します。これは、下流の目的でビデオモデルと完全に統合され、共同トレーニングが行われるエンドツーエンドのビデオトークナイザーモジュールです。TrajTokは、動画の長さに依存せず、セマンティックな複雑さに応じてそのトークンの粒度を動的に適応します。TrajTokには、空間と時間の両方でピクセル上で暗黙のクラスタリングを行い、単一のフォワードパスで直接オブジェクト軌道を生成する統合セグメンテータが含まれています。ピクセルごとに完璧なセグメンテーションの正確さよりも下流への適応性を優先することで、TrajTokは軽量で効率的でありながら、実証的にビデオ理解パフォーマンスを向上させます。TrajTokを使用して、ゼロからトレーニングされたビデオCLIPモデル（TrajViT2）を実装しました。これは、分類および検索の両方のベンチマークでスケールにおいて最高の精度を達成していますが、トークン結合方法の中でも最良の効率性を維持しています。TrajTokはトークナイザーとしての役割を超えた汎用性も証明されています。事前学習済み視覚特徴に対するプロービングヘッドとして（TrajAdapter）またはビジョン・ランゲージモデル内のアライメントコネクターとして（TrajVLM）シームレスに統合できることを示しました。特に長時間動画の推論において強力なパフォーマンスが得られます。
</details>

<details>
<summary> 英語要旨 </summary>

Tokenization in video models, typically through patchification, generates an excessive and redundant number of tokens. This severely limits video efficiency and scalability. While the recent trajectory-based tokenizers offer a promising solution by decoupling video duration from token count, they rely on complex, external segmentation and tracking pipelines that are slow and task-agnostic. We propose TrajTok, an end-to-end video tokenizer module that is fully integrated and co-trained with video models for a downstream objective, dynamically adapting its token granularity to semantic complexity, independent of video duration. TrajTok contains a unified segmenter that performs implicit clustering over pixels in both space and time to directly produce object trajectories in a single forward pass. By prioritizing downstream adaptability over pixel-perfect segmentation fidelity, TrajTok is lightweight, efficient, and yet empirically improves video understanding performance. With TrajTok, we implement a video CLIP model trained from scratch (TrajViT2). It achieves the best accuracy at scale across both classification and retrieval benchmarks, while maintaining efficiency comparable to the best token-merging methods. TrajTok also proves to be a versatile component beyond its role as a tokenizer. We show that it can be seamlessly integrated as either a probing head for pretrained visual features (TrajAdapter) or an alignment connector in vision–language models (TrajVLM) with especially strong performance in long-video reasoning.
</details>

---

### FlashMotion: Few-Step Controllable Video Generation with Trajectory Guidance
著者: Quanhao Li, Zhen Xing, Rui Wang, Haidong Cao, Qi Dai, Daoguo Dong, Zuxuan Wu

<details>
<summary> 日本語要旨 </summary>

最近の軌道制御可能なビデオ生成技術は、顕著な進歩を遂げています。これまでの方法では、主にアダプタベースのアーキテクチャを使用して、事前定義された軌道沿いで正確な動き制御を行ってきました。しかし、これらのすべての方法は多段階のノイズ除去プロセスに依存しており、大幅な時間冗長性と計算オーバーヘッドが発生します。既存のビデオ蒸留手法は、多段階ジェネレータを少数ステップにまで簡素化することに成功していますが、これらのアプローチをそのまま軌道制御可能なビデオ生成に適用すると、ビデオ品質および軌道精度の両方で顕著な劣化が生じます。このギャップを埋めるために、私たちはFlashMotionという新しいトレーニングフレームワークを導入します。これは少数ステップの軌道制御可能なビデオ生成用に設計されています。まず、正確な軌道制御のために多段階ビデオジェネレータ上でアダプタをトレーニングします。次に、ジェネレータを少数ステップ版に簡素化してビデオ生成を加速します。最後に、混合戦略を用いて拡散と対抗的な目標を組み合わせたものでアダプタを微調整し、少数ステップジェネレータと一致させることで高品質かつ軌道精度の高いビデオを生成します。評価のために、長シーケンス軌道制御可能なビデオ生成のベンチマークであるFlashBenchを導入しました。これは、異なる数の前景オブジェクトにわたってビデオ品質と軌道精度の両方を測定します。2つのアダプタアーキテクチャでの実験では、FlashMotionが既存のビデオ蒸留手法および以前の多段階モデルを視覚品質と軌道一貫性の両方で上回ることが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advances in trajectory-controllable video generation have achieved remarkable progress. Previous methods mainly use adapter-based architectures for precise motion control along predefined trajectories. However, all these methods rely on a multi-step denoising process, leading to substantial time redundancy and computational overhead. While existing video distillation methods successfully distill multi-step generators into few-step, directly applying these approaches to trajectory-controllable video generation results in noticeable degradation in both video quality and trajectory accuracy. To bridge this gap, we introduce FlashMotion, a novel training framework designed for few-step trajectory-controllable video generation. We first train a trajectory adapter on a multi-step video generator for precise trajectory control. Then, we distill the generator into a few-step version to accelerate video generation. Finally, we finetune the adapter using a hybrid strategy that combines diffusion and adversarial objectives, aligning it with the few-step generator to produce high-quality, trajectory-accurate videos. For evaluation, we introduce FlashBench, a benchmark for long-sequence trajectory-controllable video generation that measures both video quality and trajectory accuracy across varying numbers of foreground objects. Experiments on two adapter architectures show that FlashMotion surpasses existing video distillation methods and previous multi-step models in both visual quality and trajectory consistency.
</details>

---

### ColaVLA: Leveraging Cognitive Latent Reasoning for Hierarchical Parallel Trajectory Planning in Autonomous Driving
著者: Qihang Peng, Xuesong Chen, Chenye Yang, Shaoshuai Shi, Hongsheng Li

<details>
<summary> 日本語要旨 </summary>

自律走行には、複雑な多モーダル入力から安全で信頼性の高い経路を生成する必要があります。伝統的なモジュラー型パイプラインでは認識、予測、計画を分離していますが、最近のエンド・トゥ・エンド（E2E）システムはこれらを共に学習します。ビジョン–言語モデル（VLMs）はこのパラダイムをさらに豊かにし、クロスモーダルの事前知識と常識的推論を導入していますが、現在のVLMベースのプランナーは三つの主要な課題に直面しています：（i）離散的テキスト推論と連続制御の不一致、（ii）自己回帰チェーン・オブ・シンク思考デコーディングからの高いレイテンシー、および（iii）効率が悪いまたは非因果的なプランナーによるリアルタイム展開の制限。私たちはColaVLAを提案します。これはビジョン–言語–行動フレームワークで、テキストから統一された潜在空間への推論を移し、それを階層的な並列経路デコーダーと結合します。認知潜在推論者はシーン理解を決定指向のコンパクトなメタアクション埋め込みに圧縮し、エゴ適応的選択とVLMの前方伝播を2回だけ行います。階層的並列プランナーは単一の前方伝播で因果性一貫なマルチスケール経路を生成します。これらのコンポーネントはVLMsの汎用性と解釈可能性を保持しつつ、効率的かつ正確で安全な経路生成を可能にします。nuScenesベンチマークでの実験では、ColaVLAがオープンループおよびクローズドループ設定の両方で最先端の性能を達成し、有利な効率と堅牢性を示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Autonomous driving requires generating safe and reliable trajectories from complex multimodal inputs. Traditional modular pipelines separate perception, prediction, and planning, while recent end-to-end (E2E) systems learn them jointly. Vision–language models (VLMs) further enrich this paradigm by introducing cross-modal priors and commonsense reasoning, yet current VLM-based planners face three key challenges: (i) a mismatch between discrete text reasoning and continuous control, (ii) high latency from autoregressive chain-of-thought decoding, and (iii) inefficient or non-causal planners that limit real-time deployment. We propose ColaVLA, a unified vision–language–action framework that transfers reasoning from text to a unified latent space and couples it with a hierarchical, parallel trajectory decoder. The Cognitive Latent Reasoner compresses scene understanding into compact, decision-oriented meta-action embeddings through ego-adaptive selection and only two VLM forward passes. The Hierarchical Parallel Planner then generates multi-scale, causality-consistent trajectories in a single forward pass. Together, these components preserve the generalization and interpretability of VLMs while enabling efficient, accurate and safe trajectory generation. Experiments on the nuScenes benchmark show that ColaVLA achieves state-of-the-art performance in both open-loop and closed-loop settings with favorable efficiency and robustness.
</details>

---

### Expanding MmWave Datasets for Human Pose Estimation with Unlabeled Data and LiDAR Datasets
著者: Zhuoxuan Peng, Boan Zhu, Xingjian Zhang, Wenying Li, S.-H. Gary Chan

<details>
<summary> 日本語要旨 </summary>

現在のミリ波（mmWave）データセットは、点群（PC）属性および人間のポーズにおいて多様性が欠けており、その結果としてトレーニングされたモデルの汎用性を大きく制限しています。一方で、ラベルなしのミリ波人間姿勢推定（HPE）データおよび多様なLiDAR HPEデータセットは容易に入手可能です。本研究では、ラベルなしのミリ波データとLiDARデータを用いて既存のミリ波データセットの量と多様性を拡張するための新手法EMDULを提案します。EMDULは、ラベルなしのミリ波データに対して仮ラベル推定器をトレーニングし、与えられたLiDAR点群をそのミリ波版に変換することができます。LiDARから変換されたものと仮ラベル付けされたミリ波PCを用いて拡張した結果、私たちのミリ波データセットはすべてのHPEモデルの性能および汎用性を大幅に向上させました。具体的には、ドメイン内で15.1%、ドメイン外で18.9%の誤差削減が達成されています。
</details>

<details>
<summary> 英語要旨 </summary>

Current mmWave datasets for human pose estimation (HPE) are scarce and lack diversity in both point cloud (PC) attributes and human poses, severely hampering the generalization ability of their trained models. On the other hand, unlabeled mmWave HPE data and diverse LiDAR HPE datasets are readily available. We propose EMDUL, a novel approach to expand the volume and diversity of an existing mmWave dataset using unlabeled mmWave data and a LiDAR dataset. EMDUL trains a pseudo-label estimator to annotate the unlabeled mmWave data and is able to convert, or translate, a given annotated LiDAR PC to its mmWave counterpart. Expanded with both LiDAR-converted and pseudo-labeled mmWave PCs, our mmWave dataset significantly boosts the performance and generalization ability of all our HPE models, with substantial 15.1% and 18.9% error reductions for in-domain and out-of-domain settings, respectively.
</details>

---

### ARES: Unifying Asymmetric RGB-Event Stereo for Probabilistic Scene Flow Estimation
著者: Jie Long Lee, Gim Hee Lee

<details>
<summary> 日本語要旨 </summary>

動的高速シーンにおける密な三次元運動の推定は、モーションブラー、照明変化、従来のカメラの限られた時間分解能により依然として難しいです。私たちは、これらの問題を対称的なRGB-イベントステレオの統一フレームワークARESを通じて解決する新しいアプローチを紹介します。このハイブリッドセットアップでは、イベントカメラが微細な時間的ダイナミクスを捉え、RGBカメラが豊かな空間構造を提供します。これらの異種モダリティを統合するために、私たちはトランスフォーマーに基づく融合メカニズムであるマルチモーダルコンテクストアテンションを提案します。これは、異なる視点の制約下で空間的および時間的文脈に注意を払い、不一致と光流推定のための統一された対応空間を形成します。この共有表現に基づき、私たちは確率的フレームワークである時間的不一致事後融合を導入し、不一致の進化をモデル化して不一致の変化を推定し、メトリックに整合したシーンフローを回復します。希薄な監督と密な自己整合性手がかりで訓練されたARESは、多様な運転シナリオにわたって幾何学的に一貫した時間的に安定した三次元運動推定を実現します。実験では、ARESがシーンフロー推定で最先端の性能を達成し、非対称マルチモーダルステレオセンシングに向けた原則的な道筋を確立しています。コードは論文受理後に公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Estimating dense three dimensional motion in dynamic high speed scenes remains challenging due to motion blur, illumination variation, and the limited temporal resolution of conventional cameras. We introduce ARES, a unified framework for Asymmetric RGB-Event Stereo that addresses these issues through a hybrid setup where an event camera captures fine grained temporal dynamics and an RGB camera provides rich spatial structure. To integrate these heterogeneous modalities, we propose Multimodal Contextual Attention, a transformer based fusion mechanism that attends to spatial and temporal contexts under cross view constraints and forms a unified correspondence space for disparity and optical flow estimation. Building on this shared representation, we introduce Temporal Disparity Posterior Fusion, a probabilistic framework that models the evolution of disparity posteriors to infer disparity change and recover metrically coherent scene flow. Trained with sparse supervision and dense self consistency cues, our ARES achieves geometrically consistent and temporally stable three dimensional motion estimation across diverse driving scenarios. Experiments show that ARES attains state of the art performance in scene flow estimation, establishing a principled path toward unified asymmetric multimodal stereo sensing. Our code will be released upon paper acceptance.
</details>

---

### Are Image-to-Video Models Good Zero-Shot Image Editors?
著者: Zechuan Zhang, Zhenyuan Chen, Zongxin Yang, Yi Yang

<details>
<summary> 日本語要旨 </summary>

大規模なビデオ拡散モデルは強力な世界シミュレーション能力と時間的推論能力を示していますが、ゼロショット画像エディターとしての可能性は未だ十分に探求されていません。私たちは \ifedit{IF-Edit} (\textbf{I}mage Edit by Generating \textbf{F}rames) を提案します。これは、事前学習済みの画像から動画への拡散モデルを指示に基づく画像編集用に再利用するチューニングフリーのフレームワークです。 \ifedit{IF-Edit} は、プロンプトの不一致、冗長な時間的潜在変数、および後期段階のぼやけたフレームという3つの核心的な課題に対処します。具体的には：(1) チェーン・オブ・シンク思考プロンプト強化モジュールを用いて、静的な編集指示を時間的に根拠のある推論プロンプトとして再構成します；(2) 時間的潜在変数ドロップアウト戦略を用いて、専門家切り替え点後にフレームの潜在変数を圧縮し、ノイズ除去を加速しつつグローバルセマンティクスと時間的一貫性を保持します；(3) 自己整合的なポストリファインメントステップで、最も鋭い後期段階のフレームを短い静止動画軌道を通じて微調整し、よりシャープで忠実な結果を得るためにビデオ事前知識を活用します。四つの公開ベンチマーク（非剛体変形、物理的および時間的推論、一般指示編集をカバー）での広範な実験により、 \ifedit{IF-Edit} は非剛体および推論中心のタスクで強力な性能を発揮し、一般的な編集でも競争力を保持することが示されました。私たちの研究はビデオ拡散モデルを画像エディターとして体系的に捉える視点を提供し、その独自の強み、限界、および統一された動画・画像生成推論のためのシンプルなレシピを明らかにします。
</details>

<details>
<summary> 英語要旨 </summary>

Large-scale video diffusion models exhibit strong world-simulation and temporal reasoning capabilities, yet their potential as zero-shot image editors remains underexplored. We present \ifedit{IF-Edit} (\textbf{I}mage Edit by Generating \textbf{F}rames), a tuning-free framework that repurposes pre-trained image-to-video diffusion models for instruction-driven image editing. \ifedit{IF-Edit} addresses three core obstacles—prompt misalignment, redundant temporal latents, and blurry late-stage frames—via: (1) a Chain-of-Thought Prompt Enhancement module that reformulates static editing instructions into temporally grounded reasoning prompts; (2) a Temporal Latent Dropout strategy that compresses frame latents after the expert-switch point, accelerating denoising while preserving global semantics and temporal coherence; and (3) a Self-Consistent Post-Refinement step that refines the sharpest late-stage frame through a brief still-video trajectory, leveraging the video prior for sharper and more faithful results. Extensive experiments across four public benchmarks—covering non-rigid deformations, physical and temporal reasoning, and general instruction editing—show that \ifedit{IF-Edit} achieves strong performance on non-rigid and reasoning-centric tasks while remaining competitive on general-purpose edits. Our study offers a systematic view of video diffusion models as image editors, revealing their unique strengths, limitations, and a simple recipe for unified video–image generative reasoning.
</details>

---

### GPFlow: Gaussian Prototype Probability Flow for Unsupervised Multi-Modal Anomaly Detection
著者: YITING LI, Xulei Yang, Jingyi Liao, Jing Zhang, Fayao Liu

<details>
<summary> 日本語要旨 </summary>

我々は、各クラスにごく少数の正常な例しか利用できないようなフェアショット状況における教師なしマルチモーダル異常検知（MAD）を扱います。既存手法は、正常な外観や幾何学の分布レベル情報を捉えられないため、このようなデータ不足に苦労しています。多様で連続した正常性変動を捕捉するために、我々は確率流に触発されたフレームワークであるGPFlowを提案します。これは、学習可能なガウスプロトタイプの潜在空間に多様な正常パターンを埋め込みます。その核として、GPFlowは特徴を高確率領域であるプロトタイプ中心へと移動させることで異常の単純な再構成を防ぐ明示的情報ボトルネックとして機能する解析的Posterior-Mean Path（PMP）ルーターを使用します。マルチモーダル手がかりを活用するために、GPFlowはプロトタイプレベルでの内部およびクロスモーダル一貫性を強制する結合再構成アーキテクチャを採用します。最後に、希薄な訓練サンプルと未見のテストサンプル間の分布シフトを処理するために、GPFlowは新しい正常変動へのカバレッジをテスト時に動的に拡張する推論認識型プロトタイプ精緻化を取り入れます。MVTec-3D-ADおよびEyecandiesでの広範な実験では、GPFlowがごく少数の正常訓練サンプルであっても最先端の性能を達成し、計算効率も保持していることが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

We address unsupervised multi-modal anomaly detection (MAD) in few-shot regimes, where only a handful of normal exemplars are available per class. Existing approaches struggle with such data scarcity due to their incapacity in capturing the distribution-level information of normal appearance and geometry. To capture diverse and continuous normality variations, we propose GPFlow, a probability flow inspired framework that embeds diverse normal patterns into a latent space of learnable Gaussian prototypes. At its core, GPFlow uses an analytical Posterior‑Mean Path (PMP) router that iteratively moves features toward prototype‑centered high‑probability neighborhoods, acting as an explicit information bottleneck to prevent trivial reconstruction of anomalies. To exploit multi-modal cues, GPFlow employs a coupled reconstruction architecture enforces both intra- and cross-modal consistency at the prototype level. Finally, to handle distribution shift between sparse training samples and unseen test samples, GPFlow incorporates inference-aware prototype refinement to dynamically expand the prototypes' coverage to new normal variations during test time. Extensive experiments on MVTec‑3D‑AD and Eyecandies show that GPFlow achieves state‑of‑the‑art performance with only a few normal training samples, while remaining computationally efficient.
</details>

---

### Real-World Point Tracking with Verifier-Guided Pseudo-Labeling
著者: Görkay Aydemir, Fatma Güney, Weidi Xie

<details>
<summary> 日本語要旨 </summary>

長期的な点追跡モデルは通常、大規模な合成データセットでトレーニングされます。しかし、実際のビデオでは、異なる特性と密なグラウンドトゥルースアノテーションの欠如により、これらのモデルのパフォーマンスが低下します。未ラベルビデオでの自己学習は実用的な解決策として探求されていますが、教師予測の信頼性に強く依存するため、プセウドラベルの品質はフレームやシーンごとに変動します。本論文では、実世界での微調整問題を扱い、「Verifier」というメタモデルを導入しました。これはトラッカ予測の信頼性を評価し、プセウドラベル生成をガイドするものです。複数の事前学習されたトラッカから得られる候補軌道に対して、Verifierはフレームごとに評価し、最も信頼できる予測を選択して洗練されたプセウドラベルの軌道を構築します。微調整中にVerifierガイド付きのプセウドラベリングが適用されると、監督の質が大幅に向上し、未ラベルビデオへのデータ効率的な適応を可能にします。4つの実世界ベンチマークで行われた広範な実験は、私たちのアプローチが少ないデータであっても最先端の結果を達成しており、以前の自己学習方法よりも少ないデータしか必要としないことを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Models for long-term point tracking are typically trained on large synthetic datasets. The performance of these models degrades in real-world videos due todifferent characteristics and the absence of dense ground-truth annotations. Self-training on unlabeled videos has been explored as a practical solution, but the quality of pseudo-labels strongly depends on the reliability of teacher predictions, which vary across frames and scenes. In this paper, we address the problem of real-world fine-tuning and introduce Verifier, a meta-model that learns to assess the reliability of tracker predictions and guide pseudo-label generation. Given candidate trajectories from multiple pretrained trackers, the verifier evaluates them per frame and selects the most trustworthy predictions to construct refined pseudo-label trajectories. When applied during fine-tuning, verifier-guided pseudo-labeling substantially improves the quality of supervision and enables data-efficient adaptation to unlabeled videos. Extensive experiments on four real-world benchmarks demonstrate that our approach achieves state-of-the-art results while requiring less data than prior self-training methods.
</details>

---

### AutoDebias: An Automated Framework for Detecting and Mitigating Backdoor Biases in Text-to-Image Models
著者: Hongyi Cai, HONGYI CAI, MingKang Dong, Muxin Pu, Moayad Aloqaily, jie li, Xinfeng Li, Jialie Shen, Meikang Qiu, Qingsong Wen

<details>
<summary> 日本語要旨 </summary>

テキスト・トゥ・イメージ（T2I）モデルは高品質の画像を生成しますが、有害なバイアス（例えば、トリガーによって活性化されるジェンダーや人種のステレオタイプ）を注入する悪意のあるバックドア攻撃に対して脆弱です。これらの故意で微妙な注入攻撃には、自然統計的バイアス用に設計された既存のデバイアス除去方法が苦労します。私たちは、特定の攻撃ベクトルを事前に知らずにT2Iモデル内のこれらの悪意あるバイアスを自動的に識別し軽減するフレームワークであるAutoDebiasを提案します。具体的には、AutoDebiasはビジョン・ランゲージモデルを活用してトリガーによって活性化された視覚パターンを検出し、対抗プロンプトを生成することで中和ガイドを構築します。これらのガイドは、有害な関連付けを破壊しながら元のモデルの画像品質や多様性を保持するCLIPによる指導訓練プロセスを駆動します。自然バイアス用に設計された方法とは異なり、AutoDebiasは微妙で注入されたステレオタイプや複数の相互作用する攻撃を効果的に対処します。私たちは17種類の異なるバックドア攻撃シナリオをカバーする新しいベンチマークでフレームワークを評価し、複数のバックドアが共存する難易度の高いケースも含めています。AutoDebiasは有害なパターンを91.6％の精度で検出し、成功率を90％から無視できるレベルに低下させますが、元のモデルの視覚的忠実性は保持されています。
</details>

<details>
<summary> 英語要旨 </summary>

Text-to-Image (T2I) models generate high-quality images but are vulnerable to malicious backdoor attacks that inject harmful biases (e.g., trigger-activated gender or racial stereotypes). Existing debiasing methods, often designed for natural statistical biases, struggle with these deliberate and subtle injected attacks. We propose AutoDebias, a framework that automatically identifies and mitigates these malicious biases in T2I models without prior knowledge of the specific attack vectors. Specifically, AutoDebias leverages vision-language models to detect trigger-activated visual patterns and constructs neutralization guides by generating counter-prompts. These guides drive a CLIP-guided training process that breaks the harmful associations while preserving the original model's image quality and diversity. Unlike methods designed for natural bias, AutoDebias effectively addresses subtle, injected stereotypes and multiple interacting attacks. We evaluate the framework on a new benchmark covering 17 distinct backdoor attack scenarios, including challenging cases where multiple backdoors co-exist. AutoDebias detects malicious patterns with 91.6\% accuracy and reduces the backdoor success rate from 90\% to negligible levels, while preserving the visual fidelity of the original model.
</details>

---

### Visual-Aware CoT: Achieving High-Fidelity Visual Consistency in Unified Models
著者: Zixuan Ye, Quande Liu, Cong Wei, Yuanxing Zhang, Xintao Wang, Pengfei Wan, Kun Gai, Wenhan Luo

<details>
<summary> 日本語要旨 </summary>

最近、チェーン・オブ・シンキング（CoT）の導入により、統一モデルの生成能力が大幅に向上しました。しかし、現在の多様な生成中の思考プロセスは、テキストプロンプトとのテキストの一貫性に主に焦点を当てており、視覚的文脈と視覚参照画像との一貫性を無視しています。例えば、マルチリファレンス生成では、このような一貫性が欠如することで、重要な視覚的特徴（人物IDやオブジェクト属性、スタイルなど）を維持できない結果につながります。このため、私たちは統一モデルの推論に視覚的文脈の一貫性を統合し、1) 適応型視覚計画：必要な一貫性を保持するための構造化された視覚チェックリストを生成し、2) イテレーティブ・ビジュアル・コレクション：チェックリストに基づいて自己反省を行い、結果を反復的に洗練することで、明示的にモデルがそのような一貫性を維持するよう動機付けます。これを達成するために、私たちはモデルに視覚チェックの計画方法、自己反省と自己洗練の方法を教えるために監督学習で微調整し、カスタマイズされた視覚チェック報酬を用いてflow-GRPOを使用してさらに視覚的一貫性を強化します。実験結果は、私たちの方法がゼロショット統一モデルやテキストCoTを持つものよりもマルチモーダル生成において優れており、高い視覚的文脈の一貫性を示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Recently, the introduction of Chain-of-Thought (CoT) has largely improved generation ability of unified models. However, it is observed that the current thinking process during generation mainly focuses on the text consistency with the text prompt, ignoring the visual context consistency with the visual reference images during the multi-modal generation, e.g., multi-reference generation. The lack of such consistency results in the failure in maintaining key visual features (like human ID, object attribute, style). To this end, we integrate the visual context consistency into the reasoning of unified models, explicitly motivating the model to sustain such consistency by 1) Adaptive Visual Planning: generating structured visual check list to figure out the visual element of needed consistency keeping, and 2) Iterative Visual Correction: performing self-reflection with the guidance of check lists and refining the generated result in an iterative manner. To achieve this, we use supervised finetuning to teach the model how to plan the visual checking, conduct self-reflection and self-refinement, and use flow-GRPO to further enhance the visual consistency through a customized visual checking reward. The experiments show that our method outperforms both zero-shot unified models and those with text CoTs in multi-modal generation, demonstrating higher visual context consistency.
</details>

---

### Modeling Cross-vision Synergy for Unified Large Vision Model
著者: Shengqiong Wu, Lanhu Wu, Mingyang Bao, Wenhao Xu, Hanwang Zhang, Shuicheng Yan, Hao Fei, Tat-seng Chua

<details>
<summary> 日本語要旨 </summary>

最近の大規模ビジョンモデル（LVM）の進歩は、画像、動画、3Dデータを同時に処理する統一アーキテクチャへと移行しています。しかし、既存の統一LVMは機能的な統合を追求することが主であり、異なる視覚モダリティ間で補完的な事前知識を用いて推論する能力というより深い目標であるクロスビジョンシナジーを見落としています。これに対処するため、私たちはPolyVを提案します。これはアーキテクチャレベルおよびトレーニングレベルの両方でクロスビジョンシナジーを達成する統一LVMです。アーキテクチャ的に、PolyVは動的なモダリティルーターによって調整された希薄な専門家の混合物として構築されており、各専門家がモダリティ固有の事前知識を特化する一方で、異なるモダリティ間で双方向の相互作用と相互補完を可能にします。トレーニング面では、シナジー意識のパラダイムが知識転移とオブジェクト・関係レベルの整合性を通じた粗いから細かいシナジータッチアップを含む、モダリティ固有の事前学習を組み合わせています。画像、動画、3D理解にまたがる10のベンチマークおよび空間的または時間的な事前知識を必要とするシナジー重視のデータセットでの広範な実験では、PolyVが既存のモデルを一貫して上回り、バックボーンに対して平均10％以上の改善を達成することが示されました。全体として、PolyVはシナエステジア的な視覚推論のための統一フレームワークを確立し、真にシナジックな大規模ビジョンモデルへと進化しています。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advances in large vision models (LVMs) have shifted from modality-specific designs toward unified architectures that jointly process images, videos, and 3D data. However, existing unified LVMs primarily pursue functional integration, while overlooking the deeper goal of cross-vision synergy: the ability to reason over complementary priors across visual modalities. To address this, we present PolyV, a unified LVM that achieves cross-vision synergy at both the architectural and training levels. Architecturally, PolyV adopts a sparse Mixture-of-Experts LVM coordinated by a dynamic modality router, allowing each expert to specialize in modality-specific priors while enabling bidirectional interaction and mutual refinement across modalities. Training-wise, a synergy-aware paradigm combines modality-specific pretraining with coarse-to-fine synergy tuning via knowledge distillation and object-/relation-level alignment. Extensive experiments on ten benchmarks spanning image, video, and 3D understanding, including synergy-focused datasets requiring spatial or temporal priors, demonstrate that PolyV consistently outperforms existing models, achieving over 10\% average improvement over its backbone. Overall, PolyV establishes a unified framework for synesthetic visual reasoning, advancing toward truly synergistic large vision models.
</details>

---

### From Remember to Transfer: Interpretable Open-World Reasoning in MLLMs
著者: Chenghao Li, Jun Liu, Songbo Zhang, HuaDong Jian, Hao Ni, LIK-HANG LEE, SUNG BAE BAE, Guoqing Wang, Yang Yang, Chaoning Zhang

<details>
<summary> 日本語要旨 </summary>

多モーダルエージェント、例えばJARVIS-1のようなものは、オープンワールド環境で急速に進化しています。その基本的なワークフローは通常、知覚–推論–行動–記憶サイクルをたどります。既存の研究では主にメモリ表現とストレージフォーマットの改善に重点が置かれ、メモリは情報のデポとして扱われることが多いです。しかし、保存された経験から移転可能な知識を抽出することは依然として重要でありながら未解明の課題です。実世界の設定では構造やパターンが再発しやすい傾向にあります。エージェントがこれらの潜在的なパターンを捉え、再利用できれば、過去の経験から新たな行動可能な知識を推論し、より効率的かつ柔軟にタスクを実行することができます。この能力を探るために、私たちはエコー（Echo）を提案します。エコーは知識を移転可能性の5つの明示的な次元、すなわち構造、属性、プロセス、機能、相互作用に分解します。この形式に基づき、エコーはイン・コンテキスト・アナロジー学習（ICAL）を活用して過去の経験を効果的に取り出し、新たなタスクに一般化します。実験では、ゼロから学習する設定でエコーがオブジェクト解錠タスクで1.3倍～1.7倍の速度向上を達成していることが示されました。さらに、エコーは連鎖解錠現象を発生させ、短時間内に複数の類似アイテムを急速に解錠することが観察されています。これらの結果は、文脈的な例の効果的な活用によって推進される堅牢な知識移転が、オープンワールド多モーダルエージェントを進化させるための非常に有望な方向性であることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Multimodal agents, such as JARVIS-1, are rapidly advancing in open-world environments. Their core workflow typically follows a perception–reasoning–action–memory cycle. Existing studies primarily emphasize improving memory representations and storage formats, treating memory mainly as an information repository. However, distilling transferable knowledge from stored experiences remains an important yet underexplored challenge. In real-world settings, structures and patterns tend to recur. If an agent can capture and reuse these latent patterns, it can infer new actionable knowledge from prior experience, enabling more efficient and flexible task execution. To explore this capability, we propose Echo. Echo decomposes knowledge into five explicit dimensions of transferability: structure, attribute, process, function, and interaction. Based on this formulation, Echo leverages In-Context Analogy Learning (ICAL) to effectively retrieve past experiences and generalize them to new tasks. Experiments show that, under a from-scratch learning setting, Echo achieves a 1.3×–1.7× speed-up in object-unlocking tasks. Moreover, Echo exhibits a burst-like chain-unlocking phenomenon, rapidly unlocking multiple similar items within a short time interval. These results demonstrate that robust knowledge transfer, driven by effective utilization of contextual examples, is a highly promising direction for advancing open-world multimodal agents.
</details>

---

### PromptEnhancer: Taming Your Rewriter for Text-to-Image Generation Via Fine-Grained Reward
著者: Linqing Wang, zhiyong xu, XiMing Xing, YIJI CHENG, Zhiyuan Zhao, Donghao Li, Tiankai Hang, Zhenxi Li, Jiale Tao, wangqixun wangqixun, Ruihuang Li, Comi Chen, Xin LI, Mingrui Wu, Xinchi Deng, Shuyang Gu, Chunyu Wang, qinglin lu

<details>
<summary> 日本語要旨 </summary>

最近のテキストから画像（T2I）拡散モデルは、高品質な画像を生成する驚異的な能力を示しています。しかし、これらのモデルはしばしば属性バインディング、否定、構成関係といった複雑なユーザープロンプトを忠実にレンダリングすることに苦労します。この課題に対処するために、私たちはPromptEnhancerという新しい普遍的なプロンプト再構成フレームワークを導入します。これは事前学習済みのT2Iモデルの能力を向上させるものです。具体的には、理解とリライトパフォーマンスを系統的に強化するためのマルチステージトレーニングパイプラインを採用しています。第一段階では、CoT（Chain of Thought）対応データを使用した監督付き微調整（SFT）を行い、リライターがチェーン・オブ・シンクスタイルの構造化された回答を生成できるようにします。第二段階では、ユーザープロンプトと細部までの好みをGRPO（Guided Reinforcement Policy Optimization）を通じて一致させるタスク固有の報酬モデル—AlignEvaluator—を設計します。AlignEvaluatorは、T2Iの一般的な失敗ケースから導かれた体系的な分類に基づいて明示的で細部までのフィードバックを提供するようにトレーニングされます。AlignEvaluatorから得られる報酬を最大化することでリライターを最適化することにより、私たちのフレームワークはT2Iモデルがより正確に解釈できるプロンプトを生成する方法を学びます。さらに、この方向性の将来的な研究を促進するための包括的な人間と一致したベンチマークも導入します。広範囲の意味論的および構成的課題にわたって、PromptEnhancerが画像-テキストの整合性を大幅に改善することを示す包括的な実験結果があります。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advances in text-to-image (T2I) diffusion models have demonstrated remarkable capabilities in generating high-fidelity images. However, these models often struggle to faithfully render complex user prompts, particularly in aspects such as attribute binding, negation, and compositional relationships. To address this challenge, we introduce PromptEnhancer, a novel and universal prompt rewriting framework that enhances any pre-trained T2I model. Specifically, we adopt a multi-stage training pipeline to systematically boost the rewriter's understanding and rewriting performance. In the first stage, we conduct supervised fine-tuning (SFT) using CoT-enabled data to enable the rewriter to generate structured, chain-of-thought-style responses. In the second stage, we design a task-specific reward model—AlignEvaluator—to further align user prompts with fine-grained preferences through GRPO. The AlignEvaluator is trained to provide explicit and fine-grained feedback based on a systematic taxonomy derived from common T2I failure cases. By optimizing the rewriter to maximize the reward from AlignEvaluator, our framework learns to generate prompts that T2I models can interpret more precisely. Furthermore, we introduce a comprehensive human-aligned benchmark to facilitate future research in this direction. Extensive experiments demonstrate that PromptEnhancer significantly improves image-text alignment across a wide range of semantic and compositional challenges.
</details>

---

### Wavelet-based Frame Selection By Detecting Semantic Boundary for Long Video Understanding
著者: Wang Chen, Yuhui zeng, Yongdong Luo, Tianyu Xie, Luojun Lin, Jiayi Ji, Yan Zhang, Xiawu Zheng

<details>
<summary> 日本語要旨 </summary>

長尺の動画に大規模ビジョン言語モデル（LVLMs）を適用する際、フレーム選択は高いフレーム冗镳性と限られたコンテキストウィンドウのために重要です。現在の方法では、与えられたクエリに関連度が高いフレームを選択し、動画の物語性構造を無視した不連続なフレームセットを生成します。本論文では、トレーニング不要の新たな枠組みであるウェーブレットベースのフレーム選択によるセマンティック境界検出（WFS-SB）を紹介します。これは、効果的な動画理解が高い関連性だけでなく、物語性の変化点として重要なセマンティックシフトを捕捉することに依存するという新しい視点を提示します。しかし、クエリ-フレーム類似性信号の急激な変化を直接検出することは、モデル不確実性や一時的な視覚的変動による高周波ノイズが原因でしばしば信頼性が低いです。この問題を解決するために、ウェーブレット変換を利用します。これは時間と周波数の両方のドメインで多重解像度分析を提供し、理想的なソリューションです。この変換を適用することで、ノイズ信号を複数のスケールに分解し、最も粗いスケールからクリーンなセマンティックシフト信号を抽出します。この信号の局所極大値をセマンティック境界として識別し、動画を連続したクリップに分割します。これに基づき、WFS-SBは二段階戦略で構成されます：まず、各クリップに対して複合重要度スコアに基づいてフレーム予算を適応的に割り当てること；次に、各クリップ内で最大マージナル関連性アプローチを用いて多様かつ関連するフレームセットを選択します。広範な実験では、WFS-SBがLVLMのパフォーマンスを大幅に向上させることが示されています。例えば、VideoMMEで5.5％、MLVUで9.5％、LongVideoBenchで6.2％の精度改善が見られ、常に最先端の方法を上回っています。
</details>

<details>
<summary> 英語要旨 </summary>

Frame selectoin is crucial due to high frame redundancy and limited context windows when applying Large Vision-Language Models (LVLMs) to long videos. Current methods typically select frames with high relevance to a given query, resulting a disjointed set of frames that disregard the narrative structure of video. In this paper, we introduce $\textbf{W}$avelet-based $\textbf{F}$rame $\textbf{S}$election by Detecting $\textbf{S}$emantic $\textbf{B}$oundary ($\textbf{WFS-SB}$), a training-free framework that presents a new perspective: effective video understanding hinges not only on high relevance but, more importantly, on capturing semantic shifts—pivotal moments of narrative change that are essential to comprehending the holistic storyline of video. However, a direct detection of abrupt changes in the query-frame similarity signal is often unreliable due to high-frequency noise arising from model uncertainty and transient visual variations. To address this, we leverage the wavelet transform, which provides an ideal solution through its multi-resolution analysis in both time and frequency domains. By applying this transform, we decompose the noisy signal into multiple scales and extract a clean semantic change signal from the coarsest scale. We identify the local extrema of this signal as semantic boundaries, which segment the video into coherent clips. Building on this, WFS-SB comprises a two-stage strategy: first, adaptively allocating a frame budget to each clip based on a composite importance score; and second, within each clip, employing the Maximal Marginal Relevance approach to select a diverse yet relevant set of frames. Extensive experiments show that WFS-SB significantly boosts LVLM performance, e.g., improving accuracy by $\textbf{5.5\\% on VideoMME, 9.5\\% on MLVU, and 6.2\\% on LongVideoBench}$, consistently outperforming state-of-the-art methods.
</details>

---

### NaTex: Seamless Texture Generation As Latent Color Diffusion
著者: Zeqiang Lai, Yunfei Zhao, Zibo Zhao, Xin Yang, Xin Huang, Jingwei Huang, Xiangyu Yue, Chunchao Guo

<details>
<summary> 日本語要旨 </summary>

私たちは、NaTexというネイティブなテクスチャ生成フレームワークを紹介します。これは3D空間で直接テクスチャの色を予測するものです。以前のアプローチが幾何学条件付きマルチビュー拡散モデル（MVD）によって合成された2Dマルチビュー画像を焼き付けることに依存しているのに対し、NaTexはMVDパイプライン固有のいくつかの制限を回避します。これらの制限には、補完が必要な隠れた領域の処理の難しさ、境界沿いでのメッシュテクスチャの正確な整列の実現、および内容と色強度の両方における異視点間の一貫性と連続性の維持が含まれます。NaTexはテクスチャを密集したカラーポイントクラウドとして見なす新しいパラダイムを特徴としており、これによって上記の問題を解決します。この考え方に基づき、幾何学認識カラーポイントクラウドVAEと多制御拡散変換器（DiT）からなる新しい概念である「潜在色拡散」を提案します。これは3Dデータのみを用いてスクラッチからトレーニングされ、テクスチャ再構築と生成に使用されます。正確な整列を可能にするために、DiTを直接3D空間情報で条件付けるネイティブ幾何学制御を導入します。これは位置埋め込みと幾何学潜在変数を用いて行われます。また、色VAEに密接に結合された献身的な幾何学ブランチから抽出される幾何学潜在変数を備えたVAE–DiTアーキテクチャを共同設計します。これにより、細部までの表面ガイダンスが提供され、テクスチャと強い対応関係を維持します。このデザインにより、NaTexはテクスチャの一貫性と整列において大幅なパフォーマンス向上を示し、以前の方法を大きく凌駕しています。さらに、NaTexはトレーニングフリーまたは簡単なチューニングで強力な汎用性を発揮し、材質生成、テクスチャの洗練、および部品セグメンテーションとテクスチャリングなど様々な下流アプリケーションに適用可能です。
</details>

<details>
<summary> 英語要旨 </summary>

We present NaTex, a native texture generation framework that predicts texture color directly in 3D space. In contrast to previous approaches that rely on baking 2D multi-view images synthesized by geometry-conditioned Multi-View Diffusion models (MVDs), NaTex avoids several inherent limitations of the MVD pipeline. These include difficulties in handling occluded regions that require inpainting, achieving precise mesh-texture alignment along boundaries, and maintaining cross-view consistency and coherence in both content and color intensity. NaTex features a novel paradigm that addresses the aforementioned issues by viewing texture as a dense color point cloud. Driven by this idea, we propose latent color diffusion, which comprises a geometry-awared color point cloud VAE and a multi-control diffusion transformer (DiT), entirely trained from scratch using 3D data, for texture reconstruction and generation. To enable precise alignment, we introduce native geometry control that conditions the DiT on direct 3D spatial information via positional embeddings and geometry latents. We co-design the VAE–DiT architecture, where the geometry latents are extracted via a dedicated geometry branch tightly coupled with the color VAE, providing fine-grained surface guidance that maintains strong correspondence with the texture. With these designs, NaTex demonstrates strong performance, significantly outperforming previous methods in texture coherence and alignment. Moreover, NaTex also exhibits strong generalization capabilities, either training-free or with simple tuning, for various downstream applications, e.g., material generation, texture refinement, and part segmentation and texturing.
</details>

---

### Stable Mean Flow: Lyapunov-Inspired One-Step Flow Matching
著者: Guangxun Zhang, Mason Haberle, Davi Geiger

<details>
<summary> 日本語要旨 </summary>

Mean Flow Matchingアルゴリズムは、一ステップ生成モデルにおける最先端技術です。この考えを基に、我々はStable Mean Flowアルゴリズムを提案し、単一ステップの輸送マップの局所的非拡張性を強制するLyapunov型安定化正則化子を導入します。この設計により、特徴量の一意性が保証され、軌道のずれが制限されます。実験ではMean Flowと比較して出力品質と収束速度が向上することを示しました。さらに、一ステップおよび多ステップ生成の両方に対する誤差増加の明確な上限を設定します。
</details>

<details>
<summary> 英語要旨 </summary>

The Mean Flow Matching algorithm is the state-of-the-art for one-step generative models. Building on this idea, we propose the Stable Mean Flow algorithm and introduce a Lyapunov-inspired stability regularizer that enforces local non-expansivity of the single-step transport map. This design guarantees uniqueness of characteristics and bounds trajectory drift. We conduct experiments that show improved output quality and convergence speed over Mean Flow. Moreover, we establish explicit upper bounds on error growth for both one-step and multi-step generation.
</details>

---

### Bridging Fidelity-Reality with Controllable One-Step Diffusion for Image Super-Resolution
著者: Hao Chen, Junyang Chen, Jinshan Pan, Jiangxin Dong

<details>
<summary> 日本語要旨 </summary>

最近の拡散ベースの一ステップ法は超解像画像分野で顕著な進歩を遂げていますが、3つの重要な制約に直面しています：（1）低品質（LQ）入力の圧縮符号化による情報損失に起因する劣った忠実度性能；（2）生成的事前知識の領域差別的活性化が不十分であること；（3）テキストプロンプトとその対応する意味論的領域との整合性の欠如。これらの制約に対処するため、我々は画像超解像用の可制御一ステップ拡散ネットワークであるCODSRを提案します。まず、LQ入力から得られる元の非圧縮情報を利用して拡散過程に高忠実度な条件付けを提供するために、LQガイド付き特徴変調モジュールを提案します。次に、局所構造の忠実性を犠牲にせずに知覚的豊かさを効果的に向上させるために、領域適応生成的事前知識活性化方法を開発します。最後に、テキストプロンプトの条件付けポテンシャルを完全に引き出すためにテキストマッチングガイダンス戦略を採用します。広範な実験は、CODSRが効率的な一ステップ推論を維持しながら、最先端の手法と競合する忠実度性能を達成し、優れた知覚品質を示すことを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Recent diffusion-based one-step methods have shown remarkable progress in the field of image super-resolution, yet they remain constrained by three critical limitations: (1) inferior fidelity performance caused by the information loss from compression encoding of low-quality (LQ) inputs; (2) insufficient region-discriminative activation of generative priors; (3) misalignment between text prompts and their corresponding semantic regions. To address these limitations, we propose CODSR, a controllable one-step diffusion network for image super-resolution. First, we propose an LQ-guided feature modulation module that leverages original uncompressed information from LQ inputs to provide high-fidelity conditioning for the diffusion process. We then develop a region-adaptive generative prior activation method to effectively enhance perceptual richness without sacrificing local structural fidelity. Finally, we employ a text-matching guidance strategy to fully harness the conditioning potential of text prompts. Extensive experiments demonstrate that CODSR achieves superior perceptual quality and competitive fidelity compared with state-of-the-art methods while maintaining efficient one-step inference.
</details>

---

### DreamOmni2: Multimodal Instruction-based Generation and Editing
著者: Bin Xia, Bohao Peng, Yuechen Zhang, Junjia Huang, JiyangLiu JiyangLiu, Jingyao Li, Haoru Tan, WU Sitong, Chengyao Wang, Yitong Wang, Bei Yu, Jiaya Jia

<details>
<summary> 日本語要旨 </summary>

最近の指示に基づく画像編集と主題駆動型生成技術は大きな注目を集めていますが、両方のタスクは依然として実用的なユーザー要求を満たすには限界があります。指示に基づく編集は言語指示だけに頼っており、具体的な編集詳細を捉えることが難しく、参考画像が必要です。一方で、主題駆動型生成は具体的なオブジェクトや人物の組み合わせに限定されており、広範な抽象的概念を見落としています。これらの課題に対処するため、私たちは二つの新しいタスクを提案します：マルチモーダル指示に基づく編集と生成です。これらのタスクはテキストおよび画像の両方の指示をサポートし、具体的かつ抽象的な概念を含む範囲を拡大することで、その実用性が大幅に向上します。私たちはDreamOmni2を導入し、二つの主要な課題に取り組みます：データ作成とモデルフレームワーク設計です。私たちのデータ合成パイプラインは三つのステップで構成されています：（1）具体的および抽象的な概念の抽出データを作成するために特徴混合法を使用、（2）編集モデルと抽出モデルを用いてマルチモーダル指示に基づく編集トレーニングデータを生成、（3）さらに抽出モデルを適用してマルチモーダル指示に基づく編集のトレーニングデータを作成します。フレームワークについては、複数画像入力を処理するためにインデックスエンコーディングと位置エンコーディングシフト方式を提案しました。これにより、モデルが画像を区別しピクセルの混乱を避けることができます。また、複雑な指示処理を向上させるために、VLMと私たちの生成・編集モデルのジョイントトレーニングも導入しました。さらに、これら二つの新しいタスクの開発を促進する包括的なベンチマークを提案しています。実験結果はDreamOmni2が印象的な成果を達成したことを示しています。モデルとコードはリリースされます。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advancements in instruction-based image editing and subject-driven generation have garnered significant attention, yet both tasks still face limitations in meeting practical user needs. Instruction-based editing relies solely on language instructions, which often fail to capture specific editing details, making reference images necessary. Meanwhile, subject-driven generation is limited to combining concrete objects or people, overlooking broader, abstract concepts. To address these challenges, we propose two novel tasks: multimodal instruction-based editing and generation. These tasks support both text and image instructions and extend the scope to include both concrete and abstract concepts, greatly enhancing their practical applications. We introduce DreamOmni2, tackling two primary challenges: data creation and model framework design. Our data synthesis pipeline consists of three steps: (1) using a feature mixing method to create extraction data for both abstract and concrete concepts, (2) generating multimodal instruction-based editing training data using the editing and extraction models, and (3) further applying the extraction model to create training data for multimodal instruction-based editing. For the framework, to handle multi-image input, we propose an index encoding and position encoding shift scheme, which helps the model distinguish images and avoid pixel confusion. Additionally, we introduce joint training with the VLM and our generation/editing model to better process complex instructions. In addition, we have proposed comprehensive benchmarks for these two new tasks to drive their development. Experiments show that DreamOmni2 has achieved impressive results. Models and codes will be released.
</details>

---

### Flow3r: Factored Flow Prediction for Visual Geometry Learning
著者: Zhongxiao Cong, Qitao Zhao, Minsik Jeon, Shubham Tulsiani

<details>
<summary> 日本語要旨 </summary>

私たちは、未ラベルの単眼動画を利用して流れ予測を活用する可視化幾何学学習のスケーラブルなフレームワークであるFlow3rを提案します。現在の3D/4D再構成システムは主に密な幾何学と姿勢の監督に依存しており、多様な動的な実世界のシーンへの一般化が容易ではありません。本研究では、未ラベルのビデオから直接トレーニングを強化するメカニズムを提案します。これは任意の画像ペア間の密な2D対応（または「流れ」）を監督として活用します。私たちの重要な洞察は、一つの画像から得られる「幾何学ラテンス」ともう一方の画像から得られる「姿勢ラテンス」を使用して2つの画像から計算される因子分解流れ予測モジュールが可視化幾何学学習を導くことです。まず、制御された設定での流れ監督の利点とスケーラビリティを強調し、その後大規模な未ラベルデータを活用してオフ・ザ・シェルフの可視化幾何学モデルを改善します。Flow3rは多様な3Dベンチマークで評価し、競争力のあるまたは最先端の性能を示しました。これはより多くのラベル付きデータでトレーニングされた監督モデルをも上回っています。
</details>

<details>
<summary> 英語要旨 </summary>

We propose Flow3r, a scalable framework for visual geometry learning that leverages flow prediction to guide learning using unlabeled monocular videos. Current 3D/4D reconstruction systems primarily rely on dense geometry and pose supervision, and cannot easily generalize to diverse dynamic real-world scenes. In this work, we propose a mechanism to augment training directly from unlabeled videos, leveraging dense 2D correspondences (or ‘flow’) between arbitrary image pairs as supervision. Our key insight is that a factored flow prediction module that computes from two images using ‘geometry latents’ from one image and the ‘pose latent’ from the othercan guide visual geometry learning. We first highlight the benefits and scalability of flow supervision in controlled settings and then leverage large-scale unlabeled data to improve off-the-shelf visual geometry models. We evaluate Flow3r across diverse 3D benchmarks and demonstrate competitive or state-of-the-art performance, even surpassing supervised models trained with more labeled data.
</details>

---

### Particulate: Feed-Forward 3D Object Articulation
著者: Ruining Li, YUXIN YAO, Chuanxia Zheng, Christian Rupprecht, Joan Lasenby, Shangzhe Wu, Andrea Vedaldi

<details>
<summary> 日本語要旨 </summary>

私たちは、Particulateというフィードフォワードモデルを紹介します。このモデルは、日常的なオブジェクトの単一の静止3Dメッシュから、その3Dパーツ、運動構造、および関節パラメータを予測します。従来のアーティキュレートされた3Dオブジェクトモデリングは、高コストな個別最適化や小規模な検索データベースに限定されているか、または大規模なビジョンや言語のファウンデーションモデルを必要としますが、私たちのアプローチは柔軟でスケーラブルかつ軽量なトランスフォーマー構造に基づいています。Particulateは、公開された多様なアーティキュレート3D資産のコレクションで訓練され、画像から3Dモデルを生成した新しいオブジェクトを含む、未知のオブジェクトのアーティキュレート構造を正確に推定することができます。これは単一のフィードフォワードパスで行われます。さらに、高品質な公開3D資産から編纂されたアーティキュレート3Dオブジェクト推定のベンチマークを導入します。量的および質的結果は、Particulateが最先端の手法を大幅に上回ることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

We introduce Particulate, a feed-forward model that, given a single static 3D mesh of an everyday object, predicts its 3D parts, kinematic structure, and articulation parameters. Unlike prior work on articulated 3D object modeling that is limited by costly per-object optimization and small retrieval databases or requires large vision or language foundation models, our approach is based on a flexible, scalable and lightweight transformer architecture. Trained on a diverse collection of articulated 3D assets from public datasets, Particulate accurately infers the articulated structure of novel objects, including those generated by image-to-3D models, in a single feed-forward pass. We further introduce a benchmark for articulated 3D object estimation curated from high-quality public 3D assets. Quantitative and qualitative results show that Particulate significantly outperforms state-of-the-art approaches.
</details>

---

### Motion 3-to-4: 3D Motion Reconstruction for 4D Synthesis
著者: hongyuan chen, Xingyu Chen, Zexiang Xu, Anpei Chen

<details>
<summary> 日本語要旨 </summary>

私たちは、単眼ビデオと任意の3D参照メッシュから高品質な4次元動的オブジェクトを合成するフィードフォワードフレームワーク「Motion 3-to-4」を提案します。最近の進歩により、2D画像、ビデオ、および3Dコンテンツ生成は大幅に向上しましたが、4次元合成は依然として限られたトレーニングデータと単眼視点からの幾何学的形状および動きの回復の固有の曖昧さにより難しいです。Motion 3-to-4は、静的な3D形状生成と運動再構築に分解することでこれらの課題に対処します。標準参照メッシュを使用して、私たちのモデルはコンパクトな運動ラテント表現を学習し、フレームごとの頂点軌道を予測することで完全かつ時間的に一貫した幾何学を回復します。スケーラブルなフレーム単位トランスフォーマーは、異なるシーケンス長に対して堅牢性をさらに強化します。標準的なベンチマークおよび正確なグラウンドトゥルース幾何学を持つ新しいデータセットでの評価結果は、Motion 3-to-4が以前の研究に比べて優れた忠実度と空間的一貫性を提供することを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

We present Motion 3-to-4, a feed-forward framework for synthesising high-quality 4D dynamic objects from a single monocular video and an optional 3D reference mesh. While recent advances have significantly improved 2D, video, and 3D content generation, 4D synthesis remains difficult due to limited training data and the inherent ambiguity of recovering geometry and motion from a monocular viewpoint. Motion 3-to-4 addresses these challenges by decomposing 4D synthesis into static 3D shape generation and motion reconstruction. Using a canonical reference mesh, our model learns a compact motion latent representation and predicts per-frame vertex trajectories to recover complete, temporally coherent geometry. A scalable frame-wise transformer further enables robustness to varying sequence lengths. Evaluations on both standard benchmarks and a new dataset with accurate ground-truth geometry show that Motion 3-to-4 delivers superior fidelity and spatial consistency compared to prior work.
</details>

---

### What Is It Like to Be A Noise? An Entropy-based Gaussian Noise Regularization for Diffusion Models
著者: Pascal Chang, Kai Lascheit, Jingwei Tang, Markus Gross, Vinicius C. Azevedo

<details>
<summary> 日本語要旨 </summary>

拡散モデルにおけるノイズラテンスの最適化は、制御可能な生成、報酬ガイド付きサンプリング、ラテンス逆転に強力ですが、そのプロセスは非常に不安定です。原理的な正則化子がないと、最適化されたラテンスはガウシアン事前分布から離れてしまい、典型集合から崩壊して重大なアーティファクトを生じさせます。既存の制約であるノルムマッチングや単純なKLダイバージェンス損失は、しばしば不十分であり、真のガウシアンノイズの全統計的特性を捉えられません。私たちは、高質量典型集合ではなく高確率モードを正しくターゲットにする原理的で微分可能な正則化子を提案します。私たちのエネルギー関数は低次統計をマッチングすることでKLダイバージェンスを実用的に近似します。これは、ピクセル値ヒストグラムを一致させる1Dの偏微分項と、非相関性を強制する2Dの空間項を組み合わせています。この方法をマルチスケールピラミッドで適用することにより、すべての範囲で相関を罰し、サンプルを真のガウシアン典型集合に近く射影します。この方法が堅牢でアーティファクトフリーな報酬ガイド付き生成とモデルフリーのラテンス逆転において効果的であることを示します。
</details>

<details>
<summary> 英語要旨 </summary>

Optimizing noise latents in diffusion models is powerful for controllable generation, reward-guided sampling, and latent inversion, but the process is notoriously unstable. Without a principled regularizer, optimized latents drift away from the Gaussian prior, collapsing out of the typical set and producing severe artifacts. Existing constraints like norm-matching or simple KL divergence losses are often insufficient, as they fail to capture the full statistical properties of true Gaussian noise. We propose a principled, differentiable regularizer that correctly targets the high-mass typical set rather than the high-probability mode. Our energy function tractably approximates the KL divergence by matching low-order statistics. It combines a 1D marginal term to match the pixel-value histogram and a 2D spatial term to enforce decorrelation. By applying this in a multi-scale pyramid, our method penalizes correlations at all ranges, effectively projecting samples closer onto the true Gaussian typical set. We demonstrate its effectiveness for robust, artifact-free reward-guided generation and model-free latent inversion.
</details>

---

### VINS-120K: Ultra High-Resolution Image Editing with A Large-Scale Dataset
著者: Zhizhou Chen, Shanyan Guan, Zhanxin Gao, En Ci, Yanhao Ge, Wei Li, Zhenyu Zhang, Jian Yang, Ying Tai

<details>
<summary> 日本語要旨 </summary>

超高解像度（UHR）画像の直接編集は価値があるものの、まだ十分に探求されていない。その主な理由として、高品質データの不足と高周波テキスト詳細をモデリングする難しさが挙げられる。私たちは指示に基づくUHR画像編集用の最初の大規模なデータセットであるVINS-120Kを導入し、これは指示、入力画像、および編集された画像から成る12万件の慎重に選ばれたトリプレットで構成されている。各画像は4K解像度を超え（4096×4096以上）、視覚品質、指示の整合性、および美的忠実性を確保するために厳格な多段階パイプラインでフィルタリングされている。第二の課題として、以前の非高解像度モデルが細部まで正確に高周波詳細を生成することを可能にする高周波に対応したポスト適応戦略を提案する。さらに、UHR環境での一貫した評価を促進するために、多様な編集タイプをカバーするベンチマークVINS-4KEvalを提示する。実験結果は、私たちの作業がUHR画像編集で優れた細部とテクスチャリアリズムを提供していることを確認している。データセットとコードは公開される予定である。
</details>

<details>
<summary> 英語要旨 </summary>

Directly editing ultra-high-resolution (UHR) images is valuable but underexplored, primarily due to the lack of high-quality data and the challenge in modeling high-frequency textual details. We introduce VINS-120K, the first large-scale dataset for instruction-based UHR image editing, comprising 120K carefully curated triplets of instruction, input image, and edited image. Each image exceeds 4K resolution ($\geq$4096×4096) and is filtered through a rigorous multi-stage pipeline to ensure visual quality, instruction alignment, and aesthetic fidelity. For the second challenge, we propose a high-frequency-aware post-adaptation strategy that allows previous non-high-resolution models to accurately generate fine-grained, high-frequency details. We further present VINS-4KEval, a benchmark covering diverse editing types, to facilitate consistent evaluation in UHR settings. Experiments confirm that our work delivers superior fine-grained detail and texture realism in UHR image editing. The dataset and code will be released.
</details>

---

### FlashPortrait: 6$\times$ Faster Infinite Portrait Animation with Adaptive Latent Prediction
著者: Shuyuan Tu, Yueming Pan, Yinming Huang, Xintong Han, Zhen Xing, Qi Dai, Kai Qiu, Chong Luo, Zuxuan Wu

<details>
<summary> 日本語要旨 </summary>

現在の長尺ポートレートアニメーション用の拡散ベースの加速方法は、アイデンティティ（ID）一貫性を確保することに苦労しています。本論文では、FlashPortraitというエンド・トゥ・エンドのビデオ拡散変換器を紹介します。これは、アイデンティティを保持しながら無限長の動画を合成し、推論速度を最大6倍に加速することができます。具体的には、FlashPortraitはまずオフ・ザ・シェルフの抽出器を用いてアイデンティティ非依存の顔の表情特徴を計算します。次に、正規化された顔の表情ブロックを導入し、それぞれの平均と分散で正規化することで拡散潜在変数と顔の特徴を整列させます。これにより、顔モデリングにおけるアイデンティティの安定性が向上します。推論時には、重なり領域での加重ブレンドを伴う動的スライディングウィンドウ方式を採用し、長時間アニメーションにおける滑らかな遷移とID一貫性を確保します。各コンテキストウィンドウ内では、特定のタイムステップでの潜在変数の変動率や拡散層間の導関数大きさ比に基づいて、現在のタイムステップでの高次潜在変数導関数を用いて将来のタイムステップの潜在変数を直接予測し、複数のノイズ除去ステップを飛ばして6倍の速度加速を達成します。ベンチマークにおける実験結果は、FlashPortraitが質的・量的に効果的であることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Current diffusion-based acceleration methods for long-portrait animation struggle to ensure identity (ID) consistency. This paper presents FlashPortrait, an end-to-end video diffusion transformer capable of synthesizing ID-preserving, infinite-length videos while achieving up to 6$\times$ acceleration in inference speed. In particular, FlashPortrait begins by computing the identity-agnostic facial expression features with an off-the-shelf extractor. It then introduces a Normalized Facial Expression Block to align facial features with diffusion latents by normalizing them with their respective means and variances, thereby improving identity stability in facial modeling. During inference, FlashPortrait adopts a dynamic sliding-window scheme with weighted blending in overlapping areas, ensuring smooth transitions and ID consistency in long animations. In each context window, based on the latent variation rate at particular timesteps and the derivative magnitude ratio among diffusion layers, FlashPortrait utilizes higher-order latent derivatives at the current timestep to directly predict latents at future timesteps, thereby skipping several denoising steps and achieving 6$\times$ speed acceleration. Experiments on benchmarks show the effectiveness of FlashPortrait both qualitatively and quantitatively.
</details>

---

