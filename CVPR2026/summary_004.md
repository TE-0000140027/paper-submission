# CVPR2026 論文要旨 (Part 4)

### Edit2Perceive: Image Editing Diffusion Models Are Strong Dense Perceivers
著者: Yiqing Shi, Yiren Song, Mike Zheng Shou

<details>
<summary> 日本語要旨 </summary>

最近の拡散変換器に関する進歩は、視覚合成において顕著な汎化性能を示していますが、多くの密度推定手法は依然として確率的生成を目的としたテキストから画像（T2I）ジェネレーターに依存しています。このパラダイムを再検討し、画像編集の拡散モデルが本質的に画像間で一貫性があることを示します。これは密度推定タスクに適したより良い基盤を提供します。私たちは、編集モデルを深さ、法線、マッティングに適応させる統一的な拡散フレームワークであるEdit2Perceiveを導入します。FLUX.1 Kontextアーキテクチャの上に構築された私たちのアプローチは、全パラメーター微調整とピクセル空間での一貫性損失を用いて、中間ノイズ除去状態にわたる構造保存的な洗練を強制します。さらに、私たちの単一ステップ決定論的推論は、比較的小規模なデータセットでのトレーニングでも最大で実行時間が速くなります。広範囲にわたる実験では、すべての3つのタスクにおいて総合的な最先端結果を示し、幾何学認識に対する編集指向の拡散変換器の強力な可能性を明らかにしています。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advances in diffusion transformers have shown remarkable generalization in visual synthesis, yet most dense perception methods still rely on text-to-image (T2I) generators designed for stochastic generation. We revisit this paradigm and show that image editing diffusion models are inherently image-to-image consistent, providing a more suitable foundation for dense perception task. We introduce Edit2Perceive, a unified diffusion framework that adapts editing models for depth, normal, and matting. Built upon the FLUX.1 Kontext architecture, our approach employs full-parameter fine-tuning and a pixel-space consistency loss to enforce structure-preserving refinement across intermediate denoising states. Moreover, our single-step deterministic inference yields up to faster runtime while training on relatively small datasets. Extensive experiments demonstrate comprehensive state-of-the-art results across all three tasks, revealing the strong potential of editing-oriented diffusion transformers for geometry-aware perception.
</details>

---

### MultiBanana: A Challenging Benchmark for Multi-Reference Text-to-Image Generation
著者: Yuta Oshima, Daiki Miyake, Kohsei Matsutani, Yusuke Iwasawa, Masahiro Suzuki, Yutaka Matsuo, Hiroki Furuta

<details>
<summary> 日本語要旨 </summary>

最近のテキストから画像生成モデルは、複数の参照画像から被写体の外観を受け継ぎ、新しい文脈で再レンダリングする能力を獲得しています。しかし、既存のベンチマークデータセットは通常、単一または少数の参照画像に基づく生成に焦点を当てており、これが異なる複数参照条件下でモデル性能の進歩を測定したり、その弱点を指摘することを妨げています。さらに、タスクの定義は曖昧で、「何を編集するか」や「与えられる参照画像の数」といった軸に限定されがちであり、結果として多重参照設定の固有の難しさを捉えきれていません。このギャップを埋めるために、私たちはMultiBananaを導入します。これは、モデル能力の限界を広範に評価するよう設計されており、多重参照特有の問題をスケールでカバーしています：(1) 参照画像の数を変化させること、(2) 参照間のドメイン不一致（例えば、写真対アニメ）、(3) 参照とターゲットシーンのスケール不一致、(4) 珍しい概念を含む参照画像（例えば、赤いバナナ）、および (5) 描写用の多言語テキスト参照。さまざまなテキストから画像生成モデルに対する分析は、それらの優れたパフォーマンス、典型的な失敗モード、改善すべき領域を明らかにします。MultiBananaはオープンベンチマークとしてリリースされ、多重参照画像生成のための公平な比較基準を確立し、その限界を押し広げることに貢献します。
</details>

<details>
<summary> 英語要旨 </summary>

Recent text-to-image generation models have acquired the ability of multi-reference generation and editing; the ability to inherit the appearance of subjects from multiple reference images and re-render them under new contexts. However, the existing benchmark datasets often focus on the generation with single or a few reference images, which prevents us from measuring the progress on how model performance advances or pointing out their weaknesses, under different multi-reference conditions. In addition, their task definitions are vague, typically limited to axes such as "what to edit" or "how many references are given", and therefore fail to capture the intrinsic difficulty of multi-reference settings. To address this gap, we introduce MultiBanana, which is carefully designed to assesses the edge of model capabilities by widely covering multi-reference-specific problems at scale: (1) varying the number of references, (2) domain mismatch among references (e.g., photo vs. anime), (3) scale mismatch between reference and target scenes, (4) references containing rare concepts (e.g., a red banana), and (5) multilingual textual references for rendering. Our analysis among a variety of text-to-image models reveals their superior performances, typical failure modes, and areas for improvement. MultiBanana will be released as an open benchmark to push the boundaries and establish a standardized basis for fair comparison in multi-reference image generation.
</details>

---

### HandX+: Scaling Up Text-Conditioned Bimanual Motion Generation
著者: Zimu Zhang, Yucheng Zhang, Xiyan Xu, Ziyin Wang, Sirui Xu, Kai Zhou, Bing Zhou, Chuan Guo, Jian Wang, Yu-Xiong Wang, Liangyan Gui

<details>
<summary> 日本語要旨 </summary>

テキスト条件付きの人間動作およびビデオ生成は急速に進歩していますが、リアルな手の動きや両手の相互作用は依然として大幅に未探索です。既存の全身モデルは、自然な器用な行動を実現するために必要な微細な詳細（指の可動性、接触タイミング、両手間の調整）をしばしば見落としています。このギャップを埋めるために、私たちは手中心のアニメーションフレームワークを導入します。基盤として、多様な情報源から得られた大規模な動作データを厳格なアニメーション品質管理のもとで統合した一貫したコーパスを構築します。この過程で、既存リソースの多くにおける制限点を特定しました：微細な指動作や両手間の協調を捉えた高精度な双手動作データの不在です。これを解決するため、欠落している側面を豊かにする新しいデータセットを収集します。運動言語アライメントを自動的にスケールさせるために、大規模な言語モデルが生の動作シーケンス上で直接推論するのではなく、分離されたパラダイムを提案します。これは、接触イベントや指屈曲といった代表的な運動特徴を抽出し、その後LLMの推論を利用してこれらの特徴に合致した細部まで描写された意味豊かな記述を生成します。私たちのコーパスと注釈に基づき、拡散およびFSQベースのアーキテクチャを用いてベンチマークモデルを開発し、標準的なテキスト条件付き生成、手反応合成、運動インビトウェニング、キーフレームガイド生成、長期間の時間的組み立てといった多様な条件モードを可能にします。実験では、私たちのアプローチが強力なテキストアライメント、高品質な器用動作、正確な接触予測を達成しており、これは新しく設計された手アニメーションに特化した指標で支持されています。さらに、明確なスケーリング挙動を観察しました：より大きく、高品質のデータセットで訓練されたモデルは、意味的に一貫した双手動作を顕著に生成します。すべてのデータを将来の研究支援のために公開します。
</details>

<details>
<summary> 英語要旨 </summary>

Text-conditioned human motion and video generation have progressed rapidly, yet realistic hand motion and bimanual interaction remain significantly underexplored. Existing whole-body models often overlook the fine-grained details required for natural dexterous behavior, such as finger articulation, contact timing, and inter-hand coordination. We aim to close this gap by introducing a hand-centric animation framework. As a foundation, we consolidate large-scale motion data from diverse sources into a unified corpus with rigorous animation quality control. Through this process, we identify a limitation in most of the existing resources: the absence of high-fidelity bimanual motion data that capture nuanced finger dynamics and inter-hand collaboration. To remedy this, we collect a new dataset designed to enrich these underrepresented aspects. To scale motion-language alignment automatically, rather than relying on large language models to directly reason over raw motion sequences, we propose a decoupled paradigm. It extracts representative motion features, such as contact events and finger flexion, and then leverages LLM's reasoning to generate fine-grained, semantically rich descriptions aligned with these features. Building on our corpus and annotations, we develop benchmark models using diffusion and FSQ-based architectures and enable versatile conditioning modes, including standard text-conditioned generation, hand-reaction synthesis, motion inbetweening, keyframe-guided generation, and long-horizon temporal composition. Experiments show that our approach achieves strong text alignment, high-quality dexterous motion, and accurate contact prediction, supported by newly designed metrics tailored for hand animation. We additionally observe clear scaling behavior: larger models trained on larger, higher-quality datasets produce markedly more semantically coherent bimanual motions. All data will be released to support future research.
</details>

---

### Mixture of Style Experts for Diverse Image Stylization
著者: Shihao Zhu, Ziheng Ouyang, Yijia Kang, Qilong Wang, Mi Zhou, Bo Li, Ming-Ming Cheng, Qibin Hou

<details>
<summary> 日本語要旨 </summary>

拡散に基づくスタイリゼーションは大きな進歩を遂げていますが、既存の方法は色駆動型変換に限定され、複雑なセマンティクスや材質の詳細を無視しています。私たちは、Mixture of Experts（MoE）に基づくセマンティック・アウェアフレームワークであるStyleExpertを提案します。このフレームワークは、大規模なコンテンツ-スタイル-スタイリゼーショントリプレットデータセットに基づいて訓練された統一型のスタイルエンコーダーを使用し、多様なスタイルを一貫した潜在空間に埋め込みます。この埋め込みは、類似性に基づくゲートメカニズムで条件付けられ、動的に専門家にスタイルをルーティングします。MoEアーキテクチャ内の特化した専門家です。このMoEアーキテクチャを活用することで、私たちの方法は、浅いテクスチャから深いセマンティクスに至るまで多様なスタイルを巧みに処理します。広範な実験により、StyleExpertが既存のアプローチと比較してセマンティクスや材質の詳細を保持し、未見のスタイルへも一般化することが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

Diffusion-based stylization has advanced significantly, yet existing methods are limited to color-driven transformations, neglecting complex semantics and material details. We introduce StyleExpert, a semantic-aware framework based on Mixture of Experts (MoE). Our framework employs a unified style encoder, trained on our large-scale dataset of content-style-stylized triplets, to embed diverse styles into a consistent latent space. This embedding is then used to condition a similarity-aware gating mechanism, which dynamically routes styles to specialized experts within the MoE architecture. Leveraging this MoE architecture, our method adeptly handles diverse styles spanning multiple semantic levels, from shallow textures to deep semantics. Extensive experiments show that StyleExpert outperforms existing approaches in preserving semantics and material details, while generalizing to unseen styles.
</details>

---

### Image Generation from Contextually-Contradictory Prompts
著者: Saar Huberman, Or Patashnik, Omer Dahary, Ron Mokady, Daniel Cohen-Or

<details>
<summary> 日本語要旨 </summary>

テキストから画像への拡散モデルは、自然言語プロンプトから高品質で多様な画像を生成することに優れています。しかし、学習済みの事前知識と矛盾するコンセプト組み合わせが含まれる場合、しばしば意味的に正確な結果を生成できません。この失敗モードを文脈的矛盾と定義し、学習中に絡み合った関連付けのために一つのコンセプトが他を暗黙的に否定する場合です。これに対処するために、特定のノイズ除去段階での意味内容にマッチしたプロキシープロンプトの順序を用いてノイズ除去過程をガイドするステージ認識型プロンプト分解フレームワークを提案します。各プロキシープロンプトは、文脈的一貫性を保ちながら、特定のノイズ除去段階で現れるべき意味内容にマッチするよう構築されます。これらのプロキシープロンプトを構築するために、大規模言語モデル（LLM）を利用してターゲットプロンプトを分析し、矛盾を特定し、元の意図を保持しつつ文脈的な衝突を解決する代替表現を生成します。プロンプト情報とノイズ除去進行を整合させることで、私たちの方法は細かい意味制御を可能にし、文脈的矛盾が存在する中でも正確な画像生成を実現します。多様な挑戦的プロンプトにわたる実験では、テキストプロンプトへの整合性が大幅に向上していることが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

Text-to-image diffusion models excel at generating high-quality, diverse images from natural language prompts. However, they often fail to produce semantically accurate results when the prompt contains concept combinations that contradict their learned priors. We define this failure mode as contextual contradiction, where one concept implicitly negates another due to entangled associations learned during training. To address this, we propose a stage-aware prompt decomposition framework that guides the denoising process using a sequence of proxy prompts. Each proxy prompt is constructed to match the semantic content expected to emerge at a specific stage of denoising, while ensuring contextual coherence. To construct these proxy prompts, we leverage a large language model (LLM) to analyze the target prompt, identify contradictions, and generate alternative expressions that preserve the original intent while resolving contextual conflicts. By aligning prompt information with the denoising progression, our method enables fine-grained semantic control and accurate image generation in the presence of contextual contradictions. Experiments across a variety of challenging prompts show substantial improvements in alignment to the textual prompt.
</details>

---

### PixelDiT: Pixel Diffusion Transformers for Image Generation
著者: Yongsheng Yu, Wei Xiong, Weili Nie, Yichen Sheng, Shiqiu Liu, Jiebo Luo

<details>
<summary> 日本語要旨 </summary>

ディフュージョントランスフォーマー（DiTs）において、隠れ空間モデリングが標準とされてきました。しかし、事前学習済みのオートエンコーダを用いた二段階パイプラインは、損失のある再構成を導入し、誤差蓄積を引き起こしながら共同最適化を妨げます。これらの問題に対処するため、オートエンコーダを不要とし、ピクセル空間で直接ディフュージョンプロセスを学習する単一段階、端から端までのモデルであるPixelDiTを提案します。PixelDiTは、グローバルな意味を捉えるパッチレベルのDiTとテクスチャーの細部を洗練するピクセルレベルのDiTによって形作られた完全にトランスフォーマーベースのアーキテクチャを採用しています。これにより、ピクセル空間でのディフュージョンモデルを効率的に学習しつつ、細部を保持することが可能です。PixelDiTはImageNet 256で1.61 FID、ImageNet 512で2.21 FIDを達成し、既存のピクセル生成モデルを大きく上回りました。さらに、PixelDiTをテキストから画像への生成に拡張し、ピクセル空間で$1024^{2}$解像度で事前学習します。これによりGenEvalで0.74、DPG-benchで83.5を達成し、最良の隠れディフュージョンモデルに近づきます。
</details>

<details>
<summary> 英語要旨 </summary>

Latent-space modeling has been the standard for Diffusion Transformers (DiTs). However, it relies on a two-stage pipeline where the pretrained autoencoder introduces lossy reconstruction, leading to error accumulation while hindering joint optimization. To address these issues, we propose PixelDiT, a single-stage, end-to-end model that eliminates the need for the autoencoder and learns the diffusion process directly in the pixel space. PixelDiT adopts a fully transformer-based architecture shaped by a dual-level design: a patch-level DiT that captures global semantics and a pixel-level DiT that refines texture details, enabling efficient training of a pixel-space diffusion model while preserving fine details. PixelDiT achieves 1.61 FID on ImageNet 256 and 2.21 FID on ImageNet 512, surpassing existing pixel generative models by a large margin. We further extend PixelDiT to text-to-image generation and pretrain it at the $1024^{2}$ resolution in pixel space. It achieves 0.74 on GenEval and 83.5 on DPG-bench, approaching the best latent diffusion models.
</details>

---

### Bridge: Basis-Driven Causal Inference Marries VFMs for Domain Generalization
著者: Mingbo Hong, Feng Liu, Caroline Gevaert, George Vosselman, Hao Cheng

<details>
<summary> 日本語要旨 </summary>

検出器は、ソースドメインとターゲットドメインの分布的なギャップにより、性能が低下することが多いです。特に単一ソースドメインでデータが限られている場合、モデルはソースドメインからの共変量（例えば、照明、共起、スタイル）に依存しやすく、これが不適切な相関を引き起こして一般化能力を妨げます。この問題に対処するため、本論文では新しいドメイン一般化のための基盤となるフレームワークである**Bridge**を提案します。これは因果推論をオブジェクト検出に組み込むものです。前方道調整のための低ランク基底を学習することで、**Bridge**は共変量の影響を遮断し、不適切な相関を軽減します。同時に、冗長でタスクに無関係な成分をフィルタリングすることで表現を洗練させます。**Bridge**は、識別的（例えば、DINOv2/3, SAM）および生成的（例えば、Stable Diffusion）ビジョンファウンデーションモデル（VFMs）ともシームレスに統合できます。クロスカメラ、悪天候、リアルからアートへのドメイン一般化オブジェクト検出データセット、多様な気象条件データセット、および我々が新たに強化した実世界UAVベースのリアルタイムドメイン一般化車両（Diverse Weather DroneVehicle）を含む多数のドメイン一般化オブジェクト検出データセットにわたる広範な実験が、提案手法の優位性を示しています。コード、モデル、およびデータは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Detectors often suffer from degraded performance, primarily due to the distributional gap between the source and target domains. This issue is especially evident in single-source domains with limited data, as models tend to rely on confounders (e.g., illumination, co-occurrence, and style) from the source domain, leading to spurious correlations that hinder generalization. To this end, this paper proposes a novel Basis-driven framework for domain generalization, namely **Bridge**, that incorporates causal inference into object detection. By learning the low-rank bases for front-door adjustment, **Bridge** blocks confounders' effects to mitigate spurious correlations, while simultaneously refining representations by filtering redundant and task-irrelevant components.**Bridge** can be seamlessly integrated with both discriminative (e.g., DINOv2/3, SAM) and generative (e.g., Stable Diffusion) Vision Foundation Models (VFMs). Extensive experiments across multiple domain generalization object detection datasets, i.e., Cross-Camera, Adverse Weather, Real-to-Artistic, Diverse Weather Datasets, and Diverse Weather DroneVehicle (our newly augmented real-world UAV-based benchmark), underscore the superiority of our proposed method over previous state-of-the-art approaches. Code, models, and data will be publicly released.
</details>

---

### Token Warping Helps MLLMs Look from Nearby Viewpoints
著者: Phillip Y. Lee, Chanho Park, Mingue Park, Seungwoo Yoo, Juil Koo, Minhyuk Sung

<details>
<summary> 日本語要旨 </summary>

大規模多様な言語モデル（MLLMs）が、近傍の視点からシーンがどのように見えるかを理解するために、ピクセルではなくトークンをねじ曲げることは役立つでしょうか？ MLLMs は単一画像推論において優れた性能を発揮しますが、視点の変化に対しては依然として脆弱です。これは、ピクセルレベルでのねじ曲げが小さな深度誤差に非常に敏感であり、しばしば幾何学的歪みを導入するためです。心像理論に基づき、人間の視点変換の基盤となる部分レベルの構造表現を仮定し、ViTベースのMLLMs内の画像トークンが視点ねじ曲げの効果的な基盤として機能するかどうかを調査します。前方および後方変換戦略の2つのトークンレベル変換手法を比較し、ターゲットビューのグリッド位置にあるトークンを選択し、それらの対応するものをソースビューから取得する後方トークンフェッチングが、視点シフト下でより安定性を保ち、意味的一貫性をより良く維持することを発見しました。私たちが提案した ViewBench ベンチマークにおける実験は、トークンレベルのねじ曲げが MLLMs が近傍視点から信頼性を持って推論することを可能にし、ピクセルねじ曲げアプローチ、空間的推論のために微調整された MLLMs、および生成的なねじ曲げ方法を含むすべてのベースラインを一貫して上回ることを示しました。
</details>

<details>
<summary> 英語要旨 </summary>

Can warping tokens, rather than pixels, help multimodal large language models (MLLMs) understand how a scene appears from nearby viewpoints? While MLLMs perform well on a single image reasoning, they remain fragile to viewpoint changes because pixel-level warping is highly sensitive to small depth errors and often introduces geometric distortions. Drawing on theories of mental imagery that posit part-level structural representations as the basis for human perspective transformation, we examine whether image tokens in ViT-based MLLMs serve as an effective substrate for viewpoint warping. We compare two token-level transformation strategies, forward and backward warping, and find that backward token fetching, which selects tokens at target-view grid locations and retrieves their counterparts from the source view, achieves greater stability and better preserves semantic coherence under viewpoint shifts. Experiments on our proposed ViewBench benchmark demonstrate that token-level warping enables MLLMs to reason reliably from nearby viewpoints, while consistently outperforming all baselines, including pixel-warping approaches, MLLMs fine-tuned for spatial reasoning, and a generative warping method.
</details>

---

### Tokenization Allows Multimodal Large Language Models to Understand, Generate and Edit Architectural Floor Plans
著者: Sizhong Qin, Ramon Weber, Xinzheng Lu

<details>
<summary> 日本語要旨 </summary>

建築のフロアプランデザインは、幾何学、意味論、空間階層に関する共同的な推論を要求し、現在のAIシステムにとって大きな課題であり続けています。最近の拡散モデルや言語モデルは視覚的な忠実度を向上させましたが、まだ一貫した空間推論と制御可能な生成に苦労しています。私たちはHouseMindというマルチモーダル大言語モデルを紹介します。これはフロアプランの理解、生成、編集を一つの枠組みで統合します。部屋インスタンストークンという離散的なものを導入し、レイアウトと象徴的推論を橋渡しする統一された語彙を構築します。マルチモーダル整合性とインストラクションチューニングにより、モデルはテキスト指示から一貫した制御可能なレイアウトを合成できます。実験結果は、このフレームワークが幾何学的妥当性と制御可能性において優れたパフォーマンスを達成しつつも効率的でローカルデプロイメントが可能であることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Architectural floor plan design demands joint reasoning over geometry, semantics, and spatial hierarchy, which remains a major challenge for current AI systems. Although recent diffusion and language models improve visual fidelity, they still struggle with coherent spatial reasoning and controllable generation. We present HouseMind, a multimodal large language model that unifies floor plan understanding, generation, and editing in one framework. We introduce discrete room-instance tokens to construct a unified vocabulary that bridges layouts and symbolic reasoning. With multimodal alignment and instruction tuning, the model synthesizes coherent, controllable layouts from text instructions. Experiments show how the framework achieves superior geometric validity and controllability while remaining efficient and locally deployable.
</details>

---

### Adaptive 3D Perception Under Sparse Sampling Via Reinforcement Learning
著者: Shenghai Yuan, Wei Yihan, Jason Yee, Zhuoran Qiao, boyang lou, Enwen Hu

<details>
<summary> 日本語要旨 </summary>

長距離LiDARを用いた小型航空目標（SATs）の検出は、点密度が動きによって劇的に変化するため困難です。高速飛行では極端に希薄なリターンを生じ、一方でホバリングや遅い動きは密集した局所クラスターを形成し、標準的な3D検出器およびトラッカーの固定ビューロールと静的しきい値の仮定を破ります。我々は、LiDARセンシングと追跡の間にループを閉じる強化学習（RL）駆動型適応認識フレームワークであるA3PRLを導入します。A3PRLは、時間的拡散署名と速度変化の手がかりに基づく希薄性に配慮したプロポーザルステージを構築し、5Dポリシーを展開して、空間的および時間的な希薄性、前景受容、トラッキングの連続性を要約する純粋にラベルフリーの統計量に基づいてビューロール解像度、検出感度、および関連付けゲートを同時に調整します。このポリシーは、幾何学的精度、時間的安定性、規則化された受容のバランスを取る報酬を形成するために、特権付き監督から地上真値軌道を用いてトレーニングされますが、テスト時には完全にラベルフリーで動作します。公開のMMAUDベンチマークでは、V1でのトレーニングと未見のV2/V3ドメインでの評価を行い、A3PRLは非RL対応品に比べて3Dローカリゼーションエラーを約19％削減し、昼夜問わずLiDAR単独およびマルチモーダルベースラインを一貫して上回ります。さらに、同じポリシーが自社のLiDAR-RTKセットアップと異なるスキャンパターンを持つ公開マルチLiDAR SATデータセットに転移することを示し、変動する希薄性下で正確な軌道と安定したトラックを維持しつつ、10 HzのLiDAR予算内でフレームあたり2 ms未満のオーバーヘッドしか追加しません。
</details>

<details>
<summary> 英語要旨 </summary>

Detecting small aerial targets (SATs) from long-range LiDAR is challenging because point density changes dramatically with motion: fast flights produce ultra-sparse returns, while hovering or slow motion yields dense local clusters, breaking fixed-voxel and static-threshold assumptions in standard 3D detectors and trackers. We introduce A3PRL, an RL-driven adaptive perception framework that closes the loop between LiDAR sensing and tracking. A3PRL builds on a sparsity-aware proposal stage with Temporal Dispersion Signatures and velocity-change cues, and deploys a lightweight 5D policy that jointly adjusts voxel resolution, detection sensitivity, and association gating based on purely label-free statistics summarizing spatio–temporal sparsity, foreground acceptance, and tracking continuity. The policy is trained with privileged supervision from ground-truth trajectories to shape a reward that balances geometric accuracy, temporal stability, and regularized acceptance, but runs fully label-free at test time. On the public MMAUD benchmark, training on V1 and evaluating on unseen V2/V3 domains, A3PRL reduces 3D localization error by about 19\% compared to its non-RL counterpart and consistently outperforms LiDAR-only and multimodal baselines under both day and night conditions. We further show that the same policy transfers to an in-house LiDAR–RTK setup and a public multi-LiDAR SAT dataset with heterogeneous scan patterns, where it maintains accurate trajectories and stable tracks under varying sparsity, while adding less than 2 ms per frame on a 10 Hz LiDAR budget.
</details>

---

### Inference-time Physics Alignment of Video Generative Models with Latent World Models
著者: Jianhao Yuan, Zhang Xiaofeng, Felix Friedrich, Nicolas Beltran-Velez, Melissa Hall, Reyhane Askari, Xiaochuang Han, Nicolas Ballas, Michal Drozdzal, Adriana Romero-Soriano

<details>
<summary> 日本語要旨 </summary>

最先端のビデオ生成モデルは、魅力的な視覚コンテンツを生み出す一方で、しばしば基本的な物理原理に違反し、その有用性が制限されています。この欠陥の一部は事前学習時の物理理解不足に起因すると考えられますが、私たちは物理的妥当性の不足も最適でない推論戦略から生じることを発見しました。そこで、WMRewardを導入し、ビデオ生成における物理的妥当性の向上を推論時の整合問題として扱います。具体的には、強力な物理事前知識を持つ潜在世界モデル（ここではVJEPA-2）を報酬として利用し、複数の候補となるノイズ除去経路を探索・制御することで、より良い生成パフォーマンスのためにテスト時の計算能力を拡張します。実験的には、画像条件付き、複数フレーム条件付き、およびテキスト条件付きの生成設定において物理的妥当性が大幅に向上し、人間評価研究で検証されました。特筆すべきは、難易度の高いPhysicsIQベンチマークで62.00%という最終スコアを達成し、これまでの最先端技術を6.78%上回ったことです。私たちの研究は、特定の実装やパラメータ化に限らず、潜在世界モデルを用いてビデオ生成の物理的妥当性を向上させることが可能であることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

State-of-the-art video generative models produce promising visual content yet often violate basic physics principles, limiting their utility. While some attribute this deficiency to insufficient physics understanding from pre-training, we find that the shortfall in physics plausibility also stems from suboptimal inference strategies. We therefore introduce WMReward and treat improving physics plausibility of video generation as an inference-time alignment problem. In particular, we leverage the strong physics prior of a latent world model (here, VJEPA-2) as a reward to search and steer multiple candidate denoising trajectories, enabling scaling test-time compute for better generation performance. Empirically, our approach substantially improves physics plausibility across image-conditioned, multiframe-conditioned, and text-conditioned generation settings, with validation from human preference study. Notably, on the challenging PhysicsIQ benchmark we achieve 62.00% final score, outperforming previous state of the art by 6.78%. Our work demonstrates the viability of using latent world models to improve physical plausibility of video generation, beyond this specific instantiation or parameterization.
</details>

---

### Time-Aware One Step Diffusion Network for Real-World Image Super-Resolution
著者: Tianyi Zhang, Zheng-Peng Duan, Chun-Le Guo, Peng-Tao Jiang, Bo Li, Ming-Ming Cheng, Chongyi Li

<details>
<summary> 日本語要旨 </summary>

現実世界の画像超解像（Real-ISR）において、拡散ベースの方法が印象的な性能を示しています。効率的なReal-ISRを達成するために、多くの研究では事前学習済みの安定した拡散（SD）モデルを一ステップSR用に固定ステップタイムで変換するために変分スコア蒸留（VSD）を使用しています。しかし、SDは異なるステップタイムで異なる生成的事前知識を行うため、固定ステップタイムではこれらの方法がSD内の生成的事前知識を完全に活用することが難しく、性能が最適でない結果となります。この問題に対処するため、私たちはタイムアウェア一ステップ拡散ネットワークを提案します（TADSR）。まず、同じ画像を異なるステップタイムに基づいて異なる潜在特徴に投影するタイムアウェアVAEエンコーダーを導入します。ステップタイムと潜在特徴の共同動的変化により、学習モデルは事前学習済みSDの入力パターン分布により良く一致し、SDの生成能力をより効果的に活用できるようになります。さらに、異なるステップタイムでSDの生成事前知識をより適切に活性化するために、学習モデルと教師モデルのステップタイムを橋渡しするタイムアウェアVSD損失を提案します。これにより、ステップタイムに条件付けられた一貫した生成事前知識ガイダンスが得られます。また、異なるステップタイムでSDの生成事前知識を利用することで、私たちの方法は自然に忠実度とリアリズムのトレードオフを制御可能にし、ステップタイムを変更することで達成できます。実験結果は、私たちの方法が単一ステップで最先端の性能および制御可能なSR結果を両立させることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Diffusion-based real-world image super-resolution (Real-ISR) methods have demonstrated impressive performance. To achieve efficient Real-ISR, many works employ Variational Score Distillation (VSD) to distill pre-trained stable-diffusion (SD) model for one-step SR with a fixed timestep. However, since SD will perform different generative priors at different timesteps, a fixed timestep is difficult for these methods to fully leverage the generative priors in SD, leading to suboptimal performance. To address this, we propose a Time-Aware one-step Diffusion Network for Real-ISR (TADSR). We first introduce a Time-Aware VAE Encoder, which projects the same image into different latent features based on timesteps. Through joint dynamic variation of timesteps and latent features, the student model can better align with the input pattern distribution of the pre-trained SD, thereby enabling more effective utilization of SD's generative capabilities. To better activate the generative prior of SD at different timesteps, we propose a Time-Aware VSD loss that bridges the timesteps of the student model and those of the teacher model, thereby producing more consistent generative prior guidance conditioned on timesteps. Additionally, though utilizing the generative prior in SD at different timesteps, our method can naturally achieve controllable trade-offs between fidelity and realism by changing the timestep. Experimental results demonstrate that our method achieves both state-of-the-art performance and controllable SR results with only a single step.
</details>

---

### SaPaVe: Towards Active Perception and Manipulation in Vision-Language Action Models for Robot
著者: MENGZHEN LIU, Enshen Zhou, Cheng Chi, Yi Han, Shanyu Rong, Liming Chen, Pengwei Wang, Zhongyuan Wang, Shanghang Zhang

<details>
<summary> 日本語要旨 </summary>

活動的な知覚と操作は、複雑なシーンと相互作用するためにエンボディロボットにとって重要です。既存の方法では、セマンティック駆動の活発な知覚を堅牢で視点不変の実行と統一することが難しいです。この課題に対処するため、我々はSaPaVeというエンドツーエンドフレームワークを提案します。これはデータ効率的な方法でこれらの能力を共同学習します。我々のアプローチの中心にあるのは、カメラと操作行動を分離することです（シェアード・アクションスペースではなく）、そしてボトムアップ戦略で学習します：まず、我々が提案した大規模データセット上でセマンティックカメラ制御を訓練し、その後ハイブリッドデータを用いて両方の行動タイプを共同最適化します。この学習を支援するために、我々はセマンティックカメラ移動学習のための200k画像-言語-カメラ動作ペアからなるActiveViewPose-200Kを導入し、3D幾何学に対応したモジュールを追加してダイナミック視点下での実行の堅牢性を向上させます。また、活発な操作を評価するためのギャップを埋める最初のベンチマークとしてActiveManip-Benchを提示します。シミュレーションおよび実世界の設定での広範な実験により、SaPaVeがGR00Tや$\pi_0$などの最近のVLAモデルを上回り、実際のタスクで31.25%高い成功率を達成することが示されました。我々の結果は、分離されたが調整された戦略で訓練された知覚と実行の密接な統合が効率的かつ汎用性のある活発な操作を可能にすることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Active perception and manipulation are crucial for embodied robots to interact with complex scenes. Existing methods struggle to unify semantic-driven perception actively with robust, viewpoint-invariant execution accordingly. To this end, we propose SaPaVe, an end-to-end framework that jointly learns these capabilities in a data-efficient manner. Central to our approach is a decoupling of camera and manipulation actions, contrary to shared-action-space, and learning in a bottom-up strategy: we first train semantic camera control on our proposed large-scale dataset, then jointly optimize both action types via hybrid data. To support this learning, we introduce ActiveViewPose-200K, comprising 200k image-language-camera movement pairs for semantic camera movement learning, and a 3D geometry-aware module that improves execution robustness under dynamic viewpoints. We further present ActiveManip-Bench, the first benchmark filling the gap to evaluate active manipulation. Extensive experiments in both simulation and real-world settings show that SaPaVe outperforms recent VLA models such as GR00T and $\pi_0$, achieving up to 31.25\% higher success rates in real-world tasks. Our results show that tightly coupled perception and execution, when trained with decoupled yet coordinated strategies, enable efficient and generalizable active manipulation.
</details>

---

### Multi-Scale Gaussian-Language Map for Embodied Navigation and Reasoning
著者: Sixian Zhang, Yiyao Wang, Xinhang Song, Keming Zhang, Zijian Xu, Shuqiang Jiang

<details>
<summary> 日本語要旨 </summary>

環境の幾何学的および意味構造を理解することは、具現化されたエージェントにとって不可欠です。既存のセマンティックマッピング手法は、明示的な幾何学と多スケールセマンティクスの間でトレードオフを行い、大規模モデル用のネイティブインターフェースが欠如しており、結果として意味合わせのために特徴投影の追加的なトレーニングを必要とします。この問題に対処するため、我々は多スケールガウシアン-言語マップ（GLMap）を提案します。これには三つの重要な設計が含まれます：(1) 明示的幾何学、(2) インスタンスレベルおよび地域レベルの概念をカバーする多スケールセマンティクス、そして(3) それぞれのセマンティック単位が自然言語記述と3Dガウシアン表現を共に保持するデュアルモダリティインターフェース。3Dガウシアンは、Gaussian splattingを用いたタスク関連画像のコンパクトな保存と高速レンダリングを可能にします。効率的な増分構築を可能にするために、我々はさらに密度点群から勾配ベース最適化を用いずにガウシアンパラメータを解析的に導出するGaussian Estimatorを提案します。ObjectNav、InstNav、およびSQAタスクの実験結果は、GLMapが標的ローカリゼーションと文脈的推論を効果的に強化する一方で、ゼロショット方式で大規模モデルベースの方法と互換性があることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Understanding the geometric and semantic structure of environments is essential for embodied agents. Existing semantic mapping methods trade off between explicit geometry and multi-scale semantics,and lack a native interface for large models, thus requiring additional training of feature projection for semantic alignment. To this end, we propose the multi-scale Gaussian-Language Map (GLMap), which introduces three key designs: (1) explicit geometry, (2) multi-scale semantics covering both instance and region level concepts, and (3) a dual-modality interface where each semantic unit jointly stores a natural language description and a 3D Gaussian representation. The 3D Gaussians enable compact storage and fast rendering of task-relevant images via Gaussian splatting. To enable efficient incremental construction, we further propose a Gaussian Estimator that analytically derives Gaussian parameters from dense point clouds without gradient-based optimization. Experiments on ObjectNav, InstNav, and SQA tasks show that GLMap effectively enhances target localization and contextual reasoning, while remaining compatible with large-model-based methods in a zero-shot manner.
</details>

---

### VOLD: Reasoning Transfer from LLMs to Vision-Language Models Via On-Policy Distillation
著者: Walid Bousselham, Hilde Kuehne, Cordelia Schmid

<details>
<summary> 日本語要旨 </summary>

ビジョン言語モデル（VLM）の複雑な推論タスクにおけるトレーニングは、高品質な画像テキスト推論データの希少性などから依然として困難です。一方で、テキストベースの推論リソースは豊富かつスケーラブルですが、それらをVLM推論に活用する方法については未解決の問題となっています。この問題に対処するため、私たちはテキスト専用の教師モデルからVLM学習者モデルへ推論能力を移行させるフレームワークであるVOLDを提案します。この目的のために、VOLDはGroup Relative Policy Optimization（GRPO）を用いた強化学習とオンポリシー転移学習を組み合わせており、これによって教師モデルが学習者の推論トレースをガイドし、GRPO単体使用時と比べて顕著な向上をもたらします。さらに、オンライントレーニングフェーズで効果的な移行のためには冷スタートアライメントが不可欠であり、教師と学習者間の分布的アライメントが十分でない場合、オンポリシー転移学習は有意義なガイダンスを提供できないことを示します。私たちはVOLDをMMMU-Pro、MathVision、MathVista、LogicVistaなど多様なベンチマークにわたって評価し、VOLDが基準モデルを大幅に上回り、最先端技術を一定の余裕で改善することを示します。また、冷スタートアライメントをSFTを通じて行うことがテキスト専用教師モデルにおけるオンポリシー転移学習の重要性を示す分解実験も提示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Training vision-language models (VLMs) for complex reasoning remains a challenging task, i.a. due to the scarcity of high-quality image-text reasoning data. Conversely, text-based reasoning resources are abundant and scalable, but it is still an open question how to leveraging them for VLM reasoning. To address this problem, we propose VOLD, a framework to transfer reasoning capabilities from text-only teacher models to VLM student models. To this end, VOLD combines reinforcement learning via Group Relative Policy Optimization (GRPO) with on-policy distillation, which allows the student reasoning traces to be guided by the teacher model, resulting in a significant gain over using GRPO alone. We further show that a cold-start alignment is essential for an effective transfer during the online training phase in this scenario and that without sufficient distributional alignment between teacher and student, on-policy distillation fails to provide meaningful guidance. We evaluate VOLD across diverse benchmarks including MMMU-Pro, MathVision, MathVista, and LogicVista, showing that VOLD outperforms the baseline model significantly and improves over the state of the art by a margin. Our ablation shows the importance of a cold-start alignment via SFT for on-policy distillation with a text-only teacher
</details>

---

### Generative Modeling of Weights: Generalization or Memorization?
著者: Boya Zeng, Yida Yin, Zhiqiu Xu, Zhuang Liu

<details>
<summary> 日本語要旨 </summary>

生成モデルは、画像や動画の生成における成功を受けて、効果的なニューラルネットワーク重みの合成について最近探求されています。これらのアプローチは、トレーニングデータとしてトレーニング済みのニューラルネットワークチェックポイントを取り入れ、推論時に高性能なニューラルネットワーク重みを生成することを目指しています。本研究では、この新興分野で代表的かつよく知られた4つの方法をその新規モデル重み（トレーニング時に見たチェックポイントと異なる重み）生成能力について検証しました。以前の研究で主張されていたこととは対照的に、これらの方法が合成する重みは大部分が記憶によるものであることを発見しました：彼らはトレーニングチェックポイントの複製または最善でも単純な補間を生成します。現在の方法は、重みにノイズを加えたり、単純な重みアンサンブルを取ったりするような簡単な基準値を上回ることができません。これによって異なりかつ同時に高性能なモデルを得ることはできません。さらなる結果から、記憶の原因は限定されたデータ、過パラメトリックなモデル、および重みデータに特有の構造的事前知識の未活用である可能性が示唆されています。これらの発見は、新しい領域における生成モデルの設計と評価をより慎重に行う必要性を浮き彫りにしています。
</details>

<details>
<summary> 英語要旨 </summary>

Generative models, with their success in image and video generation, have recently been explored for synthesizing effective neural network weights. These approaches take trained neural network checkpoints as training data, and aim to generate high-performing neural network weights during inference. In this work, we examine four representative, well-known methods in this emerging area on their ability to generate novel model weights, i.e., weights that are different from the checkpoints seen during training. Contrary to claims in prior work, we find that these methods synthesize weights largely by memorization: they produce either replicas, or at best simple interpolations, of the training checkpoints. Current methods fail to outperform simple baselines, such as adding noise to the weights or taking a simple weight ensemble, in obtaining different and simultaneously high-performing models. Our further results suggest that the memorization potentially resulted from limited data, overparameterized models, and the underuse of structural priors specific to weight data. Our findings highlight the need for more careful design and evaluation of generative models in new domains.
</details>

---

### Vision-Language Attribute Disentanglement and Reinforcement for Lifelong Person Re-Identification
著者: Kunlun Xu, Haotong Cheng, Jiangmeng Li, Xu Zou, Jiahuan Zhou

<details>
<summary> 日本語要旨 </summary>

ライフロング人物再識別（LReID）は、異なるドメインから学習し、統一された人物検索モデルを得ることを目指しています。既存のLReID手法は通常、ゼロから学習するか、視覚分類で事前にトレーニングされたモデルに焦点を当てており、ビジョン・ランゲージ・モデル（VLM）は多様なタスクで汎用的な知識を示しています。既存の方法は直接VLMに適応可能ですが、それらはグローバル認識学習しか考慮せず、微細な属性知識が十分に活用されていないため、限定的な取得能力と反復防止能力を持っています。この問題に対処するため、私たちはVLM駆動のLReIDアプローチであるビジョン・ランゲージ属性分離と強化（VLADR）を導入します。私たちの主要な考え方は、普遍的に共有される人間の属性を明示的にモデル化することで、ドメイン間知識転移を改善し、歴史的知識を活用して新たな知識学習を強化し、忘却を軽減することです。具体的には、VLADRには多様で局所的なテキスト属性を画像から探索するマルチグレイン・テキスト属性分離メカニズムが含まれています。次に、異ドメイン間モーダル属性強化スキームを開発しました。これはクロスモーダル属性整列を導入して視覚的属性抽出をガイドし、異ドメイン属性整列を採用して微細な知識転送を達成します。実験結果は、私たちのVLADRが反復防止能力で1.9%〜2.2%、一般化能力で2.1%〜2.5%にわたって最先端手法を上回ることを示しています。私たちのコードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Lifelong person re-identification (LReID) aims to learn from varying domains to obtain a unified person retrieval model. Existing LReID approaches typically focus on learning from scratch or a visual classification-pretrained model, while the Vision-Language Model (VLM) has shown generalizable knowledge in a variety of tasks. Although existing methods can be directly adapted to the VLM, since they only consider global-aware learning, the fine-grained attribute knowledge is underleveraged, leading to limited acquisition and anti-forgetting capacity. To address this problem, we introduce a novel VLM-driven LReID approach named Vision-Language Attribute Disentanglement and Reinforcement (VLADR). Our key idea is to explicitly model the universally shared human attributes to improve inter-domain knowledge transfer, thereby effectively utilizing historical knowledge to reinforce new knowledge learning and alleviate forgetting. Specifically, VLADR includes a Multi-grain Text Attribute Disentanglement mechanism that mines the global and diverse local text attributes of an image. Then, an Inter-domain Cross-modal Attribute Reinforcement scheme is developed, which introduces cross-modal attribute alignment to guide visual attribute extraction and adopts inter-domain attribute alignment to achieve fine-grained knowledge transfer. Experimental results demonstrate that our VLADR outperforms the state-of-the-art methods by 1.9%-2.2% and 2.1%-2.5% on anti-forgetting and generalization capacity. Our code will be released.
</details>

---

### Motion-Aware Animatable Gaussian Avatars Deblurring
著者: Muyao Niu, Yifan Zhan, Qingtian Zhu, Zhuoxiao Li, Wei Wang, Zhihang Zhong, Xiao Sun, Yinqiang Zheng

<details>
<summary> 日本語要旨 </summary>

複数視点のビデオから3Dヒューマンアバターを作成することは、コンピュータビジョンにおいて重要でありながらも困難な課題です。しかし、既存の手法は高品質で鮮明な画像を入力として必要とし、これらは人間の動きの速度や強度による変化があるため、現実世界ではしばしば取得が困難です。本論文では、ぼやけたビデオから鮮明な3Dヒューマンガウスシェイプアバターを直接再構成する新しい方法を紹介します。提案された手法は、人間の動きによって引き起こされるぼやけ形成の3D認識可能な物理モデルと、運動誘発ぼやけの曖昧さを解決するために設計された3D人間動作モデルを組み合わせています。このフレームワークは、粗い初期化からアバター表現と運動パラメータの共同最適化を可能にします。シンセティックなデータセットおよび360度同期ハイブリッド露出カメラシステムで撮影された実世界のデータセットを用いて包括的なベンチマークが確立されました。広範囲にわたる評価は、多様な条件下でモデルの効果と堅牢性を示しています。
</details>

<details>
<summary> 英語要旨 </summary>

The creation of 3D human avatars from multi-view videos is a significant yet challenging task in computer vision. However, existing techniques rely on high-quality, sharp images as input, which are often impractical to obtain in real-world scenarios due to variations in human motion speed and intensity. This paper introduces a novel method for directly reconstructing sharp 3D human Gaussian avatars from blurry videos. The proposed approach incorporates a 3D-aware, physics-based model of blur formation caused by human motion, together with a 3D human motion model designed to resolve ambiguities in motion-induced blur. This framework enables the joint optimization of the avatar representation and motion parameters from a coarse initialization. Comprehensive benchmarks are established using both a synthetic dataset and a real-world dataset captured with a 360-degree synchronous hybrid-exposure camera system. Extensive evaluations demonstrate the effectiveness and robustness of the model across diverse conditions.
</details>

---

### WorldGen: From Text to Traversable and Interactive 3D Worlds
著者: Dilin Wang, Hyunyoung Jung, Tom Monnier, Kihyuk Sohn, Chuhang Zou, Xiaoyu Xiang, Yu-Ying Yeh, Di Liu, Zixuan Huang, Thu Nguyen-Phuoc, Yuchen Fan, Sergiu Oprea, Ziyan Wang, Roman Shapovalov, Nikolaos Sarafianos, Thibault Groueix, Antoine Toisoul, Prithviraj Dhar, Xiao Chu, Minghao Chen, Geon Yeong Park, Rakesh Ranjan, Andrea Vedaldi

<details>
<summary> 日本語要旨 </summary>

私たちは、単一のテキストプロンプトから大規模で完全に形成された、ナビゲーション可能な3Dワールドを生成するWorldGenという方法を紹介します。既存の3Dシーン生成手法は、通常、シーンの多様性、完全性、正確性を異なる方法でトレードオフしています。私たちはこの限界を押し広げ、個々の高品質3Dメッシュに明示的に分解された大規模なシーンを生成することで、標準ゲームエンジンと互換性があります。まず、言語駆動のプロシージャルジェネレータを使用して、シーンの基本的な体積やナビゲーション可能な領域を配置します。次に、画像ジェネレータがシーンのテーマ、スタイル、詳細を確立します。その後、計画されたシーンの高品質で構成的な3D再構築を取得します。この手順では、まず画像から3Dモデルによって全体的な再構築を行い、すべてのシーンオブジェクトの形状と位置を暗黙的に決定し、コンテキストやナビゲーション性を考慮します。その後、再構築は個々のエンティティに分解され、画像ジェネレータからの指導に基づいて追加の詳細を合成しながら高解像度で再生成されます。私たちは重要な設計選択肢を検証し、既存のシーンジェネレータと比較して質的に評価し、多くの共通の課題に対処する私たちのデザインであることを示します。
</details>

<details>
<summary> 英語要旨 </summary>

We introduce WorldGen, a method for generating large, fully formed, navigable 3D worlds from a single text prompt. Existing approaches to 3D scene generation often trade off scene diversity, completeness, and correctness in different ways. We push this envelope by producing large scenes explicitly decomposed into individual, high-quality 3D meshes, making them compatible with standard game engines. Our approach first uses a language-driven procedural generator to lay out the scene's basic volumes and navigable regions. An image generator then establishes the scene's theme, style, and details. Next, we obtain a high-quality, compositional 3D reconstruction of the planned scene. This step first uses an image-to-3D model to perform a holistic reconstruction that implicitly determines the shape and location of all scene objects, accounting for context and navigability. The reconstruction is then decomposed into individual entities, which are regenerated at higher resolution, synthesizing additional details with guidance from the image generator. We ablate key design choices and compare qualitatively against existing scene generators, showing that our design addresses many of their common challenges.
</details>

---

### Describe Anything Anywhere At Any Moment
著者: Nicolas Gorlo, Lukas Schmid, Luca Carlone

<details>
<summary> 日本語要旨 </summary>

コンピュータビジョンおよびロボティクスの応用は、拡張現実から大規模環境におけるロボット自律まで多岐にわたり、正確な言語アンカリングを可能にする幾何学的構造とセマンティックディテールの両方を捉えるスパースタイムメモリフレームワークが必要です。既存の方法は、3Dでアンカリングするために豊富なオープンバケット説明を生成することがリアルタイムパフォーマンスの犠牲になるというトレードオフに直面しています。これらの課題に対処するため、我々は大規模かつリアルタイムで4Dシーン理解を可能にする新しいスパースタイムメモリフレームワーク「Describe Anything, Anywhere, at Any Moment（DAAAM）」を提案します。DAAAMは、ローカライズされたキャプショニングモデルであるDescribe Anything Model（DAM）から詳細なセマンティック説明を推論するための新しい最適化ベースフロントエンドを導入します。これにより、オンライン処理での推論速度が桁違いに向上します。このセマンティック理解を活用して、効果的なグローバルスペーシャルおよびタイムリーに一貫したメモリ表現として機能する階層的4Dシーングラフ（SG）を構築します。DAAAMは、詳細で幾何学的にアンカリングされた説明を持つ4D SGを構築しながらリアルタイムパフォーマンスを維持します。我々は、DAAAMの4D SGが推論および推論に対するツール呼び出しエージェントと良好にインターフェースすることを示しています。我々は、NaVQAベンチマークでのスパースタイム質問応答（SQA）という複雑なタスクにおいてDAAAMを徹底的に評価し、その連続タスクアンカリングへの汎用性をSG3Dベンチマークで示します。さらに、大規模かつ長期間の評価のために拡張されたOC-NaVQAベンチマークを編纂しました。DAAAMは両方のタスクで最先端の結果を達成し、それぞれ53.6％、21.9％、21.6％、27.8％というOC-NaVQA質問精度、位置誤差、時間誤差、SG3Dタスクアンカリング精度の改善を最も競争力のあるベースラインに対して達成しました。我々はデータとコードをオープンソースで公開します。
</details>

<details>
<summary> 英語要旨 </summary>

Computer vision and robotics applications ranging from agumented reality to robot autonomy in large-scale environments require spatio-temporal memory frameworks that capture both geometric structure for accurate language-grounding as well as semantic detail. Existing methods face a tradeoff, where producing rich open-vocabulary descriptions comes at the expense of real-time performance when these descriptions have to be grounded in 3D. To address these challenges, we propose Describe Anything, Anywhere, at Any Moment (DAAAM), a novel spatio-temporal memory framework for large-scale and real-time 4D scene understanding. DAAAM introduces a novel optimization-based frontend to infer detailed semantic descriptions from localized captioning models, such as the Describe Anything Model (DAM), leveraging batch processing to speed up inference by an order of magnitude for online processing. It leverages such semantic understanding to build a hierarchical 4D scene graph (SG), which acts as an effective globally spatially and temporally consistent memory representation. DAAAM constructs 4D SGs with detailed, geometrically grounded descriptions while maintaining real-time performance. We show that DAAAM's 4D SG interfaces well with a tool-calling agent for inference and reasoning. We thoroughly evaluate DAAAM in the complex task of spatio-temporal question answering (SQA) on the NaVQA benchmark and show its generalization capabilities for sequential task grounding on the SG3D benchmark. We further curate an extended OC-NaVQA benchmark for large-scale and long-time evaluations. DAAAM achieves state-of-the-art results in both tasks, improving OC-NaVQA question accuracy by 53.6\%, position errors by 21.9\%, temporal errors by 21.6\%, and SG3D task grounding accuracy by 27.8\% over the most competitive baselines, respectively. We release our data and code open-source.
</details>

---

### Efficient Frame Selection for Long Video Understanding Via Reinforcement Learning
著者: Yaxuan Qin, Hefei Li, Wenqi Mu, Yancheng He

<details>
<summary> 日本語要旨 </summary>

最近のマルチモーダル大規模言語モデル（MLLMs）の進歩により、ビデオ理解分野で顕著な進展が見られています。しかし、限られたコンテキストウィンドウと計算上のオーバーヘッドのため、多くのMLLMsは均一フレームサンプリングを採用しており、これによって重要な視覚情報が見落とされるリスクが高まり、特に長いビデオではパフォーマンスが制約されます。この問題に対処するため、我々はキー・フレームを識別し、それらを訓練するための軽量なフレーム選択方法を提案します。これは二段階戦略によって行われます。事前学習段階では、フレームセレクターが個々のビデオフレームとクエリ間の関連性をモデル化することを学びます。強化学習（RL）段階では、選択品質を組み合わせとフレームレベルで評価する階層的報酬を用いています。フレームの組み合わせに対する確率的探索を通じて、セレクターは単にクエリ関連性を最大化するだけでなく、タスクパフォーマンスを向上させるフレームを識別し保持することを学びます。これは誤導的です。選択されたフレームは、ビデオ理解および推論の下流MLLMsに入力として使用されます。実験結果は、提案されたセレクターが中長期間のビデオを含むさまざまなベンチマークで多様な下流MLLMsのパフォーマンスを向上させることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advances in Multimodal Large Language Models (MLLMs) have led to significant progress in video understanding. Due to limited context windows and computational overhead, most MLLMs adopt uniform frame sampling. This approach is at high risk of missing critical visual information and constrains performance especially for long videos. To address this problem, we propose a lightweight frame selection method to identify keyframes and train it via a two-stage strategy. In the pre-training stage, the frame selector learns to model relevance between individual video frames and queries. In the reinforcement learning (RL) stage, we employ a hierarchical reward that evaluates selection quality at combination and frame levels. Through stochastic exploration of frame combinations, the selector learns to identify and retain frames that improve task performance rather than merely maximizing query relevance, which can be misleading. The selected frames serve as input to downstream MLLMs for video understanding and reasoning. Experimental results demonstrate the proposed selector improves performance of diverse downstream MLLMs across benchmarks spanning medium to long videos.
</details>

---

### UVU: Improving Multimodal Understanding Via Vision-Language Unified Autoregressive Paradigm
著者: Zhehan Kan, Xinghua Jiang, Yanlin Liu, Xiaochen Yang, ZHIXIANG WEI, Shifeng Liu, Yubo Zhu, Qingmin Liao, Wenming Yang, Xin Li, Yinsong Liu, Deqiang Jiang, Xing Sun

<details>
<summary> 日本語要旨 </summary>

多様なモダリティの大規模言語モデル（MLLMs）は、卓越した進歩を遂げているものの、その細部にわたる視覚理解能力は、純粋なテキスト監督に依存することで制限されています。統合的な自己回帰多様モーダルモデルは、視覚監督を導入して理解と生成能力を統一しようとしますが、視覚特徴の離散化効果や画像テキスト損失勾配の直交性により、多様モーダル理解が阻害されます。本論文では、ピクセルレベルの画像パッチとテキストトークンが原始的な高次元空間で固有の入力対称性を持って共存していることに注目します。この洞察に基づき、私たちはベクター量子化を排除する新しいビジョン言語統一自己回帰フレームワークであるUVUを提案します。これは視覚入力の損失なしの表現のために連続的な視覚エンコーディングを採用し、大規模な反復階層クラスタリングアルゴリズムを提案してピクセルレベルの視覚辞書を構築し、統一監督のために語彙を拡張し、テキストトークンと共にピクセルレベルの画像トークンの自己回帰生成を可能にします。UVUはピクセルレベルの視覚知覚と意味レベルの視覚理解を効果的に融合し、視覚生成能力を内包し、初めて視覚監督が理解強化における促進役割を解放します。多様なタスクにわたる広範囲の実験は、UVUの監督学習パラダイム下でMLLMsが優れた多様モーダル理解性能を達成することが可能であることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Despite remarkable advancements in multimodal large language models (MLLMs), their fine-grained visual understanding is constrained by reliance on pure textual supervision. To unify understanding and generation capabilities, unified autoregressive multimodal models introduce visual supervision; however, they impair multimodal understanding due to the effects of visual feature discretization and orthogonality between image-text loss gradients. In this paper, we observe that pixel-level image patches and textual tokens coexist in raw high-dimensional spaces with inherent input symmetry. Motivated by this insight, we propose UVU, a novel vision-language unified autoregressive framework that eschews vector quantization. It uniquely employs continuous visual encoding for lossless representation of visual inputs and proposes a large-scale iterative hierarchical clustering algorithm to construct a pixel-level visual codebook, thereby extending the vocabulary for unified supervision and enabling autoregressive generation of pixel-level image tokens alongside textual tokens. UVU effectively synergizes pixel-level visual perception with semantic-level visual understanding, internalizing visual generation capabilities and, for the first time, unlocking the facilitative role of visual supervision in enhancing understanding. Extensive experiments across multiple tasks demonstrate that MLLMs are capable of achieving superior multimodal understanding performance under the supervised learning paradigm of UVU.
</details>

---

### E-RayZer: Self-supervised 3D Reconstruction As Spatial Visual Pre-training
著者: Qitao Zhao, Hao Tan, Qianqian Wang, Sai Bi, Kai Zhang, Kalyan Sunkavalli, Shubham Tulsiani, Hanwen Jiang

<details>
<summary> 日本語要旨 </summary>

自己監督学習による事前学習は、言語や2次元画像・動画の基礎モデルを革新しましたが、多視点画像から3D意識的表現を学ぶことはまだ十分に探求されていません。本論文では、E-RayZerという自己監督の大規模な3Dビジョンモデルを紹介します。これはラベル付き画像から直接に学習された真に3D意識的表現です。RayZerのような従来の自己監督手法が潜在空間での視点合成を通じて3Dを間接的に推測するのとは異なり、E-RayZerは直接3D空間で作業し、明示的な幾何学を持つ自己監督3D再構成を行います。この形式化によって短絡解が排除され、表現が幾何学的に根拠付けられます。収束とスケーラビリティを確保するために、訓練を容易なサンプルから難しいサンプルへ組織化し、完全に無監督で異種データソースを調和させる新規の細部学習カリキュラムを導入します。実験では、E-RayZerが姿勢推定においてRayZerを大幅に上回り、VGGTのような完全監督再構成モデルと同等またはそれ以上の性能を示すことが確認されました。さらに、その学習済み表現はDINOv2、CroCo v2、VideoMAE V2、RayZerなどの主要な視覚事前学習モデルを上回り、3Dダウンストリームタスクへの転移において優れた性能を発揮します。これにより、E-RayZerは3D意識的視覚事前学習の新しいパラダイムとして確立されます。
</details>

<details>
<summary> 英語要旨 </summary>

Self-supervised pre-training has revolutionized foundation models for language, 2D images and videos, but remains largely unexplored for learning 3D-aware representations from multi-view images. In this paper, we present E-RayZer, a self-supervised large 3D Vision model that learns truly 3D-aware representations directly from unlabeled images. Unlike prior self-supervised methods such as RayZer that infer 3D indirectly through latent-space view synthesis, E-RayZer operates directly in 3D space, performing self-supervised 3D reconstruction with explicit geometry. This formulation eliminates shortcut solutions and yields representations that are geometrically grounded. To ensure convergence and scalability, we introduce a novel fine-grained learning curriculum that organizes training from easy to hard samples and harmonizes heterogeneous data sources in an entirely unsupervised manner. Experiments demonstrate that E-RayZer significantly outperforms RayZer on pose estimation, matches or sometimes surpasses fully supervised reconstruction models such as VGGT. Furthermore, its learned representations outperform leading visual pre-training models (e.g., DINOv2, CroCo v2, VideoMAE V2, and RayZer) when transferring to 3D downstream tasks, establishing E-RayZer as a new paradigm for 3D-aware visual pre-training.
</details>

---

### DLWM: Dual Latent World Models Enable Holistic Gaussian-centric Pre-training in Autonomous Driving
著者: Yiyao Zhu, Ying Xue, Haiming Zhang, Guangfeng Jiang, Wending Zhou, Xu Yan, Jiantao Gao, Yingjie CAI, Bingbing Liu, Zhen Li, Shaojie Shen

<details>
<summary> 日本語要旨 </summary>

ビジョンベースの自動運転は、低コストで優れた性能を持つことから多くの注目を集めています。密なBEV（鳥瞰図）やスパースクエリーモデルに比べて、ガウシアンセントリック法は3Dセマンティックガウシアンでシーンを記述することにより、包括的かつスパースな表現です。本論文では、自動運転用のホリスティックなガウシアンセントリックプレトレーニングを可能にするために、Dual Latent World Models（DLWM）という新しいパラダイムを2段階で導入します。第1段階では、自己監督学習によるマルチビューのセマンティック画像および深度画像の再構成から3Dガウシアンをクエリから予測します。第2段階では、細部まで考慮した文脈的特徴を備えており、時間的特徴学習のために2つのラテントワールドモデルが別々にトレーニングされます。これには、下流の占有性認識と予測タスク用のガウシアンフローガイド付きラテント予測および運動計画用のエゴプランニングガイド付きラテント予測が含まれます。SurroundOccとnuScenesベンチマークにおける広範な実験は、DLWMが3D占有性認識、4D占有性予測、運動計画タスクにわたって顕著なパフォーマンス向上を示していることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Vision-based autonomous driving has gained much attention due to its low costs and excellent performance. Compared with dense BEV (Bird’s Eye View) or sparse query models, Gaussian-centric method is a comprehensive yet sparse representation by describing scene with 3D semantic Gaussians. In this paper, we introduce DLWM, a novel paradigm with Dual Latent World Models specifically designed to enable holistic gaussian-centric pre-training in autonomous driving using two stages. In the first stage, DLWM predicts 3D Gaussians from queries by self-supervised reconstructing multi-view semantic and depth images. Equipped with fine-grained contextual features, in the second stage, two latent world models are trained separately for temporal feature learning, including Gaussian-flow-guided latent prediction for downstream occupancy perception and forecasting tasks, and ego-planning-guided latent prediction for motion planning. Extensive experiments in SurroundOcc and nuScenes benchmarks demonstrate that DLWM shows significant performance gains across Gaussian-centric 3D occupancy perception, 4D occupancy forecasting and motion planning tasks.
</details>

---

### SDUIE: Semi-Supervised Diffusion for Underwater Image Enhancement with Quant-Text Dual Control
著者: Xiaofeng Cong, Yu-Xin Zhang, Hao Shen, Yeying Jin, Junming Hou, Jie Gui

<details>
<summary> 日本語要旨 </summary>

水中画像は、波長依存の光減衰により、青緑色が支配的になることが多いです。既存の強化方法は有望な成果を達成していますが、通常は視覚的好みの主観性を無視します。このギャップを埋めるために、私たちはSDUIE（水中画像強化のレベル認識セミ教師付き拡散フレームワーク）を提案します。これは定量的およびテキスト入力による二重制御を可能にします。SDUIE-Quantでは、低ランク適応重みのマージを用いて、強化レベルを連続的かつ数値的に調整できます。このモデルは、監督された枝（合成水中陸上ペアでトレーニング）と自己監督された枝（実際の水中シーンの自然な色を保持するように設計）から構成される二重分岐拡散モデルです。これに基づき、SDUIE-Textはセマンティックプロンプトと視覚強化効果を整合させることで直感的な言語ガイド付き制御を導入します。これにより学習された融合重みを活用します。この二重モダリティ設計は、正確な制御と柔軟でユーザー好みの強化を提供します。実験結果によると、SDUIEは従来の方法がしばしば見逃す美的品質をより良く保持しつつ、最先端の成果を達成しています。ソースコードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Underwater images often exhibit dominant blue-green hues due to wavelength-dependent light attenuation. While existing enhancement methods have achieved promising performance, they typically overlook the subjective nature of visual preferences. To address this gap, we propose SDUIE, a level-aware Semi-supervised Diffusion framework for Underwater Image Enhancement that enables dual control through both quantitative and textual inputs. SDUIE-Quant allows continuous, numerical adjustment of enhancement levels via low-rank adaptation weight merging within a dual-branch diffusion model. This model comprises a supervised branch trained on synthetic underwater-terrestrial pairs and a self-supervised branch designed to preserve the natural hues of real-world underwater scenes. Building on this, SDUIE-Text introduces intuitive, language-guided control by aligning semantic prompts with visual enhancement effects, leveraging the learned fusion weights. This dual-modality design offers both precise control and flexible, user-preferred enhancement. Experimental results demonstrate that SDUIE achieves state-of-the-art results while better preserving the aesthetic qualities often missed by conventional methods. The source code will be made publicly available.
</details>

---

### Align Images Before You Generate
著者: Shihua Zhang, Qiuhong Shen, Xinchao Wang

<details>
<summary> 日本語要旨 </summary>

マルチ画像拡散モデルは、静的または動的なシーンを記述するためにマルチビューやビデオのような画像を生成できますが、テクスチャや構造のずれが依然として存在し、空間時間的一貫性を大幅に損なっています。この問題に対処することは特に、純粋な生成推論中に外部の幾何学的または意味的事前知識がない場合、依然として課題です。本論文では、CorrAdapterを導入します。これは、マルチ画像拡散自体に内在する特性を発見し活用するプラグアンドプレイ型のアダプターであり、実際に生成される前にすべての出力画像を整列させます。具体的には、CorrAdapterはマルチ画像拡散モデル内のトランスフォーマーブロックにバイパスブランチを設計し、中間特徴から信頼性のある対応関係を構築するネイティブな対応関係構成者と、曖昧な情報交換を避けるために一致した領域からのメッセージだけを統合する整列領域アグリゲーターを含んでいます。ネイティブな対応関係を指針として、CorrAdapterは追加入力なしに空間時間的一貫性を向上させることができ、トレーニングフリーかつベースライン非依存であるため、様々な生成タスクへのシームレスな汎用化が可能です。また、より改善された可能性を探索するオプションのトレーニングスキームも提供しています。静的マルチビュー生成および動的ビデオ生成に関する実験では、CorrAdapterが強力なベースラインを一貫して上回り、空間時間的一貫性と知覚品質の向上を示しました。これは幾何学的に忠実なマルチ画像拡散へのシンプルでありながら汎用的なドロップインアプローチを提供します。
</details>

<details>
<summary> 英語要旨 </summary>

Multi-image diffusion models can generate images like multi-views or videos to describe static or dynamic scenes, yet texture and structure drift persist, severely undermining the spatiotemporal consistency. Addressing this issue remains challenging, especially without any external geometric or semantic priors during the pure generative inference. In this paper, we introduce CorrAdapter, a plug-and-play adapter that discovers and exploits an innate property of the multi-image diffusion itself, aligning all output images before they are in fact generated. Specifically, CorrAdapter designs a bypass branch for transformer blocks in the multi-image diffusion model, encompassing a native correspondence constructor that builds reliable correspondences from the diffusion model's intermediate features, and an aligned area aggregator that integrates messages from only matching regions to avoid ambiguous information interactions. Given the native correspondences as guidance, CorrAdapter can enhance spatiotemporal consistency without any auxiliary inputs, and remains training-free and baseline-agnostic, which enables it to generalize seamlessly to various generation tasks. Additionally, we provide an optional training scheme to explore further-improved possibilities. Experiments on both static multi-view generation and dynamic video generation show that CorrAdapter consistently improves spatiotemporal consistency and perceptual quality over strong baselines, offering a simple yet versatile drop-in approach to geometrically faithful multi-image diffusion.
</details>

---

### Bi-directional Autoregressive Diffusion for Large Complex Motion Interpolation
著者: Yongrui Ma, Shijie Zhao, Mingde Yao, Junlin Li, Li zhang, Xiaohong Liu, Qi Dou, Jinwei Gu, Tianfan Xue

<details>
<summary> 日本語要旨 </summary>

最近の進歩にもかかわらず、拡散ベースの動画フレーム補間方法は依然として大規模で複雑な運動に苦労し、不連続な運動やフレーム間でのオブジェクト外観の一貫性を欠く結果となっています。これらの制限は、現在の全シーケンス補間戦略およびピクセル再構成訓練目的に起因していることが観察されています。これらの課題を解決するために、我々は大規模で複雑な運動補間用の新しい拡散ベースの動画補間方法であるARVFIを提案します。ARVFIは、すべての中間フレームを同時に生成する代わりに、2つの入力フレームから中間フレームに向けて自己回帰的に補間します。したがって、ARVFIは以前のすべての補間結果に基づいて入力から遠く離れたフレームを補間し、より滑らかな運動移行と優れた時間的一貫性を実現します。さらに、ARVFIはDINOv3特徴を運動表現として利用し、単純なピクセルレベルの損失に比べて高次元の意味論を提供し、正確な運動推定が可能です。これらの設計により、ARVFIはまず中間DINOv3特徴を生成し、その後効果的な条件付き生成方法でフレームを生成します。我々のARVFIは、優れた補間精度と視覚品質において一貫して既存の手法を上回ります。
</details>

<details>
<summary> 英語要旨 </summary>

Despite recent progress, diffusion-based video frame interpolation methods still struggle with large complex motions, resulting in discontinuous motions and inconsistent object appearances across frames. We observe that these limitations arise from both the current full-sequence interpolation strategy and the pixel reconstruction training objective. To solve these challenges, we propose ARVFI, a novel video diffusion-based interpolation method for large complex motion interpolation. Instead of generating all intermediate frames simultaneously, ARVFI interpolates in an autoregressive manner from two input frames to the middle ones. Thus, ARVFI interpolates a frame that is further away from the inputs based on all previous interpolation results, resulting in smoother motion transitions and better temporal consistency. Additionally, ARVFI further utilizes DINOv3 features as motion representations, which provide high-level semantics for accurate motion estimation, compared with a simple pixel-level loss. With all these designs, ARVFI generates the intermediate DINOv3 features first and then the frames with an effective conditional generation method for frames. Our ARVFI consistently outperforms existing methods with superior interpolation accuracy and visual quality.
</details>

---

### The Devil Is in The Details: Enhancing Video Virtual Try-On Via Keyframe-Driven Details Injection
著者: Qingdong He, Xueqin Chen, Yanjie Pan, Peng Tang, Pengcheng Xu, Zhenye Gan, Chengjie Wang, Xiaobin Hu, Jiangning Zhang, Yabiao Wang

<details>
<summary> 日本語要旨 </summary>

ディフュージョントランスフォーマー（DiT）ベースのビデオ仮想試着（VVT）は、リアルな動画を合成する点で大きな進歩を遂げていますが、現在の手法では細部にわたる衣服のダイナミクスを捉えることや、ビデオフレーム間で背景の完全性を保つことに苦労しています。また、DiTに追加された相互作用モジュールにより計算コストが高くなる一方で、公開されているデータセットの規模や品質が限られており、モデルの汎化性能と効果的なトレーニングを制約しています。これらの課題に対処するため、我々は新しいフレームワーク「KeyTailor」と大規模で高解像度のデータセット「ViT-HD」を提案します。KeyTailorの核となるアイデアは、キーフレーム駆動型の詳細注入戦略であり、キーフレームが本質的に前景ダイナミクスと背景の一貫性を含んでいることに着想を得ています。具体的には、KeyTailorは指示に基づくキーフレームサンプリング戦略を採用し、入力ビデオから情報豊富なフレームを選別します。その後、衣服の詳細強化モジュールと協調的背景最適化モジュールという2つのキーフレーム駆動型モジュールを用いて、衣服関連ラテンスに衣服ダイナミクスを凝縮し、背景ラテンスの完全性を最適化します。これらはキーフレームによってガイドされます。これらの詳細が標準的なDiTブロックにポーズ、マスク、ノイズラテンスと共に注入されることで、効率的かつリアルな試着ビデオ合成が可能になります。この設計はDiTのアーキテクチャを明示的に変更することなく一貫性を保ちつつ、同時に追加の複雑さを避けるものです。また、我々のデータセットViT-HDは、810×1080ピクセル解像度で15,070本の高品質ビデオサンプルから構成されており、多様な衣服をカバーしています。広範囲にわたる実験では、KeyTailorが動的・静的シナリオの両方で衣服の忠実度と背景の完全性において最先端のベースラインを上回っていることが示されました。データセットとコードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Although diffusion transformer (DiT)-based video virtual try-on (VVT) has made significant progress in synthesizing realistic videos, existing methods still struggle to capture fine-grained garment dynamics and preserve background integrity across video frames. They also incur high computational costs due to additional interaction modules introduced into DiTs, while the limited scale and quality of existing public datasets also restrict model generalization and effective training. To address these challenges, we propose a novel framework, KeyTailor, along with a large-scale, high-definition dataset, ViT-HD. The core idea of KeyTailor is a keyframe-driven details injection strategy, motivated by the fact that keyframes inherently contain both foreground dynamics and background consistency. Specifically, KeyTailor adopts an instruction-guided keyframe sampling strategy to filter informative frames from the input video. Subsequently, two tailored keyframe-driven modules—the garment details enhancement module and the collaborative background optimization module—are employed to distill garment dynamics into garment-related latents and to optimize the integrity of background latents, both guided by keyframes. These enriched details are then injected into standard DiT blocks together with pose, mask, and noise latents, enabling efficient and realistic try-on video synthesis. This design ensures consistency without explicitly modifying the DiT architecture, while simultaneously avoiding additional complexity. In addition, our dataset ViT-HD comprises 15,070 high-quality video samples at a resolution of 810 × 1080, covering diverse garments. Extensive experiments demonstrate that KeyTailor outperforms state-of-the-art baselines in terms of garment fidelity and background integrity across both dynamic and static scenarios. The dataset and code will be publicly released.
</details>

---

### MoCoDiff: A Controllable Autoregressive Diffusion Model for Expressive Motion Generation
著者: Wenfeng Song, Xuehan Wang, Shuai Li, Yi Chen, Yuting Guo, Zhenyu Wu, Xingliang Jin, Chenglizhao Chen, Fei Hou, Hongyu Wu, Aimin Hao

<details>
<summary> 日本語要旨 </summary>

拡散ベースの動作生成は急速に進歩していますが、現在の方法では長期的な一貫性、スタイル制御、およびマルチ条件ガイダンスにまだ苦労しています。その主な理由は、融合された条件付け設計であり、意味的、スタイリッシュ、時間的信号が単一の経路を共有し、干渉を引き起こし制御可能性を制限しています。私たちは、注入モジュレーションコントローラー（IMC）を導入する制御可能な自己回帰拡散フレームワークであるMoCoDiffを提案します。IMCは、テキスト、スタイル、および履歴信号を別々の条件付けパスを通じて注入する軽量かつモーダリティ固有の線形モジュレーションモジュールです。IMCは凍結されたバックボーンの単純さを保持しつつ、融合条件付けに内在する絡み合いを避けることで、より安定かつ解釈可能なマルチ条件制御を可能にします。長距離合成をさらに強化するために、歴史をステップ依存の修正信号として適用するタイムリーIMC（TIMC）を備えた制御可能な自己回帰拡散モデルを開発しました。この制御可能な形式は、ドリフトを積極的に抑制し、動作セグメント間で滑らかな遷移を強制し、長期シーケンスにおける時間的一貫性を大幅に向上させます。実験では、MoCoDiffが最先端のスタイル忠実度、トランジション品質、効率を達成し、再訓練なしで柔軟かつ解釈可能なマルチ条件動作合成をサポートしていることが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

Diffusion-based motion generation has advanced rapidly, but current methods still struggle with long-horizon consistency, style control, and multi-condition guidance. A major reason is the fused-conditioning design, where semantic, stylistic, and temporal signals share a single pathway, causing interference and limiting controllability. We propose MoCoDiff, a controlable autoregressive diffusion framework that introduces Injection Modulation Controllers (IMC). IMC is a lightweight, modality-specific linear modulation modules that inject text, style, and history signals through separate conditioning paths. IMC preserves the simplicity of a frozen backbone while avoiding the entanglement inherent to fused conditioning, enabling more stable and interpretable multi-condition control. To further enhance long-range synthesis, we develop a controllable autoregressive diffusion model equipped with Temporal IMC (TIMC), which applies history as a timestep-dependent corrective signal. This controllable formulation actively suppresses drift, enforces smooth transitions across motion segments, and significantly improves temporal coherence over extended sequences. Experiments show that MoCoDiff achieves state-of-the-art style fidelity, transition quality, and efficiency, while supporting flexible and interpretable multi-condition motion synthesis without retraining.
</details>

---

### MuViT: Multi-Resolution Vision Transformers for Learning Across Scales in Microscopy
著者: Albert Dominguez Mantes, Gioele Manno, Martin Weigert

<details>
<summary> 日本語要旨 </summary>

現代の顕微鏡は、細胞形態から組織全体の配置までを含むギガピクセル画像を一般的に生成します。多くの解析タスクではこれらのスケールを組み合わせる必要がありますが、ほとんどのビジョンモデルは単一の解像度で動作するか、あるいは1つの視点から多重解像度特徴を導出します。これにより、顕微鏡データの本質的なマルチレゾリューション性を活用できなくなっています。私たちは、MuViTというトランスフォーマー構造を導入しました。これは同じ基礎画像からの真のマルチレゾリューション観測を融合するように設計されています。MuViTはすべてのパッチを共通の世界座標系に埋め込み、これらの座標に回転位置埋め込みを拡張します。これにより、エンコーダー内で単一のものとして広範囲の文脈と高解像度の詳細を統合する注意が可能になります。合成ベンチマーク、腎臓病理学、および高解像度マウス脳顕微鏡にわたって、MuViTは強力なViTとCNNの基準値を一貫して上回ります。マルチレゾリューションMAE事前学習はさらにスケール一貫性のある表現を生成し、下流タスクを強化します。これらの結果は、明示的な世界座標モデリングが大規模顕微鏡解析におけるマルチレゾリューション情報の活用に簡単でありながら強力なメカニズムを提供することを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Modern microscopy routinely produces gigapixel images that contain structures across multiple spatial scales, from fine cellular morphology to broader tissue organization. Many analysis tasks require combining these scales, yet most vision models operate at a single resolution or derive multi-scale features from one view, limiting their ability to exploit the inherently multi-resolution nature of microscopy data. We introduce MuViT, a transformer architecture built to fuse true multi-resolution observations from the same underlying image. MuViT embeds all patches into a shared world-coordinate system and extends rotary positional embeddings to these coordinates, enabling attention to integrate wide-field context with high-resolution detail within a single encoder. Across synthetic benchmarks, kidney histopathology, and high-resolution mouse-brain microscopy, MuViT delivers consistent improvements over strong ViT and CNN baselines. Multi-resolution MAE pretraining further produces scale-consistent representations that enhance downstream tasks. These results demonstrate that explicit world-coordinate modeling provides a simple yet powerful mechanism for leveraging multi-resolution information in large-scale microscopy analysis.
</details>

---

### Tracking By Predicting 3-D Gaussians Over Time
著者: Tanish Baranwal, Himanshu Singh Singh, Jathushan Rajasegaran, Jitendra Malik

<details>
<summary> 日本語要旨 </summary>

私たちは、画像のシーケンスを時間と共に移動するガウススプラッツのセットにエンコードする自己監督アプローチであるビデオGaussian Masked Autoencoders（Video-GMAE）を提案します。ビデオをガウス分布のセットとして表現することは、2次元のビデオがしばしば動的な3次元シーンの一貫した投影であるという合理的な帰納バイアスを強制します。このアーキテクチャでネットワークを事前学習することにより、トラッキングが現れることを発見しました。学習されたガウス分布の軌跡を画像平面上にマッピングすることで、事前訓練なしでのトラッキング性能が最先端技術と比較可能になります。小規模な微調整により、私たちのモデルはKineticsおよびKubricデータセットで34.6%および13.1%の改善を達成し、既存の自己監督ビデオアプローチを上回ります。
</details>

<details>
<summary> 英語要旨 </summary>

We propose Video Gaussian Masked Autoencoders (Video-GMAE), a self-supervised approach for representation learning that encodes a sequence of images into a set of Gaussian splats moving over time. Representing a video as a set of Gaussians enforces a reasonable inductive bias: that 2-D videos are often consistent projections of a dynamic 3-D scene. We find that tracking emerges when pre-training a network with this architecture. Mapping the trajectory of the learnt Gaussians onto the image plane gives zero-shot tracking performance comparable to state-of-the-art. With small-scale finetuning, our models achieve 34.6% improvement on Kinetics, and 13.1% on Kubric datasets, surpassing existing self-supervised video approaches.
</details>

---

### SRPO: Self-Referential Policy Optimization for Vision-Language-Action Models
著者: Senyu Fei, Siyin Wang, Li Ji, Ao Li, Shiduo Zhang, Liming Liu, Jinlong Hou, Jingjing Gong, Xianzhong Zhao, Xipeng Qiu

<details>
<summary> 日本語要旨 </summary>

ビジョン・ランゲージ・アクション（VLA）モデルはロボット操作において優れた性能を発揮しますが、専門家のデモンストレーションへの強い依存により、デモンストレーションバイアスが生じ、パフォーマンスが制限されます。この限界を克服するためには、強化学習（RL）が重要なポストトレーニング戦略として機能しますが、現在のVLA-RL手法、特にグループベースの最適化アプローチは、極端な報酬スパース性によって制約されています。バイナリ成功指標に依存することで失敗した軌道から得られる貴重な情報が無駄になり、トレーニング効率が低下します。これを解決するために、私たちは新しいVLA-RLフレームワークであるSelf-Referential Policy Optimization（SRPO）を提案します。SRPOは外部のデモンストレーションや手動による報酬エンジニアリングを必要とせず、現在のトレーニングバッチ内で生成されたモデル自身の成功した軌道を自己参照として利用します。これにより、失敗した試みに対して段階的な報酬を割り当てることができます。中核的な革新は、行動の進捗を堅牢に測定するためにLatent World Representationsを使用することです。生のピクセルやドメイン固有の微調整に依存する代わりに、ワールドモデルの潜在空間から得られる圧縮された移転可能なエンコーディングを利用します。これらの表現は自然に異なる環境間で進捗パターンを捉え、正確かつ一般化された軌道比較を可能にします。LIBEROベンチマークにおける実証評価では、SRPOの効率性と有効性が示されています。48.9%の成功率からスタートした監督学習ベースラインから、SRPOはわずか200 RLステップで新たな最先端の成功率99.2%を達成し、追加の監視なしに103%の相対的改善を示します。さらに、LIBERO-Plusベンチマークにおいて167%のパフォーマンス向上を実現することで、SRPOは大幅な堅牢性も示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Vision-Language-Action (VLA) models excel in robotic manipulation but are constrained by their heavy reliance on expert demonstrations, leading to demonstration bias and limiting performance. Reinforcement learning (RL) is a vital post-training strategy to overcome these limits, yet current VLA-RL methods, including group-based optimization approaches, are crippled by severe reward sparsity. Relying on binary success indicators wastes valuable information in failed trajectories, resulting in low training efficiency. To solve this, we propose Self-Referential Policy Optimization (SRPO), a novel VLA-RL framework. SRPO eliminates the need for external demonstrations or manual reward engineering by leveraging the model’s own successful trajectories, generated within the current training batch, as a self-reference. This allows us to assign a progress-wise reward to failed attempts. A core innovation is the use of Latent World Representations to measure behavioral progress robustly. Instead of relying on raw pixels or requiring domain-specific fine-tuning, we utilize the compressed, transferable encodings from a world model’s latent space. These representations naturally capture progress patterns across environments, enabling accurate, generalized trajectory comparison. Empirical evaluations on the LIBERO benchmark demonstrate SRPO’s efficiency and effectiveness. Starting from a supervised baseline with 48.9% success, SRPO achieves a new state-of-the-art success rate of 99.2% in just 200 RL steps, representing a 103% relative improvement without any extra supervision. Furthermore, SRPO shows substantial robustness, achieving a 167% performance improvement on the LIBERO-Plus benchmark.
</details>

---

### LIBERO-Plus: A Progressive Robustness Benchmark for Visual-Language-Action Models
著者: Senyu Fei, Siyin Wang, Junhao Shi, Zihao Dai, Jikun Cai, Pengfang Qian, Li Ji, Xinzhe He, Shiduo Zhang, Zhaoye Fei, Jinlan Fu, Jingjing Gong, Xipeng Qiu

<details>
<summary> 日本語要旨 </summary>

視覚・言語・行動（VLA）モデルは、ロボット操作のベンチマークで95％を超える印象的な成功率を報告していますが、これらの結果は堅牢性における基本的な弱点を隠している可能性があります。現在のシミュレーションベースの堅牢性評価は、狭い摂動カバー範囲、手作業による設計制約、および失敗の時期や方法を明らかにしない粗視化された分析に苦しんでいます。このギャップに対処するために、私たちはLIBERO-Plusという包括的で自動的で細部まで行き届いた評価フレームワークを提案します。これは、オブジェクト配置、カメラ視点、ロボットの初期状態、言語指示、照明条件、背景テクスチャ、センサーノイズという7つの次元にわたる制御された摂動を持っています。私たちの系統的な分析は、10の最先端モデルで一貫した脆弱性が明らかになり、95％からわずかな摂動下では30％未満にパフォーマンスが低下することを示しています。これらの発見は、高いベンチマークスコアが真の能力を意味するという仮定に挑戦し、現実的な変動下での信頼性を評価する評価慣行の必要性を浮き彫りにしています。
</details>

<details>
<summary> 英語要旨 </summary>

Visual–Language–Action (VLA) models report impressive success rates exceeding 95\% on robotic manipulation benchmarks, yet these results may mask fundamental weaknesses in robustness. Current simulation-based robustness evaluations suffer from narrow perturbation coverage, manual design constraints, and coarse-grained analysis that fails to reveal when and how models fail. To address this gap, we propose LIBERO-Plus, a comprehensive, automatic, and fine-grained evaluation framework with controlled perturbations across seven dimensions: object layouts, camera viewpoints, robot initial states, language instructions, lighting conditions, background textures, and sensor noise. Our systematic analysis of ten state-of-the-art models reveals consistent brittleness beneath apparent competence, with performance dropping from 95\% to below 30\% under modest perturbations. Our findings challenge the assumption that high benchmark scores equate to true competency and highlight the need for evaluation practices that assess reliability under realistic variation.
</details>

---

### VideoWorld 2: Learning Transferable Knowledge from Real-world Videos
著者: Zhongwei Ren, Yunchao Wei, Xiao Yu, Guixun Luo, Yao Zhao, Bingyi Kang, Jiashi Feng, Xiaojie Jin

<details>
<summary> 日本語要旨 </summary>

ラベルなしのビデオデータから学習した移植可能な知識を新しい環境で適用することは、高度な人工知能の特徴です。私たちはVideoWorld 2を紹介します。これはVideoWorldを拡張し、初めて原始的な実世界ビデオから直接移植可能な知識を学習することについての調査を提供します。その核心部分では、VideoWorld 2はアクションダイナミクスと視覚的外見を切り離すdisentangled Latent Dynamics Model（dLDM）を導入しています：予め学習されたビデオ拡散モデルが外見のモデリングを処理し、これによってdLDMはタスク関連のコンパクトで意味のある変化に焦点を当てた潜在的なコードを学習することが可能になります。その後、これらの潜在的なコードはタスクポリシーを学ぶために自己回帰的に系列としてモデル化され、長期的な推論をサポートします。私たちはVideoWorld 2を実世界のビデオ手工芸作成タスクで評価しました。ここでは、以前のビデオ生成モデルや潜在ダイナミクスモデルが信頼性を持って動作することに苦労しています。VideoWorld 2はタスク成功率で70%以上の改善を達成し、一貫した長期実行ビデオを生成します。ロボティクスでは、Open-Xデータセットから有効な操作知識を獲得することができることを示し、これによりCALVIN上のタスクパフォーマンスが大幅に向上します。この研究は、すべてのコード、データ、モデルがさらなる研究のためにオープンソース化されることを明らかにし、原始的なビデオから直接移植可能な世界知識を学ぶ可能性を示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Learning transferable knowledge from unlabeled video data and applying it in new environments is a hallmark of advanced artificial intelligence. We present VideoWorld 2, which extends VideoWorld and offers the first investigation into learning transferable knowledge directly from raw real-world videos. At its core, VideoWorld 2 introduces a disentangled Latent Dynamics Model (dLDM) that decouples action dynamics from visual appearance: a pretrained video diffusion model handles appearance modeling, enabling the dLDM to learn latent codes that focus on compact and meaningful task-related changes. These latent codes are then modeled autoregressively as a sequence to learn task policies and support long-horizon reasoning. We evaluate VideoWorld 2 on real-world video handcraft making tasks, where prior video generation and latent-dynamics models struggle to operate reliably. VideoWorld 2 achieves over a 70% improvement in task success rate and produces coherent long execution videos. In robotics, we show that VideoWorld 2 can acquire effective manipulation knowledge from the Open-X dataset, which substantially improves task performance on CALVIN. This study reveals the potential of learning transferable world knowledge directly from raw videos, with all code, data, and models to be open-sourced for further research.
</details>

---

### Visual Autoregressive Modeling Via Next Focus Prediction
著者: Xiaofan Li, Chenming Wu, Yanpeng Sun, Jiaming Zhou, Delin Qu, Yansong Qu, Weihao Bo, Haibao Yu, Dingkang Liang

<details>
<summary> 日本語要旨 </summary>

視覚的自己回帰モデルは、多スケールトークンピラミッドにわたる次スケール予測を通じて顕著な生成品質を達成します。しかし、従来の方法では均一なダウンサンプリングを使用してこれらのピラミッドを構築し、細部が失われるほか、不要なジャギーやモアレパターンを引き起こす疎視効果が生じます。この問題に対処するために、私たちは**FVAR**を提案します。これは、次スケール予測から次フォーカス予測へのパラダイム転換を行い、カメラがぼやけからクリアさへと焦点を合わせる自然なプロセスを模倣します。私たちのアプローチは三つの重要な革新を導入します：1) 次フォーカス予測パラダイム、これにより単純なダウンサンプリングではなくぼやけを徐々に減少させることで多スケール自己回帰を変換します；2) 物理的に一貫したデフォーカスカーネルを使用してクリーンかつ疎視効果のない多スケール表現を構築する進行的再焦点化ピラミッド構築；3) 特殊な残差教師ネットワークを使用してトレーニング中に疎視情報を効果的に取り入れつつ、展開の単純さを保持する高周波数残差学習。具体的には、減少半径のデフォーカスポイント拡がり関数（PSF）カーネルを使用して光学低域通過ビューを構築し、ぼやけからクリアさへの滑らかな移行を作成することで疎視効果の発生源を排除します。詳細生成をさらに強化するために、清浄構造および疎視残差から学習する高周波数残差教師を導入し、これを通常のVAR展開ネットワークに効果的に転移させてシームレスな推論が可能とします。ImageNetでの広範な実験では、FVARが疎視効果を大幅に減少させ、細部の保存性を向上させ、テキストの読みやすさを高めることで、既存のVARフレームワークと完全な互換性を持ちつつ優れたパフォーマンスを達成することが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

Visual autoregressive models achieve remarkable generation quality through next-scale predictions across multi-scale token pyramids. However, the conventional method uses uniform scale downsampling to build these pyramids, leading to aliasing artifacts that compromise fine details and introduce unwanted jaggies and moiré patterns. To tackle this issue, we present \textbf{FVAR}, which reframes the paradigm from \emph{next-scale prediction} to \emph{next-focus prediction}, mimicking the natural process of camera focusing from blur to clarity. Our approach introduces three key innovations: 1) \emph{Next-Focus Prediction Paradigm} that transforms multi-scale autoregression by progressively reducing blur rather than simply downsampling; 2) \emph{Progressive Refocusing Pyramid Construction} that uses physics-consistent defocus kernels to build clean, alias-free multi-scale representations; and 3) \emph{High-Frequency Residual Learning} that employs a specialized residual teacher network to effectively incorporate alias information during training while maintaining deployment simplicity. Specifically, we construct optical low-pass views using defocus point spread function (PSF) kernels with decreasing radius, creating smooth blur-to-clarity transitions that eliminate aliasing at its source. To further enhance detail generation, we introduce a High-Frequency Residual Teacher that learns from both clean structure and alias residuals, distilling this knowledge to a vanilla VAR deployment network for seamless inference. Extensive experiments on ImageNet demonstrate that FVAR substantially reduces aliasing artifacts, improves fine detail preservation, and enhances text readability, achieving superior performance with perfect compatibility to existing VAR frameworks.
</details>

---

### Towards Highly-Constrained Human Motion Generation with Retrieval-Guided Diffusion Noise Optimization
著者: Hanchao Liu, Fang-Lue Zhang, Shining Zhang, Tai-Jiang Mu, Shi-Min Hu

<details>
<summary> 日本語要旨 </summary>

カスタマイズされたゼロショット目標関数を満たす人間の動作生成は、制御可能なキャラクターアニメーションやバーチャルエージェントの行動合成といった応用において重要な能力です。現在のアプローチは多くの未見制約を処理できますが、厳しい空間時間的制限を持つタスク（例えば、深刻な空間障害物や指定された歩数）では失敗します。これらの高度に制約されたタスクに対応する動作生成器を装備するために、トレーニングフリーな拡散ノイズ最適化フレームワークに基づく検索ガイド法を提案します。このアイデアの核心は、困難な制約を満たす可能性のあるガイダンスを大規模な動作データセット内で探すことです。ターゲット制約をグループ化し、取得された参照によって処理されるべき困難なものを特定するために関係的タスク解析を導入します。その後、ランダムノイズと取得ノイズを組み合わせた報酬ガイドマスクを用いて、より良い拡散ノイズの初期化が得られます。この改善された初期化から拡散ノイズを最適化することで、高度に制約された生成タスクを成功裏に解決します。LLMを活用した関係的タスク解析により、フレームワーク全体が何を取得すべきか自動的に推論できるようになり、トレーニングフリー最適化方式の下で移動エージェントの知能が向上します。コードは公開時にリリースされます。
</details>

<details>
<summary> 英語要旨 </summary>

Generating human motion that satisfies customized zero-shot goal functions, enabling applications such as controllable character animation and behavior synthesis for virtual agents, is a critical capability. While current approaches handle many unseen constraints, they fail on tasks with very challenging spatiotemporal restrictions, such as severe spatial obstacles or specified numbers of walking steps. To equip motion generators for these highly constrained tasks, we present a retrieval-guided method built on the training-free diffusion noise optimization framework. The key idea is to search within large motion datasets for guidance that can potentially satisfy difficult constraints. We introduce relational task parsing to group target constraints and identify the difficult ones to be handled by retrieved reference. A better initialization for diffusion noise is then obtained via a reward-guided mask that combines random noise with retrieved noise. By optimizing diffusion noise from this improved initialization, we successfully solve highly constrained generation tasks. By leveraging LLM for relational task parsing, the whole framework is further enabled to automatically reason for what to retrieve, improving the intelligence of moving agents under a training-free optimization scheme. Code will be released upon publication.
</details>

---

### Scaling Instruction-Based Video Editing with A High-Quality Synthetic Dataset
著者: Qingyan Bai, Qiuyu Wang, Hao Ouyang, Yue Yu, Hanlin Wang, Wen Wang, Ka Leong Cheng, Shuailei Ma, Yanhong Zeng, Zichen Liu, Yinghao Xu, Yujun Shen, Qifeng Chen

<details>
<summary> 日本語要旨 </summary>

指示に基づくビデオ編集はコンテンツ作成を民主化するという約束を持っていますが、大規模で高品質なトレーニングデータの不足によりその進展は大きく妨げられています。私たちはこの基本的な課題に対処するための総合的なフレームワークであるDittoを紹介します。Dittoの中核として、主要な画像エディタの創造性の多様性とインコンテキストビデオジェネレータを融合した革新的なデータ生成パイプラインがあります。これにより、既存モデルの限られた範囲を克服しています。このプロセスを実現可能にするために、私たちのフレームワークは効率的な蒸留されたモデルアーキテクチャとタイムリンクエンハンサーを採用し、これにより計算オーバーヘッドを削減しつつ時間的一貫性を向上させます。最後に、このパイプライン全体は賢いエージェントが多様な指示を作成し厳密に出力をフィルタリングすることで品質管理をスケール化します。このフレームワークを使用して、私たちは12,000 GPU日以上を投じてDitto-1Mという新しい100万の高品質ビデオ編集例からなるデータセットを構築しました。カリキュラム学習戦略に基づき、私たちはEdittoモデルをDitto-1Mでトレーニングしました。結果は優れた指示従属能力を示し、指示に基づくビデオ編集の新たな最先端を確立しています。私たちは再現性のためにデータセットとモデルを公開します。
</details>

<details>
<summary> 英語要旨 </summary>

Instruction-based video editing promises to democratize content creation, yet its progress is severely hampered by the scarcity of large-scale, high-quality training data. We introduce Ditto, a holistic framework designed to tackle this fundamental challenge. At its heart, Ditto features a novel data generation pipeline that fuses the creative diversity of a leading image editor with an in-context video generator, overcoming the limited scope of existing models. To make this process viable, our framework resolves the prohibitive cost-quality trade-off by employing an efficient, distilled model architecture augmented by a temporal enhancer, which simultaneously reduces computational overhead and improves temporal coherence. Finally, to achieve full scalability, this entire pipeline is driven by an intelligent agent that crafts diverse instructions and rigorously filters the output, ensuring quality control at scale. Using this framework, we invested over 12,000 GPU-days to build Ditto-1M, a new dataset of one million high-fidelity video editing examples. We trained our model, Editto, on Ditto-1M with a curriculum learning strategy. The results demonstrate superior instruction-following ability and establish a new state-of-the-art in instruction-based video editing. We will release our dataset and models for reproducibility.
</details>

---

### TopoHR: Hierarchical Centerline Representation for Cyclic Topology Reasoning in Driving Scenes with Point-to-Instance Relations
著者: Yifeng Bai, Zhirong Chen, Bo Song, Erkang Cheng, Haibin Ling

<details>
<summary> 日本語要旨 </summary>

自律走行において、トポロジー推論は重要です。現在の方法は主にセンターライン検出のインスタンスレベル学習に焦点を当て、その後に単純なMLP層に依存する順次モジュールでトポロジー推論が行われます。また、これらのアプローチはしばしばトポロジー推論における点からインスタンス（P2I）関係の重要性を無視しています。これらの制限に対処するため、センターライン検出とトポロジー推論間で循環的な相互作用を確立し、お互いを反復して向上させることができる新しいエンドツーエンドフレームワーク「TopoHR（トポロジカル階層表現）」を提案します。具体的には、点クエリ、インスタンスクエリ、セマンティック表現を含む階層的なセンターライン表現を導入しています。これらの多レベル特徴は、階層的センターラインデコーダー内でシームレスに統合・融合されます。さらに、細部のP2I関係とグローバルなインスタンス間（I2I）接続を一体化したアーキテクチャ内で捉える階層的トポロジー推論モジュールを設計しています。これらの新しいコンポーネントにより、TopoHRは正確かつ堅牢なトポロジー推論を保証します。OpenLane-V2ベンチマークでは、TopoHRが顕著な改善と共に最先端のパフォーマンスを更新しました。特に、以前の最良結果と比較して、TopoHRはsubset_Aで$\mathrm{DET}\_{\text{l}}$が+3.8、$\mathrm{TOP}\_{\text{ll}}$が+5.4、subset_Bでは$\mathrm{DET}\_{\text{l}}$が+11.0、$\mathrm{TOP}\_{\text{ll}}$が+7.9を達成し、提案されたコンポーネントの有効性を検証しています。論文受理後にコードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Topology reasoning is crucial for autonomous driving. Current methods primarily focus on instance-level learning for centerline detection, followed by a sequential module for topology reasoning that relies on simplified MLP layers. Moreover, these approaches often neglect the importance of point-to-instance (P2I) relationships in topology reasoning. To address these limitations, we present TopoHR (Topological Hierarchical Representation), a novel end-to-end framework that establishes cyclic interaction between centerline detection and topology reasoning, allowing them to iteratively enhance each other. Specifically, we introduce a hierarchical centerline representation including point queries, instance queries, and semantic representations. These multi-level features are seamlessly integrated and fused within a hierarchical centerline decoder. Furthermore, we design a hierarchical topology reasoning module that captures both fine-grained P2I relationships and global instance-to-instance (I2I) connections within a unified architecture. With these novel components, TopoHR ensures accurate and robust topology reasoning. On the OpenLane-V2 benchmark, TopoHR refreshes state-of-the-art performance with significant improvements. Notably, compared with previous best results, TopoHR achieves +3.8 in $\mathrm{DET}\_{\text{l}}$, +5.4 in $\mathrm{TOP}\_{\text{ll}}$ on subset_A and +11.0 in $\mathrm{DET}\_{\text{l}}$, +7.9 in $\mathrm{TOP}\_{\text{ll}}$ on subset_B, validating the effectiveness of the proposed components. The code will be shared publicly upon paper acceptance.
</details>

---

### Stable and Efficient Single-Rollout RL for Multimodal Reasoning
著者: Rui Liu, Dian Yu, Lei Ke, Haolin Liu, Yujun Zhou, Zhenwen Liang, Haitao Mi, Pratap Tokekar, Dong Yu

<details>
<summary> 日本語要旨 </summary>

強化学習における検証可能な報酬（RLVR）は、多モーダル大規模言語モデル（MLLMs）の推論能力を向上させるための重要なパラダイムとして浮上しています。しかし、一般的なグループベースのアルゴリズムであるGRPOは、各プロンプトに対してマルチロールアウトサンプリングを必要とします。テキストのみの設定では最近より効率的なシングルロールアウトバリエーションが探求されていますが、私たちはこれらが多モーダルコンテキストで重大な不安定性を引き起こし、しばしば訓練の崩壊につながることを発見しています。このサンプル効率-安定性トレードオフに対処するために、私たちはグループフリーのRLVRフレームワークである**MSSR（Multimodal Stabilized Single-Rollout）**を導入します。これは安定した最適化と効果的な多モーダル推論パフォーマンスの両方を実現します。MSSRは、利点の大きさを適応的に規制し、崩壊を防ぎ訓練の安定性を維持するエントロピーに基づく利点形成メカニズムを通じてこれを実現します。このようなメカニズムはグループベースのRLVRで使用されてきましたが、私たちは多モーダルシングルロールアウト設定では安定性にとって単に有益であるだけでなく不可欠であることを示しています。分布内評価では、MSSRは優れたロールアウトサンプル効率を示し、同等の検証精度を半分の訓練ステップで達成しています。同じ数のステップで訓練された場合、MSSRのパフォーマンスはグループベースのベースラインを上回り、5つの多様な推論集中的ベンチマークにわたって一貫した汎化改善を示しています。これらの結果は、MSSRが複雑な多モーダル推論タスクにおける安定でサンプル効率的かつ効果的なRLVRを可能にすることを示しています。コードとチェックポイントは受理後にリリースされます。
</details>

<details>
<summary> 英語要旨 </summary>

Reinforcement Learning with Verifiable Rewards (RLVR) has become a key paradigm to improve the reasoning capabilities of Multimodal Large Language Models (MLLMs). However, prevalent group-based algorithms such as GRPO require multi-rollout sampling for each prompt. While more efficient single-rollout variants have recently been explored in text-only settings, we find that they suffer from severe instability in multimodal contexts, often leading to training collapse. To address this sample efficiency-stability trade-off, we introduce $\textbf{MSSR}$ (Multimodal Stabilized Single-Rollout), a group-free RLVR framework that achieves both stable optimization and effective multimodal reasoning performance. MSSR achieves this via an entropy-based advantage-shaping mechanism that adaptively regularizes advantage magnitudes, preventing collapse and maintaining training stability. While such mechanisms have been used in group-based RLVR, we show that in the multimodal single-rollout setting they are not merely beneficial but essential for stability. In in-distribution evaluations, MSSR demonstrates superior rollout sample efficiency, achieving similar validation accuracy with half the training steps. When trained for the same number of steps, MSSR's performance surpasses the group-based baseline and shows consistent generalization improvements across five diverse reasoning-intensive benchmarks. Together, these results demonstrate that MSSR enables stable, sample-efficient, and effective RLVR for complex multimodal reasoning tasks. We will release code and checkpoints upon acceptance.
</details>

---

### Order Matters: 3D Shape Generation from Sequential VR Sketches
著者: Yizi Chen, Sidi Wu, Tianyi Xiao, Nina Wiedemann, Loic Landrieu

<details>
<summary> 日本語要旨 </summary>

VRスケッチングは、従来のCADソフトウェアに比べてより速く直感的な代替手段を提供し、ユーザーが3Dで直接アイデアを探索・反復することを可能にします。しかし、既存のスケッチから形状へのモデルは、ストロークの時間的順序を無視し、構造や設計意図に関する重要な手がかりを捨てています。私たちは、VRSketch2Shapeを提案します。これは、連続したVRスケッチから3D形状生成のための初めてのフレームワークおよびマルチカテゴリデータセットです。私たちの貢献は三つあります：（i）任意の形状から順序付けられたVRスケッチを自動生成するパイプライン、（ii）4カテゴリにわたる20,000以上の合成および900の手描きスケッチ・形状ペアからなるデータセット、（iii）順序を考慮したスケッチエンコーダーと拡散ベースの3Dジェネレーター。私たちのアプローチは、以前の研究よりも幾何学的な忠実度が高く、最小限の監督で合成から現実のスケッチへ効果的に一般化します。すべてのデータとモデルはオープンアクセスで公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

VR sketching lets users explore and iterate on ideas directly in 3D, offering a faster and more intuitive alternative to conventional CAD software. However, existing sketch-to-shape models ignore the temporal ordering of strokes, discarding crucial cues about structure and design intent. We introduce VRSketch2Shape, the first framework and multi-category dataset for 3D shape generation from sequential VR sketches. Our contributions are threefold: (i) an automated pipeline that generates ordered VR sketches from arbitrary shapes, (ii) a dataset comprising over 20k synthetic and 900 hand-drawn sketch–shape pairs across four categories, and (iii) an order-aware sketch encoder coupled with a diffusion-based 3D generator. Our approach yields higher geometric fidelity than prior work and generalizes effectively from synthetic to real sketches with minimal supervision. All data and models will be released in open access.
</details>

---

### V$^{2}$-SAM: Marrying SAM2 with Multi-Prompt Experts for Cross-View Object Correspondence
著者: Jiancheng Pan, Runze Wang, Tianwen Qian, Mohammad Mahdi, Yanwei Fu, Xiangyang Xue, Xiaomeng Huang, Luc Van Gool, Danda Paudel, Yuqian Fu

<details>
<summary> 日本語要旨 </summary>

エゴ・エクソオブジェクト対応を例に挙げると、異なる視点（例えば、エゴセントリックおよびエクソセントリック）間で同一のオブジェクトに対する一貫した関連付けを確立しようとするクロスビューオブジェクト対応は、大きな視点や外見の変化により重要な課題が存在します。このため、SAM2のような既存のセグメンテーションモデルを直接適用することは容易ではありません。これに対処するため、私たちはクロスビュー対応を単一ビューのセグメンテーションからSAM2へと適応させる統合的なフレームワークであるV²-SAMを提案します。これは、二つの補完的なプロンプトジェネレータによって実現されます。具体的には、DINOv3特徴に基づいて構築されたクロスビュー・アンカープロンプトジェネレータ（V²-Anchor）が幾何学的な対応を確立し、初めてSAM2のクロスビュー状況における座標ベースのプロンピングを可能にします。一方で、クロスビュー・ビジュアルプロンプトジェネレータ（V²-Visual）は、新しいビジュアルプロンプトマッチャーを通じて外見ガイド付きの手がかりを強化し、エゴ・エクソ表現を特徴と構造の両面から整合させます。これらのプロンプトの強みを効果的に活用するため、私たちはマルチエキスパート設計を採用し、環状一貫性に基づいて最も信頼できるエキスパートを選択するポストホックサイクリックコンシステンシーセレクター（PCCS）を導入します。広範な実験により、V²-SAMの有効性が検証され、Ego-Exo4D（エゴ・エクソオブジェクト対応）、DAVIS-2017（動画オブジェクト追跡）、HANDAL-X（ロボット向けクロスビュー対応）において新たな最先端の性能を達成しました。コードは受理後に公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Cross-view object correspondence, exemplified by the representative task of ego–exo object correspondence, aims to establish consistent associations of the same object across different viewpoints (e.g., ego-centric and exo-centric). This task poses significant challenges due to drastic viewpoint and appearance variations, making existing segmentation models, such as SAM2, non-trivial to apply directly. To address this, we present V$^{2}$-SAM, a unified cross-view object correspondence framework that adapts SAM2 from single-view segmentation to cross-view correspondence through two complementary prompt generators. Specifically, the Cross-View Anchor Prompt Generator (V$^{2}$-Anchor), built upon DINOv3 features, establishes geometry-aware correspondences and, for the first time, unlocks coordinate-based prompting for SAM2 in cross-view scenarios, while the Cross-View Visual Prompt Generator (V$^{2}$-Visual) enhances appearance-guided cues via a novel visual prompt matcher that aligns ego–exo representations from both feature and structural perspectives. To effectively exploit the strengths of both prompts, we further adopt a multi-expert design and introduce a Post-hoc Cyclic Consistency Selector (PCCS) that adaptively selects the most reliable expert based on cyclic consistency. Extensive experiments validate the effectiveness of V$^{2}$-SAM, achieving new state-of-the-art performance on Ego-Exo4D (Ego–Exo object correspondence), DAVIS-2017 (video object tracking), and HANDAL-X (robotic-ready cross-view correspondence). Codes will be released upon acceptance.
</details>

---

### Pushing The Frontier of Audiovisual Perception with Large-Scale Multimodal Correspondence Learning
著者: Apoorv Vyas, Heng-Jui Chang, Cheng-Fu Yang, Po-Yao Huang, Luya Gao, Julius Richter, Sanyuan Chen, Matthew Le, Piotr Dollár, Christoph Feichtenhofer, Ann Lee, Wei-Ning Hsu

<details>
<summary> 日本語要旨 </summary>

私たちは、スケーラブルな対比学習で訓練された新しいエンコーダーのファミリー、Perception Encoder-Audiovisual（PE-AV）を紹介します。これはPE\citep{pe}に基づき、音声と映像理解のための表現を拡張し、オーディオ–ビデオ、オーディオ–テキスト、ビデオ–テキストのモダリティ間でネイティブに統合された埋め込みをサポートすることが主な貢献です。PE-AVの統一的なクロスモーダル埋め込みは、音声検索のような新しいタスクを可能にし、標準的なオーディオおよびビデオベンチマークで新たな基準を設定します。これを実現するために、高品質のキャプションをO(100M)のオーディオ–ビデオペアに合成する強力なオーディオビジュアルデータエンジンを構築しました。これにより、モダリティ間で一貫した大規模な監督が可能となります。私たちの音声データにはスピーチ、音楽、および一般的なサウンドエフェクトが含まれており、これにより以前の研究で見られる単一ドメインの制限を回避しています。私たちは10種類のペアワイズ対比目的を利用し、クロスモーダリティおよびキャプションタイプのペアを拡大することで整列が強化され、ゼロショットパフォーマンスが向上することを示しています。私たちのモデルとコードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

We introduce Perception Encoder-Audiovisual, PE-AV, a new family of encoders for audio and video understanding trained with scaled contrastive learning. Built on PE~\citep{pe}, PE-AV makes several key contributions to extend representations to audio, and natively support joint embeddings across audio–video, audio–text, and video–text modalities. PE-AV's unified cross-modal embeddings enable novel tasks such as speech retrieval, and set a new state of the art across standard audio and video benchmarks. We unlock this by building a strong audiovisual data engine that synthesizes high-quality captions for O(100M) audio–video pairs, enabling large-scale supervision consistent across modalities. Our audio data includes speech, music, and general sound effects—avoiding single-domain limitations common in prior work. We exploit ten pairwise contrastive objectives, showing that scaling cross-modality and caption-type pairs strengthens alignment and improves zero-shot performance. Our models and code will be available.
</details>

---

### APPO: Attention-guided Perception Policy Optimization for Video Reasoning
著者: Henghui Du, Chang Zhou, Xi Chen, Di Hu

<details>
<summary> 日本語要旨 </summary>

実際には、複雑なビデオ推論は細部までの知覚に過度に依存しており、専門的（例えば、博士号レベル）な推論よりもそちらを重視しています。広範囲にわたる実証観察を通じて、知覚の重要性が認識されました。特に、知覚能力がほぼ一定である場合、Qwen3-8BからOpenAI-o3への推論強化はパフォーマンス改善率がわずか0.7%しかありません。対照的に、知覚モデルのスケールを7Bから32Bに少し変更するだけでパフォーマンスが1.4%向上し、これは推論よりも知覚を強化することがパフォーマンス改善においてより重要であることを示しています。したがって、高価な細部までの注釈情報を必要とせずに推論を通じて知覚能力を向上させる方法を探求することは有益です。この目標を達成するために、私たちはAPPO（Attention-guided Perception Policy Optimizationアルゴリズム）を特別に提案します。これはトークンレベルの密な報酬を利用してモデルの細部までの知覚能力を向上させます。APPOの核心的な考え方は、同じ重要なビデオフレームに主に焦点を当てる異なる応答からのトークン（これを「インターグループ知覚トークン」と呼びます）を最適化することです。多様なビデオベンチマークおよび異なるスケールのモデル（3/7B）に関する実験結果は、APPOが一貫してGRPOやDAPO（0.5% ~ 4%）を上回っていることを示しています。私たちは、多様なシナリオや要求に対応する低コストで効果的にモデルの知覚能力を向上させる有望なアプローチを提供したいと考えています。
</details>

<details>
<summary> 英語要旨 </summary>

Complex video reasoning, actually, relies excessively on fine-grained perception rather than on expert (e.g., Ph.D, Science)-level reasoning. Through extensive empirical observation, we have recognized the critical impact of perception. In particular, when perception ability is almost fixed, enhancing reasoning from Qwen3-8B to OpenAI-o3 yields only 0.7% performance improvement. Conversely, even minimal change in perception model scale (from 7B to 32B) boosts performance by 1.4%, indicating enhancing perception, rather than reasoning, is more critical to improve performance. Therefore, exploring how to enhance perception ability through reasoning without the need for expensive fine-grained annotation information is worthwhile. To achieve this goal, we specially propose APPO, the Attention-guided Perception Policy Optimization algorithm that leverages token-level dense rewards to improve model's fine-grained perception. The core idea behind APPO is to optimize those tokens from different responses that primarily focus on the same crucial video frame (called intra-group perception tokens). Experimental results on diverse video benchmarks and models with different scales (3/7B) demonstrate APPO consistently outperforms GRPO and DAPO (0.5% ~ 4%). We hope our work provides a promising approach to effectively enhance model's perception abilities through reasoning in a low-cost manner, serving diverse scenarios and demands.
</details>

---

### Beyond Single-View Sufficiency: CVBench for Cross-View Human Understanding
著者: Tianchen Guo, Chen Liu, Xin Yu

<details>
<summary> 日本語要旨 </summary>

人間の社会環境に対する認識は、本質的に多視点合成問題であり、空間と時間をまたいで補完的かつしばしば遮蔽された情報を統合する必要があります。しかし、既存のマルチモーダル大規模言語モデル（MLLMs）に関する基準は、「十分な視点」仮定に基づいており、単一視点パターン認識を報酬とし、クロスビューフュージョンの評価を怠っています。この重要なギャップに対処するために、私たちは**CVBench**を導入します。これは、クロスビュー人間理解のための大規模かつマルチタスク基準です。CVBenchは、12の空間的および時間的タスクにわたる3,000の挑戦的な質問から構成されており、各アイテムは*verifiable single-view insufficiency*を設計しており、モデルが曖昧さを解決するために異なる証拠を合成することを義務付けています。最先端のオープンソースおよびクローズドソースMLLMs（InternVLからGemini 2.5 Proまで）に対する包括的な評価では、大きなパフォーマンスギャップが明らかになりました。最良のモデル（例えば、Gemini 2.5 Pro、空間精度約42%）は、人間のパフォーマンス（約94%）からほぼ50ポイント下回っています。私たちはすべてのモデルにおけるシステマティックな失敗メカニズムを特定しました：「Single-View Bias」と呼ばれる支配的なバイアスで、モデルは矛盾する証拠を無視し、最も自信のあるが誤った単一視点予測にデフォルトします。これは、現在のMLLMsが幾何学的な根拠付け、アイデンティティの持続性、真の空間時間フュージョンといった基本的なメカニズムを欠いていることを示しています。CVBenchは、クロスビュー認識能力を備えた次世代アーキテクチャの開発を促進するための厳格な診断フレームワークを提供します。
</details>

<details>
<summary> 英語要旨 </summary>

Human perception of social environments is inherently a multi-view synthesis problem, requiring the integration of complementary and often occluded information across space and time. However, existing benchmarks for Multimodal Large Language Models (MLLMs) are overwhelmingly predicated on a "sufficient-view" assumption, rewarding single-view pattern recognition while failing to evaluate cross-view fusion. To address this critical gap, we introduce \textbf{CVBench}, a large-scale, multi-task benchmark for cross-view human understanding. CVBench comprises 3,000 challenging questions across 12 spatial and temporal tasks, where every item is designed with \textit{verifiable single-view insufficiency}, mandating that models synthesize disparate evidence to resolve ambiguities. Our comprehensive evaluation of state-of-the-art open and closed-source MLLMs (from InternVL to Gemini 2.5 Pro) reveals a substantial performance gap, with the best models (e.g., Gemini 2.5 Pro, $\sim$42\% spatial accuracy) falling nearly 50 points behind human performance ($\sim$94\%). We identify a systemic failure mechanism across all models: a dominant "Single-View Bias," whereby models ignore conflicting evidence and default to the most confident but incorrect single-view prediction. This demonstrates that current MLLMs lack the fundamental mechanisms for geometric grounding, identity persistence, and true spatio-temporal fusion. CVBench provides a rigorous diagnostic framework to catalyze the development of next-generation, cross-view–aware architectures.
</details>

---

### X-Part: High Fidelity And Structure Coherent Shape Decomposition And Completion
著者: XINHAO YAN, Jiachen Xu, Yang Li, Changfeng Ma, Yunhan Yang, Chunshi Wang, Zibo Zhao, Zeqiang Lai, Yunfei Zhao, Zhuo Chen, Chunchao Guo

<details>
<summary> 日本語要旨 </summary>

3D形状の部品レベルでの生成は、メッシュリトポロジー、UVマッピング、3Dプリントなどの下流アプリケーションにおいて重要です。しかし、既存の部品ベースの生成方法は十分な制御性を欠き、意味的に有意義な分解が難しいという問題があります。このため、私たちはX-Partを提案します。これは、高い幾何学的忠実度でセマンティックに意味のある構造的に一貫した部品に全体の3Dオブジェクトを分解することが可能な制御可能な生成モデルです。X-Partは、部品生成のためのプロンプトとしてバウンディングボックスを利用し、意味的に有意義な分解のために点ごとのセマンティック特徴を注入します。さらに、インタラクティブな部品生成のための編集可能なパイプラインを設計しました。広範な実験結果は、X-Partが部品レベルでの形状生成において最先端の性能を達成していることを示しています。この研究は、生産準備が整った、編集可能で構造的に安定した3Dアセットを作成する新しいパラダイムを確立します。コードは公開研究のためにリリースされます。
</details>

<details>
<summary> 英語要旨 </summary>

Generating 3D shapes at part level is pivotal for downstream applications such as mesh retopology, UV mapping, and 3D printing. However, existing part-based generation methods often lack sufficient controllability and suffer from poor semantically meaningful decomposition. To this end, we introduce X-Part, a controllable generative model designed to decompose a holistic 3D object into semantically meaningful and structurally coherent parts with high geometric fidelity. X-Part exploits the bounding box as prompts for the part generation and injects point-wise semantic features for meaningful decomposition. Furthermore, we design an editable pipeline for interactive part generation. Extensive experimental results show that X-Part achieves state-of-the-art performance in part-level shape generation. This work establishes a new paradigm for creating production-ready, editable, and structurally sound 3D assets. Codes will be released for public research.
</details>

---

### PE3R: Perception-Efficient 3D Reconstruction
著者: Jie Hu, Shizun Wang, Xinchao Wang

<details>
<summary> 日本語要旨 </summary>

最近の2次元から3次元への認識技術の進歩により、ポーズがない画像から3次元シーンセマンティクスを復元することが可能になりました。しかし、現在の方法は一般化性能が限られており、シーンごとの最適化や視点間でのセマンティック不整合に依存していることが多いです。これらの制約を解決するために、調整なしで効率的かつ一般化可能な3次元セマンティック再構築フレームワークであるPE3Rを提案します。多視点幾何学と2Dセマンティック事前知識を統合したフィードフォワードパイプラインにより、PE3Rはシーン固有の微調整なしでさまざまなシーンやオブジェクトカテゴリーに対してゼロショット一般化を達成します。開放的な用語セグメンテーションとマルチビュー深度推定の広範な評価では、PE3Rが最大で9倍速い推論を実現するだけでなく、セマンティックおよび幾何学的メトリクスにおいて新たな最先端の精度を達成していることが示されました。このアプローチは、拡張可能で言語駆動型の3次元シーン理解への道を開きます。再現性のためにコードは補足資料で公開しています。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advances in 2D-to-3D perception have enabled the recovery of 3D scene semantics from unposed images. However, prevailing methods often suffer from limited generalization, reliance on per-scene optimization, and semantic inconsistencies across viewpoints. To address these limitations, we introduce PE3R, a tuning-free framework for efficient and generalizable 3D semantic reconstruction. By integrating multi-view geometry with 2D semantic priors in a feed-forward pipeline, PE3R achieves zero-shot generalization across diverse scenes and object categories without any scene-specific fine-tuning. Extensive evaluations on open-vocabulary segmentation and multi-view depth estimation show that PE3R not only achieves up to 9$\times$ faster inference but also sets new state-of-the-art accuracy in both semantic and geometric metrics. Our approach paves the way for scalable, language-driven 3D scene understanding. Code is available in supplementary material for reproducibility.
</details>

---

### Efficient and High-Fidelity Omni Modality Retrieval
著者: Chuong Huynh, Manh Luong, Abhinav Shrivastava

<details>
<summary> 日本語要旨 </summary>

マルチモーダル検索は、異なるモダリティからのクエリ情報を集約して目的のターゲットを取得する作業です。最先端のマルチモーダル検索モデルは複雑なクエリを理解できますが、通常は2つのモダリティ（テキストとビジョン）に限定されています。この制約は、3つ以上のモダリティを組み合わせたクエリを理解する普遍的な検索システムの開発を妨げます。この目標に向けて進展するため、私たちはテキスト、ビジョン、オーディオという3つの主要モダリティをまたいだ複雑な組み合わせクエリを処理できる初の検索モデル、OmniRetを提案します。私たちのOmniRetモデルは、普遍的検索における2つの重要な課題、計算効率と表現忠実度に対処しています。まず、モダリティ固有エンコーダから生成された巨大なトークンシーケンスを大規模言語モデル（LLM）に供給することは計算効率が悪いです。そのため、これらのシーケンスからコンパクトで固定サイズの表現を生成するための注意力ベースのリサンプリングメカニズムを導入します。この共有モジュールは、表現多様性と汎用化能力を維持しつつ、モダリティ固有情報に敏感であるよう設計されています。次に、豊富なオムニモーダルデータを単一の埋め込みベクトルに圧縮することは必然的に情報損失を引き起こし、細部が失われます。これらの細かい詳細を保持するために、Attention Sliced Wasserstein Poolingを提案します。これにより改善されたオムニモーダル表現が得られます。OmniRetは、30のデータセットにまたがる約600万組のクエリターゲットペアの集合でトレーニングされています。私たちは13の検索タスクとMMEBv2サブセットでモデルをベンチマークしました。私たちのモデルは、組み合わせクエリ、オーディオおよびビデオ検索タスクにおいて顕著な改善を示していますが、他のタスクでは最先端モデルと同等の性能を達成しています。さらに、新しいオーディオセントリックマルチモーダルベンチマーク（ACM）を編纂します。この新しいベンチマークは、組み合わせオーディオ検索とオーディオビジュアル検索の2つの重要な、これまで欠けていたタスクを導入し、モデルのオムニモーダル埋め込み能力をより包括的に評価することが可能です。私たちはこのベンチマークが普遍的検索システムの開発を促進すると考えています。
</details>

<details>
<summary> 英語要旨 </summary>

Multimodal retrieval is the task of aggregating information from queries across heterogeneous modalities to retrieve desired targets. State-of-the-art multimodal retrieval models can understand complex queries, yet they are typically limited to two modalities: text and vision. This limitation impedes the development of universal retrieval systems capable of comprehending queries that combine more than two modalities. To advance toward this goal, we present OmniRet, the first retrieval model capable of handling complex, composed queries spanning three key modalities: text, vision, and audio. Our OmniRet model addresses two critical challenges for universal retrieval: computational efficiency and representation fidelity. First, feeding massive token sequences from modality-specific encoders to Large Language Models (LLMs) is computationally inefficient. We therefore introduce an attention-based resampling mechanism to generate compact, fixed-size representations from these sequences. This shared module is designed to maintain representational diversity and generalization capabilities while remaining sensitive to modality-specific information. Second, compressing rich omni-modal data into a single embedding vector inevitably causes information loss and discards fine-grained details. We propose Attention Sliced Wasserstein Pooling to preserve these fine-grained details, leading to improved omni-modal representations. OmniRet is trained on an aggregation of approximately 6 million query-target pairs spanning 30 datasets. We benchmark our model on 13 retrieval tasks and a MMEBv2 subset. Our model demonstrates significant improvements on composed query, audio and video retrieval tasks, while achieving on-par performance with state-of-the-art models on others. Furthermore, we curate a new Audio-Centric Multimodal Benchmark (ACM). This new benchmark introduces two critical, previously missing tasks—composed audio retrieval and audio-visual retrieval—to more comprehensively evaluate a model's omni-modal embedding capacity. We believe our benchmark will facilitate the development of universal retrieval systems.
</details>

---

### OnlinePG: Online Open-Vocabulary Panoptic Mapping with 3D Gaussian Splatting
著者: Hongjia Zhai, Qi Zhang, Xiaokun Pan, Xiyu Zhang, Yitong Dong, Huaqi Zhang, Dan Xu, Guofeng Zhang

<details>
<summary> 日本語要旨 </summary>

オープンボキャブラリーのシーン理解とオンラインパノプティックマッピングは、エージェントが環境を認識し対話するために不可欠です。しかし、既存の方法は主にオフラインであるか、インスタンスレベルの理解が欠けており、実世界のロボットタスクへの適用性が制限されています。本論文では、3Dガウシアンスプラッティングをオンライン設定で統合することにより、幾何学的再構築とオープンボキャブラリー認識を組み合わせた新しい効果的なシステムであるOnlinePGを提案します。技術的には、オンラインパノプティックマッピングを達成するために、効率的なローカル・トゥ・グローバルのパラダイムとスライディングウィンドウを採用します。ローカル一貫性マップを構築するために、幾何学的およびセマンティックな手がかりを共同で活用した3Dセグメントクラスタリンググラフを構築し、スライディングウィンドウ内の不整合なセグメントを完全なインスタンスに融合します。その後、ローカル3Dガウシアンマップの明示的な空間属性グリッドを構築し、堅牢な双方向二部グラフィックインスタンスマッチングを介してそれらをグローバルマップに融合します。最後に、3D空間属性グリッド内の融合されたVLM特徴を利用してオープンボキャブラリーのシーン理解を達成します。広く使用されているデータセットでの包括的な実験により、私たちの方法がオンラインアプローチの中で優れた性能を示しており、リアルタイム効率も維持されていることが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

Open-vocabulary scene understanding with online panoptic mapping is essential for embodied applications to perceive and interact with environments. However, existing methods are predominantly offline or lack instance-level understanding, limiting their applicability to real-world robotic tasks. In this paper, we propose OnlinePG, a novel and effective system that integrates geometric reconstruction and open-vocabulary perception using 3D Gaussian Splatting in an online setting. Technically, to achieve online panoptic mapping, we employ an efficient local-to-global paradigm with a sliding window. To build local consistency map, we construct a 3D segment clustering graph that jointly leverages geometric and semantic cues, fusing inconsistent segments within sliding window into complete instances. Subsequently, to update the global map, we construct explicit spatial attribute grids for the local 3D Gaussian map and fuse them into the global map via robust bidirectional bipartite 3D Gaussian instance matching. Finally, we utilize the fused VLM features inside the 3D spatial attribute grids to achieve open-vocabulary scene understanding. Extensive experiments on widely used datasets demonstrate that our method achieves better performance among online approaches, while maintaining real-time efficiency.
</details>

---

### Downscaling Intelligence: Exploring Perception and Reasoning Bottlenecks in Small Multimodal Models
著者: Mark Endo, Serena Yeung

<details>
<summary> 日本語要旨 </summary>

多様なモーダルモデルのスケールアップは視覚理解と推論において顕著な進歩をもたらしましたが、実用的な要求はより小さく効率的なシステムを必要としています。本研究では、多様モーダルモデルにおける知能のダウンスケーリングについて体系的な分析を行い、大規模言語モデル（LLM）の容量削減が多様モーダル能力にどのように影響するかを検討します。初期の結果は興味深い傾向を示しています：LLMのダウンスケーリングが視覚的な能力に不釣り合いに影響を与えることが多く、LLMから受け継がれた能力よりもそちらに偏っています。この低下は主に予想される視覚的推論の衰退を反映しているのか、それともより基本的な知覚能力の喪失を示しているのかを検証します。LLMダウンスケーリングが知覚に与える影響を隔離することで、パフォーマンスは依然として急激に低下し、推論への影響を匹敵または上回ることが多いことがわかりました。このボトルネックに対処するために、私たちは視覚抽出チューニングを導入し、モデルがタスク全体で指示に関連する視覚的詳細を一貫して抽出するように明示的にトレーニングします。これらの抽出された視覚的詳細を用いて、ステップバイステップで推論を行い答えを生成します。これらの要素が組み合わさって私たちのExtract+Thinkアプローチを形成し、この分野における効率性とパフォーマンスの新基準を設定しています。
</details>

<details>
<summary> 英語要旨 </summary>

Scaling up multimodal models has enabled remarkable advances in visual understanding and reasoning, but practical demands call for smaller, efficient systems. In this work, we conduct a principled analysis of downscaling intelligence in multimodal models, examining how reduced large language model (LLM) capacity affects multimodal capabilities. Our initial findings reveal an interesting trend: LLM downscaling disproportionately affects visual capabilities, rather than abilities inherited from the LLM. We then examine whether this drop mainly reflects the expected decline in visual reasoning or a more fundamental loss of perceptual abilities. Isolating the effect of LLM downscaling on perception, we find performance still drops sharply, often matching or exceeding the impact on reasoning. To address this bottleneck, we introduce visual extraction tuning, which explicitly trains the model to extract instruction-relevant visual details consistently across tasks. With these extracted visual details, we then apply step-by-step reasoning to generate answers. Together, these components form our Extract+Think approach, setting a new standard for efficiency and performance in this space.
</details>

---

### Adaptive Action Chunking at Inference-time for Vision-Language-Action Models
著者: Yuanchang Liang, Xiaobo Wang, Kai Wang, Shuo Wang, Xiaojiang Peng, Haoyu Chen, David Chua, Prahlad Vadakkepat

<details>
<summary> 日本語要旨 </summary>

ビジョン言語行動（VLA）モデルにおいて、アクションチャンキング（すなわち、中間再計画をせずに一連のアクションを実行すること）はロボット操作能力を向上させるための重要な技術です。しかし、大きなチャンクサイズは新しい情報へのモデルの反応性を低下させますが、小さいものではモードジャンピング（異なるチャンク間の不連続によって生じるガタつき）の可能性が高まります。したがって、モデルの反応性と一貫性をバランスさせるために最適なチャンクサイズを選択することは急務です。残念ながら、現在のVLAモデルの主流は推論時に固定された経験的なチャンク長を採用しており、多様な操作タスクにわたるその優位性と拡張性が制限されています。この問題に対処するため、私たちはアクションエントロピーを手掛かりとして現在の予測に基づいて適応的にチャンクサイズを決定する新しい適応型アクションチャンキング（AAC）戦略を提案します。広範なシミュレーションおよび実世界のロボット操作タスクにわたる詳細な実験は、私たちのアプローチが最先端の代替手段を大幅に上回るパフォーマンス向上を示しています。ビデオとソースコードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

In Vision-Language-Action (VLA) models, action chunking (i.e., executing a sequence of actions without intermediate replanning) is a key technique to improve robotic manipulation abilities. However, a large chunk size reduces the model’s responsiveness to new information, while a small one increases the likelihood of mode-jumping, jerky behavior resulting from discontinuities between chunks. Therefore, selecting the optimal chunk size is an urgent demand to balance the model's reactivity and consistency. Unfortunately, a dominant trend in current VLA models is an empirical fixed chunk length at inference-time, hindering their superiority and scalability across diverse manipulation tasks. To address this issue, we propose a novel Adaptive Action Chunking (AAC) strategy, which exploits action entropy as the cue to adaptively determine the chunk size based on current predictions. Extensive experiments on a wide range of simulated and real-world robotic manipulation tasks have demonstrated that our approach substantially improves performance over the state-of-the-art alternatives. The videos and source code will be made publicly available.
</details>

---

### ChArtist: Generating Pictorial Charts with Unified Spatial and Subject Control
著者: Shishi Xiao, Tongyu Zhou, David H. Laidlaw, Gromit Yeuk-Yin Chan

<details>
<summary> 日本語要旨 </summary>

ピクトグラムチャートは、視覚要素とデータチャートをシームレスに統合することで効果的なビジュアルストーリーテリングの手段です。しかし、このような画像を作成することは難しいです。視覚要素の柔軟性がチャート構造の硬直性としばしば衝突するためです。その結果、データの忠実さと視覚的美学を維持する創造的な変形が必要になります。現在の方法では、自然画像から密度の高い構造的手掛かり（例えば、エッジや深度マップ）を抽出しますが、これらはピクトグラムチャート生成における条件信号として適していません。私たちは、自動的にピクトグラムチャートを生成するドメイン固有の方法であるChArtistを提案します。これは2つの異なるタイプの制御を提供します：1) チャート構造とよく一致する空間制御、および2) 参照画像の視覚的特性を尊重する主題駆動型制御。これを達成するために、スケルトンベースの空間制御表現を導入します。この表現はチャートのデータエンコーディング情報のみを符号化し、参照ビジュアルを容易に組み込むことができるため、厳格な輪郭制約はありません。私たちの方法はDiffusion Transformer（DiT）に基づいて実装され、この2つの制御を管理するために適応位置符号化メカニズムを活用しています。さらに、空間制御と主題制御の相互作用を調整するためにSpatially Gated Attentionを導入します。このタスクのために事前学習モデルを微調整するサポートとして、30,000トリプレット（骨格、参照画像、ピクトグラムチャート）からなる大規模データセットを作成しました。また、生成されたチャートのデータ忠実性を評価する統一的なデータ精度メトリックを提案します。この研究は、現在のジェネラティブモデルがタスク固有の表現に移行することで、データ駆動型のビジュアルストーリーテリングを達成できることを示しています。コードとデータセットは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

A pictorial chart is an effective medium for visual storytelling, seamlessly integrating visual elements with data charts. However, creating such images is challenging because the flexibility of visual elements often conflicts with the rigidity of chart structures. This process thus requires a creative deformation that maintains both data faithfulness and visual aesthetics. Current methods that extract dense structural cues from natural images (e.g., edge or depth maps) are ill-suited as conditioning signals for pictorial chart generation. We present ChArtist, a domain-specific method for generating pictorial charts automatically, offering two distinct types of control: 1) spatial control that aligns well with the chart structure, and 2) subject-driven control that respects the visual characteristics of a reference image. To achieve this, we introduce a skeleton-based spatial control representation. This representation encodes only the data-encoding information of the chart, allowing for the easy incorporation of reference visuals without a rigid outline constraint. We implement our method based on the Diffusion Transformer (DiT) and leverage an adaptive position encoding mechanism to manage these two controls. We further introduce Spatially Gated Attention to modulate the interaction between spatial control and subject control. To support the fine-tuning of pre-trained models for this task, we created a large-scale dataset of 30,000 triplets (skeleton, reference image, pictorial chart). We also propose a unified data accuracy metric to evaluate the data faithfulness of the generated charts. We believe this work demonstrates that current generative models can achieve data-driven visual storytelling by moving beyond general-purpose conditions to task-specific representations. The code and dataset will be released.
</details>

---

### Photo-Guided Tooth Segmentation on 3D Oral Scan Model
著者: Shaojie Zhuang, Guangshun Wei, Jiangxin He, Yuanfeng Zhou

<details>
<summary> 日本語要旨 </summary>

デジタル歯科、矯正分析、臨床シミュレーションにおいては、正確な3次元歯のセグメンテーションが基本的です。口腔内スキャン（IOS）モデルはしばしば不完全または信頼性の低いテクスチャ情報を持っており、歯と歯肉の微細な境界線を描くことが難しいです。一方で、2次元口腔内画像は豊富な意味的および色彩情報を提供し、3D幾何学に補完することができます。このため、私たちは新しい写真ガイド付き3次元モデル歯セグメンテーションフレームワーク、PMTSegを提案します。これは口腔内写真からのテクスチャ手がかりを統合することで3D歯のセグメンテーションを強化します。私たちのフレームワークには、画像-モデル登録の正確性を高めるカメラアライメントモジュール（CAM）、適応的なマルチビュー特徴選択のための機能フィルタリングゲート（FFG）、テクスチャ-幾何学対応を学習する一貫した特徴学習（CFL）メカニズムという3つの重要なコンポーネントが導入されています。私たちの方法は任意の数およびビューの口腔内写真をサポートします。実験結果によると、隣接する歯や歯-歯肉境界線を区別する点で顕著な改善が示されており、これは口腔内写真が3Dスキャンの効率的かつ意味的に豊富な補完として正確な歯科セグメンテーションに役立つことを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Accurate 3D tooth segmentation is fundamental for digital dentistry, orthodontic analysis, and clinical simulation. Intraoral scan (IOS) models often suffer from incomplete or unreliable texture information, making it difficult to delineate fine boundaries between teeth and gingiva, while 2D intraoral images provide rich semantic and chromatic information that can complement 3D geometry. Thus, we propose a novel Photo-guided 3D Model Tooth Segmentation framework, PMTSeg, that enhances 3D tooth segmentation by integrating texture cues from intraoral photos. Our framework introduces three key components: a Camera Alignment Module (CAM) for accurate image-model registration, a Feature Filtering Gate (FFG) for adaptive multi-view feature selection, and a Consistent Feature Learning (CFL) mechanism for learning texture-geometry correspondence. Our method supports arbitrary numbers and views of intraoral photos. Experiments show significant improvements in distinguishing adjacent teeth and tooth–gingiva boundaries, demonstrating that intraoral photographs serve as an efficient, semantically rich supplement to 3D scans for precise dental segmentation.
</details>

---

### Counterfactual VLA: Self-Reflective Vision-Language-Action Model with Adaptive Reasoning
著者: Zhenghao Peng, Wenhao Ding, Yurong You, Yuxiao Chen, Wenjie Luo, Thomas Tian, Yulong Cao, Apoorva Sharma, Danfei Xu, Boris Ivanovic, Boyi Li, Yan Wang, Marco Pavone

<details>
<summary> 日本語要旨 </summary>

最近の推論強化されたビジョン言語行動（VLA）モデルは、エンドツーエンドの自律運転における解釈可能性を向上させるために中間推論トレースを生成しています。しかし、これらのモデルは主に自分が何を認識し、どう行動するつもりかを記述し、計画されたアクションが安全で適切かどうかをほとんど疑問視しません。本研究では、自己反省的なVLAフレームワークである対事実VLA（CF-VLA）を紹介します。これにより、モデルは実行前に計画されたアクションを考慮し、修正することが可能になります。CF-VLAはまず、運転意図を要約した時間セグメント化されたメタアクションを生成し、その後、メタアクションおよび視覚情報の両方に条件付けられた対事実推論パスを行います。この手順では潜在的な結果をシミュレートし、危険な振る舞いを特定し、最終的な軌道生成を導く修正されたメタアクションを出力します。このような自己反省能力を効率的に得るために、我々は基本（非対事実）VLAのロールアウトから高価値シーンを採掘し、後続の対事実学習ラウンド用に対事実推論トレースをラベル付けするためのロールアウト–フィルタリング–ラベリングパイプラインを提案します。大規模な運転データセットにおける実験では、CF-VLAが最大17.6％の軌道精度向上、安全性指標の強化、そして適応的思考（対事実推論を難しいシナリオでのみ有効にする）を示しています。推論トレースを一発記述から因果的自己修正信号へと変換することで、CF-VLAは行動前に考える学習能力を持つ自己反省型の自律運転エージェントに向けた一歩を進めます。
</details>

<details>
<summary> 英語要旨 </summary>

Recent reasoning-augmented Vision-Language-Action (VLA) models have improved the interpretability of end-to-end autonomous driving by generating intermediate reasoning traces. Yet these models primarily describe what they perceive and intend to do, rarely questioning whether their planned actions are safe or appropriate. This work introduces Counterfactual VLA (CF-VLA), a self-reflective VLA framework that enables the model to reason about and revise its planned actions before execution. CF-VLA first generates time-segmented meta-actions that summarize driving intent, then performs a counterfactual reasoning pass conditioned on both the meta-actions and the visual. This step simulates potential outcomes, identifies unsafe behaviors, and outputs corrected meta-actions that guide the final trajectory generation. To efficiently obtain such self-reflection capabilities, we propose a rollout–filter–label pipeline that mines high-value scenes from a base (non-counterfactual) VLA's rollouts and labels counterfactual reasoning traces for subsequent counterfactual training rounds. Experiments on large-scale driving datasets show that CF-VLA improves trajectory accuracy by up to 17.6\%, enhances safety metrics, and exhibits adaptive thinking: it only enables counterfactual reasoning in challenging scenarios. By transforming reasoning traces from one-shot descriptions to causal self-correction signals, CF-VLA takes a step toward self-reflective autonomous driving agents that learn to think before they act.
</details>

---

### Material Magic Wand: Material-Aware Grouping of 3D Parts in Untextured Meshes
著者: Umangi Jain, Vladimir G. Kim, Matheus Gadelha, Igor Gilitschenski, Zhiqin Chen

<details>
<summary> 日本語要旨 </summary>

私たちは、無地のメッシュにおける材質認識部分グループ化の問題を提起します。多くの実世界の形状、例えば松ぼっくりの鱗や建物の窓などは、同じ材質を共有しつつ幾何学的変化を示す反復構造を含んでいます。このようなメッシュに材質を割り当てる際、これらの繰り返し部分は通常、一つずつ手作業で識別・選択する必要があり、これは面倒で時間がかかる作業です。この問題に対処するために、「Material Magic Wand」というツールを提案します。このツールでは、アーティストが推定された材質特性に基づいて部分グループを選択できます。一つの部分が選択されると、私たちのアルゴリズムは同じ材質を共有する可能性のある他のすべての部分を自動的に取得します。このアプローチの鍵となる要素は、各3D部分に対して局所幾何学および全体的なコンテキストを考慮した材質認識埋め込みを生成する部分エンコーダーです。私たちは、同じ材質の部分の埋め込みを近づけ、異なる材質のものを離すように訓練された監督付き対比損失でモデルを学習します。したがって、選択された部分の埋め込みに近い埋め込みを取得することで部分グループ化が実現可能です。このタスクをベンチマークするために、100形状および241の部分レベルクエリを含むキュレーションされたデータセットを導入します。私たちは広範な実験を通じて方法の有効性を検証し、インタラクティブな材質割り当てアプリケーションでその実用的価値を示します。
</details>

<details>
<summary> 英語要旨 </summary>

We introduce the problem of material-aware part grouping in untextured meshes. Many real-world shapes, such as scales of pinecones or windows of buildings, contain repeated structures that share the same material but exhibit geometric variations. When assigning materials to such meshes, these repeated parts often require piece-by-piece manual identification and selection, which is tedious and time-consuming. To address this, we propose Material Magic Wand, a tool that allows artists to select part groups based on their estimated material properties -- when one part is selected, our algorithm automatically retrieves all other parts likely to share the same material. The key component of our approach is a part encoder that generates a material-aware embedding for each 3D part, accounting for both local geometry and global context. We train our model with a supervised contrastive loss that brings embeddings of material-consistent parts closer while separating those of different materials;therefore, part grouping can be achieved by retrieving embeddings that are close to the embedding of the selected part. To benchmark this task, we introduce a curated dataset of 100 shapes with 241 part-level queries. We verify the effectiveness of our method through extensive experiments and demonstrate its practical value in an interactive material assignment application.
</details>

---

### InternData-A1: Pioneering High-Fidelity Synthetic Data for Pre-training Generalist Policy
著者: Yang Tian, Yuyin Yang, Yiman Xie, Zetao Cai, Xu Shi, Ning Gao, Hangxu Liu, Xuekun Jiang, Zherui Qiu, Feng Yuan, Yaping Li, Ping Wang, Junhao Cai, Jia Zeng, Hao Dong, Jiangmiao Pang

<details>
<summary> 日本語要旨 </summary>

最近の研究では、VLAモデルの汎化における実際のデータと合成データの寄与を探求しています。$\pi$-seriesモデルは大規模なリアルロボット事前学習の強力な効果を示しましたが、これまでに合成データは同様のスケールで比較可能な能力を示していませんでした。本論文では、最も強力な$\pi$-datasetと同等の性能でVLAモデルの事前学習に合成データだけが十分であることを初めて示し、大規模シミュレーションの重要な価値を明らかにしています。結果として得られたモデルは、いくつかの難易度の高いタスクで驚くほど強力なゼロショットのシム・トゥ・リアル転移を示します。私たちの合成データセットInternData-A1には、4つのエンボディメント、18のスキル、70のタスク、227のシーンを含む、剛体、可動部品、変形可能なオブジェクト、流体オブジェクト操作をカバーする6万3000以上の軌道と7,433時間が含まれています。これは高度に自律的で完全に分離された構成可能なシミュレーションパイプラインを通じて生成され、柔軟なタスク組み立て、長期間のスキル構成、および最小限の手動調整で異種エンボディメントを可能にします。$\pi_0$と同じアーキテクチャを使用してInternData-A1だけで完全に事前学習したモデルは、49のシミュレーションタスク、5つのリアルワールドタスク、および4つの長期間の器用なタスクにわたって公式$\pi_0$と同等であることが分かりました。私たちはデータセットと生成パイプラインをオープンソース化し、大規模ロボティックデータへのアクセス拡大およびエンバデッドAI研究におけるスケーラブルなデータ作成の障壁を低減することを目指します。
</details>

<details>
<summary> 英語要旨 </summary>

Recent work explores how real and synthetic data contribute to VLA model generalization. While the $\pi$-series model has shown the strong effectiveness of large-scale real-robot pre-training, synthetic data has not previously demonstrated comparable capability at scale. This paper provides the first evidence that synthetic data alone can match the performance of the strongest $\pi$-dataset in pre-training a VLA model, revealing the substantial value of large-scale simulation. The resulting model also exhibits surprisingly strong zero-shot sim-to-real transfer on several challenging tasks. Our synthetic dataset, InternData-A1, contains over 630k trajectories and 7,433 hours across 4 embodiments, 18 skills, 70 tasks, and 227 scenes, covering rigid, articulated, deformable, and fluid-object manipulation. It is generated through a highly autonomous, fully decoupled, and compositional simulation pipeline that enables flexible task assembly, long-horizon skill composition, and heterogeneous embodiments with minimal manual tuning. Using the same architecture as $\pi_0$, we pre-train a model entirely on InternData-A1 and find that it matches the official $\pi_0$ across 49 simulation tasks, 5 real-world tasks, and 4 long-horizon dexterous tasks. We will open-source both the dataset and the generation pipeline to broaden access to large-scale robotic data and to lower the barrier to scalable data creation for embodied AI research.
</details>

---

### PrITTI: Primitive-based Generation of Controllable and Editable 3D Semantic Urban Scenes
著者: Christina Ourania Tze, Daniel Dauner, Yiyi Liao, Dzmitry Tsishkou, Andreas Geiger

<details>
<summary> 日本語要旨 </summary>

既存の3次元セマンティック都市シーン生成手法は、主にボクセルベースの表現を用いており、これらは固定解像度であり、編集が難しく、密な形態ではメモリを大量に消費します。対照的に、私たちはコンパクトでセマンティックに意味のある3次元要素を用いて都市シーンを表現するプリミティブベースのパラダイムを提唱します。これらは操作や構成が容易です。このために、私たちはPrITTIという名前の潜在的なドリフトモデルを導入しました。これはベクトル化されたオブジェクトプリミティブとラスタライズされた地面表面を用いて、多様で制御可能かつ編集可能な3次元セマンティック都市シーンを生成します。このハイブリッド表現は、オブジェクトレベルおよび地面レベルの操作を容易にする構造化された潜在空間をもたらします。KITTI-360での実験では、プリミティブベースの表現がドリフト変換器の全能力を解放し、より低いメモリ要件、速い推論、およびボクセルベースの方法に比べて大幅な編集可能性で最先端の3次元シーン生成品質を達成しています。生成以外にも、PrITTIはシーン編集、インパイント、アウトパイント、およびフォトリアルなストリートビューシンセシスといった多様な下流応用をサポートします。
</details>

<details>
<summary> 英語要旨 </summary>

Existing approaches to 3D semantic urban scene generation predominantly rely on voxel-based representations, which are bound by fixed resolution, challenging to edit, and memory-intensive in their dense form. In contrast, we advocate for a primitive-based paradigm where urban scenes are represented using compact, semantically meaningful 3D elements that are easy to manipulate and compose. To this end, we introduce PrITTI, a latent diffusion model that leverages vectorized object primitives and rasterized ground surfaces for generating diverse, controllable, and editable 3D semantic urban scenes. This hybrid representation yields a structured latent space that facilitates object- and ground-level manipulation. Experiments on KITTI-360 show that primitive-based representations unlock the full capabilities of diffusion transformers, achieving state-of-the-art 3D scene generation quality with lower memory requirements, faster inference, and greater editability than voxel-based methods. Beyond generation, PrITTI supports a range of downstream applications, including scene editing, inpainting, outpainting, and photo-realistic street-view synthesis.
</details>

---

### Foca-VLA: Unleashing Hybrid Force-Position Control with Force Awareness for Contact-Rich Manipulation
著者: Yang Li, Zhaxizhuoma Zhaxizhuoma, Hongru Jiang, Junjie Xia, Hongquan Zhang, Jinda Du, Yunsong Zhou, Jia Zeng, Ce Hao, Jieji Ren, Qiaojun Yu, Cewu Lu, Yu Qiao, Jiangmiao Pang

<details>
<summary> 日本語要旨 </summary>

接触豊富な操作における具現化された知能は、主に位置制御を依存してきましたが、相互作用力の明示的な認識と規制は未だ十分に探求されていません。これにより、実世界のタスクでの安定性、精度、堅牢性が限られています。私たちは、ハイブリッドな力-位置制御と明示的な力認識を備えたエンド・トゥ・エンドのビジョン言語行動フレームワークであるFoca-VLAを提案します。Foca-VLAは、VLM専門家に力ベースのプロンプトを導入し、段階ごとに力認識タスク概念を構築し、行動専門家でインピーダンス制御を用いたクロススケールルーティングのMixture-of-Experts（MoE）を採用して、これらの概念とリアルタイムの相互作用力を適応的に融合し、閉ループハイブリッドな力-位置制御を実現します。学習と評価を支援するために、Foca-Datasetを構築しました。これは、ウィピング、プレス、組み立てなどの5つの接触豊富なタスクで1,000の軌跡を含んでおり、マルチビュー画像、タスクプロンプト、内部状態、力信号が含まれています。広範な実験により、Foca-VLAは接触豊富な操作の成功率と信頼性を大幅に向上させ、Pi0およびPi0.5をそれぞれ48.0%と35.0%上回ることが示されました。これらは5つのタスク全体で達成されています。また、アームオーバーロードや不安定な接触といった一般的な失敗モードを軽減し、VLAsにおける力認識物理知能の進展に寄与しています。
</details>

<details>
<summary> 英語要旨 </summary>

Embodied intelligence for contact-rich manipulation has predominantly relied on position control, while explicit awareness and regulation of interaction forces remain under-explored, limiting stability, precision, and robustness in real-world tasks. We propose Foca-VLA, an end-to-end vision-language-action framework that equips robots with hybrid force-position control and explicit force awareness. Foca-VLA introduces force-based prompts into the VLM expert to construct force-aware task concepts across stages, and employs a cross-scale routing Mixture-of-Experts (MoE) with impedance control in the action expert to adaptively fuse these concepts with real-time interaction forces for closed-loop hybrid force--position regulation. To support learning and evaluation, we construct Foca-Dataset, containing 1,000 trajectories over 5 contact-rich tasks, including wiping, pressing, and assembling, with multi-view images, task prompts, proprioceptive state, and force signals. Extensive experiments show that Foca-VLA substantially improves success rates and reliability in contact-rich manipulation, outperforming Pi0 and Pi0.5 by 48.0% and 35.0%, respectively, across the 5 tasks, and mitigating common failure modes such as arm overload and unstable contact, thereby advancing force-aware physical intelligence in VLAs.
</details>

---

### Avatar Forcing: Real-Time Interactive Head Avatar Generation for Natural Conversation
著者: Taekyung Ki, Sangwon Jang, Jaehyeong Jo, Jaehong Yoon, Sung Ju Hwang

<details>
<summary> 日本語要旨 </summary>

静止画からリアルなアバターを生成し、仮想コミュニケーションやコンテンツ作成に活用する「トーキング・ヘッド生成」が進展しています。しかし、現在のモデルはまだ本当にインタラクティブなコミュニケーションを伝えることができず、しばしば感情的な関与が欠けた一方通行の応答を生成します。本研究では、真にインタラクティブなアバターを実現するための2つの主要な課題を特定しています：リアルタイムで因果制約下における動作生成と、追加のラベル付きデータなしで表現力豊かで活気ある反応を学習することです。これらの課題に対処するため、「アバター・フォース」を提案します。これは、リアルタイムユーザー-アバター相互作用を拡散強制を通じてモデル化する新しいインタラクティブな頭部アバター生成のためのフレームワークです。この設計により、アバターは低遅延でリアルタイムのマルチモーダル入力を処理し、話し言葉やうなずき、笑いといった口頭および非口頭の手がかりに対して即座に反応することができます。さらに、ユーザー条件を削除した合成的な失敗サンプルを構築し、ラベルフリーの表現力豊かなインタラクション学習を可能にする直接優先最適化方法を導入します。実験結果は、私たちのフレームワークがリアルタイムで低遅延（約500ms）のインタラクションを可能にし、ベースラインと比較して6.8倍の速度向上を実現し、反応性と表現力豊かなアバター動作を生成することを示しています。これはベースラインに対して80%以上好まれました。
</details>

<details>
<summary> 英語要旨 </summary>

Talking head generation creates lifelike avatars from static portraits for virtual communication and content creation. However, current models do not yet convey the feeling of truly interactive communication, often generating one-way responses that lack emotional engagement. We identify two key challenges toward truly interactive avatars: generating motion in real-time under causal constraints and learning expressive, vibrant reactions without additional labeled data. To address these challenges, we propose Avatar Forcing, a new framework for interactive head avatar generation that models real-time user-avatar interactions through diffusion forcing. This design allows the avatar to process real-time multimodal inputs, including the user’s audio and motion, with low latency for instant reactions to both verbal and non-verbal cues such as speech, nods, and laughter. Furthermore, we introduce a direct preference optimization method that leverages synthetic losing samples constructed by dropping user conditions, enabling label-free learning of expressive interaction. Experimental results demonstrate that our framework enables real-time interaction with low latency (about 500ms), achieving 6.8x speedup compared to the baseline, and produces reactive and expressive avatar motion, which is preferred over 80% against the baseline.
</details>

---

### Iris: Integrating Language Into Diffusion-based Monocular Depth Estimation
著者: Ziyao Zeng, Jingcheng Ni, Daniel Wang, Patrick Rim, Younjoon Chung, Fengyu Yang, Byung-Woo Hong, Alex Wong

<details>
<summary> 日本語要旨 </summary>

従来の単眼深度推定は、固有の曖昧さや視覚的な障害に苦しんでいます。私たちは、言語が画像だけではなく、現実的な3Dシーンと整合する追加条件を提供することで単眼深度推定を強化できることを示します。これにより、深度推定の解決空間が縮小されます。この条件付き分布は、ディフュージョンモデルのテキストから画像への事前学習中に学習されます。モデルは、オブジェクトのサイズ、形状、スケール、それらの空間的関係、および全体のシーン構造を暗黙的にモデリングすることで、テキスト記述を正確に反映したさまざまな視点やレイアウトの画像を生成します。本論文では、Irisとして、私たちの戦略がどのようにしてディフュージョンベースの深度推定モデルの訓練および推論にテキスト記述を統合する利点を調査します。3つの異なるディフュージョンベース単眼深度推定器（Marigold、Lotus、E2E-FT）およびそのバリアントで実験を行いました。HyperSimとVirtual KITTIでの訓練、NYUv2、KITTI、ETH3D、ScanNet、DIODEでの評価により、私たちの戦略が全体的な単眼深度推定精度を向上させることを見つけました。特に小領域では顕著です。また、テキストで記述された特定の地域の深度認識も改善されています。より詳細なテキストを提供することで、深度予測が反復的に洗練されることも見つけました。同時に、言語が訓練および推論のディフュージョン経路の収束を加速する制約として機能することもわかりました。コードと生成されたテキストデータは、採択後にリリースされます。
</details>

<details>
<summary> 英語要旨 </summary>

Traditional monocular depth estimation suffers from inherent ambiguity and visual nuisances. We demonstrate that language can enhance monocular depth estimation by providing an additional condition (rather than images alone) aligned with plausible 3D scenes, thereby reducing the solution space for depth estimation. This conditional distribution is learned during the text-to-image pre-training of diffusion models. To generate images under various viewpoints and layouts that precisely reflect textual descriptions, the model implicitly models object sizes, shapes, and scales, their spatial relationships, and the overall scene structure. In this paper, Iris, we investigate the benefits of our strategy to integrate text descriptions into training and inference of diffusion-based depth estimation models. We experiment with three different diffusion-based monocular depth estimators (Marigold, Lotus, and E2E-FT) and their variants. By training on HyperSim and Virtual KITTI, and evaluating on NYUv2, KITTI, ETH3D, ScanNet, and DIODE, we find that our strategy improves the overall monocular depth estimation accuracy, especially in small areas. It also improves the model's depth perception of specific regions described in the text. We find that by providing more details in the text, the depth predication can be iteratively refined. Simultaneously, we find that language can act as a constraint to accelerate the convergence of both training and the inference diffusion trajectory. Code and generated text data will be released upon acceptance.
</details>

---

### KV-Tracker: Real-Time Pose Tracking with Transformers
著者: Marwan Taher, Ignacio Alzugaray, Kirill Mazur, Xin Kong, Andrew J. Davison

<details>
<summary> 日本語要旨 </summary>

マルチビュー3D幾何ネットワークは強力な事前知識を提供しますが、リアルタイムアプリケーションにおいて非常に遅くなります。私たちはオンライン使用のためにこれらを適応させる新しい方法を提案し、モノクロRGBビデオから6自由度（DoF）姿勢追跡とオブジェクトおよびシーンのリアルタイム再構築を可能にします。私たちの方法は、$\pi^3$ \cite{wang2025pi3} を用いて全双方向注意を持ってシーンまたはオブジェクトをマッピングするために画像セットを迅速に選択し管理します。次に、グローバル自己注意のブロックからキーエンド（KV）ペアをキャッシュし、オンライントラッキングの唯一のシーン表現として使用します。これにより、漂流や壊滅的な忘却の心配なく推論時に最大15倍の高速化を実現します。私たちのキャッシング戦略はモデル非依存であり、再トレーニングなしに他のオフ・ザ・シェルフマルチビューネットワークに適用可能です。私たちはKV-Trackerをシーンレベルの追跡だけでなく、より困難なタスクである深度測定やオブジェクト事前知識なしに即席のオブジェクト追跡と再構築においても示します。TUM RGB-D、7-Scenes、Arctic、OnePoseデータセットでの実験は、私たちのシステムが強力な性能を発揮していることを示し、約27 FPSまでの高フレームレートを維持しています。
</details>

<details>
<summary> 英語要旨 </summary>

Multi-view 3D geometry networks offer a powerful prior but are prohibitively slow for real-time applications. We propose a novel way to adapt them for online use, enabling real-time 6-DoF pose tracking and online reconstruction of objects and scenes from monocular RGB videos. Our method rapidly selects and manages a set of images as keyframes to map a scene or object via $\pi^3$~\cite{wang2025pi3} with full bidirectional attention. We then cache the global self-attention block's key-value (KV) pairs and use them as the sole scene representation for online tracking. This allows for up to $15\times$ speedup during inference without the fear of drift or catastrophic forgetting. Our caching strategy is model-agnostic and can be applied to other off-the-shelf multi-view networks without retraining. We demonstrate KV-Tracker on both scene-level tracking and the more challenging task of on-the-fly object tracking and reconstruction without depth measurements or object priors. Experiments on the TUM RGB-D, 7-Scenes, Arctic and OnePose datasets show the strong performance of our system while maintaining high frame-rates up to ${\sim}27$ FPS.
</details>

---

### GeoDiff4D: Geometry-Aware Diffusion for 4D Head Avatar Reconstruction
著者: Chao Xu, Xiaochen Zhao, xiang deng, Jingxiang Sun, Donglin Di, Zhuo Su, Yebin Liu

<details>
<summary> 日本語要旨 </summary>

単一の肖像画から写実的でアニメーション可能な4Dヘッドアバターを再構築することは、コンピュータビジョンにおける基本的な課題です。拡散モデルがアバター再構築のための画像や動画生成で顕著な進歩を達成していますが、既存の方法は主に2Dの事前知識に依存し、一貫した3D幾何学を実現することに苦労しています。我々は、強力な幾何学的事前知識を抽出するために幾何学認識拡散を活用した新しいフレームワークを提案します。このアプローチでは、肖像画と対応する表面法線を共同で合成し、ポーズフリーの表現エンコーダが暗黙的な表現表現を捉えます。合成された画像と表現ラテントは3Dガウスモデルに基づくアバターに抽出され、正確な幾何学でのフォトリアリスティックレンダリングを可能にします。広範な実験は、我々の方法が視覚品質、表現忠実度、クロスID一般化において最先端のアプローチを大幅に上回り、リアルタイムレンダリングもサポートしていることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Reconstructing photorealistic and animatable 4D head avatars from a single portrait image remains a fundamental challenge in computer vision. While diffusion models have enabled remarkable progress in image and video generation for avatar reconstruction, existing methods primarily rely on 2D priors and struggle to achieve consistent 3D geometry. We propose a novel framework that leverages geometry-aware diffusion to distill strong geometry priors for high-fidelity head avatar reconstruction. Our approach jointly synthesizes portrait images and corresponding surface normals, while a pose-free expression encoder captures implicit expression representations. Both synthesized images and expression latents are distilled into 3D Gaussian-based avatars, enabling photorealistic rendering with accurate geometry. Extensive experiments demonstrate that our method substantially outperforms state-of-the-art approaches in visual quality, expression fidelity, and cross-identity generalization, while supporting real-time rendering.
</details>

---

### Rethinking Token Reduction for Large Vision-Language Models
著者: Yi Wang, Haofei Zhang, Qihan Huang, Anda Cao, Gongfan Fang, Wei Wang, Xuan Jin, Jie Song, Mingli Song, Xinchao Wang

<details>
<summary> 日本語要旨 </summary>

大規模ビジョン言語モデル（LVLMs）は、視覚理解と推論に優れていますが、過剰な視覚トークンのために高い推論コストが発生します。最近のトークン削減方法はこの問題を緩和していますが、主にシングルターンのビジョン質問応答（VQA）を対象としており、より実用的なマルチターンVQA（MT-VQA）シナリオはほとんど探求されていません。MT-VQAは、後続の質問が事前に不明であり、任意の画像領域を参照する可能性があるため、追加の課題を導入します。これにより、既存の削減戦略は効果的ではありません。具体的には、現在のアプローチは二つのカテゴリーに分かれます：初期のテキストプロンプトに偏ったプロンプト依存方法と、後続のターンで有用な情報を捨てるもの；そして、ヒューリスティック削減メトリクス（例えば注意スコア）に依存するため、最適ではないパフォーマンスとなるプロンプト非依存方法です。本論文では、ヒューリスティック設計の限界を克服する学習に基づくプロンプト非依存手法であるMetaCompressを提案します。まず、トークン削減を可変的な圧縮マッピングとして定式化し、既存の形式（例えば、プルーニングやマージ）を単一の学習目標に統合します。この定式化に基づき、限られた計算コストで最適な圧縮マッピングを学習するデータ効率的なトレーニングパラダイムを導入します。MT-VQAベンチマークおよび複数のLVLMアーキテクチャにわたる広範な実験では、MetaCompressが優れた効率性と精度のトレードオフを達成し、ダイアログターン全体で強力な汎用性を維持することを示しています。将来の研究を促進するために、コードを公開します。
</details>

<details>
<summary> 英語要旨 </summary>

Large Vision-Language Models (LVLMs) excel in visual understanding and reasoning, but the excessive visual tokens lead to high inference costs. Although recent token reduction methods mitigate this issue, they mainly target single-turn Visual Question Answering (VQA), leaving the more practical multi-turn VQA (MT-VQA) scenario largely unexplored. MT-VQA introduces additional challenges, as subsequent questions are unknown beforehand and may refer to arbitrary image regions, making existing reduction strategies ineffective. Specifically, current approaches fall into two categories: prompt-dependent methods, which bias toward the initial text prompt and discard information useful for subsequent turns; prompt-agnostic ones, which, though technically applicable to multi-turn settings, rely on heuristic reduction metrics such as attention scores, leading to suboptimal performance. In this paper, we propose a learning-based prompt-agnostic method, termed MetaCompress, overcoming the limitations of heuristic designs. We begin by formulating token reduction as a learnable compression mapping, unifying existing formats such as pruning and merging into a single learning objective. Upon this formulation, we introduce a data-efficient training paradigm capable of learning optimal compression mappings with limited computational costs. Extensive experiments on MT-VQA benchmarks and across multiple LVLM architectures demonstrate that MetaCompress achieves superior efficiency–accuracy trade-offs while maintaining strong generalization across dialogue turns. Our code will be released to facilitate future research.
</details>

---

### VidEoMT: Your ViT Is Secretly Also A Video Segmentation Model
著者: Narges Norouzi, Idil Esen Zulfikar, Niccolò Cavagnero, Tommie Kerssies, Bastian Leibe, Gijs Dubbelman, Daan de Geus

<details>
<summary> 日本語要旨 </summary>

既存のオンライン動画セグメンテーションモデルは、通常、フレームごとのセグメンターを複雑な専用トラッキングモジュールと組み合わせています。これらのモジュールは効果的ですが、大きなアーキテクチャの複雑さや計算オーバーヘッドを導入します。最近の研究では、十分な容量で大規模な事前学習を行った単純なビジョントランスフォーマー（ViT）エンコーダーが、専用モジュールを必要とせずに正確な画像セグメンテーションを実行できることが示唆されています。この観察に基づき、私たちは専用トラッキングモジュールを必要としないシンプルなエンコーダーのみの動画セグメンテーションモデルであるVideo Encoder-only Mask Transformer（VidEoMT）を提案します。ViTのエンコーダーのみで時間的モデリングを可能にするため、VidEoMTは前フレームからクエリを再利用して情報をフレーム間で伝播させる軽量なクエリプロパゲーションメカニズムを導入します。新しいコンテンツへの適応性とのバランスを取るため、時間的に無関心な学習済みクエリのセットと伝播されたクエリを統合するクエリフュージョン戦略を採用しています。その結果、VidEoMTはトラッカーの利点を得ながら複雑さを増やすことなく、競争力のある精度を達成し、ViT-Lバックボーンで最大160 FPSまで実行速度が向上します（5倍から10倍速い）。コードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Existing online video segmentation models typically combine a per-frame segmenter with complex specialized tracking modules. While effective, these modules introduce significant architectural complexity and computational overhead. Recent studies suggest that plain Vision Transformer (ViT) encoders, when scaled with sufficient capacity and large-scale pre-training, can conduct accurate image segmentation without requiring specialized modules. Motivated by this observation, we propose the Video Encoder-only Mask Transformer (VidEoMT), a simple encoder-only video segmentation model that eliminates the need for dedicated tracking modules. To enable temporal modeling in an encoder-only ViT, VidEoMT introduces a lightweight query propagation mechanism that carries information across frames by reusing queries from the previous frame. To balance this with adaptability to new content, it employs a query fusion strategy that combines the propagated queries with a set of temporally-agnostic learned queries. As a result, VidEoMT attains the benefits of a tracker without added complexity, achieving competitive accuracy while being 5x-10x faster, running at up to 160 FPS with a ViT-L backbone. Code will be made publicly available.
</details>

---

### Beyond Strict Pairing: Arbitrarily Paired Training for High-Performance Infrared and Visible Image Fusion
著者: Yanglin Deng, Tianyang Xu, Chunyang Cheng, Hui Li, Xiaojun Wu, Josef Kittler

<details>
<summary> 日本語要旨 </summary>

赤外線と可視画像の融合（IVIF）は、両方のソースモダリティから補完的な情報を統合し、自然なテクスチャと顕著な赤外線シグニチャーを同時に保持することを目指しています。既存の解決策は主に厳密に整列された画像ペアの大規模なセットでトレーニングすることに依存していますが、このようなデータを取得することはしばしば実用的ではありません。これは高コストかつ労力を要する整列プロセスのためです。また、トレーニング中に厳密なペアリング設定を維持することで、クロスモダリティ関係の量が制限され、一般化性能が低下します。このため、本研究では高性能IVIFにおける厳密にペアトレーニングパラダイム（SPTP）の必要性を問い直し、UnPairedとArbitrarily Paired Training Paradigms（UPTPとAPTP）を体系的に調査します。APTPの理論目標を設定し、これはUPTPとSPTPの補完性を反映しています。さらに重要なことに、非常に限られたかつ整列されていないトレーニングデータでもクロスモダリティ関係を大幅に豊かにできる実用的フレームワークを開発しました。これらの提案を検証するため、エンドツーエンドの軽量な基準線と革新的な損失関数のセットが3つの古典的フレームワーク（CNN、Transformer、GAN）をカバーするように設計されました。包括的な実験は、提案されたAPTPとUPTPが非常に限られたかつコンテンツ不整合の赤外線および可視データセットでモデルをトレーニングすることが可能であり、SPTPでは100倍大きいデータセットに匹敵する性能を達成できることを示しています。この発見はデータ収集のコストと難しさを根本的に軽減し、データ観点からモデルの堅牢性を向上させ、IVIF研究に実用的な解決策を提供します。
</details>

<details>
<summary> 英語要旨 </summary>

Infrared and visible image fusion (IVIF) aims to synthesise complementary information from the two source modalities while preserving natural textures and salient thermal signatures simultaneously. Existing solutions predominantly rely on extensive sets of rigidly aligned image pairs for training. However, acquiring such data is often impractical due to the costly and labour-intensive alignment process. Besides, maintaining a rigid pairing setting during training restricts the volume of cross-modal relationships, thereby limiting the generalisation performance. To this end, this work challenges the necessity of Strictly Paired Training Paradigm (SPTP) by systematically investigating UnPaired and Arbitrarily Paired Training Paradigms (UPTP and APTP) for high-performance IVIF. We establish a theoretical objective of APTP, reflecting the complementary nature between UPTP and SPTP. More importantly, we develop a practical framework capable of significantly enriching cross-modal relationships even with severely limited and unaligned training data. To validate our propositions, three end-to-end lightweight baselines, alongside a set of innovative loss functions, are designed to cover three classic frameworks (CNN, Transformer, GAN). Comprehensive experiments demonstrate that the proposed APTP and UPTP are feasible and capable of training models on a severely limited and content-inconsistent infrared and visible dataset, achieving performance comparable to that of a dataset 100$\times$ larger in SPTP. This finding fundamentally alleviates the cost and difficulty of data collection while enhancing model robustness from the data perspective, delivering a feasible solution for IVIF studies.
</details>

---

### RobotSeg: A Model and Dataset for Segmenting Robots in Image and Video
著者: Haiyang Mei, Qiming Huang, Hai Ci, Mike Zheng Shou

<details>
<summary> 日本語要旨 </summary>

ロボットセグメンテーションの精度は、ロボット知覚における基本的な能力です。これにより、ロボットアプリケーション向けのデジタルツインや世界モデルの正確な構築が可能となり、ロボット中心のデータ拡張をサポートし、信頼性の高い手掛かりを提供してロボットアクションや姿勢の抽出に役立ちます。現代のセグメンテーションモデルが強力な能力を持っているにも関わらず、驚くほどロボットのセグメンテーションは依然として難しいです。これは、ロボットの多様性、外観の曖昧さ、構造的複雑さ、急速な形状変化に起因します。この課題を受け入れる中で、私たちは画像とビデオにおけるロボットセグメンテーションの基盤モデルであるRobotSegを導入します。RobotSegは汎用性の高いSAM 2基盤モデルに構築されていますが、アーティキュレートロボットへの適応不足、手動プロンプトへの依存、フレームごとのトレーニングマスク注釈の必要性という3つの制限を克服するために、構造強化メモリアソシエーター、ロボットプロンプトジェネレーター、ラベル効率的なトレーニング戦略を導入しています。これらの革新は構造に配慮した自動化されたラベル効率的なソリューションを可能にします。さらに、多様なロボットエンボディメントと環境を含むビデオロボットセグメンテーション（VRS）データセットを2.8k以上のビデオ（138kフレーム）で構築しました。広範な実験により、RobotSegが画像とビデオの両方で最先端の性能を達成しており、ロボット知覚の将来的な進展のための強固な基盤を築いていることが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

Accurate robot segmentation is a fundamental capability for robotic perception. It enables precise construction of digital twins and world models for robotic applications, supports robot-centric data augmentation, and provides reliable cues for extracting robot actions and poses. Despite the strong capabilities of modern segmentation models, surprisingly it remains challenging to segment robots. This is due to robot embodiment diversity, appearance ambiguity, structural complexity, and rapid shape changes. Embracing these challenges, we introduce RobotSeg, a foundation model for robot segmentation in image and video. RobotSeg is built upon the versatile SAM 2 foundation model but addresses its three limitations for robot segmentation, namely the lack of adaptation to articulated robots, reliance on manual prompts, and the need for per-frame training mask annotations, by introducing a structure-enhanced memory associator, a robot prompt generator, and a label-efficient training strategy. These innovations collectively enable a structure-aware, automatic, and label-efficient solution. We further construct the video robot segmentation (VRS) dataset comprising over 2.8k videos (138k frames) with diverse robot embodiments and environments. Extensive experiments demonstrate that RobotSeg achieves state-of-the-art performance on both images and videos, establishing a strong foundation for future advances in robot perception.
</details>

---

### The Consistency Critic: Correcting Inconsistencies in Generated Images Via Reference-Guided Attentive Alignment
著者: Ziheng Ouyang, Yiren Song, Yaoli Liu, Shihao Zhu, Qibin Hou, Ming-Ming Cheng, Mike Zheng Shou

<details>
<summary> 日本語要旨 </summary>

これまでの研究では、参照画像を用いたさまざまなカスタマイズ生成タスクが探求されてきましたが、依然として生成される細部の一貫性に限界があります。本論文では、生成画像の不整合問題を解決するために参照ガイド付きのポストエディットアプローチを適用し、ImageCriticを提案します。まず、VLMベースの選択と明示的な劣化を通じて構築された参照-劣化-ターゲットトリプレットのデータセットを用いることで、既存の生成モデルにおける一般的な不正確さや不整合を効果的にシミュレートします。また、モデルの注意機構と内在表現を徹底的に調査し、それに基づいて注意アライメント損失と詳細エンコーダーを考案して不整合を正確に修正します。ImageCriticはエージェントフレームワークに統合され、複雑なシナリオで自動的に不整合を検出し、多回と局所編集によってそれらを修正することが可能です。広範囲の実験により、ImageCriticはさまざまなカスタマイズ生成シナリオで詳細関連の問題を効果的に解決し、既存手法と比較して大幅な改善を提供することが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

Previous works have explored various customized generation tasks given a reference image, but they still face limitations in generating consistent fine-grained details. In this paper, our aim is to solve the inconsistency problem of generated images by applying a reference-guided post-editing approach and present our ImageCritic. We first construct a dataset of reference-degraded-target triplets obtained via VLM-based selection and explicit degradation, which effectively simulates the common inaccuracies or inconsistencies observed in existing generation models. Furthermore, building on a thorough examination of the model's attention mechanisms and intrinsic representations, we accordingly devise an attention alignment loss and a detail encoder to precisely rectify inconsistencies. ImageCritic can be integrated into an agent framework to automatically detect inconsistencies and correct them with multi-round and local editing in complex scenarios. Extensive experiments demonstrate that ImageCritic can effectively resolve detail-related issues in various customized generation scenarios, providing significant improvements over existing methods.
</details>

---

### U-Mind: A Unified Framework for Real-Time Multimodal Interaction with Audiovisual Generation
著者: xiang deng, Feng Gao, Yong Zhang, Youxin Pang, Xu Xiaoming, Zhuoliang Kang, Xiaoming Wei, Yebin Liu

<details>
<summary> 日本語要旨 </summary>

リアルタイムでのフルスタックマルチモーダルインタラクションは、自然で動的なコミュニケーションが可能な知能を持つエンファッシングエージェントを構築する上での中心的な目標です。しかし、既存のシステムは単一モーダル生成に限定されているか、または低下した推論能力と不十分なクロスモーダルアライメントにより、調和的で感覚的に根拠のあるインタラクションが妨げられています。本研究では、リアルタイム生成をサポートし、言語、スピーチ、動作、ビデオ合成を単一の対話ループ内で共同モデリングする初めての統一型高知能マルチモーダルダイアログシステムとして\textbf{U-Mind}を紹介します。その核心には、クロスモーダル同期の強化を目的とした\textit{セグメントウィズアラインメント戦略}と推論能力の維持を目指す\textit{リハーサルドリブンラーニング}により、二つの重要な課題に対処する\textit{統一アライメントと推論フレームワーク}が実装されています。推測時には、U-Mindは内部でのチェインオブスロート計画を行った後、モダリティ間で時間的に同期した生成を行う\textit{テキストファーストデコーディングパイプライン}を採用します。ループを閉じるために、ポーズとスピーチに条件付けられたリアルタイムビデオレンダリングフレームワークを実装し、表現力豊かで同期した視覚的なフィードバックを可能にします。広範囲のマルチモーダルインタラクションタスク（質問応答、指示従事、動作生成など）での実験が示すように、U-Mindは最先端のパフォーマンスを達成し、知能的で没入感のある会話エージェントへの道を開いています。
</details>

<details>
<summary> 英語要旨 </summary>

Full-stack multimodal interaction in real-time is a central goal in building intelligent embodied agents capable of natural, dynamic communication. However, existing systems are either limited to unimodal generation or suffer from degraded reasoning and poor cross-modal alignment, preventing coherent and perceptually grounded interactions. In this work, we introduce \textbf{U-Mind}, the first unified system for high-intelligence multimodal dialogue that supports real-time generation and jointly models language, speech, motion, and video synthesis within a single interactive loop. At its core, U-Mind implements a \textit{Unified Alignment and Reasoning Framework} that addresses two key challenges: enhancing cross-modal synchronization via a \textit{segment-wise alignment strategy}, and preserving reasoning abilities through \textit{Rehearsal-Driven Learning}. During inference, U-Mind adopts a \textit{text-first decoding pipeline} that performs internal chain-of-thought planning followed by temporally synchronized generation across modalities. To close the loop, we implement a real-time video rendering framework conditioned on pose and speech, enabling expressive and synchronized visual feedback. Extensive experiments demonstrate that U-Mind achieves state-of-the-art performance on a range of multimodal interaction tasks, including question answering, instruction following, and motion generation, paving the way toward intelligent, immersive conversational agents.
</details>

---

### Coupled Diffusion Sampling for Training-free Multi-view Image Editing
著者: Hadi Alzayer, Yunzhi Zhang, Chen Geng, Jia-Bin Huang, Jiajun Wu

<details>
<summary> 日本語要旨 </summary>

与えられたマルチビュー画像のコレクションに対して、事前学習済みの2Dエディティングモデルと生成的マルチビューモデルを使用したトレーニングフリーなフレームワークで一貫性のあるマルチビューエディットを行います。2Dエディティングモデルは3Dシーンのマルチビュー画像セット内の各画像を独立して編集できますが、ビュー間で一貫性を保つことはできません。既存のアプローチでは通常、明示的な3D表現を使用して不整合を平均化しますが、これらは長時間の最適化、スパースビュー設定下での不安定性、ぼやけた結果を生じることがあります。私たちは異なる視点からこの問題に取り組み、2Dエディティングモデルを使用して拡散サンプリング過程でマルチビュー生成モデルを制御します。これは私たちの新しいカップリングされた拡散サンプリングプロセスによって実現されます。2つのトラジェクトリをマルチビュー画像分布と2D編集済み画像分布から同時にサンプリングし、サンプルをカップリング項で接続します。効果的には、両方のモデルがサンプリング中にお互いをガイドし、結果として得られるマルチビューモデルからのサンプルは一貫性を保ちながら望ましい編集を満たします。このフレームワークの有効性と汎用性を3つの異なるマルチビュー画像エディティングタスクで検証し、さまざまなモデルアーキテクチャにわたる適用可能性を示します。また、カップリングの効果をSoTAの画像およびビデオ生成モデルで示し、私たちの方法がマルチビュー編集を超えて潜在的な応用があることを強調します。
</details>

<details>
<summary> 英語要旨 </summary>

Given a collection of multi-view images, we perform consistent multi-view editing with a training-free framework using pre-trained 2D editing models and a generative multi-view model. While 2D editing models can independently edit each image in a set of multi-view images of a 3D scene, they do not maintain consistency across views. Existing approaches typically rely on explicit 3D representations to average out the inconsistencies, but they suffer from a lengthy optimization, instability under sparse view settings, and can produce blurry results. We address the problem from a different lens, where we use the 2D editing model to steer a multi-view generative model in the diffusion sampling process. This is achieved through our novel coupled diffusion sampling process. We concurrently sample two trajectories from both a multi-view image distribution and a 2D edited image distribution, and connect the samples with a coupling term. Effectively, the two models guide each other during sampling, and the resulting sample from the multi-view model remains consistent while satisfying the desired edit. We validate the effectiveness and generality of this framework on three distinct multi-view image editing tasks, and demonstrate its applicability across various model architectures. We further illustrate the effects of coupling on SoTA image and video generation models, highlighting the potential of our method beyond multi-view editing.
</details>

---

### OneSparse: A Unified Framework for Sparse Activation Layers in Vision Models
著者: Xingkui Zhu, Dingkang Liang, Cheng Chen, Daoxin Zhang, lv hanxiang, Zhe Xu, Yao Hu, Xiang Bai

<details>
<summary> 日本語要旨 </summary>

大規模モデルのスケーリングにおいて中心的なアプローチであるスパース活性化層、特にMixture-of-Experts（MoE）とメモリベースモジュールは、ビジョンタスクでも注目を集めています。これらのパラダイムは概念的に類似しているものの、独立して進化してきたため、体系的な比較やそれぞれの補完的な強みを活かしたモジュール開発が妨げられています。このギャップを埋めるために、私たちは**OneSparse**という統一フレームワークを提案します。これはMoEとメモリモジュールを共通の抽象化の下で再定式化するものです。このことにより、それらの体系的な比較と統合が可能となり、連続した設計空間が明らかになります。この抽象化を指針として、**Nexus Layer**を設計しました。これは二つの主要な革新を特徴としています：メモリ取得の効率性とMoEの負荷分散を統合した一体化されたルーティング機構により、安定かつスケーラブルなトークン割り当てが保証されること、およびメモリモジュールが粗い表現をスケッチし、専門家モジュールが重要領域を洗練する適応処理戦略です。画像分類、物体検出、セマンティックセグメンテーションにおける広範な実験は、私たちのNexus Layerが新しいパフォーマンス効率フロンティアを確立し、畳み込みとトランスフォーマーアーキテクチャにおける代表的なスパースベースラインを超えていることを示しています。これらの結果は、OneSparseフレームワークが補完的なスパースパラダイムを統一し統合する力を証明し、ビジョンにおけるハイブリッドスパースモデリングの可能性を強調しています。
</details>

<details>
<summary> 英語要旨 </summary>

Sparse activation layers, primarily Mixture-of-Experts (MoE) and memory-based modules, are a central approach for scaling large models and are gaining traction in vision tasks. Despite conceptual similarities, these paradigms have evolved independently, hindering systematic comparison and the development of modules that exploit their complementary strengths. To bridge this gap, we propose **OneSparse**, a unified framework that reformulates MoE and memory modules under a common abstraction. This enables their systematic comparison and integration, revealing a continuous design space. Guided by this abstraction, we design the **Nexus Layer**, which features two key innovations: a unified routing mechanism that merges the efficiency of memory retrieval with MoE's load balancing to ensure stable and scalable token assignment, and an adaptive processing strategy where memory modules sketches coarse representations while expert modules refine critical regions. Extensive experiments on image classification, object detection, and semantic segmentation demonstrate that our Nexus Layer establishes a new performance efficiency frontier, surpassing representative sparse baselines on convolutional and transformer architectures. These results validate the power of the OneSparse framework to unify and integrate complementary sparse paradigms and underscores the potential of hybrid sparse modeling in vision.
</details>

---

### RunawayEvil: Jailbreaking The Image-to-Video Generative Models
著者: yueming lyu, Rufan Qian, Yueming Lyu, Qinglong Liu, Linzhuang Zou, Jie Qin, Songhua Liu, Caifeng Shan

<details>
<summary> 日本語要旨 </summary>

画像から動画（I2V）生成は、モデルが画像とテキストプロンプトの両方を組み合わせて考慮することでダイナミックなビジュアルシーケンスを合成するコンテンツ作成の最前線を代表します。このマルチモーダルグラウンディングにより、動画属性への多様な制御が可能となります。しかし、これが正確には重要なセキュリティ上の盲点を導入します：視覚的およびテキスト的手掛かりの相互作用を悪用することで、攻撃者が出力のセキュリティを深刻に妨害するマルチモーダルジェイルブレイク攻撃を開始できるからです。現実世界のI2Vシステムにおけるセキュリティメカニズムの増加にもかかわらず、このようなクロスモーダル脅威は未だ探求されていません。既存の攻撃方法は単一モーダル設定に限定され、孤立したテキストまたは画像の擾乱に依存しており、その効果を大幅に制限しています。このギャップを埋めるために、我々はI2Vモデル向けの最初のマルチモーダルジェイルブレイクフレームワークであるRunaway Evilを提案します。このフレームワークは動的進化能力を持ち、Strategy-Tactic-Actionパラダイムに基づいて構築されています。我々のフレームワークは三つのコアコンポーネントを通じて自己増幅攻撃を示します：（1）強化学習による戦略カスタマイズと大規模言語モデル（LLM）に基づく戦略探索を可能にする、戦略意識のあるコマンドユニット；（2）選択された戦略に基づいて協調的なテキストジェイルブレイク指示と画像改ざんガイドラインを生成する、マルチモーダルタクティカルプランニングユニット；（3）調整された攻撃を実行し評価する、タクティカルアクションユニット。この自己進化型のアーキテクチャにより、フレームワークは人間の介入なしで攻撃戦略を継続的に適応させ強化することが可能です。広範囲の実験では、Runaway EvilがOpen-Sora 2.0やCogVideoXなどの商用I2Vモデルで最先端の攻撃成功率を達成していることが示されています。この研究はマルチモーダル脆弱性を探求し軽減するための重要なツールを提供し、より堅牢な動画生成システム構築の基盤を築きます。
</details>

<details>
<summary> 英語要旨 </summary>

Image-to-Video (I2V) generation represents a frontier in content creation, where models synthesize dynamic visual sequences by jointly reasoning from both image and text prompts. This multimodal grounding enables diverse controllability over video attributes. However, it is precisely this capability that introduces a critical security blind spot: by exploiting the interplay between visual and textual cues, attackers can launch multimodal jailbreak attacks that severely compromise output security. Despite the increasing implementation of security mechanisms in real-world I2V systems, such cross-modal threats remain unexplored. Existing attack methods remain confined to single-modal settings, relying solely on isolated text or image perturbations, which severely limits their effectiveness. To bridge this gap, we propose Runaway Evil, the first multimodal jailbreaking framework for I2V models with dynamic evolutionary capability. Built on a Strategy-Tactic-Action paradigm, our framework exhibits self-amplifying attack through three core components: (1) a strategy-aware command unit that enables the attack to self-evolve its strategies through reinforcement learning-driven strategy customization and large language model (LLM)-based strategy exploration; (2) a multimodal tactical planning unit that generates synergistic text jailbreak instructions and image tampering guidelines based on the selected strategies; and (3) an tactical action Unit executes and evaluates the coordinated attacks. This self-evolving architecture allows the framework to continuously adapt and intensify its attack strategies without human intervention. Extensive experiments demonstrate that Runaway Evil achieves state-of-the-art attack success rates on commercial I2V models, such as Open-Sora 2.0 and CogVideoX. This work provides a critical tool for probing and mitigating multimodal vulnerabilities, laying a foundation for building more robust video generation systems.
</details>

---

### Diffusion Probe: Generated Image Result Prediction Using CNN Probes
著者: Bukun Huang, Benlei Cui, Zhizeng Ye, Xuemei Dong, Tuo Chen, Hui Xue, Dingkang Yang, Longtao Huang, Haiwen Hong, Jingqun Tang

<details>
<summary> 日本語要旨 </summary>

テキストから画像（T2I）の拡散モデルは、現在、効率的な早期品質評価メカニズムを欠いており、複数の生成が必要なシナリオ（例：プロンプトの反復、エージェントベースの画像生成、フローグループ）ではコストのかかるランダムな試行錯誤を強いられています。これに対処するために、まず初期拡散プロセスの注意分布と最終画像品質との間に強い相関があることを明らかにします。この洞察に基づき、モデル内部のクロスアテンションマップを予測信号として利用する画期的なフレームワークである**Diffusion Probe**を導入します。私たちは軽量の予測器を提案し、これは初期ノイズ除去ステップから抽出された新生クロスアテンション分布の統計的特性と最終画像の包括的な品質との直接マッピングを確立するように訓練されています。これにより、私たちのプローブは、どんな具体的な基準とも無関係に、画像品質のさまざまな側面を正確に予測することができます。完全合成が終了する前に長い時間からです。私たちは、広範囲の条件下で一貫して強力な予測精度を示すDiffusion Probeの信頼性と汎用性を実証的に検証します。多様なT2Iモデル（例：SDXL、FLUX、Qwen-Image）で広範囲の初期ノイズ除去ウィンドウを通じて、さまざまな解像度と品質メトリクスにおいて、**高い相関（PCC > 0.7）**と**分類性能（AUC-ROC > 0.9）**を達成します。この固有の信頼性は、早期品質ガイド付きの意思決定が利益をもたらすT2Iワークフローの最適化に成功することで実践的にさらに示されています。例えば、**プロンプト最適化**、**シード選択**、および**加速RLトレーニング**です。これらのアプリケーションでは、プローブの早期信号がよりターゲットを絞ったサンプリング戦略を可能にし、低ポテンシャルなパスでのコストのかかる計算を予防します。これにより二重の利点がもたらされます：計算オーバーヘッドの大幅な削減と最終的な成果品質の同時改善であり、Diffusion Probeはモデル非依存かつ広く適用可能なツールとして位置づけられ、T2I効率を革命する準備が整っています。
</details>

<details>
<summary> 英語要旨 </summary>

Text-to-image (T2I) diffusion models currently lack an efficient mechanism for early quality assessment, forcing costly random trial-and-error in scenarios requiring multiple generations (e.g., iterating on prompts, agent-based image generation, flow-grpo). To address this, we first reveal a strong correlation between the attention distribution in the early diffusion process and the final image quality. Building upon this insight, we introduce **Diffusion Probe**, a pioneering framework that leverages the model’s internal cross-attention maps as a predictive signal. We propose a lightweight predictor, trained to establish a direct mapping from statistical properties of these nascent cross-attention distributions—extracted from the initial denoising steps—to the final image’s comprehensive quality. This allows our probe to accurately forecast various aspects of image quality, regardless of the specific ground-truth quality metric, long before full synthesis is complete. We empirically validate the reliability and generalizability of Diffusion Probe through its consistently strong predictive accuracy across a wide spectrum of conditions. On diverse T2I models (e.g., SDXL, FLUX, Qwen-Image), throughout broad early-denoising windows, across various resolutions, and with different quality metrics, it achieves **high correlation (PCC > 0.7)** and **classification performance (AUC-ROC > 0.9)**. This intrinsic reliability is further demonstrated in practice by successfully optimizing T2I workflows that benefit from early, quality-guided decisions, such as **Prompt Optimization**, **Seed Selection**, and **Accelerated RL Training**. In these applications, the probe's early signal enables more targeted sampling strategies, preempting costly computations on low-potential paths. This yields a dual benefit: a significant reduction in computational overhead and a simultaneous improvement in final outcome quality, establishing Diffusion Probe as a model-agnostic and broadly applicable tool poised to revolutionize T2I efficiency.
</details>

---

### Unleashing Vision-Language Semantics for Video Deepfake Detection
著者: Jiawen Zhu, Yunqi Miao, Xueyi Zhang, Jiankang Deng, Guansong Pang

<details>
<summary> 日本語要旨 </summary>

最近のビデオ深層偽造検出（DFD）研究では、CLIPなどの事前学習済みVision-Language Models（VLMs）が異なるアイデンティティにわたってアーティファクトを検出する際の強力な汎用性を示しています。しかし、既存の手法は視覚特徴のみを活用し、その最も顕著な強みである潜在空間に埋め込まれた豊富なビジョン・ランゲージセマンティクスを見落としています。私たちは、このようなクロスモーダルセマンティクスの可能性を解放し、深層偽造検出におけるモデルの識別力を向上させる新しいDFDフレームワークであるVLAForgeを提案します。この研究では、i) ForgePerceiverを通じてVLMの視覚認識能力を強化し、事前学習済みVision–Language Alignment（VLA）知識を保持しつつ、細部と全体的にわたる微妙で多様な偽造手がかりを捉える独立したラーナーとして機能し、ii) ForgePerceiverによって学習された偽造手がかりとクロスモーダルセマンティクスを結合して導出される補完的な識別手がかりであるアイデンティティ認識VLAスコアを提供します。特に、VLAスコアは各アイデンティティに合わせた真正性の手がかりを捉えるためにアイデンティティ優先情報に基づくテキストプロンプトで強化され、より識別力のあるクロスモーダルセマンティクスを可能にします。古典的な顔交換偽造や最近のフルフェイス生成偽造を含むビデオDFDベンチマークで行われた包括的な実験は、私たちのVLAForgeがフレームおよびビデオレベルの両方で最先端手法を大幅に上回ることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Recent video Deepfake Detection (DFD) studies have demonstrated that pre-trained Vision-Language Models (VLMs) such as CLIP exhibit strong generalization capabilities in detecting artifacts across different identities. However, existing approaches focus on leveraging visual features only, overlooking their most distinctive strength — the rich vision-language semantics embedded in the latent space. We proposes VLAForge, a novel DFD framework that unleashes the potential of such cross-modal semantics in enhancing model's discriminability in deepfake detection. This work i) enhances the visual perception of VLM through a ForgePerceiver, which acts as an independent learner to capture subtle and diverse forgery cues both granularly and holistically, while preserving the pretrained Vision–Language Alignment (VLA) knowledge, and ii) provides a complementary discriminative cue — Identity-aware VLA score, derived by coupling cross-modal semantics with the forgery cues learned by ForgePerceiver. Notably, the VLA score is augmented by an identity prior-informed text prompting to capture authenticity cues tailored to each identity, thereby enabling more discriminative cross-modal semantics. Comprehensive experiments on video DFD benchmarks, including classical face-swapping forgeries and recent full-face generation forgeries, demonstrate that our VLAForge substantially outperforms state-of-the-art methods at both frame and video levels.
</details>

---

### From Softmax to Dirichlet: Evidential Learning for Semi-supervised Semantic Segmentation
著者: Huayu Mai, Rui Sun, Yujia Chen, Wangkai Li, Bingzhou Wang, Aibing Li, Zhangyu He, Yuan Wang

<details>
<summary> 日本語要旨 </summary>

半教師ありセマンティックセグメンテーションの重要な課題は、大量の未ラベルデータを活用してモデルの汎化性能を向上させる方法です。しかし、既存のソフトマックススコアに基づくフィルタリング手法はニューラルネットワークの過信問題に影響されやすく、誤ったプーシュドラベルが含まれることでトレーニングプロセスに悪影響を及ぼします。本論文では、信頼性の高いプーシュドラベル選択のために予測不確実性を明示的にモデリングする新しい証拠学習フレームワークを提案します。クラス確率分布をディリクレ分布でモデル化することで、分布論的観点から原則に基づいた改善された不確実性推定を得ます。さらに、HESS（Hyper-ESS）を提案し、排他的および集合的証拠のモデリングを分離して包括的な証拠認識を行い、より正確な不確実性推定を得ることができます。3つの挑戦的なベンチマークにおける広範な実験では、HESSを既存の半教師ありセマンティックセグメンテーションフレームワークに統合することで一貫して性能が向上し、より信頼性の高いプーシュドラベル選択から恩恵を受けることが示されました。本研究は半教師ありセマンティックセグメンテーションにおける証拠学習の可能性を浮き彫りにし、将来の研究への新たな道を開くものです。コードとモデルは将来の研究を促進するために公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

The critical challenge of semi-supervised semantic segmentation lies in how to fully exploit a large volume of unlabeled data to improve the model's generalization performance for robust segmentation. However, existing softmax scores-based filtering methods tend to be affected by the overconfidence issue in neural networks, leading to the inclusion of incorrect pseudo-labels that negatively impact the training process. In this paper, we propose a novel evidential learning framework to explicitly model the prediction uncertainty for reliable pseudo-label selection. By modeling the distribution of class probabilities using Dirichlet distributions, we obtain principled and improved uncertainty estimates from a distributional perspective. Furthermore, we propose HESS (Hyper-ESS), decoupling the modeling of exclusive and collective evidence for comprehensive evidence perception, to yield more accurate uncertainty estimates. Extensive experiments on three challenging benchmarks demonstrate that integrating HESS into existing semi-supervised semantic segmentation frameworks consistently improves performance, benefiting from more reliable pseudo-label selection. Our work sheds light on the potential of evidential learning in semi-supervised semantic segmentation and opens up new avenues for future research. Code and models will be made available to facilitate future research.
</details>

---

### MeanFlow Transformers with Representation Autoencoders
著者: Zheyuan Hu, Chieh-Hsin Lai, Ge Wu, Yuki Mitsufuji, Stefano Ermon

<details>
<summary> 日本語要旨 </summary>

MeanFlow（MF）は、ノイズからデータへの長跳躍を直接学習することで効率的な少ステップ生成を可能にする拡散動機付け型生成モデルです。実際には、高次元データのモデリングにおいて事前学習済みのStable Diffusion変分自己符号化器（SD-VAE）を活用することで潜在MFとして使用されます。しかし、MFのトレーニングは計算量が多く不安定な場合があります。推論時には、SD-VAEデコーダーが生成コストを支配し、MFはクラス条件付き生成において複雑なガイダンスハイパーパラメータに依存します。本研究では、事前学習済みのビジョンエンコーダー（例えばDINO）がセマンティックリッチな潜在変数を提供し、軽量デコーダーとペアになっている表現自己符号化器（RAE）の潜在空間でMFの効率的なトレーニングおよびサンプリングスキームを開発しました。RAEの潜在空間におけるMFの初期トレーニングは重大な勾配爆発を引き起こすことが観察されます。このため、安定化および加速化するために、軌道認識型初期化のための一貫性中間トレーニングを採用し、二段階スキームを使用します：事前学習済みの流れマッチング教師からの転移による収束速度の向上と分散の削減、その後任意で一点速度推定子を用いたブートストラップステージを追加し、オラクル平均流からの偏差をさらに低減します。この設計はガイダンスの必要性を排除し、トレーニング構成を簡素化し、トレーニングおよびサンプリングの両方で計算量を削減します。実験的には、我々の方法は1ステップFIDが2.03となり、vanilla MFの3.43を上回ります。また、ImageNet 256においてサンプリングGFLOPSを38%削減し、総トレーニングコストを83%削減します。さらに我々はアプローチをImageNet 512まで拡張し、競合他社の中で最も低いGFLOPSでありながら1ステップFIDが3.23という優れた結果を達成しています。コードおよび証明は補足資料にて公開されています。
</details>

<details>
<summary> 英語要旨 </summary>

MeanFlow (MF) is a diffusion-motivated generative model that enables efficient few-step generation by learning long jumps directly from noise to data. In practice, it is often used as a latent MF by leveraging the pre-trained Stable Diffusion variational autoencoder (SD-VAE) for high-dimensional data modeling. However, MF training remains computationally demanding and is often unstable. During inference, the SD-VAE decoder dominates the generation cost, and MF depends on complex guidance hyperparameters for class-conditional generation. In this work, we develop an efficient training and sampling scheme for MF in the latent space of a Representation Autoencoder (RAE), where a pre-trained vision encoder (e.g., DINO) provides semantically rich latents paired with a lightweight decoder. We observe that naive MF training in the RAE latent space suffers from severe gradient explosion. To stabilize and accelerate training, we adopt Consistency Mid-Training for trajectory-aware initialization and use a two-stage scheme: distillation from a pre-trained flow matching teacher to speed convergence and reduce variance, followed by an optional bootstrapping stage with a one-point velocity estimator to further reduce deviation from the oracle mean flow. This design removes the need for guidance, simplifies training configurations, and reduces computation in both training and sampling. Empirically, our method achieves a 1-step FID of 2.03, outperforming vanilla MF’s 3.43, while reducing sampling GFLOPS by 38% and total training cost by 83% on ImageNet 256. We further scale our approach to ImageNet 512, achieving a competitive one-step FID of 3.23 with the lowest GFLOPS among all baselines. Code and proofs are available in the supplementary material.
</details>

---

### AffordGen: Generating Diverse Demonstrations for Generalizable Object Manipulation with Affordance Correspondence
著者: Jiawei Zhang, Kaizhe Hu, Yingqian Huang, Yuanchen Ju, Zhengrong Xue, Huazhe Xu

<details>
<summary> 日本語要旨 </summary>

最近のロボット操作における現代的な模倣学習手法は成功を収めているものの、その性能は特定のオブジェクト形状に限られがちであり、これはデータ多様性の制約に起因しています。提案されたAffordGenフレームワークは、強力な3D生成モデルとビジョンファウンデーションモデル（VFM）を活用し、大規模な3Dメッシュ間の意味的対応関係に基づく重要なキーポイントを利用して新たなロボット操作トラジェクトリを生成することでこの制約を克服します。この大規模かつアフォードアンス認識型のデータセットは、アフォードアンスの意味的汎用性とエンドツーエンド学習における反応的な堅牢性を組み合わせた強力で閉ループ型の視覚運動ポリシーのトレーニングに使用されます。シミュレーションと現実世界の実験では、AffordGenを用いてトレーニングされたポリシーが高い成功率を達成し、本当に未見のオブジェクトへのゼロショット一般化を可能にすることが示されました。これはロボット学習におけるデータ効率性を大幅に向上させます。
</details>

<details>
<summary> 英語要旨 </summary>

Despite the recent success of modern imitation learning methods in robot manipulation, their performance is often limited to specific object shapes due to the constrained data diversity. Leveraging powerful 3D generative models and vision foundation models (VFM), the proposed AffordGen framework overcomes this limitation by utilizing the semantic correspondence of meaningful keypoints across large-scale 3D meshes to generate new robot manipulation tra-jectories. This large-scale, affordance-aware dataset is then used to train a robust, closed-loop visuomotor policy, combining the semantic generalizability of affordances with the reactive robustness of end-to-end learning. Experiments in simulation and the real world show that policies trained with AffordGen achieve high success rates and enable zero-shot generalization to truly unseen objects, significantly im-proving data efficiency in robot learning.
</details>

---

### Robust Remote Sensing Image–Text Retrieval with Noisy Correspondence
著者: qiya song, Yiqiang Xie, Yuan Sun, Renwei Dian, Xudong Kang

<details>
<summary> 日本語要旨 </summary>

遠隔センシング画像-テキスト検索（RSITR）は、遠隔視覚と言語理解をつなぐ重要なタスクであり、近年多くの研究関心を集めています。しかし、ほとんどのRSITR手法は画像-テキストペアが完全に一致していることを暗黙的に仮定しています。実際には、大規模なよく整列したデータペアセットを取得するのは非常に高価であったり不可能である場合が多いです。いくつかの研究ではノイズの存在を認識していますが、そのようなノイズに対するニューラルネットワークの堅牢性をどのように確保するかについてはほとんど研究されていません。これらの観察に基づき、RSITRにおける重要で未解決の問題であるノイズ付き対応（NC）を明らかにします。この課題を克服するために、私たちは人間の認知学習パターンを模倣する自己ペース学習戦略を設計した新しい堅牢な遠隔センシング画像-テキスト検索（RRSITR）の枠組みを提案します。これにより、NCを伴うマルチモーダルデータから簡単なものから難しいものへと学習することができます。具体的には、すべてのトレーニングサンプルペアを各ペアの損失大きさに基づいて3つのカテゴリー（クリーンサンプルペア、曖昧なサンプルペア、ノイズのあるサンプルペア）に分けます。次に、各トレーニングペアの信頼性を損失値に基づいて重みを割り当てることで推定します。さらに、サンプルのトレーニングシーケンスと重みを動的に制御する新しい自己ペース関数をそれぞれ設計し、進行的な学習過程を確立します。最後に、ノイズのあるサンプルペアに対しては、セマンティック類似度に基づいて動的に調整される強化トリプレット損失を提示し、ノイズに対する堅牢性を向上させます。3つの人気のあるベンチマークデータセットで行った広範な実験では、提案されたRRSITRが特に高いノイズ率で状態・オブ・ザ・アート手法を大きく上回ることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

As a pivotal task that bridges remote visual and linguistic understanding, Remote Sensing Image-Text Retrieval (RSITR) has attracted considerable research interest in recent years. However, almost all RSITR methods implicitly assume that image-text pairs are matched perfectly. In practice, acquiring a large set of well-aligned data pairs is often prohibitively expensive or even infeasible. Although several studies have acknowledged the presence of noisy pairs, little work has explored how to endow neural networks with robustness against such noise. Based on the above observations, we reveal an important but untouched problem in RSITR, i.e., Noisy Correspondence (NC). To overcome these challenges, we propose a novel Robust Remote Sensing Image–Text Retrieval (RRSITR) paradigm that designs a self-paced learning strategy to mimic human cognitive learning patterns, thereby learning from easy to hard from multi-modal data with NC. Specifically, we first divide all training sample pairs into three categories based on the loss magnitude of each pair, i.e., clean sample pairs, ambiguous sample pairs, and noisy sample pairs. Then, we respectively estimate the reliability of each training pair by assigning a weight to each pair based on the values of the loss. Further, we respectively design a new self-paced function to dynamically regulate the training sequence and weights of the samples, thus establishing a progressive learning process. Finally, for noisy sample pairs, we present an enhanced triplet loss to dynamically adjust the soft margin based on semantic similarity, thereby enhancing the robustness against noise. Extensive experiments on three popular benchmark datasets demonstrate that the proposed RRSITR significantly outperforms the state-of-the-art methods, especially in high noise rates.
</details>

---

### ARGUS: Defending Against Multimodal Indirect Prompt Injection Via Steering Instruction-Following Behavior
著者: Weikai Lu, Ziqian Zeng, Kehua Zhang, Haoran Li, Huiping Zhuang, Ruidong Wang, Cen Chen, Hao Peng

<details>
<summary> 日本語要旨 </summary>

多モーダル大規模言語モデル（MLLMs）は、画像、ビデオ、または音声に悪意のある指示を埋め込むことでモデルの動作を乗っ取ろうとする多モーダル間接プロンプト注入（IPI）攻撃にますます脆弱です。これらの多モーダル脅威に対抗するために設計された既存の防御策は、主にテキスト専用LLMs向けであり、容易に回避されるか、モダリティ依存であったり、一般化が悪いため不適切です。活性化方向付けの研究に触発され、私たちは、表現空間内でモデルの動作を誘導することにより、モダリティに依存しない堅牢な一般的防御が達成可能であると仮定しました。広範囲の実験を通じて、私たちはMLLMsの指示に従う挙動がサブスペース内にエンコードされていることを発見しました。このサブスペース内の方向に沿って誘導することで、ユーザーの指示への従順性を強制でき、防御の基礎が形成されます。しかし、私たちはまた、単純な防御方向が有用性低下方向と結合する可能性があり、過度の介入強度がモデルパフォーマンスを悪化させることも発見しました。これに対処するために、私たちはARGUSを提案します。これは安全性低下方向から分離された最適な防御方向を安全性サブスペース内で検索し、さらに適応強度誘導を組み合わせてより良い安全性-有用性のトレードオフを実現します。ARGUSはまた、必要に応じて防御を活性化するための軽量な注入検出段階と、防御成功を確認するポストフィルタリング段階を導入します。実験結果は、ARGUSが多モーダルIPIに対して堅牢な防御を達成しつつ、MLLMの有用性を最大限に保持できることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Multimodal Large Language Models (MLLMs) are increasingly vulnerable to multimodal Indirect Prompt Injection (IPI) attacks, which embed malicious instructions in images, videos, or audio to hijack model behavior. Existing defenses, designed primarily for text-only LLMs, are unsuitable for countering these multimodal threats, as they are easily bypassed, modality-dependent, or generalize poorly. Inspired by activation steering researches, we hypothesize that a robust, general defense independent of modality can be achieved by steering the model's behavior in the representation space. Through extensive experiments, we discover that the instruction-following behavior of MLLMs is encoded in a subspace. Steering along directions within this subspace can enforce adherence to user instructions, forming the basis of a defense. However, we also found that a naive defense direction could be coupled with a utility-degrading direction, and excessive intervention strength harms model performance. To address this, we propose ARGUS, which searches for an optimal defense direction within the safety subspace that decouples from the utility degradation direction, further combining adaptive strength steering to achieve a better safety-utility trade-off. ARGUS also introduces lightweight injection detection stage to to activate the defense on-demand, and a post-filtering stage to verify defense success. Experimental results show that ARGUS can achieve robust defense against multimodal IPI while maximally preserving the MLLM's utility.
</details>

---

### When Visualizing Is The First Step to Reasoning: MIRA, A Benchmark for Visual Chain-of-Thought
著者: Yiyang Zhou, Haoqin Tu, Zijun Wang, Zeyu Wang, Niklas Muennighoff, Fan Nie, Chaorui Deng, Shen Yan, Haoqi Fan, Yejin Choi, James Zou, Cihang Xie, Huaxiu Yao, Qinghao Ye

<details>
<summary> 日本語要旨 </summary>

私たちは、中間の視覚的な画像を生成することが成功した推論に不可欠であるシナリオでモデルを評価する新しい基準としてMIRA（Multimodal Imagination for Reasoning Assessment）を提案します。従来のチェーン・オブ・スローグ（CoT）手法がテキストに依存するのに対し、MIRAのタスクではモデルが中間画像を生成して利用する必要があります。これらはスケッチ、構造図、または経路図などであり、推論プロセスを導くために使用されます。この設定は、「考えるための描画」として人間が複雑な問題を解決する方法に近いものです。これを解決するため、MIRAは本質的に挑戦的であり、言語だけでは表現しづらい複雑な構造、空間関係、または推論ステップ（例えば、ボード上のダイスの動きを追跡し、各投げた後に裏向きの値を合計する）を含むタスクに焦点を当てます。私たちの評価データが高品質であることを確保するために、中間視覚的な画像と最終答えで注釈された546のマルチモーダル問題を含みます。また、MIRA用の統一評価プロトコルも提案し、3つのレベルの評価入力にわたります：画像と質問のみの直接入力、画像と思考プロンプトを含むテキスト-チェーン・オブ・スローグ（Text-CoT）入力、そしてアノテートされた画像手がかりとテキスト的な思考プロンプトの両方を含むビジュアル-チェーン・オブ・スローグ（Visual-CoT）入力です。私たちの基準におけるモデル容量の上限を探るため、異なるk設定でのpass@kと多数決投票精度も報告します。実験結果は、テキストプロンプトに依存する場合、最強のプライベートモデル（例えばGPT-5、o3、Gemini 2.5 Pro）や強力なオープンウェイトモデル（例えばQwen2.5-VL、GLM 4.5V）を含む既存のマルチモーダル大規模言語モデル（MLLMs）が悪いパフォーマンスを示すことを示しています。しかし、中間視覚的な手がかりが提供されると、モデルのパフォーマンスは一貫して改善し、全てのモデルとタスクにわたって平均相対的な増加率33.7%を達成します。また、検索空間を拡大し、Visual-CoTに整合したテキストプロンプトを設計することで上限を探りますが、どちらも私たちのビジュアル-チェーン・オブ・スローグ設定に比べて限定的な改善しか示しません。これらの結果は、MIRA上で成功した推論を可能にする想像された視覚情報の重要な役割を強調しています。
</details>

<details>
<summary> 英語要旨 </summary>

We propose MIRA (Multimodal Imagination for Reasoning Assessment), a new benchmark designed to evaluate models in scenarios where generating intermediate visual images is essential for successful reasoning. Unlike traditional Chain-of-thought (CoT) methods that rely solely on text, tasks in MIRA require models to generate and utilize intermediate images --- such as sketches, structural diagrams, or path drawings --- to guide their reasoning process. This setup closely mirrors how humans solve complex problems through "drawing to think". To solve this, MIRA focuses on tasks that are intrinsically challenging and involve complex structures, spatial relationships, or reasoning steps that are difficult to express through language alone (e.g., tracking a die’s movement on a board and summing the face-down values after each roll). To ensure that our evaluation data is of high-quality, we include 546 multimodal problems, annotated with intermediate visual images and final answers. We also propose a unified evaluation protocol for MIRA that spans three levels of evaluation input: direct input with image and question only, text-only CoT (Text-CoT) input with image and thinking prompts, and Visual-CoT input with both annotated image clues and textual thinking prompts. To probe the upper bound of model capacity on our benchmark, we also report pass@k and majority voting accuracies under different k settings. Experimental results show that existing multimodal large language models (MLLMs), including strongest private models (e.g., GPT-5, o3, Gemini 2.5 Pro) as well as strong open-weight models (e.g., Qwen2.5-VL, GLM 4.5V), perform poorly when relying solely on textual prompts. However, when intermediate visual cues are provided, model performance improves consistently, yielding an average relative gain of 33.7% across all models and tasks. We also probe the upper bound by expanding the search space and designing textual prompts aligned with Visual-CoT, but both yield only limited improvements compared to our Visual-CoT setting. These results underscore the critical role of imagined visual information in enabling successful reasoning on MIRA.
</details>

---

### FlexAvatar: Flexible Large Reconstruction Model for Animatable Gaussian Head Avatars with Detailed Deformation
著者: Cheng Peng, Zhuo Su, Liao Wang, Chen Guo, Zhaohu Li, Chengjiang Long, Zheng Lv, Jingxiang Sun, Chenyangguang Zhang, Yebin Liu

<details>
<summary> 日本語要旨 </summary>

私たちは、カメラの姿勢や表情ラベルを必要とせずに、単一または少数の画像から高精度な3Dヘッドアバターを再構築する柔軟性のある大規模モデルであるFlexAvatarを提案します。このモデルは、カメラ姿勢や表情に依存しない入力数に対応した構造化された頭部クエリトークンを基準として使用し、それらの入力を堅牢な3Dカノニカル表現に集約する変換器ベースの再構築モデルを活用します。詳細な動的歪みのために、UV空間位置マップで条件付けられた軽量なUNetデコーダーを導入し、これによりリアルタイムで表情依存の詳細な歪みを生成することが可能です。さらに、皺やむき出しの歯などの希少だが重要な表情をより良く捉えるために、トレーニングセット内でこれらの表情の分布をバランスするデータ分布調整戦略も採用しています。また、軽量な10秒間のリファインメントにより、極端なアイデンティティにおける個別の詳細をさらに向上させつつ、歪みの品質に影響を与えません。広範な実験により、FlexAvatarが3D一貫性と動的リアリズムの詳細面で従来の方法を上回ることが示されており、アニメーション可能な3Dアバター作成の実用的なソリューションを提供しています。
</details>

<details>
<summary> 英語要旨 </summary>

We present FlexAvatar, a flexible large reconstruction model for high-fidelity 3D head avatars with detailed dynamic deformation from single or sparse images, without requiring camera poses or expression labels. It leverages a transformer-based reconstruction model with structured head query tokens as canonical anchor to aggregate flexible input-number-agnostic, camera-pose-free and expression-free inputs into a robust canonical 3D representation. For detailed dynamic deformation, we introduce a lightweight UNet decoder conditioned on UV-space position maps, which can produce detailed expression-dependent deformations in real time. To better capture rare but critical expressions like wrinkles and bared teeth, we also adopt a data distribution adjustment strategy during training to balance the distribution of these expressions in the training set. Moreover, a lightweight 10-second refinement can further enhances identity-specific details in extreme identities without affecting deformation quality. Extensive experiments demonstrate that our FlexAvatar achieves superior 3D consistency, detailed dynamic realism compared with previous methods, providing a practical solution for animatable 3D avatar creation.
</details>

---

### OneStory: Coherent Multi-Shot Video Generation with Adaptive Memory
著者: Zhaochong An, Menglin Jia, Haonan Qiu, Zijian Zhou, Xiaoke Huang, Zhiheng Liu, Weiming Ren, Kumara Kahatapitiya, Ding Liu, Sen He, Chenyang Zhang, Tao Xiang, Fanny Yang, Serge Belongie, Tian Xie

<details>
<summary> 日本語要旨 </summary>

現実世界のビデオにおけるストーリーテリングは、しばしば複数のショットを通じて展開されます。これらのショットは連続していないものの、意味的につながり合っており、一貫した物語を伝えるために協力します。しかし、既存のマルチショットビデオ生成（MSV）手法は、限られた時間枠や単一キーフレーム条件付けに依存しており、複雑な物語に対するパフォーマンスが低下します。これは長距離のクロスショットコンテキストを効果的にモデル化できていないためです。本研究では、OneStoryという手法を提案し、一貫性のあるかつ拡張可能なナラティブ生成のためのグローバルでありながらコンパクトなクロスショットコンテキストモデリングを可能にします。OneStoryはMSVを次のショット生成タスクとして再定式化し、自己回帰的なショット合成を可能にしつつ、事前学習済みの画像から動画（I2V）モデルを活用した強力な視覚条件付けを行います。私たちは二つの重要なモジュールを導入します：フレーム選択モジュールは、以前のショットからの情報豊富なフレームに基づいて意味的に関連するグローバルメモリを構築し、アダプティブコンディショナーは重要性ガイド付きのパッチ化を行い、直接条件付け用のコンパクトなコンテキストを生成します。また、リファレンスキャプションを含む高品質なマルチショットデータセットを編纂し、現実世界のストーリーテリングパターンを反映させます。次のショットパラダイムに基づいた効果的なトレーニング戦略も設計します。事前学習済みI2Vモデルから、私たちが編纂した60Kデータセットで微調整されたOneStoryは、テキストおよび画像条件付けの両方において、多様かつ複雑なシーンにわたるナラティブの一貫性を最先端で達成します。これにより、制御可能で没入感のある長編ビデオストーリーテリングが可能となります。私たちのモデルとデータは論文と共に公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Storytelling in real-world videos often unfolds through multiple shots—discontinuous yet semantically connected clips that together convey a coherent narrative. However, existing multi-shot video generation (MSV) methods struggle to effectively model long-range cross-shot context, as they rely on limited temporal windows or single keyframe conditioning, leading to degraded performance under complex narratives. In this work, we propose OneStory, enabling global yet compact cross-shot context modeling for consistent and scalable narrative generation. OneStory reformulates MSV as a next-shot generation task, enabling autoregressive shot synthesis while leveraging pretrained image-to-video (I2V) models for strong visual conditioning. We introduce two key modules: a Frame Selection module that constructs a semantically-relevant global memory based on informative frames from prior shots, and an Adaptive Conditioner that performs importance-guided patchification to generate compact context for direct conditioning. We further curate a high-quality multi-shot dataset with referential captions to mirror real-world storytelling patterns, and design effective training strategies under the next-shot paradigm. Finetuned from a pretrained I2V model on our curated 60K dataset, OneStory achieves state-of-the-art narrative coherence across diverse and complex scenes in both text- and image-conditioned settings, enabling controllable and immersive long-form video storytelling. Our model and data will be released with the paper.
</details>

---

### Same or Not? Enhancing Visual Perception in Vision-Language Models
著者: Damiano Marsili, Aditya Mehta, Ryan Lin, Georgia Gkioxari

<details>
<summary> 日本語要旨 </summary>

視覚言語モデル（VLMs）は広範な視覚理解に優れていますが、粗雑であり、視覚的バイアスを持ち、微細な視覚的詳細を見逃してしまうことがあります。既存のトレーニングコーパスはこの制限を強化する傾向にあり、一般的な認識（「それは猫か犬か？」）を細部への知覚よりも重視しています。これに対処するため、VLMsの知覚能力を向上させる新しいトレーニングコーパスとタスクを導入します。TWINは、モデルが2つの類似した画像が同じオブジェクトを描写しているかどうかを判断するように設計された561,000対の画像ペアクエリからなる大規模データセットです。これは微細な視覚的手がかりへの注意を促します。このデータセットは、日常生活で見られる多様なオブジェクトにわたり、文脈、視点、外観をカバーしています。TWINでVLMsを微細認識の向上が得られます。これは芸術、動物、植物、ランドマークなど未見の領域でも当てはまります。これらの向上を定量化するために、FGVQAという12,000のクエリから成るベンチマークスイートを導入します。これは複数のドメインからの微細認識および検索データセットを再利用しています。既存のVLMsはFGVQAで苦戦する一方、TWINで微調整されると最大19.3%改善し、一般的なVQAベンチマークにおけるパフォーマンスを損なうことはありません。最後に、私たちのTWINデータセットはオブジェクト注釈と良好にスケールし、分析からスケールがパフォーマンスにおいて重要であることが示されます。私たちはTWINを将来のモデルの知覚精度を進化させるオープンソースVLMトレーニングコーパスへのドロップイン追加として想定します。
</details>

<details>
<summary> 英語要旨 </summary>

Vision–language models (VLMs) excel at broad visual understanding but remain coarse-grained, exhibit visual biases, and miss subtle visual details. Existing training corpora reinforce this limitation by emphasizing general recognition (“Is it a cat or a dog?”) over fine-grained perception. To address this, we introduce a new training corpus and task designed to enhance the perceptual abilities of VLMs. TWIN is a large-scale dataset of 561,000 image-pair queries that task models to determine whether two visually similar images depict the same object, encouraging attention to nuanced visual cues. The dataset spans a diverse range of everyday objects across contexts, viewpoints, and appearances. Fine-tuning VLMs on TWIN yields notable gains in fine-grained recognition, even on unseen domains such as art, animals, plants, and landmarks. To quantify these gains, we introduce FGVQA, a benchmark suite of 12,000 queries that repurposes fine-grained recognition and retrieval datasets from multiple domains. While existing VLMs struggle on FGVQA, when fine-tuned on TWIN they improve by up to 19.3%, without compromising performance on general VQA benchmarks. Finally, our TWIN dataset scales favorably with object annotations, and our analysis shows that scale is key to performance. We envision TWIN as a drop-in addition to open-source VLM training corpora, advancing perceptual precision of future models.
</details>

---

### Semantic Context Matters: Improving Conditioning for Autoregressive Models
著者: Dongyang Jin, Ryan Xu, Jianhao Zeng, Rui Lan, Yancheng Bai, Lei Sun, Xiangxiang Chu

<details>
<summary> 日本語要旨 </summary>

最近、自己回帰（AR）モデルは画像生成において強力な可能性を示しています。これらのモデルは、拡散法と比較してスケーラビリティが高く、統一されたマルチモーダルモデルへの統合も容易です。しかし、ARモデルを制御可能な画像編集に拡張することは依然として困難であり、その理由は効率的でない条件付け戦略がしばしば最適でない意味の整合性や視覚品質を引き起こすためです。この制限に対処するため、私たちは自己回帰モデル向けのセマンティックコンテキスト駆動法であるSCARを提案します。SCARは圧縮セマンティックプリフィリングとセマンティックアライメントガイダンスを導入し、これらが共同して文脈理解と生成の一貫性を向上させます。従来の方法は希薄な視覚トークンやデコーディング段階への注入に依存していましたが、SCARは入力段階から強力なセマンティックガイダンスを可能にし、モデル非依存であり、次トークンおよび次スケールの両方のARパラダイムに適用可能です。指示編集と制御可能な生成に関する広範な実験は、私たちの方法が視覚的忠実度とセマンティックアライメントを大幅に改善し、既存のARベースの手法を上回りつつ制御可能性を維持することを示しています。すべてのコードはリリースされます。
</details>

<details>
<summary> 英語要旨 </summary>

Recently, autoregressive (AR) models have shown strong potential in image generation, offering better scalability and easier integration with unified multi-modal models compared to diffusion methods. However, extending AR models to controllable image editing remains challenging due to weak and inefficient conditioning strategies, which often lead to suboptimal semantic alignment and visual quality. To address this limitation, we present SCAR, a Semantic-Context-driven method for AutoregRessive models. SCAR introduces Compressed Semantic Prefilling and Semantic Alignment Guidance that jointly enhance contextual understanding and generation coherence. Unlike prior methods that rely on sparse visual tokens or decoding stage injection, SCAR enables strong semantic guidance from the input stage, while remaining model-agnostic and applicable to both next-token and next-scale AR paradigms. Extensive experiments on instruction editing and controllable generation demonstrate that our method significantly improves visual fidelity and semantic alignment, outperforming existing AR-based methods while maintaining controllability. All the code will be released.
</details>

---

### Matching Every Pair to Track Every Point: PairFormer for All-Pairs Tracking and Video Trajectory Fields
著者: Guangyang Wu, Youran Ding, Xinyu Che, BENYUAN SUN, Yi Yang, Xiaohong Liu

<details>
<summary> 日本語要旨 </summary>

トラッキング・アニ・ポイント（TAP）はクエリ条件付きの対応を解決しますが、ビデオの密な全ペア構造を暗黙的に残しています。私たちはAll-Pairs Tracking（APT）を定式化しました：与えられたビデオから、すべてのソースターゲットフレームペアに対する密な変位と可視性を予測し、そこからピクセル単位の軌跡を読み取ります。このために、APTを一回通過で解決するフィードフォワードトランスフォーマーであるPairFormerを提案します。スペースタイムパッチエンコーダはすべてのフレームに対して時間条件付き特徴を計算します。CorrBankは各フレームペア用に学習可能な相関記憶を構築し、そこからペアワイズ動作トークンを取得します。ブロードキャスト動作ミキサーは空間と時間をまたいで情報を集約し、グローバルコンテキストでこれらのトークンを洗練します。その後、軌跡ヘッドが各ペアに対するフル解像度変位を予測し、一貫した全ペア軌跡場を生成します。APTのスケールでのサポートを目的として、密な注釈付きの写実的動態シーンを合成するデータプラットフォームであるPAIRenderを開発しました。PAIRenderからトレーニングセット（$\pi$-R10K）と全対全評価プロトコルを持つベンチマーク（APT-Bench）を導出します。実験により、PairFormerがAPT-Benchで強力な性能を示し、標準TAPベンチマークでも競争力のある結果を達成することがわかりました。コードとデータセットは発表時に公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Tracking-any-point (TAP) answers query-conditioned correspondence but leaves the dense, all-pairs structure of a video implicit. We formulate All-Pairs Tracking (APT): given a video, predict dense displacement and visibility for every source-target frame pair, from which per-pixel trajectories can be read out. To this end, we propose PairFormer, a feed-forward transformer that addresses APT in a single pass. A spatio-temporal patch encoder computes temporally conditioned features for all frames. CorrBank constructs a learnable correlation memory for each frame pair to obtain pairwise motion tokens. A broadcast motion mixer aggregates information across space and time and refines these tokens with global context. A trajectory head then predicts full-resolution displacement for each pair, yielding a coherent all-pairs trajectory field. To support APT at scale, we develop PAIRender, a data platform that synthesizes photo-realistic dynamic scenes with dense annotations. From PAIRender we derive a training set ($\pi$-R10K) and a benchmark (APT-Bench) with an all-to-all evaluation protocol. Experiments show that PairFormer achieves strong performance on APT-Bench and competitive results on standard TAP benchmarks. Code and dataset will be released upon publication.
</details>

---

### Customized Fusion: A Closed-Loop Dynamic Network for Adaptive Multi-Task-Aware Infrared-Visible Image Fusion
著者: Zengyi Yang, Yu Liu, Juan Cheng, Zhiqin Zhu, Yafei Zhang, Huafeng Li

<details>
<summary> 日本語要旨 </summary>

赤外線と可視画像の融合は、堅牢な視覚理解を実現するために補完的な情報を統合しようとしますが、既存の融合手法は多様な下流タスクへの同時適応に苦労しています。この問題に対処するために、私たちはダウンストリームタスクのセマンティック要件に応じて適応的に反応し、タスクカスタマイズされた画像融合を実現する閉ループ動的ネットワーク（CLDyN）を提案します。具体的には、CLDyNは要件駆動型セマンティック補償（RSC）モジュールを通じてダウンストリームタスクからフュージョンネットワークへの明示的なフィードバックを実現する閉ループ最適化メカニズムを導入し、セマンティック伝送チェーンを確立します。RSCモジュールは基底ベクトル銀行（BVB）とアーキテクチャ適応型セマンティック注入（A2SI）ブロックを利用して、タスク要件に応じてネットワークアーキテクチャをカスタマイズし、タスク特化のセマンティック補償を可能にします。これにより、再トレーニングなしでフュージョンネットワークが多様なタスクへ積極的に適応することができます。正確なセマンティック補償を促進するため、タスクパフォーマンスの変動に基づいてRSCモジュールを報酬または罰則で評価する報酬-罰則戦略が導入されます。M3FD、FMB、VT5000データセットの実験結果により、CLDyNは高品質な融合を維持しつつ、強力なマルチタスク適応性も示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Infrared-visible image fusion aims to integrate complementary information for robust visual understanding, but existing fusion methods struggle with simultaneously adapting to multiple downstream tasks. To address this issue, we propose a Closed-Loop Dynamic Network (CLDyN) that can adaptively respond to the semantic requirements of diverse downstream tasks for task-customized image fusion. Specifically, CLDyN introduces a closed-loop optimization mechanism that establishes a semantic transmission chain to achieve explicit feedback from downstream tasks to the fusion network through a Requirement-driven Semantic Compensation (RSC) module. The RSC module leverages a Basis Vector Bank (BVB) and an Architecture-Adaptive Semantic Injection (A2SI) block to customize the network architecture according to task requirements, thereby enabling task-specific semantic compensation and allowing the fusion network to actively adapt to diverse tasks without retraining. To promote accurate semantic compensation, a reward-penalty strategy is introduced to reward or penalize the RSC module based on task performance variations. Experiments on the M3FD, FMB, and VT5000 datasets demonstrate that CLDyN not only maintains high fusion quality but also exhibits strong multi-task adaptability.
</details>

---

### Mesh-Pro: Asynchronous Advantage-guided Ranking Preference Optimization for Artist-style Quadrilateral Mesh Generation
著者: Zhen Zhou, Jian Liu, Biwen Lei, Jing Xu, Haohan Weng, Yiling Zhu, Zhuo Chen, Junfeng Fan, Yunkai Ma, Dazhao Du, Song Guo, Fengshui Jing, Chunchao Guo

<details>
<summary> 日本語要旨 </summary>

強化学習（RL）はテキストや画像生成において顕著な成功を収めていますが、3D生成の可能性はまだ十分に探求されていません。既存の試みは通常、オフライン直接優先度最適化（DPO）法に依存しており、これは訓練効率が低く一般化能力が限られています。本研究では、3Dメッシュ生成におけるRLの訓練効率と生成品質を向上させることを目指します。具体的には、(1) 訓練効率改善後に初めて設計された3Dメッシュ生成用の非同期オンラインRLフレームワークを提案し、これは従来の同期RLよりも3.75倍速いです。(2) 訓練効率と一般化能力のバランスが良好な新しいRLアルゴリズムであるAdvantage-guided Ranking Preference Optimization（ARPO）を提案します。これは、3Dメッシュ生成用に設計された現在のRLアルゴリズム（例えば、DPOやGroup Relative Policy Optimization（GRPO））よりも優れています。(3) 非同期ARPOを基に、新しい対角線認識混合三角形四辺形トークン化をメッシュ表現に導入すると共に、幾何学的整合性のためのレイベース報酬を追加したMesh-Proを提案します。Mesh-Proは芸術的および密なメッシュで最先端のパフォーマンスを達成しています。コードは近日公開予定です。
</details>

<details>
<summary> 英語要旨 </summary>

Reinforcement learning (RL) has demonstrated remarkable success in text and image generation, yet its potential in 3D generation remains largely unexplored. Existing attempts typically rely on offline direct preference optimization (DPO) method, which suffers from low training efficiency and limited generalization. In this work, we aim to enhance both the training efficiency and generation quality of RL in 3D mesh generation. Specifically, (1) we design the first asynchronous online RL framework tailored for 3D mesh generation post-training efficiency improvement, which is 3.75$\times$ faster than synchronous RL. (2) We propose Advantage-guided Ranking Preference Optimization (ARPO), a novel RL algorithm that achieves a better trade-off between training efficiency and generalization than current RL algorithms designed for 3D mesh generation, such as DPO and group relative policy optimization (GRPO). (3) Based on asynchronous ARPO, we propose Mesh-Pro, which additionally introduces a novel diagonal-aware mixed triangular-quadrilateral tokenization for mesh representation and a ray-based reward for geometric integrity. Mesh-Pro achieves state-of-the-art performance on artistic and dense meshes. Code will be available soon.
</details>

---

### Dynamic Important Example Mining for Reinforcement Finetuning
著者: Haoru Tan, WU Sitong, Yanfeng Chen, Shizhen Zhao, Yangtian Sun, Tianjia Liu, Chirui Chang, Shaofeng Zhang, Xingwu Sun, Xiuzhe Wu, Ruobing Xie, Xiaojuan Qi

<details>
<summary> 日本語要旨 </summary>

強化微調整（RFT）は、大規模モデルの推論能力を向上させるためにますます使用されていますが、その効果はトレーニングデータの選択と利用方法によって制限されています。ほとんどのデータ中心のRFT手法は、サンプルの価値が訓練中一定であるという暗黙の前提に基づいた静的またはヒューリスティックなサンプル選択に依存しています。これにより、ポリシー学習の非定常的ダイナミクスが見落とされ、最適でない更新が生じる可能性があります。私たちは**動的重要例採掘（DIEM）**を提案します。これはデータ利用をRFT全体を通して適応させる原則に基づき、完全自動化されたフレームワークです。DIEMは各最適化ステップに以下の2つのコンポーネントを統合します：（i）勾配整列重要度推定器であり、これは効率的に各サンプルがポリシー改善に対してもたらす限界貢献を近似する；および（ii）制約付きバッチ再重み付けスキームであり、これは最適化の安定性を保つために更新の勾配大きさを保存しつつ、総合的な有用性を最大化します。このアプローチにより、データ選択が一度限りの前処理ヒューリスティックから学習アルゴリズムの固有部分へと変わります。これにより、外部スコアではなくモデルダイナミクスによって駆動される自己組織化型、カリキュラムのような訓練軌道が生まれます。多様なマルチモーダル推論ベンチマークにおいて、DIEMは強力な静的および動的ベースラインを一貫して上回り、基本RFTアルゴリズムのパフォーマンス向上を約**1%から6%**提供します。これには訓練オーバーヘッドがわずか**1.2%**しか追加されません。
</details>

<details>
<summary> 英語要旨 </summary>

Reinforcement fine-tuning (RFT) is increasingly used to strengthen the reasoning abilities of large models, yet its effectiveness is bounded by how training data are selected and used. Most data-centric RFT methods rely on static or heuristic sample selection, implicitly assuming a sample’s value is fixed over training. This overlooks the non-stationary dynamics of policy learning and can lead to suboptimal updates. We propose **Dynamic Important Example Mining (DIEM)**, a principled and fully automated framework that makes data utilization adaptive throughout RFT. DIEM integrates two components into each optimization step: (i) a gradient-alignment importance estimator that efficiently approximates each sample’s marginal contribution to policy improvement; and (ii) a constrained batch reweighting scheme that maximizes aggregate utility while preserving the update’s gradient magnitude to stabilize optimization. This converts data selection from a one-time preprocessing heuristic into an intrinsic part of the learning algorithm, yielding a self-organizing, curriculum-like training trajectory driven by model dynamics rather than external scores. Across several multimodal reasoning benchmarks, DIEM consistently outperforms strong static and dynamic baselines, providing a significant performance uplift to the base RFT algorithm of approximately **1%** to **6%**, while introducing only a minimal **1.2%** training overhead.
</details>

---

### Dataset Distillation Via Influence Matching
著者: Haoru Tan, Wang Wang, WU Sitong, Xiuzhe Wu, Yangtian Sun, Chirui Chang, Shaofeng Zhang, Xiaojuan Qi

<details>
<summary> 日本語要旨 </summary>

データセットの蒸留を結果中心的な視点から再考します。プロセスの代理（ステップごとの勾配やトレーニングの軌跡）を整合させるのではなく、Influence Matching (**Inf-Match**) は最終的なトレーニングの成果を整合させます。具体的には、収束したパラメータへの影響がフルデータセットと同じであるコンパクトな合成セットを学習します。我々は逆ヘッシアン積や凹性仮定を必要とせずに、パラメータのシフトをデータの追加または削除によって量子化する完全に微分可能なサンプルレベルの影響推定器を導入します。この推定器は最適化ダイナミクスを展開し、一次テイラー近似を適用することで線形時間で動作します。その後、合成セットを学習するために、その影響と実データセットの影響の不整合を最小化し、結果の整合性ではなくヒューリスティックなプロセスの模倣を達成します。**Inf-Match** は標準的な分類ベンチマークで最高の精度を提供します。例えば、Tiny-ImageNet (IPC=10) では **Inf-Match** が31.5% を達成し、NCFM に対して+4.7% の改善を示します。分類のみならず、**Inf-Match** はFlickr30Kでのビジョン言語蒸留にもスケールし、強力なプロセスマッチングベースラインを上回ります。例えば、200から1000の合成サンプルを使用した場合、我々の方法は画像/テキスト検索タスクで平均値がNCFMより2.5%高い印象的なリーダーシップを達成しました。
</details>

<details>
<summary> 英語要旨 </summary>

We revisit dataset distillation from an outcome-centric perspective. Rather than aligning process surrogates (per-step gradients or training trajectories), Influence Matching (**Inf-Match**) aligns the final outcome of training: it learns a compact synthetic set whose effect on the converged parameters matches that of the full dataset. Concretely, we introduce a fully differentiable, sample-level influence estimator that quantifies parameter shifts from adding or removing data-- without time-consuming inverse-Hessian products or convexity assumptions. The estimator runs in linear time by unrolling the optimization dynamics and applying a first-order Taylor approximation. We then learn the synthetic set by minimizing the mismatch between its influence and that of the real dataset, yielding outcome alignment rather than heuristic process imitation. **Inf-Match** delivers the best accuracy across standard classification benchmarks. For instance, on Tiny-ImageNet (IPC=10), **Inf-Match** attains 31.5\%, a +4.7\% improvement over NCFM. Beyond classification, **Inf-Match** scales to vision-language distillation on Flickr30K, outperforming strong process-matching baselines. For instance, with 200 to 1000 synthetic samples, our method achieved a leading impressive average on image/text retrieval tasks, higher than NCFM by 2.5\%.
</details>

---

### CoD: A Diffusion Foundation Model for Image Compression
著者: Zhaoyang Jia, Zihan Zheng, Naifu Xue, Jiahao Li, Bin Li, Zongyu Guo, Xiaoyi Zhang, Houqiang Li, Yan Lu

<details>
<summary> 日本語要旨 </summary>

既存の拡散コーデックは、Stable Diffusionのようなテキストから画像への拡散ベースモデルに基づいて構築されることが多いです。しかし、テキスト条件付けは圧縮観点から最適ではなく、特に超低ビットレートでの下流拡散コーデックの可能性を制限しています。これに対処するために、私たちは初めてのCompression-oriented Diffusion（圧縮指向拡散）ベースモデルであるCoDを導入します。これは、圧縮と生成の両方のエンドツーエンド最適化を可能にするためにゼロからトレーニングされています。CoDは固定コーデックではなく、さまざまな拡散ベースコーデック用の一般的なベースモデルとして設計されています。以下のような複数の利点を提供します：高い圧縮効率、下流コーデックであるDiffCにCoDを導入することでSOTA（State of the Art）結果が得られます。特に超低ビットレート（例えば0.0039 bpp）では顕著です；低コストかつ再現可能なトレーニング、Stable Diffusionの約300倍速いトレーニングが可能であり（約20日対約6,250 A100 GPU日）、完全にオープンな画像のみのデータセットを使用しています；新たな洞察を提供します。例えば、ピクセル空間拡散がVTMレベルのPSNR（ピーク信号対雑音比）を高い知覚品質で達成し、より少ないパラメータでGANベースコーデックを上回ることがわかりました。私たちはCoDが将来の拡散コーデック研究の基盤になることを期待しています。ソースコードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Existing diffusion codecs typically build on text-to-image diffusion foundation models like Stable Diffusion. However, text conditioning is suboptimal from a compression perspective, hindering the potential of downstream diffusion codecs, particularly at ultra-low bitrates. To address it, we introduce CoD, the first Compression-oriented Diffusion foundation model, trained from scratch to enable end-to-end optimization of both compression and generation. CoD is not a fixed codec but a general foundation model designed for various diffusion-based codecs. It offers several advantages: High compression efficiency, replacing Stable Diffusion with CoD in downstream codecs like DiffC achieves SOTA results, especially at ultra-low bitrates (e.g., 0.0039 bpp); Low-cost and reproducible training, 300$\times$ faster training than Stable Diffusion ($\sim$ 20 vs. $\sim$ 6,250 A100 GPU days) on entirely open image-only datasets; Providing new insights, e.g., We find pixel-space diffusion can achieve VTM-level PSNR with high perceptual quality and can outperform GAN-based codecs using fewer parameters. We hope CoD lays the foundation for future diffusion codec research. Codes will be released.
</details>

---

### Alternative Reprogramming for Service Models
著者: Yunbei Zhang, Chengyi Cai, Feng Liu, Jihun Hamm

<details>
<summary> 日本語要旨 </summary>

閉じた箱のサービスモデル（つまり、API）をターゲットタスクに適応させる際は、通常ゼロ次最適化（ZOO）を用いて再プログラムします。しかし、この標準的な戦略は多くの高コストAPI呼び出しに依存しており、また遅く不安定な最適化が知られています。さらに、現代のAPI（例えばGPT-4o）では新たな課題に直面することを観察します。これらのモデルはZOOが依存する入力の微小変動に対して敏感性が低く、パフォーマンス向上を妨げる可能性があります。この限界に対処するため、私たちはサービスモデル用の代替効率的再プログラムアプローチ（AReS）を提案します。直接かつ連続した閉じた箱最適化ではなく、AReSはサービスAPIとの単一パスインタラクションから始めて、受容性の高いローカルプリトレーニングエンコーダーを準備します。このプライミング段階では、ローカルエンコーダー上に軽量層のみを訓練し、その後のガラス箱（白箱）再プログラム段階が直接ローカルモデルで行われるようにします。したがって、すべての後続の適応と推論はこのローカルプロキシに依存し、さらなるAPIコストを排除します。実験では、AReSの効果的性がZOOベースの方法が苦戦する場面で示されています：GPT-4o上で、AReSはゼロショットベースラインに対して+27.8％の向上を達成し、これはZOOベースの方法がほとんどまたは全く改善しないタスクです。広範囲にわたり、10種類の多様なデータセットでAReSは最先端手法を上回ります（VLMsでは+2.5％、標準VMsでは+15.6％）と同時にAPI呼び出しを99.99％以上削減します。AReSは現代の閉じた箱モデルを適応させるための堅牢で実用的なソリューションを提供します。
</details>

<details>
<summary> 英語要旨 </summary>

Adapting closed-box service models (i.e., APIs) for target tasks typically relies on reprogramming via Zeroth-Order Optimization (ZOO). However, this standard strategy is known for extensive, costly API calls and often suffers from slow, unstable optimization. Furthermore, we observe that this paradigm faces new challenges with modern APIs (e.g., GPT-4o). These models can be less sensitive to the input perturbations ZOO relies on, thereby hindering performance gains. To address these limitations, we propose an Alternative efficient Reprogramming approach for Service models (AReS). Instead of direct, continuous closed-box optimization, AReS initiates a single-pass interaction with the service API to prime an amenable local pre-trained encoder. This priming stage trains only a lightweight layer on top of the local encoder, making it highly receptive to the subsequent glass-box (white-box) reprogramming stage performed directly on the local model. Consequently, all subsequent adaptation and inference rely solely on this local proxy, eliminating all further API costs. Experiments demonstrate AReS's effectiveness where prior ZOO-based methods struggle: on GPT-4o, AReS achieves a +27.8\% gain over the zero-shot baseline, a task where ZOO-based methods provide little to no improvement. Broadly, across ten diverse datasets, AReS outperforms state-of-the-art methods (+2.5\% for VLMs, +15.6\% for standard VMs) while reducing API calls by over 99.99\%. AReS thus provides a robust and practical solution for adapting modern closed-box models.
</details>

---

### MICON-Bench: Benchmarking and Enhancing Multi-Image Context Image Generation in Unified Multimodal Models
著者: Mingrui Wu, Hang Liu, Jiayi Ji, Xiaoshuai Sun, Rongrong Ji

<details>
<summary> 日本語要旨 </summary>

最近の統合マルチモーダルモデル（UMMs）の進歩により、画像理解と生成能力が顕著に向上しました。しかし、Gemini-2.5-Flash-Imageのようなモデルは、関連する複数の画像を対象とした推論能力を示しているものの、既存のベンチマークでは多画像コンテキスト生成の課題にほとんど取り組まれておらず、主にテキストから画像への変換や単一画像編集タスクに焦点を当てています。本研究では、MICON-Benchという6つのタスクをカバーする包括的なベンチマークを紹介します。これは、画像間の構成、文脈的推論、およびアイデンティティ保持を評価します。さらに、セマンティックとビジュアルの一貫性を自動で確認するためのMLLM駆動型Evaluation-by-Checkpointフレームワークを提案しました。ここでは、マルチモーダル大規模言語モデル（MLLM）が検証者として機能します。また、トレーニング不要でプラグアンドプレイ可能なダイナミック・アテンション・リバランス（DAR）メカニズムを提示しました。これは推論時に注意を動的に調整して一貫性を向上させ、幻覚を減少させます。様々な最先端のオープンソースモデルで行った広範な実験は、MICON-Benchが多画像推論の課題を明らかにする厳密さと、DARが生成品質と画像間の一貫性を改善する効果を示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advancements in Unified Multimodal Models (UMMs) have enabled remarkable image understanding and generation capabilities. However, while models like Gemini-2.5-Flash-Image show emerging abilities to reason over multiple related images, existing benchmarks rarely address the challenges of multi-image context generation, focusing mainly on text-to-image or single-image editing tasks. In this work, we introduce MICON-Bench, a comprehensive benchmark covering six tasks that evaluate cross-image composition, contextual reasoning, and identity preservation. We further propose an MLLM-driven Evaluation-by-Checkpoint framework for automatic verification of semantic and visual consistency, where multimodal large language model (MLLM) serves as a verifier. Additionally, we present Dynamic Attention Rebalancing (DAR), a training-free, plug-and-play mechanism that dynamically adjusts attention during inference to enhance coherence and reduce hallucinations. Extensive experiments on various state-of-the-art open-source models demonstrate both the rigor of MICON-Bench in exposing multi-image reasoning challenges and the efficacy of DAR in improving generation quality and cross-image coherence.
</details>

---

### TRivia: Self-supervised Fine-tuning of Vision-Language Models for Table Recognition
著者: JUNYUAN ZHANG, Bin Wang, Qintong Zhang, Fan Wu, Zichen Wen, Jialin Lu, Junjie Shan, Ziqi Zhao, Shuya Yang, Ziling Wang, Ziyang Miao, Huaping Zhong, Yuhang Zang, Xiaoyi Dong, Ka-Ho Chow, Conghui He

<details>
<summary> 日本語要旨 </summary>

表の認識（TR）は、画像からHTMLやMarkdownなどの半構造化された形式に変換することを目的としています。文書解析の重要なコンポーネントであるTRは長らく監督学習に依存してきましたが、最近ではラベル付きデータを用いたビジョン言語モデル（VLM）の微調整が主流となっています。VLMはTRを次のレベルへ引き上げましたが、さらにパフォーマンスを向上させるためにはコストがかかる大規模なラベル付きデータが必要です。その結果、プロプライエタリモデルは継続的にパフォーマンスの限界を押し広げていますが、オープンソースモデルは資源が限られており、実際に多くの場合プライバシー規制のため唯一の選択肢となっているものの、大きく後れを取っています。このギャップを埋めるために、私たちはTRiviaという自己監督学習法を導入します。これは事前学習済みVLMがラベルなしの実際の表画像から直接TRを学ぶことを可能にします。Group Relative Policy Optimizationに基づいて構築されたTRiviaは、学習を最も効果的に促進するラベルなしサンプルを自動的に特定し、質問応答に基づく報酬メカニズムを通じて人間の注釈を不要とします。注意ガイド付きモジュールは各表画像に対して多様な質問を生成し、認識結果を解釈し正しく答える能力がTRモデルの最適化へフィードバックを提供します。この閉じたループプロセスにより、TRモデルはラベルなしで表を認識・構造化・理解することを自律的に学ぶことが可能です。このパイプラインを活用して、私たちはオープンソースでコンパクトかつ最先端のTRモデルであるTRivia-3Bを提案します。これはGemini 2.5 ProやMinerU2.5などの既存システムを三つの人気バイナリックスで上回っています。
</details>

<details>
<summary> 英語要旨 </summary>

Table recognition (TR) aims to transform table images into semi-structured representations such as HTML or Markdown. As a core component of document parsing, TR has long relied on supervised learning, with recent efforts dominated by fine-tuning vision-language models (VLMs) using labeled data. While VLMs have brought TR to the next level, pushing performance further demands large-scale labeled data that is costly to obtain. Consequently, although proprietary models have continuously pushed the performance boundary, open-source models, often trained with limited resources and, in practice, the only viable option for many due to privacy regulations, still lag far behind. To bridge this gap, we introduce TRivia, a self-supervised fine-tuning method that enables pretrained VLMs to learn TR directly from unlabeled table images in the wild. Built upon Group Relative Policy Optimization, TRivia automatically identifies unlabeled samples that most effectively facilitate learning and eliminates the need for human annotations through a question-answering-based reward mechanism. An attention-guided module generates diverse questions for each table image, and the ability to interpret the recognition results and answer them correctly provides feedback to optimize the TR model. This closed-loop process allows the TR model to autonomously learn to recognize, structure, and reason over tables without labeled data. Leveraging this pipeline, we present TRivia-3B, an open-sourced, compact, and state-of-the-art TR model that surpasses existing systems (e.g., Gemini 2.5 Pro, MinerU2.5) on three popular benchmarks.
</details>

---

### See What I Mean: Aligning Vision and Language Representations for Video Fine-grained Object Understanding
著者: Bo-Yuan Sun, Bo-Wen Yin, Yuan-Ming Li, Xihan Wei, Qibin Hou

<details>
<summary> 日本語要旨 </summary>

私たちは、SWIM（See What I Mean）という新しいトレーニング戦略を提案します。これは、テキストプロンプトだけから細部までのオブジェクト理解を可能にするために視覚と言語表現を整合させるものです。既存のアプローチがマスクやポイントなどの明示的なビジュアルプロンプトを必要とするのに対し、SWIMはトレーニング中だけマスク監督を利用してクロスモーダル注意を導きます。これにより、モデルが推論時に自動的にユーザー指定のオブジェクトに注目できるようになります。事前学習済みのマルチモーダル大規模言語モデル（MLLMs）のクロス注意分析では、系統的な不一致が明らかになりました：属性語は視覚モダリティで鋭く局所化された活性化を生じさせますが、オブジェクト名詞は意味参照バイアスと分散した高レベル表現により拡散し散在するパターンを示します。この不整合を解消するために、私たちはNL-Referという豊かなデータセットを構築しました。ここでは各オブジェクトマスクが正確な自然言語参照表現とペアになっています。SWIMはオブジェクト名詞から複数層のクロス注意マップを抽出し、地上真のマスクとの空間的一貫性を強制します。実験結果により、SWIMがテキスト・ビジュアル整合を大幅に改善し、細部までのオブジェクト理解ベンチマークにおいてビジュアルプロンプトベースの方法を上回る性能を達成することが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

We present SWIM (See What I Mean), a novel training strategy that aligns vision and language representations to enable fine-grained object understanding solely from textual prompts. Unlike existing approaches that require explicit visual prompts, such as masks or points, SWIM leverages mask supervision only during training to guide cross-modal attention, allowing the model to automatically attend to the user-specified object at inference. Our cross-attention analysis of pretrained multimodal large language models (MLLMs) reveals a systematic discrepancy: Attribute words produce sharp, localized activations in the visual modality, whereas object nouns yield diffuse and scattered patterns due to semantic reference bias and distributed high-level representations. To address this misalignment, we construct NL-Refer, an enriched dataset, in which each object mask is paired with a precise natural language referring expression. SWIM extracts multi-layer cross-attention maps from object nouns and enforces spatial consistency with ground-truth masks. Experimental results demonstrate that SWIM substantially improves text–visual alignment and achieves superior performance over visual-prompt-based methods on fine-grained object understanding benchmarks.
</details>

---

### GeoAgent: Learning to Geolocate Everywhere with Reinforced Geographic Characteristics
著者: Modi Jin, Yiming Zhang, Bo-Yuan Sun, Dingwen Zhang, Ming-Ming Cheng, Qibin Hou

<details>
<summary> 日本語要旨 </summary>

本論文では、人間に近い推論能力を持ち、細かな住所結論を導き出すことができるGeoAgentモデルを提案します。過去のRL（強化学習）ベースの手法は性能や解釈可能性において飛躍的な進歩を遂げましたが、AI生成のチェーン・オブ・シンク（CoT）データとトレーニング戦略に依存しているため、地理学的特性との矛盾から懸念が残っています。これらの問題を解決するために、まずGeoSeekという新しい位置情報データセットを紹介します。このデータセットは地理学専門家およびプロフェッショナルプレイヤーによって注釈付けされたCoTデータで構成されています。さらに、地理的タスクの固有の特性を徹底的に探求し、一貫性エージェントによって評価される地理類似報酬と一貫性報酬を提案します。これにより、モデルは正解へ収束するよう促されますが、その推論プロセスの整合性と一貫性も確保されます。実験結果では、GeoAgentが既存手法や多様な粒度で一般的なVLLMsを上回り、人間に近い推論を生成することが示されました。事前学習済みモデルおよびデータは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

This paper presents GeoAgent, a model capable of reasoning closely with humans and deriving fine-grained address conclusions. Previous RL-based methods have achieved breakthroughs in performance and interpretability but still remain concerns because of their reliance on AI-generated chain-of-thought (CoT) data and training strategies, which conflict with geographic characteristics. To address these issues, we first introduce GeoSeek, a new geolocation dataset comprising CoT data annotated by geographic experts and professional players. We further thoroughly explore the inherent characteristics of geographic tasks and propose a geo-similarity reward and a consistency reward assessed by a consistency agent to assist training. This encourages the model to converge towards correct answers from a geographic perspective while ensuring the integrity and consistency of its reasoning process. Experimental results show that GeoAgent outperforms existing methods and a series of general VLLMs across multiple grains, while generating reasoning that closely aligns with humans. Pretrained model and data will be openly available.
</details>

---

### Revisiting The Necessity of Lengthy Chain-of-Thought in Vision-centric Reasoning Generalization
著者: Yifan Du, Kun Zhou, Yingqian Min, Yue Ling, Xin Zhao, Youbin Wu, Ji-Rong Wen

<details>
<summary> 日本語要旨 </summary>

私たちは、ビジョン言語モデル（VLMs）における一般化可能な視覚的推論能力の獲得にどのように異なるチェーン・オブ・シンキング（CoT）設計が影響するかを研究しています。特に「画像で考える」などの長いまたは視覚的なCoTデータは、中間推論を監督するために広く使用されてきましたが、具体的なCoT設計がどのように役立つか、そしてどれが本当に一般化可能な推論をサポートしているかは明確ではありません。中間ステップの誤りリスクを増加させ、下流の強化学習（RL）を損なう可能性がある複雑なフォーマットを含むCoTデータの構築や合成はコストがかかります。これを体系的に評価するため、全ての中間ステップが自動生成可能であり、推論ルールが完全に視覚的である制御された迷路解決ベンチマークに焦点を当てます。グリッドサイズで難易度を調整することも可能です。標準のSFT-then-RLパイプラインを使用し、Qwen2.5-VL-7Bモデルで3つの代表的なCoTフォーマット（言語CoT、グランドリングCoT（空間座標軌跡付き）、視覚CoT（画像操作付き））を比較しました。実験の結果、視覚的で長いCoTは収束速度を加速するものの、最終的なパフォーマンスの上限を引き上げるわけではなく、必要最小限のグランドリングステップだけを含む簡潔なCoTが長いトレースよりも優れており、驚くべきことに、最小限のグランドリング結果を保持するCoTが異なる迷路サイズにわたって最も一般化できることが示されました。これらの洞察は他のビジョン中心のタスクでも検証しました。これらの発見は「短い方が長い」効果を強調し、視覚的推論用のより一般化可能なSFTデータセットの構築に実践的なガイダンスを提供します。私たちのコードとデータは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

We study how different Chain-of-Thought (CoT) designs affect the acquisition of the generalizable visual reasoning ability in vision-language models (VLMs). While CoT data, especially long or visual CoT such as ''think with image'', has been widely used to supervise intermediate reasoning, it remains unclear why specific CoT designs help and which ones truly support generalizable reasoning. \ignore{However, it is costly to construct or synthesize and may contain a complicated format that increases the risk of incorrect intermediate steps, hurting downstream reinforcement learning (RL).} To systematically evaluate this, we focus on a controlled maze-solving benchmark where reasoning rules are fully visual, difficulty can be tuned by grid size, and all the intermediate steps can be automatically generated. Using Qwen2.5-VL-7B under a standard SFT-then-RL pipeline, we compare three representative CoT formats: Language CoT, Grounding CoT (with spatial coordinate trajectories), and Visual CoT (with image manipulations). Our experiments reveal that visual and longer CoT mainly accelerate convergence but do not lift the final performance ceiling; concise CoT containing only essential grounding steps outperforms longer traces; and, strikingly, CoT retaining only the minimal grounding results generalizes best across different maze sizes. We further validate these insights on other vision-centric tasks. These findings highlight a ``short is long'' effect and provide practical guidance for constructing more generalizable SFT datasets for visual reasoning. Our code and data will be publicly released.
</details>

---

### Image-to-Point Cloud Feature Back-projection for Multimodal Training of 3D Semantic Segmentation
著者: Jiawei Han, Matteo Poggi, HUAN LI, Changshuo Wang, Kaiqi Liu, Wei Li

<details>
<summary> 日本語要旨 </summary>

画像カメラとLiDARから取得されるマルチモーダルデータの効果的な統合と利用は、認識システムにおいて極めて重要です。本論文では、画像特徴センター（非投影アラインメント画素から）を推定された深度マップを介して点群特徴セットへ逆投影する新しい方法である**I**mage-to-**P**oint Cloud **F**eature Back-**P**rojection (**IPFP**) を提案します。これにより、画像特徴と点群特徴が同じ三次元空間内に存在し、ネットワークの前方伝播中に自然な画像情報の点群への強化を可能にします。このプロセスは必要に応じて選択的に有効にすることができ、例えばトレーニング時に有効にし、マルチモーダルデータがない場合（例えば、テスト時にLiDARセンサーのみが利用可能な場合）は無効化できます。実験結果は、**IPFP** が3次元セマンティックセグメンテーションモデルに一貫して改善をもたらし、かつ推論時にLiDARのみのデータ処理能力を維持できることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

The effective integration and utilization of multimodal data acquired from image cameras and LiDAR is of paramount importance for perception systems. This paper proposes **I**mage-to-**P**oint Cloud **F**eature Back-**P**rojection (**IPFP**), a novel method for training multimodal fusion networks that back-projects aggregated image-feature centers (from non-projection-aligned image pixels) into the point-cloud feature set via the estimated depth map. Consequently, image features and point cloud features reside within the same three-dimensional space, enabling the natural enrichment of image information into the point cloud during the network forward pass. This process can be selectively enabled when desired -- for instance, at training time -- and turned off in the absence of multimodal data -- for example, at testing time if only LiDAR sensors are available. Experimental results demonstrate that **IPFP** can consistently improve state-of-the-art 3D semantic segmentation models, while retaining the ability to process LiDAR-only data at inference time.
</details>

---

### Rethinking MLLM Itself As A Segmenter with A Single Segmentation Token
著者: Anqi Zhang, Xiaokang Ji, Guangyu Gao, Jianbo Jiao, Chi Harold Liu, Yunchao Wei

<details>
<summary> 日本語要旨 </summary>

最近のマルチモーダル大規模言語モデル（MLLMs）を活用したセグメンテーション手法は、信頼性のあるオブジェクトレベルのセグメンテーションと空間知覚能力を示しています。しかし、ほとんどの既存方法は、生成されたセグメンテーション関連埋め込みやビジュアル特徴からマスクを解釈する専門的なマスクデコーダーに依存しているか、追加のトークンを多数組み込んでいます。本論文では、1つのセグメンテーション埋め込み（SELF1E）を用いてMLLM自体からセグメンテーションを解放することが可能かどうか、その方法について調査します。これにより外部デコーダーの必要性を排除しつつ競争力ある結果を達成できます。このために、我々はMLLMから得られるピクセルシャッフルされた画像特徴の解像度低下という基本的な制限に対処します。まず、画像特徴を元の圧縮されていない解像度で保持し、MLLMで処理された圧縮特徴から抽出した残差特徴でそれらを補充することにより、特徴の精度を向上させます。次に、MLLM処理を行った場合としない場合の画像特徴に対してピクセルアンシャッフル操作を統合し、圧縮された特徴の詳細を解放し、未圧縮解像度での残差特徴を模倣することにより、補充された特徴の解像度をさらに向上させます。また、画像から画像へと画像からセグメンテーションへの二重知覚経路を持つ注意マスクを再設計し、ピクセルとセグメンテーショントークン間で豊富な特徴相互作用を可能にします。複数のセグメンテーションタスクにわたる包括的な実験は、SELF1Eが専門的なマスクデコーダーを使用した方法と競争力のある性能を達成していることを検証し、MLLMにおけるデコーダーフリーセグメンテーションの実現可能性を示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Recent segmentation methods leveraging Multi-modal Large Language Models (MLLMs) have shown reliable object-level segmentation and enhanced spatial perception. However, almost all previous methods predominantly rely on specialist mask decoders to interpret masks from generated segmentation-related embeddings and visual features, or incorporate multiple additional tokens to assist. This paper aims to investigate whether and how we can unlock segmentation from MLLM itSELF with 1 segmentation Embedding~(SELF1E) while achieving competitive results, which eliminates the need for external decoders. To this end, our approach targets the fundamental limitation of resolution reduction in pixel-shuffled image features from MLLMs. First, we retain image features at their original uncompressed resolution, and refill them with residual features extracted from MLLM-processed compressed features, thereby improving feature precision. Subsequently, we integrate pixel-unshuffle operations on image features with and without MLLM processing, respectively, to unleash the details of compressed features and simulate the residual features under uncompressed resolution, which further enhances the resolution of refilled features. Moreover, we redesign the attention mask with dual perception pathways, i.e., image-to-image and image-to-segmentation, enabling rich feature interaction between pixels and the segmentation token. Comprehensive experiments across multiple segmentation tasks validate that SELF1E achieves performance competitive with specialist mask decoder-based methods, demonstrating the feasibility of decoder-free segmentation in MLLMs.
</details>

---

### Do You Have Freestyle? Expressive Humanoid Locomotion Via Audio Control
著者: Zhe Li, Cheng Chi, Yangyang Wei, Boan Zhu, Tao Huang, Zhenguo Sun, Yibo Peng, Pengwei Wang, Zhongyuan Wang, Fangzhou Liu, Chang Xu, Shanghang Zhang

<details>
<summary> 日本語要旨 </summary>

人間は本能的に音に反応して動くが、現在のヒューマノイドロボットは表現力豊かな即興演奏能力を欠き、予め定義された動作や限られた命令に制約されている。音から生成した動作をロボットに適用する際は明示的な動作再構築が必要となり、これによってエラーの連鎖、高いレイテンシ、不連続な音響-アクチュエーションマッピングが生じる。私たちは「動作 = 内容 + スタイル」という核となる原則に基づき、音を暗黙のスタイル信号として扱い、明示的な動作再構築を不要とする初めての統一されたオーディオから移動へのフレームワーク「RoboPerform」を提案する。このフレームワークは音楽駆動のダンスや発話駆動の共同発声ジェスチャーを直接生成できる。ResMoE教師方針を統合し、多様な動作パターンへの適応を図り、オーディオスタイル注入用に拡散ベースの学生方針を導入する。この再ターゲティング不要設計により低レイテンシと高精度が保証される。実験的検証では、RoboPerformは物理的妥当性およびオーディオの整合性において有望な結果を達成し、音に反応して即興演奏が可能なフリースタイルパフォーマーとしてロボットを変革することに成功した。
</details>

<details>
<summary> 英語要旨 </summary>

Humans intuitively move to sound, but current humanoid robots lack expressive improvisational capabilities, confined to predefined motions or sparse commands. Generating motion from audio and then retargeting it to robots relies on explicit motion reconstruction, leading to cascaded errors, high latency, and disjointed acoustic-actuation mapping. We propose RoboPerform, the first unified audio-to-locomotion framework that can directly generate music-driven dance and speech-driven co-speech gestures from audio. Guided by the core principle of "motion = content + style", the framework treats audio as implicit style signals and eliminates the need for explicit motion reconstruction. RoboPerform integrates a ResMoE teacher policy for adapting to diverse motion patterns and a diffusion-based student policy for audio style injection. This retargeting-free design ensures low latency and high fidelity. Experimental validation shows that RoboPerform achieves promising results in physical plausibility and audio alignment, successfully transforming robots into responsive freestyle performers capable of reacting to audio.
</details>

---

### Meta-CoT: Enhancing Granularity and Generalization in Image Editing
著者: Shiyi Zhang, YIJI CHENG, Tiankai Hang, Zijin Yin, Runze He, Yu Xu, Wenxun Dai, yunlong lin, Chunyu Wang, qinglin lu, Yansong Tang

<details>
<summary> 日本語要旨 </summary>

統一されたマルチモーダル理解/生成モデルは、そのChain-of-Thought（CoT）プロセスに細部までの理解を取り入れることで画像編集性能が向上しています。しかし、重要な問いが十分に探求されていません：どのようなCoT形式やトレーニング戦略が理解の細部化と一般化を同時に強化できるか。これに対処するため、私たちはMeta-CoTを提案します。これは、任意の単一画像編集操作について二重レベルの分解を行うパラダイムであり、以下の2つの主要な特性があります：(1) 分解可能性。私たちは、どんな編集意図もタスク、ターゲット、必要とされる理解能力から成るトリプレットで表現できることを観察しました。このインスピレーションに基づき、Meta-CoTは編集タスクとターゲットの両方を分解し、タスク固有のCoTを生成しつつ、すべてのターゲットで編集操作を横断します。この分解により、モデルは編集操作の理解細部化が強化され、トレーニング中にトリプレットの各要素を学ぶことが導かれ、編集能力が大幅に向上します。(2) 一般化可能性。第二の分解レベルでは、さらに編集タスクを5つの基本的なメタタスクに細分化します。これら5つのメタタスクとトリプレットの他の2要素でトレーニングすることが、多様な未見編集タスクに対して強力な一般化を達成するのに十分であることがわかりました。モデルのCoT推論による編集行動をさらに整合させるため、私たちはCoT–Editing Consistency Rewardを導入し、編集中にCoT情報をより正確かつ効果的に利用することを促進します。実験では、私たちの方法が21の編集タスクで全体的に15.8％の改善を達成し、少数のメタタスクだけでトレーニングした場合でも未見編集タスクへの効果的な一般化が可能であることを示しています。私たちのコード、ベンチマーク、およびモデルは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Unified multi-modal understanding/generative models have shown improved image editing performance by incorporating fine-grained understanding into their Chain-of-Thought (CoT) process. However, a critical question remains underexplored: what forms of CoT and training strategy can jointly enhance both the understanding granularity and generalization? To address this, we propose Meta-CoT, a paradigm that performs a two-level decomposition of any single-image editing operation with two key properties: (1) Decomposability. We observe that any editing intention can be represented as a triplet — (task, target, required understanding ability). Inspired by this, Meta-CoT decomposes both the editing task and the target, generating task-specific CoT and traversing editing operations on all targets. This decomposition enhances the model's understanding granularity of editing operations and guides it to learn each element of the triplet during training, substantially improving the editing capability.(2) Generalizability. In the second decomposition level, we further break down editing tasks into five fundamental meta-tasks. We find that training on these five meta-tasks, together with the other two elements of the triplet, is sufficient to achieve strong generalization across diverse, unseen editing tasks. To further align the model's editing behavior with its CoT reasoning, we introduce the CoT–Editing Consistency Reward, which encourages more accurate and effective utilization of CoT information during editing. Experiments demonstrate that our method achieves an overall 15.8\% improvement across 21 editing tasks, and generalizes effectively to unseen editing tasks when trained on only a small set of meta-tasks. Our code, benchmark, and model will be released publicly.
</details>

---

### MapReduce LoRA: Advancing The Pareto Front in Multi-Preference Optimization for Generative Models
著者: Chieh-Yun Chen, Zhonghao Wang, Qi Chen, Zhifan Ye, Min Shi, Yue Zhao, Yinan Zhao, Hui Qu, Wei-An Lin, Yiru Shen, Ajinkya Kale, Irfan Essa, Humphrey Shi

<details>
<summary> 日本語要旨 </summary>

人間のフィードバックから学習する強化学習（RLHF）と報酬モデルを用いることで、生成モデルの人間の美的および知覚的好みへの整合性が進歩しました。しかし、複数の報酬を同時に最適化すると、一つの次元を改善しながら他の次元を低下させる「整合税」が発生します。これに対処するために、2つの補完的な方法を導入します：MapReduce LoRAとReward-aware Token Embedding（RaTE）。MapReduce LoRAは好み特化のLoRAエキスパートを並列で訓練し、それらを反復的に統合して共有ベースモデルを洗練します。一方、RaTEは推論時に柔軟な好み制御のために構成される報酬特化のトークン埋め込みを学習します。テキストから画像生成（Stable Diffusion 3.5 MediumおよびFLUX.1-dev）に関する実験では、GenEvalで36.1%、PickScoreで4.6%、OCRで55.7%の改善が見られました。また、テキストからビデオ生成（HunyuanVideo）では視覚品質と動作品質がそれぞれ48.1%および90.0%向上しました。私たちのフレームワークは、複数の好みに対する整合性を横断的に設定する新しい最先端のレシピとなっています。
</details>

<details>
<summary> 英語要旨 </summary>

Reinforcement learning from human feedback (RLHF) with reward models has advanced alignment of generative models to human aesthetic and perceptual preferences. However, jointly optimizing multiple rewards often incurs an alignment tax—improving one dimension while degrading others. To address this, we introduce two complementary methods: MapReduce LoRA and Reward-aware Token Embedding (RaTE). MapReduce LoRA trains preference-specific LoRA experts in parallel and iteratively merges them to refine a shared base model; RaTE learns reward-specific token embeddings that compose at inference for flexible preference control. Experiments on Text-to-Image generation (Stable Diffusion 3.5 Medium and FLUX.1-dev) show improvements of 36.1%, 4.6%, and 55.7%, and 32.7%, 4.3%, and 67.1% on GenEval, PickScore, and OCR, respectively. On Text-to-Video generation (HunyuanVideo), visual and motion quality improve by 48.1% and 90.0%, respectively. Our framework sets a new state-of-the-art multi-preference alignment recipe across modalities.
</details>

---

### MatPedia: A Universal Generative Foundation for High-Fidelity Material Synthesis
著者: Di Luo, Shuhui Yang, Mingxin Yang, Jiawei Lu, Yixuan Tang, Xintong Han, Zhuo Chen, Beibei Wang, Chunchao Guo

<details>
<summary> 日本語要旨 </summary>

物理ベースのレンダリング（PBR）材質は、写実的なグラフィックスにおいて基本的であるが、その作成は依然として労力を要し、専門知識が必要です。生成モデルは材質の合成を進化させましたが、既存の方法では自然な画像の外観とPBR特性を統一的に表現するものが欠けており、タスクごとの断片化されたパイプラインや大規模なRGB画像データの活用不足につながっています。私たちは、新しい統合型RGB-PBR表現を基盤とした**MatPedia**というファウンデーションモデルを提案します。この表現は材質を2つの相互依存する潜在変数にコンパクトにエンコードします：一方はRGB外観用、もう一方は4つのPBRマップ（補完的な物理特性をエンコード）用です。これらを5チャネルシーケンスとして定式化し、ビデオ拡散アーキテクチャを利用することで、その相関関係を自然に捉えつつ、RGB生成モデルからの視覚的事前知識を転送します。この統合表現により、単一アーキテクチャ内で複数の材質タスク（テキストから材質生成、画像から材質生成、および固有分解）を処理する統一フレームワークが可能になります。MatHybrid-410KというPBRデータセットと大規模RGB画像を組み合わせた混合コーパスでトレーニングされたMatPediaは、1024×1024のネイティブ合成を実現し、既存手法を品質と多様性の両面で大幅に上回ります。
</details>

<details>
<summary> 英語要旨 </summary>

Physically-based rendering (PBR) materials are fundamental to photorealistic graphics, yet their creation remains labor-intensive and requires specialized expertise. While generative models have advanced material synthesis, existing methods lack a unified representation bridging natural image appearance and PBR properties, leading to fragmented task-specific pipelines and inability to leverage large-scale RGB image data. We present \textbf{MatPedia}, a foundation model built upon a novel joint RGB-PBR representation that compactly encodes materials into two interdependent latents: one for RGB appearance and one for the four PBR maps encoding complementary physical properties. By formulating them as a 5-channel sequence and employing video diffusion architectures, MatPedia naturally captures their correlations while transferring visual priors from RGB generation models. This joint representation enables a unified framework handling multiple material tasks—text-to-material generation, image-to-material generation, and intrinsic decomposition—within a single architecture. Trained on MatHybrid-410K, a mixed corpus combining PBR datasets with large-scale RGB images, MatPedia achieves native 1024×1024 synthesis that substantially surpasses existing approaches in both quality and diversity.
</details>

---

