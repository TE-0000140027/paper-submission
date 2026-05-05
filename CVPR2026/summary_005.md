# CVPR2026 論文要旨 (Part 5)

### Beyond Endpoints: Path-Centric Reasoning for Vectorized Off-Road Network Extraction
著者: wenfei guan, Jilin Mei, Tong Shen, Xumin Wu, Shuo Wang, Chen Min, Yu Hu

<details>
<summary> 日本語要旨 </summary>

ディープラーニングは都市環境におけるベクトル化された道路抽出を進展させましたが、オフロード環境は未だ十分に探索されていないと同時に挑戦的です。大きなドメインギャップが原因で、先進モデルは野生の地形では失敗しやすく、その理由は二つあります：大規模なベクトル化されたデータセットの不足と、現行手法の構造的弱点です。SAM-Roadのようなノード中心のパラダイムを採用するモデルは、スパースエンドポイントで推論を行い、オフロードシーンにおける遮蔽や曖昧なジャンクションに対して脆弱であり、トポロジカルエラーを引き起こします。本研究はこれらの制限を二つの補完的方法で解決します。まず、私たちはWildRoadというグローバルなオフロード道路ネットワークデータセットを効率的に構築し、道路ネットワークラベリング用に特化した専用のインタラクティブアノテーションツールを使用して公開します。次に、マスク認識ジオデシックロードネットワーク抽出器（MaGRoad）というパス中心のフレームワークを導入し、候補経路沿いで多スケールの視覚的証拠を集約して接続性を堅牢に推論します。広範な実験では、MaGRoadが私たちの挑戦的なWildRoadベンチマークで最先端のパフォーマンスを達成し、都市データセットにも良好に一般化することが示されました。また、ストリームライン化されたパイプラインは約2.5倍速い推論を実現し、実用的な適用性を向上させます。データセットとパス中心のパラダイムが組み合わされることで、野生における道路マッピングのためのより強固な基盤が提供されます。
</details>

<details>
<summary> 英語要旨 </summary>

Deep learning has advanced vectorized road extraction in urban settings, yet off-road environments remain underexplored and challenging. A significant domain gap causes advanced models to fail in wild terrains due to two key issues: lack of large-scale vectorized datasets and structural weakness in prevailing methods. Models such as SAM-Road employ a node-centric paradigm that reasons at sparse endpoints, making them fragile to occlusions and ambiguous junctions in off-road scenes, leading to topological errors. This work addresses these limitations in two complementary ways. First, we release WildRoad, a gloabal off-road road network dataset constructed efficiently with a dedicated interactive annotation tool tailored for road-network labeling. Second, we introduce MaGRoad (Mask-aware Geodesic Road network extractor), a path-centric framework that aggregates multi-scale visual evidence along candidate paths to infer connectivity robustly. Extensive experiments show that MaGRoad achieves state-of-the-art performance on our challenging WildRoad benchmark while generalizing well to urban datasets. A streamlined pipeline also yields roughly 2.5x faster inference, improving practical applicability. Together, the dataset and path-centric paradigm provide a stronger foundation for mapping roads in the wild.
</details>

---

### Bridging Facial Understanding and Animation Via Language Models
著者: Luchuan Song, Pinxin Liu, Haiyang Liu, Zhenchao Jin, Yunlong Tang, Zichong Xu, Susan Liang, Jing Bi, Jason Corso, Chenliang Xu

<details>
<summary> 日本語要旨 </summary>

テキストガイドによる人体アニメーションは急速に進歩していますが、顔のアニメーションはテキスト対応した顔のコーパスが不足しているため遅れをとっています。このギャップを埋めるために、我々は基盤となる生成モデルを活用し、バランスの取れた大規模な顔の動作コーパスを合成します。感情や頭部運動をカバーするプロンプトスイートを設計し、複数のジェネレーターで約80時間の顔のビデオを生成し、フレームごとに3D顔パラメータを適合させることで、トレーニング用の大規模な（プロンプトおよびパラメータ）ペアを得ました。このデータセットを基に、言語モデルが顔の動作に対して双方向の能力を持つかどうかを2つの補完的なタスクで検証します：（1）Motion2Language：与えられた3D顔パラメータのシーケンスに対して、モデルは内容、スタイル、ダイナミクスを捉える自然言語記述を生成します；（2）Language2Motion：与えられたプロンプトに基づいて、モデルは下流のアニメーション用に量子化された動作トークンを介して対応する3D顔パラメータのシーケンスを合成します。広範な実験では、この設定で言語モデルが強力な一般化能力を持って顔の動作を解釈し、生成することが示されました。我々の知る限り、これは初めて顔パラメーターモデリングを言語問題として捉えた研究であり、テキスト条件付きの顔アニメーションと動作理解の統一された道筋を確立しました。
</details>

<details>
<summary> 英語要旨 </summary>

Text-guided human body animation has advanced rapidly, yet facial animation lags due to the scarcity of well-annotated, text-paired facial corpora. To close this gap, we leverage foundation generative models to synthesize a large, balanced corpus of facial behavior. We design prompts suite covering emotions and head motions, generate about 80 hours of facial videos with multiple generators, and fit per-frame 3D facial parameters, yielding large-scale (prompt and parameter) pairs for training. Building on this dataset, we probe language models for bidirectional competence over facial motion via two complementary tasks: (1) Motion2Language: given a sequence of 3D facial parameters, the model produces natural-language descriptions capturing content, style, and dynamics; and (2) Language2Motion: given a prompt, the model synthesizes the corresponding sequence of 3D facial parameters via quantized motion tokens for downstream animation. Extensive experiments show that in this setting language models can both interpret and synthesize facial motion with strong generalization. To best of our knowledge, this is the first work to cast facial-parameter modeling as a language problem, establishing a unified path for text-conditioned facial animation and motion understanding.
</details>

---

### 4D Primitive-Mâché: Glueing Primitives for Persistent 4D Scene Reconstruction
著者: Kirill Mazur, Marwan Taher, Andrew J. Davison

<details>
<summary> 日本語要旨 </summary>

私たちは、カジュアルな単眼RGBビデオを入力として受け取り、シーンの完全かつ持続的な再構築を出力する動的再構築システムを提案します。具体的には、現在見えている部分だけでなく、過去に観測されたすべての部分も再構築し、全てのタイムステップにわたって完全な再構築を再生可能にします。私たちの方法では、シーン内で動き続けると仮定される一連の剛体3Dプリミティブにシーンを分解します。推定された密な2D対応関係を用いて、これらプリミティブの剛体運動を最適化パイプラインを通じて共同で推測し、シーンの4次元再構築を行います。すなわち、時間を通じて動的に変化する3D幾何学情報を提供します。このために、オブジェクトが見えなくなったときの運動を予測するメカニズムも導入し、運動グループ化技術を用いて連続性を保持します。結果として得られるシステムは4次元空間時間認識を可能にし、時間を通じた可動式オブジェクトの再生可能な3D再構築、マルチオブジェクトスキャニング、およびオブジェクトの持続性といった能力を提供します。オブジェクトスキャニングやマルチオブジェクトデータセットにおいて、私たちのシステムは既存手法を定量的・定性的に大きく上回ります。
</details>

<details>
<summary> 英語要旨 </summary>

We present a dynamic reconstruction system that receives a casual monocular RGB video as input, and outputs a complete and persistent reconstruction of the scene. In other words, we reconstruct not only the the currently visible parts of the scene, but also all previously viewed parts, which enables replaying the complete reconstruction across all timesteps. Our method decomposes the scene into a set of rigid 3D primitives, which are assumed to be moving throughout the scene. Using estimated dense 2D correspondences, we jointly infer the rigid motion of these primitives through an optimisation pipeline, yielding a 4D reconstruction of the scene, i.e. providing 3D geometry dynamically moving through time. To achieve this, we also introduce a mechanism to extrapolate motion for objects that become invisible, employing motion-grouping techniques to maintain continuity. The resulting system enables 4D spatio-temporal awareness, offering capabilities such as replayable 3D reconstructions of articulated objects through time, multi-object scanning, and object permanence. On object scanning and multi-object datasets, our system significantly outperforms existing methods both quantitatively and qualitatively.
</details>

---

### Taming The Long Tail: Rebalancing Adversarial Training Via Adaptive Perturbation
著者: Lilin Zhang, Yimo Guo, Li Yue, Jiancheng Shi, Xianggen Liu

<details>
<summary> 日本語要旨 </summary>

深層ニューラルネットワークは、小さな摂動がモデルの性能を大幅に低下させることができる敵対的例に非常に脆弱です。防御戦略としては、主に敵対的トレーニングが採用されていますが、多くの研究ではバランスの取れたデータセットを前提とし、実際の長尾データによってもたらされる課題を見落としています。敵対的例の摂動が訓練分布を本質的に変化させることから、その影響を理論的に調査する動機付けを得ています。まず、長尾データに対する敵対的トレーニングを再考し、2つの主要な制限点を特定します：（i）クラス不均衡による歪んだ訓練目標、および（ii）敵対的分布の不安定な進化。さらに、摂動が同時に敵対的脆弱性とクラス不均衡を解決できることを示します。これらの洞察に基づいて、我々は再バランスされた長尾データ用敵対的強度（RAIL）を提案します。これは、敵対的トレーニング中に摂動を適応的に調整するプラグアンドプレイフレームワークです。広範な実験が示すところによると、RAILは長尾データセット上で一貫して敵対的耐性を向上させ、クラスバランスも改善します。
</details>

<details>
<summary> 英語要旨 </summary>

Deep neural networks are highly vulnerable to adversarial examples, i.e.,small perturbations that can significantly degrade model performance. While adversarial training has become the primary defense strategy, most studies focus on balanced datasets, overlooking the challenges posed by real-world long-tail data. Motivated by the fact that perturbations in adversarial examples inherently alter the training distribution, we theoretically investigate their impact. We first revisit adversarial training for long-tail data and identify two key limitations: (i) a skewed training objective caused by class imbalance, and (ii) unstable evolution of adversarial distributions. Furthermore, we show that perturbations can simultaneously address both adversarial vulnerability and class imbalance. Based on these insights, we propose Rebalanced Adversarial Intensity for Long-Tailed Data (RAIL), a plug-and-play framework that adaptively adjusts perturbations during adversarial training. Extensive experiments demonstrate that RAIL consistently enhances adversarial robustness and class-balance on long-tailed datasets.
</details>

---

### WeDetect: Fast Open-Vocabulary Object Detection As Retrieval
著者: Shenghao Fu, Yukun Su, Fengyun Rao, Jing LYU, Xiaohua Xie, Wei-Shi Zheng

<details>
<summary> 日本語要旨 </summary>

オープンボキャブラリー物体検出は、テキストプロンプトを用いて任意のクラスを検出することを目指しています。クロスモーダル融合層（非融合）を持たない手法は、認識を検索問題として扱うことでより速い推論が可能になります。つまり、領域をテキストクエリと一致させる共通の埋め込み空間内で行います。本研究では、この検索哲学を徹底的に探求し、モデルファミリー「WeDetect」を通じてその効率性と汎用性の独自な利点を示します：（1）最先端のパフォーマンス。WeDetectはリアルタイム検出器で、デュアルタワー構造を持っています。よく整備されたデータと完全なトレーニングにより、非融合のWeDetectが他の融合モデルを上回り、強力なオープンボキャブラリー基盤を確立します。 （2）歴史的データの迅速なバックトラック。WeDetect-UniはWeDetectに基づく汎用プロポジションジェネレータです。全体の検出器を凍結し、カテゴリーを超えた一般的なオブジェクトプロポジションを取得するために、単にオブジェクトネスプロンプトのみを微調整します。重要なことに、プロポジション埋め込みはクラス固有であり、歴史的データ内のオブジェクト検索という新しい応用を可能にします。 （3）LMMsとの統合による参照表現理解（REC）。さらに、WeDetect-RefというLMMベースのオブジェクト分類器を提案し、複雑な参照表現を処理します。これは、WeDetect-Uniから抽出されたプロポジションリストからターゲットオブジェクトを検索します。次のトークン予測を捨て、単一の前向きパスでオブジェクトを分類します。WeDetectファミリーは、検出、プロポジション生成、オブジェクト検索、RECを統一的な検索フレームワークの下にまとめ、高い推論効率で15のベンチマークにおいて最先端のパフォーマンスを達成します。すべてのモデルをオープンソース化します。
</details>

<details>
<summary> 英語要旨 </summary>

Open-vocabulary object detection aims to detect arbitrary classes via text prompts. Methods without cross-modal fusion layers (non-fusion) offer faster inference by treating recognition as a retrieval problem, i.e., matching regions to text queries in a shared embedding space. In this work, we fully explore this retrieval philosophy and demonstrate its unique advantages in efficiency and versatility through a model family named WeDetect: (1) State-of-the-art performance. WeDetect is a real-time detector with a dual-tower architecture. We show that, with well-curated data and full training, the non-fusion WeDetect surpasses other fusion models and establishes a strong open-vocabulary foundation. (2) Fast backtrack of historical data. WeDetect-Uni is a universal proposal generator based on WeDetect. We freeze the entire detector and only finetune an objectness prompt to retrieve generic object proposals across categories. Importantly, the proposal embeddings are class-specific and enable a new application, object retrieval, supporting retrieval objects in historical data. (3) Integration with LMMs for referring expression comprehension (REC). We further propose WeDetect-Ref, an LMM-based object classifier to handle complex referring expressions, which retrieves target objects from the proposal list extracted by WeDetect-Uni. It discards next-token prediction and classifies objects in a single forward pass. Together, the WeDetect family unifies detection, proposal generation, object retrieval, and REC under a coherent retrieval framework, achieving state-of-the-art performance across 15 benchmarks with high inference efficiency. We will open-source all models.
</details>

---

### MeshSplatting: Differentiable Rendering with Opaque Meshes
著者: Jan Held, Sanghyun Son, Renaud Vandeghen, Daniel Rebain, Matheus Gadelha, Yi Zhou, Anthony Cioppa, Ming Lin, Marc Van Droogenbroeck, Andrea Tagliasacchi

<details>
<summary> 日本語要旨 </summary>

プリミティブベースのスプラッティング手法である3次元ガウシアン・スプラッティング（3DGS）は、リアルタイムレンダリングを伴う新視点合成に革命をもたらしました。しかし、そのポイントベースの表現は、AR/VRやゲームエンジンを動かすメッシュベースのパイプラインと互換性がありません。私たちは、異分化レンダリングを通じて幾何学と外観を同時に最適化するメッシュベースの再構成アプローチであるMeshSplattingを提案します。制限されたデラウナイ三角分割によって接続性を強制し、表面一貫性を洗練することで、MeshSplattingはエンドツーエンドで滑らかで視覚的に高品質なメッシュを作成し、リアルタイム3Dエンジンで効率よくレンダリングします。Mip-NeRF360では、現在の最先端技術であるMiLoと比較してPSNRが+0.69 dB向上し、メッシュベースの新視点合成においてトレーニング速度を2倍にし、使用するメモリも半分に抑えることで、ニューラルレンダリングとインタラクティブ3Dグラフィックスの間に橋渡しを行い、シームレスなリアルタイムシーンインタラクションを実現します。
</details>

<details>
<summary> 英語要旨 </summary>

Primitive-based splatting methods like 3D Gaussian Splatting (3DGS) have revolutionized novel view synthesis with real-time rendering. However, their point-based representations remain incompatible with mesh-based pipelines that power AR/VR and game engines. We present MeshSplatting, a mesh-based reconstruction approach that jointly optimizes geometry and appearance through differentiable rendering. By enforcing connectivity via restricted Delaunay triangulation and refining surface consistency, MeshSplatting creates end-to-end smooth, visually high-quality meshes that render efficiently in real-time 3D engines. On Mip-NeRF360, it boosts PSNR by +0.69 dB over the current state-of-the-art MiLo for mesh-based novel view synthesis, while training 2x faster and using 2x less memory, bridging neural rendering and interactive 3D graphics for seamless real-time scene interaction.
</details>

---

### Visual Diffusion Models Are Geometric Solvers
著者: Nir Goren, Shai Yehezkel, Omer Dahary, Andrey Voynov, Or Patashnik, Daniel Cohen-Or

<details>
<summary> 日本語要旨 </summary>

この論文では、視覚的拡散モデルが効果的な幾何学的ソルバーとして機能することを示します。これらのモデルはピクセル空間で作業し、直接幾何学的問題について推論することができます。まず、長年にわたって研究されてきたジョーダン曲線内に四角形を形成する4点が存在するかどうかを問う「内接正方形問題」でこのアプローチを示します。次に、他の2つのよく知られた難解な幾何学的問題、すなわちスタインツリー問題と最大面積多角形問題へのアプローチを拡張します。私たちの方法では、各問題インスタンスを画像として扱い、ガウシアンノイズから有効な近似解を表す画像に変換する標準的な視覚的拡散モデルを訓練します。このモデルは、正しい配置にノイズのある幾何学的構造を変換することで学習し、幾何学的推論を画像生成へと再定義します。従来の方法では、パラメトリックな幾何学的表現に拡散を適用する際に特殊なアーキテクチャやドメイン固有の適応が必要でしたが、私たちは問題の視覚的表現上で動作する標準的な視覚的拡散モデルを使用します。この単純さは、生成モデリングと幾何学的問題解決の間に驚くべき架け橋があることを示しています。本研究で扱った特定の問題を超えて、私たちの結果はより広範なパラダイムを指し示します：画像空間で作業することによって、難解な問題を近似する一般的かつ実用的なフレームワークが提供され、挑戦的な幾何学的タスクの広範なクラスへの道が開かれます。
</details>

<details>
<summary> 英語要旨 </summary>

In this paper we show that visual diffusion models can serve as effective geometric solvers: they can directly reason about geometric problems by working in pixel space. We first demonstrate this on the Inscribed Square Problem, a long-standing problem in geometry that asks whether every Jordan curve contains four points forming a square. We then extend the approach to two other well-known hard geometric problems: the Steiner Tree Problem and the Maximum Area Polygon Problem. Our method treats each problem instance as an image and trains a standard visual diffusion model that transforms Gaussian noise into an image representing a valid approximate solution that closely matches the exact one. The model learns to transform noisy geometric structures into correct configurations, effectively recasting geometric reasoning as image generation. Unlike prior work that necessitates specialized architectures and domain-specific adaptations when applying diffusion to parametric geometric representations, we employ a standard visual diffusion model that operates on the visual representation of the problem. This simplicity highlights a surprising bridge between generative modeling and geometric problem solving. Beyond the specific problems studied here, our results point toward a broader paradigm: operating in image space provides a general and practical framework for approximating notoriously hard problems, and opens the door to tackling a far wider class of challenging geometric tasks.
</details>

---

### BrickNet: Graph-Backed Generative Brick Assembly
著者: Peter Kulits, Cordelia Schmid

<details>
<summary> 日本語要旨 </summary>

私たちはLEGO®ブロックの組み立てシーケンスを生成する言語モデルを訓練します。従来の研究は、離散的なビクセルのような塔に限定されていましたが、私たちは多様な接続意味を持つ数千種類の部品タイプを含む広範なパーツセットを考慮します。これを可能にするために、まず100,000以上の人間設計LDrawブロックオブジェクトとシーンから成る大規模データセットを収集します。私たちの環境の複雑さは、物理的制約を満たす構造を自己回帰的に組み立てることが困難であることを意味します。ブロックポーズを直接予測すると、短いステップ数後にすぐに無効な組み立てシーケンスになります。部品は3D空間に配置されますが、全体を定義するのは部品同士の空間関係です。このことを念頭に置き、構造を接続性でパラメータ化し、生成されたシーケンスの物理的な根拠を改善するグラフベースのプログラム表現を設計します。将来の応用を可能にするために、私たちは研究目的でデータセットとモデルを公開します。https://kulits.github.io/BrickNet
</details>

<details>
<summary> 英語要旨 </summary>

We train a language model to generate LEGO®-brick build sequences. While prior work has been restricted to discrete, voxel-like towers, we consider a much broader set of pieces, encompassing thousands of part types with diverse connection semantics. To enable this, we first collect a large-scale dataset of over 100,000 human-designed LDraw brick objects and scenes. The complexity of our setting makes it challenging to autoregressively assemble structures that satisfy physical constraints. When predicting block pose directly, build sequences quickly become invalid after a small number of steps. Although pieces are placed in 3D space, it is the spatial relationships of the parts which define the whole. With this in mind, we design a graph-based program representation that parametrizes structure through connectivity, improving the physical grounding of generated sequences. To enable future applications, we make our dataset and models available for research purposes. https://kulits.github.io/BrickNet
</details>

---

### Audio-sync Video Instance Editing with Granularity-Aware Mask Refiner
著者: Haojie Zheng, Shuchen Weng, Jingqi Liu, Siqi Yang, Boxin Shi, Xinlong Wang

<details>
<summary> 日本語要旨 </summary>

最近の動画生成技術の進歩は、リアルな音声と映像の同期が魅力的なコンテンツ作成において重要であることを強調しています。しかし、既存の動画編集方法は多くの場合、音声と映像の同期を無視し、正確なインスタンスレベルの編集に必要な細かい空間的および時間的制御が不足しています。本論文では、音声同期動画インスタンス編集フレームワークであるAVI-Editを提案します。私たちは、粒度に配慮したマスクリファイナーを提案し、これはユーザーが提供する粗いマスクを反復的に正確なインスタンスレベルの領域に洗練します。さらに、高品質な音声ガイダンスをキュレートし、細かい時間制御を提供する自己フィードバック型のオーディオエージェントを設計しています。このタスクを容易にするために、インスタンス中心の対応関係と包括的な注釈を持つ大規模データセットも構築しました。広範囲にわたる実験は、AVI-Editがビジュアル品質、条件遵守、音声と映像の同期において最先端の方法を上回っていることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advancements in video generation highlight that realistic audio-visual synchronization is crucial for engaging content creation. However, existing video editing methods largely overlook audio-visual synchronization and lack the fine-grained spatial and temporal controllability required for precise instance-level edits. In this paper, we propose AVI-Edit, a framework for audio-sync video instance editing. We propose a granularity-aware mask refiner that iteratively refines coarse user-provided masks into precise instance-level regions. We further design a self-feedback audio agent to curate high-quality audio guidance, providing fine-grained temporal control. To facilitate this task, we additionally construct a large-scale dataset with instance-centric correspondence and comprehensive annotations. Extensive experiments demonstrate that AVI-Edit outperforms state-of-the-art methods in visual quality, condition following, and audio-visual synchronization.
</details>

---

### DuetSVG: Unified Multimodal SVG Generation with Internal Visual Guidance
著者: Peiying Zhang, Nanxuan Zhao, Matthew Fisher, Yiran Xu, Jing Liao, Difan Liu

<details>
<summary> 日本語要旨 </summary>

最近のビジョン・ランゲージモデル（VLM）に基づくアプローチは、SVG生成において印象的な成果を達成しています。しかし、これらの手法がテキストのみを生成し、解読中に視覚信号を欠いているため、複雑なセマンティクスに苦戦し、視覚的に魅力的で幾何学的に一貫性のあるSVGを生成することがしばしば困難です。私たちは、画像トークンと対応するSVGトークンをエンドツーエンドで同時に生成する統合的なマルチモーダルモデル「DuetSVG」を導入します。DuetSVGは画像およびSVGの両方のデータセットでトレーニングされます。推論時には、モデル固有の視覚予測をガイドとして活用することでSVG解読品質を向上させる新しいテストタイムスケーリング戦略を適用します。広範な実験により、私たちの方法が既存の手法を凌ぎ、多様なアプリケーション領域で視覚的に忠実でセマンティックに整合し、文法的にクリーンなSVGを生成することが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

Recent vision–language model (VLM)–based approaches have achieved impressive results on SVG generation. However, because they generate only text and lack visual signals during decoding, they often struggle with complex semantics and fail to produce visually appealing or geometrically coherent SVGs. We introduce DuetSVG, a unified multimodal model that jointly generates image tokens and corresponding SVG tokens in an end-to-end manner. DuetSVG is trained on both image and SVG datasets. At inference, we apply a novel test-time scaling strategy that leverages the model’s native visual predictions as guidance to improve SVG decoding quality. Extensive experiments show that our method outperforms existing methods, producing visually faithful, semantically aligned, and syntactically clean SVGs across a wide range of applications.
</details>

---

### Extending Embodied Question Answering from Perception to Decision
著者: Xicheng Gong, Qiwei Li, Peiran Xu, Yadong Mu

<details>
<summary> 日本語要旨 </summary>

エンボディド・クエスチョン・アンサー（EQA）は、知覚、推論、および具現化された環境内での相互作用を結びつけます。しかし、既存のデータセットやベンチマークは断片的なままであり、空間理解や手順推論といった限られた推論スキルに焦点を当てており、包括的評価のための統一された大規模フレームワークを提供していません。私たちは、具現化された推論の4つの補完的次元を体系的にカバーする大規模なエンボディドQAデータセットであるEQA-Decisionを提示します：静的シーン構築、空間理解、タスクダイナミクス推論、および即時決定。このデータセットには、多様な具現化されたシナリオを通じて階層的アノテーションが付けられた4,000万以上の質問・回答ペアが含まれています。さらに、EQA-Decisionベンチマークと整合した強力な基準モデルであるRoboDecisionを開発しました。これは、具現化された環境内の知覚、推論、および行動レベルの意思決定を統一的に評価するフレームワークを提供します。結果は、EQA-Decisionが空間と相互作用の推論におけるVLM（ビジュアル・ランゲージ・モデル）能力を効果的にベンチマークし向上させていることを示しており、具現化された知性研究の進展のための堅固な基盤を提供します。
</details>

<details>
<summary> 英語要旨 </summary>

Embodied Question Answering (EQA) connects perception, reasoning, and interaction within embodied environments. However, existing datasets and benchmarks remain fragmented, each focusing on a limited subset of reasoning skills such as spatial understanding or procedural reasoning, without offering a unified large-scale framework for comprehensive evaluation. We present EQA-Decision, a large-scale embodied QA dataset that systematically covers four complementary dimensions of embodied reasoning: static scene construction, spatial understanding, task dynamics reasoning, and instant decision. The dataset contains over four million question–answer pairs with hierarchical annotations across diverse embodied scenarios. In addition, we develop RoboDecision, a strong baseline model aligned with the EQA-Decision Benchmark, providing a unified framework that jointly evaluates perception, reasoning, and action-level decision-making in embodied environments. Results demonstrate that EQA-Decision effectively benchmarks and enhances VLM capabilities in spatial and interaction reasoning, providing a solid foundation for advancing embodied intelligence research.
</details>

---

### MM-OVSeg: Multimodal Optical–SAR Fusion for Open-Vocabulary Segmentation in Remote Sensing
著者: YIMIN WEI, Aoran Xiao, Hongruixuan Chen, Junshi Xia, Naoto Yokoya

<details>
<summary> 日本語要旨 </summary>

オープンボキャブラリー分割は、固定クラスを超えた一般化を可能にする開放的なテキストカテゴリからのピクセルレベル認識を可能にします。しかし、遠隔センシングにおけるその大きなポテンシャルにもかかわらず、この分野での進歩は主に晴天時の光学データに限定されており、曇りや霧が混入した条件下では苦戦しています。私たちは、不利な気象条件下での頑健なオープンボキャブラリー分割を可能にするマルチモーダル光学–SAR融合フレームワーク、MM-OVSegを提案します。MM-OVSegは、2つのモダリティの補完的な強みを活用しています—光学画像は豊富なスペクトルセマンティクスを提供し、合成開口レーダー（SAR）は雲を貫通する構造的手がかりを提供します。現在のビジョン–言語モデルの限られた密な予測能力とクロスモーダルドメインギャップに対処するため、2つの重要な設計を提案します：複数センサー表現の整合性を図るクロスモーダル統一プロセスと、テキストに整列したマルチモーダル分割のために複数のビジョンファウンデーションモデルから階層的特徴を統合するダブルエンコーダー融合モジュール。広範な実験は、MM-OVSegが多様な雲の条件にわたって優れた頑健性と一般化能力を達成していることを示しています。すべてのデータセットとコードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Open-vocabulary segmentation enables pixel-level recognition from an open set of textual categories, allowing generalization beyond fixed classes. Despite great potential in remote sensing, progress in this area remains largely limited to clear-sky optical data and struggles under cloudy or haze-contaminated conditions. We present MM-OVSeg, a multimodal Optical–SAR fusion framework for resilient open-vocabulary segmentation under adverse weather conditions. MM-OVSeg leverages the complementary strengths of the two modalities—optical imagery provides rich spectral semantics, while synthetic aperture radar (SAR) offers cloud-penetrating structural cues. To address the cross-modal domain gap and the limited dense prediction capability of current vision–language models, we propose two key designs: a cross-modal unification process for multi-sensor representation alignment, and a dual-encoder fusion module that integrates hierarchical features from multiple vision foundation models for text-aligned multimodal segmentation. Extensive experiments demonstrate that MM-OVSeg achieves superior robustness and generalization across diverse cloud conditions. All dataset and code will be publicly released.
</details>

---

### RealUnify: Do Unified Models Truly Benefit from Unification? A Comprehensive Benchmark
著者: Yang Shi, Yuhao Dong, Yue Ding, Yuran Wang, Xuanyu Zhu, Sheng Zhou, Wenting Liu, Haochen Tian, rundong wang, Huanqian Wang, Zuyan Liu, Bohan Zeng, Ruizhe Chen, Qixun Wang, Zhuoran Zhang, Xinlong Chen, Chengzhuo Tong, bozhou li, Qiang Liu, Haotian Wang, Wenjing Yang, Yuanxing Zhang, Pengfei Wan, YiFan Zhang, Ziwei Liu

<details>
<summary> 日本語要旨 </summary>

視覚理解と生成を統合した統一的なマルチモーダルモデルの開発は、汎用AIに向けた重要な進歩を示しています。しかし、既存のベンチマークでは未解決の基本的な問いが残っています：このアーキテクチャの統一は、構成能力間でシナジー効果をもたらすことを実際に可能にするのでしょうか？理解と生成を個別に評価する既存の評価パラダイムは、統一モデルがその理解能力を活用して生成を向上させることや、生成シミュレーションを通じてより深い理解を促進することができるかどうかを判断するには不十分です。この重要なギャップに対処するため、私たちはRealUnifyというベンチマークを導入します。これは、10のカテゴリと32のサブタスクを含む1,000の慎重に人間が注釈したインスタンスから成り立ち、双方向の能力シナジーを評価するために特別に設計されています。RealUnifyは2つの主要な軸で構成されています：1) 理解が生成を強化する、これは画像生成をガイドするために推理（例えば、常識や論理）を必要とします。2) 生成が理解を強化する、これは推論タスクを解決するために変形されたり乱れた視覚入力の精神的シミュレーションや再構築を必要とします。重要な貢献は、直接的なエンド・トゥ・エンド評価と診断ステップバイステップ評価を組み合わせた二重評価プロトコルです。このプロトコルにより、パフォーマンスのボトルネックが基本能力の欠陥から生じるか、それらを統合できないことから生じるかを正確に判定することが可能です。12の主要な統一モデルと6つの専門的な基準線を大規模評価した結果、現在の統一モデルは依然として効果的なシナジーを達成することに苦戦しており、アーキテクチャの統一だけでは不十分であることが示されました。これらの結果は、統一モデリングの潜在能力を完全に解放するために新しいトレーニング戦略や誘導バイアスが必要であることを強調しています。
</details>

<details>
<summary> 英語要旨 </summary>

The integration of visual understanding and generation into unified multimodal models represents a significant stride toward general-purpose AI. However, a fundamental question remains unanswered by existing benchmarks: does this architectural unification actually enable synergetic interaction between the constituent capabilities? Existing evaluation paradigms, which primarily assess understanding and generation in isolation, are insufficient for determining whether a unified model can leverage its understanding to enhance its generation, or use generative simulation to facilitate deeper comprehension. To address this critical gap, we introduce RealUnify, a benchmark specifically designed to evaluate bidirectional capability synergy. RealUnify comprises 1,000 meticulously human-annotated instances spanning 10 categories and 32 subtasks. It is structured around two core axes: 1) Understanding Enhances Generation, which requires reasoning (e.g., commonsense, logic) to guide image generation, and 2) Generation Enhances Understanding, which necessitates mental simulation or reconstruction (e.g., of transformed or disordered visual inputs) to solve reasoning tasks. A key contribution is our dual-evaluation protocol, which combines direct end-to-end assessment with a diagnostic stepwise evaluation that decomposes tasks into distinct understanding and generation phases. This protocol allows us to precisely discern whether performance bottlenecks stem from deficiencies in core abilities or from a failure to integrate them. Through large-scale evaluations of 12 leading unified models and 6 specialized baselines, we find that current unified models still struggle to achieve effective synergy, indicating that architectural unification alone is insufficient. These results highlight the need for new training strategies and inductive biases to fully unlock the potential of unified modeling.
</details>

---

### Plug-and-Play Incomplete Multi-View Clustering Via Janus-Faced Affinity Learning with Topology Harmonization
著者: Shengju Yu, Suyuan Liu, Wenhao SHAO, Siwei Wang, KE LIANG, Xihong Yang, Tiejun Li, Xinwang Liu

<details>
<summary> 日本語要旨 </summary>

従来の不完全多視点クラスタリング（IMVC）手法は、通常、ビュー固有のアーティファクトが観測されるときに、ビューコンセンサス表現を学習する際にその干渉を考慮しないため、結果として得られる類似度の信頼性が損なわれます。また、ビュー間でアンカーオーダーが不一致になることでグラフ構造が歪み、クラスタリングパフォーマンスが低下します。さらに、正確に調整された規則化ハイパーパラメータへの依存も通常はモデルの実用性を損ないます。これらの問題を軽減するため、我々はプラグアンドプレイIMVCフレームワークであるPJFTHを提案します。このフレームワークは、双面的な親和性学習とトポロジー調和を組み込んでいます。それはビュー固有の表現とコンセンサス間の相互作用を明示的にモデル化し、各ビューからビュープライベートグラフを導出し、その特性に応じてそれらをグローバルコンセンサス親和性に適応的に統合します。さらに、アンカー行列には順序変換と単一符号化制約が適用され、アンカートポロジーを再整列しつつ値を保持します。このプロセスは類似度統合前にアンカーオーダーを同期させ、元のアンカー特性を維持します。注目すべきことに、全てのコンポーネントがシームレスに連携され、共同で最適化されます。また、証明可能な全体的な線形複雑性はその拡張性と実用性をさらに高めています。実験結果は、PJFTHがいくつかの主要手法と競合するパフォーマンスを確認しています。
</details>

<details>
<summary> 英語要旨 </summary>

Prevailing incomplete multi-view clustering (IMVC) approaches typically fail to account for the interference of view-exclusive artifacts when learning view-consensus representations, which could compromise the fidelity of the resulting similarity measure. Moreover, inconsistencies in anchor order across views may distort the graph structure, impairing the clustering performance. The reliance on carefully-tuned regularization hyper-parameters also usually undermines the model's practical utility. To alleviate these issues, we propose a plug-and-play IMVC framework named PJFTH that incorporates Janus-faced affinity learning with topology harmonization. It explicitly models the exclusive-to-consensus interplay, derives a view-private graph from each view, and adaptively integrates them into a global consensus affinity according to the respective view's intrinsic characteristics. Furthermore, a permutation transformation with unary encoding constraints is applied to anchor matrix, realigning anchor topology while preserving the values. This process synchronizes anchor order prior to similarity integration and maintains original anchor properties. Notably, all components are coupled seamlessly and optimized in a joint manner. Also, the provable overall linear complexity further enlarges its scalability and practicality. Experimental results confirm that PJFTH receives competitive performance compared to several leading methods.
</details>

---

### UniDex: A Robot Foundation Suite for Universal Dexterous Hand Control from Egocentric Human Videos
著者: Gu Zhang, Qicheng Xu, Haozhe Zhang, Jianhan Ma, Long He, Yiming Bao, Zeyu Ping, Zhecheng Yuan, Chenhao Lu, Chengbo Yuan, Tianhai Liang, Xiaoyu Tian, Maanping Shao, Feihong Zhang, Mingyu Ding, Yang Gao, Hao Zhao, Hang Zhao, Huazhe Xu

<details>
<summary> 日本語要旨 </summary>

巧緻な操作は、実ロボットのテレオペレーションデータ収集コスト、手部分身の異質性、および制御の高次元性に起因する課題が残っています。本研究では、普遍的な巧緻な手操作を可能にするためのロボット基盤スイートであるUniDexを提案します。これは、大規模なロボット中心データセットと統一されたビジョン・言語・アクション（VLA）ポリシー、実用的な人間データキャプチャセットアップを組み合わせています。まず、UniDex-Datasetと呼ばれるロボット中心の10M対の画像・点群・アクションフレームおよび8つの巧緻な手（6～24自由度）にわたる50,000以上の軌道を含む大規模データセットを構築します。これは、エゴセントリックな人間動画データセットから導出されています。人間データをロボット実行可能な軌道に変換するために、指先の軌道を整列させつつ、現実的な手・物体接触を保持するためのヒューマンインザループリターゲティング手順を採用し、人間の手がマスクされた明示的な3D点群で操作します。次に、機能的に類似したアクチュエータを共有座標にマッピングすることで、異なる手間の転送を可能にする統一されたアクション空間であるFunction–Actuator–Aligned Space（FAAS）を導入します。FAASをアクションパラメータ化として利用し、UniDex-VLAと呼ばれる3D VLAポリシーをUniDex-Datasetで事前学習し、タスクデモンストレーションにより微調整します。さらに、同期したRGB-Dストリームおよび人間の手姿勢を記録し、ロボット実行可能な軌道に変換することで、高コストなロボットデモンストレーションに依存しない人間・ロボット共同学習を可能にするシンプルなポータブルキャプチャセットアップUniDex-Capを構築します。2つの異なる手での挑戦的な工具使用タスクにおいて、UniDex-VLAは平均81%のタスク進捗を達成し、既存のVLAベースラインよりも大幅に優れた性能を示します。また、空間的、物体的、ゼロショットクロスハンド一般化といった強力な特性を発揮しています。UniDex-Dataset、UniDex-VLA、およびUniDex-Capは共に、普遍的な巧緻操作のためのスケーラブルな基盤スイートを提供します。
</details>

<details>
<summary> 英語要旨 </summary>

Dexterous manipulation remains challenging due to the cost of collecting real-robot teleoperation data, the heterogeneity of hand embodiments, and the high dimensionality of control. We present UniDex, a robot foundation suite that couples a large-scale robot-centric dataset with a unified vision–language–action (VLA) policy and a practical human-data capture setup for universal dexterous hand control. First, we construct UniDex-Dataset, a robot-centric dataset of 10M paired image–pointcloud–action frames and over 50K trajectories across eight dexterous hands (6–24 DoFs), derived from egocentric human video datasets. To transform human data into robot-executable trajectories, we employ a human-in-the-loop retargeting procedure to align fingertip trajectories while preserving plausible hand–object contacts, and we operate on explicit 3D pointclouds with human hands masked to narrow kinematic and visual gaps. Second, we introduce the Function–Actuator–Aligned Space (FAAS), a unified action space that maps functionally similar actuators to shared coordinates, enabling cross-hand transfer. Leveraging FAAS as the action parameterization, we train UniDex-VLA, a 3D VLA policy pretrained on UniDex-Dataset and finetuned with task demonstrations. In addition, we build UniDex-Cap, a simple portable capture setup that records synchronized RGB-D streams and human hand poses and converts them into robot-executable trajectories to enable human–robot data co-training that reduces reliance on costly robot demonstrations. On challenging tool-use tasks across two different hands, UniDex-VLA achieves 81\% average task progress and outperforms prior VLA baselines by a large margin, while exhibiting strong spatial, object, and zero-shot cross-hand generalization. Together, UniDex-Dataset, UniDex-VLA, and UniDex-Cap provide a scalable foundation suite for universal dexterous manipulation.
</details>

---

### AnimaMimic: Imitating 3D Animation from Video Priors
著者: Tianyi Xie, Yunuo Chen, Yaowei Guo, Yin Yang, Bolei Zhou, Demetri Terzopoulos, Ying Jiang, Chenfanfu Jiang

<details>
<summary> 日本語要旨 </summary>

リアルな3Dアニメーションの作成は、手動でのリギング、キーフレーミング、複雑な動きの微調整を必要とする時間がかかり専門知識に依存したプロセスです。一方で、ビデオ拡散モデルは最近、テキストや画像プロンプトから動的で視覚的に一貫性のある動きを生成することで、2Dにおける驚異的な動作想像力を示しています。しかし、その結果は明確な3D構造が欠如し、直接アニメーションやシミュレーションに使用することはできません。私たちは、ビデオ拡散モデルから学習した動作事前知識を用いて静的3Dメッシュをアニメーション化するフレームワーク「AnimaMimic」を提案します。入力メッシュから始め、AnimaMimicは単眼のアニメーションビデオを合成し、自動的にスケルトンとスキニング重みを構築し、異分化レンダリングとビデオベースの監視を通じてジョイントパラメータを洗練します。さらに現実感を高めるために、物理的に根拠付けされたソフト組織ダイナミクスを通じてメッシュ変形を洗練する異分化シミュレーションモジュールを統合します。私たちの方法は、ビデオ拡散の創造性と3Dリグアニメーションの構造制御をつなぎ、物理的に妥当で時間的に一貫した、アーティストが編集可能な動作シーケンスを生成し、これらは標準的なアニメーションパイプラインに無縁に統合されます。
</details>

<details>
<summary> 英語要旨 </summary>

Creating realistic 3D animation remains a time-consuming and expertise-dependent process, requiring manual rigging, keyframing, and fine-tuning of complex motions. Meanwhile, video diffusion models have recently demonstrated remarkable motion imagination in 2D, generating dynamic and visually coherent motion from text or image prompts. However, their results lack explicit 3D structure and cannot be directly used for animation or simulation. We present AnimaMimic, a framework that animates static 3D meshes using motion priors learned from video diffusion models. Starting from an input mesh, AnimaMimic synthesizes a monocular animation video, automatically constructs a skeleton with skinning weights, and refines joint parameters through differentiable rendering and video-based supervision. To further enhance realism, we integrate a differentiable simulation module that refines mesh deformation through physically grounded soft-tissue dynamics. Our method bridges the creativity of video diffusion and the structural control of 3D rigged animation, producing physically plausible, temporally coherent, and artist-editable motion sequences that integrate seamlessly into standard animation pipelines.
</details>

---

### Towards GUI Agents: Vision-Language Diffusion Models for GUI Grounding
著者: Shrinidhi Kumbhar, Haofu Liao, srikar appalaraju, Kunwar Yashraj Singh

<details>
<summary> 日本語要旨 </summary>

自己回帰（AR）のビジョン・ランゲージモデル（VLM）は、多様な理解、推論、およびグラフィカルユーザーインターフェース（GUI）の基礎付けに長らく優位を保ってきました。最近では、離散的拡散ビジョン・ランゲージモデル（DVLM）が多様な推論で強力な性能を示し、双方向の注意、平行したトークン生成、反復的な洗練を提供しています。しかし、GUIの基礎付けにおけるその可能性は未だ探求されていません。本研究では、離散的DVLMがARモデルと同様にGUIの基礎付けに有効な代替手段であるかを評価します。LLaDA-Vを単一ターンアクションおよびバウンディングボックス予測用に適応させ、多様な入力からのテキスト生成として課題をフレーム化します。バウンディングボックス幾何学の階層的構造をより良く捉えるために、線形マスキングと決定論的マスキングを組み合わせたハイブリッドマスキングスケジュールを提案し、これがGUI適応LLaDA-Vの線形マスキングで訓練されたものに対して、ステップ成功率（SSR）で最大6.1ポイント向上することを示します。ウェブ、デスクトップ、モバイルインターフェースを含む4つのデータセットにおける評価では、ハイブリッドマスキングを用いた適応拡散モデルが線形マスクされたバージョンを一貫して上回り、限られた事前学習にもかかわらず自己回帰の対抗馬と競争力を持っていることが示されました。系統的なアブレーション分析では、拡散ステップ数、生成長さ、およびブロック長の増加が正確性を向上させますが、ある一定の拡散ステップ数を超えると正確性は頭打ちになり、かつ遅延も増大することが明らかにされました。GUIドメインの多様化したトレーニングデータを拡張することで、約1.3秒の遅延削減と平均20ポイントの基礎付け正確性向上がベンチマーク全体にわたって観察されました。これらの結果は、離散的DVLMがGUIの基礎付けにおいて有望なモデリングフレームワークであることを示し、拡散ベースのGUIエージェントへの重要な一歩を表しています。
</details>

<details>
<summary> 英語要旨 </summary>

Autoregressive (AR) vision–language models (VLMs) have long dominated multimodal understanding, reasoning, and graphical user interface (GUI) grounding. Recently, discrete diffusion vision–language models (DVLMs) have shown strong performance in multimodal reasoning, offering bidirectional attention, parallel token generation, and iterative refinement. However, their potential for GUI grounding remains unexplored. In this work, we evaluate whether discrete DVLMs can serve as a viable alternative to AR models for GUI grounding. We adapt LLaDA-V for single-turn action and bounding-box prediction, framing the task as text generation from multimodal input. To better capture the hierarchical structure of bounding-box geometry, we propose a hybrid masking schedule that combines linear and deterministic masking, improving grounding accuracy by up to 6.1 points in Step Success Rate (SSR) over the GUI-adapted LLaDA-V trained with linear masking. Evaluations on four datasets spanning web, desktop, and mobile interfaces show that the adapted diffusion model with hybrid masking consistently outperforms the linear-masked variant and performs competitively with autoregressive counterparts despite limited pretraining. Systematic ablations reveal that increasing diffusion steps, generation length, and block length improves accuracy but also increases latency, with accuracy plateauing beyond a certain number of diffusion steps. Expanding the training data with diverse GUI domains further reduces latency by about 1.3 seconds and improves grounding accuracy by an average of 20 points across benchmarks. These results demonstrate that discrete DVLMs are a promising modeling framework for GUI grounding and represent an important step toward diffusion-based GUI agents.
</details>

---

### Elastic Weight Consolidation Done Right for Continual Learning
著者: Xuan Liu, Xiaobin Chang

<details>
<summary> 日本語要旨 </summary>

継続的学習（CL）における重み正則化手法は、モデルの重要な重みへの変更を評価し罰することで、致命的な忘却を軽減します。Elastic Weight Consolidation（EWC）はこの枠組み内で基礎的かつ広く使用されているアプローチの一つであり、勾配に基づいて重みの重要性を推定します。しかし、これまでに常に最適なパフォーマンスを示していません。本論文では、EWCにおける重要度推定を勾配ベースの観点から体系的に分析します。初めて、我々はEWCがFisher Information Matrix（FIM）に依存することが特定のシナリオで勾配消失および不正確な重要度推定を引き起こすことを発見しました。また、我々の分析は、Memory Aware Synapses（MAS）というEWCのバリエーションが過去のタスクに関係しないパラメータに不必要な制約を課すこと、これを冗長保護と呼びます。その結果、EWCおよびそのバリエーションは重みの重要度推定に基本的なズレがあり、パフォーマンスが劣ることが明らかになりました。これらの問題を解決するために、我々はLogits Reversal（LR）操作を提案します。これは重要度推定の誤りを修正する簡単で効果的な変更です。具体的には、FIMの計算中にロジット値を反転させることで、勾配消失および冗長保護の両方を防ぐことができます。様々なCLタスクやデータセットにわたる広範囲な実験では、提案された方法が既存のEWCおよびそのバリエーションを大幅に上回ることが示されました。したがって、我々はこれを「EWC Done Right（EWC-DR）」と呼んでいます。
</details>

<details>
<summary> 英語要旨 </summary>

Weight regularization methods in continual learning (CL) alleviate catastrophic forgetting by assessing and penalizing changes to important model weights. Elastic Weight Consolidation (EWC) is a foundational and widely used approach within this framework that estimates weight importance based on gradients. However, it has consistently shown suboptimal performance. In this paper, we conduct a systematic analysis of importance estimation in EWC from a gradient-based perspective. For the first time, we find that EWC’s reliance on the Fisher Information Matrix (FIM) results in gradient vanishing and inaccurate importance estimation in certain scenarios. Our analysis also reveals that Memory Aware Synapses (MAS), a variant of EWC, imposes unnecessary constraints on parameters irrelevant to prior tasks, termed the redundant protection. Consequently, both EWC and its variant exhibit fundamental misalignments in estimating the importance of weights, leading to inferior performance. To tackle these issues, we propose the Logits Reversal (LR) operation, a simple yet effective modification that rectifies the importance estimation of EWC. Specifically, reversing the logit values during the calculation of the FIM can effectively prevent both the gradient vanishing and the redundant protection. Extensive experiments across various CL tasks and datasets show that the proposed method significantly outperforms existing EWC and its variants. Therefore, we refer to it as EWC Done Right (EWC-DR).
</details>

---

### LoL: Longer Than Longer, Scaling Video Generation to Hour
著者: Jiaxing Cui, Jie Wu, Ming Li, Tao Yang, Xiaojie Li, Rui Wang, Andrew Bai, Yuanhao Ban, Cho-Jui Hsieh

<details>
<summary> 日本語要旨 </summary>

最近の長尺動画生成研究は、双方向モデルから自己回帰モデルへと移行していますが、これらの方法は一般的にエラー蓄積や長期的な一貫性の喪失を引き起こします。パフォーマンス低下を緩和するために注意集中フレームが導入されましたが、これらはしばしば「sink-collapse」と呼ばれる致命的な障害モードを引き起こします。生成されたコンテンツが繰り返し集中フレームに戻り、突然のシーンリセットや周期的な動作パターンが発生する現象です。私たちの分析では、sink-collapseは回転位置埋め込み（RoPE）の周期構造と、現在の生成モデルで一般的なマルチヘッド注意メカニズムとの間に存在する本質的な矛盾から生じることが明らかになりました。これを解決するため、私たちはトレーニング不要で軽量なアプローチを提案します。このアプローチは、マルチヘッドRoPEジッターを導入して異なる注意頭間の均質化を破り、長期的な崩壊を軽減することでこの挙動を効果的に抑制します。広範囲の実験では、私たちの方法がsink-collapseを成功裏に緩和しつつ生成品質を保持していることが示されました。現時点で、この作業はリアルタイム、ストリーミング、無限長動画生成の初めての実証例を達成し、ほとんど品質低下なく行われました。この堅牢性の一例として、私たちは12時間に及ぶ連続動画を生成しましたが、これはストリーミング動画生成で公開されている中でも最長の結果の一つだと考えられます。
</details>

<details>
<summary> 英語要旨 </summary>

Recent research in long-form video generation has shifted from bidirectional to autoregressive models, yet these methods commonly suffer from error accumulation and a loss of long-term coherence. While attention sink frames have been introduced to mitigate this performance decay, they often induce a critical failure mode we term sink-collapse: the generated content repeatedly reverts to the sink frame, resulting in abrupt scene resets and cyclic motion patterns. Our analysis reveals that sink-collapse originates from an inherent conflict between the periodic structure of Rotary Position Embedding (RoPE) and the multi-head attention mechanisms prevalent in current generative models. To address it, we propose a lightweight, training-free approach that effectively suppresses this behavior by introducing multi-head RoPE jitter that breaks inter-head attention homogenization and mitigates long-horizon collapse. Extensive experiments show that our method successfully alleviates sink-collapse while preserving generation quality. To the best of our knowledge, this work achieves the first demonstration of real-time, streaming, and infinite-length video generation with little quality decay. As an illustration of this robustness, we generate continuous videos up to 12 hours in length, which, to our knowledge, is among the longest publicly demonstrated results in streaming video generation.
</details>

---

### YOSE: You Only Select Essential Tokens for Efficient DiT-based Video Object Removal
著者: wu chenyang, Lina Lei, Fan Li, Chun-Le Guo, Dehong Kong, Xinran Qin, Zhixin Wang, Ming-Ming Cheng, Chongyi Li

<details>
<summary> 日本語要旨 </summary>

最近のDiffusion Transformer（DiT）ベースのビデオ生成技術は、ビデオオブジェクト除去において印象的な結果を示しています。しかし、これらの方法は依然として大きな推論遅延に悩まされています。例えば、MiniMax Removerは最先端の視覚品質を実現しているものの、全体的なスパティオタイム空間上で密集した計算が行われるために約10 FPSでしか動作しません。これは、処理が必要なマスクされた領域が小さい場合でも同様です。本論文では、YOSE（You Only Select Essential Tokens）という効率的な微調整フレームワークを提案します。YOSEには2つの主要なコンポーネントがあります：Batch Variable-length Indexing（BVI）とDiffusion Process Simulator（DiffSim）モジュールです。BVIは、マスク情報に基づいて必須トークンを適応的に選択する可微分な動的インデックス演算子であり、サンプル間で変数長のトークン処理を可能にします。DiffSimは、DiT自己注意内でマスクされていない領域の影響をシミュレートすることで、マスクされたトークンの意味的一貫性を維持するための拡散プロセス近似メカニズムを提供します。これらの設計により、YOSEはマスク認識加速を実現し、推論時間がマスクされた領域とほぼ線形的にスケールすることができます。これに対して、全トークン拡散方法では計算量はマスクサイズに関わらず一定のままです。広範な実験により、YOSEは70%のケースで最大2.5倍の高速化を達成しながらベースラインと同等の視覚品質を維持することが示されました。コードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advances in Diffusion Transformer (DiT)-based video generation technologies have shown impressive results for video object removal. However, these methods still suffer from substantial inference latency. For instance, although MiniMax Remover achieves state-of-the-art visual quality, it operates at only around 10 FPS, primarily due to dense computations over the entire spatiotemporal token space—even when only a small masked region actually requires processing. In this paper, we present YOSE — You Only Select Essential Tokens, an efficient fine-tuning framework. YOSE introduces two key components: Batch Variable-length Indexing (BVI) and Diffusion Process Simulator (DiffSim) Module. BVI is a differentiable dynamic indexing operator that adaptively selects essential tokens based on mask information, enabling variable-length token processing across samples. DiffSim provides a diffusion process approximation mechanism for unmasked tokens, which simulates the influence of unmasked regions within DiT self-attention to maintain semantic consistency for masked tokens. With these designs, YOSE achieves mask-aware acceleration, where the inference time scales approximately linearly with the masked regions — in contrast to full-token diffusion methods whose computation remains constant regardless of the mask size. Extensive experiments demonstrate that YOSE achieves up to 2.5x speedup in 70% of cases while maintaining visual quality comparable to the baseline. The code will be made publicly available.
</details>

---

### AVA-Bench: Atomic Visual Ability Benchmark for Vision Foundation Models
著者: Zheda Mai, Arpita Chowdhury, Zihe Wang, Sooyoung Jeon, Lemeng Wang, Jiacheng Hou, Jihyung Kil, Wei-Lun Chao

<details>
<summary> 日本語要旨 </summary>

視覚基盤モデル（VFMs）の台頭は、体系的な評価を求めています。一般的なアプローチでは、大規模言語モデル（LLMs）を汎用ヘッドとしてVFMsに組み合わせ、広範なビジュアルクエスチョンアンサリング（VQA）の基準で評価します。しかし、このプロトコルには2つの重要な盲点があります：(i) 指示調整データがVQAテスト分布と一致しない可能性があるため、間違った予測はそのようなデータ不一致に起因するかもしれず、VFMsの視覚的欠点ではありません；(ii) VQA基準はしばしば単一の質問で複数の視覚能力を必要とするため、エラーがすべての必要な能力の不足によるものか、あるいは1つの重要な能力だけの不足によるものかを判断することが難しいです。これらのギャップに対処するために、私たちは14の原子視覚能力（AVAs）を明示的に分解する最初の基準であるAVA-Benchを導入します。局在化、深度推定、空間理解などの基礎スキルを含むこれらの能力は、複雑な視覚的推論タスクを支えています。AVAsを分離し、各々内でトレーニングとテスト分布を一致させることにより、AVA-BenchはVFMsがどこで優れているか、または失敗しているかを正確に特定します。この基準を主要なVFMsに適用することで、「能力の指紋」が明らかになり、VFMの選択が教養ある推測から原理的なエンジニアリングへと変わります。特筆すべきことに、0.5B LLMは7B LLMと同様のVFMランキングを提供し、GPU時間を8倍削減することで、より効率的な評価が可能です。包括的かつ透明性のある基準を提供することにより、AVA-Benchは次世代VFMsのための基盤を築くことを期待しています。
</details>

<details>
<summary> 英語要旨 </summary>

The rise of vision foundation models (VFMs) calls for systematic evaluation. A common approach pairs VFMs with large language models (LLMs) as general-purpose heads, followed by evaluation on broad Visual Question Answering (VQA) benchmarks. However, this protocol has two key blind spots: (i) Instruction tuning data may not align with VQA test distributions, meaning a wrong prediction can stem from such data mismatch rather than VFMs' visual shortcomings; (ii) VQA benchmarks often require multiple visual abilities in a single question, making it difficult to determine whether errors arise from the lack of all required abilities or just one key ability. To address these gaps, we introduce AVA-Bench, the first benchmark that explicitly disentangles 14 Atomic Visual Abilities (AVAs), foundational skills such as localization, depth estimation, and spatial understanding, which collectively support complex visual reasoning tasks. By decoupling AVAs and matching training and test distributions within each, AVA-Bench pinpoints exactly where a VFM excels or falters. Applying AVA-Bench to leading VFMs thus reveals distinctive "ability fingerprints," turning VFM selection from educated guesswork into principled engineering. Notably, we find that a 0.5B LLM yields similar VFM rankings as a 7B LLM while cutting GPU hours by 8x, enabling more efficient evaluation. By offering a comprehensive and transparent benchmark, we hope AVA-Bench lays the foundation for the next generation of VFMs.
</details>

---

### Image Diffusion Preview with Consistency Solver
著者: Fu-Yun Wang, Hao Zhou, Liangzhe Yuan, Sanghyun Woo, Boqing Gong, Bohyung Han, Ming-Hsuan Yang, Han Zhang, Yukun Zhu, Ting Liu, Long Zhao

<details>
<summary> 日本語要旨 </summary>

画像拡散モデルの遅い推論プロセスは、インタラクティブなユーザー体験を大幅に低下させます。これに対処するために、我々は新しいパラダイムであるDiffusion Previewを導入します。これは、ユーザー評価のための予備出力を生成するために迅速な低ステップサンプリングを利用し、その後、満足できるまでフルステップの洗練を延期します。既存の加速方法（トレーニングフリーソルバーおよびポストトレーニングの蒸留）は、高品質な予備出力を提供したり、予備と最終出力の一貫性を保証することに苦労しています。本論文では、一般的な線形多段法から導かれた新しいソルバーであるConsistencySolverを提案します。これは、強化学習を用いて最適化された軽量でトレーニング可能な高次ソルバーであり、予備の品質と一貫性を向上させます。実験結果は、ConsistencySolverが低ステップシナリオにおいて生成品質を大幅に改善し、効率的な予備・洗練ワークフローに理想的であることを示しています。特に、Multistep DPM-Solverの47%少ないステップで同等のFIDスコアを達成し、蒸留ベースラインを上回っています。さらに、ユーザー調査では、我々のアプローチが生成品質を維持しつつ、全体的なユーザーインタラクション時間をほぼ50%削減することを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

The slow inference process of image diffusion models significantly degrades interactive user experiences. To address this, we introduce Diffusion Preview, a novel paradigm employing rapid, low-step sampling to generate preliminary outputs for user evaluation, deferring full-step refinement until the preview is deemed satisfactory. Existing acceleration methods, including training-free solvers and post-training distillation, struggle to deliver high-quality previews or ensure consistency between previews and final outputs. In this paper, we propose ConsistencySolver derived from general linear multistep methods, a lightweight, trainable high-order solver optimized via Reinforcement Learning, that enhances preview quality and consistency. Experimental results demonstrate that ConsistencySolver significantly improves generation quality in low-step scenarios, making it ideal for efficient preview-and-refine workflows. Notably, it achieves FID scores on-par with Multistep DPM-Solver using 47% fewer steps, while outperforming distillation baselines. Furthermore, user studies indicate our approach reduces overall user interaction time by nearly 50% while maintaining generation quality.
</details>

---

### PhysX-Anything: Simulation-Ready Physical 3D Assets from Single Image
著者: Ziang Cao, Fangzhou Hong, Zhaoxi Chen, Liang Pan, Ziwei Liu

<details>
<summary> 日本語要旨 </summary>

3Dモデリングは、シミュレーションやインタラクションで直接使用可能な物理的かつ可動性のある資産に向けて、静的な視覚表現から移行しています。しかし、多くの既存の3D生成方法は重要な物理的および可動性特性を見落としているため、エンボディAIにおけるその有用性が制限されています。このギャップを埋めるために、私たちは**シミュレーション準備済み**の物理3D生成フレームワークである\textbf{PhysX-Anything}を導入します。これは、単一の自然な画像から高品質なシミュレーション用3Dアセットを生成し、明示的な幾何学、可動性、物理属性を持たせます。具体的には、最初のVLMベースの物理3D生成モデルと、幾何学を効率的にトークン化する新しい3D表現を提案します。これにより、特別なトークンを導入せずに標準のVLMトークン予算内で明示的な幾何学学習が可能となり、生成品質が大幅に向上します。さらに、既存の物理3Dデータセットの多様性の限界を克服するために、**PhysX-Mobility**という新しいデータセットを構築しました。これは、以前の物理3Dデータセットのオブジェクトカテゴリーを2倍以上拡張し、豊富な物理アノテーションを持つ2000種類以上の一般的な実世界オブジェクトを含んでいます。PhysX-Mobilityと自然な画像における広範な実験では、PhysX-Anythingが強力な生成性能と堅牢な一般化能力を示していることが確認されました。さらに、MuJoCoスタイルの環境でのシミュレーションベースの実験では、私たちのシミュレーション準備済みアセットが接触豊富なロボティクスポリシー学習に直接使用可能であることを検証しました。私たちは、PhysX-Anythingが特にエンボディAIや物理ベースのシミュレーションなど、幅広い下流アプリケーションを大きく強化できると考えています。
</details>

<details>
<summary> 英語要旨 </summary>

3D modeling is shifting from static visual representations toward physical, articulated assets that can be directly used in simulation and interaction. However, most existing 3D generation methods overlook key physical and articulation properties, thereby limiting their utility in embodied AI. To bridge this gap, we introduce \textbf{PhysX-Anything}, the first \textbf{simulation-ready} physical 3D generative framework that, given a single in-the-wild image, produces high-quality sim-ready 3D assets with explicit geometry, articulation, and physical attributes. Specifically, we propose the first VLM-based physical 3D generative model, along with a new 3D representation that efficiently tokenizes geometry. It reduces the number of tokens by \textbf{193$\times$}, enabling explicit geometry learning within standard VLM token budgets without introducing any special tokens during fine-tuning and significantly improving generative quality. In addition, to overcome the limited diversity of existing physical 3D datasets, we construct a new dataset, \textbf{PhysX-Mobility}, which expands the object categories in prior physical 3D datasets by over \textbf{2$\times$} and includes more than 2K common real-world objects with rich physical annotations. Extensive experiments on PhysX-Mobility and in-the-wild images demonstrate that PhysX-Anything delivers strong generative performance and robust generalization. Furthermore, simulation-based experiments in a MuJoCo-style environment validate that our sim-ready assets can be directly used for contact-rich robotic policy learning. We believe PhysX-Anything can substantially empower a broad range of downstream applications, especially in embodied AI and physics-based simulation.
</details>

---

### The Power of Prior: Training-Free Open-Vocabulary Semantic Segmentation with LLaVA
著者: Bingfeng Zhang, Siyue Yu, Hui Li, Jiahua Lin, Wenwu Wang, Jimin Xiao

<details>
<summary> 日本語要旨 </summary>

多モーダル大規模言語モデル（MLLMs）であるLLaVAは、マルチモーダル理解と生成において顕著な能力を示しています。この成功が私たちを動機付け、これらのMLLMsに内在する先天的な知識がタスク固有の微調整を必要とせずに密度予測タスクに十分な空間認識を持っているかどうかを調査することに導きました。したがって、本論文ではLLaVAを用いたトレーニングフリーのオープンボキャブラリセマンティックセグメンテーションの利用可能性を探ります。私たちは、LLaVAのLLM部分において特定の層が与えられたオブジェクトクラスに対応する局所化された特徴を生成できることを発見しました。この固有能力に基づき、ターゲットクラスの画像内識別用の質問-回答パイプライン、初期信頼性のあるピクセルレベル活性化を抽出するテキストビジュアル応答モジュール、およびSAMによる予測生成のためのガイダンスとしてさらに役立つ信頼性のある洗練されたプロンプトを生成するビジュアル生成モジュールの3つのモジュールを設計しました。私たちのLLaVAベースのアプローチは、「Thing」カテゴリーのデータセット、例えばPASCAL VOC 2012およびCOCO-objectにおいて新たな最先端パフォーマンスを達成しました。さらに、私たちの方法は明示的な背景クラス名を必要とせず、オープンワールドシナリオでの取り扱いにおけるその卓越したポテンシャルを示しています。コードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Multimodal Large Language Models (MLLMs) like LLaVA have demonstrated remarkable capabilities in multi-modal understanding and generation. This success motivates us to investigate whether the inherent prior knowledge embedded within such MLLMs contains sufficient spatial awareness for dense prediction tasks, without requiring any task-specific fine-tuning. Thus, in this paper, we explore the utilization of LLaVA for training-free open-vocabulary semantic segmentation. We discover that certain layers within the LLM part of LLaVA can generate localized features corresponding to given object classes. Building on this intrinsic capability, we design three modules: A question-answer pipeline to identify target classes in the image, a text-visual response module to extract initial reliable pixel-level activations for the target class, and a visual generation module to produce reliable refined prompts, which further serve as guidance for SAM to generate the predictions. Our LLaVA-based approach achieves new state-of-the-art performance on ``Thing" category datasets, \eg, PASCAL VOC 2012 and COCO-object. Moreover, our method does not require explicit background class names, demonstrating its exceptional potential for handling open-world scenarios. The code will be released.
</details>

---

### TEXTRIX: Latent Attribute Grid for Native Texture Generation and Beyond
著者: Yifei Zeng, Bao Yajie, Jiachen Qian, Shuang Wu, Youtian Lin, Hao Zhu, Buyu Li, Feihu Zhang, Xun Cao, Yao Yao

<details>
<summary> 日本語要旨 </summary>

従来の3Dテクスチャ生成方法は、多視点融合に依存することが多く、異なるビュー間の不整合や複雑な表面のカバー不足によって制約されています。これにより生成コンテンツの忠実度と完全性が限定されます。この課題を克服するため、我々はTEXTRIXという新しい3D属性生成フレームワークを導入します。これにより高品質なテクスチャ合成や精密な3D部分セグメンテーションなどの下流アプリケーションが可能となります。我々のアプローチでは、潜在的な3D属性格子を構築し、スパース注意を備えたDiffusion Transformerを利用して、直接的にボリュメトリック空間で3Dモデルの塗装を行い、多視点融合の制約を根本的に回避します。このネイティブ表現に基づき、フレームワークは同じアーキテクチャを格子上でセマンティック属性を予測するように訓練することで自然に高精度3Dセグメンテーションへ拡張されます。広範な実験が両タスクにおける最先端の性能を示し、滑らかで高品質なテクスチャと精密な境界を持つ正確な3D部分セグメンテーションを生成しています。
</details>

<details>
<summary> 英語要旨 </summary>

Prevailing 3D texture generation methods, which often rely on multi-view fusion, are frequently hindered by inter-view inconsistencies and incomplete coverage of complex surfaces, limiting the fidelity and completeness of the generated content. To overcome these challenges, we introduce TEXTRIX, a native 3D attribute generation framework for high-fidelity texture synthesis and downstream applications such as precise 3D part segmentation. Our approach constructs a latent 3D attribute grid and leverages a Diffusion Transformer equipped with sparse attention, enabling direct coloring of 3D models in volumetric space and fundamentally avoiding the limitations of multi-view fusion. Built upon this native representation, the framework naturally extends to high-precision 3D segmentation by training the same architecture to predict semantic attributes on the grid. Extensive experiments demonstrate state-of-the-art performance on both tasks, producing seamless, high-fidelity textures and accurate 3D part segmentation with precise boundaries.
</details>

---

### Mario: Multimodal Graph Reasoning with Large Language Models
著者: Yuanfu Sun, Kang Li, Pengkang Guo, Jiajin Liu, Qiaoyu Tan

<details>
<summary> 日本語要旨 </summary>

最近の大規模言語モデル（LLMs）の進歩は、多様なモーダル推論への新たな道を開いています。しかし、現在の多くの方法は依然として事前学習されたビジョン・ランゲージ・モデル（VLMs）に頼り、画像-テキストペアを個別にエンコードし、実際の多様なモーダルデータが自然に形成する関係構造を無視しています。これは、各ノードがテキストとビジュアル属性を持ち、エッジが構造的手掛かりを提供する多様なモーダルグラフ（MMGs）上での推論に動機付けられます。このような異種多様なシグナルにおいて、グラフトポロジーを保持しつつLLMベースの推論を可能にすることは、弱いクロスモーダル一貫性の解決と異種モダリティ優先度の処理という2つの主要な課題を導入します。これに対応するため、私たちはMarioと呼ばれる統一フレームワークを提案しました。このフレームワークは上記の2つの課題を同時に解決し、MMGs上で効果的なLLMベースの推論を可能にします。Marioは2つの革新的なステージから構成されています。まず第一に、グラフトポロジーによって導かれた細部にわたるクロスモーダル対照学習を通じてテキストとビジュアル特徴を共同で洗練するグラフ条件付きVLM設計です。第二に、多様なモーダル特徴をグラフ認識型のインストラクションビューとして整理し、学習可能なルーターを用いて各ノードおよびその近傍に対して最も情報量の多いモダリティ構成をLLMに提示するモダリティ適応グラフインストラクションチューニングメカニズムです。多様なMMGベンチマークにわたる広範な実験は、Marioがノード分類とリンク予測の両方で監督学習およびゼロショットシナリオにおいて最先端のグラフモデルを一貫して上回ることを示しています。コードは補足資料で利用可能です。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advances in large language models (LLMs) have opened new avenues for multimodal reasoning. Yet, most existing methods still rely on pretrained vision–language models (VLMs) to encode image–text pairs in isolation, ignoring the relational structure that real-world multimodal data naturally form. This motivates reasoning on multimodal graphs (MMGs), where each node has textual and visual attributes and edges provide structural cues. Enabling LLM-based reasoning on such heterogeneous multimodal signals while preserving graph topology introduces two key challenges: resolving weak cross-modal consistency and handling heterogeneous modality preference. To address this, we propose Mario, a unified framework that simultaneously resolves the two above challenges and enables effective LLM-based reasoning over MMGs. Mario consists of two innovative stages. Firstly, a graph-conditioned VLM design that jointly refines textual and visual features through fine-grained cross-modal contrastive learning guided by graph topology. Secondly, a modality-adaptive graph instruction tuning mechanism that organizes aligned multimodal features into graph-aware instruction views and employs a learnable router to surface, for each node and its neighborhood, the most informative modality configuration to the LLM. Extensive experiments across diverse MMG benchmarks demonstrate that Mario consistently outperforms state-of-the-art graph models in both supervised and zero-shot scenarios for node classification and link prediction. The code is available in supplementary materials.
</details>

---

### Multi-Crit: Benchmarking Multimodal Judges on Pluralistic Criteria-Following
著者: Tianyi Xiong, Yi Ge, Ming Li, Zuolong Zhang, Pranav Kulkarni, Kaishen Wang, Qi He, Zeying Zhu, Chenxi Liu, Ruibo Chen, Tong Zheng, Yanshuo Chen, Xiyao Wang, Renrui Zhang, Wenhu Chen, Heng Huang

<details>
<summary> 日本語要旨 </summary>

大規模マルチモーダルモデル（LMMs）は、その強力な指示に従う能力と人間の好みとの一貫性から、多様な評価システムで審査員として採用されることが増えています。しかし、彼らが多様で細かい評価基準に従う能力は未だ十分に探求されていません。私たちはMulti-Critを開発しました。これは、複数の基準に従う能力と信頼性のある基準レベル判断を評価するマルチモーダル審査員向けのベンチマークです。Multi-Critは、多基準人間による注釈付きの挑戦的な応答ペアを収集する厳格なデータキュレーションパイプラインを通じて構築され、オープンエンド生成タスクと検証可能な推論タスクの両方をカバーしています。さらに、多基準への従順性、基準切り替えの柔軟性、および基準レベルでの好みの衝突を認識する能力を体系的に評価するための3つの新しい指標を導入しています。25のLMMsに対する包括的な分析では、1）プロプライエタリモデルは特にオープンエンド評価で多基準への一貫した従順性を維持することが依然として難しいこと、2）オープンソースモデルはさらに多様な基準に柔軟に従う点で遅れていること、3）全体的な判断信号を用いた批評家の微調整が視覚的根拠を強化するものの、多基準レベルの判断に一般化できないことが明らかになりました。推論の微調整、テスト時スケーリング、オープンソースとプロプライエタリモデル間の境界の一貫性に関する追加分析は、現在のマルチモーダル審査員の限界をさらに探求しています。先駆的な研究として、Multi-Critは信頼できるかつ操縦可能なマルチモーダルAI評価の基盤を築いています。
</details>

<details>
<summary> 英語要旨 </summary>

Large multimodal models (LMMs) are increasingly adopted as judges in multimodal evaluation systems due to their strong instruction following and consistency with human preferences. However, their ability to follow diverse, fine-grained evaluation criteria remains underexplored. We develop Multi-Crit, a benchmark for evaluating multimodal judges on their capacity to follow pluralistic criteria and produce reliable criterion-level judgments. Covering both open-ended generation and verifiable reasoning tasks, Multi-Crit is built through a rigorous data curation pipeline that gathers challenging response pairs with multi-criterion human annotations. It further introduces three novel metrics for systematically assessing pluralistic adherence, criterion-switching flexibility, and the ability to recognize criterion-level preference conflicts. Comprehensive analysis of 25 LMMs reveals that 1) proprietary models still struggle to maintain consistent adherence to pluralistic criteria—especially in open-ended evaluation; 2) open-source models lag further behind in flexibly following diverse criteria; and 3) critic fine-tuning with holistic judgment signals enhances visual grounding but fails to generalize to pluralistic criterion-level judgment. Additional analyses on reasoning fine-tuning, test-time scaling, and boundary consistency between open-source and proprietary models further probe the limits of current multimodal judges. As a pioneering study, Multi-Crit lays the foundation for building reliable and steerable multimodal AI evaluation.
</details>

---

### Simple But Effective Triplet-Based Compression Strategies for Compact Visual Localization
著者: Torsten Sattler, Zuzana Kukelova

<details>
<summary> 日本語要旨 </summary>

視覚的ローカリゼーション、すなわち画像が撮影されたカメラの姿勢を推定する問題は、拡張現実や自律型ロボットなどの応用において重要です。これらの多くのアプリケーションではコンパクトなメモリフットプリントが求められます。そのため、視覚的ローカリゼーション用にメモリ効率の良いシーン表現を設計するために多くの研究が行われています。本論文では、構造から動作（Structure-from-Motion, SfM）点群から一部の点を選択して3Dシーン構造を圧縮することに焦点を当てます。従来の研究が複雑な最適化問題を解決しようとするのに対し、私たちは実装もほぼ容易なシンプルな戦略を提案します。私たちの圧縮戦略は、各データベース画像（SfM点群構築に使用される）のカメラ姿勢がこれらのトリプレットから正確に推定できるような点のトリプレットを選択するという考えに基づいています。その単純さにもかかわらず、私たちの戦略は現在の構造圧縮手法の最先端と同等またはそれ以上の性能を発揮します。標準的なプロダクト量子化アプローチによる特徴記述子の圧縮と組み合わせた場合、私たちのアプローチはコンパクトな視覚的ローカリゼーション用の最近の学習ベース手法と比較して有利です。
</details>

<details>
<summary> 英語要旨 </summary>

Visual localization, i.e., the problem of estimating the camera pose from which an image was taken, is an important part of applications such as augmented reality and autonomous robots. Many of these applications require a compact memory footprint. Thus, a considerable amount of work has been spent on designing memory-efficient scene representations for visual localization. In this paper, we focus on compressing the 3D structure of the scene by selecting a subset of points from a Structure-from-Motion (SfM) point cloud. In contrast to prior work, which aims to solve (complex) optimization problems, we propose a simple strategy that is almost trivial to implement. Our compression strategy is based on the idea of selecting triplets of points such that the camera pose of each database image (used to build the SfM point cloud) can be accurately estimated from these triplets. Despite its simplicity, our strategy performs similarly to or better than current state-of-the-art structure compression approaches. Combined with standard product quantization approaches to compress feature descriptors, our approach compares favorably with recent learning-based approaches for compact visual localization.
</details>

---

### Text-Driven 3D Hand Motion Generation from Sign Language Data
著者: Léore Bensabath, Mathis Petrovich, Gul Varol

<details>
<summary> 日本語要旨 </summary>

私たちの目標は、手の形状や位置、指・手・腕の動きなどの特徴を自然言語で指定することによって条件付けられる3D手の動作の生成モデルを訓練することです。このために、これまでにない規模で3D手の動作とそれに関連するテキストラベルのペアを自動的に構築します。具体的には、大規模なサイン言語ビデオデータセットと、騒音が混じった仮想的なサインカテゴリーの注釈を活用し、これらを手の動作の記述に変換します。この変換は、サイン属性の辞書や補完的な動作スクリプトのヒントを使用するLLM（大規模言語モデル）を利用して行います。このデータにより、テキスト条件付き手の動作拡散モデル（HandMDM）を訓練し、同じサイン言語内で未見のサインカテゴリーだけでなく、別のサイン言語や非サイン手の動きにも頑健性を持たせます。これらのシナリオについて広範な実験的検討を行い、私たちの訓練済みモデルとデータを公開して、この比較的新しい分野での将来の研究を支援することに貢献します。
</details>

<details>
<summary> 英語要旨 </summary>

Our goal is to train a generative model of 3D hand motions, conditioned on natural language descriptions specifying motion characteristics such as handshapes, locations, finger/hand/arm movements. To this end, we automatically build pairs of 3D hand motions and their associated textual labels with unprecedented scale. Specifically, we leverage a large-scale sign language video dataset, along with noisy pseudo-annotated sign categories, which we translate into hand motion descriptions via an LLM that utilizes a dictionary of sign attributes, as well as our complementary motion-script cues. This data enables training a text-conditioned hand motion diffusion model (HandMDM), that is robust across domains such as unseen sign categories from the same sign language, but also signs from another sign language and non-sign hand movements. We contribute extensive experimental investigation of these scenarios and will make our trained models and data publicly available to support future research in this relatively new field.
</details>

---

### DisCa: Accelerating Video Diffusion Transformers with Distillation-Compatible Learnable Feature Caching
著者: Chang Zou, Changlin Li, Songtao Liu, Zhao Zhong, Kailin Huang, Linfeng Zhang

<details>
<summary> 日本語要旨 </summary>

ディフュージョンモデルはビデオ生成分野で大きな成功を収めていますが、この進歩に伴い計算負荷が急速に増加しています。既存の加速方法の中で、トレーニングフリーの特性と顕著なスピードアップパフォーマンスを持つため人気のあるFeature Cachingがありますが、さらに圧縮すると必然的にセマンティックや詳細の低下に直面します。また、トレーニングアウェアなステップ蒸留法は画像生成では成功していますが、ビデオ生成では少数のステップで劇的な劣化を経験します。さらに、単純にトレーニングフリーのFeature Cachingをステップ蒸留モデルに適用すると、より希薄なサンプリングステップによって品質損失がさらに深刻化します。本論文では、初めてdistillation-compatibleな学習可能なFeature Cachingメカニズムを導入しています。従来のトレーニングフリーヒューリスティクスの代わりに、ディフュージョンモデル用の軽量学習可能なニューラル予測器を使用し、高次元特徴進化プロセスをより正確に捉えることができます。さらに、大規模ビデオモデルにおける極端な圧縮蒸留の課題を探求し、より安定かつ損失のない蒸留を実現するために保守的なRestricted MeanFlowアプローチを提案します。これらの取り組みにより、生成品質を維持しつつ加速境界を11.8倍まで押し広げることができました。実験は本手法の効果を示しています。コードは補足資料に含まれ、公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

While diffusion models have achieved great success in the field of video generation, this progress is accompanied by a rapidly escalating computational burden. Among the existing acceleration methods, Feature Caching is popular due to its training-free property and considerable speedup performance,but it inevitably faces semantic and detail drop with further compression. Another widely adopted method, training-aware step-distillation, though successful in image generation, also faces drastic degradation in video generation with a few steps. Furthermore, the quality loss becomes more severe when simply applying training-free feature caching to the step-distilled models, due to the sparser sampling steps. This paper novelly introduces a distillation-compatible learnable feature caching mechanism for the first time. We employ a lightweight learnable neural predictor instead of traditional training-free heuristics for diffusion models, enabling a more accurate capture of the high-dimensional feature evolution process. Furthermore, we explore the challenges of highly compressed distillation on large-scale video models and propose a conservative Restricted MeanFlow approach to achieve more stable and lossless distillation. By undertaking these initiatives, we further push the acceleration boundaries to $11.8\times$ while preserving generation quality. Extensive experiments demonstrate the effectiveness of our method. The code is in the supplementary materials and will be publicly available.
</details>

---

### GSV2X: Geometry-Aware Uncertainty Modeling and Orthogonal Fusion for Robust Roadside Perception
著者: jianqiang xu, Gensheng Pei, 刘华峰 Liu, Yazhou Yao

<details>
<summary> 日本語要旨 </summary>

信頼性の高い3D認識は、カメラとLiDARデータの堅牢な融合に依存しており、幾何学的不整合やセンサー校正エラーがこれを複雑化させています。本論文では、この課題に対処するためのGSV2Xというフレームワークを提案します。その主な貢献は二つあります。第一に、空間不確実性に対する堅牢性を達成するために、我々は2D画像特徴を3次元ガウス分布として表現し、統一された鳥瞰図（BEV）空間へ持ち上げます。カメラの幾何学に基づく可学習な摂動を取り入れることで、潜在的な校正不正確さを明示的に考慮します。第二に、モダリティ間のシナジーを最大化するために、新しい直交融合モジュールを提案します。このモジュールは制約付き注意を用いてカメラとLiDAR特徴間の直交性を強制し、冗長な情報を効果的に分離し、補完的表現の学習を促進します。挑戦的なRCooperデータセットでの広範な実験は、GSV2Xが多視点路側認識において新たな最先端を設定し、複雑な現実世界シナリオでも顕著な堅牢性を示すことを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Reliable 3D perception from multi-view roadside sensors hinges on the robust fusion of camera and LiDAR data, a task complicated by geometric misalignments and sensor calibration errors. This paper presents GSV2X, a fusion framework that tackles these challenges through two core contributions. First, to achieve robustness against spatial uncertainty, we lift 2D image features into a unified Bird's-Eye-View (BEV) space by representing them as 3D Gaussian distributions. By incorporating learnable perturbations guided by camera geometry, our model explicitly accounts for potential calibration inaccuracies. Second, to maximize the synergy between modalities, we propose a new orthogonal fusion module. This module employs constrained attention to enforce orthogonality between camera and LiDAR features, effectively disentangling redundant information and promoting the learning of complementary representations. Extensive experiments on the challenging RCooper dataset demonstrate that GSV2X sets a new state-of-the-art in multi-view roadside perception and exhibits remarkable robustness in complex, real-world scenarios.
</details>

---

### Reevaluating The Intra-modal Misalignment Hypothesis in CLIP
著者: Jonas Herzog, Yue Wang

<details>
<summary> 日本語要旨 </summary>

最近の研究では、CLIPのような対比的言語画像トレーニングによって生成される埋め込みが、画像のみのタスクには理想的でない可能性が示唆されています。主要な仮説として、対モーダル（言語-画像）の整合損失がインタラモーダル（画像-画像）の整合を無視し、画像間の類似度が不適切にキャリブレーションされることが挙げられています。本研究では、このインタラモーダルの誤整合仮説を問い直します。誤整合を示そうとする理論的議論や手法を再検討しました。その結果、コサイン類似度の分布や少数ショットまたはリトリーバルメトリクスが誤整合の信頼できる指標とならないことが明らかになりました。実際、これらのメトリクスは言語-画像トレーニングモデル（CLIP、SigLIP）と画像-画像トレーニングモデル（DINO、SigLIP2）で類似した結果を示し、これにより対比的言語-画像トレーニングから生じるインタラモーダルの誤整合は存在しないことが示されました。観測された現象は、画像埋め込み空間に根本的な欠陥を仮定することなく説明できると主張します。リトリーバルや少数ショット分類のような一般的に研究されているインタラモーダルタスクを用いた実験では、仮定された誤整合に対処することは強力なパフォーマンスを達成する上で不要であることが確認されました。
</details>

<details>
<summary> 英語要旨 </summary>

Recent research has indicated that the embeddings generated by contrastive language-image training like CLIP may not be ideal for image-only tasks. The main theory is that the inter-modal (language-image) alignment loss ignores intra-modal (image-image) alignment, leading to poorly calibrated similarities between images. In this study, we question this intra-modal misalignment hypothesis. We reexamine the theoretical arguments and techniques that seek to demonstrate the misalignment. Our findings reveal that neither the distribution of cosine similarities nor few-shot or retrieval metrics serve as reliable indicators of misalignment. In fact, these metrics yield similar results for language-image trained models (CLIP, SigLIP) and image-image trained models (DINO, SigLIP2), which indicates there is no intra-modal misalignment stemming from contrastive language-image training. We argue the observed phenomena can be explained without assuming a fundamental flaw in the image embedding space. Experiments on the commonly studied intra-modal tasks retrieval and few-shot classification confirm that addressing supposed misalignment is unnecessary for achieving strong performance.
</details>

---

### When Numbers Speak: Aligning Textual Numerals and Visual Instances in Text-to-Video Diffusion Models
著者: Zhengyang Sun, Yu Chen, Xin Zhou, Xiaofan Li, Xiwu Chen, Dingkang Liang, Xiang Bai

<details>
<summary> 日本語要旨 </summary>

テキストからビデオへの拡散モデルは、開放的なビデオ合成を可能にしましたが、プロンプトで指定された正確な数のオブジェクトを生成することにしばしば苦労します。私たちは、NUMINAというトレーニングフリーの識別後ガイドフレームワークを導入し、数値的な整合性を向上させます。NUMINAは、選択された差別化自己およびクロスアテンションヘッドを用いてプロンプトとレイアウトの不一致を識別し、カウント可能な潜在的レイアウトを導出します。その後、このレイアウトを保守的に洗練させ、クロスアテンションを調整して再生成をガイドします。新たに導入されたCountBenchでは、NUMINAはWan2.1-1.3Bモデルでカウントの精度を最大7.4％向上させ、5Bおよび14Bモデルではそれぞれ4.9％と5.5％向上します。また、CLIPの整合性も改善されつつ、時間的一貫性が維持されます。これらの結果は、構造的なガイダンスが種子探索とプロンプト強化を補完し、カウント精度の高いテキストからビデオへの拡散に向けた実用的な道筋を提供することを示しています。コードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Text-to-video diffusion models have enabled open-ended video synthesis, but often struggle with generating the correct number of objects specified in a prompt. We introduce NUMINA, a training-free identify-then-guide framework for improved numerical alignment. NUMINA identifies prompt–layout inconsistencies by selecting discriminative self- and cross-attention heads to derive a countable latent layout. It then refines this layout conservatively and modulates cross-attention to guide regeneration. On the introduced CountBench, NUMINA improves counting accuracy by up to 7.4\% on Wan2.1-1.3B, and by 4.9\% and 5.5\% on 5B and 14B models, respectively. Furthermore, CLIP alignment is improved while maintaining temporal consistency. These results demonstrate that structural guidance complements seed search and prompt enhancement, offering a practical path toward count-accurate text-to-video diffusion. The code will be made available.
</details>

---

### Ov3R: Open-Vocabulary Semantic 3D Reconstruction from RGB Videos
著者: ZIREN GONG, Xiaohan Li, Fabio Tosi, Jiawei Han, Stefano Mattoccia, Jianfei Cai, Matteo Poggi

<details>
<summary> 日本語要旨 </summary>

私たちは、RGBビデオストリームからの開放語彙セマンティック3D再構成を進化させることを目的とした新しいフレームワークであるOv3Rを紹介します。このシステムは、CLIP-informed 3D再構成モジュールのCLIP3Rと、2D-3D開放語彙セマンティックモジュールの2D–3D OVSの二つの主要なコンポーネントを特徴としています。CLIP3Rは重複するクリップから密な点マップを予測し、オブジェクトレベルのセマンティクスも提供します。2D–3D OVSは空間的、幾何学的、およびセマンティックな手がかりを統合した融合された記述子を学習することで、2D特徴を3Dに昇華します。Ov3Rは他の方法と異なり、再構成プロセスに直接CLIPセマンティクスを組み込んでおり、グローバルに一貫した幾何学と細部までのセマンティックアライメントを可能にします。私たちのフレームワークは、密な3D再構成と開放語彙3Dセグメンテーションの両方で最先端の性能を達成し、リアルタイムかつセマンティックに対応したSpatial AIへの一歩前進を示しています。
</details>

<details>
<summary> 英語要旨 </summary>

We present Ov3R, a novel framework for open-vocabulary semantic 3D reconstruction from RGB video streams, designed to advance Spatial AI. The system features two key components: CLIP3R, a CLIP-informed 3D reconstruction module that predicts dense point maps from overlapping clips alongside object-level semantics; and 2D–3D OVS, a 2D-3D open-vocabulary semantic module that lifts 2D features into 3D by learning fused descriptors integrating spatial, geometric, and semantic cues. Unlike prior methods, Ov3R incorporates CLIP semantics directly into the reconstruction process, enabling globally consistent geometry and fine-grained semantic alignment. Our framework achieves state-of-the-art performance in both dense 3D reconstruction and open-vocabulary 3D segmentation — marking a step forward toward real-time, semantics-aware Spatial AI.
</details>

---

### MD2E: Modeling Depth-to-Edge Cues for Monocular Metric Depth Estimation
著者: Chao Ning, Minghe Shen, Naoto Yokoya

<details>
<summary> 日本語要旨 </summary>

私たちは、トレーニングや推論時にカメラの内部パラメータを使用せずに単眼測定深度推定（MMDE）を研究します。焦点距離とシーンの深さが一緒に変化する場合、画像からの深さの変化は認識しにくいですが、エッジ周波数統計は系統的でスケール相関のあるシフトを示します。この観察に基づき、予測されたエッジマップのフーリエスペクトルを分析し、メトリックスケールの代理として使用する単一のスコアを出力するスペクトラル量的推定器（SQE）を導入します。私たちは、深度注釈からエッジターゲットを導き出し、スペクトラルスコアを用いてメトリックスケールをキャリブレートし、エッジ予測を使用して深度境界を正則化しながらメトリック深度を生成する方法であるMD2Eを提案します。多様なカメラやデータセットにわたり、MD2Eはゼロショットおよびファインチューニングの設定で、カメラメタデータを使用せずに単眼測定深度の最先端を達成します。
</details>

<details>
<summary> 英語要旨 </summary>

We study monocular metric depth estimation (MMDE) without camera intrinsics at training or inference. When focal length and scene depth vary together, depth changes are difficult to perceive from image, yet the edge-frequency statistics exhibit systematic, scale-correlated shifts. Building on this observation, we introduce a spectral quantile estimator (SQE) that analyzes the Fourier spectrum of a predicted edge map and outputs a single score used as a proxy for metric scale. We propose MD2E, a method that models depth-to-edge cues by deriving edge targets from depth annotations, calibrating metric scale using the spectral score, and using edge predictions to regularize depth boundaries while producing metric depth. Across diverse cameras and datasets, MD2E achieves state-of-the-art monocular metric depth in both zero-shot and fine-tuning settings without camera metadata.
</details>

---

### Multi-Scale Speculative Decoding
著者: Elia Peruzzo, Guillaume Sautiere, Amirhossein Habibian

<details>
<summary> 日本語要旨 </summary>

自己回帰（AR）モデルは画像合成において顕著な成功を収めていますが、その順次的性質は大きな遅延制約を課します。仮定的デコーディングは加速の有望な手段ですが、既存のアプローチはトークンレベルの曖昧さと空間認識の欠如によって制限されています。本研究では、多解像度ドラフティングを空間情報に基づく検証と組み合わせた新しいフレームワークであるマルチスケールローカル仮定的デコーディング（MuLo-SD）を紹介します。この方法は、低解像度のドラッファーと学習済みアップサンプラーを組み合わせて候補画像トークンを提案し、それらが高解像度ターゲットモデルによって並列で検証されます。重要なことに、私たちはローカル拒否および再サンプリングメカニズムを導入し、初回の拒否後のラスタースキャン再サンプリングではなく、空間的近傍に焦点を当てたドラフトエラーの効率的な修正を可能にします。MuLo-SDが最大で1.7倍の加速を達成し、EAGLE-2やLANTERNといった強力な仮定的デコーディングベースラインを超えることを示します。これは加速性能においてでありながら、セマンティックアライメントと知覚品質の面では同等の結果を維持しています。これらの結果はGenEval、DPG-Bench、MS-COCO 5k検証分割におけるFID/HPSv2を用いて検証されました。広範なアブレーション実験では、アップサンプリングデザイン、確率プーリング、近傍拡張付きのローカル拒否および再サンプリングの影響を明らかにしています。私たちのアプローチは画像合成における仮定的デコーディングの新しいステート・オブ・ザ・アートを設定し、効率と忠実度の間のギャップを埋めています。
</details>

<details>
<summary> 英語要旨 </summary>

Autoregressive (AR) models have achieved remarkable success in image synthesis, yet their sequential nature imposes significant latency constraints. Speculative Decoding offers a promising avenue for acceleration, but existing approaches are limited by token-level ambiguity and lack of spatial awareness. In this work, we introduce Multi-Scale Local Speculative Decoding (MuLo-SD), a novel framework that combines multi-resolution drafting with spatially informed verification to accelerate AR image generation. Our method leverages a low-resolution drafter paired with learned up-samplers to propose candidate image tokens, which are then verified in parallel by a high-resolution target model. Crucially, we incorporate a local rejection and resampling mechanism, enabling efficient correction of draft errors by focusing on spatial neighborhoods rather than raster-scan resampling after the first rejection. We demonstrate that MuLo-SD achieves substantial speedups --- up to $\mathbf{1.7\times}$ --- outperforming strong speculative decoding baselines such as EAGLE-2 and LANTERN in terms of acceleration, while maintaining comparable semantic alignment and perceptual quality. These results are validated using GenEval, DPG-Bench, and FID/HPSv2 on the MS-COCO 5k validation split. Extensive ablations highlight the impact of up-sampling design, probability pooling, and local rejection and resampling with neighborhood expansion. Our approach sets a new state-of-the-art in speculative decoding for image synthesis, bridging the gap between efficiency and fidelity.
</details>

---

### Linking Modality Isolation in Heterogeneous Collaborative Perception
著者: Changxing Liu, Zichen Chao, Siheng Chen

<details>
<summary> 日本語要旨 </summary>

複数のエージェント間でデータ交換を活用する協調知覚は、全体的な知覚能力を向上させます。しかし、エージェント間の異質性によりドメインギャップが生じ、これが協調を妨げるという問題があります。この問題はさらに「モダリティ孤立」と呼ばれる未解明の問題によって悪化します。これは、異なるモダリティを持つ複数のエージェントがトレーニングデータフレームで共起しない場合に発生し、クロスモーダルドメインギャップを拡大します。既存の整列方法は空間的に重なる観測からの監督に依存しており、モダリティ孤立を処理できません。この課題に対応するため、我々はCodeAlignという初めての効率的な共起フリー整列フレームワークを提案します。これはクロスモーダル特徴-コード-特徴（FCF）翻訳によってモダリティを滑らかに整列させます。主なアイデアは、コードブックを用いて表現の一貫性を明示的に識別し、モダリティ固有の特徴空間間で直接マッピングを学習することです。これにより、空間的対応が不要になります。コードブックは特徴空間をコード空間に規則化し、コンパクトでありながら表現力豊かな表現を提供します。各モダリティ用のコード空間を準備した後、CodeAlignは特徴を他のモダリティの対応するコードにマッピングし、それをターゲットコード空間で再び特徴にデコードすることで効果的な整列を可能にします。実験結果は、3つのモダリティを統合した場合、CodeAlignが既存の整列方法よりもトレーニングパラメータを8%しか必要とせず、通信負荷を1024倍削減し、OPV2VおよびDAIR-V2Xデータセットで最先端の知覚性能を達成することを示しています。コードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Collaborative perception leverages data exchange among multiple agents to enhance overall perception capabilities. However, heterogeneity across agents introduces domain gaps that hinder collaboration, and this is further exacerbated by an underexplored issue: modality isolation. It arises when multiple agents with different modalities never co-occur in any training data frame, enlarging cross-modal domain gaps. Existing alignment methods rely on supervision from spatially overlapping observations, thus fail to handle modality isolation. To address this challenge, we propose CodeAlign, the first efficient, co-occurrence-free alignment framework that smoothly aligns modalities via cross-modal feature-code-feature(FCF) translation. The key idea is to explicitly identify the representation consistency through codebook, and directly learn mappings between modality-specific feature spaces, thereby eliminating the need for spatial correspondence. Codebooks regularize feature spaces into code spaces, providing compact yet expressive representations. With a prepared code space for each modality, CodeAlign learns FCF translations that map features to the corresponding codes of other modalities, which are then decoded back into features in the target code space, enabling effective alignment. Experiments show that, when integrating three modalities, CodeAlign requires only 8% of the training parameters of prior alignment methods, reduces communication load by 1024x, and achieves state-of-the-art perception performance on both OPV2V and DAIR-V2X dataset. Code will be released.
</details>

---

### DocPrune: Efficient Document Question Answering Via Background, Question, and Comprehension-aware Token Pruning
著者: Joonmyung Choi, Sanghyeok Lee, Jongha Kim, Sehyung Kim, Dohwan Ko, Jihyung Kil, Hyunwoo J. Kim

<details>
<summary> 日本語要旨 </summary>

最近の視覚言語モデルは、テキスト、表、図などの構造化された視覚的手がかりを活用したドキュメント質問応答を含む多様なマルチモーダルタスクで強力な性能を示しています。しかし、自然画像とは異なり、ドキュメント画像には大きな背景があり、支持する証拠が少ないため、特に長文書では多くの計算資源が無駄になっています。私たちは、自然画像や動画向けの既存のトークン削減方法がドキュメント固有の構造的希薄性を活用することに限界があることを観察しました。これに対処するため、効率的な長文書理解のためのトレーニングフリーのドキュメントトークンプルーニングフレームワークであるDOCPRUNEを提案します。この方法はタスクに必要なトークンだけを保持し、不要なトークン（背景や質問と関係のないもの）を削除します。さらに、モデルの理解レベルに基づいて適切な層でトークンプルーニングを開始することが自動的に行われます。M3DocRAGベンチマークでの実験では、DOCPRUNEがエンコーダーで3.0倍、デコーダーで3.3倍のスループットを向上させ、F1スコアも+1.0ポイント改善し、追加のトレーニングなしに高い精度と効率性を両立しています。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advances in vision–language models have shown strong performance across diverse multimodal tasks, including document question answering that leverages structured visual cues from text, tables, and figures. However, unlike natural images, document images contain large backgrounds and only sparse supporting evidence, leading to the waste of substantial computational resources, especially for long documents. We observe that existing token reduction methods for natural images and videos fall short in utilizing the structural sparsity unique to documents. To address this, we propose DOCPRUNE, a training-free document token pruning framework designed for efficient long document understanding. The proposed method preserves only the essential tokens for the task while removing unnecessary ones, such as background or question-irrelevant tokens. Moreover, it automatically selects the appropriate layers to initiate token pruning based on the model’s level of comprehension. Our experiments on the M3DocRAG benchmark show that DOCPRUNE improves throughput by 3.0× and 3.3× in the encoder and decoder, respectively, while boosting the F1 score by +1.0, achieving both higher accuracy and efficiency without any additional training.
</details>

---

### StereoWorld: Geometry-Aware Monocular-to-Stereo Video Generation
著者: Ke Xing, longfei li, Yuyang Yin, Hanwen Liang, Guixun Luo, Chen Fang, Jue Wang, Konstantinos N. Plataniotis, Xiaojie Jin, Yao Zhao, Yunchao Wei

<details>
<summary> 日本語要旨 </summary>

XRデバイスの普及拡大に伴い、高品質な立体映像への需要が急増していますが、その制作はコストがかかり、アーティファクトが発生しやすいという課題があります。この問題に対処するため、我々は高品質なモノステレオ映像生成のために事前学習済みビデオジェネレータを再利用する**エンド・トゥ・エンドフレームワーク、StereoWorld**を提案します。このフレームワークは、モノステレオ映像入力に対してモデルを条件付けると同時に、3D構造の忠実性を保証するために**幾何学的認識に基づく正則化**で生成を明示的に監督します。さらに、効率的な高解像度合成を可能にするスペースタイムティリング方式が統合されています。大規模なトレーニングと評価を可能にするため、自然な人間の網膜間距離（IPD）に整列した**高解像度立体映像データセット**を構築しました。このデータセットは11Mフレーム以上を含んでいます。広範な実験により、StereoWorldが既存の手法を大幅に上回ることが示されており、視覚的忠実性と幾何学的一貫性に優れた立体映像を生成しています。
</details>

<details>
<summary> 英語要旨 </summary>

The growing adoption of XR devices has fueled strong demand for high-quality stereo video, yet its production remains costly and artifact-prone. To address this challenge, we present **StereoWorld**, an **end-to-end framework** that repurposes a pretrained video generator for high-fidelity monocular-to-stereo video generation. Our framework jointly conditions the model on the monocular video input while explicitly supervising the generation with a **geometry-aware regularization** to ensure 3D structural fidelity. A spatio-temporal tiling scheme is further integrated to enable efficient, high-resolution synthesis. To enable large-scale training and evaluation, we curate a **high-definition stereo video dataset** containing over 11M frames aligned to natural human interpupillary distance (IPD). Extensive experiments demonstrate that StereoWorld substantially outperforms prior methods, generating stereo videos with superior visual fidelity and geometric consistency.
</details>

---

### DABO: Difficulty-Aware Bayesian Optimization with Diffusion-Learned Priors
著者: Mengyang Li, Pinlong Zhao

<details>
<summary> 日本語要旨 </summary>

ハイパーパラメータ最適化（HPO）の効率性はディープラーニングにおいて重要ですが、現状の手法には根本的な欠陥があります：それらは難易度を無視しており、すべてのハイパーパラメータ設定を均一に扱います。このアプローチは効率的でないリソース配分を引き起こし、単純な領域では予算を無駄にしつつ、複雑で険しい地形を十分に探索せず、その結果として検索効率や最終的なパフォーマンスを重大に損ないます。この普遍的な課題に対処するために、私たちはDABOというフレームワークを導入します。これは、効率的なFreeze-Thaw Bayesian Optimizationの文脈で難易度に配慮したチューニングを先駆けています。まず、最適化の難易度を階層的にモデル化します。次に、手作りの事前分布から脱却し、120,000個の実際の学習曲線で条件付き拡散モデルをトレーニングし、2.3倍高い忠実度を持つ合成データを生成します。このデータは私たちの難易度に配慮した代理モデルと獲得関数をトレーニングし、探索戦略を動的に適応させます。75のタスクでDABOは、最先端の難易度無視型手法であるifBOと比較して11-18％のリグレット削減を実現します。私たちの研究はHPOにおける新しいパラダイムを確立し、設定中心から難易度に配慮したリソース配分へと焦点を移すことで、より堅牢かつ効率的な最適化を可能にします。
</details>

<details>
<summary> 英語要旨 </summary>

The efficiency of hyperparameter optimization (HPO) is critical for deep learning, yet state-of-the-art methods share a fundamental flaw: they are difficulty-agnostic, treating all hyperparameter configurations homogeneously. This approach leads to inefficient resource allocation, wasting budget in simple regions while under-exploring complex, rugged landscapes, and thereby critically undermining both search efficiency and final performance. To address this universal challenge, we introduce DABO, a framework that pioneers difficulty-aware tuning within the efficient context of Freeze-Thaw Bayesian Optimization. We first model optimization difficulty hierarchically. Then, departing from hand-crafted priors, we train a conditional diffusion model on 120,000 real learning curves, generating synthetic data with 2.3$\times$ higher fidelity. This data trains our difficulty-aware surrogate model and acquisition function to dynamically adapt the search strategy. Across 75 tasks, DABO reduces regret by 11-18\% compared to the leading difficulty-agnostic method, ifBO. Our work establishes a new paradigm for HPO, shifting the focus from configuration-centric to difficulty-aware resource allocation to enable more robust and efficient optimization.
</details>

---

### AwareVLN: Reasoning with Self-awareness for Vision-Language Navigation
著者: Wenxuan Guo, Xiuwei Xu, Yichen Liu, Xiangyu Li, Hang Yin, Huangxing Chen, Wenzhao Zheng, Jianjiang Feng, Jie Zhou, Jiwen Lu

<details>
<summary> 日本語要旨 </summary>

ビジョンと言語によるナビゲーション（VLN）は、エージェントが自身の動きを視覚環境に基づいて言語指示に根拠付けることを要求します。最先端の手法では、ビジョン・ランゲージモデル（VLM）の推論能力を活用してエンドツーエンドでアクション予測を行いますが、多くはエージェント、指示、およびシーン間の関係について明確かつ説明可能な理解を欠いています。一方で、ヒューリスティックプランニング用にシーンマップを明示的に構築することは直感的に魅力的ですが、追加の3Dセンサーに依存し、大規模なビジョン・ランゲージ事前学習を妨げます。このギャップを埋めるために、私たちは自己認識推論メカニズムを搭載した新しいフレームワークであるAwareVLNを提案します。これにより、エージェントは完全なエンドツーエンドかつデータ駆動の方法で自身の状態とタスク進行を理解することが可能になります。私たちのアプローチは、2つの重要な革新点を特徴としています：（1）空間的およびタスク指向の自己認識を促進する構造推論モジュール、（2）効果的なトレーニング用に設計された進捗分割付きの自動データエンジン。Habitatシミュレーター上の様々なデータセットで行った広範囲な実験により、私たちのAwareVLNは以前の最先端ビジョン・ランゲージナビゲーション手法を大幅に上回ることが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

Vision-and-Language Navigation (VLN) requires an agent to ground language instructions to its own movement within a visual environment. While state-of-the-art methods leverage the reasoning capabilities of Vision-Language Models (VLMs) for end-to-end action prediction, they often lack an explicit and explainable understanding of the relationships between the agent, the instruction, and the scene. Conversely, explicitly building a scene map for heuristic planning is intuitively appealing but relies on additional 3D sensors and hinders large-scale vision-language pre-training. To bridge this gap, we propose AwareVLN, a novel framework that equips the navigation model with a self-aware reasoning mechanism, enabling it to understand the agent's state and task progress in a fully end-to-end and data-driven manner. Our approach features two key innovations: (1) a structural reasoning module that fosters spatial and task-oriented self-awareness, and (2) an automatic data engine with progress division for effective training. Extensive experiments on various datasets in Habitat simulator show our AwareVLN significantly outperforms previous state-of-the-art vision-language navigation methods.
</details>

---

### Beyond Generation: Advancing Image Editing Priors for Depth and Normal Estimation
著者: jiyuan WANG, Chunyu Lin, Lei Sun, Rongying Liu, Lang Nie, Mingxing Li, Kang Liao, Xiangxiang Chu

<details>
<summary> 日本語要旨 </summary>

事前学習されたテキストから画像（T2I）生成モデルの先行知識は、深度と法線予測において成功を収めています。しかし、密な予測は本質的に画像から画像へのタスクであるため、画像編集モデルがT2I生成モデルよりも微調整の基盤として適している可能性を示唆します。この動機に基づき、密な幾何学推定のための編集者およびジェネレーターの両方の微調整挙動について体系的な分析を行います。私たちの発見は、編集モデルが固有の構造的先行知識を持っており、「洗練」することでその内在的特徴に基づいてより安定して収束し、最終的に生成モデルの対抗馬よりも高い性能を達成することを示しています。これらの発見に基づき、私たちはDiffusion Transformer（DiT）アーキテクチャに基づく先進的な編集モデルを密な幾何学予測のために適応する初めてのフレームワークである\textbf{FE2E}を導入します。具体的には、この決定論的タスクに編集者を合わせるために、元々の流れマッチング損失を「一貫した速度」トレーニング目標に再設計します。また、編集者のネイティブBFloat16フォーマットと私たちのタスクが要求する高精度との間の精度の衝突を解決するために対数量子化を使用します。さらに、編集者の廃棄された領域を再利用して、コストなしで深度と法線の共同推定を行い、これが推論効率を向上させます。トレーニングデータを拡大することなく、FE2Eはゼロショット単眼深度および法線予測において複数のデータセットで顕著な性能向上を達成します。特に、ETH3Dデータセットで35％以上のパフォーマンス向上を実現し、100倍のデータでトレーニングされたDepthAnythingシリーズを凌駕しています。
</details>

<details>
<summary> 英語要旨 </summary>

Pre-trained text-to-image (T2I) generative priors have shown success in depth and normal prediction. However, dense prediction is inherently an image-to-image task, suggesting that image editing models, rather than T2I generative models, may be a more suitable foundation for fine-tuning. Motivated by this, we conduct a systematic analysis of the fine-tuning behaviors of both editors and generators for dense geometry estimation. Our findings show that editing models possess inherent structural priors, which enable them to converge more stably by "refining" their innate features, and ultimately achieve higher performance than their generative counterparts. Based on these findings, we introduce \textbf{FE2E}, a framework that pioneeringly adapts an advanced editing model based on Diffusion Transformer (DiT) architecture for dense geometry prediction. Specifically, to tailor the editor for this deterministic task, we reformulate the editor's original flow matching loss into the "consistent velocity" training objective. And we use logarithmic quantization to resolve the precision conflict between the editor's native BFloat16 format and the high precision demand of our tasks. Additionally, we repurpose the editor's discarded region for a cost-free joint estimation of depth and normals, which improves the inference efficiency. Without scaling up the training data, FE2E achieves impressive performance improvements in zero-shot monocular depth and normal estimation across multiple datasets. Notably, it achieves over 35\% performance gains on the ETH3D dataset and outperforms the DepthAnything series, which is trained on 100$\times$ data.
</details>

---

### QuietPrune: Query-Guided Early Token Pruning for Vision-Language Models
著者: Tianxiao Gao, Shanwei Zhao, Shuo Fang, Shiai Zhu, Chenguang Ma

<details>
<summary> 日本語要旨 </summary>

ビジョン言語モデル（VLMs）はマルチモーダルタスクにおいて強力な能力を示しますが、多数の視覚トークンが大きな計算コストを引き起こします。本論文では、冗長な視覚トークンをVLMsから除去し、計算効率を向上させるための「QuietPrune」というQUery-guIded Early Token Pruning法を提案します。従来の後期剪定方法とは異なり、ビジョントランスフォーマー（ViT）内で早期剪定を実施することによって、ラテンシーの低減と精度維持の両方の利点が得られることを認識しています。早期剪定で生じるセマンティック損失問題に対処するため、VLMs内のプロジェクターの逆変換を行う軽量アダプターを設計しました。この提案されたアダプターは文脈的なクエリを視覚領域の[Q-CLS]（Query [CLS]）トークンに変換し、ViT剪定のためのテキストガイドを提供します。剪定中は、視覚的・テキスト的関連性に基づく半構造化剪定スキームを導入します。具体的には、主流のVLMsで一般的な視覚トークンのマージ操作を受け入れるために、空間的に隣接する$2 \times 2$トークンをグループ化します。各グループの関連性メトリックとして、[Q-CLS]トークンと視覚トークン間の平均注意スコアを使用し、追加計算を避けます。その後、位置的な連続性を保持しつつ、関連性スコアに基づいてグループレベルで剪定が行われます。剪定後は冗長トークンを単一のトークンに集約して文脈的な手掛かりを維持します。私たちの方法は、既存の後期剪定法と比較してQwen3-VLおよびInternVL3シリーズで最大19.0%のプレフィルラテンシー低減を達成し、4.2%の精度向上を実現します。
</details>

<details>
<summary> 英語要旨 </summary>

Vision-language models (VLMs) demonstrate powerful capabilities in multimodal tasks. However, the large number of visual tokens imposes a significant computational cost. In this paper, we propose QuietPrune, a QUery-guIded Early Token Pruning method to remove redundant visual tokens within VLMs, thereby enhancing computational efficiency. Unlike previous late pruning methods, we recognize that implementing early pruning within the vision transformer (ViT) can achieve benefits in both latency reduction and accuracy maintenance. To address the semantic loss problem in early pruning, we design a lightweight adapter by performing a inverse transformation of the projector in VLMs. The proposed adapter converts the contextual query into a visual domain [Q-CLS] (Query [CLS]) token, providing textual guidance for ViT pruning. During pruning, we further introduce a semi-structured pruning scheme based on visual-textual relevance. Specifically, we group spatially adjacent $2 \times 2$ tokens to accommodate the visual token merging operation prevalent in mainstream VLMs. We use the mean attention scores between the [Q-CLS] token and the visual tokens as the relevance metric for each group, avoiding additional computation. Pruning is then applied at the group level based on the relevance score, preserving positional continuity. After pruning, we aggregate the redundant tokens into a single token to maintain context cues. Our method achieves up to 19.0\% reduction in prefill latency while outperforming 4.2\% in accuracy on the recent Qwen3-VL and InternVL3 series compared to existing late pruning methods.
</details>

---

### ViBES: A Conversational Agent with Behaviorally-Intelligent 3D Virtual Body
著者: Juze Zhang, Changan Chen, Xin Chen, Heng Yu, Tiange Xiang, Ali Sartaz Khan, Shrinidhi Kowshika Lakshmikanth, Ehsan Adeli

<details>
<summary> 日本語要旨 </summary>

人間のコミュニケーションは本質的に多様なモードと社会的であり、言葉、音調、身振りが共同して意図を伝えます。しかし、これまでのシステムでは人間の行動を翻訳タスクとしてモデル化し、特定の発話に対応する動作クリップへのマッピング（共起ジェスチャーやテキストからの動き）を行っており、いつ動くか、何をするか、または多ターンダイアログでどのように適応するかという主体的な意思決定が必要ありません。これにより、タイミングが脆弱化し、社会的根拠が弱く、スピーチ、テキスト、動きが孤立してトレーニングまたは推測される断片的な構造に陥ります。私たちはViBES（Voice in Behavioral Expression and Synchrony）を導入します。これは言語と動作を共同で計画し、対話条件付きの身体行動を実行する会話型3Dエージェントです。具体的には、ViBESはスピーチ・言語・行動（SLB）モデルであり、混合モダリティ専門家（MoME）バックボーンを持っています：スピーチ、顔の表情、体の動きに分割されたトランスフォーマー専門家です。このモデルは、各専門家ごとにパラメータが分割されるハードなモダリティ別ルーティングを用いて交互の多様なトークンストリームを処理し、クロス専門家注意によって情報を共有します。強力な事前学習済みの音声言語モデルを活用することで、エージェントは混合イニシアチブインタラクションをサポートし、ユーザーが会話中にスピーチ、入力、または身体行動の指示を発出できるようになり、システムはストリーミング応答用の制御可能な振る舞いフックを公開します。さらに、多ターン会話におけるダイアログ・動作整合性と行動品質の自動評価指標でベンチマークし、強力な共起ジェスチャーやテキストからの動きベースラインに対して一貫した改善を観察します。ViBESは「音声条件付き動作生成」を超えて、言語、音調、動きが共同で生成される主体的なバーチャルボディに向かい、制御可能で社会的に優れた3Dインタラクションを実現します。
</details>

<details>
<summary> 英語要旨 </summary>

Human communication is inherently multimodal and social: words, prosody, and body language jointly carry intent. Yet most prior systems model human behavior as a translation task—co-speech gesture or text-to-motion that maps a fixed utterance to motion clips—without requiring agentic decision-making about when to move, what to do, or how to adapt across multi-turn dialogue. This leads to brittle timing, weak social grounding, and fragmented stacks where speech, text, and motion are trained or inferred in isolation. We introduce ViBES (Voice in Behavioral Expression and Synchrony), a conversational 3D agent that jointly plans language and movement and executes dialogue-conditioned body actions. Concretely, ViBES is a speech-language-behavior (SLB) model with a mixture-of-modality-experts (MoME) backbone: modality-partitioned transformer experts for speech, facial expression, and body motion. The model processes interleaved multimodal token streams with hard routing by modality (parameters are split per expert), while sharing information through cross-expert attention. By leveraging strong pretrained speech-language models, the agent supports mixed-initiative interaction: users can speak, type, or issue body-action directives mid-conversation, and the system exposes controllable behavior hooks for streaming responses. We further benchmark on multi-turn conversation with automatic metrics of dialogue–motion alignment and behavior quality, and observe consistent gains over strong co-speech and text-to-motion baselines. ViBES goes beyond “speech-conditioned motion generation” toward agentic virtual bodies where language, prosody, and movement are jointly generated, enabling controllable, socially competent 3D interaction.
</details>

---

### Coverage Optimization for Camera View Selection
著者: Timothy Chen, Adam Dai, Maximilian Adang, Grace Gao, Mac Schwager

<details>
<summary> 日本語要旨 </summary>

3D再構成の学習に使用されるデータの質は、効率的かつ正確なシーンモデリングを可能にするために重要です。私たちはアクティブビュー選択問題を研究し、情報量のあるカメラポジションを選択するための単純で解釈可能な基準を導く原理的分析を開発しました。私たちの重要な洞察は、情報量のあるビューが計算可能なフィッシャー情報利得の近似値を最小化することで得られるというものです。これにより、過去のカメラによって不十分に観測された幾何学をカバーするビューポイントが好まれるようになります。この結果、トランスミッタンス推定を必要とせず、ノイズやトレーニングダイナミクスに対して頑健な軽量カバレッジベースのビュー選択メトリックが導かれます。私たちはこの方法をNerfstudioフレームワークに統合し、シンセティックおよび実際のシーンで評価しました。複数のデータセットと放射場基準線を用いた比較では、私たちの方法は最先端のアクティブビュー選択手法に対して一貫して改善された再構成品質を達成しました。
</details>

<details>
<summary> 英語要旨 </summary>

What makes a good viewpoint? The quality of the data used to learn 3D reconstructions is crucial for enabling efficient and accurate scene modeling. We study the active view selection problem and develop a principled analysis that yields a simple and interpretable criterion for selecting informative camera poses. Our key insight is that informative views can be obtained by minimizing a tractable approximation of the Fisher Information Gain, which reduces to favoring viewpoints that cover geometry that has been insufficiently observed by past cameras. This leads to a lightweight coverage-based view selection metric that avoids expensive transmittance estimation and is robust to noise and training dynamics. We integrate our method into the Nerfstudio framework and evaluate it on synthetic and real scenes. Across multiple datasets and radiance-field baselines, our method achieves consistently improved reconstruction quality compared to state-of-the-art active view selection methods.
</details>

---

### Feed-forward Gaussian Registration for Head Avatar Creation and Editing
著者: Malte Prinzler, Paulo Gotardo, Siyu Tang, Timo Bolkart

<details>
<summary> 日本語要旨 </summary>

私たちは、MATCH（Multi-view Avatars from Topologically Corresponding Heads）を紹介します。これは、高品質な頭部アバターの作成と編集に使用されるマルチビューガウシアン登録法です。最先端のマルチビューヘッドアバターは時間がかかるヘッドトラッキングを必要とし、その後高価なアバター最適化が行われます。これにより、合計作成時間が1日以上になることがあります。MATCHでは、カリブレーションされたマルチビュー画像から直接、0.5秒/フレームで対応するガウシアンスプラットテクスチャを予測します。学習したフレーム間の個別の対応関係により、迅速にパーソナライズされた頭部アバターを構築できますが、異なる被写体間の対応関係は表情転送、最適化フリートラッキング、セマンティック編集、およびアイデンティティ補間など、さまざまな用途に利用できます。このような対応関係をエンドツーエンドで確立するために、固定されたテンプレートメッシュのUVレイアウト上でガウシアンスプラットのテクスチャを予測するトランスフォーマー型モデルを学習します。この目的のために、各UVマップトークンがその対応するメッシュ領域を描写する画像トークンにのみ注意を払うという新しい登録ガイド付きアテンションブロックを導入します。MATCHは、新視点合成、幾何学的登録、頭部アバター生成などの分野で既存の方法を上回ります。特に後者は、質的に最も近いベースラインよりも10倍速いです。コードとモデル重みは受理され次第公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

We present MATCH (Multi-view Avatars from Topologically Corresponding Heads), a multi-view Gaussian registration method for high-quality head avatar creation and editing. State-of-the-art multi-view head avatars require time-consuming head tracking, which is followed by an expensive avatar optimization, often resulting in a total creation time that exceeds one day. MATCH instead directly predicts Gaussian splat textures in correspondence from calibrated multi-view images in 0.5 seconds per frame. While the learned intra-subject correspondence across frames allows us to quickly build personalized head avatars, correspondence across subjects enables various applications such as expression transfer, optimization-free tracking, semantic editing, and identity interpolation. We learn to establish such correspondences end-to-end, with a transformer-based model that predicts textures of Gaussian splats in the fixed UV layout of a template mesh. To this end, we introduce a novel registration-guided attention block, in which each UV map token attends exclusively to image tokens depicting its corresponding mesh region. MATCH outperforms existing methods for novel-view synthesis, geometry registration, and head avatar generation, the latter being $10\times$ faster than the qualitatively closest baseline. Code and model weights will be published upon acceptance.
</details>

---

### Reliev3R: Relieving Feed-forward 3D Reconstruction from Multi-View Geometric Annotations
著者: Youyu Chen, Junjun Jiang, Yueru Luo, Kui Jiang, Xianming Liu, Xu Yan, Dave Zhenyu Chen

<details>
<summary> 日本語要旨 </summary>

最近の進歩により、フィードフォワード再構成モデル（FFRMs）は、再構成品質と複数の下流タスクへの適応性において大きな可能性を示しています。しかし、3D点マップやカメラ姿勢などの多視点幾何学的アノテーションに対する過度の依存は、FFRMsの完全監督トレーニングスキームを拡張しにくくしています。本論文では、コストがかさむ多視点幾何学的アノテーションなしでFFRMsをゼロから訓練するための弱監督パラダイム「Reliev3R」を提案します。幾何学的センサーデータや計算集約型の構造復元前処理に依存しないことで、我々の方法はプリトレーニングモデルのゼロショット予測から得られる単眼相対深度や画像スパースな対応関係を直接利用して3D知識を引き出します。Reliev3Rの中核には、多視点幾何学的一貫性のための監督を容易にするための不確実性認識型相対深度損失と三角法ベースの再投影損失が設計されています。データ量が少ない中でゼロからトレーニングすることにより、Reliev3Rはその完全監督の兄弟モデルに追いつき、低コストの3D再構成監視およびスケーラブルなFFRMsへの一歩を踏み出します。
</details>

<details>
<summary> 英語要旨 </summary>

With recent advances, Feed-forward Reconstruction Models (FFRMs) have demonstrated great potential in reconstruction quality and adaptiveness to multiple downstream tasks. However, the excessive reliance on multi-view geometric annotations, e.g. 3D point maps and camera poses, makes the fully-supervised training scheme of FFRMs difficult to scale up. In this paper, we propose Reliev3R, a weakly-supervised paradigm for training FFRMs from scratch without cost-prohibitive multi-view geometric annotations. Relieving the reliance on geometric sensory data and compute-exhaustive structure-from-motion preprocessing, our method draws 3D knowledge directly from monocular relative depths and image sparse correspondences given by zero-shot predictions of pretrained models. At the core of Reliev3R, we design an ambiguity-aware relative depth loss and a trigonometry-based reprojection loss to facilitate supervision for multi-view geometric consistency. Training from scratch with the less data, Reliev3R catches up with its fully-supervised sibling models, taking a step towards low-cost 3D reconstruction supervisions and scalable FFRMs.
</details>

---

### TriDF: Evaluating Perception, Detection, and Hallucination for Interpretable DeepFake Detection
著者: Jian-Yu Jiang-Lin, Kang-Yang Huang, LING ZOU, Ling Lo, Sheng-Ping Yang, Yu-Wen Tseng, Kun-Hsiang Lin, Chia-Ling Chen, Yu-Ting Ta, Yan-Tsung Wang, Po-Ching Chen, Hongxia Xie, Hong-Han Shuai, Wen-Huang Cheng

<details>
<summary> 日本語要旨 </summary>

生成モデリングの進歩により、個人を現実的に描写することが容易になり、セキュリティ、コミュニケーション、公共信頼に対して深刻なリスクが生じています。このような人物駆動の操作を検出するためには、変更されたコンテンツと本物のメディアを区別し、明確で信頼性のある理由付けが可能なシステムが必要です。この論文では、解釈可能なDeepFake検出用の包括的ベンチマークである\benchnameを紹介します。\benchnameには、高品質の偽造物が含まれており、これらは先進的な合成モデルから生成されたもので、画像、動画、音声といった16種類のDeepFakeタイプをカバーしています。このベンチマークでは、三つの重要な側面を評価します：Perceptionは、人間によって注釈された証拠を用いて細部までの操作アーティファクトを識別するモデルの能力を測定します；Detectionは、多様な偽造家族とジェネレーターにわたる分類パフォーマンスを評価します；Hallucinationは、モデル生成された説明の信頼性を定量化します。最先端のマルチモーダル大規模言語モデルに対する実験では、正確なPerceptionが信頼できるDetectionには不可欠であることが示されましたが、Hallucinationが意思決定を深刻に乱す可能性があり、これら三つの側面の相互依存関係を明らかにしています。\benchnameは、検出精度、証拠識別、説明信頼性の相互作用を理解するための統一されたフレームワークを提供し、現実世界の合成メディア脅威に対処する信頼できるシステム構築の基盤を提供します。
</details>

<details>
<summary> 英語要旨 </summary>

Advances in generative modeling have made it increasingly easy to fabricate realistic portrayals of individuals, creating serious risks for security, communication, and public trust. Detecting such person-driven manipulations requires systems that not only distinguish altered content from authentic media but also provide clear and reliable reasoning. In this paper, we introduce \benchname, a comprehensive benchmark for interpretable DeepFake detection. \benchname\ contains high-quality forgeries from advanced synthesis models, covering 16 DeepFake types across image, video, and audio modalities. The benchmark evaluates three key aspects: Perception, which measures the ability of a model to identify fine-grained manipulation artifacts using human-annotated evidence; Detection, which assesses classification performance across diverse forgery families and generators; and Hallucination, which quantifies the reliability of model-generated explanations. Experiments on state-of-the-art multimodal large language models show that accurate perception is essential for reliable detection, but hallucination can severely disrupt decision-making, revealing the interdependence of these three aspects. \benchname\ provides a unified framework for understanding the interaction between detection accuracy, evidence identification, and explanation reliability, offering a foundation for building trustworthy systems that address real-world synthetic media threats.
</details>

---

### Few-shot Acoustic Synthesis with Multimodal Flow Matching
著者: Amandine Brunetto

<details>
<summary> 日本語要旨 </summary>

没入型仮想環境において、シーンと音響的に一致するオーディオを生成することは不可欠です。最近のニューラルアコースティックフィールド手法は空間的に連続したサウンドレンダリングを可能にしますが、シーン固有であり、各環境ごとに密なオーディオ測定と高コストのトレーニングが必要です。フェイズホットアプローチは部屋間のスケーラビリティを向上させますが、複数の録音に依存し、決定論的であるため、希薄なコンテキスト下でのシーンアコースティクスの固有の不確実性を捉えられません。私たちは、FLow-matching ACoustic generation（FLAC）という名前のプロビジョナルメソッドを導入します。これは、最小限のシーンコンテキストが与えられた場合に妥当な部屋インパルス応答（RIR）の分布をモデリングするものです。FLACは、フローマッチング目的でトレーニングされた拡散変換器を活用し、空間的、幾何学的、および音響的な手がかりに基づいて新規シーン内の任意の位置でRIRを生成します。FLACは、AcousticRoomsとHearing Anything Anywhereデータセットの両方で1回のフェイズホットで8回のフェイズホット基準に対して優れた性能を発揮します。標準的な知覚メトリクスを補完するため、さらにAGREE（Acoustic–GeometRy EmbEdding）というジョイント評価手法を導入し、生成されたRIRの幾何学的一貫性を検索および分布メトリクスを通じて評価します。この研究は、音響に対するジェネラティブフローマッチングの適用が初めてであり、堅牢かつデータ効率的な音響合成の新たな方向性を確立します。
</details>

<details>
<summary> 英語要旨 </summary>

Generating audio that is acoustically consistent with a scene is essential for immersive virtual environments. Recent neural acoustic field methods enable spatially continuous sound rendering but remain scene-specific, requiring dense audio measurements and costly training for each environment. Few-shot approaches improve scalability across rooms but still rely on multiple recordings and, being deterministic, fail to capture the inherent uncertainty of scene acoustics under sparse context. We introduce FLow-matching ACoustic generation (FLAC), a probabilistic method for few-shot acoustic synthesis that models the distribution of plausible room impulse responses (RIRs) given minimal scene context. FLAC leverages a diffusion transformer trained with a flow-matching objective to generate RIRs at arbitrary positions in novel scenes, conditioned on spatial, geometric, and acoustic cues. FLAC outperforms state-of-the-art eight-shot baselines with one-shot on both the AcousticRooms and Hearing Anything Anywhere datasets. To complement standard perceptual metrics, we further introduce AGREE, a joint Acoustic–GeometRy EmbEdding, enabling geometry-consistent evaluation of generated RIRs through retrieval and distributional metrics. This work is the first to apply generative flow matching to acoustics, establishing a new direction for robust and data-efficient acoustic synthesis.
</details>

---

### TokenTrace: Multi-Concept Attribution Through Watermarked Token Recovery
著者: Li Zhang, Shruti Agarwal, John Collomosse, Pengtao Xie, Vishal Asnani

<details>
<summary> 日本語要旨 </summary>

生成的AIモデルは、独自の芸術スタイルや概念を帰属なしに複製できるため、知的財産（IP）に対して大きな課題をもたらします。ウォーターマークは潜在的な解決策として提案されていますが、既存の方法は複数の概念（例えば、オブジェクトと芸術スタイル）を単一の画像内で組み合わせた複雑なシナリオではしばしば失敗します。これらの方法は個別に概念を分離し帰属することが困難です。本研究では、堅牢で複数概念の帰属を可能にする新たなプロアクティブウォーターマークフレームワーク「TokenTrace」を提案します。私たちの方法は、テキストプロンプト埋め込みと初期ラテントノイズ（両方が拡散モデルの生成過程を導く）に同時に微小な変動を加えることで、セマンティックドメイン内に秘密の署名を埋め込みます。検索用には、指定された概念（例えば特定のオブジェクトやスタイル）を取得する必要があるテキストクエリと生成画像を入力として受け取るTokenTraceモジュールを提案します。このクエリベースのメカニズムにより、単一の生成画像から複数の概念を分離し独立して存在を確認することが可能です。広範な実験では、私たちの方法がオブジェクトおよびスタイル（単一概念）や複数概念の帰属タスクにおいて最先端の性能を達成し、既存のベースラインを大幅に上回ることが示されました。また、高品質な視覚的出力と一般的な変換への堅牢性も維持しています。
</details>

<details>
<summary> 英語要旨 </summary>

Generative AI models pose a significant challenge to intellectual property (IP), as they can replicate unique artistic styles and concepts without attribution. While watermarking offers a potential solution, existing methods often fail in complex scenarios where multiple concepts (e.g., an object and an artistic style) are composed within a single image. These methods struggle to disentangle and attribute each concept individually. In this work, we introduce TokenTrace, a novel proactive watermarking framework for robust, multi-concept attribution. Our method embeds secret signatures into the semantic domain by simultaneously perturbing the text prompt embedding and the initial latent noise that guide the diffusion model's generation process. For retrieval, we propose a query-based TokenTrace module that takes the generated image and a textual query specifying which concepts need to be retrieved (e.g., a specific object or style) as inputs. This query-based mechanism allows the module to disentangle and independently verify the presence of multiple concepts from a single generated image. Extensive experiments show that our method achieves state-of-the-art performance on both single-concept (object and style) and multi-concept attribution tasks, significantly outperforming existing baselines while maintaining high visual quality and robustness to common transformations.
</details>

---

### Efficient Video Object Segmentation and Tracking with Recurrent Dynamic Submodel
著者: Weidong Tang, Zhiyuan Liang, Xinyan Wan, Chen Zhu, Zhaopan Xu, Pengfei Zhou, Yan Song, Yang You, Wangbo Zhao

<details>
<summary> 日本語要旨 </summary>

大規模ビジョンファウンデーションモデルであるSAM2は、動画オブジェクトセグメンテーションおよび追跡（VOST）において顕著な性能を達成しています。しかし、その効果は大きな計算負荷によって制限されています。この問題に対処するための一般的な戦略としてモデルプルーニングがありますが、従来の静的で入力非依存型のプルーニングアプローチは、動画データの多様性や複雑さを効果的に管理することに限界があります。有望な代替手段として動的ネットワークが挙げられますが、これらはしばしば理論上の計算削減を実際の加速に翻訳することに苦労します。また、静的および動的アプローチの両方が通常、個々のフレームの視覚特徴に焦点を当てる一方で、それらの間の時間的相関を無視することが多く、複雑な動画ストリームを処理する際の性能が制限されます。これらの課題に対応するために、私たちはフレームごとにサブモデルブロックを適応的に選択する動的アーキテクチャであるRecurrent Dynamic Submodel（RDS）を提案します。具体的には、軽量なPrediction-aware Router（PAR）があり、これは前フレームのセグメンテーションマスクと現在フレームの視覚特徴を利用してルーティング決定を行い、サブモデルが動画データの時間的性質を明示的に捉えることを可能にします。さらに、動的サブモデルの適応コストを削減するために、最も重要なブロックでパラメータのみを調整するImportance-aware LoRA（I-LoRA）を導入します。様々なベンチマークで行った広範囲な実験により、私たちのアプローチの有効性が示されています。例えば、DAVIS 2017データセットでは1.3倍の速度向上を達成し、パフォーマンス低下はわずかに1%未満でありながら、追加するトレーニング可能なパラメータはたった3%（6.7M）で、SAM2のトレーニングデータの0.003%（6.7k）だけを必要とします。
</details>

<details>
<summary> 英語要旨 </summary>

The large vision foundation model, SAM2, has achieved remarkable performance in video object segmentation and tracking (VOST). However, its effectiveness is hindered by significant computational overhead. While model pruning is a widely used strategy to address this issue, traditional static and input-agnostic pruning approaches fall short in managing the diverse and complex nature of video data effectively. A promising alternative is dynamic networks, yet they often struggle to translate theoretical computational reductions into actual acceleration. Furthermore, both static and dynamic approaches typically focus on visual features of individual frames while neglecting the temporal correlations between them, limiting their performance in handling complex video streams. To address these challenges, we propose Recurrent Dynamic Submodel (RDS), a dynamic architecture that adaptively selects submodel blocks for each frame. Specifically, it has a lightweight Prediction-aware Router (PAR), which leverages both the segmentation mask from the previous frame and the visual features of the current frame to make routing decisions, enabling the submodel to explicitly capture the temporal nature of video data. Additionally, to reduce the cost of adapting the dynamic submodel, we introduce an Importance-aware LoRA (I-LoRA), tuning parameters only in the most critical blocks. Extensive experiments on various benchmarks demonstrate the effectiveness of our approach. For example, it achieves a 1.3× speedup on the DAVIS 2017 dataset with less than 1% performance degradation, while introducing only 3% (6.7M) trainable parameters and requiring only 0.003% (6.7k) of the SAM2 training data.
</details>

---

### GenMatter: Perceiving Physical Objects with Generative Matter Models
著者: Eric Li, Arijit Dasgupta, Yoni Friedman, Mathieu Huot, Vikash Mansinghka, Thomas O&#x27;Connell, William Freeman, Joshua B. Tenenbaum

<details>
<summary> 日本語要旨 </summary>

人間の視覚知覚は、動きに基づくシーン解釈の計算原理を理解するための貴重な洞察を提供します。人間は、散らばった移動点、テクスチャ付き表面、または自然的なシーンにおいても、独立して動かせる物質の塊である動くエンティティを頑健に検出しセグメント化します。一方、既存のコンピュータビジョンシステムは、これら多様な設定にわたって統一されたアプローチが欠けています。人間の知覚の原理に触発され、私たちは低レベルの動きと外見特徴を階層的に粒子（局所物質を表す小さなガウス）にグループ化し、それらの粒子を一貫して独立して動く物理エンティティを捉えるクラスターにグループ化する生成モデルを提案します。安定した粒子の動きとグループ化を回復するために、並列化されたブロックGibbsサンプリングに基づくハードウェア加速推論アルゴリズムを開発しました。このモデルは異なる種類の入力（ランダムドット、スタイライズされたテクスチャ、または自然的なRGB動画）に対応することができ、生物学的視覚が成功しているが既存のコンピュータビジョンアプローチでは失敗している設定全体で機能します。この統一フレームワークを3つの領域にわたって検証しました：2Dランダムドットキネマトグラムでは、私たちのアプローチは曖昧な条件下での人間のオブジェクト知覚を捉えると同時に不確実性も段階的に表現します；ゲシュタルトに触発されたカモフラージュされた回転オブジェクトのデータセットでは、私たちのアプローチは運動から正しい3D構造を復元し、それによって正確な2Dオブジェクトセグメンテーションを可能にします；自然的なRGB動画では、私たちのモデルは変形するオブジェクトを構成する移動3D物質を追跡し、堅牢なオブジェクトレベルのシーン理解を可能にします。この研究は、人間視覚の原理に基づいた動きに基づく知覚の一般的なフレームワークを確立しました。
</details>

<details>
<summary> 英語要旨 </summary>

Human visual perception offers valuable insights for understanding computational principles of motion-based scene interpretation. Humans robustly detect and segment moving entities that constitute independently moveable chunks of matter, whether observing sparse moving dots, textured surfaces, or naturalistic scenes. In contrast, existing computer vision systems lack a unified approach that works across these diverse settings. Inspired by principles of human perception, we propose a generative model that hierarchically groups low-level motion and appearance features into particles (small Gaussians representing local matter), and groups particles into clusters capturing coherently and independently moveable physical entities. We develop a hardware-accelerated inference algorithm based on parallelized block Gibbs sampling to recover stable particle motion and groupings. Our model operates on different kinds of inputs (random dots, stylized textures, or naturalistic RGB video), enabling it to work across settings where biological vision succeeds but existing computer vision approaches do not. We validate this unified framework across three domains: on 2D random dot kinematograms, our approach captures human object perception including graded uncertainty across ambiguous conditions; on a Gestalt-inspired dataset of camouflaged rotating objects, our approach recovers correct 3D structure from motion and thereby accurate 2D object segmentation; and on naturalistic RGB videos, our model tracks the moving 3D matter that makes up deforming objects, enabling robust object-level scene understanding. This work thus establishes a general framework for motion-based perception grounded in principles of human vision.
</details>

---

### MV-Fashion: Towards Enabling Virtual Try-On and Size Estimation with Multi-View Paired Data
著者: Hunor Laczko, Libang Jia, Phat Truong, Diego Hernández, Sergio Escalera, Jordi Gonzàlez, Meysam Madadi

<details>
<summary> 日本語要旨 </summary>

既存の4D人間データセットは、リアルな衣服動態やタスク特化型注釈が不足しており、ファッション研究には適していません。合成データセットは現実味の欠如に苦しみ、一方でリアルワールドキャプチャーは仮想試着（VTON）やサイズ推定タスクに必要な詳細な注釈とペアデータを欠いています。このギャップを埋めるため、私たちはドメイン特化型ファッション分析のために設計された大規模マルチビュー動画データセットであるMV-Fashionを導入します。MV-Fashionは、80人の多様な被験者がそれぞれ3〜10着の衣服を身につけた3,273シーケンス（約72.5百万フレーム）から成り立っています。このデータセットは、複数層や様々なスタイリング（例えば、タックインしたシャツやロールアップした袖）を含む複雑で現実的な衣服動態のキャプチャーに特化しています。重要な貢献は、ピクセルレベルのセマンティック注釈や弾性などの真正な材料特性、3Dポイントクラウドを含む豊富なデータ表現です。VTONアプリケーションにとって重要なことに、MV-Fashionはペアデータを提供しています：着用された衣服のマルチビュー同期キャプチャーとその対応する平らなカタログ画像。このデータセットを活用し、仮想試着、衣類サイズ推定、新視点合成などのファッション中心のタスクに対するベースラインを確立します。
</details>

<details>
<summary> 英語要旨 </summary>

Existing 4D human datasets fall short for fashion-specific research, lacking either realistic garment dynamics or task-specific annotations. Synthetic datasets suffer from a realism gap, whereas real-world captures lack the detailed annotations and paired data required for virtual try-on (VTON) and size estimation tasks. To bridge this gap, we introduce MV-Fashion, a large-scale, multi-view video dataset engineered for domain-specific fashion analysis. MV-Fashion features 3,273 sequences (72.5 million frames) from 80 diverse subjects wearing 3-10 outfits each. It is designed to capture complex, real-world garment dynamics, including multiple layers and varied styling (e.g., tucked shirts, rolled sleeves). A core contribution is a rich data representation that includes pixel-level semantic annotations, ground-truth material properties like elasticity, and 3D point clouds. Crucially for VTON applications, MV-Fashion provides paired data: multi-view synchronized captures of worn garments alongside their corresponding flat, catalogue images. We leverage this dataset to establish baselines for fashion-centric tasks, including virtual try-on, clothing size estimation, and novel view synthesis.
</details>

---

### LuxRemix: Lighting Decomposition and Remixing for Indoor Scenes
著者: Ruofan Liang, Norman Müller, Ethan Weber, Duncan Zauss, Nandita Vijaykumar, Peter Kontschieder, Christian Richardt

<details>
<summary> 日本語要旨 </summary>

私たちは、単一のマルチビュー・シーンキャプチャから室内シーンにおけるインタラクティブな照明編集のための新しいアプローチを提案します。私たちの方法は、複雑な室内シーンの照明を構成する光源に分解する生成画像ベースの光分解モデルを利用しています。この分解により、個々の光源を独立して操作できるようになり、具体的にはその状態（オン/オフ）、色相、および強度を制御することが可能です。さらに、すべてのシーンビュー間で一貫した光分解の伝播を保証するためにマルチビュー照明調和法を導入しています。これはリライト可能な3Dガウススプラッティング表現に統合され、個々の光源に対するリアルタイムインタラクティブ制御が提供されます。私たちの結果は、多様な室内シーンでの高度に写実的な照明分解とリライト結果を示しています。この方法を合成および現実世界のデータセットで評価し、最先端技術との定量的および定性的比較を提供します。
</details>

<details>
<summary> 英語要旨 </summary>

We present a novel approach for interactive light editing in indoor scenes from a single multi-view scene capture. Our method leverages a generative image-based light decomposition model that factorizes complex indoor scene illumination into its constituent light sources. This factorization enables independent manipulation of individual light sources, specifically allowing control over their state (on/off), chromaticity, and intensity. We further introduce multi-view lighting harmonization to ensure consistent propagation of the lighting decomposition across all scene views. This is integrated into a relightable 3D Gaussian splatting representation, providing real-time interactive control over the individual light sources. Our results demonstrate highly photorealistic lighting decomposition and relighting outcomes across diverse indoor scenes. We evaluate our method on both synthetic and real-world datasets and provide a quantitative and qualitative comparison to state-of-the-art techniques.
</details>

---

### Reviving ConvNeXt for Efficient Convolutional Diffusion Models
著者: Taesung Kwon, Lorenzo Bianchi, Lennart Wittke, Felix Watine, Fabio Carrara, Jong Chul Ye, Romann M. Weber, Vinicius C. Azevedo

<details>
<summary> 日本語要旨 </summary>

最近の拡散モデルは、完全に注意機構を持つアーキテクチャの驚異的なスケーラビリティにより、トランスフォーマー背骨がますます好まれるようになっています。しかし、ローカルバイアス、パラメータ効率性、ハードウェアフレンドリーさといった特徴は、コンボニューラルネットが効率的なビジョン背骨として確立される要因でありながら、現代の生成モデリングにおける探求が限定的です。ここでは、条件付き拡散モデリング用に再設計されたConvNeXtインスパイアの背骨を持つ完全畳み込み拡散モデル（FCDM）を紹介します。私たちは、FCDM-XLがDiT-XL/2の50%のFLOPsで同等の性能を達成し、256×256および512×512解像度においてそれぞれ7倍と7.5倍の高速化を実現することを発見しました。驚くべきことに、FCDM-XLは4-GPUシステムでトレーニング可能であり、私たちのアーキテクチャの優れたトレーニング効率を強調しています。私たちの結果は、現代の畳み込み設計が拡散モデルのスケーリングにおいて競争力のある高効率な選択肢を提供し、効率的な生成モデリングのためのシンプルでありながら強力な構成要素としてConvNeXtを復活させていることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Recent diffusion models increasingly favor Transformer backbones, motivated by the remarkable scalability of fully attentional architectures. Yet the locality bias, parameter efficiency, and hardware friendliness—the attributes that established ConvNets as the efficient vision backbone—have seen limited exploration in modern generative modeling. Here we introduce the fully convolutional diffusion model (FCDM), a ConvNeXt-inspired backbone redesigned for conditional diffusion modeling. We find that FCDM-XL, using only 50$\%$ of the FLOPs of DiT-XL/2, achieves comparable performance while delivering 7$\times$ and 7.5$\times$ speedups at 256$\times$256 and 512$\times$512 resolutions, respectively. Remarkably, FCDM-XL can be trained on a 4-GPU system, highlighting the exceptional training efficiency of our architecture. Our results demonstrate that modern convolutional designs provide a competitive and highly efficient alternative for scaling diffusion models, reviving ConvNeXt as a simple yet powerful building block for efficient generative modeling.
</details>

---

### From Manuals to Actions: A Unified VLA Model for Chain-of-Thought Manual Generation and Robotic Manipulation
著者: Chenyang Gu, Jiaming Liu, Hao Chen, Runzhong Huang, Qingpo Wuwu, Xiaoqi Li, Zhuoyang Liu, Ying Li, Renrui Zhang, Peng Jia, Pheng-Ann Heng, Shanghang Zhang

<details>
<summary> 日本語要旨 </summary>

最近、ビジョン・ランゲージ・アクション（VLA）モデルが登場し、ロボットのシーン理解と操作において強力な汎用性を示しています。しかし、定義された目標状態を必要とする長期的なタスク（例えばLEGO組み立てやオブジェクトの再配置）に直面した際、既存のVLAモデルは依然として長期計画と正確な操作を調整することに苦労しています。そのため、私たちは「何」の結果から「どうやって」プロセスを推論できるVLAモデルを開発し、目標状態を実行可能な手順に変換することを目指します。本論文では、Mixture-of-Transformers（MoT）アーキテクチャに基づく統一されたVLAフレームワークであるManualVLAを紹介します。これにより、マルチモーダルな手順生成と行動実行の間で調和した協力が可能になります。以前のVLAモデルがセンサー入力を直接アクションにマッピングするのとは異なり、ManualVLAにはまず計画専門家を搭載し、画像、視覚プロンプト、テキスト指示から成る中間的な手順書を生成します。これらのマルチモーダルな手順書に基づき、各手順が明示的な制御条件を提供し、その潜在表現が正確な操作のための暗黙のガイダンスを提供するManual Chain-of-Thought（ManualCoT）推論プロセスを設計します。データ収集の負担を軽減するため、3D Gaussian Splattingに基づく高精度なデジタルツインツールキットを開発し、計画専門家のトレーニング用の手順書データを自動生成します。ManualVLAは実世界で強力なパフォーマンスを示し、LEGO組み立てやオブジェクト再配置タスクにおいて、以前の階層的SOTAベースラインよりも平均成功率が32％高くなっています。
</details>

<details>
<summary> 英語要旨 </summary>

Vision–Language–Action (VLA) models have recently emerged, demonstrating strong generalization in robotic scene understanding and manipulation. However, when confronted with long-horizon tasks that require defined goal states, such as LEGO assembly or object rearrangement, existing VLA models still face challenges in coordinating long-horizon planning with precise manipulation. Therefore, we aim to endow a VLA model with the capability to infer the “how” process from the “what” outcomes, transforming goal states into executable procedures. In this paper, we introduce ManualVLA, a unified VLA framework built upon a Mixture-of-Transformers (MoT) architecture, enabling coherent collaboration between multimodal manual generation and action execution. Unlike prior VLA models that directly map sensory inputs to actions, we first equip ManualVLA with a planning expert that generates intermediate manuals consisting of images, visual prompts, and textual instructions. Building upon these multimodal manuals, we design a Manual Chain-of-Thought (ManualCoT) reasoning process that feeds them into the action expert, where each manual step provides explicit control conditions, while its latent representation offers implicit guidance for accurate manipulation. To alleviate the burden of data collection, we develop a high-fidelity digital-twin toolkit based on 3D Gaussian Splatting, which automatically generates manual data for planning expert training. ManualVLA demonstrates strong real-world performance, achieving an average success rate 32\% higher than the previous hierarchical SOTA baseline on LEGO assembly and object rearrangement tasks.
</details>

---

### Multi-view Consistent 3D Gaussian Head Avatars ‘without’ Multi-view Generation
著者: Aviral Chharia, Fernando De la Torre

<details>
<summary> 日本語要旨 </summary>

非常に大規模な3Dヘッドアバターを、高い忠実度と強力なマルチビューコンシステト（MVC）で生成することは、合成群衆やデジタルダブル、大規模資産ライブラリーのようなアプリケーションにおいて不可欠です。高スケーラビリティを実現するためには、コストのかかるMVスタジオキャプチャや3Dデータなしでアバターを生成する必要があります。本研究では、この資源が限られた設定での3Dヘッド生成に挑戦します。また、中間MV画像生成を通じてMVCを強制する一般的な手法は高コストかつ根本的に脆弱であると主張します。代わりに、私たちはMVCがどのように設計によって誘導され得るかを分析し、中間ビュー合成は不要であることを示しています。この目的のために、私たちは「MVCHead」という高速なシングルショット状態空間モデルを導入します。これは中間生成を行わずに直接Gaussianを予測します。その核心として、グリッド整列の一貫性を強制しつつ長距離依存関係を捉えるHierarchical State Space（HiSS）ブロックを提案します。さらに、Mambaの標準的な単方向スキャンをHierarchical Bi-directional State Scan（HiBiSS）に変更し、レンダリンググリッドをより良くスキャンして幾何学的および外観の手がかりを伝播させます。最後に、自己レンダーから単一の3D構成が生じるかどうかを判断するSE(3) MV Criticを設計し、実際のMVデータなしでクロスビューピクセルアライメントを報酬とします。この環境下では、MVCHeadが形状、テクスチャー、幾何学の3つのMVC軸においてSOTAを超える知覚品質を達成しています。コードは提出され、受理後にオープンソースとしてモデルウェイトと共に公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Generating large-scale 3D head avatars of non-existent identities with high-fidelity and strong multi-view consistency (MVC) is essential for applications such as synthetic crowds, digital twins, and large asset libraries. For high scalability, avatars must be generated from minimal resources, without costly MV studio captures or any 3D data. In this work, we target this challenging minimal-resource setting for 3D head generation. Second, we argue that the common strategy of enforcing MVC via intermediate MV image generation is both expensive and fundamentally fragile. Instead, we analyze how MVC can be induced by design, showing that intermediate view synthesis is unnecessary. To this end, we introduce MVCHead — a fast, single-shot state space model that directly predicts Gaussians, without intermediate generation. At its core, we propose a Hierarchical State Space (HiSS) block that enforces grid-aligned coherence while capturing long-range dependencies. We further modify Mamba's standard unidirectional scanning into a Hierarchical Bi-directional State Scan (HiBiSS), scanning the render grid to better propagate geometric and appearance cues. Finally, we design an SE(3) MV Critic that judges whether a set of self-renders arise from a single underlying 3D configuration, rewarding cross-view pixel alignment without real MV data. In this setting, MVCHead surpasses SOTA in perceptual quality and on all three MVC axes—shape, texture, and geometry. The code has been submitted and will be open-sourced with model weights upon acceptance.
</details>

---

### DocSeeker: Structured Visual Reasoning with Evidence Grounding for Long Document Understanding
著者: Hao Yan, Yuliang Liu, Xingchen Liu, Yuyi Zhang, Minghui Liao, Jihao Wu, Wei Chen, Xiang Bai

<details>
<summary> 日本語要旨 </summary>

既存のマルチモーダル大規模言語モデル（MLLMs）は、文書の長さが増すにつれて長文理解タスクで顕著な性能低下を経験しています。これは二つの基本的な課題から生じます：1）信号対雑音比（SNR）が低く、重要な証拠が関連しないページに埋もれていること；2）監督不足であり、最終的な短い答えのみを提供するデータセットは弱い学習信号を与えます。本論文では、これらの課題に対処するために、「分析・位置特定・推論」という構造化されたワークフローを実行させるパラダイムを提案します。この能力を培うため、二段階のトレーニングフレームワークを設計しました：まず、効率的な知識蒸留戦略によって生成された高品質データで監督付き微調整を行います。次に、証拠の位置特定と答えの正確性を同時に最適化する証拠意識グループ相対政策最適化を用います。さらに、マルチページ文書でのトレーニングにおけるメモリ制約を緩和するために証拠ガイド付き解決策割り当て戦略を導入します。広範な実験では、DocSeekerがインドメインおよびアウトオブドメインのタスクで優れた性能を達成していることを示しました。短ページのトレーニングから超長文書への堅牢な一般化能力があること、また視覚的リカバリー強化生成システムと自然に相乗効果を発揮するため、その実装の理想的な基盤であることを示しました。
</details>

<details>
<summary> 英語要旨 </summary>

Existing Multimodal Large Language Models (MLLMs) suffer from significant performance degradation on the long document understanding task as document length increases. This stems from two fundamental challenges: 1) a low Signal-to-Noise Ratio (SNR), with crucial evidence buried in irrelevant pages; and 2) supervision scarcity, as datasets offering only final short answers provide a weak learning signal. In this paper, we address these challenges by proposing a paradigm that requires the model to execute a structured ``Analysis, Localization and Reasoning'' workflow. To instill this capability, we design a two-stage training framework: we first perform Supervised Fine-Tuning on high-quality data generated via an efficient knowledge distillation strategy. Subsequently, we employ an Evidence-aware Group Relative Policy Optimization which jointly optimizes for both evidence localization and answer accuracy. Additionally, we introduce a Evidence-Guided Resolution Allocation strategy to mitigate memory constraints of training on multi-pages documents. Extensive experiments demonstrate that DocSeeker achieves superior performance on both in-domain and out-of-domain tasks. We show it robustly generalizes from short-page training to ultra-long documents and is naturally synergistic with visual Retrieval-Augmented Generation systems, serving as an ideal foundation for their implementation.
</details>

---

### PointTPA: Test-Time Parameter Adaptation for 3D Scene Understanding
著者: Siyuan Liu, Chaoqun Zheng, Xin Zhou, Tianrui Feng, Dingkang Liang, Xiang Bai

<details>
<summary> 日本語要旨 </summary>

ポイントクラウドシーン理解は、多様な幾何学的形状、不均衡なカテゴリ、および高度に変動する空間レイアウトのために依然として課題が残っています。既存の手法はオブジェクトレベルの性能を向上させますが、推論時に静的なパラメータに依存し、動的シーンデータへの適応性が制限されています。私たちは、ポイントクラウドシーン認識のためのテストタイムパラメータ適応（PointTPA）を提案します。これは、入力に対応したパラメータを構築するテストタイム動的適応フレームワークであり、シーンレベルのポイントクラウドに対して使用されます。PointTPAは、Serialization-based Neighborhood Grouping（SNG）を用いて局所的に一貫したパッチを形成し、Dynamic Parameter Projector（DPP）を用いてパッチごとの適応重みを生成します。これにより、バックボーンはシーン固有の変動に応じてその挙動を調整できる一方で、パラメータコストを低く保つことが可能です。PTv3に統合されたPointTPAは、トレーニング可能なパラメータ数を95%以上削減し、フルファインチューニングと競争力のあるまたは優れた性能を達成します。S3DISで74.9%のmIoUを達成し、複数のベンチマークにわたって既存のPEFTベースラインを一貫して上回ります。これは、テストタイム動的パラメータ生成が3Dシーン理解の強化において有効であることを示しています。コードは近日公開予定です。
</details>

<details>
<summary> 英語要旨 </summary>

Scene-level point cloud understanding remains challenging due to diverse geometries, imbalanced categories, and highly varied spatial layouts. Existing methods improve object-level performance but rely on static parameters during inference, limiting their adaptability to dynamic scene data. We propose Test-time Parameter Adaptation for Point Cloud Scene Perception (PointTPA), a test-time dynamic adaptation framework that constructs input-aware parameters for scene-level point clouds. PointTPA uses a Serialization-based Neighborhood Grouping (SNG) to form locally coherent patches and a Dynamic Parameter Projector (DPP) to produce patch-wise adaptive weights, enabling the backbone to adjust its behavior according to scene-specific variations while keeping parameter cost low. Integrated into PTv3, PointTPA reduces trainable parameters by over 95% and achieves competitive or superior performance to full fine-tuning. It achieves 74.9% mIoU on S3DIS and consistently surpasses existing PEFT baselines across multiple benchmarks, highlighting the efficacy of test-time dynamic parameter generation in enhancing robust 3D scene understanding. The code will be available soon.
</details>

---

### DyaDiT: A Multi-Modal Diffusion Transformer for Socially-Aware Dyadic Gesture Generation
著者: YICHEN PENG, Jyun-Ting Song, Siyeol Jung, RUOFAN LIU, Haiyang Liu, Xuangeng Chu, Ruicong Liu, Erwin Wu, Hideki Koike, Kris Kitani

<details>
<summary> 日本語要旨 </summary>

デジタルヒューマンとの自然で社会的に魅力的なインタラクションを実現するためには、リアルな対話用ジェスチャーの生成が不可欠です。しかし、既存の方法では通常、単一の音声ストリームを単一の発言者の動きにマッピングし、社会的文脈や2人が対話する際の相互ダイナミクスを考慮していません。私たちは、DyaDiTという多モーダル拡散トランスフォーマーを提案します。これは、二人称音声信号から文脈に適した人間の動きを生成するものです。Seamless Interaction Datasetで訓練されたDyaDiTは、オプションの社会的コンテキストトークン付きの二人称音声を入力として受け取り、文脈に適した動きを生成します。両者から情報を統合し対話ダイナミクスを捉え、動作辞書を用いて動作の事前知識をエンコードし、会話相手のジェスチャーをオプションで利用してより反応性の高い動きを生成することが可能です。DyaDiTは標準的な動作生成メトリクスに基づく評価や定量的ユーザー調査を行い、既存手法を客観的指標で上回るだけでなく、ユーザーからも強く好まれており、その堅牢性と社会的に優れた動作生成能力が示されました。コードとモデルは受理後に公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Generating realistic conversational gestures are essential for achieving natural, socially engaging interactions with digital humans. However, existing methods typically map a single audio stream to a single speaker’s motion, without considering social context or modeling the mutual dynamics between two people engaging in conversation. We present DyaDiT, a multi-modal diffusion transformer that generates contextually appropriate human motion from dyadic audio signals. Trained on Seamless Interaction Dataset, DyaDiT takes dyadic audio with optional social-context tokens to produce context-appropriate motion. It fuses information from both speakers to capture interaction dynamics, uses a motion dictionary to encode motion priors, and can optionally utilize the conversational partner's gestures to produce more responsive motion. We evaluate DyaDiT on standard motion generation metrics and conduct quantitative user studies, demonstrating that it not only surpasses existing methods on objective metrics but is also strongly preferred by users, highlighting its robustness and socially favorable motion generation. Code and models will be released upon acceptance.
</details>

---

### BAMI: Training-Free Bias Mitigation in GUI Grounding
著者: Borui Zhang, Bo Zhang, Bo Wang, Wenzhao Zheng, Yuhao Cheng, Liang Tang, Yiqiang Yan, Jie Zhou, Jiwen Lu

<details>
<summary> 日本語要旨 </summary>

GUI エージェントがクリックやドラッグなどのタスクを実行するためには、GUI グランディングが重要です。しかし、ScreenSpot-Pro ベンチマークのような複雑なシナリオでは、既存モデルがしばしば最適でないパフォーマンスを示します。提案された **Masked Prediction Distribution (MPD)** 帰属法を使用することで、エラーの主要な原因は二つあります：高解像度画像（精度バイアスを引き起こす）と複雑なインターフェース要素（曖昧さバイアスをもたらす）。これらの課題に対処するため、**Bias-Aware Manipulation Inference (BAMI)** を導入します。これは、粗い焦点から細かい焦点への移行と候補選択を含む二つの重要な操作によって、これらのバイアスを効果的に軽減します。広範囲の実験結果は、BAMI がトレーニングフリー環境でさまざまな GUI グランディングモデルの精度を大幅に向上させることを示しています。例えば、TianXi-Action-7B モデルに私たちの方法を適用すると、ScreenSpot-Pro ベンチマークでの正確性が 51.9% から 57.8% に向上します。さらに、アブレーション研究は、BAMI アプローチの多様なパラメータ設定における堅牢性を確認し、その安定性と効果を強調しています。
</details>

<details>
<summary> 英語要旨 </summary>

GUI grounding is a critical capability for enabling GUI agents to execute tasks such as clicking and dragging. However, in complex scenarios like the ScreenSpot-Pro benchmark, existing models often suffer from suboptimal performance. Utilizing the proposed \textbf{Masked Prediction Distribution (MPD)} attribution method, we identify that the primary sources of errors are twofold: high image resolution (leading to precision bias) and intricate interface elements (resulting in ambiguity bias). To address these challenges, we introduce \textbf{Bias-Aware Manipulation Inference (BAMI)}, which incorporates two key manipulations, coarse-to-fine focus and candidate selection, to effectively mitigate these biases. Our extensive experimental results demonstrate that BAMI significantly enhances the accuracy of various GUI grounding models in a training-free setting. For instance, applying our method to the TianXi-Action-7B model boosts its accuracy on the ScreenSpot-Pro benchmark from 51.9\% to 57.8\%. Furthermore, ablation studies confirm the robustness of the BAMI approach across diverse parameter configurations, highlighting its stability and effectiveness.
</details>

---

### Neighbor-Aware Localized Concept Erasure in Text-to-Image Diffusion Models
著者: Zhuan Shi, Alireza Dehghanpour Farashah, Rik de Vries, Golnoosh Farnadi

<details>
<summary> 日本語要旨 </summary>

テキストから画像への拡散モデルにおける概念消去は、望ましくない概念を取り除きつつ全体的な生成能力を維持することを目指しています。局所化された消去方法は、ターゲット概念が占める空間領域における編集を制限しようとします。しかし、私たちは概念の抑制が意図せずにセマンティックに関連する隣接概念を弱め、微細な領域での忠実度を低下させることを観察しています。私たちは、ターゲット概念を除去しつつ近傍概念をより良く保持するトレーニングフリーの枠組みであるNeighbor-Aware Localized Concept Erasure（NLCE）を提案します。これは三段階で動作します：(1) ターゲット概念方向を減衰させつつ近傍概念表現を安定化するスペクトラル重み付き埋め込み変調、(2) 残留概念活性化領域を特定する注意ガイドによる空間ゲート、および(3) 必要な場所のみで残存痕跡を排除する空間的にゲートされたハード消去です。この近傍認識パイプラインは、周囲の概念隣接構造を維持しつつ局所化された概念除去を可能にします。オックスフォードフラワーズやスタンフォードドッグズなどの微細領域データセットでの実験では、私たちの方法がターゲット概念を効果的に除去しつつ密接に関連するカテゴリーをより良く保持していることが示されました。さらに、セレブリティアイデンティティ、露骨な内容、芸術スタイルの結果は、広範な消去シナリオへの堅牢性と一般化を示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Concept erasure in text-to-image diffusion models seeks to remove undesired concepts while preserving overall generative capability. Localized erasure methods aim to restrict edits to the spatial region occupied by the target concept. However, we observe that suppressing a concept can unintentionally weaken semantically related neighbor concepts, reducing fidelity in fine-grained domains. We propose Neighbor-Aware Localized Concept Erasure (NLCE), a training-free framework designed to better preserve neighboring concepts while removing target concepts. It operates in three stages: (1) a spectrally-weighted embedding modulation that attenuates target concept directions while stabilizing neighbor concept representations, (2) an attention-guided spatial gate that identifies regions exhibiting residual concept activation, and (3) a spatially-gated hard erasure that eliminates remaining traces only where necessary. This neighbor-aware pipeline enables localized concept removal while maintaining the surrounding concept neighborhood structure. Experiments on fine-grained datasets (Oxford Flowers, Stanford Dogs) show that our method effectively removes target concepts while better preserving closely related categories. Additional results on celebrity identity, explicit content and artistic style demonstrate robustness and generalization to broader erasure scenarios.
</details>

---

### AXG-Reasoner: Error Detection and Explanation in Long Task Videos with Vision–Language Models
著者: Shih-Po Lee, Ehsan Elhamifar

<details>
<summary> 日本語要旨 </summary>

仮想タスクアシスタントは、効果的で修正指導を提供するためにユーザーの誤りを認識し、説明する必要があります。本論文では、長いタスク動画におけるエラーリーズニングの問題に取り組みます。これは、エラーの検出と説明を行うことです。最近のビジョン・ランゲージモデル（VLM）は視覚的な質問応答で強力な能力を示していますが、長いタスク動画におけるエラーと関連する希薄な時空間的手掛かりに注目することは難しいです。私たちは、凍結したVLMを活用しつつ、提案されたアクション実行グラフ（AXG）およびタイムスケールの動作セグメンテーション（TAS）モデルと組み合わせるエラーリーズニングフレームワーク、AXG-Reasonerを導入します。これらは正常な（誤りのない）動画から得られ、学習されます。VLMがエラーに関連する希薄な時空間的手掛かりに注目できるようにするために、TASによって得られた各アクションセグメントをAXGと整列させて細分化されたサブアクションのシーケンスに分解します。それぞれのサブアクションセグメントについて、キーフレームの少数と強化されたプロンプトを用いてVLMを問い合わせることでエラーを検出し説明します。これにより効率的な推論が可能になります。コストのかかる手動サブアクション注釈を避けるため、私たちはトレーニングビデオからAXGを自動構築する方法を開発しました。これはファウンデーションモデルを使用して行います。EgoPERおよびCaptainCook4Dにおける広範な実験では、私たちの手法がVLMベースラインを一貫して上回り、効果的に時空間的手掛かりを特定することでエラー説明が改善され、エラーディテクションにおいて最先端の性能を達成しました。
</details>

<details>
<summary> 英語要旨 </summary>

Virtual task assistants must recognize and explain users’ mistakes to provide effective and corrective guidance. In this paper, we address the problem of error reasoning in long task videos, which is to detect and explain errors. Although recent Vision–Language Models (VLMs) demonstrate strong capabilities in visual question answering, they struggle to attend to the sparse spatiotemporal cues associated with errors in long task videos. We introduce an error reasoning framework, AXG-Reasoner, that leverages a frozen VLM in conjunction with a proposed Action eXecution Graph (AXG) and a temporal action segmentation (TAS) model, obtained and learned from normal (error-free) videos. To enable VLMs to attend to the sparse spatiotemporal cues associated with errors, we decompose each action segment of the video, obtained by TAS, into a sequence of fine-grained subactions by aligning it with the AXG. For each subaction segment, we query the VLM using a small number of keyframes and enhanced prompts to detect and explain errors, enabling efficient inference. To avoid costly manual subaction annotations, we develop a method to automatically construct AXG from training videos using foundation models. Extensive experiments on EgoPER and CaptainCook4D show that our method consistently improves over VLM baselines in error explanation by effectively identifying spationtemporal cues and achieves state-of-the-art performance in error detection.
</details>

---

### Cross-Domain Few-Shot Segmentation Via Multi-view Progressive Adaptation
著者: Jiahao Nie, Guanqiao Fu, Wenbin An, Yap-Peng Tan, Alex C. Kot, Shijian Lu

<details>
<summary> 日本語要旨 </summary>

クロスドメインフィーショットセグメンテーションは、データが乏しい領域におけるカテゴリのセグメンテーションを少数の事例に基づいて行うことを目指します。典型的な手法ではまず大規模なソースドメインでフィーショット能力を確立し、その後ターゲットドメインに適応させます。しかし、ターゲットサンプルの量と多様性が限られているため、既存手法は依然として制約されたパフォーマンスを示します。また、ソースドメインで訓練されたモデルのターゲットドメインにおける初期的なフィーショット能力が弱く、大きなドメイン間のギャップが存在することで、ターゲットサンプルの効果的な利用を妨げ、さらに適応を阻害します。このため、我々はデータおよび戦略の両方の視点からターゲットドメインへフィーショット能力を逐次的に適応させるマルチビュー・プログレッシブ・アダプテーション（MPA）を提案します。 (i) データの視点からは、ハイブリッド・プログレッシブ・アグメンテーションを導入し、積み重ねた強力な拡張によってますます多様で複雑なビューを生成することで、学習シナリオを徐々に困難化します。 (ii) 戦略の視点からは、これら逐次的に複雑化したビューを広範な監督下で順次および並列学習パスを通じて完全に活用するデュアルチェイン・マルチビュー・プレディクションを設計します。多様かつ複雑なビュー間で予測の一貫性を強制することにより、MPAはターゲットドメインへの堅牢で正確な適応を実現します。広範な実験によって、MPAがフィーショット能力を効果的にターゲットドメインに適応させることが示され、最先端手法を大きく上回ります（+7.0%）。
</details>

<details>
<summary> 英語要旨 </summary>

Cross-Domain Few-Shot Segmentation aims to segment categories in data-scarce domains conditioned on a few exemplars. Typical methods first establish few-shot capability in a large-scale source domain and then adapt it to target domains. However, due to the limited quantity and diversity of target samples, existing methods still exhibit constrained performance. Moreover, the source-trained model's initially weak few-shot capability in target domains, coupled with substantial domain gaps, severely hinders the effective utilization of target samples and further impedes adaptation. To this end, we propose Multi-view Progressive Adaptation, which progressively adapts few-shot capability to target domains from both data and strategy perspectives. (i) From the data perspective, we introduce Hybrid Progressive Augmentation, which progressively generates more diverse and complex views through cumulative strong augmentations, thereby creating increasingly challenging learning scenarios. (ii) From the strategy perspective, we design Dual-chain Multi-view Prediction, which fully leverages these progressively complex views through sequential and parallel learning paths under extensive supervision. By jointly enforcing prediction consistency across diverse and complex views, MPA achieves both robust and accurate adaptation to target domains. Extensive experiments demonstrate that MPA effectively adapts few-shot capability to target domains, outperforming state-of-the-art methods by a large margin (+7.0\%).
</details>

---

### AnyID: Ultra-Fidelity Universal Identity-Preserving Video Generation from Any Visual References
著者: Jiahao Wang, Hualian Sheng, Sijia Cai, Yuxiao Yang, Weizhan Zhang, Caixia Yan, Bing Deng, Jieping Ye

<details>
<summary> 日本語要旨 </summary>

アイデンティティを保持したビデオ生成は、ユーザーが愛するキャラクターを特徴とするビデオをカスタマイズできる強力な創造的表現手段を提供します。しかし、既存の方法は通常、単一のアイデンティティ参照に設計および最適化されています。この基本的な仮定は二つの重要な制限を導入します：多様で現実的な入力形式をうまく受け入れられず、創造的な柔軟性が制約されること、そしてより深刻にはアイデンティティの忠実度が損なわれます。単一のソースに依存する設定は不適切であり、本質的に曖昧な基盤を提供し、モデルが新たなコンテキストでアイデンティティを忠実に再現することを困難にします。これに対応して、私たちはAnyIDという超高精度のアイデンティティ保持ビデオ生成フレームワークを提案します。私たちのアプローチは二つの主要な貢献を行います。まず、異種のアイデンティティ入力（例えば顔、肖像画、ビデオ）を統一的な表現に効果的に統合するスケーラブルなオムニ参照アーキテクチャを導入します。次に、主要参照生成パラダイムを提案し、これは一つの参照を標準的なアンカーとして指定し、新規の差分プロンプトを用いて精密な属性レベルでの制御可能性を実現します。モデルは大規模かつ慎重に編集されたデータセットで訓練され、堅牢性と高い忠実度が確保されます。さらに、強化学習を用いた最終的な微調整ステージを行います。このプロセスは人間の評価から構築された好みデータセットを利用し、アノテーターがアイデンティティ忠実度とプロンプト制御可能性に基づいてビデオのペア比較を行います。広範な評価はAnyIDが異なるタスク設定で超高精度のアイデンティティ忠実度と優れた属性レベルの制御可能性を達成することを検証します。すべてのコード、データ、モデルは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Identity-preserving video generation offers powerful tools for creative expression, allowing users to customize videos featuring their beloved characters. However, prevailing methods are typically designed and optimized for a single identity reference. This underlying assumption introduces two significant limitations: it curtails creative flexibility by poorly accommodating diverse, real-world input formats, and more critically, it compromises identity fidelity. Relying on a single source is an ill-posed setting, and provides an inherently ambiguous foundation, making it difficult for the model to faithfully reproduce an identity across novel contexts. In response, we present AnyID, an ultra-fidelity identity-preservation video generation framework. Our approach makes two core contributions. First, we introduce a scalable omni-referenced architecture that effectively unifies heterogeneous identity inputs (e.g., faces, portraits, and videos) into a cohesive representation. Second, we propose a primary-referenced generation paradigm, which designates one reference as a canonical anchor and uses a novel differential prompt to enable precise, attribute-level controllability. The model is trained on a large-scale, meticulously curated dataset to ensure robustness and high fidelity. In addition, we perform a final fine-tuning stage using reinforcement learning. This process leverages a preference dataset constructed from human evaluations, where annotators performed pairwise comparisons of videos based on two key criteria: identity fidelity and prompt controllability. Extensive evaluations validate that AnyID achieves ultra-high identity fidelity as well as superior attribute-level controllability across different task settings. All the codes, data and models will be publicly released.
</details>

---

### ShreddingNet: Coarse-to-Fine Restoration for Multi-Source Shredded Manuscripts
著者: Haoyang Cui, Hao Jiang, Yadong Mu

<details>
<summary> 日本語要旨 </summary>

人間の文化遺産における重要な研究課題として、芸術作品や書道の修復は大きな意義を持ちます。しかし、断片が必ずしも同一の作品からであることが保証されていない多源（すなわち、複数のソース）に基づく断片指向の修復タスクを考慮した研究は少ないです。私たちは、制約条件を必要としない多源写本の修復のための粗視化から細部までの二段階パイプラインであるShreddingNetを提案します。提案された粗視化ステージでは、各断片の特徴を比較し、トップK候補を選択し、ソースごとに断片をクラスタリングします。この設計は、誤ったマッチがほとんどソースの境界を越えないという重要な洞察を活用しており、高精度なクラスタリングを可能にします。提案された細部指向のステージでは、候補を評価し、マッチングスコアを得て、誤ったマッチングペアを候補セットから除外し、より正確な最終的なマッチングペアを生成してグローバルアセンブリに使用します。2つのデータセットから4,000以上の画像で行われた実験では、平均再構成F1スコアが98.37％となり、これは現在の最先端手法よりも5.72％高く、方法の有効性と堅牢性を確認しています。補足資料にソースコードがあります。
</details>

<details>
<summary> 英語要旨 </summary>

As an important research task of human cultural heritage, the restoration of artworks and calligraphy is of great significance. Seldom existing works have taken the multi-source (*i.e.*, fragments are not ensured to be from the same piece of artworks) fragment-oriented restoration task into account. We propose ShreddingNet, a coarse-to-fine two-stage pipeline for multi-source manuscript restoration that operates without restrictive conditions. The proposed coarse stage compares the features of each fragment, selecting top-K candidates and clustering fragments by source. This design leverages the key insight that erroneous matches rarely cross source boundaries, enabling high-precision clustering. The proposed fine-grained stage evaluates candidates, yielding matching scores and filters out erroneous matching pairs from the candidate set; producing more precise final matching pairs for global assembly. Experiments conducted on more than 4,000 images from two datasets demonstrate the average reconstruction F1-score achieves 98.37\%, which is 5.72\% higher than the current state-of-the-art method, confirming the method’s effectiveness and robustness. Source code is available in the supplementary material.
</details>

---

### WonderZoom: Multi-Scale 3D World Generation
著者: Jin Cao, Hong-Xing Yu, Jiajun Wu

<details>
<summary> 日本語要旨 </summary>

私たちは、単一の画像から複数の空間スケールにわたるコンテンツを持つ3Dシーンを生成する新しいアプローチであるWonderZoomを紹介します。既存の3D世界生成モデルは、単一スケール合成に限定されており、異なる粒度のシーンコンテンツを生成することができません。基本的な課題は、大幅に異なる空間サイズのコンテンツを生成しレンダリングできるスケール感知型3D表現の欠如です。WonderZoomは以下の2つの主要な革新を通じてこの問題に対処します：(1) 多スケール3Dシーンの生成とリアルタイムレンダリング用のスケール適応型ガウスサーフェル、および (2) 微細なスケールの3Dコンテンツを反復的に生成する進行的詳細シンセサイザー。このアプローチにより、ユーザーは3D領域に「ズームイン」し、風景から微視的特徴までの以前存在しなかった微細な詳細を自己回帰的に合成することが可能になります。実験結果は、WonderZoomが品質および整合性の両面で最先端の動画モデルや3Dモデルを大幅に上回り、単一の画像から多スケール3D世界を作成することを可能にしていることを示しています。生成された多スケール3D世界の動画結果およびインタラクティブビューアーは、補足資料のウェブサイトで公開しています。
</details>

<details>
<summary> 英語要旨 </summary>

We present WonderZoom, a novel approach to generating 3D scenes with contents across multiple spatial scales from a single image. Existing 3D world generation models remain limited to single-scale synthesis and cannot produce coherent scene contents at varying granularities. The fundamental challenge is the lack of a scale-aware 3D representation capable of generating and rendering content with largely different spatial sizes. WonderZoom addresses this through two key innovations: (1) scale-adaptive Gaussian surfels for generating and real-time rendering of multi-scale 3D scenes, and (2) a progressive detail synthesizer that iteratively generates finer-scale 3D contents. Our approach enables users to ``zoom into'' a 3D region and auto-regressively synthesize previously non-existent fine details from landscapes to microscopic features. Experiments demonstrate that WonderZoom significantly outperforms state-of-the-art video and 3D models in both quality and alignment, enabling multi-scale 3D world creation from a single image. We show video results and an interactive viewer of generated multi-scale 3D worlds on the website of the supplementary materials.
</details>

---

### PointGS: Semantic-Consistent Unsupervised 3D Point Cloud Segmentation with 3D Gaussian Splatting
著者: Yixiao Song, Qingyong Li, Wen Wang, Zhicheng Yan

<details>
<summary> 日本語要旨 </summary>

無監督点群セグメンテーションは、完全に監視された方法が必要とする密な点レベルの注釈の高コストを軽減することで、具現化知能や自律走行において重要です。セマンティック情報を補完するために2D事前学習モデル（例えばSAM）を統合するのは自然な選択ですが、このアプローチは離散的な3D点と連続的な2D画像との基本的な不一致に直面します。この不一致は避けられない投影重複と複雑なモダリティ整合を引き起こし、結果として2D-3D転送におけるセマンティックの一貫性が損なわれます。この制限を克服し、セマンティック一貫性のあるセグメンテーションを達成するために、本論文では単純で効果的な無監督3D点群セグメンテーション用パイプラインであるPointGSを提案します。PointGSは離散-連続ドメインのギャップを埋めるために、統一された中間表現として3Dガウススプラッティングを利用します。入力の希薄な点群はまず多視点観測を通じて密な3Dガウス空間に再構築され、空間的な隙間を埋め、遮蔽関係をエンコードして投影誘発のセマンティック混同を排除します。多視点密画像はガウス空間からレンダリングされ、SAMによって2Dセマンティックマスクが抽出され、対比的学習を通じて3Dガウス原始体へのセマンティックが転送され、異なる視点間で一貫したセマンティック割り当てが保証されます。ガウス空間は元の点群と2段階登録によって整合され、ラベル付きガウスから最近傍探索を通じて点セマンティックが割り当てられます。実験ではPointGSが最先端の無監督方法を上回り、ScanNet-V2で+0.9% mIoU、S3DISで+2.8% mIoUを達成し、ラベルフリー3Dセグメンテーションにおけるその効果を強調しています。
</details>

<details>
<summary> 英語要旨 </summary>

Unsupervised point cloud segmentation is critical for embodied intelligence and autonomous driving, as it mitigates the prohibitive cost of dense point-level annotations required by fully supervised methods. Integrating 2D pre-trained models such as SAM to supplement semantic information is a natural choice, yet this approach faces a fundamental mismatch between discrete 3D points and continuous 2D images. This mismatch leads to inevitable projection overlap and complex modality alignment, resulting in compromised semantic consistency across 2D-3D transfer.​ To address these limitations and achieve semantic-consistent segmentation, this paper proposes PointGS, a simple yet effective pipeline for unsupervised 3D point cloud segmentation. PointGS leverages 3D Gaussian Splatting as a unified intermediate representation to bridge the discrete-continuous domain gap. Input sparse point clouds are first reconstructed into dense 3D Gaussian spaces via multi-view observations, filling spatial gaps and encoding occlusion relationships to eliminate projection-induced semantic conflation. Multi-view dense images are rendered from the Gaussian space, with 2D semantic masks extracted via SAM, and semantics are distilled to 3D Gaussian primitives through contrastive learning to ensure consistent semantic assignments across different views. The Gaussian space is aligned with the original point cloud via two-step registration, and point semantics are assigned through nearest-neighbor search on labeled Gaussians. Experiments demonstrate that PointGS outperforms state-of-the-art unsupervised methods, achieving +0.9\% mIoU on ScanNet-V2 and +2.8\% mIoU on S3DIS, highlighting its effectiveness in label-free 3D segmentation.​
</details>

---

### CrackSSM: Reviving SSMs for Crack Segmentation Via Dynamic Scanning
著者: Yubin Gu, Boyang Hou, Yuan Meng, Wenting Luo, Jiayi Ji, Xiaoshuai Sun

<details>
<summary> 日本語要旨 </summary>

生産シナリオにおける構造的な点検と保守のため、クラックセグメンテーション（CS）は重要です。高精度かつ効率性を達成するために、最近の方法では状態空間モデル（SSMs）に基づくマンバアーキテクチャが採用されており、これによって長距離依存関係を線形複雑性でモデリングすることが可能になっています。しかし、既存のアプローチは通常、視覚特徴を固定された多方向スキャンを用いてシーケンスに平坦化します。この固定された平坦化順序は空間的連続性を妨げ、SSMが不規則なクラックパターンを効果的にモデル化する能力を弱めます。この制限に対処するため、私たちは**CrackSSM**という新しいクラック認識セグメンテーションフレームワークを提案します。これは各画像の基礎構造に適応する動的スキャニング戦略を特徴としています。具体的には、高次元セマンティック特徴から4つの方向で方向応答強度を計算し、これらの値を用いてトークンを再配置します。このようにすることで、クラック関連領域がシーケンス内で隣接したままになります。この整列はSSMの因果モデリング能力を向上させつつ効率性を保ち、不規則かつ微細なクラックの特性により適しています。また、詳細な特徴を回復するためにウェーブレットガイド付きデコードメカニズムを設計しました。これは入力画像から抽出された高周波成分を取り込み、それらを用いて特徴の洗練とエッジ認識融合をガイドし、さらにセグメンテーション精度を向上させます。3つのベンチマークデータセットでの実験では、私たちの方法が既存の最先端モデルと比較して優れたセグメンテーション精度を達成し、かつ少ないパラメータでより速い推論を行うことが示されました。ソースコードは補足資料にて提供しています。
</details>

<details>
<summary> 英語要旨 </summary>

Crack segmentation (CS) is crucial for structural inspection and maintenance in production scenarios. To achieve both high accuracy and efficiency, recent methods have adopted Mamba-based architectures built upon state space models (SSMs), which enable linear-complexity modeling of long-range dependencies. However, existing approaches typically rely on static multi-directional scanning to flatten visual features into sequences. This fixed flattening order disrupts spatial continuity and weakens the SSM’s ability to model irregular crack patterns effectively. To address this limitation, we propose \textbf{CrackSSM}, a novel crack-aware segmentation framework featuring a dynamic scanning strategy that adapts the token sequence to the underlying structure of each image. Specifically, we compute directional response strength along four orientations from high-level semantic features, and use these values to reorder tokens so that crack-relevant regions remain adjacent in sequence. This alignment improves the causal modeling ability of SSMs while preserving their efficiency and better suits the irregular, fine-grained nature of cracks. Additionally, we design a wavelet-guided decoding mechanism to recover detailed features. It incorporates high-frequency components extracted from the input image and applies them to guide feature refinement and edge-aware fusion, further enhancing segmentation precision. Experiments on three benchmark datasets demonstrate that our method achieves superior segmentation accuracy with fewer parameters and faster inference compared to existing state-of-the-art models. Source code is available in supplementary materials.
</details>

---

### DeltaQuant: 4-bit Video Diffusion Models with Spatiotemporal Delta Smoothing
著者: Xingyang Li, Samuel Tesfai, Zhekai Zhang, Haocheng Xi, Shuo Yang, Lvmin Zhang, Yufei Sun, Kelly Peng, Maneesh Agrawala, Ion Stoica, Kurt Keutzer, Jun-Yan Zhu, Song Han, Yujun Lin, Muyang Li

<details>
<summary> 日本語要旨 </summary>

ビデオ拡散モデルは驚異的な生成性能を達成していますが、その大規模な計算およびメモリコストは特に消費者向けGPUでの展開において重要な課題となっています。最近の注意深い最適化の進歩が以前の計算上のボトルネックを緩和する一方で、線形層は現在、計算コストおよび推論メモリの両方を支配しています。本研究では、これらの層を加速するために重みと活性化関数をそれぞれ4ビットで量子化することに焦点を当てます。SVDQuantなどの以前の方法は、ノイズ除去ステップ間で非常にダイナミックな活性化関数の特性を無視しており、チャンネルや大きさが劇的に変動します。しかし、ビデオデータは空間と時間の近傍トークン間で強い活性化類似性を示し、これを**スパイソテンポラル活性化類似性**と呼びます。これはビデオコーデックがインターフレームおよびインフレーム冗長性を利用するのに類似しています。この特性を活かし、我々は**DeltaQuant**を導入します。これは活性化関数を局所的な3Dスパイソテンポラルキューブに分割し、各キューブの平均トークンを**コアトークン**として使用し、4ビットで小さな差異（デルタトークン）だけを量子化しつつ、コアトークンはFP8で保持します。この分解により、ほとんどオーバーヘッドを増やすことなく量子化誤差が大幅に削減されます。重みの量子化においては、DeltaQuantはSVDQuantの低ランク分解を取り入れることでさらに量子化誤差を削減します。また、DeltaQuantの計算上の利点を実際の速度向上に翻訳する効率的なカーネルも実装しています。Wan 2.2 I2V、Wan 2.2 T2V、LTX-Video T2Vでの広範囲な実験では、DeltaQuantが高い生成忠実度を維持することを示しています。Wan 2.2においてはモデルサイズを2.9倍圧縮し、メモリフットプリントを2.3倍削減します。DeltaQuantは効率的な注意機構と少ステップの蒸留に互換性があります。これらの技術と統合することで、追加の3.0倍の加速を達成し、総計111.8倍のエンドツーエンドのスピードアップを実現します。コードおよびモデルは発表時にリリースされます。
</details>

<details>
<summary> 英語要旨 </summary>

Video diffusion models have achieved remarkable generative performance, but their substantial computational and memory costs pose significant challenges for deployment, especially on consumer GPUs. As recent advances in attention optimization mitigate previous computational bottlenecks, linear layers now dominate both computational cost and inference memory. In this work, we focus on quantizing both weights and activations to 4 bits to accelerate these layers. Previous methods, such as SVDQuant, overlook the highly dynamic nature of activations across denoising timesteps, where outlier channels and magnitudes vary dramatically. However, video data inherently exhibits strong activation similarity among neighboring tokens in space and time, which we term \textbf{spatiotemporal activation similarity}, analogous to how video codecs exploit intra- and inter-frame redundancy. Leveraging this property, we introduce \textbf{DeltaQuant}, which partitions activations into local 3D spatiotemporal cubes and uses each cube's mean token as a \coretoken, quantizing only the small differences (delta tokens) to 4 bits while keeping core tokens in FP8. This decomposition substantially reduces quantization error with minimal overhead. For weight quantization, DeltaQuant incorporates SVDQuant's low-rank decomposition to further reduce quantization error. We also implement an efficient kernel that translates DeltaQuant's computational benefits into real-world speedups. Extensive experiments on Wan 2.2 I2V, Wan 2.2 T2V, and LTX-Video T2V demonstrate that DeltaQuant maintains high generation fidelity.On Wan 2.2, it compresses model size by 2.9× and reduces memory footprint by 2.3×. DeltaQuant is compatible with efficient attention mechanisms and few-step distillation. When integrated with these techniques, it achieves an additional 3.0× acceleration, for a total 111.8× end-to-end speedup. Code and models will be released upon publication.
</details>

---

### Leveraging Verifier-Based Reinforcement Learning in Image Editing
著者: Hanzhong Guo, Jie Wu, Jie Liu, Yu Gao, Zilyu Ye, Linxiao Yuan, Xionghui Wang, Yizhou Yu, Weilin Huang

<details>
<summary> 日本語要旨 </summary>

人間からのフィードバックに基づく強化学習（RLHF）は、テキストから画像生成において重要なパラダイムとなっていますが、その応用範囲は画像編集においてまだ十分に探求されていません。主なボトルネックは、すべての編集タスクに対する堅牢な一般的報酬モデルが不足していることです。既存の編集用報酬モデルは通常、詳細なチェックを行わずに全体的なスコアを与えており、異なる指示要件を無視し偏った報酬を引き起こしています。これに対処するために、私たちは検証者ベースの推論報酬モデル（RRM）を提案します。このモデルは指示を検証可能な原則に分解し、編集された画像をそれぞれの原則に対して評価し、細かいスコアを集計することで幻覚を減少させ、より解釈可能な基準を提供します。このためには、単なるスコアラーから推論検証者への移行が鍵です。私たちはEdit-R1というフレームワークを導入し、これを使ってチェイン・オブ・シンキング（CoT）に基づく推論報酬モデル（RRM）を構築し、下流の編集タスクに応用します。Edit-RRMは指示を異なる原則に分解し、それぞれに対して編集された画像を評価し、これらのチェックを集計して解釈可能で細かい報酬を提供します。このようなRRMを構築するためには、まず「冷スタート」として監督付き微調整（SFT）を適用し、CoT報酬軌道を生成します。次に、人間のペアワイズ優先度データを活用するグループ対照的好み最適化（GCPO）という強化学習アルゴリズムを導入し、点ごとのRRMを強化します。RRMが構築された後、この非微分可能でありながらも強力な報酬モデルを用いてGRPOを使用して編集モデルをトレーニングします。広範囲の実験により、私たちのEdit-RRMはSeed-1.5-VLやSeed-1.6-VLなどの強力なVLMを編集特化型報酬モデルとして上回ることが示されました。また、パフォーマンスに明確なスケーリング傾向があり、3Bから7Bのパラメータで一貫して改善されていることを観察しました。さらに、Edit-R1はFLUX.1-kontextのような編集モデルに利益をもたらし、その画像編集向上への効果を強調しています。
</details>

<details>
<summary> 英語要旨 </summary>

While Reinforcement Learning from Human Feedback (RLHF) has become a pivotal paradigm for text-to-image generation, its application to image editing remains largely unexplored. A key bottleneck is the lack of a robust general reward model for all editing tasks. Existing edit reward models usually give overall scores without detailed checks, ignoring different instruction requirements and causing biased rewards. To address this, we propose the Verifier-Based Reasoning Reward Model (RRM), which breaks instructions into verifiable principles, evaluates the edited images against each principle, and aggregates fine-grained scores to reduce hallucinations and provide more interpretable criteria. To address this, we argue the key is to move from a simple scorer to a reasoning verifier. We introduce Edit-R1, a framework to build a chain-of-thought (CoT) verifier-based reasoning reward model (RRM) and leverage it into the downstream editing task. The Edit-RRM breaks instructions into distinct principles, evaluates the edited image against each, and aggregates these checks to provide an interpretable, fine-grained reward. To build such an RRM, we first apply supervised fine-tuning (SFT) as a “cold-start” to generate CoT reward trajectories. Then, we introduce Group Contrastive Preference Optimization (GCPO), a reinforcement learning algorithm that leverages human pairwise preference data to reinforce our pointwise RRM. After building the RRM, we use GRPO to train editing models with this non-differentiable yet powerful reward model. Extensive experiments demonstrate that our Edit-RRM surpasses powerful VLMs such as Seed-1.5-VL and Seed-1.6-VL as an editing-specific reward model, and we observe a clear scaling trend, with performance consistently improving from 3B to 7B parameters. Moreover, Edit-R1 delivers gains to editing models like FLUX.1-kontext, highlighting its effectiveness in enhancing image editing.
</details>

---

### Skyra: AI-Generated Video Detection Via Grounded Artifact Reasoning
著者: Yifei Li, Wenzhao Zheng, Yanran Zhang, Runze Sun, Yu Zheng, Lei Chen, Jie Zhou, Jiwen Lu

<details>
<summary> 日本語要旨 </summary>

AI駆動のビデオ生成技術の誤用が深刻な社会的懸念を引き起こし、信頼性の高いAI生成ビデオ検出器の必要性が急務となっています。しかし、既存の多くの方法はバイナリ分類に限定されており、人間の解釈に必要な説明を欠いています。本論文では、AI生成ビデオ内の人間が知覚可能な視覚的アーティファクトを特定し、それらを検出および説明のための根拠として活用する専門化されたマルチモーダル大言語モデル（MLLM）である**Skyra**を紹介します。この目的を支援するために、詳細な人間の注釈を持つ最初の大規模AI生成ビデオアーティファクトデータセットである**ViF-CoT-4K**を構築し、Supervised Fine-Tuning（SFT）に使用します。その後、モデルの空間的・時間的アーティファクト知覚能力、説明能力、および検出精度を体系的に向上させる二段階のトレーニング戦略を開発します。Skyraを包括的に評価するために、10以上の最先端ビデオジェネレーターで生成された3,000の高品質サンプルからなる**ViF-Bench**というベンチマークを導入します。広範な実験により、Skyraが複数のベンチマークで既存の方法を上回っていることが示されており、私たちの評価は説明可能なAI生成ビデオ検出の進展に向けた貴重な洞察をもたらしています。コード、モデル、データセットを公開します。
</details>

<details>
<summary> 英語要旨 </summary>

The misuse of AI-driven video generation technologies has raised serious social concerns, highlighting the urgent need for reliable AI-generated video detectors. However, most existing methods are limited to binary classification and lack the necessary explanations for human interpretation. In this paper, we present $\textbf{Skyra}$, a specialized multimodal large language model (MLLM) that identifies human-perceivable visual artifacts in AI-generated videos and leverages them as grounded evidence for both detection and explanation. To support this objective, we construct $\textbf{ViF-CoT-4K}$ for Supervised Fine-Tuning (SFT), which represents the first large-scale AI-generated video artifact dataset with fine-grained human annotations. We then develop a two-stage training strategy that systematically enhances our model's spatio-temporal artifact perception, explanation capability, and detection accuracy. To comprehensively evaluate Skyra, we introduce $\textbf{ViF-Bench}$, a benchmark comprising 3K high-quality samples generated by over ten state-of-the-art video generators. Extensive experiments demonstrate that Skyra surpasses existing methods across multiple benchmarks, while our evaluation yields valuable insights for advancing explainable AI-generated video detection. Our code, models, and datasets will be made publicly available.
</details>

---

### MotionV2V: Editing Motion in A Video
著者: Ryan Burgert, Charles Herrmann, Forrester Cole, Michael Ryoo, Neal Wadhwa, Andrey Voynov, Nataniel Ruiz

<details>
<summary> 日本語要旨 </summary>

生成的ビデオモデルは驚異的な忠実度と一貫性を達成していますが、これらの能力をビデオ編集に応用することは依然として複雑な課題です。最近の研究では、テキストから動画生成や画像アニメーションを向上させるために運動制御可能性を広範囲に探求していますが、私たちは正確な運動制御を編集の有望でありながら未だ十分に探究されていないパラダイムとして特定します。本研究では、入力から抽出したスパーストラジェクトリを直接編集することでビデオの運動を変更する提案を行います。入力と出力のトラジェクトリ間のずれを「運動編集」と呼び、この表現が生成モデルに組み合わされることで多くの強力なビデオ編集機能を可能にすることを示します。これを実現するために、「運動カウンタファクチュアルズ」を生成する新しいパイプラインを導入し、このデータセットで運動条件付きビデオ拡散アーキテクチャを微調整します。私たちのアプローチにより、任意のタイムスタンプから始まる編集が自然に伝播することが可能です。4対1のユーザー評価では、私たちのモデルは65%以上の好みを過去の研究に対して達成しました。
</details>

<details>
<summary> 英語要旨 </summary>

While generative video models have achieved remarkable fidelity and consistency, applying these capabilities to video editing remains a complex challenge. Recent research has extensively explored motion controllability as a means to enhance text-to-video generation or image animation; however, we identify precise motion control as a promising, yet under-explored, paradigm for editing existing videos. In this work, we propose modifying video motion by directly editing sparse trajectories extracted from the input. We term the deviation between input and output trajectories a 'motion edit' and demonstrate that this representation, when coupled with a generative backbone, enables many powerful video editing capabilities. To achieve this, we introduce a novel pipeline for generating `motion counterfactuals' — video pairs that share identical content but distinct motion — and fine-tune a motion-conditioned video diffusion architecture on this dataset. Our approach allows for edits that start at any timestamp and propagate naturally. In a 4-way head-to-head user study, our model achieves over 65% preference against prior work.
</details>

---

### SIR: Structured Image Representations for Explainable Robot Learning
著者: Paul Mattes, Jan Schwab, Jens Bosch, Maximilian Li, Nils Blank, Minh-Trung Tang, Moritz Haberland, Rudolf Lioutikov

<details>
<summary> 日本語要旨 </summary>

既存のロボットポリシーは学習された視覚的埋め込みに基づいており、明示的な構造が欠けており、視覚的な気を散らす要素に対しても感度が高いです。その結果、これらのポリシーを駆動する表現はしばしば不透明であり、意思決定プロセスを解釈することが困難になります。この問題に対処するために、私たちはシーングラフを中間表現として利用する構造化された画像表現という方法を導入します。私たちのアプローチはまず、2Dまたは3D画像から得られる特徴を初期ノード表現として使用し、完全に接続されたグラフを構築します。次に、このグラフをエンド・トゥ・エンドでスパース化するモジュールが学習され、タスクに関連した最小限の部分グラフがアクション生成モデルに渡されます。このプロセスにより、私たちのモデルは本質的に説明可能となります。RoboCasaでの評価では、私たちのスパースグラフポリシーが平均して画像ベースのベンチマークを19.5%対14.81%の成功率で上回ることが示されました。また、私たちはグラフベースの表現が気を散らすオブジェクトに対して画像表現よりも大幅に頑健であることを示し、ほとんどパフォーマンスの低下は見られません。最も重要なことに、学習されたスパースグラフが内省の強力なツールであることを示します。モデルの部分グラフが気を散らすノードを含んだり、重要なオブジェクトを欠落させたりする場合に人間の期待から逸脱しているかどうかを分析することで、データセット内のバイアス、例えば偶発的な相関や位置的バイアスを明らかにすることができました。
</details>

<details>
<summary> 英語要旨 </summary>

Existing robot policies based on learned visual embeddings lack explicit structure and are sensitive to visual distractions. Thus, the representations that drive their behaviour are often opaque, making their decision-making process difficult to interpret. To address this, we introduce Structured Image Representation, a method that leverages Scene Graphs as an intermediate representation for robot policy learning. Our approach first constructs a fully connected graph, using 2D or 3D image-derived features as initial node representations. Then, a module learns to sparsify this graph end-to-end, creating a minimal, task-relevant sub-graph that is passed to the action generation model. This process makes our model intrinsically explainable. Evaluations on RoboCasa show that our sparse graph policies outperform image-based baselines on average with 19.5% vs 14.81% success rate. We also demonstrate that our graph-based representations are significantly more robust to distractor objects, showing almost no performance degradation, as opposed to image representations. Most importantly, we show that the learned sparse graphs are a powerful tool for introspection. By analysing when the model's sub-graph deviates from human expectation, such as by including distractor nodes or omitting key objects, we successfully uncover dataset biases, including spurious correlations and positional biases.
</details>

---

### Beyond The Ground Truth: Enhanced Supervision for Image Restoration
著者: Donghun Ryou, Inju Ha, sanghyeok chu, Bohyung Han

<details>
<summary> 日本語要旨 </summary>

ディープラーニングベースの画像復元は大きな成功を収めています。しかし、実際の劣化に対処する場合、モデルの性能はデータセット内のグランドトゥルース画像の品質によって制限されます。これは、データ取得における実際的な制約に起因します。この制限を解決するために、私たちは既存のグランドトゥルース画像を強化し、より高品質な監督を提供して実世界復元に寄与する新しいフレームワークを提案します。私たちのフレームワークは、超解像処理を用いて知覚的に強化されたグランドトゥルースバリアントを生成し、条件付き周波数マスクジェネレータを使用して適応型の周波数マスクを作成します。これらのマスクは、元のグランドトゥルースとその超解像バリアントから最適に周波数成分を融合するための指針となります。この周波数領域でのミックスアップは、元のコンテンツの意味的一貫性を保持しつつ、選択的に知覚的詳細を豊かにし、忠実度を損なう可能性のある幻想的なアーティファクトを防ぎます。強化されたグランドトゥルース画像は、既存の復元モデルとシームレスに統合できる軽量な出力精緻化ネットワークを訓練するために使用されます。広範な実験は、私たちのアプローチが復元画像の品質を一貫して向上させることを示しています。また、ユーザースタディを通じて、監督強化および出力精緻化の効果を検証しました。私たちはコード、強化された画像、モデル重みを公開することで再現性を支援します。
</details>

<details>
<summary> 英語要旨 </summary>

Deep learning-based image restoration has achieved significant success. However, when addressing real-world degradations, model performance is limited by the quality of ground-truth images in datasets due to practical constraints in data acquisition. To address this limitation, we propose a novel framework that enhances existing ground truth images to provide higher-quality supervision for real-world restoration. Our framework generates perceptually enhanced ground truth variants using super-resolution, and employs a conditional frequency mask generator to produce adaptive frequency masks. These masks guide the optimal fusion of frequency components from the original ground truth and its super-resolved variants to yield enhanced ground truth images. This frequency-domain mixup preserves the semantic consistency of the original content while selectively enriching perceptual details, preventing hallucinated artifacts that could compromise fidelity. The enhanced ground truth images are used to train a lightweight output refinement network that can be seamlessly integrated with existing restoration models. Extensive experiments demonstrate that our approach consistently improves the quality of restored images. We further validate the effectiveness of both supervision enhancement and output refinement through user studies. We will publicly release our code, enhanced images and model weights to support reproducibility.
</details>

---

### Domain-Skewed Federated Learning with Feature Decoupling and Calibration
著者: Huan Wang, Jun Shen, Jun Yan, Guansong Pang

<details>
<summary> 日本語要旨 </summary>

フェデレーテッドラーニング（FL）は、分散クライアントがプライバシーを保護しながらグローバルモデルを協力してトレーニングできるようにします。しかし、主要な課題の一つはドメインスキューです。クライアントのデータが多様なドメインから来ているため、集約されたグローバルモデルが一貫した表現空間を学習することが妨げられ、複数のドメインでの汎化能力が低下します。本論文では、ドメインスキューは各クライアントのドメイン特有のバイアスを持つ特徴に反映されており、これがローカルモデルの表現を狭い低次元サブ空間に収束させる原因となっていると主張します。そこで、ドメイン特有のバイアスを持つ特徴をキャリブレーションすることで貴重なクラス関連情報を解放し、より一貫した表現を可能にするフェデレーテッド・フィーチャー・デコップルング・アンド・キャリブレーション（**$F^2$DC**）を提案します。$F^2$DCでは、各特徴ユニットの堅牢性を決定するために新しいコンポーネントであるドメイン・フィーチャー・デコッパラ（DFD）が初めて導入され、ローカル特徴をドメイン堅牢な特徴とドメイン関連の特徴に分離します。さらに、ドメイン関連の特徴を明示的に識別信号とリンクすることでキャリブレーションし、ドメイン堅牢な特徴を補完する追加のクラス関連の手がかりを捉えるためにドメイン・フィーチャー・コレクタ（DFC）が提案されます。最後に、クライアント間での合意を促進するためにローカルモデルのドメイン認識型集約が行われます。人気のある3つのマルチドメインデータセットにおける実験結果は、提案された$F^2$DCとその二つのモジュールの有効性を示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Federated learning (FL) allows distributed clients to collaboratively train a global model in a privacy-preserving manner. However, one major challenge is domain skew, where clients' data originating from diverse domains may hinder the aggregated global model from learning a consistent representation space, resulting in poor generalizable ability in multiple domains. In this paper, we argue that the domain skew is reflected in the domain-specific biased features of each client, causing the local model's representations to collapse into a narrow low-dimensional subspace. We then propose Federated Feature Decoupling and Calibration (**$F^2$DC**), which liberates valuable class-relevant information by calibrating the domain-specific biased features, enabling more consistent representations across domains. A novel component, Domain Feature Decoupler (DFD), is first introduced in $F^2$DC to determine the robustness of each feature unit, thereby separating the local features into domain-robust features and domain-related features. A Domain Feature Corrector (DFC) is further proposed to calibrate these domain-related features by explicitly linking discriminative signals, capturing additional class-relevant clues that complement the domain-robust features. Finally, a domain-aware aggregation of the local models is performed to promote consensus among clients. Empirical results on three popular multi-domain datasets demonstrate the effectiveness of the proposed $F^2$DC and the contributions of its two modules.
</details>

---

### Open The Motion Door: Atomic Motion Decomposition and Recomposition for Open-Vocabulary Motion Generation
著者: Ke Fan, Jiangning Zhang, Ran Yi, Jingyu Gong, Yabiao Wang, yating wang, Xin Tan, Chengjie Wang, Lizhuang Ma

<details>
<summary> 日本語要旨 </summary>

コンピュータビジョンにおける基本的なタスクであるテキストから動作への生成は、自然言語記述から3D人間の動作シーケンスを合成することを目指しています。しかし、既存のデータセットが限られた規模で多様性に欠けるため、モーションへ直接マッピングするように訓練されたモデルは、ドメイン外のテキスト入力に対して一般化することが難しいです。私たちは、高レベルの動作セマンティクスが広範囲にわたって変化する一方で、多くの動作が共通の原子的な動作セットを共有していることに気づきました。すなわち、単純で再利用可能な身体部分の動きです。この洞察に基づき、オープンボキャブラリーのテキストから動作生成のための**原子的動作分解と再構成フレームワーク**を導入します。私たちのアプローチは二つの主要なコンポーネントで構成されています：ドメイン外の記述を原子的動作単位に分解する**テキスト分解モジュール**と、これらの単位を統合して最終的な動作シーケンスを生成する**原子再構成モジュール**です。私たちのモデルはHumanML3Dデータセット（インドメイン）で競争力のあるパフォーマンスを達成し、IDEA400とMixamoの2つのドメイン外データセットにおける広範な実験は、私たちの方法がオープンボキャブラリー動作生成で最先端のアプローチを大幅に上回っていることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Text-to-motion generation is a fundamental task in computer vision, aiming to synthesize 3D human motion sequences from natural language descriptions. However, due to the limited scale and diversity of existing datasets, models trained to directly map raw text to motion often struggle to generalize to out-of-domain textual inputs. We observe that although high-level motion semantics vary widely, many motions share a common set of underlying atomic motions—that is, simple, reusable body-part movements. Building on this insight, we introduce an **Atomic Motion Decomposition and Recomposition** framework for open-vocabulary text-to-motion generation. Our approach consists of two key components: a **Textual Decomposition** module that parses out-of-domain descriptions into atomic motion units, and an **Atomic Recomposition** module that integrates these units to produce the final motion sequence. Our model achieves a competitive performance on the in-domain HumanML3D dataset, and extensive experiments on two out-of-domain datasets (IDEA400 and Mixamo) demonstrate that our method substantially outperforms state-of-the-art approaches in open-vocabulary motion generation.
</details>

---

### EventHub: Data Factory for Generalizable Event-Based Stereo Networks Without Active Sensors
著者: Luca Bartolomei, Fabio Tosi, Matteo Poggi, Stefano Mattoccia, Guillermo Gallego

<details>
<summary> 日本語要旨 </summary>

私たちは、高価なアクティブセンサーからのグラウンドトゥルース注釈を必要とせずに、標準的なカラー画像だけで深層イベントステレオネットワークを訓練するための新しいフレームワーク「EventHub」を提案します。これらの画像から、最先端の視点合成技術を用いてプロキシ注釈とプロキシイベントを導出するか、または既にイベントデータとペアリングされた画像であれば単にプロキシ注釈を得ます。私たちのデータファクトリーで生成した訓練セットを用いて、RGB文献からの最先端ステレオモデルをイベントデータ処理に再利用し、これまでにない一般化能力を持つ新しいイベントステレオモデルを得ます。広く使用されているイベントステレオデータセットにおける実験は、EventHubの有効性を支持し、夜間シーンなどの難しい条件下でRGBステレオ基礎モデルの精度を向上させることができる同じデータ蒸留メカニズムを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

We propose EventHub, a novel framework for training deep-event stereo networks without ground truth annotations from costly active sensors, relying instead on standard color images. From these images, we derive either proxy annotations and proxy events through state-of-the-art novel view synthesis techniques, or simply proxy annotations when images are already paired with event data. Using the training set generated by our data factory, we repurpose state-of-the-art stereo models from RGB literature to process event data, obtaining new event stereo models with unprecedented generalization capabilities. Experiments on widely used event stereo datasets support the effectiveness of EventHub and show how the same data distillation mechanism can improve the accuracy of RGB stereo foundation models in challenging conditions such as nighttime scenes.
</details>

---

### Think Before You Drive: World Model-Inspired Multimodal Grounding
著者: Haicheng Liao, Huanming Shen, Bonan Wang, yong kang li, Yihong Tang, Chengyue Wang, Dingyi Zhuang, Kehua Chen, HAI YANG, Cheng-Zhong Xu, Zhenning Li

<details>
<summary> 日本語要旨 </summary>

自動運転（AD）において、ターゲットオブジェクトをローカライズするための自然言語コマンドの解釈は重要です。現在のADにおける視覚的なアンカリング（VG）手法は、3D空間関係や予測されるシーン進化に対する推論が欠如しているため、曖昧で文脈依存の指示に苦労しています。世界モデルの原理に基づき、将来の空間状態を考慮した上でアンカリング決定を行うフレームワーク「ThinkDeeper」を提案します。その中核となるのは、現在のシーンをコマンドに対応するラテント状態に圧縮し、将来のラテント状態のシーケンスを展開して曖昧さ解消のための先読み的な手がかりを提供するSpatial-Aware World Model（SA-WM）です。これに加えて、ハイパーグラブーどされたデコーダは階層的にこれらの状態をマルチモーダル入力と融合し、堅牢なローカライズのための高次空間依存関係を捉えます。さらに、AD向けの多源VGデータセット「DrivePilot」を提示します。これはRetrieval-Augmented Generation（RAG）とChain-of-Thought（CoT）プロンプト付きLLMパイプラインで生成された意味的アノテーションを特徴としています。6つのベンチマークにおける広範な評価では、ThinkDeeperはTalk2Carリーダーボードで第1位を獲得し、DrivePilot、MoCAD、RefCOCO/+/gベンチマークのSOTAベースラインを上回りました。特に、長文、多エージェント、曖昧さがある難しいシーンでの強力な堅牢性と効率性も示しており、データの50%しか使用しなくても優れたパフォーマンスを維持します。この論文には匿名コード提出が伴い、データセットは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Interpreting natural-language commands to localize target objects is critical for autonomous driving (AD). Existing visual grounding (VG) methods in AD struggle with ambiguous, context-dependent instructions, as they lack reasoning over 3D spatial relations and anticipated scene evolution. Grounded in the principles of world models, we propose ThinkDeeper, a framework that reasons about future spatial states before making grounding decisions. At its core is a Spatial-Aware World Model (SA-WM) that learns to reason ahead by distilling the current scene into a command-aware latent state and rolling out a sequence of future latent states, providing forward-looking cues for disambiguation. Complementing this, a hypergraph-guided decoder then hierarchically fuses these states with the multimodal input, capturing higher-order spatial dependencies for robust localization. In addition, we present DrivePilot, a multi-source VG dataset in AD, featuring semantic annotations generated by a Retrieval-Augmented Generation (RAG) and Chain-of-Thought (CoT)-prompted LLM pipeline. Extensive evaluations on six benchmarks, ThinkDeeper ranks #1 on the Talk2Car leaderboard and surpasses SOTA baselines on DrivePilot, MoCAD, and RefCOCO/+/g benchmarks. Notably, it also shows strong robustness and efficiency in challenging scenes (long-text, multi-agent, ambiguity) and retains superior performance even when trained on 50% of the data. Our anonymous code submission accompanies this paper, and the dataset will be released publicly.
</details>

---

### RxnCaption: Reformulating Reaction Diagram Parsing As Visual Prompt Guided Captioning
著者: Jiahe Song, Chuang Wang, Bowen Jiang, Yinfan Wang, Hao Zheng, Xingjian Wei, Chengjin Liu, Rui Nie, Junyuan Gao, Jiaxing Sun, Yubin Wang, Lijun Wu, Zhenhua Huang, Jiang Wu, Qian Yu, Conghui He

<details>
<summary> 日本語要旨 </summary>

化学反応データセットは、化学におけるAI研究にとって重要です。しかし、既存の化学反応データは多くが論文内の画像形式で存在し、機械可読ではないため、機械学習モデルのトレーニングに使用することができません。この課題に対応するために、私たちは化学反応図解パーシング（RxnDP）タスク用に\textbf{RxnCaption}フレームワークを提案します。このフレームワークは、従来の座標予測駆動型解析プロセスを画像キャプション問題として再定式化し、これにより大規模ビジョン言語モデル（LVLMs）が自然に対応できるようにします。私たちは「\emph{BBox and Index as Visual Prompt}」（BIVP）と呼ばれる戦略を導入し、これは最先端の分子検出器MolYOLOを使用して、入力画像に直接分子バウンディングボックスとインデックスを事前描画します。この方法により、下流の解析が自然言語記述問題へと変わります。広範な実験では、BIVP戦略が構造抽出品質を大幅に向上させつつモデル設計を簡素化することが示されました。また、私たちは\texttt{RxnCaption-15k}データセットを構築しました。これは既存の実世界文献ベンチマークよりも桁違いに大きく、4つのレイアウトアーキタイプにわたってバランスの取れたテストサブセットを持ちます。実験では、RxnCaption-VLが複数の指標で最先端の性能を達成していることが示されました。私たちは、私たちの方法、データセット、モデルが化学文献からの構造情報抽出を進展させ、より広範な化学分野におけるAI応用を促進すると信じています。データ、モデル、コードはGitHubで公開します。
</details>

<details>
<summary> 英語要旨 </summary>

Large-scale chemical reaction datasets are crucial for AI research in chemistry. However, existing chemical reaction data often exist as images within papers, making them not machine-readable and unusable for training machine learning models. In response to this challenge, we propose the \textbf{RxnCaption} framework for the task of chemical Reaction Diagram Parsing (RxnDP). Our framework reformulates the traditional coordinate prediction driven parsing process into an image captioning problem, which Large Vision Language Models (LVLMs) handle naturally. We introduce a strategy termed ``\emph{BBox and Index as Visual Prompt}'' (BIVP), which uses our state-of-the-art molecular detector, MolYOLO, to pre-draw molecular bounding boxes and indices directly onto the input image. This turns the downstream parsing into a natural-language description problem. Extensive experiments show that the BIVP strategy significantly improves structural extraction quality while simplifying model design. We further construct the \texttt{RxnCaption-15k} dataset, an order of magnitude larger than prior real-world literature benchmarks, with a balanced test subset across four layout archetypes. Experiments demonstrate that RxnCaption-VL achieves state-of-the-art performance on multiple metrics. We believe our method, dataset, and models will advance structured information extraction from chemical literature and catalyze broader AI applications in chemistry. We will release data, models, and code on GitHub.
</details>

---

### Factorize, Reconstruct, Enhance: A Unified Framework for Multimodal Sentiment Analysis
著者: Zhilu Yang, Mingcheng Li

<details>
<summary> 日本語要旨 </summary>

マルチモーダル感情分析（MSA）は、言語的、視覚的、音響的なモダリティからの情報を統合して人間の感情を包括的かつ堅牢に解釈することを目指します。しかし、既存のモデルの性能は、モダリティ固有の不十分な多層セマンティック抽出と静的特徴融合によってしばしば妨げられ、低いパフォーマンスを引き起こします。したがって、本論文では、正確なマルチモーダル感情分析のための多因子因子分離とセマンティクス強化融合フレームワークを提案します。まず、各モダリティは、対比制約によるサブ空間の分離、情報利得制約によるタスク関連特徴の最大化捕捉、ペアワイズ制約による補完的なサブ空間の確保を規制する多次元情報分離メカニズムに基づいて3つの直交サブスペースに分解されます。その後、変分精製戦略が導入され、各感情表現のセマンティック整合性をさらに確保します。最後に、融合モジュールはサンプルレベルのモダリティ顕著度、グローバルサブスペースタイプ重要度、特徴レベル内部注意などの複数の直交因子を用いて並列で適応的な融合重みを計算します。3つのデータセットにおける広範な実験が、提案手法の有効性を示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Multimodal Sentiment Analysis (MSA) aims to comprehensively and robustly interpret human emotions by integrating information from verbal, visual and acoustic modalities. However, the performance of existing models is often hampered by two key challenges: insufficient multilayer semantic extraction inherent to modalities and static feature fusion, leading to low performance. Therefore, this paper proposes a Multi-factor Factor-Decoupling and Semantics-enhanced Fusion Framework for accurate multimodal sentiment analysis. First, each modality is decomposed into three orthogonal subspaces based on a multidimensional information separation mechanism, which is regulated by a contrast constraint for subspace separation, an information gain constraint for maximizing the capture of task-relevant features, and a pairwise constraint for ensuring complementary subspaces. Subsequently, a variational purification strategy is introduced to further ensure the semantic integrity of each sentiment representation. Finally, the fusion module computes the adaptive fusion weights in parallel using multiple orthogonal factors such as sample-level modality saliency, global subspace type importance and feature-level internal attention. Extensive experiments on three datasets demonstrate the effectiveness of the proposed method.
</details>

---

### Masked Region Transformer for Layered Image Generation and Editing at Scale
著者: Zhicong Tang, Jingye Chen, Zhao Zhang, Mohan Zhou, Yuchi Liu, Yifan Pu, Yalong Bai, Ethan Smith, Yuhui Yuan

<details>
<summary> 日本語要旨 </summary>

レイヤー画像の生成と編集は、生成された視覚コンテンツを層ごとに再利用、編集、組み合わせる基本的な能力であり、自然言語の単語レベルの編集に類似しています。その重要性にもかかわらず、この分野はまだ大規模に探求されていません。このギャップを埋めるために、私たちは20Bパラメータの拡散モデルであるマスクドリージョントランスフォーマーを提案します。これは多層透明画像生成と編集用に特化しており、様々なアスペクト比やテキストプロンプトを含む10M以上の多言語デザインサンプルで訓練されています。この規模を最大限に活用するため、私たちは3つの重要な技術的貢献を行いました。まず、テキストからレイヤー、画像からレイヤー、レイヤーからレイヤーという三つの補完的タスクを共有されたマスクドリージョン拡散フレームワーク内で統一しました。ここでは選択的なトークンマスキングにより、柔軟なクロスモーダル生成と細部までの層ごとの編集が可能です。次に、ビジュアルフィデリティを向上させつつ計算効率を維持するために、ゲートドデルタネットとゲート付き注意機構を取り入れた効率的な条件付き拡散デコーダーを設計しました。さらに、境界不整合を処理し半透明背景の合成をサポートすることで、可視キャンバスの境界を超えた完全な編集可能レイヤー生成を可能にするオーバーフローアウェアキャンバス層を導入しました。また、分布マッチング蒸留を適用して最小限の品質劣化でリアルタイムかつ一段階の多層生成を実現しました。広範な実験により、私たちのフレームワークがすべての三つのタスクにおいて既存の最先端アプローチを大幅に上回ることが示され、透明画像生成における領域認識新たな基準を確立しました。
</details>

<details>
<summary> 英語要旨 </summary>

Layered image generation and editing is a fundamental capability that enables layer-wise reuse, editing, and composition of the generated visual content, analogous to word-level editing in natural language. Despite its importance, this remains an underexplored area at scale. To address this gap, we present the Masked Region Transformer, a 20B-parameter diffusion model tailored for multi-layer transparent image generation and editing, trained on over 10M multilingual design samples spanning diverse aspect ratios and textual prompts. To fully leverage this scale, we make three key technical contributions. First, we unify three complementary tasks---text-to-layers, image-to-layers, and layers-to-layers---within a shared masked region diffusion framework, where selective token masking enables flexible cross-modal generation and fine-grained layer-wise editing. Second, we design an efficient conditional diffusion decoder that incorporates Gated DeltaNet and gated attention mechanisms, enhancing visual fidelity while maintaining computational efficiency. Third, we introduce an overflow-aware canvas layer to handle boundary inconsistencies and support semi-transparent background synthesis, enabling complete editable layer generation beyond visible canvas boundaries. Additionally, we apply distribution matching distillation to achieve one-step, real-time multi-layer generation with minimal quality degradation. Extensive experiments demonstrate that our framework substantially outperforms prior state-of-the-art approaches across all three tasks, establishing a new benchmark for region-aware transparent image generation.
</details>

---

### Ultra Diffusion Poser: Diffusion-Based Human Motion Tracking from Sparse Inertial Sensors and Ranging-based Between-sensor Distances
著者: Dominik Hollidt, Tommaso Bendinelli, Christian Holz

<details>
<summary> 日本語要旨 </summary>

IMU（慣性計測装置）を用いた手法は、カメラベースの動作キャプチャに対するウェアラブルな代替手段を提供します。インターセンサー間距離を超広帯域（UWB）測位で計測し、最近のスパースインダクティブポーズ推定器は、慣性信号からのドリフトを軽減するためにこれらを統合しています。これまで、UWB距離は追加入力特徴として使用されてきましたが、センサー位置に課せられる物理的制約を無視していました。しかし、これらの距離は3Dセンサーレイアウトを再構築するためにも使用でき、それがポーズ再構成のより情報豊かな入力となります。私たちは、これらの幾何学的制約を明示的にモデル化する拡散モデル「Ultra Diffusion Poser」を提案します。このモデルには、UWB測定から3Dセンサー位置を解析的に再構築するSpatial Layout Moduleが含まれています。これらのセンサー位置は、IMU信号やUWB距離と共に拡散中の条件付き信号として使用されます。しかし、ネットワーク予測は依然としてインターセンサー間距離測定を破る可能性があります。これに対処するため、「UWB-Diffusion Guidance」を導入し、拡散サンプリング中の予測ポーズと測定された距離の整合性を促進します。これらの貢献により、私たちのモデルは最先端のパフォーマンスを達成し、以前の作業と比較して関節位置エラーを最大22%削減することができます。コードは受理後に公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Methods using inertial measurement units (IMUs) provide a wearable alternative to camera-based motion capture. To mitigate drift from inertial signals, recent sparse inertial pose estimators integrate inter-sensor distances measured by ultra-wideband (UWB) ranging. So far, UWB distances have only been used as an additional input feature, ignoring the physical constraints they impose on sensor positions. However, these distances can also be used to reconstruct the underlying 3D sensor layout, which in turn provides more informative input for pose reconstruction. We propose Ultra Diffusion Poser, a diffusion model that explicitly models these geometric constraints. It includes a Spatial Layout Module that analytically reconstructs the 3D sensor positions from UWB measurements. These sensor positions are used alongside IMU signals and UWB distances as a conditioning signal during diffusion. Still, network predictions can violate inter-sensor distance measurements. To address this, we introduce UWB-Diffusion Guidance, which encourages alignment between predicted poses and measured distances during diffusion sampling. Together, these contributions enable our model to achieve state-of-the-art performance, reducing joint position error by up to 22% over prior work. Code will be released upon acceptance.
</details>

---

### CogniVerse: Revolutionizing Multi-modal Retrieval-Augmented Generation with Cognitive Reflection and Geometric Reasoning
著者: Xiang Fang, Wanlong Fang, Changshuo Wang

<details>
<summary> 日本語要旨 </summary>

多モーダルリトリーバル強化生成（MMRAG）は、外部の視覚的、テキスト、構造的知識を統合することで、知識集約型質問応答におけるマルチモーダル大規模言語モデル（MLLMs）の能力を強化する強力なパラダイムとして登場しました。しかし、既存のMMRAGフレームワークは、ノイズや関連性のないリトリーバル、異種間の意味的不整合、適応的推論の欠如、およびローカルとグローバルコンテキストにわたる生成の不連続性など、重大な制約を抱えています。私たちは、これらの課題に対処するために、認知的インスピレーションと数学的厳密さに基づく新しいMMRAGフレームワークである**CogniVerse**を導入します。人間のような推論から引用して、CogniVerseは三つの相乗的コンポーネントを統合します：（1）認知反映モジュール（CRM）は、リトリーバルの必要性を動的に評価し、関連するマルチモーダルコンテンツをフィルタリングしてノイズと計算オーバーヘッドを削減します；（2）マルチモーダルリトリーバルモジュールは、情報幾何学を用いてリーマン多様体上で埋め込みを整列させ、スペクトラルグラフ理論によって知識グラフを洗練し、正確かつ一貫したリトリーバルを保証します；（3）階層的生成モジュールは、最適輸送ベースの損失関数を用いて、トークンレベルの精度とグローバルセマンティックな一貫性をバランスさせます。CogniVerseは、幾何学的整列の収束保証やスペクトラル最適化に基づく先進的理論フレームワークに根ざしており、堅牢な異種間統合と適応的知識利用を実現します。マルチモーダル質問応答のベンチマークデータセットに関する広範な実験では、CogniVerseが精度と一貫性の両方で最先端のMMRAGシステムを大幅に上回り、リトリーバル遅延も削減していることが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

Multi-modal Retrieval-Augmented Generation (MMRAG) has emerged as a powerful paradigm for enhancing Multimodal Large Language Models (MLLMs) in knowledge-intensive question answering by integrating external visual, textual, and structural knowledge. However, existing MMRAG frameworks suffer from critical limitations, including noisy and irrelevant retrieval, cross-modal semantic misalignment, lack of adaptive reasoning, and incoherent generation across local and global contexts. We introduce \textbf{CogniVerse}, a novel MMRAG framework that addresses these challenges through a cognitive-inspired, mathematically rigorous approach. Drawing from human-like reasoning, CogniVerse integrates three synergistic components: (1) a Cognitive Reflection Module (CRM) that dynamically assesses retrieval necessity and filters relevant multi-modal content, reducing noise and computational overhead; (2) a Multi-modal Retrieval Module that aligns embeddings in a Riemannian manifold using information geometry and refines knowledge graphs via spectral graph theory, ensuring precise and coherent retrieval; and (3) a Hierarchical Generation Module that employs an optimal transport-based loss to balance token-level accuracy and global semantic coherence. Grounded in advanced theoretical frameworks, including convergence guarantees for geometric alignment and spectral optimization, CogniVerse achieves robust cross-modal integration and adaptive knowledge utilization. Extensive experiments on benchmark multi-modal question answering datasets demonstrate that CogniVerse significantly outperforms state-of-the-art MMRAG systems in both accuracy and coherence, while reducing retrieval latency.
</details>

---

### DiffDecompose: Layer-Wise Decomposition of Alpha-Composited Images Via Diffusion Transformers
著者: Hang Zhao, Hang Zhao, Qianyu Zhou, Xuequan Lu, Xiangtai Li, Hao Yang, Bo Yang, Yiren Song

<details>
<summary> 日本語要旨 </summary>

最近、生成タスク（例えばオブジェクト除去）で大きな成功を収めている拡散モデルにもかかわらず、既存の画像分解方法はマスク優先度依存性、静的オブジェクト仮定、およびデータセット不足により半透明または透明なレイヤーの重なりを分離することが困難です。本論文では、新しいタスクであるアルファ合成画像のレイヤー別分解に取り組みます。これは、半透明/透明なアルファ層非線形重なりの条件下で、オーバーラップした単一画像から構成レイヤーを回復することを目的としています。レイヤー曖昧性、汎化能力、データ不足に対処するために、まずAlphaBlendを導入します。これは透明および半透明レイヤー分解のための最初の大規模かつ高品質なデータセットであり、特徴が異なる6つのサブタスク（例：軽度フレア除去、半透明細胞分解、ガラス器具分解）を含んでいます。このデータセットに基づき、DiffDecomposeという拡散トランスフォーマーに基づくフレームワークを提示します。これは入力画像、セマンティックプロンプト、ブレンディングタイプに条件付けられた可能なレイヤー分解の事後確率を学習します。直接アルファマットを回帰する代わりに、DiffDecomposeはインコンテキスト分解を行い、モデルが個別のレイヤー監督なしで1つまたは複数のレイヤーを予測できるようにします。さらに、ピクセルレベルの対応関係を各レイヤー間で維持するためにレイヤーポジションエンコーディングクローニングを導入します。提案されたAlphaBlendデータセットおよび公開LOGOデータセットでの広範な実験により、DiffDecomposeの有効性が確認されました。コードとデータセットは論文受理後に利用可能になります。
</details>

<details>
<summary> 英語要旨 </summary>

Diffusion models have recently motivated great success in many generation tasks like object removal. Nevertheless, existing image decomposition methods struggle to disentangle semi-transparent or transparent layer occlusions due to mask prior dependencies, static object assumptions, and the lack of datasets. In this paper, we delve into a novel task: Layer-Wise Decomposition of Alpha-Composited Images, aiming to recover constituent layers from single overlapped images under the condition of semi-transparent/transparent alpha layer non-linear occlusion. To address challenges in layer ambiguity, generalization, and data scarcity, we first introduce AlphaBlend, the first large‑scale and high-quality dataset for transparent and semi‑transparent layer decomposition, containing six subtasks with different characteristics (e.g., translucent flare removal, semi-transparent cell decomposition, glassware decomposition). Building on this dataset, we present DiffDecompose, a diffusion Transformer-based framework that learns the posterior over possible layer decompositions conditioned on the input image, semantic prompts, and blending type. Rather than regressing alpha mattes directly, DiffDecompose performs In‑Context Decomposition, enabling the model to predict one or multiple layers without per‑layer supervision, and introduces Layer Position Encoding Cloning to maintain pixel‑level correspondence across layers. Extensive experiments on the proposed AlphaBlend dataset and public LOGO dataset verify the effectiveness of DiffDecompose. The code and dataset will be available upon paper acceptance.
</details>

---

### M4-RAG: A Massive-Scale Multilingual Multi-Cultural Multimodal RAG
著者: David Anugraha, Patrick Irawan, Anshul Singh, En-Shiun Annie Lee, Genta Indra Winata

<details>
<summary> 日本語要旨 </summary>

ビジョン・ランゲージ モデル（VLMs）は視覚的な質問応答（VQA）において強力な性能を発揮していますが、静的なトレーニングデータに制約されています。リカバリー・アジャンクションド・ジェネレーション（RAG）はこの限界を緩和し、最新の情報や文化的背景、多言語に対応した情報へのアクセスを可能にしますが、多言語・マルチモーダル RAG は未だ十分に探求されていません。私たちは42言語と56地域方言・レジスターをカバーする大規模な基準である M4-RAG を導入し、多様な文化的背景を持つ画像–質問ペア80,000件以上を含むこの基準を用いて言語やモダリティを超えたリカバリー・アジャンクションド VQA を評価します。現実性と再現可能性のバランスを取るため、私たちは質問領域に関連する慎重に選定された多言語文書数百万件を含む制御されたリカバリー環境を構築し、実世界のリカバリー条件を模倣しつつ一貫した実験が可能になるようにしています。系統的な評価からは、RAG が小規模な VLMs に対して常に有益であることが示されましたが、大規模モデルへのスケーリングでは失敗し、場合によってはパフォーマンスを低下させてしまうこともあり、これは現在のリカバリー効果とモデルサイズ間の重要な不一致を露呈しています。M4-RAG は言語、モダリティ、文化的背景を横断したスムーズな推論が可能な次世代 RAG システムの発展の基盤を提供します。
</details>

<details>
<summary> 英語要旨 </summary>

Vision–language models (VLMs) have achieved strong performance in visual question answering (VQA), yet they remain constrained by static training data. Retrieval-Augmented Generation (RAG) mitigates this limitation by enabling access to up-to-date, culturally grounded, and multilingual information; however, multilingual multimodal RAG remains largely underexplored. We introduce M4-RAG, a massive-scale benchmark covering 42 languages and 56 regional dialects and registers, comprising over 80,000 culturally diverse image–question pairs for evaluating retrieval-augmented VQA across languages and modalities. To balance realism with reproducibility, we build a controlled retrieval environment containing millions of carefully curated multilingual documents relevant to the query domains, approximating real-world retrieval conditions while ensuring consistent experimentation. Our systematic evaluation reveals that although RAG consistently benefits smaller VLMs, it fails to scale to larger models and often even degrades their performance, exposing a critical mismatch between model size and current retrieval effectiveness. M4-RAG provides a foundation for advancing next-generation RAG systems capable of reasoning seamlessly across languages, modalities, and cultural contexts.
</details>

---

### Language-guided Frequency Modulation for Large Vision-Language Models
著者: Shuyi Ouyang, Gongfan Fang, Xinyin Ma, Yen-Wei Chen, Lanfen Lin, Xinchao Wang

<details>
<summary> 日本語要旨 </summary>

大規模ビジョン言語モデル（LVLM）は、多様なタスクにおける視覚的推論能力を示しています。これらのタスクは視覚表現に異なる要求を置きます：一部は高レベルのグローバルコンテキストを優先し、他方では細部への注力が強調されます。しかし、既存の多くの手法は主に空間領域で視覚表現を扱い、高周波数の局所的な詳細と低周波数のグローバルコンテキストを明示的に区別するメカニズムが欠けています。この制限は視覚表現の微細な制御を妨げ、言語との階層的整合性を複雑化します。この問題に対処するために、私たちは言語ガイド付き周波数変調（LFM）を導入しました。これは、言語の指示の下で周波数領域において視覚信号を適応的に洗練するプラグアンドプレイ手法です。重要な領域や詳細を選択的に強化することで、LFMはより構造化された正確な視覚処理を可能にします。特に、追加のトレーニングパラメータを必要とせず、軽量かつ学習可能なプロジェクターを用いてLLMへの統合前に視覚トークンを洗練することで、計算上のオーバーヘッドを最小限に抑えます。多様なビジョン言語ベンチマークにわたる広範な実験は、LFMのスケーラビリティ、効果性、およびLVLMへの幅広い適用可能性を強調しています。コードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Large Vision-Language Models (LVLMs) have demonstrated remarkable capabilities in visual reasoning across diverse tasks. These tasks place different demands on visual representations: some prioritize high-level global context, while others emphasize fine-grained local details. However, most existing methods operate on visual representations primarily in the spatial domain, lacking an explicit mechanism for distinguishing between high-frequency local details and low-frequency global context. This limitation hinders fine-grained control of visual representations and complicates their hierarchical alignment with language. To address this issue, we introduce Language-guided Frequency Modulation (LFM), a plug-and-play approach that adaptively refines visual signals in the frequency domain under linguistic guidance. By selectively enhancing critical regions and details, LFM enables more structured and precise visual processing. Crucially, it adds no extra training parameters, relying solely on a lightweight learnable projector to refine visual tokens before integration into the LLM, thereby ensuring minimal computational overhead. Extensive experiments across diverse vision-language benchmarks highlight LFM’s scalability, effectiveness, and broad applicability to LVLMs. The code will be publicly available.
</details>

---

### Gated Condition Injection Without Multimodal Attention: Towards Controllable Linear-Attention Transformers
著者: Yuhe Liu, Zhenxiong Tan, Yujia Hu, Songhua Liu, Xinchao Wang

<details>
<summary> 日本語要旨 </summary>

最近の拡散ベースの制御可能な視覚生成技術は、画像品質において顕著な改善をもたらしています。しかし、これら強力なモデルは通常、大きな計算要求のためクラウドサーバー上で展開されることが多く、ユーザーデータプライバシーに関する深刻な懸念を引き起こしています。この問題に対処し、安全かつ効率的なオンデバイス生成を可能にするため、本論文では線形注意アーキテクチャ上に構築された制御可能な拡散モデルを探求します。これらのアーキテクチャは、エッジデバイスであっても優れたスケーラビリティと効率性を提供します。しかし、実験により、ControlNetやOminiControlなどの既存の制御可能生成フレームワークは、複数の異種条件タイプをサポートする柔軟性が欠けているか、線形注意モデル上での収束速度が遅いことが明らかになりました。これらの制限に対処するため、SANAのような線形注意バックボーン向けに新しい制御可能拡散フレームワークを提案します。私たちの方法の核心は、画像、セマンティック、空間的手がかりなどの多種類条件入力を効果的に調和させつつ、トレーニング安定性を維持する双方向パイプラインで動作する統一ゲート付き条件モジュールです。複数のタスクとベンチマークにおける広範な実験は、私たちのアプローチが線形注意モデルを基盤とした制御可能生成性能で最先端を達成し、既存手法を忠実度および制御可能性において上回ることを示しています。コードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advances in diffusion-based controllable visual generation have led to remarkable improvements in image quality. However, these powerful models are typically deployed on cloud servers due to their large computational demands, raising serious concerns about user data privacy. To enable secure and efficient on-device generation, we explore in this paper controllable diffusion models built upon linear attention architectures, which offer superior scalability and efficiency, even on edge devices. Yet, our experiments reveal that existing controllable generation frameworks, such as ControlNet and OminiControl, either lack the flexibility to support multiple heterogeneous condition types or suffer from slow convergence on such linear-attention models. To address these limitations, we propose a novel controllable diffusion framework tailored for linear attention backbones like SANA. The core of our method lies in a unified gated conditioning module working in a dual-path pipeline, which effectively harmonizes multi-type conditional inputs, such as image, semantic, and spatial cues, while maintaining training stability. Extensive experiments on multiple tasks and benchmarks demonstrate that our approach achieves state-of-the-art controllable generation performance based on linear-attention models, surpassing existing methods in terms of fidelity and controllability. Codes will be available.
</details>

---

### Merge3D: Efficient 3D Multimodal LLMs Via Joint 2D-3D Token Merging
著者: Tianbo Pan, Xingyi Yang, Xinchao Wang

<details>
<summary> 日本語要旨 </summary>

マルチモーダル大規模言語モデル（MLLMs）が3次元幾何学を組み込むことで、3次元シーン理解において顕著な能力を示しています。しかし、その主要なボトルネックは、多視点の長いビジュアルトークンシーケンスを処理するための大きな計算負荷です。この課題に対処するために、我々は3次元幾何学と2次元セマンティック情報の両方を統合した幾何学的トークンマージングフレームワークである**Merge3D**を提案します。従来の2次元圧縮方法は、セマンティックシグナルに依存しているため、3次元タスクでは不十分です。これらは空間的に重要なトークンを捨てがちで、地面付けのパフォーマンスを損ないます。Merge3Dはセマンティック・ジオメトリック トークン メーカー（SemGeo Merger）によってモダリティを統合します：2次元注意がセマンティックに優位な主要トークンを選択し、ハイブリッドの2D+3D類似性が空間的に一貫した3次元近隣から文脈トークンを割り当てて集約します。これにより、積極的な圧縮下でも3次元構造の優先事項とフレーム間の対応が保持されます。Merge3Dはビジュアルトークンを最大70％削減し、約3倍の推論速度向上を達成しつつ、Scan2Cap、CV-Bench、BLINKなどの3次元地面付け、キャプショニング、空間的推論ベンチマークで強力なパフォーマンスを維持します。
</details>

<details>
<summary> 英語要旨 </summary>

Multimodal Large Language Models (MLLMs) incorporating 3D geometry demonstrate significant power in 3D scene understanding. Their primary bottleneck, however, is the substantial computational burden associated with processing multi-view, lengthy visual token sequences. To surmount this challenge, we propose \textbf{Merge3D}, a geometry-aware token merging framework that integrates both 3D geometry and 2D semantic information. Conventional 2D compression methods, which rely solely on semantic signals, prove inadequate for 3D tasks, as they tend to discard spatially critical tokens and damage grounding performance. Merge3D bridges the modalities with a Semantic–Geometric Token Merger (SemGeo Merger): 2D attention is used to select semantically salient dominant tokens, while a hybrid 2D+3D similarity assigns and aggregates contextual tokens from spatially coherent 3D neighborhoods. This preserves 3D structural priors and inter-frame correspondences under aggressive compression. Merge3D achieves up to 70\% visual token reduction and up to $\sim$3$\times$ inference speedup, while retaining strong performance on 3D grounding, captioning, and spatial reasoning benchmarks such as Scan2Cap, CV-Bench, and BLINK.
</details>

---

### SpotEdit: Selective Region Editing in Diffusion Transformers
著者: ZHIBIN QIN, Zhenxiong Tan, Zeqing Wang, Songhua Liu, Xinchao Wang

<details>
<summary> 日本語要旨 </summary>

DiT（Diffusion Transformer）ベースのモデルは、条件付き画像をエンコードしトランスフォーマー層に統合することで画像編集を大幅に進化させました。しかし、ほとんどの編集では小さな領域のみが変更される一方で、現在の方法は各ステップですべてのトークンを均等に処理しノイズ除去するため、冗長な計算と未変更領域の劣化が生じる可能性があります。これは基本的な問いを投げかけます：編集中にすべての領域を再生成することは本当に必要なのでしょうか？このため、私たちはトレーニングフリーの拡散編集フレームワークであるSpotEditを提案します。これは変更された領域のみを選択的に更新するものです。SpotEditは二つの主要なコンポーネントから構成されています：SpotSelectorは類似性を用いて安定した領域を識別し、その計算をスキップして条件付き画像特徴を再利用します；SpotFusionは動的な融合メカニズムを通じてこれらの特徴と編集されたトークンを適応的にブレンドし、文脈の一貫性と編集品質を保持します。不要な計算を削減しつつ未変更領域での高い忠実度を維持することにより、SpotEditは効率的かつ正確な画像編集を達成します。
</details>

<details>
<summary> 英語要旨 </summary>

Diffusion Transformer (DiT)-based models have significantly advanced image editing by encoding conditional images and integrating them into transformer layers. However, most edits involve modifying only small regions, while current methods uniformly process and denoise all tokens at every timestep, causing redundant computation and potentially degrading unchanged areas. This raises a fundamental question: Is it truly necessary to regenerate every region during editing? To address this, we propose SpotEdit, a training-free diffusion editing framework that selectively updates only the modified regions. SpotEdit comprises two key components: SpotSelector identifies stable regions via perceptual similarity and skips their computation by reusing conditional image features; SpotFusion adaptively blends these features with edited tokens through a dynamic fusion mechanism, preserving contextual coherence and editing quality. By reducing unnecessary computation and maintaining high fidelity in unmodified areas, SpotEdit achieves efficient and precise image editing.
</details>

---

### Beyond Soft Label: Dataset Distillation Via Orthogonal Gradient Matching
著者: Deyu Bo, Xinchao Wang

<details>
<summary> 日本語要旨 </summary>

大規模で高解像度のImageNet-1Kデータセットを縮小することは、データセット圧縮（DD）において依然として課題です。既存の方法では、実際のデータセットと合成データセット間でバッチ正規化（BN）統計量、すなわち平均値と分散を一致させます。これはソフトラベルでは効果的ですが、ハードラベルでは性能が大幅に低下します。本論文では、理論的にBNマッチングが実際のデータセットと合成データセットの勾配のスケールを整列させることに主眼を置いており、その方向性は無視されていることを特定します。しかし、実験的証拠は、モデルトレーニングにおいて勾配の方向がスケールよりも重要であることを示し、これまでの方法の限界を明らかにします。この洞察に基づき、我々は**O**rthogonal **G**radient **M**atching（OGM）を導入します。これは勾配の固有方向、すなわち特異ベクトルを明示的に整列させます。具体的には、OGMは実際のデータセットと合成データセットの勾配を正規化し、全ての特異値を1に設定してそのスケールを除去し、これらの直交した勾配間の距離を最小化することで、その特異ベクトルが一致するようにします。さらなる計算削減のため、OGMは逆伝播を避けて前向き通過時に勾配を得られる最小二乗損失を使用します。ImageNet-1Kでの広範な実験がOGMの有効性を確認しています。クラスあたり10枚の画像（IPC = 10）で、OGMはソフトラベルでは47.0％、ハードラベルでは16.7％の精度を達成し、トレーニングベースのDD方法やRDEDを上回ります。
</details>

<details>
<summary> 英語要旨 </summary>

Condensing the large-scale, high-resolution ImageNet-1K dataset remains a challenge for dataset distillation (DD). Existing methods typically match batch normalization (BN) statistics, \ie, mean and variance, between real and synthetic datasets. Although effective with soft labels, their performance degrades substantially under hard labels. In this paper, we theoretically identify that BN matching mainly aligns the scales of real and synthetic gradients but overlooks their directions. However, experimental evidence demonstrates that gradient direction, rather than scale, is pivotal to model training, clarifying the limitations of prior methods. Building on this insight, we introduce \textbf{O}rthogonal \textbf{G}radient \textbf{M}atching (OGM), which explicitly aligns the intrinsic direction of gradients, \ie, singular vectors. Specifically, OGM first orthogonalizes real and synthetic gradients by setting all singular values to one, eliminating their scales, and then minimizes the distance between these orthogonal gradients so that their singular vectors coincide. To further reduce computation, OGM employs a least-squares loss whose gradients can be obtained in the forward pass, avoiding back-propagation. Extensive experiments on ImageNet-1K validate the effectiveness of OGM. With only ten images per class (IPC = 10), OGM achieves 47.0\% accuracy with soft labels and 16.7\% with hard labels, outperforming training-based DD methods and RDED.
</details>

---

### A Unified Benchmark for HOI Evaluation Across Vision-Language Models and HOI-Specific Methods
著者: Qinqian Lei, Bo Wang, Robby T. Tan

<details>
<summary> 日本語要旨 </summary>

人間-物体インタラクション（HOI）検出は、従来、特定のタスクに対するモデルを用いて取り組まれてきましたが、CLIPのような初期のビジョン言語モデルで補強されることもあります。大規模かつ生成的なVLM（Vision-Language Model）が登場したことに伴い、スタンドアロンのVLMが効果的にHOI検出を行えるかどうか、またそれらが専門的なHOI手法と比較してどのようなものであるかという自然な疑問が生じます。既存のベンチマークであるHICO-DETは、不完全なアノテーションにおいて正確なラベル一致を依拠しており、どんな未一致の予測も誤りと数えます。これにより、特に出力が制約されていないVLMでは不当なペナルティが発生し、両者のパラダイム間で公平な比較を困難にします。この限界を解決するために、明示的に定義された正例と精選された負例を持つ多選択HOIベンチマークを導入しました。これにより、VLMとHOI特化モデルの両方を統一的かつ正確に評価することが可能になります。さらに、複数人物シーンや細部まで区別されたインタラクションのような挑戦的なシナリオに焦点を当てました。これらは両者のパラダイム間の実際の違いを明らかにする上で重要です。実験結果は、大規模VLMが競争力のある場合には優れたゼロショット性能を示すこともありますが、複数の同時行動やターゲット人物へのインタラクションの正しい割り当てに苦労することを示しています。一方で、HOI特化手法は一般的なHOI推論では弱いものの、多重行動認識やどの人物がどのアクションを実行したかのより信頼性の高い同定において優れた能力を示しています。これらの発見は、不当なペナルティによって既存ベンチマークが明らかにできないVLMとHOI特化手法の補完的な強みと弱みを浮き彫りにします。
</details>

<details>
<summary> 英語要旨 </summary>

Human-object interaction (HOI) detection has traditionally been addressed using task-specific models, sometimes augmented by early vision-language models such as CLIP. With the emergence of large, generative VLMs, a natural question arises: can standalone VLMs perform HOI detection effectively, and how do they compare to specialized HOI methods? Existing benchmarks like HICO-DET rely on exact label matching under incomplete annotations, counting any unmatched prediction as wrong. This leads to incorrect penalization, especially for VLMs whose outputs are less constrained, making fair comparison between the two paradigms difficult. To address this limitation, we introduce a multi-choice HOI benchmark with explicitly defined positives and curated negatives, enabling unified and correct evaluation of both VLMs and HOI-specific models. We further focus on challenging scenarios, such as multi-person scenes and fine-grained interaction distinctions, which are crucial for revealing real differences between the two paradigms. Experiments show that large VLMs achieve competitive, sometimes superior, zero-shot performance, yet they struggle with multiple concurrent actions and with correctly assigning interactions to the target person. Conversely, HOI-specific methods remain weaker in general HOI reasoning but demonstrate stronger multi-action recognition and more reliable identification of which person performs which action. These findings expose complementary strengths and weaknesses of VLMs and HOI-specific methods, which existing benchmarks fail to reveal due to incorrect penalization.
</details>

---

### ILRM: An Iterative Large 3D Reconstruction Model
著者: Gyeongjin Kang, Seungtae Nam, Seung kwon Yang, Xiangyu Sun, Sameh Khamis, Abdelrahman Mohamed, Eunbyung Park

<details>
<summary> 日本語要旨 </summary>

フィードフォワード3Dモデリングは、迅速かつ高品質な3D再構築の有望なアプローチとして登場しました。特に、3Dガウススプラッティングのような明示的な3D表現を直接生成することは、その高速かつ高品質なレンダリング能力から大きな注目を集めています。しかし、多くの最先端手法がトランスフォーマーアーキテクチャに基づいており、複数の入力ビューからの画像トークン全体に対する完全な注意を必要とするため、ビュー数や画像解像度が増加すると計算コストが非常に高くなるという重大なスケーラビリティの問題に直面しています。スケーラブルで効率的なフィードフォワード3D再構築を目指し、我々は反復的なLarge 3D Reconstruction Model（iLRM）を導入します。これにより、三つの核心原則に基づいて3Dガウス表現が反復的な精緻化メカニズムを通じて生成されます：(1) 3D表現と入力画像を分離してコンパクトな3D表現を可能にすること、(2) 全体のマルチビュー相互作用を二段階の注意スキームに分解して計算コストを削減すること、および (3) 高精細情報を各層で注入して高品質な再構築を達成することです。RE10KやDL3DVのような広く使用されているデータセットにおける実験結果は、iLRMが既存手法を再構築品質と速度の両方で上回っていることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Feed-forward 3D modeling has emerged as a promising approach for rapid and high-quality 3D reconstruction. In particular, directly generating explicit 3D representations, such as 3D Gaussian splatting, has attracted significant attention due to its fast and high-quality rendering. However, many state-of-the-art methods, primarily based on transformer architectures, suffer from severe scalability issues because they rely on full attention across image tokens from multiple input views, resulting in prohibitive computational costs as the number of views or image resolution increases. Toward a scalable and efficient feed-forward 3D reconstruction, we introduce an iterative Large 3D Reconstruction Model (iLRM) that generates 3D Gaussian representations through an iterative refinement mechanism, guided by three core principles: (1) decoupling the scene representation from input images to enable compact 3D representations; (2) decomposing global multi-view interactions into a two-stage attention scheme to reduce computational costs; and (3) injecting high-resolution information at every layer to achieve high-fidelity reconstruction. Experimental results on widely used datasets, such as RE10K and DL3DV, demonstrate that iLRM outperforms existing methods in both reconstruction quality and speed.
</details>

---

### Multi-view Pyramid Transformer: Look Coarser to See Broader
著者: Gyeongjin Kang, Seung kwon Yang, Seungtae Nam, Younggeun Lee, Jungwoo Kim, Eunbyung Park

<details>
<summary> 日本語要旨 </summary>

私たちは、数十から数百枚の画像から大規模な3次元シーンを単一の前方通過で直接再構築するスケーラブルなマルチビュートランスフォーマーアーキテクチャ、Multi-view Pyramid Transformer（MVP）を提案します。 「広く見て全体を捉え、細かく見て詳細を捉える」という考えに基づき、MVPは二つのコアデザイン原則に基づいて構築されています。 1) ローカルビューからグループ、最終的には全シーンまでモデルの視点を徐々に広げるローカル-グローバルなインタービュー階層、および 2) 詳細な空間表現から始めてそれらをコンパクトで情報密度の高いトークンに進行的に集約するファイン-コースなインタービュー階層です。 この二重階層は、計算効率と表現力豊かさを両立し、大規模で複雑なシーンの高速再構築を可能にします。 MVPは多様なデータセットで検証され、3Dガウススプラッティングを基礎とする3次元表現と組み合わせることで、広範囲のビュー配置において高効率性とスケーラビリティを維持しながら、汎用的な再構築品質の最先端を達成することが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

We propose Multi-view Pyramid Transformer (MVP), a scalable multi-view transformer architecture that directly reconstructs large 3D scenes from tens to hundreds of images in a single forward pass. Drawing on the idea of ``looking broader to see the whole, looking finer to see the details," MVP is built on two core design principles: 1) a local-to-global inter-view hierarchy that gradually broadens the model's perspective from local views to groups and ultimately the full scene, and 2) a fine-to-coarse intra-view hierarchy that starts from detailed spatial representations and progressively aggregates them into compact, information-dense tokens. This dual hierarchy achieves both computational efficiency and representational richness, enabling fast reconstruction of large and complex scenes. We validate MVP on diverse datasets and show that, when coupled with 3D Gaussian Splatting as the underlying 3D representation, it achieves state-of-the-art generalizable reconstruction quality while maintaining high efficiency and scalability across a wide range of view configurations.
</details>

---

### DuoMo: Dual Motion Diffusion for World-Space Human Reconstruction
著者: Yufu Wang, Evonne Ng, Soyong Shin, Rawal Khirodkar, Yuan Dong, Zhaoen Su, Jinhyung Park, Kris Kitani, Alexander Richard, Fabian Prada, Michael Zollhoefer

<details>
<summary> 日本語要旨 </summary>

私たちは、制約のないビデオからノイズや不完全な観測を伴う人間の動作を世界座標で回復する生成手法であるDuoMoを提案します。このような動作を再構築するには、多様でノイズのあるビデオ入力から一般化しつつ、全体的な動作の一貫性を維持するという基本的なトレードオフを解決する必要があります。私たちのアプローチは、2つの拡散モデルによって運動学習を因数分解することでこの問題に対処します。カメラ座標内のビデオから最初に動作を推定するカメラ空間モデルがあります。次に、世界座標へとこの初期推定値を昇格させ、全体的な一貫性を保つように洗練します。これらの2つのモデルは組み合わせることで、高度にノイズがあったり不完全な観測からでも多様なシーンや軌道を通じて動作を再構築することが可能です。さらに、私たちの形式化は一般的であり、パラメトリックモデルを迂回してメッシュ頂点の運動を直接生成します。DuoMoは最先端の性能を達成しました。EMDBにおいて、私たちの手法は世界座標でのMPJPEエラーを16%削減しつつ、低い足滑りを維持します。RICHでは、30%の世界座標でのMPJPEエラー削減を達成しています。
</details>

<details>
<summary> 英語要旨 </summary>

We present DuoMo, a generative method that recovers human motion in world-space coordinates from unconstrained videos with noisy or incomplete observations. Reconstructing such motion requires solving a fundamental trade-off: generalizing from diverse and noisy video inputs while maintaining global motion consistency. Our approach addresses this problem by factorizing motion learning into two diffusion models. The camera-space model first estimates motion from videos in camera coordinates. The world-space model then lifts this initial estimate into world coordinates and refines it to be globally consistent. Together, the two models can reconstruct motion across diverse scenes and trajectories, even from highly noisy or incomplete observations. Moreover, our formulation is general, generating the motion of mesh vertices directly (bypassing parametric models). DuoMo achieves state-of-the-art performance. On EMDB, our method obtains a 16% reduction in world-space MPJPE error while maintaining low foot skating. On RICH, it obtains a 30% reduction in world-space MPJPE error.
</details>

---

### ObjectMorpher: 3D-Aware Image Editing Via Deformable 3DGS
著者: Yuhuan Xie, Aoxuan Pan, Yihua Huang, Chirui Chang, Peng Dai, Xin Yu, Xiaojuan Qi

<details>
<summary> 日本語要旨 </summary>

画像編集における正確な、オブジェクトレベルの制御は依然として難しい課題です。2D手法は3D感覚を欠き、曖昧または非現実的な結果をもたらすことが多く、既存の3D対応アプローチは重い最適化や不完全な単眼再構成に依存しています。私たちは、ObjectMorpherという統一的でインタラクティブなフレームワークを提案します。これは曖昧な2D編集を幾何学に基づく操作に変換するものです。ObjectMorpherは、画像から3D生成器を用いてターゲットインスタンスを編集可能な3Dガウシアンスプラッティング（3DGS）へと昇華させます。これにより、アイデンティティを保持した高速な操作が可能になります。ユーザーは制御点をドラッグし、物理的に妥当な形状と姿勢の変化を保証するために、as-rigid-as-possible（ARAP）制約付きのグラフベース非剛体変形が行われます。複合拡散モジュールは照明、色彩、境界を調和させ、シームレスな再統合を実現します。多様なカテゴリーにわたり、ObjectMorpherは優れた制御性と効率性で細部まで精密かつ写実的な編集を提供し、KID、LPIPS、SIFIDおよびユーザーの好みに基づく2Dドラッグや3D対応のベースラインを上回ります。
</details>

<details>
<summary> 英語要旨 </summary>

Achieving precise, object-level control in image editing remains challenging: 2D methods lack 3D awareness and often yield ambiguous or implausible results, while existing 3D-aware approaches rely on heavy optimization or incomplete monocular reconstructions. We present ObjectMorpher, a unified, interactive framework that converts ambiguous 2D edits into geometry-grounded operations. ObjectMorpher lifts target instances with an image-to-3D generator into editable 3D Gaussian Splatting (3DGS), enabling fast, identity-preserving manipulation. Users drag control points; a graph-based non-rigid deformation with as-rigid-as-possible (ARAP) constraints ensures physically sensible shape and pose changes. A composite diffusion module harmonizes lighting, color, and boundaries for seamless reintegration. Across diverse categories, ObjectMorpher delivers fine-grained, photorealistic edits with superior controllability and efficiency, outperforming 2D drag and 3D-aware baselines on KID, LPIPS, SIFID, and user preference.
</details>

---

### Group Editing: Edit Multiple Images in One Go
著者: Yue Ma, Xinyu Wang, Qianli Ma, Qinghe Wang, Mingzhe Zheng, xiangpeng yang, Hao Li, Chongbo Zhao, Jixuan Ying, Harry Yang, Hongyu Liu, Qifeng Chen

<details>
<summary> 日本語要旨 </summary>

この論文では、関連する画像セットにわたって一貫性のある統一された修正を行う問題に取り組みます。これは特に難しい課題であり、これらの画像がポーズや視点、空間配置において大きく異なる可能性があるためです。一貫した編集を達成するためには、修正が意味的に整列された領域に正確に適用できるように、画像間の信頼性の高い対応関係を確立する必要があります。これに対処するために、私たちはGroupEditingという新しいフレームワークを提案します。このフレームワークは画像グループ内の画像間で明示的および暗黙的な関係を構築します。明示的側面では、VGGTを用いて視覚特徴に基づく空間整列を提供する幾何学的対応関係を抽出します。暗黙的側面では、画像グループを仮想動画として再構成し、事前に訓練されたビデオモデルが学習した時間的一貫性の優先順位を利用して潜在的な関係を捉えます。これら二つの種類の対応関係を効果的に融合するために、私たちはVGGTから得られる明示的幾何学的手がかりを新しい融合メカニズムを通じてビデオモデルに注入します。大規模な訓練をサポートするために、高品質のマスクと多数の画像グループ用の詳細なキャプションを含む新しいデータセットGroupEditDataを構築します。また、編集中のアイデンティティ保持を確実にするために、一貫した外見を複数の画像間で維持するモデルの能力を向上させる新しいAlignment-Enhanced RoPEモジュールを導入します。最後に、グループレベルの画像編集の効果を評価するための専用ベンチマークGroupEditBenchを提示します。広範な実験は、GroupEditingが視覚品質、クロスビューコンシステンシー、およびセマンティックアライメントの面で既存手法を大きく上回ることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

In this paper, we tackle the problem of performing consistent and unified modifications across a set of related images. This task is particularly challenging because these images may vary significantly in pose, viewpoint, and spatial layout. Achieving coherent edits requires establishing reliable correspondences across the images, so that modifications can be applied accurately to semantically aligned regions. To address this, we propose GroupEditing, a novel framework that builds both explicit and implicit relationships among images within a group. On the explicit side, we extract geometric correspondences using VGGT, which provides spatial alignment based on visual features. On the implicit side, we reformulate the image group as a pseudo-video and leverage the temporal coherence priors learned by pre-trained video models to capture latent relationships. To effectively fuse these two types of correspondences, we inject the explicit geometric cues from VGGT into the video model through a novel fusion mechanism. To support large-scale training, we construct GroupEditData, a new dataset containing high-quality masks and detailed captions for numerous image groups. Furthermore, to ensure identity preservation during editing, we introduce an alignment-enhanced RoPE module, which improves the model’s ability to maintain consistent appearance across multiple images. Finally, we present GroupEditBench, a dedicated benchmark designed to evaluate the effectiveness of group-level image editing. Extensive experiments demonstrate that GroupEditing significantly outperforms existing methods in terms of visual quality, cross-view consistency, and semantic alignment.
</details>

---

### TableMix: Enhancing Multimodal Table Reasoning in MLLMs from A Data-Centric Perspective
著者: Chaohu Liu, Shida Wang, Yubo Wang, Linli Xu

<details>
<summary> 日本語要旨 </summary>

最近のマルチモーダル大規模言語モデル（MLLMs）の進歩により、ビジュアルテーブル入力からのテーブル推論において有望な進展が見られます。これらのモデルは色やレイアウトといった豊富な視覚的手がかりを捉える能力を持っていますが、テキストのみのモデルに比べてまだ劣っています。私たちは、この主要な制限はプリトレーニング過程にあり、これが誤ってモデルの固有の推論能力を弱め、テーブル推論タスクでの強化ファインチューニングの効果を妨げると主張します。本論文では、この課題に対処するためのデータ中心的な新しいフレームワークであるTableMixを紹介します。TableMixの核となるのは原則に基づくデータ混合戦略です。具体的に、TableMixは以下の3つを組み合わせたハイブリッドデータセットを構築します：(1) マルチモーダルテーブル推論データを用いてタスク固有の推論能力を向上させる、(2) テキストのみの数学的推論データを用いてモデルの論理的な能力を復活させる、および(3) 視覚的な基盤を保持するためにシンプルなマルチモーダル知覚データ。混合データの非均一な難易度を認識し、さらにDifficulty-Aware Reward Shaping（DRS）メカニズムを提案します。これによりGroup Relative Policy Optimization（GRPO）アルゴリズムが簡潔な推論を容易な問題で適応的に報酬し、一方で複雑な問題ではより詳細な推論を奨励することが可能になり、冗長な計算やエラーを削減します。広範囲の実験結果は、TableMixがMLLMsの推論能力を顕著に向上させ、強力なマルチモーダルベースラインを大きく上回り、最先端のテキストのみのモデルとも競合することを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advances in Multimodal Large Language Models (MLLMs) have enabled promising progress in table reasoning from visual table inputs. Despite their ability to capture rich visual cues such as color and layout, MLLMs still underperform compared to text-only models. We argue that a major limitation lies in the pre-training process, which inadvertently weakens the model’s intrinsic reasoning ability and consequently hinders the effectiveness of reinforcement fine-tuning on table reasoning tasks. In this paper, we introduce TableMix, a novel framework that tackles this challenge from a data-centric perspective. At the core of TableMix is a principled data mixing strategy. Specifically, TableMix constructs a hybrid dataset that combines: (1) multimodal table reasoning data to improve task-specific reasoning, (2) text-only mathematical reasoning data to revive the model’s logical competence, and (3) simple multimodal perception data to preserve visual grounding. Recognizing the non-uniform difficulty of mixed data, we further propose a Difficulty-Aware Reward Shaping (DRS) mechanism, which enables the Group Relative Policy Optimization (GRPO) algorithm to adaptively reward concise reasoning for easy problems while encouraging more elaborate reasoning for complex ones, thereby reducing redundant computation and errors. Extensive experiments show that TableMix markedly enhances the reasoning ability of MLLMs, outperforming strong multimodal baselines and even rivaling state-of-the-art text-only models.
</details>

---

### RetFormer: Multimodal Retrieval for Enhancing Image Recognition
著者: Tianrui Yu, Xiubo Liang, Hongzhi Wang

<details>
<summary> 日本語要旨 </summary>

トランスフォーマーの拡張と高品質なマルチモーダルデータセットの収集により、深層ニューラルネットワークは視覚および言語タスクでこれまでにないパフォーマンスを達成しました。しかし、これらの進歩を実際の応用に適用することは簡単ではありません。多数のパラメータがモデル更新を複雑化させ、現実世界のデータは長尾分布やノイズのあるラベルを特徴としています。これらの問題に対処するために、私たちは単にモデルパラメータ数を増やすだけでなく、サンプル間の関係性を学習するためにニューラルネットワーク内部構造を探求することを提案します。具体的には、世界知識を格納するマルチモーダル知識ベースで強化されたRetFormerモデルを導入し、知識ベースのコンテンツを活用して堅牢なマルチモーダルサンプル関係を確立するために設計されたリトリーバルクロスフュージョンモジュールを導入します。RetFormerは、外部知識ベースからの情報をモデルの意思決定プロセスに統合することで、画像とテキストモダリティ間に堅牢な関係を確立し、従来のアプローチが直面するモデルサイズやデータセットの制約を克服します。私たちの実験は、大規模な画像テキストデータセットをビジョンタスクに統合する利点を示し、画像とテキストモダリティ間の関係性をモデル化する重要性を例証しています。私たちは長尾認識およびノイズラベルでの学習タスクにおいて、最先端の精度を達成したことを示しました。
</details>

<details>
<summary> 英語要旨 </summary>

The expansion of Transformers and the collection of high-quality multimodal datasets have propelled deep neural networks to achieve unprecedented performance in vision and language tasks. However, applying these advances is non-trivial in real-world applications. The extensive number of parameters complicates model updates, and real-world data often features a long-tailed distribution along with noisy labels. To address the above issues, we propose to explore the internal structure of the neural network for learning with sample relationships, rather than just increasing the number of model parameters. Specifically, we introduce RetFormer, a model enhanced with a multimodal knowledge base for storing world knowledge, and a retrieval cross-fusion module designed to establish robust multimodal sample relationships by leveraging content from the knowledge base. RetFormer establishes a robust relationship between image and text modalities by integrating information from external knowledge bases into the model's decision-making process, thus overcoming the limitations of traditional approaches on model size and datasets. Our experiments demonstrate the benefits of integrating large-scale image-text datasets into vision tasks and exemplify the importance of modeling the relationship between image and text modalities. We have evaluated our approach on the task of long-tailed recognition and learning with noisy labels and have shown that it achieves state-of-the-art accuracies.
</details>

---

### MoLingo: Motion–Language Alignment for Text-to-Human Motion Generation
著者: Yannan He, Garvita Tiwari, Xiaohan Zhang, Pankaj Bora, Tolga Birdal, Jan Lenssen, Gerard Pons-Moll

<details>
<summary> 日本語要旨 </summary>

私たちは、連続的な潜在空間でノイズ除去を行うことにより、リアルで生き生きとした人間の動作を生成するテキスト・トゥー・モーション（T2M）モデル「MoLingo」を紹介します。最近の研究では、潜在空間全体を一度に行うか、複数の潜在変数に対して自己回帰的に行う形で潜在空間拡散が実施されています。本研究では、連続的な動作潜在変数上の拡散を最適化する方法を探ります。具体的には、(1) 拡散をより効果的に行うための意味合いが一致した潜在空間の構築方法と、(2) 動作が記述に忠実に従うための最適なテキスト条件付けの方法を焦点にしています。私たちはフレーム単位のテキストラベルで訓練された意味合いが一致した動作エンコーダーを提案し、類似したテキスト意味を持つ潜在変数が近くに留まるようにすることで、拡散に適した潜在空間を形成します。また、シングルトークン条件付けとマルチトークンのクロスアテンション方式を比較し、クロスアテンションが動作のリアリズムとテキスト・モーションの一致性に優れていることを発見しました。意味合いが一致した潜在変数、自己回帰的生成、クロスアテンションによるテキスト条件付けを組み合わせた私たちのモデルは、標準的な評価指標とユーザー調査で人間動作生成の新しいスタンダードを確立します。コードおよびモデルを研究や下流利用のために公開する予定です。
</details>

<details>
<summary> 英語要旨 </summary>

We introduce MoLingo, a text-to-motion (T2M) model that generates realistic, lifelike human motion by denoising in a continuous latent space. Recent works perform latent space diffusion, either on the whole latent at once or auto-regressively over multiple latents. In this paper, we study how to make diffusion on continuous motion latents work best. We focus on two questions: (1) how to build a semantically aligned latent space so diffusion becomes more effective, and (2) how to best inject text conditioning so the motion follows the description closely. We propose a semantic-aligned motion encoder trained with frame-level text labels so that latents with similar text meaning stay close, which makes the latent space more diffusion-friendly. We also compare single-token conditioning with a multi-token cross-attention scheme and find that cross-attention gives better motion realism and text–motion alignment. With semantically aligned latents, auto-regressive generation, and cross-attention text conditioning, our model sets a new state of the art in human motion generation on standard metrics and in a user study. We will release our code and models for further research and downstream usage.
</details>

---

