# CVPR2026 論文要旨 (Part 1)

### In Pursuit of Pixel Supervision for Visual Pre-training
著者: Lihe Yang, Shang-Wen Li, Yang Li, Xinjie Lei, Dong Wang, Abdelrahman Mohamed, Saining Xie, Hengshuang Zhao, Kaiming He, Hu Xu

<details>
<summary> 日本語要旨 </summary>

ピクセルは、人間の帰納的バイアスを最小限に抑えながら、豊かな視覚情報を保持する軽量で拡張可能な方法で物理世界をエンコードします。私たちは、ピクセルの監督だけを使用したビジュアルプリトレーニングが望ましい視覚的特性を学習し、強力な表現を生成できることを示します。これはシンプルで安定して効率的です。私たちは「ピクソ」という名前の有能な自己監督モデルを紹介し、それは単にピクセルを予測することでトレーニングされます。これはマスク付きオートエンコーディング（MAE）フレームワーク上に構築されていますが、より深いデコーダー、大規模ブロックのマスキング、追加のクラストークンを導入することでMAEを強化しています。ピクソは自己カリキュレーション戦略によって2Bのウェブクロール画像でトレーニングされています。ピクソは、単眼深度推定（例：Depth Anything）、フィードフォワード3D再構成（すなわちMapAnything）、オブジェクトセグメンテーション（例：SAM 2）、エンバデッドAIを含む多くの下流タスクで優れた性能を発揮します。私たちはトレーニングコードと予め学習されたモデルを公開する予定です。
</details>

<details>
<summary> 英語要旨 </summary>

Pixels provide a lightweight, scalable way to encode the physical world, preserving rich visual information with minimal human inductive bias. We demonstrate that visual pre-training using pixel supervision alone can learn desirable visual properties and produce strong representations, while remaining simple, stable, and efficient. We present Pixo, a capable self-supervised model trained by purely predicting pixels. It is instantiated on the masked autoencoding (MAE) framework, but enhances MAE with a deeper decoder, larger-block masking, and additional class tokens. It is trained on 2B web-crawled images with a self-curated strategy. Pixo performs well on many downstream tasks, covering monocular depth estimation (e.g., Depth Anything), feed-forward 3D reconstruction (i.e., MapAnything), object segmentation (e.g., SAM 2), and embodied AI. We will release the training code and pre-trained models.
</details>

---

### ARCache: Mitigating Error Accumulation for Caching-based Acceleration in Autoregressive Video Diffusion Models
著者: Kepan Nan, Wangbo Zhao, Penghao Zhou, Jun Li, Zhenheng Yang, Jian Yang, Ying Tai

<details>
<summary> 日本語要旨 </summary>

最近、ディフュージョンモデルを用いた効率的なビデオ生成において、キャッシングベースの加速方法が大きな進歩をもたらしています。しかし、これらの加速技術を直接自己回帰型ビデオディフュージョンモデルに適用するという重要な制限点があります。このようなモデルは、歴史的コンテキストに条件付けられたセグメントを順次合成して長いビデオを生成します。この設定では、加速によって導入される近似誤差が時間と共に伝播し蓄積する傾向があり、これにより重大なエラーの蓄積とビデオ品質の進行的劣化が生じます。この課題に対処するために、私たちは自己回帰型ビデオディフュージョンモデル向けに特別に設計された初のトレーニング不要キャッシングベース加速フレームワークであるARCacheを提案します。ARCacheは、2つの主要なコンポーネントを通じてキャッシングのタイミングと品質を向上させます。まず、歴史情報を活用して各セグメントごとに適応的にキャッシュスケジューリングを行うことでより正確かつ効率的なキャッシュ利用を可能にする歴史ガイド付きキャッシュ（HGC）があります。次に、モデル残差を適応的に近似し、後続のセグメントのための残差軌道を洗練することでエラーの蓄積を効果的に抑制しつつ同時に計算オーバーヘッドを削減する強化された残差補正（ERC）があります。Framepack-F1、SkyReels-V2、および自己回帰型ワールドモデルMatrix-Gameに関する広範な実験では、ARCacheが最先端の加速と視覚的忠実度を達成していることが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

Caching-based acceleration methods have recently driven significant progress in efficient video generation with diffusion models. However, we identify a critical limitation when directly applying these acceleration techniques to autoregressive video diffusion models, which generate long videos by sequentially synthesizing segments conditioned on historical context. In such settings, any approximation errors introduced by acceleration tend to propagate and accumulate over time, resulting in severe error accumulation and progressive degradation of video quality. To address this challenge, we propose ARCache, the first training-free caching-based acceleration framework specifically designed for autoregressive video diffusion models. ARCache improves both the timing and quality of caching through two key components. First, History-Guided Cache (HGC) leverages historical information to adaptively schedule caching for each segment, enabling more accurate and efficient cache utilization. Second, Enhanced Residual Correction (ERC) adaptively approximates model residuals and refines the residual trajectory for subsequent segments, effectively mitigating error accumulation while simultaneously reducing computational overhead. Extensive experiments on Framepack-F1, SkyReels-V2, and autoregressive world model Matrix-Game demonstrate that ARCache achieves state-of-the-art acceleration and visual fidelity.
</details>

---

### Native and Compact Structured Latents for 3D Generation
著者: Jianfeng XIANG, Xiaoxue Chen, Sicheng Xu, Ruicheng Wang, Zelong Lv, Yu Deng, Hongyuan Zhu, Yue Dong, Hao Zhao, Nicholas Jing Yuan, Jiaolong Yang

<details>
<summary> 日本語要旨 </summary>

最近の3次元生成モデリングにおける進歩は、生成されたリアリズムを大幅に向上させましたが、複雑なトポロジーや詳細な外観を捉えることに苦労する既存の表現によって依然として制限されています。本論文では、この課題に対処するためにネイティブ3Dデータから構造化された潜在的な表現を学習するアプローチを提示します。その核となるのは、幾何学と外観の両方をエンコードする新しいスパースボクセル構造であるO-Voxel（オムニ-ボクセル表現）です。O-Voxelは、開放型、非マニフォールド、完全に閉じた表面を含む任意のトポロジーを堅牢にモデリングできるだけでなく、テクスチャカラーを超えた包括的な表面属性（物理ベースレンダリングパラメータなど）も捉えます。O-Voxelに基づいて、高い空間圧縮率とコンパクトな潜在空間を提供するスパース圧縮VAEを設計しました。さらに、多様な公開3Dアセットデータセットを使用して、3次元生成のための4Bパラメータを含む大規模フローマッチングモデルをトレーニングしました。そのスケールにもかかわらず、推論は非常に効率的です。一方で、私たちが生成したアセットの幾何学と材質の品質は既存モデルを大きく上回っています。私たちは、このアプローチが3次元生成モデリングにおける重要な進歩であると考えています。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advancements in 3D generative modeling have significantly improved the generation realism, yet the field is still hampered by existing representations, which struggle to capture assets with complex topologies and detailed appearance. This paper present an approach for learning a structured latent representation from native 3D data to address this challenge. At its core is a new sparse voxel structure called O-Voxel, an omni-voxel representation that encodes both geometry and appearance. O-Voxel can robustly model arbitrary topology, including open, non-manifold, and fully-enclosed surfaces, while capturing comprehensive surface attributes beyond texture color, such as physically-based rendering parameters. Based on O-Voxel, we design a Sparse Compression VAE which provides a high spatial compression rate and a compact latent space. We train large-scale flow-matching models comprising 4B parameters for 3D generation using diverse public 3D asset datasets. Despite their scale, inference remains highly efficient. Meanwhile, the geometry and material quality of our generated assets far exceed those of existing models. We believe our approach offers a significant advancement in 3D generative modeling.
</details>

---

### Building A Precise Video Language with Human–AI Oversight
著者: Zhiqiu Lin, Siyuan Cen, Chancharik Mitra, Isaac Li, Yuhan Huang, Yu Ling, Hewei Wang, Irene Pi, Shihang Zhu, Yili Han, Yilun Du, Deva Ramanan

<details>
<summary> 日本語要旨 </summary>

ビデオ・ランゲージモデル（VLMs）は自然言語を通じて動的な視覚世界について推論することを学びます。私たちは、正確なビデオキャプションのためのスケーラブルな監督を可能にするオープンデータセット、ベンチマーク、レシピの一連を導入します。まず、映画製作者などのプロフェッショナルビデオクリエイターと共に開発された慎重に定義された視覚原理数百個をサポートする主題、シーン、動き、空間、カメラダイナミクスの記述のための構造化仕様を定義します。次に、高品質なキャプションを編集するために、訓練された人間専門家がモデル生成のプリキャプションを改善したポストキャプションに修正的批評を提供する人間・AI（CHAI）監督フレームワークを導入します。この労働分担は、テキスト生成をモデルにオフロードし、人々が検証により良く集中できることで、注釈の精度と効率を向上させます。また、プリキャプションとポストキャプション間の批評と好みは、キャプション生成、報酬モデリング、批評生成におけるオープンソースモデル（Qwen3-VL）の微調整を改善するための豊富な監督を提供します。これは標準SFT、オフラインRL（DPO）、オンラインRL（GSPO）、および推論時スケーリングを通じて行われます。控えめな専門家の監督にもかかわらず、結果として得られるシステムは、Gemini-2.5-Proのようなクローズドソースモデルを凌駕します。最後に、私たちのアプローチを大規模なプロフェッショナルビデオ（例えば映画、コマーシャル、ゲーム）の再キャプションとビデオ生成モデル（Wan）の微調整に適用し、400語以上の詳細なプロンプトに従うことをより良くするために、カメラ動き、角度、レンズ、視点、ショット構成に対するより細かい制御を達成します。全体的に、私たちの結果は、プロフェッショナルレベルのビデオ理解と生成を達成するために、正確な仕様と人間・AI監督が重要であることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Video–language models (VLMs) learn to reason about the dynamic visual world through natural language. We introduce a suite of open datasets, benchmarks, and recipes for scalable oversight that enable precise video captioning. First, we define a structured specification for describing subjects, scenes, motion, spatial, and camera dynamics, supported by hundreds of carefully defined visual primitives developed with professional video creators such as filmmakers. Next, to curate high-quality captions, we introduce a critique-based human–AI (CHAI) oversight framework, where trained human experts provide correctional critiques to revise model-generated pre-captions into improved post-captions. This division of labor improves annotation accuracy and efficiency by offloading text generation to models, allowing humans to better focus on verification. Additionally, these critiques and preferences between pre- and post-captions provide rich supervision for fine-tuning, improving open-source models (Qwen3-VL) on caption generation, reward modeling, and critique generation through standard SFT, offline RL (DPO), online RL (GSPO), and inference-time scaling. With modest expert supervision, the resulting system outperforms even closed-source models such as Gemini-2.5-Pro. Finally, we apply our approach to re-caption large-scale professional videos (e.g., films, commercials, games) and fine-tune video generation models such as Wan to better follow detailed prompts of over 400 words, achieving finer control over camera motion, angle, lens, perspectives, and shot composition. Overall, our results show that precise specification and human–AI oversight are key to achieving professional-level video understanding and generation.
</details>

---

### Omni-Attribute: Open-vocabulary Image Attribute Encoder for Visual Disentanglement and Composition
著者: Tsai-Shien Chen, Aliaksandr Siarohin, Guocheng Qian, Kuan-Chieh Wang, Egor Nemchinov, Moayed Haji Ali, Riza Alp Guler, Willi Menapace, Ivan Skorokhodov, Anil Kag, Jun-Yan Zhu, Sergey Tulyakov

<details>
<summary> 日本語要旨 </summary>

視覚的概念の個別化は、アイデンティティ、表情、照明、スタイルなど特定の画像属性を未見のコンテキストに転送することを目指しています。しかし、既存の方法は一般的な画像エンコーダーから得られる全体的な埋め込みに依存しており、これによって多くの視覚要因が絡み合い、単一の属性を分離することが困難になります。このため、情報漏洩や不整合な合成が生じることがあります。この制限に対処するために、私たちはオムニ・アトリビュートを導入します。これは、高品質で属性特化された表現を学習するための初のオープンボキャブラリー画像属性エンコーダーです。私たちのアプローチではデータとモデルを共同設計しています：（i）肯定的および否定的な属性で注釈付きの意味的にリンクされた画像ペアをキュレートし、エンコーダーが何を保持または抑制するかを明示的に教えます；（ii）生成精度と対照的な分離のバランスを取る二重目標トレーニングパラダイムを採用します。結果として得られた埋め込みは、オープンボキャブラリー属性検索、個別化、および合成生成に効果的であり、複数のベンチマークで最先端の性能を達成しています。
</details>

<details>
<summary> 英語要旨 </summary>

Visual concept personalization aims to transfer only specific image attributes, such as identity, expression, lighting, and style, into unseen contexts. However, existing methods rely on holistic embeddings from general-purpose image encoders, which entangle multiple visual factors and make it difficult to isolate a single attribute. This often leads to information leakage and incoherent synthesis. To address this limitation, we introduce Omni-Attribute, the first open-vocabulary image attribute encoder designed to learn high-fidelity, attribute-specific representations. Our approach jointly designs the data and model: (i) we curate semantically linked image pairs annotated with positive and negative attributes to explicitly teach the encoder what to preserve or suppress; and (ii) we adopt a dual-objective training paradigm that balances generative fidelity with contrastive disentanglement. The resulting embeddings prove effective for open-vocabulary attribute retrieval, personalization, and compositional generation, achieving state-of-the-art performance across multiple benchmarks.
</details>

---

### FRM: Linear-Time 3D Reconstruction Via Test-Time Training
著者: Haian Jin, Rundi Wu, Tianyuan Zhang, Ruiqi Gao, Jonathan T. Barron, Noah Snavely, Aleksander Holynski

<details>
<summary> 日本語要旨 </summary>

フィードフォワードトランスフォーマーモデルであるVGGTや$\pi^3$は高精度ですが、入力画像の数に対して計算コストが二次的に増加するため、大規模なコレクション上では評価が遅くなります。より効率的なアプローチはこのコストを軽減しますが、再構成品質の犠牲と引き換えに行います。私たちはFast Reconstruction Model（FRM）を導入しました。これは入力ビュー数に対して線形スケールする双方向アーキテクチャを持つ、状態保持型のフィードフォワード再構成モデルであり、二次時間法と同等またはそれ以上の再構成品質を達成します。FRMはテスト時トレーニング層を使用して画像を単一のフォワードパス中にコンパクトな隠れシーン状態に圧縮し、これにより私たちのモデルはシングルH100 GPU上で3Dシーンを最大75 FPSの速度で再構成することが可能です。これはVGGTなどのSOTA方法よりも20倍以上高速です。この隠れ状態はまた、リアルタイムレートでクエリを行うことによって新規ビューからカラーポイントマップを生成するための暗黙的なシーン表現としても機能します。
</details>

<details>
<summary> 英語要旨 </summary>

Feed-forward transformer models such as VGGT and $\pi^3$ are highly accurate, but their computational cost grows quadratically with the number of input images, making them slow to evaluate on large collections. More efficient approaches ameliorate this cost at the expense of reconstruction quality. We introduce Fast Reconstruction Model, a stateful feed-forward reconstruction model that uses a bidirectional architecture that scales linearly in the number of input views, while matching or surpassing the reconstruction quality of quadratic-time methods. FRM employs test-time training layers to compress images into a compact hidden scene state during a single forward pass, enabling our model to reconstruct 3D scenes at speeds up to 75 FPS on a single H100 GPU---over 20 times faster than SOTA methods such as VGGT. This hidden state also serves as an implicit scene representation which can be queried at real-time rates to produce colored point maps from novel views.
</details>

---

### Cross-View Splatter: Feed-Forward View Synthesis with Georeferenced Images
著者: Matias Turkulainen, Akshay Krishnan, Filippo Aleotti, Mohamed Sayed, Guillermo Garcia-Hernando, Juho Kannala, Arno Solin, Gabriel Brostow, Daniyar Turmukhambetov

<details>
<summary> 日本語要旨 </summary>

私たちは、地上レベルおよび衛星から撮影された屋外シーンに対してピクセルアラインメントされたガウススプラッタを予測するフィードフォワード手法である「Cross-View Splatter」を紹介します。忠実な再構成には良好なカメラカバレッジが必要ですが、地上画像の取得は大規模な屋外シーンでは時間がかかり難しいです。幸いにも、衛星画像は公共APIを通じて容易にアクセスできるグローバルな幾何学的事前情報を提供します。「Cross-View Splatter」はGPSタグ付きの地上写真と正射校正された衛星ビューを統一した3D座標フレームでガウススプラッタを予測することにより融合します。地上および鳥瞰視点の特徴表現を整列させることで、私たちのモデルは単体の地上画像に比べてシーンカバレッジと新しいビューシンセシスが向上します。我々は公開マッピングサービスから採取したペアリングされた衛星・地形データを用い、キュレーションされたジオリファレンス済みのデータセットでトレーニングします。
</details>

<details>
<summary> 英語要旨 </summary>

We present Cross-View Splatter, a feed-forward method that predicts pixel-aligned Gaussian splats for outdoor scenes captured at ground-level AND by satellite. Faithful reconstructions require good camera coverage, but ground imagery is time-consuming and hard to capture at scale for large outdoor scenes. Fortunately, satellite imagery can provide a global geometric prior that is easy to access via public APIs. Cross-View Splatter fuses orthorectified satellite views with GPS-tagged ground photos to predict Gaussian splats in a unified 3D coordinate frame. By aligning ground and bird's-eye feature representations, our model improves scene coverage and novel-view synthesis, compared to ground imagery alone. We train on curated georeferenced data sets and paired satellite--terrain data, mined from open mapping services.
</details>

---

### Towards Hierarchical 3D Spatial Understanding in Vision-Language Models
著者: Huizhi Liang, Yichao Shen, Yu Deng, Sicheng Xu, ZhiYuan Feng, Tong Zhang, Yaobo Liang, Jiaolong Yang

<details>
<summary> 日本語要旨 </summary>

ビジョン言語モデル（VLM）における人間のような空間知性を達成するためには、2次元観測から3次元構造を推論し、3次元空間でのオブジェクトの特性や関係を認識し、高度な空間的推理を行う必要があります。本研究では、VLMにおける3次元空間理解の学習を四つの段階に分解する原則に基づいた階層的フレームワークを提案します。これらは幾何学的知覚から抽象的な空間推理まで、徐々に複雑さが増すものです。このフレームワークに基づき、多様なタスクやシーンをまたいだ1億以上の3次元空間VQAペアを生成する自動化されたパイプラインを構築しました。これらはVLMの微調整に使用されます。さらに、メトリックスケールの点群マップを補助入力として取り込むRGB-D VLMも開発し、空間理解を強化しました。広範な実験により、私たちのアプローチが複数の空間理解および推理ベンチマークで最先端の性能を達成していることが示されました。これは専門的な空間モデルや大規模プロプライエタリシステム（Gemini-2.5-pro、GPT-5）をも上回っています。さらに、私たちの分析では階層的タスクレベル間の明確な依存関係が示され、多段階タスク設計が将来のVLMにおける3次元空間知性の発現をどのように促進するかについて新たな洞察を提供しています。
</details>

<details>
<summary> 英語要旨 </summary>

Achieving human-like spatial intelligence for vision-language models (VLMs) requires inferring 3D structures from 2D observations, recognizing object properties and relations in 3D space, and performing high-level spatial reasoning. In this paper, we propose a principled hierarchical framework that decomposes the learning of 3D spatial understanding in VLMs into four progressively complex stages, from geometric perception to abstract spatial reasoning. Guided by this framework, we construct an automated pipeline that generates over 1 billion 3D spatial VQA pairs across diverse tasks and scenes for VLM supervised finetuning. We also develop an RGB-D VLM that incorporates metric-scale point maps as auxiliary inputs to further enhance spatial understanding. Extensive experiments demonstrate that our approach achieves state-of-the-art performance on multiple spatial understanding and reasoning benchmarks, surpassing specialized spatial models and large proprietary systems such as Gemini-2.5-pro and GPT-5. Moreover, our analysis reveals clear dependencies among hierarchical task levels, offering new insights into how multi-level task design facilitates the emergence of 3D spatial intelligence in future VLMs.
</details>

---

### Improved Mean Flows: On The Challenges of Fastforward Generative Models
著者: ZHENGYANG GENG, Yiyang Lu, Zongze Wu, Eli Shechtman, Zico Kolter, Kaiming He

<details>
<summary> 日本語要旨 </summary>

MeanFlowは、高速進行生成モデリングのための原理に基づいたフレームワークを提供します。しかし、元々のMeanFlowにはトレーニング目的およびガイダンスの両方で重要な制限があります。まず、元々のMeanFlow予測はノイズ状態だけでなく、明示的にノイズとデータにも依存しており、トレーニングターゲットがネットワークと共にずれてしまいます。これを速度予測として再定式化し、ノイズ状態からのみ即時速度を予測することで回帰問題に還元します。次に、ガイダンス側では、元々のMeanFlowはトレーニング中に直接学習されたガイドフィールドを固定し、1-NFEサンプリングを達成していますが、推論時のガイダンス調整の柔軟性を失っています。代わりに、モデルをガイダンススケールで条件付け、さまざまなガイダンススケールでトレーニングすることで、推論時の拡散/流れモデルにおける柔軟なガイダンスを可能にしつつ、一段階サンプリングを維持します。ImageNet 256×256では、私たちの改良されたMeanFlow（iMF）は118Mパラメータのモデルで1ステップFIDが2.74に達し、最大のモデルはさらに1ステップFIDを1.72まで押し上げ、一段階生成モデリングにおける新たな最先端を確立しています。
</details>

<details>
<summary> 英語要旨 </summary>

MeanFlow provides a principled framework for fastforward generative modeling. However, the original MeanFlow has key limitations in both the training objective and the guidance. First, the original MeanFlow prediction depends not only on the noisy state but also explicitly on the noise and data, causing the training target to drift with the network. We reformulate it as velocity prediction, predicting the instantaneous velocity solely from the noisy state and reducing it to the regression problem. Second, on the guidance side, the original MeanFlow fixes the guidance scale during training by directly learning a guided field, achieving 1-NFE sampling but losing the flexibility to adjust the guidance at inference. Instead, we condition the model on guidance scale and train it on a range of guidance scales, enabling flexible guidance as diffusion/flow models in inference while preserving one-step sampling. On ImageNet 256$\times$256, our improved MeanFlow (iMF) achieves a 1-step FID of 2.74 with a model of 118M parameters, and our largest model further pushes the 1-step FID to 1.72, establishing a new state of the art for one-step generative modeling.
</details>

---

### Visual Sim-to-Real at Scale for Humanoid Loco-Manipulation
著者: Tairan He, Zi Wang, Haoru Xue, Qingwei Ben, Zhengyi Luo, Wenli Xiao, Ye Yuan, Xingye Da, Fernando Castañeda, Shankar Sastry, Changliu Liu, Guanya Shi, Linxi Fan, Yuke Zhu

<details>
<summary> 日本語要旨 </summary>

ヒューマノイドロボットの実世界での生産性における主要な障壁は、自律的な移動操作スキルの欠如です。私たちはVIRALという視覚シム・トゥ・リアルフレームワークを紹介します。これにより、完全にシミュレーション内で学習されたヒューマノイドの移動操作が、実際のハードウェアへゼロショットで展開されます。VIRALは教師-生徒設計に従います：特権を持つRL教師が完全な状態で動作し、デルタアクション空間と参照状態初期化を使用して長期的な移動操作を学習します。その後、大規模シミュレーションによるタイリングレンダリングで教師からビジョンベースの生徒ポリシーが蒸留され、オンラインDAggerと行動クローニングを混合してトレーニングされます。計算スケールが重要であることがわかりました：シミュレーションを数十のGPU（最大64）に拡張することで、教師および生徒のトレーニングが信頼性を持つ一方で、低計算環境ではしばしば失敗します。シム・トゥ・リアルのギャップを埋めるために、VIRALは大規模な視覚ドメインランダマイズ（照明、材質、カメラパラメータ、画像品質、センサー遅延）と実際のハンドおよびカメラをシムに合わせることを組み合わせています。Unitree G1ヒューマノイドで展開された結果、得られたRGBベースポリシーは、最大54サイクルの連続移動操作を実行し、任意の現実世界の微調整なしに多様な空間および外観変化に一般化し、専門家レベルのテレオペレーションパフォーマンスに近づきます。広範なアブレーションが実際に機能するRGBベースのヒューマノイド移動操作を可能にするために必要な主要な設計選択を解剖します。
</details>

<details>
<summary> 英語要旨 </summary>

A core barrier to the real-world productivity of humanoid robots is the lack of autonomous loco-manipulation skills. We introduce VIRAL, a visual sim-to-real framework that learns humanoid loco-manipulation entirely in simulation and deploys it zero-shot to real hardware. VIRAL follows a teacher-student design: a privileged RL teacher, operating on full state, learns long-horizon loco-manipulation using a delta action space and reference state initialization. A vision-based student policy is then distilled from the teacher via large-scale simulation with tiled rendering, trained with a mixture of online DAgger and behavior cloning. We find that compute scale is critical: scaling simulation to tens of GPUs (up to 64) makes both teacher and student training reliable, while low-compute regimes often fail. To bridge the sim-to-real gap, VIRAL combines large-scale visual domain randomization—over lighting, materials, camera parameters, image quality, and sensor delays—with real-to-sim alignment of the dexterous hand and cameras. Deployed on a Unitree G1 humanoid, the resulting RGB-based policy performs continuous loco-manipulation for up to 54 cycles, generalizing to diverse spatial and appearance variations without any real-world fine-tuning, and approaching expert-level teleoperation performance. Extensive ablations dissect the key design choices required to make RGB-based humanoid loco-manipulation work in practice.
</details>

---

### Open-Med-Reasoner: Data Recipes for Multimodal Medical Reasoning
著者: Timothy Ossowski, Sheng Zhang, Qianchu Liu, Guanghui Qin, Reuben Tan, Tristan Naumann, Junjie Hu, Hoifung Poon

<details>
<summary> 日本語要旨 </summary>

医療分野における大規模言語モデルのトレーニングには、高品質で慎重にキュレーションされたデータが基盤となります。これは一般化能力や未知の臨床タスクへの堅牢性に直接影響します。本研究では、医療分野での強固なマルチモーダル推論モデルを開発するためのトレーニング戦略とデータキュレーションについて調査します。私たちの研究は監督付き微調整（SFT）に焦点を当て、構造化された推論トレースを活用するデータレシピを探求しています。提案したデータレシピを使用し、8,000万以上の例と6.8兆の応答トークンを含むデータセットでスケール実験を行い、オープンソースモデルにおける多様な外部分布医療ベンチマークタスクで最先端の性能を達成しました。結果はさらに、トレーニングデータセットが高品質かつ多様であり、異なる長さの構造化された推論トレースを含むことで、微調整されたモデルが下流タスクに基づいてその推論経路の長さを自己キャリブレーションすることが可能であることを示しています。これは明示的な監督なしで行われます。私たちは重要な洞察を提示し、データキュレーション戦略を説明し、医療ビジョン言語推論システムの開発に向けた次のステップを概説します。
</details>

<details>
<summary> 英語要旨 </summary>

High-quality and carefully curated data is a cornerstone of training medical large language models, as it directly impacts both generalization and robustness to unseen clinical tasks. We investigate strategies for training and data curation to develop a robust multimodal reasoning model in the medical domain. Our work focuses on supervised fine-tuning (SFT) and explores data recipes that leverage structured reasoning traces. Using our proposed data recipe, we scale experiments to a dataset of over 8 million examples and 6.8 billion response tokens, achieving state-of-the-art performance among open-source models across diverse out-of-distribution medical benchmark tasks. Our results further indicate that curating a high-quality, diverse training dataset with varying structured reasoning trace lengths enables the fine-tuned model to self-calibrate its reasoning trajectory lengths based on the downstream task, without explicit supervision. We present key insights, describe the data curation strategy, and outline next steps toward developing robust medical vision-language reasoning systems.
</details>

---

### Masked-Diffusion Autoencoders for 3D Medical Vision Representation Learning
著者: Jiachen Tu, Guanghui Qin, Theodore Zhao, Jeya Maria Jose Valanarasu, Sheng Zhang, Tristan Naumann, Fan Lam, Sheng Wang, Hoifung Poon

<details>
<summary> 日本語要旨 </summary>

効果的な医用画像解析には、全体の解剖学的構造と微細な組織テクスチャを捉える表現が必要です。現在の自己教師ありアプローチは、これら両方の要件に同時に対応する能力が限定されています。不変性ベースの方法は、増強一貫性を通じて学習しますが、医用画像では共通の増強が診断的に関連する強度パターンを失う可能性があるため、課題に直面しています。マスク付き画像モデリングアプローチは高いマスキング比率を用いて全体的な推論を強制しますが、本質的に微細なテクスチャへの露出を限定してしまいます。一般ドメインビジョンにおける最近の研究では、生成と意味論的目標が相互に利益をもたらすことが示されていますが、このパラダイムは3D医用画像について未探索のままです。私たちはマスク付き拡散オートエンコーダー（MDAE）を導入します。これは空間的なマスキングと拡散汚染を同時に課す自己教師ありフレームワークで、モデルが補完的な目標を学習するよう促します：マスクされた領域の再構築による構造的一貫性と可視領域のノイズ除去によるテクスチャ特性。この二重汚染は、統一された時間条件付き目標内で構造-テクスチャ表現を学習することを可能にします。脳MRIにおいて腫瘍分類、分子マーカー検出、密なセグメンテーションベンチマークで評価した結果、MDAEは常に最先端のベースラインを上回り、特にクロスモーダル一般化タスクで改善が顕著です。
</details>

<details>
<summary> 英語要旨 </summary>

Effective medical image analysis requires representations that capture both global anatomical structure and fine-grained tissue texture. Current self-supervised approaches exhibit limited capacity to address both requirements simultaneously. Invariance-based methods learn through augmentation consistency but face challenges in medical imaging where common augmentations may discard diagnostically relevant intensity patterns. Masked image modeling approaches employ high masking ratios to enforce holistic reasoning, yet inherently limit exposure to fine-grained texture. Recent work in general-domain vision demonstrates that generative and semantic objectives can mutually benefit each other, yet this paradigm remains unexplored for 3D medical imaging. We introduce Masked-Diffusion Autoencoders (MDAE), a self-supervised framework that imposes concurrent spatial masking and diffusion corruption, encouraging the model to learn complementary objectives: masked region reconstruction for structural coherence and visible region denoising for textural characteristics. This dual corruption enables the network to learn structure-texture representations within a unified time-conditioned objective. Evaluated on brain MRI across tumor classification, molecular marker detection, and dense segmentation benchmarks, MDAE consistently outperforms state-of-the-art baselines, with improvements most pronounced in cross-modal generalization tasks.
</details>

---

### 4D-RGPT: Toward Region-level 4D Understanding Via Perceptual Distillation
著者: Chiao-An Yang, Ryo Hachiuma, Sifei Liu, Subhashree Radhakrishnan, Raymond A. Yeh, Yu-Chiang Frank Wang, Min-Hung Chen

<details>
<summary> 日本語要旨 </summary>

多モーダルLLM（MLLMs）の進歩にもかかわらず、3次元構造や時間的ダイナミクスを理解する能力は依然として限定されており、弱い4D知覚と時間的理解によって制約されています。既存の3Dおよび4Dビデオ質問応答（VQA）ベンチマークも静的なシーンを強調し、領域レベルのプロンプトが不足しています。これらの問題に対処するために、次のような取り組みを行いました：(a) 4D-RGPT、ビデオ入力から強化された時間的知覚で4D表現を捉えることができる特化したMLLM；(b) 感覚4D蒸留（P4D）、凍結した専門モデルから4D-RGPTへの4D表現の移行を可能にするトレーニングフレームワークで、包括的な4D知覚が実現されます；そして(c) \ourbenchmark、領域レベルプロンプト付きの深度認識動的シーン用にハイブリッド自動化と人間検証パイプラインを使用して構築されたベンチマーク。私たちの4D-RGPTは、既存の4D VQAベンチマークおよび提案されたR4D-Benchベンチマークの両方で顕著な改善を達成しました。
</details>

<details>
<summary> 英語要旨 </summary>

Despite advances in Multimodal LLMs (MLLMs), their ability to reason over 3D structures and temporal dynamics remains limited, constrained by weak 4D perception and temporal understanding. Existing 3D and 4D Video Question Answering (VQA) benchmarks also emphasize static scenes and lack region-level prompting. We tackle these issues by introducing:(a) 4D-RGPT, a specialized MLLM designed to capture 4D representations from video inputs with enhanced temporal perception;(b) Perceptual 4D Distillation (P4D), a training framework that transfers 4D representations from a frozen expert model into 4D-RGPT for comprehensive 4D perception; and(c) \ourbenchmark, a benchmark for depth-aware dynamic scenes with region-level prompting, built via a hybrid automated and human-verified pipeline. Our 4D-RGPT achieves notable improvements on both existing 4D VQA benchmarks and the proposed R4D-Bench benchmark.
</details>

---

### Monet: Reasoning in Latent Visual Space Beyond Image and Language
著者: Qixun Wang, Yang Shi, Yifei Wang, Yuanxing Zhang, Pengfei Wan, Kun Gai, Xianghua Ying, Yisen Wang

<details>
<summary> 日本語要旨 </summary>

画像を用いた思考が、テキストのみに依存する推論チェーンを超えて視覚的証拠を中間ステップに組み込むことで、視覚的推論の進展に効果的なパラダイムとして浮上しています。しかし、既存の方法は人間のような抽象的な視覚思考を実現することができず、その柔軟性は外部ツールに基本的に制限されています。この研究では、Monetというトレーニングフレームワークを導入し、これにより多様な言語モデル（MLLMs）が中間視覚思考として機能する連続的埋め込みを生成することで、直接的に潜在的な視覚空間内で推論を行うことが可能になります。MLLMsの潜在的な視覚推論トレーニングにおける二つの核心的課題—潜在–視覚整合の高い計算コストと、潜在埋め込みへの不十分な監督—を三段階の教師あり微調整（SFT）パイプラインに基づく蒸留ベースで解決します。また、GRPOが潜在的推論に適用される限界を明らかにしました：それは主にテキストベースの推論を強化するものであり、潜在的推論ではないということです。この問題を克服するために、私たちはVLPO（Visual-latent Policy Optimization）を提案します。これは、潜在埋め込みを明示的にポリシーグラディエント更新に組み込む強化学習手法です。SFTをサポートするために、私たちはMonet-SFT-125Kという高品質なテキスト–画像インターレイドのCoTデータセットを構築しました。このデータセットは、実世界、チャート、OCR、幾何学的な125,000件のCoTsを含んでいます。私たちのモデルMonet-7Bは、リアルワールドの知覚と推論評価基準において一貫した向上を示し、抽象的な視覚推論タスクでの厳しい外挿一般化能力も強調しています。また、各トレーニングコンポーネントの役割を実証分析し、初期の失敗した試みについて議論することで、将来の視覚潜在推論開発への洞察を提供しています。
</details>

<details>
<summary> 英語要旨 </summary>

Thinking with images has emerged as an effective paradigm for advancing visual reasoning, extending beyond text-only chains of thought by injecting visual evidence into intermediate reasoning steps. However, existing methods fall short of human-like abstract visual thinking, as their flexibility is fundamentally limited by external tools. In this work, we introduce Monet, a training framework that enables multimodal large language models (MLLMs) to reason directly within the latent visual space by generating continuous embeddings that function as intermediate visual thoughts. We identify two core challenges in training MLLMs for latent visual reasoning—high computational cost in latent–vision alignment and insufficient supervision over latent embeddings, and address them with a three-stage distillation-based supervised fine-tuning (SFT) pipeline. We further reveal a limitation of applying GRPO to latent reasoning: it primarily enhances text-based reasoning rather than latent reasoning. To overcome this, we propose VLPO (Visual-latent Policy Optimization), a reinforcement learning method that explicitly incorporates latent embeddings into policy gradient updates. To support SFT, we construct Monet-SFT-125K, a high-quality text–image interleaved CoT dataset containing 125K real-world, chart, OCR, and geometry CoTs. Our model, Monet-7B, shows consistent gains across real-world perception and reasoning benchmarks and exhibits strong out-of-distribution generalization on challenging abstract visual reasoning tasks. We also empirically analyze the role of each training component and discuss our early unsuccessful attempts, providing insights for future developments in visual latent reasoning.
</details>

---

### Grounded 3D-Aware Spatial Vision-Language Modeling
著者: An-Chieh Cheng, Yang Fu, Yatai Ji, Ligeng Zhu, Guanqi Zhan, Zhuoyang Zhang, Zhaojing Yang, Song Han, Yao Lu, Pavlo Molchanov, Vidya Nariyambut Murali, Jan Kautz, Xiaolong Wang, Danny Yin, Sifei Liu

<details>
<summary> 日本語要旨 </summary>

私たちは、明示的な2次元グラウンディング、暗黙の2次元グラウンディング、およびモノクロ3次元グラウンディングという三つの補完的なグラウンディング能力を単一のフレームワーク内に備えた空間視覚言語モデル、GR3Dを紹介します。GR3Dは、生成中にエンティティメンションを特定し、対応する領域トークンをテキストストリームに挿入する暗黙のグラウンディング機構を導入します。これにより、空間的な思考連鎖応答を生成する際に、視覚証拠を即座に参照できるようになります。同時に、領域プロンプト付きのモノクロ3次元グラウングデザインは、内在的認識化と密度幾何学的監督を支えるもとで、グラウンドされた領域クエリからカメラビューにおける3次元バウンディングボックスの予測を行います。これらのグラウンディング能力は、複雑な空間理解問題をグラウンドされた2次元知覚に続く3次元推論へと分解することを可能にします。GR3Dは、グラウンドされたおよび非グラウンドされた空間ベンチマークの両方で一貫した改善を達成し、VLMsにおける空間理解の強化に向けてグラウンディングが効果的な帰納的バイアスであることを示しています。これらのグラウンディング能力は、グラウンディングタスク自体を超えた一般的な空間理解の向上に寄与します。
</details>

<details>
<summary> 英語要旨 </summary>

We present GR3D, a spatial vision language model equipped with three complementary grounding capabilities—explicit 2D grounding, implicit 2D grounding, and monocular 3D grounding—within a single framework. GR3D introduces an implicit grounding mechanism that identifies entity mentions during generation and inserts the corresponding region tokens into the text stream, allowing the model to reference visual evidence on the fly when producing spatial chain-of-thought responses. In parallel, a region-prompted monocular 3D grounding design predicts 3D bounding boxes in the camera view from grounded region queries, supported by intrinsic-aware normalization and dense geometric supervision. Together, these grounding capabilities enable GR3D to decompose complex spatial understanding problems into grounded 2D perception followed by 3D inference. GR3D achieves consistent improvements across grounded and non-grounded spatial benchmarks, demonstrating grounding as an effective inductive bias for strengthening spatial understanding in VLMs. These grounding capabilities collectively enhance general spatial understanding beyond the grounding task itself.
</details>

---

### Back to Basics: Let Denoising Generative Models Denoise
著者: Tianhong Li, Kaiming He

<details>
<summary> 日本語要旨 </summary>

現在のノイズ除去拡散モデルは、古典的な意味で「ノイズを除去」するわけではありません。つまり、クリーン画像を直接予測しません。代わりに、ニューラルネットワークはノイズやノイズ付きの量を予測します。本論文では、クリーンデータの予測とノイズ付き量の予測は根本的に異なるものであると提案しています。マニフォールド仮説によれば、自然データは低次元マニフォールド上に存在するべきですが、ノイズ付き量はそうではありません。この仮定に基づいて、クリーンデータを直接予測するモデルを提唱します。これにより、明らかに容量が不足していると思われるネットワークでも、非常に高次元の空間で効果的に動作できます。私たちは、トランスフォーマーを大きなパッチサイズでピクセル上に適用することが強力な生成モデルになり得ることを示します：トークナイザーを使用せず、事前学習も追加の損失関数もありません。私たちのアプローチは、「**Just image Transformers**」または「**JiT**」と呼ばれるもので、それ以上のことではありません。ImageNetにおいてパッチサイズ16と32を使用し、解像度256と512で競争力のある結果を報告しています。これらの条件下では、高次元ノイズ付き量を予測することが壊滅的に失敗する可能性があります。私たちのネットワークはマニフォールドへの基本的なマッピングに戻り、原始的なデータを扱うトランスフォーマーに基づく拡散の自己完結型パラダイムを追求しています。
</details>

<details>
<summary> 英語要旨 </summary>

Today's denoising diffusion models do not "denoise" in the classical sense, i.e., they do not directly predict clean images. Rather, the neural networks predict noise or a noised quantity. In this paper, we suggest that predicting clean data and predicting noised quantities are fundamentally different. According to the manifold assumption, natural data should lie on a low-dimensional manifold, whereas noised quantities do not. With this assumption, we advocate for models that directly predict clean data, which allows apparently under-capacity networks to operate effectively in very high-dimensional spaces. We show that simple, large-patch Transformers on pixels can be strong generative models: using no tokenizer, no pre-training, and no extra loss. Our approach is conceptually nothing more than "**Just image Transformers**", or **JiT**, as we call it. We report competitive results using JiT with large patch sizes of 16 and 32 on ImageNet at resolutions of 256 and 512, where predicting high-dimensional noised quantities can fail catastrophically. With our networks mapping back to the basics of the manifold, our research goes back to basics and pursues a self-contained paradigm for Transformer-based diffusion on raw natural data.
</details>

---

### Global Structure-from-Motion Meets Feedforward Reconstruction
著者: Linfei Pan, Johannes Schönberger, Marc Pollefeys

<details>
<summary> 日本語要旨 </summary>

構造復元（Structure-from-Motion）は、画像の集合からカメラ位置と3Dシーン構造を同時に推定するプロセスであり、コンピュータビジョン分野における中心的な課題です。多くの未解決問題が残されています。最近のフィードフォワード3D再構成技術は、低テクスチャ、限られた画像オーバーラップ、対称性などに特徴付けられるシナリオで、古典的SfM方法の持続する失敗ケースを克服する上で大きな進歩を遂げています。しかし、フィードフォワードアプローチはこれらの難しい条件下で優れた性能を発揮しますが、スケーラビリティ、精度、堅牢性に関して制約があり、通常の再構成設定では古典的方法に劣ることが多いです。本研究では、これらの限界を体系的に分析し、古典的およびフィードフォワード手法それぞれの強みを組み合わせた新しい最先端のStructure-from-Motionパイプラインを提案します。広範な再構成シナリオにおける包括的な実験は、私たちのアプローチが全体として最先端の結果を達成することでその利点を示しました。私たちのパイプラインの実装はオープンソースソフトウェアとして公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Structure-from-Motion -- the process of simultaneously estimating camera poses and 3D scene structure from a collection of images -- remains a central challenge in computer vision, with many open problems yet to be solved. Recent advances in feedforward 3D reconstruction have made significant strides in overcoming persistent failure cases of classical SfM methods, particularly in scenarios characterized by low texture, limited image overlap, and symmetries. However, while feedforward approaches excel in these challenging conditions, they often face limitations regarding scalability, accuracy, and robustness, and typically fall short of classical methods in standard reconstruction settings. In this work, we systematically analyze these limitations and propose a new state-of-the-art Structure-from-Motion pipeline by combining the respective strengths of classical and feedforward methods. Extensive experiments over a wide range of reconstruction scenarios demonstrate the benefits of our approach by achieving state-of-the-art results across the board. The implementation of our pipeline will be shared as open source software.
</details>

---

### Iris: Bringing Real-World Priors Into Diffusion Model for Monocular Depth Estimation
著者: Xinhao Cai, Gensheng Pei, Zeren Sun, Yazhou Yao, Fumin Shen, Wenguan Wang

<details>
<summary> 日本語要旨 </summary>

この論文では、モノクルアー深度推定（MDE）のために実世界の事前知識をディフュージョンモデルに組み込む決定論的フレームワークである**Iris**を提案します。従来のフィードフォワード手法は大量のトレーニングデータに依存していますが、詳細な情報を欠いてしまうことがあります。一方で、以前のディフュージョンベースの方法は豊富な生成事前知識を活用しますが、シミュレーションから実世界へのドメイン転移に苦労しています。Irisはこれとは異なり、細部を保持し、シミュレーションから実世界のシーンへ強く一般化でき、限られたトレーニングデータでも効率的です。この目的のために、私たちは二段階のPriors-to-Geometry Deterministic（PGD）スケジュールを導入します：事前知識段階ではSpectral-Gated Distillation（SGD）を用いて低周波数の実世界の事前知識を転送し、高周波数の詳細は制約されません。幾何学段階ではSpectral-Gated Consistency（SGC）を適用して高周波数の忠実性を強制し、シミュレーションによるグラウンドトゥルースで洗練します。両段階は重みを共有し、高から低へのタイムステップスケジュールで実行されます。広範な実験結果が示すとおり、Irisは強力な野外一般化能力を持ちつつMDEパフォーマンスに顕著な改善を達成しています。
</details>

<details>
<summary> 英語要旨 </summary>

In this paper, we propose \textbf{Iris}, a deterministic framework for Monocular Depth Estimation (MDE) that integrates real-world priors into the diffusion model. Conventional feed-forward methods rely on massive training data, yet still miss details. Previous diffusion-based methods leverage rich generative priors yet struggle with synthetic-to-real domain transfer. Iris, in contrast, preserves fine details, generalizes strongly from synthetic to real scenes, and remains efficient with limited training data. To this end, we introduce a two-stage Priors-to-Geometry Deterministic (PGD) schedule: the prior stage uses Spectral-Gated Distillation (SGD) to transfer low-frequency real priors while leaving high-frequency details unconstrained, and the geometry stage applies Spectral-Gated Consistency (SGC) to enforce high-frequency fidelity while refining with synthetic ground truth. The two stages share weights and are executed with a high-to-low timestep schedule. Extensive experimental results confirm that Iris achieves significant improvements in MDE performance with strong in-the-wild generalization.
</details>

---

### SpeeDiff: Scalable Pixel-Anchored End-to-End Latent Diffusion Model
著者: Bingliang Zhang, Wenda Chu, Yizhuo Li, Linjie Yang, Yisong Yue, Katie Bouman, Yang Song, Qiushan Guo

<details>
<summary> 日本語要旨 </summary>

私たちは、スケーラブルなピクセルアンカー付きエンドツーエンド拡散（SpeeDiff）を提案します。これは、VAEと拡散モデルを一緒に初期設定からトレーニングするラテント拡散手法です。原理的には、ジョイントトレーニングにより、拡散損失勾配が直接VAEエンコーダーをガイドし、生成に優しいラテント空間の形成を促進し、事前学習済みで凍結されたVAEを用いる従来の2段階アプローチよりも速い収束が期待できます。しかし、単純なエンドツーエンド実装はパフォーマンスを大幅に低下させるため、制限のない拡散損失のバックプロパゲーションがラテント空間の崩壊を引き起こします。私たちの主要な技術的貢献は、Tweedieの式を用いて予測されたクリーンラテントを中間ノイズ状態からデコードすることで追加のピクセルレベルフィードバックを提供するシンプルかつ効果的なTweedieピクセル再構成（TPR）損失です。これにより、崩壊が軽減されます。さらに、私たちの方法は完全にトランスフォーマーベースのアーキテクチャをスケールし、エンドツーエンドフレームワーク内で表現の整合性を向上させることが可能です。SpeeDiff-XLモデルは、Vanilla SiTおよびREPAに対してそれぞれ140倍以上、61倍以上速いトレーニング時間で、ImageNet 256×256生成においてガイダンスなしでFID 1.50を達成します。さらに効率的な32倍圧縮されたVAEを用いることで、モデルはガイダンスなしでImageNet 512×512生成においてFID 1.53を達成します。
</details>

<details>
<summary> 英語要旨 </summary>

We present Scalable Pixel-anchored End-to-end Diffusion (SpeeDiff), a latent diffusion method that jointly trains the VAE and the diffusion model from scratch. In principle, joint training allows the diffusion loss gradient to directly guide the VAE encoder, encouraging the formation of a generation-friendly latent space and potentially yielding faster convergence than the conventional two-stage approach with a pretrained frozen VAE. However, a naive end-to-end implementation severely degrades performance, as unrestricted backpropagation of the diffusion loss leads to latent space collapse. Our main technical contribution is a simple yet effective Tweedie Pixel Reconstruction (TPR) loss, which provides additional pixel-level feedback by decoding a predicted clean latent from an intermediate noisy state using Tweedie's formula, thereby alleviating collapse. Furthermore, our method enables jointly scaling a fully transformer-based architecture and enhances representation alignment within the end-to-end framework. Our SpeeDiff-XL model achieves over 140× and 61× faster training compared to Vanilla SiT and REPA, respectively, while attaining an FID of 1.50 without guidance on ImageNet 256×256 generation. With a more efficient 32× compressed VAE, our model further reaches an FID of 1.53 without guidance on ImageNet 512×512 generation.
</details>

---

### OneThinker: All-in-one Reasoning Model for Image and Video
著者: Kaituo Feng, Manyuan Zhang, Hongyu Li, Kaixuan Fan, shuang chen, Yilei Jiang, Dian Zheng, Peiwen Sun, Yiyuan Zhang, Haoze Sun, Yan Feng, Peng Pei, Xunliang Cai, Xiangyu Yue

<details>
<summary> 日本語要旨 </summary>

強化学習（RL）は最近、マルチモーダル大規模言語モデル（MLLMs）における視覚的推論の引き出しに顕著な成功を収めています。しかし、既存のアプローチは通常、異なるタスクごとに別々のモデルをトレーニングし、画像および動画推論を独立したドメインとして扱います。これにより、多様なタスクやモダリティ間での知識共有が制限され、実用的な汎用性が制約される結果となっています。この問題を解決するために、私たちはOneThinkerを提案します。これは画像および動画の理解を多様な基本的視覚タスクにわたり統一したオールインワン推論モデルです。具体的には、質問応答、キャプショニング、空間および時間的なアンカリング、追跡、セグメンテーションを含みます。これを達成するために、私たちはこれらのタスクを網羅したOneThinker-600kトレーニングコーパスを構築し、商用モデルを使用してCoT注釈を行い、結果としてOneThinker-SFT-340k（SFTの冷始動）が得られました。さらに、多タスクRLにおける報酬異質性を処理するためにEMA-GRPOを提案します。これは各タスクごとに報酬の標準偏差の移動平均を追跡し、バランスの取れた最適化を行います。多様な視覚ベンチマークでの広範な実験により、OneThinkerは10の基本的な視覚理解タスクにわたる31のベンチマークで強力な性能を発揮することが示されました。また、特定のタスク間で効果的な知識転移および初期段階のゼロショット一般化能力を示し、統一されたマルチモーダル推論汎用機に向けた一歩となっています。すべてのコード、モデル、およびデータは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Reinforcement learning (RL) has recently achieved remarkable success in eliciting visual reasoning within Multimodal Large Language Models (MLLMs). However, existing approaches typically train separate models for different tasks and treat image and video reasoning as disjoint domains. This results in limited scalability toward a multimodal reasoning generalist, which restricts practical versatility and hinders potential knowledge sharing across tasks and modalities. To this end, we propose OneThinker, an all-in-one reasoning model that unifies image and video understanding across diverse fundamental visual tasks, including question answering, captioning, spatial and temporal grounding, tracking, and segmentation. To achieve this, we construct the OneThinker-600k training corpus covering all these tasks and employ commercial models for CoT annotation, resulting in OneThinker-SFT-340k for SFT cold start. Moreover, we propose EMA-GRPO to handle reward heterogeneity in multi-task RL by tracking task-wise moving averages of reward standard deviations for balanced optimization. Extensive experiments on diverse visual benchmarks show that OneThinker delivers strong performance on 31 benchmarks, across 10 fundamental visual understanding tasks. Moreover, it exhibits effective knowledge transfer between certain tasks and preliminary zero-shot generalization ability, marking a step toward a unified multimodal reasoning generalist. All code, model, and data will be released.
</details>

---

### LagerNVS: Latent Geometry for Fully Neural Real-time Novel View Synthesis
著者: Stanislaw Szymanowicz, Minghao Chen, Jianyuan Wang, Christian Rupprecht, Andrea Vedaldi

<details>
<summary> 日本語要旨 </summary>

最近の研究では、ネットワークベースのレンダリングが3Dインダクティブバイアスを欠いているにもかかわらず、より良い結果を得られることが示されています。本論文では、明示的な3D表現を用いずに強力な3Dバイアスを活用することで、さらに高品質の結果を得ることを示します。これを実現するために、我々はLagerNVSというエンコーダー・デコーダーネットワークを導入しました。このネットワークは3D認識機能を隠れ変数としてシーンの符号化に使用します。エンコーダーは3D再構成ネットワークから初期化され、軽量なデコーダーとペアになり、フォトメトリック損失を用いて終端まで訓練されます。LagerNVSは既知のカメラがある場合もない場合も含め、最先端の決定論的フィードフォワードによる新観点生成結果（Re10kで31.1 PSNRを達成）を実現し、リアルタイムでレンダリングが可能です。また、既知のカメラなしの野外データにも一般化することができ、拡散デコーダーと組み合わせて生成的補完を行うことができます。
</details>

<details>
<summary> 英語要旨 </summary>

Novel View Synthesis has often relied on explicit 3D representations, which inject a strong 3D bias in the process; however, recent work has shown that network-based rendering can work better despite lacking 3D inductive biases. In this paper, we show that much better quality can be obtained by leveraging a strong 3D bias without a 3D representation. To do so, we introduce LagerNVS, an encoder-decoder network that uses 3D-aware features as a latent scene encoding. The encoder is initialized from a 3D reconstruction network, paired with a lightweight decoder, and trained end-to-end with photometric losses. LagerNVS achieves state-of-the-art deterministic feed-forward Novel View Synthesis results (including 31.1 PSNR on Re10k), with and without known cameras, renders in real-time, generalizes to in-the-wild data without known cameras, and can be paired with a diffusion decoder for generative completions.
</details>

---

### Improving Vision-language Models with Perception-centric Process Reward Models
著者: Yingqian Min, Kun Zhou, Yifan Li, Yuhuan Wu, Han Peng, Yifan Du, Xin Zhao, Min Yang, Ji-Rong Wen

<details>
<summary> 日本語要旨 </summary>

最近の強化学習における検証可能な報酬（RLVR）の進展は、ビジョン言語モデル（VLMs）の複雑な推論能力を大幅に向上させました。しかし、その結果レベルの監督があまりにも粗いため、推論チェーン内のエラーを診断し修正することは困難です。この問題に対処するため、私たちはPercevalというプロセス報酬モデル（PRM）を提案します。これによりトークンレベルでのエラーの根拠付けが可能となり、応答から画像関連の主張を抽出し、それらを一つずつ視覚的証拠と比較することで、知覚エラーを含む主張を返すことができます。Percevalは知覚集中型の監督学習データでトレーニングされています。その後、PercevalをRLトレーニングプロセスに統合し、ポリシーモデルをトレーニングします。具体的には、従来のGRPOがシーケンスレベルでの利点を適用するのと異なり、Percevalによって特定された幻覚化したスパンに対してペナルティを適用し、トークンレベルでの利点を適用することで、微細な監督信号が可能になります。また、PercevalはVLMsのトレーニングプロセスを強化するだけでなく、推論段階でも支援します。Percevalを使用してモデルの応答の誤った部分を切り捨て、その後直接応答を再生成させるか、モデルに以前の出力を反省させることができます。このプロセスは何度も繰り返すことでテスト時のスケーリングを達成することができます。実験結果では、RLでトレーニングされたさまざまな推論VLMsにおいて様々なドメインのベンチマークで顕著な改善が示されました。テスト時スケーリングでは、主要投票法など他の戦略と比較して一貫したパフォーマンス向上も示しました。私たちのコードとデータは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advancements in reinforcement learning with verifiable rewards (RLVR) have significantly improved the complex reasoning ability of vision-language models (VLMs). However, its outcome-level supervision is too coarse to diagnose and correct errors within the reasoning chain. To this end, we propose Perceval, a process reward model (PRM) that enables token-level error grounding, which can extract image-related claims from the response and compare them one by one with the visual evidence in the image, ultimately returning claims that contain perceptual errors. Perceval is trained with perception-intensive supervised training data. We then integrate Perceval into the RL training process to train the policy models. Specifically, compared to traditional GRPO, which applies sequence-level advantages, we apply token-level advantages by targeting penalties on hallucinated spans identified by Perceval, thus enabling fine-grained supervision signals. In addition to augmenting the training process, Perceval can also assist VLMs during the inference stage. Using Perceval, we can truncate the erroneous portions of the model’s response, and then either have the model regenerate the response directly or induce the model to reflect on its previous output. This process can be repeated multiple times to achieve test-time scaling. Experiments show significant improvements on benchmarks from various domains across multiple reasoning VLMs trained with RL. For test-time scaling, it also demonstrates consistent performance gains over other strategies, such as major voting. Our code and data will be publicly released.
</details>

---

### GeoSAM2: Unleashing The Power of SAM2 for 3D Part Segmentation
著者: Ken Deng, Yunhan Yang, Jingxiang Sun, Xihui Liu, Yebin Liu, Ding Liang, Yan-Pei Cao

<details>
<summary> 日本語要旨 </summary>

私たちは、GeoSAM2というプロンプト制御可能なフレームワークを紹介します。これは3D部品セグメンテーションのタスクを多視点2Dマスク予測として扱います。質感のないオブジェクトに対し、事前定義されたビューから法線マップやポイントマップをレンダリングし、単純な2Dプロンプト（クリックやボックス）を受け入れて部品選択をガイドします。これらのプロンプトはLoRAと残差幾何学融合によって強化された共有SAM2バックボーンで処理され、ビュー固有の推論を可能にしつつ事前学習済みの優先順位を保持します。予測されたマスクはオブジェクトにバックプロジェクションされ、ビュー間で集約されます。私たちの方法では、テキストプロンプトや形状ごとの最適化、完全な3Dラベルを必要とせずに、部品特有の精密制御が可能です。グローバルクラスタリングやスケールベースの方法とは対照的に、プロンプトは明示的で空間的に根拠があり、解釈しやすいものです。私たちはPartObjaverse-TinyおよびPartNetEでクラス非依存性能において最先端を達成し、遅延最適化ベースのパイプラインと速くて粗いフィードフォワードアプローチの両方を上回りました。私たちの結果は新しいパラダイムを強調しています：3DセグメンテーションのパラダイムをSAM2と整合させ、インタラクティブな2D入力を活用することでオブジェクトレベルの部品理解における制御可能性と精度を解放します。
</details>

<details>
<summary> 英語要旨 </summary>

We introduce GeoSAM2, a prompt-controllable framework for 3D part segmentation that casts the task as multi-view 2D mask prediction. Given a textureless object, we render normal and point maps from predefined viewpoints and accept simple 2D prompts—clicks or boxes—to guide part selection. These prompts are processed by a shared SAM2 backbone augmented with LoRA and residual geometry fusion, enabling view-specific reasoning while preserving pretrained priors. The predicted masks are back-projected to the object, aggregated across views. Our method enables fine-grained, part-specific control without requiring text prompts, per-shape optimization, or full 3D labels. In contrast to global clustering or scale-based methods, prompts are explicit, spatially grounded, and interpretable. We achieve state-of-the-art class-agnostic performance on PartObjaverse-Tiny and PartNetE, outperforming both slow optimization-based pipelines and fast but coarse feedforward approaches. Our results highlight a new paradigm: aligning the paradigm of 3D segmentation with SAM2, leveraging interactive 2D inputs to unlock controllability and precision in object-level part understanding.
</details>

---

### Humanoid Generative Pre-Training for Zero-Shot Motion Tracker
著者: Zekun Qi, Xuchuan Chen, Jilong Wang, Chenghuai Lin, Yunrui Lian, Wenyao Zhang, XinQiang Yu, He Wang, Li Yi

<details>
<summary> 日本語要旨 </summary>

私たちは、全身制御のために因果的注意を用いてトレーニングされた初のGPTスタイルヒューマノイド動作変換器であるHumanoid-GPTを紹介します。これは、希少なデータと俊敏性・汎用性のトレードオフに制限された従来の浅いMLPトラッカーとは異なります。Humanoid-GPTは、すべての主要なモーションキャプチャーデータセットを大規模な社内録音と統一した2Bフレームのリターゲティングコーパスで事前トレーニングされています。データおよびモデル容量の両方を拡大することにより、任意の人間が非常にダイナミックな動作を実行している際に追跡し、未見の動作や制御タスクへの前例のないゼロショット一般化を達成する単一の生成変換器が得られます。広範な実験とスケーリング分析により、私たちのモデルは新しいパフォーマンスフロンティアを確立しており、高度で複雑な動作を同時に追跡しながら未見のタスクへの堅牢なゼロショット一般化を示しています。
</details>

<details>
<summary> 英語要旨 </summary>

We introduce Humanoid-GPT, the first GPT-style humanoid motion Transformer trained with causal attention on a billion-scale motion corpus for whole-body control. Unlike prior shallow MLP trackers constrained by scarce data and an agility–generalization trade-off, Humanoid-GPT is pre-trained on a 2B-frame retargeted corpus that unifies all major mocap datasets with large-scale in-house recordings. Scaling both data and model capacity yields a single generative Transformer that tracks arbitrary humans executing highly dynamic behaviors while achieving unprecedented zero-shot generalization to unseen motions and control tasks. Extensive experiments and scaling analyses show that our model establishes a new performance frontier, demonstrating robust zero-shot generalization to unseen tasks while simultaneously tracking highly dynamic and complex motions.
</details>

---

### FlashDecoder: Real-Time Latent-to-Pixel Streaming Decoder with Transformers
著者: Minguk Kang, Suha Kwak

<details>
<summary> 日本語要旨 </summary>

最近の動画生成における進歩は、大規模モデルを畳み込みアーキテクチャからDiffusion Transformers（DiT）へと移行させましたが、ラテンスからピクセルへの動画デコーダーは依然として主に畳み込みベースです。これらのデコーダーは重い3D畳み込みを使用し、高解像度や長時間の出力を扱うために空間・時間的なタイリングが必要とされます。私たちは、ストリーミング用に設計された最初のTransformerベースのラテンスからピクセルへの動画デコーダーであるFlashDecoderを紹介します。FlashDecoderはトレーニングおよび推論時にフレームごとに動画ラテンスを処理し、各フレーム内で双方向の空間注意を適用しつつ、ローリングKVキャッシュを通じて因果的な時間依存性を維持します。重要なことに、因果性は明示的な注意マスクではなく、フレームの順次処理によって強制されます。これにより、メモリ効率の高い双方向注意カーネルを全体で使用することが可能になります。この統一的なストリーミングアプローチは、固定サイズのKVキャッシュを用いた自動的な古いフレームの削除によって、一定のフレームごとの計算と制限されたメモリを保証し、720p解像度まで安定したトレーニングが可能です。Wan2.2動画VAEに統合されたFlashDecoderは、畳み込みデコーダー（PSNR 38.38 vs. 38.29; LPIPS 0.046 vs. 0.039）と同等の再構成品質を達成しつつ、最大4倍速い—480pで139 FPSおよび720pで69.6 FPS—の動画デコードを実現し、シングルH100 GPU上でリアルタイム高解像度動画デコードを達成します。
</details>

<details>
<summary> 英語要旨 </summary>

Recent progress in video generation has shifted large-scale models from convolutional architectures to Diffusion Transformers (DiT), yet latent-to-pixel video decoders remain predominantly convolutional. These decoders rely on heavy 3D convolutions, which slow down streaming generation and require spatial–temporal tiling to handle high-resolution or long-duration outputs. We introduce FlashDecoder, the first Transformer-based latent-to-pixel video decoder designed for streaming. FlashDecoder processes video latents frame-by-frame during both training and inference, applying bidirectional spatial attention within each frame while maintaining causal temporal dependencies through a rolling KV cache. Crucially, causality is enforced by sequential frame processing rather than explicit attention masks, enabling the use of memory-efficient bidirectional attention kernels throughout. This unified streaming approach ensures constant per-frame computation and bounded memory via a fixed-size KV cache with automatic eviction of older frames, enabling stable training at resolutions up to 720p. Integrated into the Wan2.2 video VAE, FlashDecoder matches the reconstruction quality of the convolutional decoder (PSNR 38.38 vs. 38.29; LPIPS 0.046 vs. 0.039) while decoding up to 4x faster—139 FPS at 480p and 69.6 FPS at 720p—achieving real-time high-resolution video decoding on a single H100 GPU.
</details>

---

### Reconstructing Functional 3D Scenes from Egocentric Interaction Videos
著者: Alexandros Delitzas, Chenyangguang Zhang, Alexey Gavryushin, Tommaso Di Mario, Boyang Sun, Rishabh Dabral, Leonidas Guibas, Christian Theobalt, Marc Pollefeys, Francis Engelmann, Daniel Barath

<details>
<summary> 日本語要旨 </summary>

私たちは、エゴセントリックなRGB-Dインタラクションビデオから直接機能的3Dデジタルツインを再構築する方法であるFunRECを紹介します。既存の可動部分再構成手法とは異なり、これらは制御されたセットアップ、多状態キャプチャ、またはCAD事前情報に依存していますが、FunRECはインタラクティブな3Dシーンを回収するために直接野外の人間のインタラクションシーケンスを操作します。それは可動部分を自動的に発見し、その運動学パラメータを推定し、3D運動を追跡し、標準空間で静止および移動する幾何学を再構成してシミュレーション互換のメッシュを生成します。新しい実際のおよびシミュレートされたベンチマークにわたって、FunRECは大幅に優れており、部分セグメンテーションで最大+50 mIoUの改善、5〜10倍低い可動性とポーズエラー、そして顕著に高い再構成精度を達成しています。さらに、シミュレーション用のURDF/USDエクスポート、手動アフォーダンスマッピング、ロボット-シーンインタラクションへの応用を示します。すべてのコードとデータは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

We present FunREC, a method for reconstructing functional 3D digital twins of indoor scenes directly from egocentric RGB-D interaction videos. Unlike existing methods on articulated reconstruction, which rely on controlled setups, multi-state captures, or CAD priors, FunREC operates directly on in-the-wild human interaction sequences to recover interactable 3D scenes. It automatically discovers articulated parts, estimates their kinematic parameters, tracks their 3D motion, and reconstructs static and moving geometry in canonical space, yielding simulation-compatible meshes. Across new real and simulated benchmarks, FunREC surpasses prior work by a large margin, achieving up to +50 mIoU improvement in part segmentation, 5$-$10$\times$ lower articulation and pose errors, and significantly higher reconstruction accuracy. We further demonstrate applications on URDF/USD export for simulation, hand-guided affordance mapping and robot-scene interaction. All code and data will be released.
</details>

---

### LLaDA-V: Large Language Diffusion Models with Visual Instruction Tuning
著者: Zebin You, Shen Nie, Xiaolu Zhang, JUN ZHOU, Zhiwu Lu, Ji-Rong Wen, Chongxuan Li

<details>
<summary> 日本語要旨 </summary>

本研究では、視覚指示調整とマスク付き拡散モデルを統合した純粋な拡散型の多様性大言語モデル（MLLM）であるLLaDA-Vを提案します。これは、現在のマルチモーダルアプローチにおいて支配的な自己回帰パラダイムからの転換を表しています。代表的な大言語拡散モデルであるLLaDAを基盤とし、視覚エンコーダーおよびMLPコネクタを組み込んだLLaDA-Vは、視覚特徴を言語埋め込み空間に投影することで、拡散言語モデルの双方向注意を活用し、因果的な順次処理よりも効果的に視覚データ内の空間関係を捉えます。実証調査からはいくつか興味深い結果が明らかになりました：まず、LLaDA-Vは純粋なテキストタスクではLLaMA3-8BやQwen2-7Bのような対抗モデルと比較して言語モデルが弱いにもかかわらず、有望なマルチモーダル性能を示します。同じ指示データでトレーニングした場合、LLaDA-VはLLaMA3-Vと競争力があり、より良いデータスケーラビリティを持ちます。また、Qwen2-VLに対するパフォーマンスの差を縮めており、そのアーキテクチャがマルチモーダルタスクに効果的であることを示唆しています。次に、LLaDA-Vは既存の純粋な拡散型MLLMと比較して、マルチモーダル理解において最先端の性能を達成しました。これらの結果から、大言語拡散モデルがマルチモーダルコンテキストで有望であることが示唆され、さらなる研究が必要です。このために、LLaDA-Vモデルおよびそのトレーニング・評価用のコードをオープンソース化します。
</details>

<details>
<summary> 英語要旨 </summary>

In this work, we introduce LLaDA-V, a purely diffusion-based Multimodal Large Language Model (MLLM) that integrates visual instruction tuning with masked diffusion models, representing a departure from the autoregressive paradigms dominant in current multimodal approaches. Built upon LLaDA, a representative large language diffusion model, LLaDA-V incorporates a vision encoder and MLP connector that projects visual features into the language embedding space, leveraging diffusion language models' bidirectional attention to capture spatial relationships in visual data more effectively than causal, sequential processing. Our empirical investigation reveals several intriguing results: First, LLaDA-V demonstrates promising multimodal performance despite its language model being weaker on purely textual tasks than counterparts like LLaMA3-8B and Qwen2-7B. When trained on the same instruction data, LLaDA-V is highly competitive with LLaMA3-V across multimodal tasks with better data scalability. It also narrows the performance gap to Qwen2-VL, suggesting the effectiveness of its architecture for multimodal tasks. Second, LLaDA-V achieves state-of-the-art performance in multimodal understanding compared to existing purely diffusion-based MLLMs. Our findings suggest that large language diffusion models show promise in multimodal contexts and warrant further investigation. To facilitate such research, we will open-source the LLaDA-V model along with its training and evaluation code.
</details>

---

### Cupid: Generative 3D Reconstruction Via Joint Object and Pose Modeling
著者: Binbin Huang, Haobin Duan, Yiqun Zhao, Zibo Zhao, Yi Ma, Shenghua Gao

<details>
<summary> 日本語要旨 </summary>

私たちは、カノニカルオブジェクトとカメラ姿勢の両方に対する完全な分布を同時にモデリングする生成的3D再構成フレームワークである「Cupid」を紹介します。私たちの2段階の流れベースのモデルは、まず粗い3D構造と2D-3D対応関係を生成し、カメラ姿勢を堅牢に推定します。この姿勢を条件として、次の段階ではピクセルアライメントされた画像特徴を直接生成プロセスに注入し、生成モデルの豊かな事前知識と再構成の幾何学的忠実性を融合させます。この戦略は、3 dB以上のPSNRおよび10%のチャメファー距離で最先端の再構成手法を大きく上回る卓越した忠実性を達成します。オブジェクトとカメラ姿勢を分離する統一的な生成モデルとして、Cupidはポストホック最適化や微調整を必要とせずに自然にマルチビューおよびシーンレベルの再構成タスクに拡張されます。
</details>

<details>
<summary> 英語要旨 </summary>

We introduce Cupid, a generative 3D reconstruction framework that jointly models the full distribution over both canonical objects and camera poses. Our two-stage flow-based model first generates a coarse 3D structure and 2D-3D correspondences to estimate the camera pose robustly. Conditioned on this pose, a refinement stage injects pixel-aligned image features directly into the generative process, marrying the rich prior of a generative model with the geometric fidelity of reconstruction. This strategy achieves exceptional faithfulness, outperforming state-of-the-art reconstruction methods by over 3 dB PSNR and 10\% in Chamfer Distance. As a unified generative model that decouples the object and camera pose, Cupid naturally extends to multi-view and scene-level reconstruction tasks without requiring post-hoc optimization or fine-tuning.
</details>

---

### ARC Is A Vision Problem!
著者: Keya Hu, Ali Cy, Linlu Qiu, Delores(Xiaoman) Ding, Runqian Wang, Yeyin Zhu, Jacob Andreas, Kaiming He

<details>
<summary> 日本語要旨 </summary>

Abstraction and Reasoning Corpus（ARC）は、人間の知能における基本的な要素である抽象的推論を促進するために設計されています。一般的なARCへのアプローチでは、これを言語指向の問題として扱い、大規模言語モデル（LLMs）や反復推論モデルで対処します。しかし、ARCに含まれるパズルのようなタスクは本質的に視覚的であるにもかかわらず、既存の研究では視覚中心の観点から問題をアプローチすることが稀です。この研究では、ARCをビジョンパラダイム内で定式化し、画像間変換問題としてフレーミングします。視覚的な事前知識を取り入れるために、入力を「キャンバス」として表現し、自然画像のように処理できるようにします。これにより、標準的なビジョンアーキテクチャ（例えば、vanilla Vision Transformer（ViT））を用いて画像間マッピングを行うことが容易になります。私たちのモデルはARCデータからゼロからトレーニングされ、テスト時学習を通じて未見のタスクへ一般化します。このフレームワークはVision ARC（VARC）と呼ばれ、ARC-1ベンチマークで60.4%の精度を達成し、ゼロからトレーニングされた既存手法を大幅に上回ります。私たちの結果は主要なLLMsと競争力があり、平均的な人間のパフォーマンスに近づいています。
</details>

<details>
<summary> 英語要旨 </summary>

The Abstraction and Reasoning Corpus (ARC) is designed to promote research on abstract reasoning, a fundamental aspect of human intelligence. Common approaches to ARC treat it as a language-oriented problem, addressed by large language models (LLMs) or recurrent reasoning models. However, although the puzzle-like tasks in ARC are inherently visual, existing research has rarely approached the problem from a vision-centric perspective. In this work, we formulate ARC within a vision paradigm, framing it as an image-to-image translation problem. To incorporate visual priors, we represent the inputs on a “canvas” that can be processed like natural images. It is then straightforward for us to apply standard vision architectures, such as a vanilla Vision Transformer (ViT), to perform image-to-image mapping. Our model is trained from scratch solely on ARC data and generalizes to unseen tasks through test-time training. Our framework, termed Vision ARC (VARC), achieves 60.4% accuracy on the ARC-1 benchmark, substantially outperforming existing methods that are also trained from scratch. Our results are competitive with those of leading LLMs and close the gap to average human performance.
</details>

---

### SpatialScore: Towards Comprehensive Evaluation for Spatial Intelligence
著者: Haoning Wu, Xiao Huang, Yaohui Chen, Ya Zhang, Yanfeng Wang, Weidi Xie

<details>
<summary> 日本語要旨 </summary>

既存の研究では、マルチモーダル大規模言語モデル（MLLMs）における空間理解は、断片的な評価によって制限されています。本論文では、既存のMLLMsの空間理解能力を包括的に評価することを考慮しています。具体的には、以下の貢献をこの論文で行っています：（i）私たちは**SpatialScore**を提案します。これは、約5,000件の手動で確認されたサンプルを含む30種類の異なるタスクにわたり、さまざまな視覚データタイプ、入力モダリティ、QAフォーマットを包括するこれまでで最も包括的かつ多様なマルチモーダル空間知能ベンチマークです；（ii）私たちは**SpatialCorpus**という大規模なトレーニングリソースを構築し、331,000件のマルチモーダルQAサンプルを用いて空間理解におけるQwen3-VLの教師あり微調整に使用します；（iii）私たちは**SpaitalAgent**という12種類の専門的な空間知覚ツールを統合したマルチエージェントシステムを開発し、*Plan-Execute*および*ReAct*推論パラダイムをサポートすることで、トレーニングフリーの方法で空間推論を向上させます；そして（iv）私たちは40種類の代表的なMLLMsに対して広範な評価を行い、空間知能における持続する課題を明らかにしましたが、同時にデータ駆動型とエージェントベースの解決策の有効性も示しました。すべてのデータ、コード、モデルは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Existing studies on multimodal large language models (MLLMs) in spatial understanding are typically limited by fragmented assessments. This work considers a comprehensive evaluation of the spatial understanding abilities of existing MLLMs. Concretely, we make the following contributions in this paper: (i) we propose **SpatialScore**, the most comprehensive and diverse multimodal spatial intelligence benchmark to date, encompassing various visual data types, input modalities, and QA formats with around 5K manually verified samples across 30 distinct tasks; (ii) we construct **SpatialCorpus**, a large-scale training resource with 331K multimodal QA samples for supervised fine-tuning Qwen3-VL on spatial understanding; (iii) we develop **SpaitalAgent**, a multi-agent system incorporating 12 specialized spatial perception tools, supporting both *Plan-Execute* and *ReAct* reasoning paradigms, enabling to improve spatial reasoning in a training-free manner; and (iv) we conduct extensive evaluations on 40 representative MLLMs, revealing persistent challenges in spatial intelligence while demonstrating the effectiveness of our data-driven and agent-based solutions. All data, code, and models will be publicly available.
</details>

---

### Hint2Gen: Bridging Understanding and Generation Via Code-structured Hints
著者: Yuanpeng Tu, Yunpeng Chen, Xi Chen, Liang Li, Hengshuang Zhao

<details>
<summary> 日本語要旨 </summary>

最近の統一モデルは高品質な画像を生成する点で顕著な進歩を遂げていますが、推理集約型タスク（迷路解決やタングラムの組み立てなど）では依然として失敗し続けています。興味深いことに、視覚言語モデル（VLMs）および大規模言語モデル（LLMs）はこれらのタスクを正確に解決できるものの、構造化された視覚出力インターフェースが欠如しているため、対応する画像を生成することができません。これは推理能力ではなく、高レベルの推理を正確な視覚出力に変換する構造化されたインターフェースの欠如が本質的なボトルネックであることを示しています。このギャップを埋めるため、私たちは画像平面上に推理ステップを直接エンコードするSVG/HTMLのようなコード構造化された視覚的ヒント（オーバレイ）を使用することを提案します。それに応じて、既存のデータセット用の高品質なコード構造化ヒントを生成できる自動データ構築パイプラインを開発しました。また、FLUX.1 Kontextに基づく統一モデル「Hint2Gen」を訓練し、そのようなヒントに条件付けて生成します。さらに、私たちのアプローチの効果を包括的に評価するために、「Reason2Gen」というベンチマークを導入しました。これは7つのコア次元（経路接続性、空間組み立てなど）を含む20カテゴリーにわたる4,000サンプルから構成されています。広範囲な実験は、単純にこれらのヒントを追加入力として提供するだけで（再訓練なしで）そのパフォーマンスが向上することを示しています。また、私たちのモデルは推論に配慮した生成および編集タスクにおいてすべての次元でオープンソース/プロプライエタリーの主要な方法を大きく上回っています。
</details>

<details>
<summary> 英語要旨 </summary>

Recent unified models have made remarkable strides in generating high-quality images, yet they consistently fail on reasoning-intensive tasks, i.e., solving mazes, assembling tangrams. Intriguingly, we find that vision-language models (VLMs) and large language models (LLMs) can accurately solve these tasks, but cannot generate the corresponding images because they lack a structured visual output interface. This reveals that the core bottleneck is not reasoning capacity, but the lack of a structured interface to translate high-level reasoning into precise visual output. To bridge this gap, we propose using code-structured visual hints (i.e., SVG/HTML) overlays that explicitly encode reasoning steps directly on the image plane. Accordingly, we develop an automatic data construction pipeline that can generate high-quality code-structured hints for existing datasets and train a unified model called Hint2Gen based on FLUX.1 Kontext to condition its generation on such hints. Furthermore, to comprehensively evaluate the effectiveness of our approach, we introduce Reason2Gen, a benchmark comprising 4,000 samples spanning 20 categories across 7 core dimensions, including path connectivity, spatial assembly, etc. Extensive experiments demonstrate that even simply providing such hints as extra inputs—without any retraining—boosts their performance. And our model significantly outperforms all leading open-source/closed-source methods on reasoning-aware generation and editing across all the dimensions.
</details>

---

### Temporal Equilibrium MeanFlow: Bridging The Scale Gap for One-Step Generation
著者: Yuanpeng Tu, Yunpeng Chen, Xinyu Zhang, Chao Liao, Hengshuang Zhao

<details>
<summary> 日本語要旨 </summary>

MeanFlowは、ゼロからトレーニング可能な強力な少ステップ生成フレームワークですが、一ステップ損失に大量のトレーニングデータを使用するとパフォーマンスが著しく低下します。これは時間的スケールの不均衡に起因しています：生成の異なる段階からの勾配が不均等に寄与し、最適化を不安定にすることで現れます。これはぼやけたサンプルや高いFIDスコアに顕著です。根本的な問題は、長期間の分散を増幅する項目と生成開始時に必要な強力な制約という二つの対立する力の衝突です。固定されたサンプリング戦略ではこれらを調和させることはできません。この問題を解決するために、私たちはTemporal Equilibrium MeanFlow（TEMF）を提案します。これは二つのシンプルかつ効果的なコンポーネントを通じて競合する要求をバランスさせます：(1) すべての時間スケールで勾配の影響を均等化する時間的平衡重み付け関数、および (2) 訓練開始時には初期ステップの安定化から全体の軌道の洗練へと訓練焦点を徐々にシフトする動的境界スケジューラー。モデルアーキテクチャを変更せず、TEMFは分類器なしのガイダンスと共に真の一ステップ生成を維持し、ImageNet 256×256での最先端FIDスコア2.62を達成します。これは拡散ベースおよび流れベースの一ステップ手法の中でも最高の結果です。
</details>

<details>
<summary> 英語要旨 </summary>

MeanFlow is a powerful few-step generative framework that can be trained from scratch, but its performance degrades significantly when the one-step loss uses a large portion of training data. This stems from a temporal scale imbalance: gradients from different stages of generation contribute unevenly, leading to unstable optimization—evident in blurry samples and high FID scores. The core issue is a conflict between two opposing forces: terms that amplify variance over long time spans and strong constraints needed near the start of generation, which a fixed sampling strategy cannot reconcile. To resolve this, we propose Temporal Equilibrium MeanFlow (TEMF), which balances these competing demands through two simple yet effective components: (1) a temporal equilibrium weighting function that equalizes gradient influence across all time scales, and (2) a dynamic boundary scheduler that gradually shifts training focus—from stabilizing early steps to refining the full trajectory as training progresses. Without changing the model architecture, TEMF retains true one-step generation with classifier-free guidance, achieving a state-of-the-art FID of 2.62 on ImageNet 256×256—achieving the best results among diffusion- and flow-based one-step methods.
</details>

---

### Demo2Tutorial: From Human Experience to Multimodal Software Tutorials
著者: Zechen Bai, Zhiheng Chen, Yiqi Lin, Kevin Qinghong Lin, Difei Gao, Xiangwu Guo, WANG XIN, Mike Zheng Shou

<details>
<summary> 日本語要旨 </summary>

デジタル環境における人間の経験は、豊富で未開拓な資源として、本物の、整形されていない相互作用を含み、豊かな手続き的知識が詰まっています。私たちは「Demo2Tutorial」というフレームワークを紹介します。これはスクリーン録画とインタラクションログによって捉えられた経験を構造化されたマルチモーダルなソフトウェアチュートリアルに変換し、人間およびエージェントの教育に利用します。Demo2Tutorialはまず専用レコーダーを使用して人間の経験を収集し、その後マルチモーダルアクションパーサーを用いて原始的な経験を解析し、知覚、行動、意図を再構築します。次にステッププランナーがこれらのステップを階層的タスクグラフとして抽象化し、目標や手順を表現します。最後にチュートリアルコンポーザーが解析された経験を構造化され再利用可能な画像テキストの指示に変換します。私たちは新しいベンチマーク（公式ソフトウェアドキュメンテーションから導出）を使用してチュートリアル生成の品質を評価します。さらに、この抽出された表現が(i) 人間の学習（マルチモーダルチュートリアルの自動生成によって）および(ii) エージェントの学習（GUIエージェントの計画と一般化を改善することで）に利益をもたらすことを示します。実験結果は、Demo2Tutorialが人間作成のチュートリアルを超える高品質なチュートリアルを生成し、ベースライン手法を大幅に上回りつつ、より迅速な人間タスク完了と改善されたGUIエージェント計画を可能にすることを示しています。これは構造化チュートリアルが人間の経験から抽出されることで、効果的な知識表現として両方の人間学習および最終的にエージェント能力を進展させるために役立つことを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Human experience in digital environments offers a vast, underexplored resource of authentic, untrimmed interactions that contain rich procedural knowledge. We introduce Demo2Tutorial, a framework that transforms this experience captured via screen recordings and interaction logs into structured, multimodal software tutorials for teaching both humans and agents. Demo2Tutorial first collects human experience via a dedicated recorder, then parses raw experience using a multimodal Action Parser to reconstruct perception, action, and intent. A Step Planner then abstracts these steps into hierarchical task graphs representing goals and steps. Finally, a Tutorial Composer transforms the parsed experience into structured, reusable image-text instructions. We evaluate the tutorial generation quality on a new benchmark derived from official software documentation. We further demonstrate that this distilled representation benefits (i) human learning, by automatically generating multimodal tutorials, and (ii) agent learning, by improving downstream GUI-agent planning and generalization. Experiments show Demo2Tutorial produces high-quality tutorials that surpass human-authored ones and significantly outperform baseline methods, while enabling both faster human task completion and improved GUI agent planning, demonstrating that structured tutorials distilled from human experience can serve as effective knowledge representations for advancing both human learning and, ultimately, agent capabilities.
</details>

---

### Ego2Web: A Web Agent Benchmark Grounded on Egocentric Videos
著者: Shoubin Yu, Lei Shu, Antoine Yang, Yao Fu, Srinivas Sunkara, Maria Wang, Jindong Chen, Mohit Bansal, Boqing Gong

<details>
<summary> 日本語要旨 </summary>

多様なモーダルAIエージェントは、オンラインでの実行を伴う複雑な現実世界のワークフローをますます自動化しています。しかし、現在のウェブエージェントベンチマークには重大な制限があります：それらは完全にウェブベースのインタラクションと知覚に焦点を当てており、ユーザーの現実世界の物理的環境に根ざしていません。この制限は、エージェントがARグラスなどを通じた自己中心的視覚知覚を使用してユーザーの周囲のオブジェクトを認識し、その後に関連するタスク（例えば購入）をオンラインで完了する必要がある重要なシナリオでの評価を妨げます。このギャップを埋めるため、私たちはEgo2Webを導入します。これは、自己中心的ビデオ知覚と多様なモーダルウェブエージェント実行の間に架け橋を築く最初のベンチマークです。Ego2Webは、成功した完了のためにビジュアル理解、ウェブタスク計画、オンライン環境でのインタラクションを必要とする実際の世界の一人称ビデオ録画とウェブタスクを組み合わせています。多様なウェブタスクタイプ（eコマース、ナビゲーション、メディア検索など）にわたるよく構築された高品質のビデオ-タスクペアをキュレートするために、自動データ生成パイプラインと人間による確認を組み合わせて使用しています。私たちのユニークなベンチマークの正確でスケーラブルな評価を容易にするため、LLM-as-a-Judge自動評価方法Ego2WebJudgeも開発しました。これは人間の判断と約85％の一致を示しており、既存の評価方法よりも大幅に高いです。多様な最先端の多モーダルエージェントでの実験では、彼らが人間レベルをはるかに下回っており、能力の大きなギャップを明らかにしています。また、タスク設計に関する包括的な削減研究も行い、提案されたタスクでのビデオ知覚の必要性と現在のエージェントの制限を強調しています。私たちはEgo2Webが物理的およびデジタル世界間で見る、理解し、行動することができる本当に能力のあるAIアシスタントを開発するための重要な新リソースになることを願っています。
</details>

<details>
<summary> 英語要旨 </summary>

Multimodal AI agents are increasingly automating complex real-world workflows that involve online web execution. However, current web-agent benchmarks suffer from a critical limitation: they focus entirely on web-based interaction and perception, lacking grounding in the user's real-world physical surroundings. This limitation prevents evaluation in crucial scenarios, such as when an agent must use egocentric visual perception (e.g., via AR glasses) to recognize an object in the user's surroundingsand then complete a related task online (e.g., making a purchase). To address this gap, we introduce Ego2Web, the first benchmark designed to bridge egocentric video perception and multimodal web agent execution. Ego2Web pairs real-world first-person video recordings with web tasks that require visual understanding, web task planning, and interaction in an online environment for successful completion. We utilize an automatic data-generation pipeline combined with human verification to curate well-constructed, high-quality video-task pairs across diverse web task types, including e-commercial, navigation, media search, and so on. To facilitate a more accurate and scalable evaluation for our novel benchmark, we also develop a novel LLM-as-a-Judge automatic evaluation method Ego2WebJudge, and demonstrate around 85\% agreement with human judgment, substantially higher than existing evaluation methods. Experiments with diverse SoTA multimodal agents show that they perform significantly below the human level, revealing a major gap in capability. We also conduct a comprehensive ablation study on task design, highlighting the necessity of video perception in the proposed task and the limitations of current agents. We hope Ego2Web can be a critical new resource for developing truly capable AI assistants that can seamlessly see, understand, and act across the physical and digital worlds.
</details>

---

### Spe-BEVHead: Rethinking The Detection Head Design for Bird’s-Eye-View Object Detection
著者: Junshu Zhang, Sicheng Zhao, Xin Zhao, Fan Yang, Ruike Chen, Jungong Han, Guiguang Ding

<details>
<summary> 日本語要旨 </summary>

自動運転における3次元物体検出の分野で、鳥瞰図（BEV）検出が支配的なパラダイムとして台頭しています。これはその強力な認識能力によるものです。しかし、既存の多くの方法は高品質なBEV特徴表現を構築することに主眼を置いており、タスク固有の検出ヘッドの設計を軽視しています。実際には、2D検出用に開発された中心点ベースのヘッドをそのまま採用し、特定の最適化を行っていないことが多いです。これにより以下の3つの固有の制限が生じます：（i）分類に使用されるガウスカーネルと実際のBEVオブジェクトとの幾何学的不一致、（ii）非最大抑制(NMS)なしではエンドツーエンド性能が低下すること、および（iii）監督信号の希薄化。これらの問題に対処するため、我々はBEV 3次元物体検出専用に設計された検出ヘッドであるSpe-BEVHeadを提案します。Spe-BEVHeadは以下の3つのBEV特有の適応を導入しています：（1）幾何学的に整合した分類重みを生成する回転ボックスカーネル、（2）非ピーク応答を抑制しエンドツーエンド性能を向上させるローカルレスポンスリファインメントモジュール(LRRM)、および（3）より豊富な監督信号を提供しエンドツーエンド推論における性能を本質的に保持しつつ、より堅牢な学習を促進するデュアルブランチアーキテクチャ。広範囲の実験は、Spe-BEVHeadが既存のBEVバックボーンにシームレスに統合可能であり、エンドツーエンド設定下でも競争力のある性能を維持しつつ直接的なパフォーマンス向上をもたらすことを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Bird’s-Eye-View (BEV) detection has become a dominant paradigm for 3D object detection in autonomous driving, due to its strong perception capability. However, most existing methods mainly focus on constructing high-quality BEV feature representations, while neglecting the design of task-specific detection heads. In practice, they directly adopt the center-based head originally developed for 2D detection, without any specific optimization. This leads to three inherent limitations: (i) a geometric mismatch between the Gaussian kernel used for classification and the real BEV object, (ii) degraded end-to-end performance without Non-Maximum Suppression(NMS), and (iii) sparse supervisory signals. To address these issues, we propose Spe-BEVHead, a detection head specifically tailored for BEV 3D object detection. Spe-BEVHead introduces three BEV-specific adaptations: (1) a Rotated Box Kernel that generates geometry-aligned classification weights, (2) a Local Response Refinement Module (LRRM) that suppresses non-peak responses and improves end-to-end performance, and (3) a dual-branch architecture that provides richer supervisory signals to promote more robust learning while inherently preserving the performance for end-to-end inference. Extensive experiments show that Spe-BEVHead can be seamlessly integrated into existing BEV backbones, delivering direct performance gains while retaining competitive performance under the challenging end-to-end setting.
</details>

---

### Retrieving Counterfactuals Improves Visual In-Context Learning
著者: Guangzhi Xiong, Sanchit Sinha, Zhenghao He, Aidong Zhang

<details>
<summary> 日本語要旨 </summary>

ビジョン言語モデル（VLMs）は、多様なマルチモーダル推論タスクにおいて印象的な性能を達成していますが、細かい視覚属性の分離や基礎となる因果関係の理解にはしばしば苦労します。イン・コンテキスト学習（ICL）はVLMsが新しいタスクに適応するための有望な手段を提供しますが、その効果はデモンストレーション例の選択に大きく依存しています。既存のリトリーバル強化アプローチは通常、受動的な類似性に基づいた検索を利用し、これが相関するものの非因果的な例を選択し、誤った関連付けを増幅させてモデルの堅牢性を制限します。私たちはCIRCLES（Composed Image Retrieval for Causal Learning Example Selection）という新しいフレームワークを導入します。これは、属性に基づく構成画像検索を通じて対照的な例を積極的に取得することでデモンストレーションセットを構築します。CIRCLESは、属性と結果の間の因果関係を理解するために対照的なスタイルの例を取り入れることで、表面的な相関を超えてより堅牢かつ因果的に根拠のある推論を促進します。四つの多様なデータセットにわたる包括的な実験は、CIRCLESが特に小規模モデルで既存手法を一貫して上回り、情報不足時に顕著な向上を示すことを示しています。さらに、CIRCLESはより多様で因果的に有益な例を取得し、モデルが改善された推論のためにイン・コンテキストのデモンストレーションをどのように活用するかについての質的洞察を提供します。
</details>

<details>
<summary> 英語要旨 </summary>

Vision-language models (VLMs) have achieved impressive performance across a wide range of multimodal reasoning tasks, but they often struggle to disentangle fine-grained visual attributes and reason about underlying causal relationships. In-context learning (ICL) offers a promising avenue for VLMs to adapt to new tasks, but its effectiveness critically depends on the selection of demonstration examples. Existing retrieval-augmented approaches typically rely on passive similarity-based retrieval, which tends to select correlated but non-causal examples, amplifying spurious associations and limiting model robustness. We introduce CIRCLES (Composed Image Retrieval for Causal Learning Example Selection), a novel framework that actively constructs demonstration sets by retrieving counterfactual examples through targeted, attribute-guided composed image retrieval. By incorporating counterfactual-style examples, CIRCLES enables VLMs to reason about the causal relations between attributes and outcomes, moving beyond superficial correlations and fostering more robust and causally grounded reasoning. Comprehensive experiments on four diverse datasets demonstrate that CIRCLES consistently outperforms existing methods across multiple architectures, especially on small-scale models, with pronounced gains under information scarcity. Furthermore, CIRCLES retrieves more diverse and causally informative examples, providing qualitative insights into how models leverage in-context demonstrations for improved reasoning.
</details>

---

### SynMotion: Semantic-Visual Adaptation for Motion Customized Video Generation
著者: Shuai Tan, Biao Gong, Yujie Wei, Shiwei Zhang, Zhuoxin Liu, Ke Ma, Yan Wang, Kecheng Zheng, Xing Zhu, Yujun Shen, Hengshuang Zhao

<details>
<summary> 日本語要旨 </summary>

拡散ベースのビデオ動作カスタマイズは、少数のビデオサンプルから人間の動作表現を取得し、正確なテキスト条件付けによって任意の主題への転送を実現します。既存のアプローチはしばしばセマンティックレベルでの整合性に依存し、新たな動作概念（例えば猫や犬など）を学習して他のエンティティと組み合わせて視覚的に魅力的な結果を生み出すことを期待します。しかし、ビデオデータは複雑な空間時間パターンを含んでおり、セマンティックレベルのみに焦点を当てると動作の視覚的複雑さが見過ごされます。一方、視覚表現の調整だけでは意図したアクションのセマンティックな混乱を引き起こします。これらの制限に対処するため、我々は新しい動作カスタマイズビデオ生成モデルであるSynMotionを提案します。このモデルはセマンティックガイダンスと視覚適応の両方を組み合わせて利用します。セマンティックレベルでは、主題と動作表現を分離する二重埋め込みセマンティック理解メカニズムを導入し、モデルがカスタマイズされた動作特徴を学習しつつ多様な主題に対する生成能力を保持できるようにします。視覚レベルでは、事前学習済みのビデオ生成モデルにパラメータ効率的な動作アダプターを統合し、動作忠実性と時間的一貫性を向上させます。また、新たな埋め込み特化トレーニング戦略を導入し、手動で構築されたSubject Prior Video（SPV）トレーニングデータセットによってサポートされる主題と動作埋め込みの交互最適化を行います。この戦略は、多様な主題にわたる汎用性を保持しつつ動作特異性を促進します。最後に、MotionBenchという新たに編纂されたベンチマークを導入しました。これは多様な動作パターンを含んでいます。T2VおよびI2Vの両設定にわたる実験結果では、SynMotionが既存のベースラインを上回っていることが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

Diffusion-based video motion customization facilitates the acquisition of human motion representations from a few video samples, while achieving arbitrary subjects transfer through precise textual conditioning. Existing approaches often rely on semantic-level alignment, expecting the model to learn new motion concepts and combine them with other entities (e.g., cats or dogs) to produce visually appealing results. However, video data involve complex spatio-temporal patterns, and focusing solely on semantics cause the model to overlook the visual complexity of motion. Conversely, tuning only the visual representation leads to semantic confusion in representing the intended action. To address these limitations, we propose SynMotion, a new motion-customized video generation model that jointly leverages semantic guidance and visual adaptation. At the semantic level, we introduce the dual-embedding semantic comprehension mechanism which disentangles subject and motion representations, allowing the model to learn customized motion features while preserving its generative capabilities for diverse subjects. At the visual level, we integrate parameter-efficient motion adapters into a pre-trained video generation model to enhance motion fidelity and temporal coherence. Furthermore, we introduce a new embedding-specific training strategy which alternately optimizes subject and motion embeddings, supported by the manually constructed Subject Prior Video (SPV) training dataset. This strategy promotes motion specificity while preserving generalization across diverse subjects. Lastly, we introduce MotionBench, a newly curated benchmark with diverse motion patterns. Experimental results across both T2V and I2V settings demonstrate that SynMotion outperforms existing baselines.
</details>

---

### Bidirectional Normalizing Flow: From Data to Noise and Back
著者: Yiyang Lu, Qiao Sun, Xianbang Wang, Zhicheng Jiang, Hanhong Zhao, Kaiming He

<details>
<summary> 日本語要旨 </summary>

正規化フロー（NF）は、データを単純な事前分布にマッピングする前方過程と、このマッピングの逆転によってサンプルを生成する後方過程から成る、原理的な生成モデリングフレームワークです。従来のアプローチは、厳密な可逆性の要件の下で表現力豊かな前方変換を設計することに焦点を当てており、後方過程がその正確な解析的逆関数として機能します。最近の進歩であるTARFlowは、トランスフォーマーと自己回帰構造を用いて前方モデルを強化し、生成品質が最先端レベルに達していますが、その代償として自己回帰的な復号のためにサンプリング速度が低下します。本研究では、正確な解析的逆関数を必要としない新しいフレームワークである双方向正規化フロー（**BiFlow**）を導入します。これにより、データ駆動型の柔軟な逆モデルを用いて逆マッピングを**近似**することが可能になります。この緩和は、NFsの確率的基盤を保持しながら、より豊かなアーキテクチャや損失関数の形成を可能にします。BiFlowは直接的で単一前方（1-NFE）生成を行い、自己回帰ボトルネックを排除し、最大2桁速くサンプリングしながら生成品質も向上させます。この研究が正規化フローを直接的で柔軟性のある効率的な生成モデルとして再考するきっかけになれば幸いです。
</details>

<details>
<summary> 英語要旨 </summary>

Normalizing Flows (NFs) are a principled framework for generative modeling, consisting of a forward process and a reverse process. The forward process maps data to a simple prior distribution, while the reverse process generates samples by inverting this mapping. Traditional approaches focus on designing expressive forward transformations under strict requirement of explicitly invertibility, so that the reverse process can serve as their exact analytic inverse. Recent advances such as TARFlow enhance the forward model with Transformers and autoregressive structures, achieving state-of-the-art generation quality—but at the expense of slow sampling due to autoregressive decoding. In this work, we introduce Bidirectional Normalizing Flow ($\textbf{BiFlow}$), a new framework that removes the need for an exact analytic inverse by learning a flexible, data-driven reverse model to $\textbf{approximate}$ the inverse mapping. This relaxation enables richer architectures and loss formulations while preserving the probabilistic foundation of NFs. BiFlow performs direct, single-forward (1-NFE) generation, eliminating autoregressive bottlenecks and achieving up to two orders of magnitude faster sampling with improved generation quality. We hope this work encourages rethinking Normalizing Flows as direct, flexible, and efficient generative models.
</details>

---

### SURF: Signature-retained Fast Video Generation
著者: Kaixin Ding, Xi Chen, Sihui Ji, Yuan Gao, Liang Hou, Xin Tao, Hengshuang Zhao

<details>
<summary> 日本語要旨 </summary>

高解像度ビデオ生成の需要は急速に増加しています。しかし、生成解像度は遅い推論速度によって厳しく制約されています。例えば、Wan2.1では単一の720pビデオを生成するのに50分以上かかります。以前の研究では、さまざまな側面からビデオ生成を加速する方法を探ってきましたが、多くは元モデルの特徴的なサイン（例えばレイアウト、セマンティクス、動作）を犠牲にしています。本研究では、高解像度ビデオ生成を効率的に行いつつ、特徴的なサインを最大限保持するための**SURF**というフレームワークを提案します。具体的には、SURFはビデオ生成を2段階に分けます：まず、予め学習されたモデルを最適解像度で推論し、低解像度のプレビューを高速に生成するために潜在変数をダウンサンプリングします。次に、Refinerと呼ばれるアップスケーラーを設計してプレビューを拡大します。プレビューステージでは、高解像度で学習されたモデルを低解像度で直接推論すると特徴的なサインが大幅に失われることを発見しました。そこで、初期のノイズ除去ステップを元の解像度で行い、後の段階で低解像度に切り替えるトレーニング不要な技術である「ノイズリシフト」を導入し、この問題を緩和します。Refineステージでは、プレビューと高解像度のターゲット間にマッピング関係を確立し、これによりノイズ除去ステップが大幅に削減されます。さらに、シフトウィンドウを統合し、訓練パラダイムを慎重に設計することで強力かつ効率的なRefinerを得ています。このようにSURFは、与えられた予め学習されたモデルの特徴的なサインに最大限近い形で高解像度ビデオ生成を効率的に行うことが可能です。SURFは概念的にシンプルで、さまざまな基本モデルや加速方法と互換性のあるプラグインとして利用できます。例えば、Wan 2.1を使用した5秒間、16fps、720pビデオ生成において12.5倍の高速化を達成し、HunyuanVideoを使用した同じく5秒間、24fps、720pビデオ生成では8.7倍の高速化を達成しています。
</details>

<details>
<summary> 英語要旨 </summary>

The demand for high-resolution video generation is growing rapidly. However, the generation resolution is severely constrained by slow inference speeds. For instance, Wan2.1 requires over 50 minutes to generate a single 720p video. While previous works explore accelerating video generation from various aspects, most of them compromise the distinctive signatures (e.g., layout, semantic, motion) of the original model. In this work, we propose **SURF**, an efficient framework for generating high-resolution videos, while maximally keeping the signatures. Specifically, SURF divides video generation into two stages: First, we leverage the pretrained model to infer at optimal resolution and downsample latent to generate low-resolution previews in fast speed; then we design a Refiner to upscale the preview. In the preview stage, we identify that directly inferring a model (trained with higher resolution) on lower resolution causes severe losses in signatures. So we introduce noise reshifting, a training-free technique that mitigates this issue by conducting initial denoising steps on the original resolution and switching to low resolution in later steps. In the refine stage, we establish a mapping relationship between the preview and the high-resolution target, which significantly reduces the denoising steps. We further integrate shifting windows and carefully design the training paradigm to get a powerful and efficient Refiner. In this way, SURF enables generating high-resolution videos efficiently while maximally closer to the signatures of the given pretrained model. SURF is conceptually simple and could serve as a plug-in that is compatible with various base model and acceleration methods. For example, it achieves 12.5× speedup for generating 5-second, 16fps, 720p Wan 2.1 videos and 8.7× speedup for generating 5-second, 24fps, 720p HunyuanVideo.
</details>

---

### Qwen-Image-Layered: Towards Inherent Editability Via Layer Decomposition
著者: Shengming Yin, Zekai Zhang, Zecheng Tang, Kaiyuan Gao, Xiao Xu, Kun Yan, Jiahao Li, Yilei chen, Yuxiang Chen, Heung-Yeung Shum, Lionel Ni, Junyang Lin, Chenfei Wu

<details>
<summary> 日本語要旨 </summary>

最近の視覚生成モデルは、すべてのビジュアルコンテンツが単一のキャンバスに融合されるラスタ画像の絡み合った性質により、画像編集中の一貫性を保つことが難しい。これに対して、プロフェッショナルなデザインツールはレイヤー表現を使用し、個別の編集を可能にしながら一貫性を保つことができる。この動機から、私たちはQwen-Image-Layeredを提案する。これは、単一のRGB画像を複数のセマンティックに分離されたRGBAレイヤーに分解し、それぞれのRGBAレイヤーが独立して操作できるエンドツーエンドの拡散モデルである。変数長の分解をサポートするために、次の3つの重要なコンポーネントを導入する：（1）RGBとRGBA画像の潜在表現を統一するためのRGBA-VAE；（2）変数数の画像レイヤーを分解できるVLD-MMDiT（Variable Layers Decomposition MMDiT）アーキテクチャ；および（3）事前学習された画像生成モデルをマルチレイヤー画像分解器に適応させるMulti-stage Training戦略。また、高品質なマルチレイヤー訓練画像の不足に対処するために、Photoshopドキュメント（PSD）からマルチレイヤー画像を抽出・注釈付けするパイプラインを構築する。実験では、私たちの方法が分解品質において既存手法を大きく上回り、一貫した画像編集の新しいパラダイムを確立していることを示す。
</details>

<details>
<summary> 英語要旨 </summary>

Recent visual generative models often struggle with consistency during image editing due to the entangled nature of raster images, where all visual content is fused into a single canvas. In contrast, professional design tools employ layered representations, allowing isolated edits while preserving consistency. Motivated by this, we propose Qwen-Image-Layered, an end-to-end diffusion model that decomposes a single RGB image into multiple semantically disentangled RGBA layers, enabling inherent editability, where each RGBA layer can be independently manipulated without affecting other content. To support variable-length decomposition, we introduce three key components: (1) an RGBA-VAE to unify the latent representations of RGB and RGBA images; (2) a VLD-MMDiT (Variable Layers Decomposition MMDiT) architecture capable of decomposing a variable number of image layers; and (3) a Multi-stage Training strategy to adapt a pretrained image generation model into a multilayer image decomposer. Furthermore, to address the scarcity of high-quality multilayer training images, we build a pipeline to extract and annotate multilayer images from Photoshop documents (PSD). Experiments demonstrate that our method significantly surpasses existing approaches in decomposition quality and establishes a new paradigm for consistent image editing.
</details>

---

### Toward Diffusible High-Dimensional Latent Spaces: A Frequency Perspective
著者: Bolin Lai, XuDong Wang, Sai Saketh Rambhatla, James Rehg, Zsolt Kira, Rohit Girdhar, Ishan Misra

<details>
<summary> 日本語要旨 </summary>

ラテントディファレンシエーションは視覚生成の標準的なパラダイムとなっていますが、ラテント次元性が増加するにつれて再構成-生成トレードオフが持続していることを観察します：より高容量の自己符号化器は再構成精度を向上させますが、最終的に生成品質は低下します。このギャップを高周波トークン化とデトークン化の異なる挙動に起因するものとして追跡します。RGBおよびラテントドメインの両方で制御された摂動を通じてエンコーダ/デコーダの挙動を分析し、デコーダが詳細を回復するために高周波ラテント成分に強く依存していることを発見します。一方、エンコーダは高周波コンテンツを過小表現し、ディファレンシエーションモデルのトレーニングにおける高周波帯での不十分な露出とアンダフィッティングを引き起こします。この問題に対処するため、私たちはFreqWarmを導入します。これはプラグアンドプレイの周波数ウォームアップカリキュラムであり、ディファレンシエーションまたはフローマッチングトレーニング中に高周波ラテント信号への初期段階の露出を増加させますが、自己符号化器を変更したり再訓練することなく行います。複数の高次元トークナイザーに適用されると、FreqWarmは一貫して生成品質を向上させます：Wan2.2-VAEでgFIDを14.11減少、LTX-VAEで6.14減少、DC-AE-f32で4.42減少し、アーキテクチャに依存しないまま多様なバックボーンとの互換性を保ちます。私たちの研究は、周波数露出を明示的に管理することで高次元ラテント空間をよりディファレンシエーション可能なターゲットに変えることが成功することを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Latent diffusion has become the default paradigm for visual generation, yet we observe a persistent reconstruction–generation trade-off as latent dimensionality increases: higher-capacity autoencoders improve reconstruction fidelity but generation quality eventually declines. We trace this gap to the different behaviors in high-frequency tokenization and detokenization. Through controlled perturbations in both RGB and latent domains, we analyze encoder/decoder behaviors and find that decoders depend strongly on high-frequency latent components to recover details, whereas encoders under-represent high-frequency contents, yielding insufficient exposure and underfitting in high-frequency bands for diffusion model training. To address this issue, we introduce FreqWarm, a plug-and-play frequency warm-up curriculum that increases early-stage exposure to high-frequency latent signals during diffusion or flow-matching training -- without modifying or retraining the autoencoder. Applied across several high-dimensional tokenizers, FreqWarm consistently improves generation quality: decreasing gFID by 14.11 on Wan2.2-VAE, 6.14 on LTX-VAE, and 4.42 on DC-AE-f32, while remaining architecture-agnostic and compatible with diverse backbones. Our study shows that explicitly managing frequency exposure can successfully turn high-dimensional latent spaces into more diffusible targets.
</details>

---

### Unlocking The Power of Critical Factors for 3D Visual Geometry Estimation
著者: Guangkai Xu, Hua Geng, Huanyi Zheng, Songyi Yin, Yanlong Sun, Hao Chen, Chunhua Shen

<details>
<summary> 日本語要旨 </summary>

最近のフィードフォワードアーキテクチャを用いた視覚幾何学推定における進展は顕著である。興味深いことに、一枚ごとの視覚幾何学推定アプローチは通常、マルチフレームの一貫性が弱くなりがちだが、単一フレームの精度ではマルチフレームアルゴリズムを上回る。この観察結果は、モデルパフォーマンスに影響を与える重要な要因を体系的に調査する動機となり、厳密なアブレーション研究を通じて3つの主要な洞察が明らかにされた：1) データの多様性と品質を拡大することで、最先端の視覚幾何学推定手法でもさらなるパフォーマンス向上が可能である；2) 一般的に採用されている信頼度意識型損失関数と勾配ベースの損失メカニズムは、意図せずパフォーマンスを妨げる可能性がある；3) シーケンス全体およびフレームごとの整合性に基づく共同監督が結果を改善する一方で、局所領域の整合性はパフォーマンスを意外にも低下させる。また、最適化ベース手法と高解像度入力の利点を統合するための2つの改善策を導入した：深度マップ、カメラパラメータ、およびポイントマップ間の整合性を強制する一貫性損失関数と、高解像度幾何学推定を可能にする効率的なアーキテクチャ設計である。これらの貢献はCFGモデルに統合されており、このモデルは多様な入力視点から高解像度で精密かつ一貫した幾何学的表現を同時に生成する。ポイントクラウド再構築、ビデオ深度推定、およびカメラ姿勢/固有パラメータ推定の複数のベンチマークでの包括的なテストにより、CFGの優れた性能が確認され、視覚幾何学タスクにおける最先端ソリューションとしての地位を確立した。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advancements in feed-forward architectures for visual geometry estimation have achieved significant progress. Interestingly, per-frame visual geometry estimation approaches typically exhibit weaker multi-frame consistency but demonstrate superior per-frame accuracy compared to multi-frame algorithms. This observation motivates our systematic investigation into the critical factors driving model performance through rigorous ablation studies, which reveals three key insights: 1) Scaling up data diversity and quality unlocks further performance gains even in state-of-the-art visual geometry estimation methods; 2) Commonly adopted confidence-aware loss and gradient-based loss mechanisms may unintentionally hinder performance; 3) Joint supervision through both per-sequence and per-frame alignment improves results, while local region alignment surprisingly degrades performance. Furthermore, we introduce two enhancements to integrate the advantages of optimization-based methods and high-resolution inputs: a consistency loss function that enforces alignment between depth maps, camera parameters, and point maps, and an efficient architectural design that enables high-resolution geometry estimation. These contributions are integrated into CFG, a model that simultaneously generates precise and coherent geometric representations from diverse input perspectives at high resolutions. Comprehensive testing across multiple benchmarks for point cloud reconstruction, video depth estimation, and camera pose/intrinsic parameter estimation confirms CFG's superior performance, establishing it as a state-of-the-art solution for visual geometry tasks.
</details>

---

### Proxy3D: Efficient 3D Representations for Vision-Language Models Via Semantic Clustering and Alignment
著者: Jerry Jiang, Haowen Sun, Denis Gudovskiy, Yohei Nakata, Tomoyuki Okuno, Kurt Keutzer, Wenzhao Zheng

<details>
<summary> 日本語要旨 </summary>

ビジョン言語モデル（VLM）における空間知性は、実用的な要求から3次元世界での推論を行うために研究者の関心を集めています。しかし、多くの既存手法がVLMsにおける従来の2Dパイプラインに従い、ビジョンモダリティーでピクセルアラインメントされた表現を使用しているにもかかわらず、暗黙的な3次元シーン理解を持つ対応モデルは空間一貫性を達成することができず、3D幾何学的事前知識を持つ表現ベースのモデルはビジョンシーケンスのシリアライズに効率が欠けています。これに対処するため、我々は3Dプロキシ表現を提案します。この方法はビジョンモダリティーにとってコンパクトでありながら包括的です。入力として動画フレームのみを与える場合、我々はセマンティックおよび幾何学エンコーダーを用いてシーン特徴を抽出し、そのセマンティックに対応したクラスタリングを行うことで3次元空間内のプロキシの集合を得ます。表現の整合性を図るために、さらにSpaceSpanデータセットを編纂し、複数段階のトレーニングを適用して提案された3Dプロキシ表現をVLMと組み合わせます。ビジョン情報においてより短いシーケンスを使用する場合、我々の方法は3次元視覚質問応答、視覚的アンカリング、一般的な空間知性ベンチマークにおいて競争力のあるまたは最先端のパフォーマンスを達成します。
</details>

<details>
<summary> 英語要旨 </summary>

Spatial intelligence in vision-language models (VLMs) attracts research interest with the practical demand to reason in the 3D world. Despite promising results, most existing methods follow the conventional 2D pipeline in VLMs and use pixel-aligned representations for the vision modality. However, correspondence-based models with implicit 3D scene understanding often fail to achieve spatial consistency, and representation-based models with 3D geometric priors lack efficiency in vision sequence serialization. To address this, we propose a Proxy3D method with compact yet comprehensive 3D proxy representations for the vision modality. Given only video frames as input, we employ semantic and geometric encoders to extract scene features and then perform their semantic-aware clustering to obtain a set of proxies in the 3D space. For representation alignment, we further curate the SpaceSpan dataset and apply multi-stage training to adopt the proposed 3D proxy representations with the VLM. When using shorter sequences for vision information, our method achieves competitive or state-of-the-art performance in 3D visual question answering, visual grounding and general spatial intelligence benchmarks.
</details>

---

### DrivePI: Spatial-aware 4D MLLM for Unified Autonomous Driving Understanding, Perception, Prediction and Planning
著者: Zhe Liu, Runhui Huang, Rui Yang, Siming Yan, Zining Wang, Lu Hou, Di Lin, Xiang Bai, Hengshuang Zhao

<details>
<summary> 日本語要旨 </summary>

多モーダル大規模言語モデル（MLLMs）は、さまざまな分野で顕著な能力を示していますが、細部にわたる3D知覚と予測出力を統一フレームワーク内で生成する応用は未だ十分に探求されていません。本論文では、自動運転のための新しい空間認識型4D MLLMであるDrivePIを提案します。これはビジョン・ランゲージ・アクション（VLA）フレームワークとして機能し、空間理解、3D知覚（すなわち3D占有）、予測（すなわち占有流れ）、計画（すなわちアクション出力）を並列に行うための共同最適化を通じて機能します。私たちはこれを4D MLLMと呼びます。なぜなら、それは3D占有と流れの両方を出力し、細部にわたる空間時間ダイナミクスを捉えているからです。具体的には、正確な幾何学情報と豊かな外観を捉えるために、私たちのアプローチは単一のMLLMアーキテクチャ内で点群、マルチビュー画像、言語指示を統合しています。驚くべきことに、0.5B Qwen2.5モデルのみを使用した私たちが提案するDrivePIは、テキストシーン理解能力を維持しつつ、3D知覚、予測、計画タスクにおいて競争力のあるパフォーマンスを達成しています。さらに、DrivePIはこれらのタスクにおいてほとんどの専門的なビジョンベースのモデルを上回り、私たちの統一アプローチの効果を強調しています。この新しいVLAフレームワークが将来の研究にインスピレーションを与え、言語的推論と細部にわたる3D出力を通じて解釈可能性と説明可能な意思決定を向上させた自動運転システムの開発を促進することを期待しています。将来の研究を支援するために、コードとアノテーション付きデータセットを公開します。
</details>

<details>
<summary> 英語要旨 </summary>

Although multimodal large language models (MLLMs) have shown remarkable capabilities across diverse domains, their application in generating fine-grained 3D perception and prediction outputs within a unified framework remains underexplored. In this paper, we propose DrivePI, a novel spatial-aware 4D MLLM that serves as a unified Vision-Language-Action (VLA) framework for autonomous driving, performing spatial understanding, 3D perception (i.e., 3D occupancy), prediction (i.e., occupancy flow), and planning (i.e., action outputs) in parallel through joint optimization. We term it 4D MLLM as it outputs both 3D occupancy and flow, capturing fine-grained spatial-temporal dynamics. Specifically, to capture both precise geometric information and rich appearance, our approach integrates point clouds, multi-view images and language instructions within a single MLLM architecture. Remarkably, despite utilizing only a 0.5B Qwen2.5 model as the MLLM, our proposed DrivePI still maintains promising textual scene understanding while achieving competitive performance in 3D perception, prediction, and planning tasks. Moreover, DrivePI even surpasses most specialized vision-based models across these tasks, highlighting the effectiveness of our unified approach. We hope this new VLA framework can inspire future research to enhance autonomous driving systems with improved interpretability and explainable decision-making through language reasoning and fine-grained 3D outputs. To facilitate future research, we will release the code and annotated datasets.
</details>

---

### Language Models Can Explain Visual Features Via Steering
著者: Javier Ferrando, Enrique Lopez-Cuena, Pablo Agustin Martin-Torres, Daniel Hinjos, Anna Arias Duart, Dario Garcia-Gasulla

<details>
<summary> 日本語要旨 </summary>

自己符号化器はビジョンモデルに数千の特徴を明らかにしますが、人間介入なしでこれらの特徴を説明することは依然として開いた課題です。以前の研究では、トップアクティベーションを引き起こす入力例に基づく相関ベースの説明生成が提案されていますが、私たちは因果的介入に基づく根本的に異なる代替手法を提示します。ビジョン言語モデルの構造を活用し、空白画像を提供した後で個々の自己符号化器特徴を視覚エンコーダー内で操作します。その後、言語モデルに「見えるもの」を説明させることで、各特徴が表現する視覚的概念を効果的に引き出します。結果は、Steeringが伝統的な入力例ベースのアプローチを補完し、ビジョンモデルにおける自動解釈可能性の新たな軸としてスケーラブルな代替手段であることを示しています。さらに、説明の質は言語モデルの規模と一貫して向上し、私たちの方法が将来の研究における有望な方向性であることを強調します。最後に、因果的介入と入力ベースアプローチの強みを組み合わせたSteering-informed Top-kというハイブリッド手法を提案し、追加の計算コストなしで最先端の説明品質を達成します。
</details>

<details>
<summary> 英語要旨 </summary>

Sparse Autoencoders uncover thousands of features in vision models, yet explaining these features without requiring human intervention remains an open challenge. While previous work has proposed generating correlation-based explanations based on top activating input examples, we present a fundamentally different alternative based on causal interventions. We leverage the structure of Vision-Language Models and steer individual SAE features in the vision encoder after providing an empty image. Then, we prompt the language model to explain what it "sees", effectively eliciting the visual concept represented by each feature. Results show that Steering offers an scalable alternative that complements traditional approaches based on input examples, serving as a new axis for automated interpretability in vision models. Moreover, the quality of explanations improves consistently with the scale of the language model, highlighting our method as a promising direction for future research. Finally, we propose Steering-informed Top-k, a hybrid approach that combines the strengths of causal interventions and input-based approaches to achieve state-of-the-art explanation quality without additional computational cost.
</details>

---

### R-4B: Incentivizing General-Purpose Auto-Thinking Capability in MLLMs Via Bi-Mode Annealing and Reinforce Learning
著者: Qi Yang, Bolin Ni, Shiming Xiang, Houwen Peng

<details>
<summary> 日本語要旨 </summary>

マルチモーダル大規模言語モデル（MLLMs）における明示的なステップバイステップの推論は、複雑なタスクで強力な性能を発揮しています。しかし、多くの単純な問い合わせではそのような推論が不要であり、大きな計算オーバーヘッドを導入します。この非効率性に対処するため、私たちは自動的に推論プロセスの必要性を判断し、入力の複雑さに基づいて呼び出すかどうかを決定するオートシンキングMLLMであるR-4Bを提案します。私たちの主なアイデアは、推論と非推論の両方の能力を持つ単一モデルに対して適切なモードを選択するように訓練することです。まず、明示的な複雑さ注釈を必要とせずに推論集約型および直接回答型の両方で優れたモデルを構築する統一トレーニングパラダイムであるバイモードアニーリングを導入します。この基盤に基づき、私たちは軽量な強化学習アルゴリズムであるバイモードポリシーオプティマイゼーション（BPO）を提案します。これは二重ロールアウトメカニズムを用いており、各入力に対して推論と非推論の両方の応答を生成します。この方法によりモード崩壊が防止され、単純なルールベースの報酬だけで適応的な推論ポリシーの堅牢な学習を可能にします。25のベンチマークにわたる広範な実験では、R-4Bが同規模のモデルの中で最先端の性能を達成していることが示されました。それはQwen2.5-VL-7Bを一貫して上回り、Kimi-VL-A3B-Thinking-2506（16B）などのより大きなモデルに匹敵またはそれを超える推論集約型タスクでの性能を示しました。一方で冗長な推論を避けることで計算コストを削減しています。私たちの結果は、適応的オートシンキングがより効率的なマルチモーダル推論モデルに向かう有効でスケーラブルな道筋を提供することを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Multimodal Large Language Models (MLLMs) with explicit step-by-step reasoning have achieved strong performance on complex tasks. However, such reasoning is unnecessary for many simple queries and introduces substantial computational overhead. To address this inefficiency, we present R-4B, an auto-thinking MLLM that dynamically determines whether to invoke the reasoning process based on input complexity. Our key idea is to equip a single model with both thinking and non-thinking capabilities and train it to select the appropriate mode. We first introduce bi-mode annealing, a unified training paradigm that constructs a model competent in both reasoning-intensive and direct-answer settings without requiring explicit complexity annotations. Building on this foundation, we propose Bi-mode Policy Optimization (BPO), a lightweight reinforcement learning algorithm that employs a dual-rollout mechanism: for each input, the model generates both thinking and non-thinking responses. This prevents mode collapse and enables robust learning of an adaptive reasoning policy using only simple, rule-based rewards. Extensive experiments across 25 benchmarks show that R-4B achieves state-of-the-art performance among models of similar scale. It consistently surpasses Qwen2.5-VL-7B and matches or exceeds larger models such as Kimi-VL-A3B-Thinking-2506 (16B) on reasoning-intensive tasks, while reducing computational cost by avoiding redundant reasoning. Our results demonstrate that adaptive auto-thinking offers an effective and scalable pathway toward more efficient multimodal reasoning models.
</details>

---

### Opening The Sim-to-Real Door for Humanoid Pixel-to-Action Policy Transfer
著者: Haoru Xue, Tairan He, Zi Wang, Qingwei Ben, Wenli Xiao, Zhengyi Luo, Xingye Da, Fernando Castañeda, Guanya Shi, Shankar Sastry, Linxi Fan, Yuke Zhu

<details>
<summary> 日本語要旨 </summary>

最近のGPU加速によるフォトリアリスティックシミュレーションの進歩は、ロボット学習のためのスケーラブルなデータ生成経路を開きました。これにより、大量の物理的および視覚的ランダム化が可能となり、ポリシーはキュレーションされた環境を超えて一般化できます。この進歩に基づいて、私たちはビジョンベースの人間型ロコマニピュレーション用の教師-生徒-ブートストラップ学習フレームワークを開発しました。これは可動物体との相互作用を代表的な高難易度ベンチマークとして使用します。私たちのアプローチでは、長期間の特権ポリシートレーニングを安定化させるステージドリセット探索戦略を導入し、部分観測性を軽減しシミュレーションから実世界への強化学習（RL）における閉ループ一貫性を向上させるために設計されたGRPOベースの微調整手順を導入しています。完全に合成シミュレーションデータでトレーニングされた結果として得られたポリシーは、多様な可動物体（複数のドアタイプを含む）に対する堅牢なゼロショットパフォーマンスを達成し、同じ全身制御スタックで人間オペレーターを最大31.7%まで上回るタスク完了時間を記録しています。これは純粋なRGB知覚から多様な可動ロコマニピュレーションに対応可能な初の人間型シミュレーションから実世界へのポリシーを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Recent progress in GPU-accelerated, photorealistic simulation has opened a scalable data-generation path for robot learning, where massive physics and visual randomization allow policies to generalize beyond curated environments. Building on these advances, we develop a teacher–student–bootstrap learning framework for vision-based humanoid loco-manipulation, using articulated-object interaction as a representative high-difficulty benchmark. Our approach introduces a staged-reset exploration strategy that stabilizes long-horizon privileged-policy training, and a GRPO-based fine-tuning procedure designed to mitigate partial observability and improve closed-loop consistency in sim-to-real RL. Trained entirely on synthetic simulation data, the resulting policy achieves robust zero-shot performance across diverse articulated objects—including multiple door types—and outperforms human teleoperators by up to 31.7% in task completion time under the same whole-body control stack. This represents the first humanoid sim-to-real policy capable of diverse articulated loco-manipulation from pure RGB perception.
</details>

---

### GenieDrive: Towards Physics-Aware Driving World Model with 4D Occupancy Guided Video Generation
著者: Zhenya Yang, Zhe Liu, Yuxiang Lu, Liping Hou, Chenxuan Miao, peng siyi, Bailan Feng, Xiang Bai, Hengshuang Zhao

<details>
<summary> 日本語要旨 </summary>

物理学に基づいたドライブワールドモデルは、運転計画、外れ値データの合成、閉ループ評価に不可欠です。しかし、既存の方法では通常、単一の拡散モデルを使用してドライビングアクションを直接動画にマッピングしようとしますが、これは学習を困難にし、物理的に不整合な出力を引き起こす可能性があります。これらの課題を克服するために、私たちは新しいフレームワークであるGenieDriveを提案します。これは物理学に基づいたドライビング動画生成のためのものです。私たちのアプローチは、4D占有率の生成から始まります。これは後続の動画生成のための物理情報を含む基盤として機能します。4D占有率には高解像度3D構造やダイナミクスなど、豊富な物理情報が含まれています。このような高解像度の占有率を効果的に圧縮するために、私たちはVAE（教師あり変分モデル）を提案し、これは占有率を三次元平面表現へと符号化して潜在サイズを以前の方法で使用されているものの58%に削減します。さらに、制御が占有率進化に与える影響を正確にモデル化するためにMutual Control Attention（MCA）を導入し、VAEとその後の予測モジュールをエンドツーエンドで共同トレーニングして予測精度を最大化します。これらの設計により、推論速度41FPSで予測mIoUが7.2%向上し、パラメータ数はわずか3.47Mです。また、動画生成モデルにNormalized Multi-View Attentionを導入することで、4D占有率からのガイダンスにより多視点ドライビング動画を生成し、FVDが20.7%減少して動画品質が大幅に向上します。実験結果は、GenieDriveが高度に制御可能で、多視点一貫性のある物理学に基づいたドライビング動画生成を可能にすることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Physics-aware driving world model is essential for drive planning, out-of-distribution data synthesis, and closed-loop evaluation. However, existing methods often rely on a single diffusion model to directly map driving actions to videos, which makes learning difficult and leads to physically inconsistent outputs. To overcome these challenges, we propose GenieDrive, a novel framework designed for physics-aware driving video generation. Our approach starts by generating 4D occupancy, which serves as a physics-informed foundation for subsequent video generation. 4D occupancy contains rich physical information, including high-resolution 3D structures and dynamics. To facilitate effective compression of such high-resolution occupancy, we propose a VAE that encodes occupancy into a latent tri-plane representation, reducing the latent size to only 58% of that used in previous methods. We further introduce Mutual Control Attention (MCA) to accurately model the influence of control on occupancy evolution, and we jointly train the VAE and the subsequent prediction module in an end-to-end manner to maximize forecasting accuracy. Together, these designs yield a 7.2% improvement in forecasting mIoU at an inference speed of 41 FPS, while using only 3.47 M parameters. Additionally, a Normalized Multi-View Attention is introduced in the video generation model to generate multi-view driving videos with guidance from our 4D occupancy, significantly improving video quality with a 20.7% reduction in FVD. Experiments demonstrate that GenieDrive enables highly controllable, multi-view consistent, and physics-aware driving video generation.
</details>

---

### GDRO: Group-level Reward Post-training Suitable for Diffusion Models
著者: Yiyang Wang, Xi Chen, Xiaogang Xu, Yu Liu, Hengshuang Zhao

<details>
<summary> 日本語要旨 </summary>

最近の進歩では、大規模言語モデル（LLMs）からオンライン強化学習（RL）を採用し、テキストから画像への修正流れる拡散モデルに報酬整合性を適用しています。グループレベルの報酬を使用することで、モデルはターゲットされた報酬に成功裏に整合されますが、低効率、確率的サンプラーへの依存性、および報酬ハッキングといった課題に直面しています。問題は修正流れるモデルがLLMsと根本的に異なることです：1) 効率の観点から、オンライン画像サンプリングは時間を要し、トレーニング時間を支配します。2) 確率性の観点から、修正流れは初期ノイズが固定されると決定論的になります。これらの問題に対処し、LLMsから得られたグループレベル報酬の効果に触発されて、私たちはグループレベル直接報酬最適化（GDRO）を設計しました。GDROは、修正流れるモデルの特性を組み合わせた新しいポストトレーニングパラダイムであり、グループレベル報酬整合に使用されます。厳密な理論分析を通じて、GDROは画像ロールアウトサンプリングの大きな時間コストを節約する完全オフライントレーニングをサポートしていることを指摘します。また、拡散サンプラーに依存しないため、確率性を得るためのODEからSDEへの近似が不要です。さらに、報酬ハッキングの罠を実証的に研究し、これを評価に含めて修正スコアを使用します。このスコアは元の評価報酬だけでなく、報酬ハッキングの傾向も考慮します。広範囲の実験により、GDROがOCRおよびGenEvalタスクを通じてグループごとのオフライン最適化を行うことで、拡散モデルの報酬スコアを効果的かつ効率的に改善する一方で、報酬ハッキングを軽減する際の安定性と堅牢性が強いことが示されています。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advancements adopt online reinforcement learning (RL) from LLMs to text-to-image rectified flow diffusion models for reward alignment. The use of group-level rewards successfully aligns the model with the targeted reward. However, it faces challenges including low efficiency, dependency on stochastic samplers, and reward hacking. The problem is that rectified flow models are fundamentally different from LLMs: 1) For efficiency, online image sampling takes much more time and dominates the time of training. 2) For stochasticity, rectified flow is deterministic once the initial noise is fixed. Aiming at these problems and inspired by the effects of group-level rewards from LLMs, we design Group-level Direct Reward Optimization (GDRO). GDRO is a new post-training paradigm for group-level reward alignment that combines the characteristics of rectified flow models. Through rigorous theoretical analysis, we point out that GDRO supports full offline training that saves the large time cost for image rollout sampling. Also, it is diffusion-sampler-independent, which eliminates the need for the ODE-to-SDE approximation to obtain stochasticity. We also empirically study the reward hacking trap that may mislead the evaluation, and involve this factor in the evaluation using a corrected score that not only considers the original evaluation reward but also the trend of reward hacking. Extensive experiments demonstrate that GDRO effectively and efficiently improves the reward score of the diffusion model through group-wise offline optimization across the OCR and GenEval tasks, while demonstrating strong stability and robustness in mitigating reward hacking.
</details>

---

### CGHair: Compact Gaussian Hair Reconstruction with Card Clustering
著者: Haimin Luo, Srinjay Sarkar, Albert Mosella-Montoro, Francisco Vicente Carrasco, Fernando De la Torre

<details>
<summary> 日本語要旨 </summary>

私たちは、多視点画像からの高精度な髪の再構築のためのコンパクトなパイプラインを提案します。最近の3Dガウススプラッティング（3DGS）手法はリアルな結果を達成していますが、しばしば数百万もの原始体を必要とし、そのために高いストレージおよびレンダリングコストが生じます。髪がヘアスタイル全体で構造的および視覚的な類似性を示すことに注目し、私たちは繊維を代表的なヘアカードにクラスタリングし、これらを共有テクスチャコードブックにグループ化します。この手法は3DGSレンダリングと構造を統合し、再構築時間およびストレージの大幅な削減を実現しつつ、視覚品質を維持します。さらに、画像セットから初期繊維幾何学を再構築するための生成的事前加速法を提案します。実験では、繊維再構築時間が4倍に削減され、メモリフットプリントが200倍以上低いながらも同等のレンダリングパフォーマンスを達成しています。
</details>

<details>
<summary> 英語要旨 </summary>

We present a compact pipeline for high-fidelity hair reconstruction from multi-view images. While recent 3D Gaussian Splatting (3DGS) methods achieve realistic results, they often require millions of primitives, leading to high storage and rendering costs. Observing that hair exhibits structural and visual similarities across a hairstyle, we cluster strands into representative hair cards and group these into shared texture codebooks. Our approach integrates this structure with 3DGS rendering, significantly reducing reconstruction time and storage while maintaining comparable visual quality. In addition, we propose a generative prior accelerated method to reconstruct the initial strand geometry from a set of images. Our experiments demonstrate a 4-fold reduction in strand reconstruction time and achieve comparable rendering performance with over 200× lower memory footprint.
</details>

---

### Hierarchical Action Learning for Weakly-Supervised Action Segmentation
著者: Junxian Huang, Ruichu Cai, Juntao Fang, Hao Zhu, Boyan Xu, Weilin Chen, Zijian Li, Shenghua Gao

<details>
<summary> 日本語要旨 </summary>

人間は、複数の抽象化レベルにわたって行動を構造化する重要な遷移を通じて行動を認識しますが、一方で機械は視覚的特徴に依存し、過剰セグメンテーションの傾向があります。これはビデオ理解における階層的推論を可能にする難しさを浮き彫りにしています。興味深いことに、低レベルの視覚変数と高レベルの行動潜在変数が異なる速度で進化することを観察します。具体的には、低レベルの視覚変数は急速に変化し、一方で高レベルの行動変数はよりゆっくり進化するため、識別が容易です。この洞察を基に、弱教師ありアクションセグメンテーションのために階層的行動学習（**HAL**）モデルを提案します。私たちのアプローチでは、高レベルの潜在行動が低レベルの視覚特徴のダイナミクスを支配する階層的因果データ生成過程を導入します。これら異なる時間スケールを効果的にモデリングするために、これらの潜在変数を時間とともに整合させる決定論的プロセスを導入します。**HAL** モデルは階層ピラミッドトランスフォーマーを使用して視覚特徴と潜在変数の両方を捉え、高レベル行動変数の遅いダイナミクスを強制するために希薄な移行制約が適用されます。このメカニズムは時間とともにこれらの潜在変数の識別を向上させます。ある程度の仮定の下で、これらの潜在的な行動変数が厳密に識別可能であることを証明します。いくつかのベンチマークにおける実験結果は、**HAL** モデルが弱教師ありアクションセグメンテーションにおいて既存の方法を大幅に上回り、その現実世界での応用における実践的な効果を確認しています。
</details>

<details>
<summary> 英語要旨 </summary>

Humans perceive actions through key transitions that structure actions across multiple abstraction levels, whereas machines, relying on visual features, tend to over-segment. This highlights the difficulty of enabling hierarchical reasoning in video understanding. Interestingly, we observe that lower-level visual and high-level action latent variables evolve at different rates, with low-level visual variables changing rapidly, while high-level action variables evolve more slowly, making them easier to identify. Building on this insight, we propose the Hierarchical Action Learning (\textbf{HAL}) model for weakly-supervised action segmentation. Our approach introduces a hierarchical causal data generation process, where high-level latent action govern the dynamics of low-level visual features. To model these varying timescales effectively, we introduce deterministic processes to align these latent variables over time. The \textbf{HAL} model employs a hierarchical pyramid transformer to capture both visual features and latent variables, and a sparse transition constraint is applied to enforce the slower dynamics of high-level action variables. This mechanism enhances the identification of these latent variables over time. Under mild assumptions, we prove that these latent action variables are strictly identifiable. Experimental results on several benchmarks show that the \textbf{HAL} model significantly outperforms existing methods for weakly-supervised action segmentation, confirming its practical effectiveness in real-world applications.
</details>

---

### COT-FM: Cluster-wise Optimal Transport Flow Matching
著者: Chiensheng Chiang, Kuan-Hsun Tu, Jia-Wei Liao, Cheng-Fu Chou, Tsung-Wei Ke

<details>
<summary> 日本語要旨 </summary>

私たちは、COT-FMという一般的なフレームワークを紹介します。これはFlow Matching（FM）における確率パスの形状を変えて、より速く信頼性の高い生成を実現します。FMモデルはランダムまたはバッチ単位での結合によって曲がった軌道を生じることが多く、これにより離散化誤差が増加しサンプル品質が低下します。COT-FMはターゲットサンプルをクラスタリングし、各クラスターに逆方向の事前学習済みFMモデルから得られた専用のソース分布を割り当てることでこの問題を解決します。この分割統治戦略により、より正確な局所輸送が可能となり、モデルアーキテクチャを変更することなく大幅に直線的なベクトル場が得られます。プラグアンドプレイのアプローチとして、COT-FMは2Dデータセット、画像ベンチマーク、およびロボティック操作タスクにわたってサンプリングを一貫して加速し、生成品質を向上させます。
</details>

<details>
<summary> 英語要旨 </summary>

We introduce COT-FM, a general framework that reshapes the probability path in Flow Matching (FM) to achieve faster and more reliable generation. FM models often produce curved trajectories due to random or batch-wise couplings, which increase discretization error and reduce sample quality. COT-FM fixes this by clustering target samples and assigning each cluster a dedicated source distribution obtained by reversing pretrained FM models. This divide-and-conquer strategy yields more accurate local transport and significantly straighter vector fields, all without changing the model architecture. As a plug-and-play approach, COT-FM consistently accelerates sampling and improves generation quality across 2D datasets, image benchmarks, and robotic manipulation tasks.
</details>

---

### MeshWeaver: Sparse-Voxel-Guided Surface Weaving for Autoregressive Mesh Generation
著者: Jiale Xu, Wang Zhao, Ying Shan

<details>
<summary> 日本語要旨 </summary>

自己回帰的メッシュ生成は、メッシュをシーケンスにトークナイズし、言語モデリングのような方法でモデルを訓練することで注目されています。しかし、既存のアプローチは2つの基本的な制限を抱えています：（i）低いトークナイズ効率により長いトークンシーケンスが生じ、高ポリメッシュへの拡張が阻害されること、および（ii）幾何学的なガイダンスが欠如している点で、生成はグローバルな形状埋め込みにのみ条件付けられており、局所的な表面手掛かりではありません。私たちはMeshWeaverを導入します。これは自己回帰フレームワークであり、メッシュ生成を直接次の頂点を予測することによって表面織りプロセスとして扱います。その核心には、3つの補完的な方法で生成過程に幾何学的コンテキストを注入する多レベルスパースボクセルエンコーダーがあります：（i）頂点表現としてボクセル特徴を提供、（ii）ボクセル特徴へのクロスアテンションによってトークン予測をガイドし、（iii）入力面周りで生成を制約する構造的な骨組みとして機能します。この階層設計により、単一のデコードステップで粗い頂点から細かい頂点への予測が可能となり、生成モデルを3D幾何学と密接に結合させます。広範囲の実験は、MeshWeaverが圧縮比率18％という最先端の性能を達成し、16,000面までのメッシュ生成が可能であり、幾何学的忠実度において既存手法を大きく改善することを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Autoregressive mesh generation has gained attention by tokenizing meshes into sequences and training models in a language‑modeling fashion. However, existing approaches suffer from two fundamental limitations: (i) low tokenization efficiency, which yields long token sequences and prevents scaling to high‑poly meshes, and (ii) absence of geometry‑aware guidance, as generation is conditioned only on global shape embeddings rather than local surface cues. We introduce MeshWeaver, an autoregressive framework that treats mesh generation as a surface weaving process by directly predicting the next vertex instead of independent coordinates. At its core is a multi‑level sparse‑voxel encoder that injects geometric context into the generative process in three complementary ways: providing voxel features as vertex representations, guiding token prediction via cross‑attention to voxel features, and serving as a structural scaffold that constrains generation around the input surface. Our hierarchical design enables coarse‑to‑fine vertex prediction in a single decoding step, while tightly couples the generative model with 3D geometry. Extensive experiments demonstrate that MeshWeaver achieves a state‑of‑the‑art compression ratio of 18%, can generates meshes with up to 16K faces, and significantly improves geometric fidelity over prior approaches.
</details>

---

### Weaver: Decoupled Training for Interleaved Multi-modal Generation
著者: Jinbo Xing, Zeyinzi Jiang, Yuxiang Tuo, Chaojie Mao, Xiaotang Gai, Xi Chen, Jingfeng Zhang, Yulin Pan, Zhen Han, Jie Xiao, Keyu Yan, Chen-Wei Xie, Chongyang Zhong, Kai Zhu, Shen Tong, Lianghua Huang, Yu Liu, Yujiu Yang

<details>
<summary> 日本語要旨 </summary>

最近の統一型マルチモーダルモデルは、理解と生成において前例のない進歩を遂げていますが、主に単一モダリティ出力を持つマルチモーダル入力をサポートしており、データ不足や長距離クロスモーダルコンテキストのモデリングが困難であるため、複雑な交錯したテキスト・画像コンテンツを生成することに苦労しています。私たちはWeaverを紹介します。これは統一型マルチモーダルアーキテクチャ内での自己回帰的な計画・視覚化プロセスとして交錯した生成をフレーム化します。計画者、すなわち理解専門家は豊富なテキスト・画像コンテキストを消化し、視覚化トリガーおよびその密なテキストガイダンス（ただのプレーンテキストではない）を生成します。一方、ビジュアライザ、すなわち生成専門家は計画者のテキストガイダンスと視覚的参照に基づいて画像を生成します。この設計により分離学習が可能になります：私たちは大量のテキスト計画データと参照ガイド付き画像データのコレクションで2つの専門家を並行してトレーニングし、推論時に強力な交錯したマルチモーダル生成能力を実現します。さらに、計画者を多様な理解と生成タスクのデータセットでトレーニングすることで、モデルは自動的なタスク推論能力を備えます。モデルを複数の側面から分析・評価するために、私たちは日常使用ケースをカバーするベンチマークも導入します。広範な実験では、Weaverが実際の交錯データトレーニングなしまたは非常に限られた状態でも、交錯したマルチモーダル生成において優れた性能を達成することが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

Recent unified multi-modal models have made unprecedented progress in understanding and generation, yet they largely support multi-modal inputs with single-modality outputs, struggling to produce complex interleaved text–image content due to data scarcity and the difficulty of modeling long-range cross-modal context. We introduce Weaver, which frames interleaved generation as an autoregressive planning–visualization process within a unified multi-modal architecture. A planner, i.e., understanding expert, digests rich text–image context to produce visualization triggers and their dense textual guidance except for plain text, while a visualizer, i.e., generation expert, produces images conditioned on the planner’s textual guidance and visual references. This design enables decoupled learning: we train the two experts on large collections of textual planning and reference-guided image data in parallel, yielding powerful interleaved multi-modal generation capability at inference. Moreover, training the planner with datasets from diverse understanding and generation tasks equips the model with automatic task inference. To analyze and evaluate the model from multiple dimensions, we further introduce a benchmark that covers a range of everyday use cases. Extensive experiments show that, even without or with only very limited real interleaved data training, Weaver achieves superior performance on interleaved multi-modal generation.
</details>

---

### VOSR: A Vision-Only Generative Model for Image Super-Resolution
著者: Rongyuan Wu, Lingchen Sun, Zhengqiang ZHANG, Xiangtao Kong, Jixin Zhao, Shihao Wang, Lei Zhang

<details>
<summary> 日本語要旨 </summary>

大規模な事前学習済みテキスト・トゥ・イメージ（T2I）拡散モデル、例えばStable Diffusionは、非常にリアルな詳細を持つ画像超解像（SR）のために微調整することができます。印象的ですが、このようなマルチモーダルモデルの事前学習は、高品質なテキスト・イメージペア数十億枚と膨大な計算リソースを必要とします。これにもかかわらず、SRは本質的に画像・トゥ・イメージ（I2I）タスクです。このことから重要な問いが生じます：純粋にビジョンタスクを解決するために、本当にマルチモーダルの事前知識や数十億規模のテキスト・イメージデータが必要なのでしょうか？この論文では、**VOSR**という**V**ision-**O**nly **S**uper-**R**esolutionフレームワークを提案します。これはテキスト的事前知識やマルチモーダルの事前学習が不要であることを特徴としています。以前の画像ベース、単一モーダル拡散モデルにおける二つの主な制約点を特定しました：限られた視覚的セマンティックガイダンスと不安定な無条件学習です。これに対処するため、事前学習済みのビジョンエンコーダを用いてセマンティックな手がかりを注入し、低品質条件を部分的に使用してトレーニングを安定化させる緩和された無条件目標を導入します。推論の加速のため、一歩でSRが可能な修正済みショートカットモデルを採用し、品質劣化を最小限に抑えます。VOSRはT2Iベースの拡散モデルと比較して大幅に少ないデータでかつ低コストで訓練されていますが、VOSRは合成および実世界のベンチマークの両方で最先端のT2I調整SR方法と比較して同等またはそれ以上の性能を達成しました。これにより、VOSRが生成的SRのためのスケーラブルかつ競争力のある代替手段である可能性を示しています。コードとモデルは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Large-scale pre-trained text-to-image (T2I) diffusion models, such as Stable Diffusion, can be finetuned for image super-resolution (SR) with highly realistic details. While impressive, pre-training such multi-modal models demands billions of high-quality text-image pairs and substantial computational resources, despite that SR is fundamentally an image-to-image (I2I) task. This raises a critical question: do we truly need multi-modal priors and billion-scale text-image data to solve a purely vision task? In this paper, we propose **VOSR**, a **V**ision-**O**nly **S**uper-**R**esolution framework that eliminates the need for textual priors and multi-modal pretraining. We identify two key limitations in previous image-based, uni-modal diffusion models: limited visual semantic guidance and unstable unconditional training. To this end, we leverage a pretrained vision encoder to inject semantic cues, and introduce a relaxed unconditional objective that partially uses the low-quality condition to stabilize training. To accelerate inference, we adopt a modified shortcut model for one-step SR with minimal quality degradation. VOSR is trained from scratch with significantly less data and a lower computational cost compared to T2I-based diffusion models. However, VOSR achieves comparable or even better performance than state-of-the-art T2I-tuned SR methods on both synthetic and real-world benchmarks, demonstrating its potential as a scalable and competitive alternative for generative SR. Codes and models will be made publicly available.
</details>

---

### Pointer-CAD: Unifying B-Rep and Command Sequences Via Pointer-based Edges & Faces Selection
著者: Dacheng Qi, Chenyu Wang, Jingwei Xu, Tianzhe Chu, Zibo Zhao, Wen Liu, Wenrui Ding, Yi Ma, Shenghua Gao

<details>
<summary> 日本語要旨 </summary>

コンピュータ支援設計（CAD）モデルの構築は労力を要するが、エンジニアリングや製造において不可欠です。最近の大規模言語モデル（LLM）の進歩により、CADをコマンドシーケンスとして表現することでLLMに基づくCAD生成が可能になりました。しかし、これらの方法は実際のシナリオでは困難を伴います。コマンドシーケンス表現は面や辺などのエンティティ選択をサポートしていないため、チャムフェルやフィレットといった複雑な編集操作に対応できません。さらに、スケッチやエクストルーダー操作中の連続変数の離散化はトポロジカルエラーを引き起こす可能性があります。これらの制限に対処するため、我々はB-repモデルの幾何情報を順次モデリングに明示的に組み込むポインターに基づくコマンドシーケンス表現を利用した新しいLLMベースのCAD生成フレームワークであるPointer-CADを提案します。具体的には、Pointer-CADはCADモデル生成をステップごとに分解し、各ステップの生成を前のステップから得られたB-repおよびテキスト記述の両方で条件付けます。特定の幾何エンティティを選択する操作が必要な場合、LLMは利用可能なセットから最も特徴一致度の高い候補を選択するポインターを予測します。このような選択操作により、コマンドシーケンスベースの表現で発生する量子化誤差も削減されます。Pointer-CADのトレーニングをサポートするため、専門家レベルの自然言語記述を生成するデータアノテーションパイプラインを開発し、約575KのCADモデルからなるデータセットを構築しました。広範囲にわたる実験結果は、Pointer-CADが複雑な幾何学的構造の生成を効果的にサポートし、分割エラーを極めて低いレベルまで減少させることを示しており、これはコマンドシーケンス手法に対する大幅な改善であり、量子化誤差によって導入されるトポロジカル不正確性を大きく軽減しています。
</details>

<details>
<summary> 英語要旨 </summary>

Constructing computer-aided design (CAD) models is labor-intensive but essential for engineering and manufacturing. Recent advances in Large Language Models (LLMs) have inspired the LLM-based CAD generation by representing CAD as command sequences. But these methods struggle in practical scenarios because command sequence representation does not support entity selection (e.g. faces or edges), limiting its ability to support complex editing operations such as chamfer or fillet. Further, the discretization of a continuous variable during sketch and extrude operations may result in topological errors. To address these limitations, we present Pointer-CAD, a novel LLM-based CAD generation framework that leverages a pointer-based command sequence representation to explicitly incorporate the geometric information of B-rep models into sequential modeling. In particular, Pointer-CAD decomposes CAD model generation into steps, conditioning the generation of each subsequent step on both the textual description and the B-rep generated from previous steps. Whenever an operation requires the selection of a specific geometric entity, the LLM predicts a Pointer that selects the most feature-consistent candidate from the available set. Such a selection operation also reduces the quantization error in the command sequence-based representation. To support the training of Pointer-CAD, we develop a data annotation pipeline that produces expert-level natural language descriptions and apply it to build a dataset of approximately 575K CAD models. Extensive experimental results demonstrate that Pointer-CAD effectively supports the generation of complex geometric structures and reduces segmentation error to an extremely low level, achieving a significant improvement over prior command sequence methods, thereby significantly mitigating the topological inaccuracies introduced by quantization error.
</details>

---

### Gallant: Voxel Grid-based Humanoid Locomotion and Local-navigation Across 3-D Constrained Terrains
著者: Qingwei Ben, Botian Xu, Kailin Li, Feiyu Jia, Wentao Zhang, Jingping Wang, Jingbo Wang, Dahua Lin, Jiangmiao Pang

<details>
<summary> 日本語要旨 </summary>

堅牢なヒューマノイドの歩行には、周囲の3D環境を正確かつ全体的に一貫して認識することが必要です。しかし、現在の知覚モジュールは主に深度画像や高度マップに基づいており、環境の部分的で平坦化されたビューしか提供せず、完全な3D構造を捉えることができません。本論文では、制約された3D地形におけるヒューマノイドの歩行と局所的なナビゲーションのための立方体グリッド–ベースのフレームワークである**Gallant**を紹介します。これは、軽量かつ構造化された知覚表現としてのビニアル化LiDARデータを活用し、この表現を制御方針にマッピングするz-grouped 2D CNNを使用します。これにより、完全なエンドツーエンド最適化が可能となります。リアルタイムでの観測を動的に生成し、スケーラブルなLiDARベースのトレーニングをサポートし、シミュレーションから実世界への一貫性を確保する高精度なLiDARシミュレーションが開発されました。実験結果は、Gallantの広範な知覚カバーにより、地面レベルの障害物に限定された従来の方法を超えて、横方向のごみ、天井制約、多層構造、狭い通路などに対応する単一のポリシーが使用可能であることを示しています。Gallantはまた、改善されたエンドツーエンド最適化を通じて階段昇降や高いプラットフォームへの乗り越えなどの難易度の高いシナリオで初めて近く100％の成功率を達成しました。このプロジェクトは完全にオープンソースとして公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Robust humanoid locomotion requires accurate and globally consistent perception of the surrounding 3D environment. However, existing perception modules, mainly based on depth images or elevation maps, offer only partial and locally flattened views of the environment, failing to capture the full 3D structure. This paper presents $\textbf{Gallant}$, a voxel-grid–based framework for humanoid locomotion and local navigation in 3D constrained terrains. It leverages voxelized LiDAR data as a lightweight and structured perceptual representation, and employs a z-grouped 2D CNN to map this representation to the control policy, enabling fully end-to-end optimization. A high-fidelity LiDAR simulation that dynamically generates realistic observations is developed to support scalable, LiDAR-based training and ensure sim-to-real consistency. Experimental results show that Gallant’s broader perceptual coverage facilitates the use of a single policy that goes beyond the limitations of previous methods confined to ground-level obstacles, extending to lateral clutter, overhead constraints, multi-level structures, and narrow passages. Gallant also firstly achieves near-100\% success rates in challenging scenarios such as stair climbing and stepping onto elevated platforms through improved end-to-end optimization. This project will be fully open-source.
</details>

---

### Enhancing Hands in 3D Whole-Body Pose Estimation with Conditional Hands Modulator
著者: Gyeongsik Moon

<details>
<summary> 日本語要旨 </summary>

3D全身姿勢推定において、体の文脈内で手のポーズを正確に復元することは依然として大きな課題です。この困難さは基本的な監督ギャップから生じます：全身姿勢推定器は手の多様性が限られたフルボディデータセットでトレーニングされていますが、一方で手専用の推定器は手中心のデータセットでトレーニングされ、詳細な指の可動を得意としていますが、全体的な身体認識に欠けます。これに対処するため、私たちは両方の事前学習済み全身および手姿勢推定器の強みを活用するモジュラーなフレームワークであるWholeBody++を提案します。また、私たちはCHAM（Conditional Hands Modulator）という軽量モジュールを導入しました。これは、手特有の特徴を抽出した事前学習済みの手姿勢推定器から全身の特徴ストリームを調整します。この調整により、全身モデルは上半身の運動構造と一貫性のある正確な腕時計の向きを予測できるようになりますが、フルボディモデル全体を再トレーニングする必要はありません。同時に、手姿勢推定器によって予測された指の可動と手の形状を微分可能な剛体整列を通じてフルボディメッシュに直接組み込んでいます。この設計により、WholeBody++は全体的に一貫した身体推論と細部までの手の詳細を組み合わせることが可能です。広範な実験によって、WholeBody++が手の精度を大幅に向上させ、全体的なフルボディ姿勢の品質を高めていることが示されました。コードおよび事前学習済みモデルは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Accurately recovering hand poses within the body context remains a major challenge in 3D whole-body pose estimation. This difficulty arises from a fundamental supervision gap: whole-body pose estimators are trained on full-body datasets with limited hand diversity, while hand-only estimators, trained on hand-centric datasets, excel at detailed finger articulation but lack global body awareness. To address this, we propose WholeBody++, a modular framework that leverages the strengths of both pre-trained whole-body and hand pose estimators. We introduce CHAM (Conditional Hands Modulator), a lightweight module that modulates the whole-body feature stream using hand-specific features extracted from a pre-trained hand pose estimator. This modulation enables the whole-body model to predict wrist orientations that are both accurate and coherent with the upper-body kinematic structure, without retraining the full-body model. In parallel, we directly incorporate finger articulations and hand shapes predicted by the hand pose estimator, aligning them to the full-body mesh via differentiable rigid alignment. This design allows WholeBody++ to combine globally consistent body reasoning with fine-grained hand detail. Extensive experiments demonstrate that WholeBody++ substantially improves hand accuracy and enhances overall full-body pose quality. Code and pretrained models will be released publicly.
</details>

---

### Watch and Learn: Learning to Use Computers from Online Videos
著者: Chan Hee Song, Yiwen Song, Palash Goyal, Yu Su, Oriana Riva, Hamid Palangi, Tomas Pfister

<details>
<summary> 日本語要旨 </summary>

コンピューターを使用するエージェント（CUA）は、多様で進化し続けるアプリケーション間でタスクワークフローを計画しなければなりませんが、大規模かつ高品質のトレーニングデータ不足によって進展は限られています。既存のデータセットは狭く静的であり、アノテーションが高価です。一方、合成データは過度に単純化されたり誤った振る舞いを引き起こすことが多いです。私たちは「Watch & Learn（W&L）」というフレームワークを提案します。これは、インターネット上で容易に入手可能な人間のコンピュータ使用動画を大規模に実行可能なUIトラジェクトリに変換するものです。直接的にアクションを生成したり、ハンドクラフテッドなヒューリスティックスに依存するのではなく、連続する画面状態からユーザーの行動を予測する逆ダイナミクス問題としてトラジェクトリアノテーションを捉えることで学習を単純化し、ドメイン間で一般化します。タスクに配慮した取得およびラベル付けパイプラインを通じて、W&Lは53,000以上の高品質トラジェクトリを生成し、CUAをコンテキスト内の例示としてだけでなく、監督学習データとしても強化します。OSWorldでは一般的な目的および特化したCUAの両方に一貫して改善をもたらし、WindowsAgentArenaでは15ステップ制限下で7B規模モデルの中でも最先端のパフォーマンスを達成します。これらの結果は、ウェブスケールの人間によるデモンストレーションビデオが、実世界のCUAを進展させるための実用的かつ拡張可能な基盤として機能することを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Computer-using agents (CUAs) must plan task workflows across diverse and evolving applications, yet progress is limited by the lack of large-scale, high-quality training data. Existing datasets are narrow, static, and costly to annotate, while synthetic data often yields oversimplified or misaligned behaviors. We present Watch & Learn (W&L), a framework that converts readily available Internet videos of human computer use into executable UI trajectories at scale. Instead of directly generating actions or relying on handcrafted heuristics, we cast trajectory annotation as an inverse dynamics problem that predicts user actions from consecutive screen states, which simplifies learning and generalizes across domains. Through a task-aware retrieval and labeling pipeline, W&L yields over 53K high-quality trajectories that enhance CUAs both as in-context exemplars and as supervised training data. On OSWorld, it consistently improves general-purpose and specialized CUAs, while on WindowsAgentArena it achieves state-of-the-art performance among 7B-scale models under the 15-step limit. These results show that web-scale human demonstration videos can serve as a practical and scalable foundation for advancing real-world CUAs.
</details>

---

### EgoEdit: Dataset, Real-Time Streaming Model, and Benchmark for Egocentric Video Editing
著者: Runjia Li, Moayed Haji Ali, Ashkan Mirzaei, Chaoyang Wang, Arpit Sahni, Ivan Skorokhodov, Aliaksandr Siarohin, Tomas Jakab, Junlin Han, Sergey Tulyakov, Philip H.S. Torr, Willi Menapace

<details>
<summary> 日本語要旨 </summary>

私たちは、インタラクティブARアプリケーションのための自己中心的ビデオの指示に基づく編集を研究しています。最近のAIビデオエディターは第三者視点の映像で優れた性能を発揮しますが、自己中心的な視点には固有の課題があります。これには急速な自己運動や頻繁な手と物体の相互作用が含まれ、大きなドメインギャップを生じさせています。また、既存のオフラインエディットパイプラインは高い遅延を伴うため、リアルタイムでのインタラクションが制限されます。これらの問題に対処するため、自己中心的ビデオエディットの完全なエコシステムを提案します。まず、手と物体の豊かな相互作用を特徴とし、明示的に手を保持するよう設計された自己中心的編集シナリオ専用のEgoEditDataデータセットを構築します。次に、単一GPUでのリアルタイムストリーミング推論をサポートする指示に従う自己中心的ビデオエディターであるEgoEditを開発します。最後に、自己運動下での指示忠実性、手と相互作用の保持、および時間的安定性を対象とした評価スイートであるEgoEditBenchを導入します。両方の自己中心的編集タスクと一般的な編集タスクにわたり、EgoEditはインタラクティブ遅延で指示忠実性を持つ時間的に安定した結果を生成します。自己中心的編集ベンチマークでは既存の方法が苦戦するところで明確な進歩を達成し、一般的な編集タスクにおいては最も強力なベースラインと比較可能な性能を維持します。EgoEditDataとEgoEditBenchは研究コミュニティ向けに公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

We study instruction-guided editing of egocentric videos for interactive AR applications. While recent AI video editors perform well on third-person footage, egocentric views present unique challenges — including rapid egomotion, and frequent hand–object interactions — that create a significant domain gap. Moreover, existing offline editing pipelines suffer from high latency, limiting real-time interaction. To address these issues, we present a complete ecosystem for egocentric video editing. First, we construct EgoEditData, a carefully designed and manually curated dataset specifically designed for egocentric editing scenarios, featuring rich hand-object interactions, while explicitly preserving hands. Second, we develop EgoEdit, an instruction-following egocentric video editor that supports real-time streaming inference on a single GPU. Finally, we introduce EgoEditBench, an evaluation suite targeting instruction faithfulness, hand and interaction preservation, and temporal stability under egomotion. Across both egocentric and general editing tasks, EgoEdit produces temporally stable, instruction-faithful results with interactive latency. It achieves clear gains on egocentric editing benchmarks—where existing methods struggle—while maintaining performance comparable to the strongest baselines on general editing tasks. EgoEditData and EgoEditBench will be made public for the research community.
</details>

---

### DUO-VSR: Dual-Stream Distillation for One-Step Video Super-Resolution
著者: Zhengyao Lv, Menghan Xia, Xintao Wang, Kwan-Yee K. Wong

<details>
<summary> 日本語要旨 </summary>

拡散ベースのビデオ超解像（VSR）は驚異的な忠実度を達成しますが、許容できないサンプリングコストに苦しんでいます。分布マッチング蒸留（DMD）は拡散モデルを一ステップ生成に加速させますが、これを直接VSRに適用するとトレーニングの不安定性や劣化した、不十分な監督が生じます。これらの問題に対処するために、私たちは\textbf{DUO-VSR}を提案します。これは、分布マッチングと敵対的監督を統合した\textbf{DU}al-Stream Distillation戦略を中心とする三段階のフレームワークです。\textbf{O}ne-step VSRに適用されます。まず、トレジェクトリ保存型蒸留を通じて後続のトレーニングを安定化させるProgressive Guided Distillation Initializationを採用します。次に、DMDとReal–Fake Score Feature GAN（RFS-GAN）ストリームを同時最適化するDual-Stream Distillation Strategyを導入し、後者は実際のスコアモデルと偽のスコアモデルから得られる特徴に基づく補完的な敵対的監督を提供します。最後に、Preference-Guided Refinementが学習者を知覚品質の好みと整合させます。包括的な実験は、DUO-VSRが以前の一ステップVSR手法よりも優れた視覚品質と効率を達成していることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Diffusion-based video super-resolution (VSR) achieves remarkable fidelity but suffers from prohibitive sampling cost. While distribution matching distillation (DMD) accelerates diffusion models to one-step generation, directly applying it to VSR leads to training instability and degraded, insufficient supervision. To address these issues, we propose \textbf{DUO-VSR}, a three-stage framework centered on a \textbf{DU}al-Stream Distillation strategy that integrates distribution matching and adversarial supervision for \textbf{O}ne-step VSR. We first adopt a Progressive Guided Distillation Initialization to stabilize subsequent training through trajectory-preserving distillation. We then introduce a Dual-Stream Distillation Strategy to jointly optimize DMD and Real–Fake Score Feature GAN (RFS-GAN) streams, with the latter providing complementary adversarial supervision using features from both real and fake score models. Finally, a Preference-Guided Refinement aligns the student with perceptual quality preferences. Comprehensive experiments demonstrate that DUO-VSR achieves superior visual quality and efficiency over previous one-step VSR methods.
</details>

---

### Learning to Track Instance from Single Nature Language Description
著者: Yaozong Zheng, Bineng Zhong, Qihua Liang, Shuimu Zeng, Haiying Xia, Shuxiang Song

<details>
<summary> 日本語要旨 </summary>

ビデオシーケンスからの自然言語記述を用いた視覚言語（VL）トラッキングを、どのようにしてバウンディングボックスの正解情報に依存せずに達成するか？本研究では、この目標を自己教師付きVLトラッキングという課題に取り組むことで達成しています。これは、自然言語記述によって導かれるトラッキング能力を評価するものです。我々は、新しい自己教師付きVLトラッカー\textbf{\tracker}を提案します。これは、言語記述によって指定された任意のオブジェクトを追跡する能力を持ちます。従来の方法がすべての言語と視覚トークンを等しく融合させるのに対し、我々は効率的なDynamic Token Aggregation Moduleを提案します。このモジュールでは各視覚トークンが\textbf{不均等}に扱われます。モジュールは三つの主要ステップから成り立っています：i) アンカートークンを基に、テンプレートフレームから複数の重要なターゲットトークンを選択します。ii) 選ばれたターゲットトークンはその注意スコアに従って統合され、言語トークンと融合されることで冗長な視覚トークンのノイズが排除され、セマンティックな整列が強化されます。iii) 最後に、融合された言語トークンは検索フレームから潜在的なターゲットトークンを抽出するガイド信号として機能し、それらが次のフレームに伝播されることで時間的プロンプトが強化され、トラッカーは未ラベル動画から自律的にインスタンス追跡を学習するよう促します。この新しいモデリングアプローチにより、大規模なバウンディングボックス注釈が不要であることから、言語ガイド付きトラッキング表現の効果的な自己教師付き学習を可能にします。VLトラッキングベンチマークにおける広範囲な実験では、\textbf{\tracker}がSOTAの自己教師付き手法を超え、OTB99、LaSOT、TNL2Kデータセットでそれぞれ11.2%以上、5%、3.3%のAUCスコアの改善を達成しています。
</details>

<details>
<summary> 英語要旨 </summary>

How to achieve vision-language (VL) tracking using natural language descriptions from a video sequence \textbf{without relying on any bounding-box ground truth}? In this work, we achieve this goal by tackling \textit{self-supervised VL tracking}, which aims to evaluate tracking capabilities guided by natural language descriptions. We introduce \textbf{\tracker}, a novel self-supervised VL tracker that is capable of tracking any referred object by a language description. Unlike traditional methods that equally fuse all language and visual tokens, we propose an efficient Dynamic Token Aggregation Module, which treats each visual token \textbf{unequally}. The module consists of three main steps: i) Based on an anchor token, it selects multiple important target tokens from the template frame. ii) The selected target tokens are merged according to their attention scores and aggregated into the language tokens, thereby eliminating redundant visual token noise and enhancing semantic alignment. iii) Finally, the fused language tokens serve as guiding signals to extract potential target tokens from the search frame and propagate them to subsequent frames, enhancing temporal prompts and encouraging the tracker to autonomously learn instance tracking from unlabeled videos. This new modeling approach enables the effective self-supervised learning of language-guided tracking representations without the need for large-scale bounding box annotations. Extensive experiments on VL tracking benchmarks show that {\tracker} surpasses SOTA self-supervised methods, achieving an improvement of more than 11.2\%, 5\%, and 3.3\% in AUC score on the OTB99, LaSOT, and TNL2K datasets, respectively.
</details>

---

### Boosting Self-Supervised Tracking with Contextual Prompts and Noise Learning
著者: Yaozong Zheng, Qihua Liang, Bineng Zhong, Shuimu Zeng, Yuanliang Xue, Ning Li, Shuxiang Song

<details>
<summary> 日本語要旨 </summary>

自己教師付きトラッキングの進展には、ラベルなしビデオから学習された堅牢なコンテクスト知識が不可欠です。しかし、従来の自己教師付きトラッカーは効果的なコンテクストモデリングを欠いており、非セマンティッククエリに基づく既存のコンテクスト関連方法はラベルなしトラッキングシナリオに適応することが難しく、信頼性のあるコンテクスト手掛かりを学習することが困難です。本研究では、新しい自己教師付きトラッキングフレームワークである\textbf{\tracker}を提案します。これは、細部にわたるセマンティックプロンプトとコンテクストノイズを組み合わせて利用することで堅牢なトラッキング表現の学習を促進する二重モーダルコンテクスト関連メカニズムを導入します。易しいものから難しいものへと学習する原則に従い、私たちのコンテクスト関連メカニズムは二段階で動作します。初期トレーニングでは、インスタンスパッチトークン（プロンプト）が前方および後方のトラッキングブランチに割り当てられ、トラッキング知識の獲得を促進します。トレーニングが進むと、コンテクストノイズが徐々にモデルに注入され、特徴を乱すことで、より複雑な特徴空間において堅牢なトラッキング表現の学習を促します。この新しいコンテクスト関連メカニズムにより、私たちの自己教師付きモデルは効率的な推論を保持しつつ、ラベルなしビデオから高品質なトラッキング表現を学習することが可能になります。多くのトラッキングベンチマークで行われた広範な実験は、私たちの方法の優位性を示し、SOTAパフォーマンスを達成しています。
</details>

<details>
<summary> 英語要旨 </summary>

Learning robust contextual knowledge from unlabeled videos is essential for advancing self-supervised tracking. However, conventional self-supervised trackers lack effective context modeling, while existing context association methods based on non-semantic queries struggle to adapt to unlabeled tracking scenarios, making it difficult to learn reliable contextual cues. In this work, we propose a novel self-supervised tracking framework, named \textbf{\tracker}, which introduces a dual-modal context association mechanism that jointly leverages fine-grained semantic prompts and contextual noise to drive the model toward learning robust tracking representations. Adherent to the easy-to-hard learning principle, our contextual association mechanism operates based on two stages. During early training, instance patch tokens (prompts) are assigned to both forward and backward tracking branches to facilitate the acquisition of tracking knowledge. As training progresses, contextual noise is gradually injected into the model to perturb feature, encouraging the tracker to learn robust tracking representations in a more complex feature space. Thus, this novel contextual association mechanism enables our self-supervised model to learn high-quality tracking representations from unlabeled videos, while being applied exclusively during training to preserve efficient inference. Extensive experiments on multiple tracking benchmarks demonstrate the superiority of our method, achieving SOTA performance.
</details>

---

### LEAD: Minimizing Learner-Expert Asymmetry in End-to-End Driving
著者: Long Nguyen, Micha Fauth, Bernhard Jaeger, Daniel Dauner, Maximilian Igl, Andreas Geiger, Kashyap Chitta

<details>
<summary> 日本語要旨 </summary>

自律走行用のシミュレーション生成データセットは、隠れたシーン情報（例えば、視界不良地域から）を利用して運転判断を下す「専門家」ポリシーに依存する全知的なデータ収集を行います。このようなデータがエンドツーエンドのポリシートレーニングで使用されると、センサー覆域やナビゲーション意図情報に限界がある「学習者」ポリシーと専門家間に情報非対称性を生じさせます。この非対称性が学習者のパフォーマンス低下につながることを示します。これに対処するため、CARLAシミュレータで収集された新しい高品質合成データセットLEADを提案します。このデータセットは3つの主要な改善点があります。(1) 専門家は、学習者の視野内で隠れる可能性のあるエンティティを入力状態から除去することにより、不可視情報の使用を最小限に抑えます。さらに、(2) 詳細なドライバー意図情報と(3) 充実したセンサーモダリティ（カメラ、LiDAR、レーダー、オドメトリ）を提供することで、学習者と専門家間の情報ギャップを縮小します。その後、LEAD上で訓練されたシンプルなエンドツーエンド学習ポリシーTransFuser v6（TFv6）を提案します。これらの改善により、TFv6はすべての公開CARLAクローズドループ走行ベンチマークで最先端技術を大きく進展させ、Bench2Driveで95点、Longest6 v2で62点、Town13検証コースで15点の運転スコアを記録します。最後に、LEADデータセットといくつかの公開された実世界データセットを統一リポジトリに集約し、クロスデータセット評価を可能にします。LEADからの合成データでTFv6を事前学習した後、NAVSIM v1、NAVSIM v2、WOD-E2Eベンチマークの実世界データで微調整することにより一貫したパフォーマンス向上が見られることを示します。
</details>

<details>
<summary> 英語要旨 </summary>

Simulation-generated datasets for autonomous driving rely on omniscient data collection 'expert' policies, which use unobservable scene information (e.g., from occluded regions) to make driving decisions. When such data is used for end-to-end policy training, it results in an information asymmetry between the expert and the 'learner' policy, which has limited sensor coverage and navigational intent information compared to the expert. We show that this asymmetry leads to a significant drop in the performance of the learner. To combat this, we present LEAD, a new high-quality synthetic dataset collected in the CARLA simulator with three key improvements.(1) The expert minimizes its use of unobservable information by removing entities from its input state that would be occluded in the learner's field of view. By providing the learner with (2) detailed driver intent information and (3) rich sensor modalities (cameras, LiDARs, radars, and odometry), the dataset narrows down the information gap between the learner and expert. We then propose TransFuser v6 (TFv6), a simple end-to-end learner policy trained on LEAD. As a result of our improvements, TFv6 substantially advances the state of the art on all publicly available CARLA closed-loop driving benchmarks, reaching driving scores of 95 on Bench2Drive, 62 on Longest6 v2, and 15 on the Town13 validation routes. Finally, we aggregate the LEAD dataset with several public real-world datasets under a unified repository to enable cross-dataset evaluation. We show that pre-training TFv6 on synthetic data from LEAD leads to consistent performance gains when followed by fine-tuning with real data from the NAVSIM v1, NAVSIM v2, and WOD-E2E benchmarks.
</details>

---

### Pico-Banana-400K: A Large-Scale Dataset for Text-Guided Image Editing
著者: Yusu Qian, Eli Bocek-Rivele, Liangchen Song, Jialing Tong, Yinfei Yang, Jiasen Lu, Wenze Hu, Zhe Gan

<details>
<summary> 日本語要旨 </summary>

最近のマルチモーダルモデルの進歩は、GPT-4oやNano-Bananaなどのシステムによって示されるように、注目すべきテキストガイド付き画像編集能力を実証しています。しかし、大規模で高品質かつオープンアクセス可能なリアル写真から構築されたデータセットの不在により、研究コミュニティの進歩は制約を受けています。私たちは、指示に基づく画像編集用の包括的な400K画像データセットであるPico-Banana-400Kを導入します。このデータセットは、Nano-Bananaを利用してOpenImagesコレクション内のリアル写真から多様な編集ペアを生成することによって構築されています。Pico-Banana-400Kが以前の合成データセットと異なる点は、品質と多様性への体系的なアプローチです。私たちは細分化された画像編集分類法を用いて、編集タイプの包括的なカバレッジを確保しつつ、MLLMベースの品質スコアリングと慎重なキュレーションによって正確な内容保存と指示忠実性を維持しています。単一ターン編集に限定されず、Pico-Banana-400Kは複雑な編集シナリオの研究を可能にします。このデータセットには、3つの特化したサブセットが含まれています：（1）連続的な修正にわたる順次編集、推論、計画を研究するための72K例のマルチターンコレクション；（2）アライメント研究と報酬モデルトレーニング用の56K例の好みサブセット；および（3）指示書き換えや要約能力を開発するためのペアリングされた長短編集指示。この大規模で高品質かつタスク豊富なリソースを提供することにより、Pico-Banana-400Kは次世代のテキストガイド付き画像編集モデルのトレーニングおよびベンチマークのための堅牢な基盤を確立します。
</details>

<details>
<summary> 英語要旨 </summary>

Recent advances in multimodal models have demonstrated remarkable text-guided image editing capabilities, with systems like GPT-4o and Nano-Banana setting new benchmarks. However, the research community's progress remains constrained by the absence of large-scale, high-quality, and openly accessible datasets built from real images. We introduce Pico-Banana-400K, a comprehensive 400K-image dataset for instruction-based image editing. Our dataset is constructed by leveraging Nano-Banana to generate diverse edit pairs from real photographs in the OpenImages collection. What distinguishes Pico-Banana-400K from previous synthetic datasets is our systematic approach to quality and diversity. We employ a fine-grained image editing taxonomy to ensure comprehensive coverage of edit types while maintaining precise content preservation and instruction faithfulness through MLLM-based quality scoring and careful curation. Beyond single turn editing, Pico-Banana-400K enables research into complex editing scenarios. The dataset includes three specialized subsets: (1) a 72K-example multi-turn collection for studying sequential editing, reasoning, and planning across consecutive modifications; (2) a 56K-example preference subset for alignment research and reward model training; and (3) paired long-short editing instructions for developing instruction rewriting and summarization capabilities. By providing this large-scale, high-quality, and task-rich resource, Pico-Banana-400K establishes a robust foundation for training and benchmarking the next generation of text-guided image editing models.
</details>

---

### HAVE-Bench: Hierarchical Audio-Visual Evaluation from Perception to Interaction
著者: Zhong Muyan, Erfei Cui, Sen Xing, Weiyun Wang, Wen Wu, Yuchen Hu, Yanting Zhang, Xiaowei Hu, Wenhai Wang, Chao Zhang, Jifeng Dai

<details>
<summary> 日本語要旨 </summary>

マルチモーダル大規模言語モデル（MLLMs）は、ビジョン・ランゲージシステムからオーディオを含めることで拡張され、クロスモーダル推論やインタラクションの新たな能力が解放されました。既存のベンチマークが主に知覚タスクに焦点を当て、統一的な認知評価フレームワークが欠けているという制限に対処するため、我々は階層型オーディオ・ビジュアル評価ベンチマーク（HAVE-Bench）を提案します。これは、2,451の精選されたサンプルと手動で注釈付けられた多ターンインタラクションレベルのタスクを利用して、MLLMsのオーディオ関連能力を三段階の認知階層（知覚、推論、インタラクション）に沿って体系的に評価します。この統一フレームワークを用いた実験では、既存のモデルが推論およびインタラクションレベルで顕著なギャップを抱えていることが明らかになりました。特に、音声駆動の視覚的質問応答（VQA）のパフォーマンスはテキスト・画像設定に比べて大きく遅れをとっています。これらの発見は、モデルが長時間かつ複雑なオーディオを処理する能力を向上させること、およびビジョン・テキストからオーディオ・ビジュアル領域への推論能力の移行を促進する緊急性を浮き彫りにしています。
</details>

<details>
<summary> 英語要旨 </summary>

Multimodal large language models (MLLMs) have expanded from vision–language systems to include audio, unlocking new capabilities in cross-modal reasoning and interaction. To address the limitation that existing benchmarks focus mainly on perception tasks and lack a unified cognitive evaluation framework, we propose Hierarchical Audio-Visual Evaluation Benchmark (HAVE-Bench). It systematically evaluates the audio-related capabilities of MLLMs along a three-level cognitive hierarchy: Perception, Reasoning, and Interaction, utilizing 2,451 curated samples and manually annotated multi-turn interaction-level tasks. Experiments using this unified framework reveal significant gaps in existing models at the reasoning and interaction levels, with speech-driven visual question answering (VQA) performance significantly lagging behind the text–image setting. These findings underscore the urgency of enhancing models’ handling of long and complex audio and facilitating the transfer of reasoning capabilities from the vision–text to the audio–visual domain.
</details>

---

### VLIC: Vision-Language Models As Perceptual Judges for Human-Aligned Image Compression
著者: Kyle Sargent, Ruiqi Gao, Philipp Henzler, Charles Herrmann, Aleksander Holynski, Li Fei-Fei, Jiajun Wu, Jason Y. Zhang

<details>
<summary> 日本語要旨 </summary>

画像圧縮性能の評価に人間の好みを含めると、一般的にはMSEなどの単純な歪み関数が人間の知覚と十分に整合していないことがわかっています。圧縮モデルを人間の知覚に合わせるため、以前の研究では大規模な人間の心理視覚判断データセットでキャリブレーションされた異分化可能な知覚損失を用いています。驚くべきことに、我々は最先端のビジョン言語モデル（VLMs）が、画像ペア間の違いについて推論する際にゼロショットで二者択一強制選択（2AFC）判断を再現できることを示します。VLMsの強力なゼロショット視覚推論能力を活用するために、ビジョン言語モデルを用いた画像圧縮（VLIC）システムを提案します。これは、二者択一VLM判断でポストトレーニング可能な拡散ベースの画像圧縮システムです。我々は、このシステムをVLM判断にキャリブレーションすることで、人間に合わせた視覚的圧縮性能が競争力のあるものまたは最先端のものになることを示します。これは、知覚メトリクスおよび大規模ユーザー調査に基づいています。さらに、VLMベースの報酬設計やトレーニング手順を詳細に分析し、重要な洞察を共有しています。
</details>

<details>
<summary> 英語要旨 </summary>

Evaluations of image compression performance which include human preferences have generally found that naive distortion functions such as MSE are insufficiently aligned to human perception. In order to align compression models to human perception, prior work has employed differentiable perceptual losses consisting of neural networks calibrated on large-scale datasets of human psycho-visual judgments. We show that, surprisingly, state-of-the-art vision-language models (VLMs) can replicate binary human two-alternative forced choice (2AFC) judgments zero-shot when asked to reason about the differences between pairs of images. Motivated to exploit the powerful zero-shot visual reasoning capabilities of VLMs, we propose Vision Language Models for Image Compression (VLIC), a diffusion-based image compression system designed to be post-trained with binary VLM judgments. VLIC leverages existing techniques for diffusion model post-training with preferences, rather than distilling the VLM judgments into a separate perceptual loss network. We show that calibrating this system on VLM judgments produces competitive or state-of-the-art performance on human-aligned visual compression depending on the dataset, according to perceptual metrics and large-scale user studies. We additionally conduct an extensive analysis of the VLM-based reward design and training procedure and share important insights.
</details>

---

### Frequency-Aware Flow Matching for High-Quality Image Generation
著者: Sucheng Ren, Qihang Yu, Ju He, Xiaohui Shen, Liang-Chieh Chen

<details>
<summary> 日本語要旨 </summary>

フロー・マッチングモデルは、逐次的にガウスノイズを加えることで画像の劣化プロセスを学習し、その逆過程を行うことにより現実的な画像生成フレームワークとして登場しました。しかし、ノイズが潜在領域で注入されるため、異なる周波数成分への影響は非均一です。その結果、推論時にフロー・マッチングモデルは逆過程の初期段階で低周波数成分（全体的な構造）を生成し、高周波数成分（細部）は後の段階で現れる傾向があります。この洞察に基づき、私たちはフロー・マッチングフレームワークに時間依存的な適応重み付けを通じて周波数認識条件付けを明示的に組み込む新しいアプローチであるFrequency-Aware Flow Matching（FreqFlow）を提案します。私たちは二分枝アーキテクチャを導入しています：(1) 低周波数成分と高周波数成分を別々に処理し、全体的な構造を捉えてテクスチャやエッジを洗練する周波数枝、および(2) 周波数枝の出力に従って潜在領域で画像を合成する空間枝です。生成過程に周波数情報を明示的に統合することで、FreqFlowは大規模な一貫性と細部の両方が効果的にモデル化されるようにします—低周波数条件付けは全体的な構造を強化し、高周波数条件付けはテクスチャの忠実度と詳細の鮮明さを向上させます。クラス条件付きImageNet-256生成ベンチマークにおいて、私たちの方法はFID 1.38で最先端の性能を達成し、以前のディフュージョンモデルDiTとフローマッチングモデルSiTをそれぞれ0.79および0.58 FIDで上回ります。コードは公開される予定です。
</details>

<details>
<summary> 英語要旨 </summary>

Flow matching models have emerged as a powerful framework for realistic image generation by learning to reverse a corruption process that progressively adds Gaussian noise. However, because noise is injected in the latent domain, its impact on different frequency components is non-uniform. As a result, during inference, flow matching models tend to generate low-frequency components (global structure) in the early stages, while high-frequency components (fine details) emerge only later in the reverse process. Building on this insight, we propose Frequency-Aware Flow Matching (FreqFlow), a novel approach that explicitly incorporates frequency-aware conditioning into the flow matching framework via time-dependent adaptive weighting. We introduce a two-branch architecture: (1) a frequency branch that separately processes low- and high-frequency components to capture global structure and refine textures and edges, and (2) a spatial branch that synthesizes images in the latent domain, guided by the frequency branch's output. By explicitly integrating frequency information into the generation process, FreqFlow ensures that both large-scale coherence and fine-grained details are effectively modeled—low-frequency conditioning reinforces global structure, while high-frequency conditioning enhances texture fidelity and detail sharpness. On the class-conditional ImageNet-256 generation benchmark, our method achieves state-of-the-art performance with an FID of 1.38, surpassing the prior diffusion model DiT and flow matching model SiT by 0.79 and 0.58 FID, respectively. Code will be made available.
</details>

---

### Active Intelligence in Video Avatars Via Closed-loop World Modeling
著者: Xuanhua He, Tianyu Yang, Ke Cao, Rui-Qi Wu, Meng Cheng, Yong Zhang, Zhuoliang Kang, Xiaoming Wei, Qifeng Chen

<details>
<summary> 日本語要旨 </summary>

現在のビデオアバター生成方法は、アイデンティティ保持と動作整合性に優れていますが、本物のエージェンシーを欠いており、適応的な環境インタラクションを通じて自律的に長期目標を追求することはできません。これに対処するために、L-IVA（Long-horizon Interactive Visual Avatar）を導入しました。これは、確率生成環境における目的指向計画の評価のためのタスクとベンチマークであり、ORCA（Online Reasoning and Cognitive Architecture）はビデオアバターにおける能動的知性を可能にする初のフレームワークです。ORCAは、2つの主要な革新を通じて内部世界モデル（IWM）機能を具現化しています：(1) 予測された結果と実際の生成物を継続的に確認することで、生成不確実性下でも堅牢な状態追跡を維持する閉ループOTARサイクル（Observe-Think-Act-Reflect）、および(2) システム2が状態予測に基づく戦略的推論を行い、システム1が抽象的な計画をモデル固有の具体的なアクションキャプションに変換する階層的二重系統アーキテクチャ。ORCAは、POMDPとしてアバター制御を定式化し、結果の確認による連続的な信念更新を実装することで、オープンドメインシナリオにおける自律的多ステップタスク完了を可能にします。広範囲の実験は、ORCAが開ループおよび非反省ベースラインと比較してタスク成功率と行動一貫性で大幅に優れていることを示し、私たちのIWMに触発された設計がビデオアバター知能を受動的なアニメーションから能動的かつ目標指向の行動へと進化させることを確認しています。
</details>

<details>
<summary> 英語要旨 </summary>

Current video avatar generation methods excel at identity preservation and motion alignment but lack genuine agency—they cannot autonomously pursue long-term goals through adaptive environmental interaction. We address this by introducing L-IVA (Long-horizon Interactive Visual Avatar), a task and benchmark for evaluating goal-directed planning in stochastic generative environments, and ORCA (Online Reasoning and Cognitive Architecture), the first framework enabling active intelligence in video avatars. ORCA embodies Internal World Model (IWM) capabilities through two key innovations: (1) a closed-loop OTAR cycle (Observe-Think-Act-Reflect) that maintains robust state tracking under generative uncertainty by continuously verifying predicted outcomes against actual generations, and (2) a hierarchical dual-system architecture where System 2 performs strategic reasoning with state prediction while System 1 translates abstract plans into precise, model-specific action captions. By formulating avatar control as a POMDP and implementing continuous belief updating with outcome verification, ORCA enables autonomous multi-step task completion in open-domain scenarios. Extensive experiments demonstrate that ORCA significantly outperforms open-loop and non-reflective baselines in task success rate and behavioral coherence, validating our IWM-inspired design for advancing video avatar intelligence from passive animation to active, goal-oriented behavior.
</details>

---

### VGGT-$\Omega$
著者: Jianyuan Wang, Minghao Chen, Shangzhan Zhang, Nikita Karaev, Johannes Schönberger, Patrick Labatut, Piotr Bojanowski, David Novotny, Andrea Vedaldi, Christian Rupprecht

<details>
<summary> 日本語要旨 </summary>

私たちは、静的および動的シーンの両方に対して精度、効率性、能力を大幅に向上させるフィードフォワードモデルであるVGGT-Ωを提案します。これまでの研究では、VGGTなどのフィードフォワード3D再構成が既に伝統的な最適化ベースの手法と競争力を持つことが示されています。本研究では、これらのモデルの精度と堅牢性がモデル容量およびデータサイズに対して予測可能にスケールすることをさらに示します。3D再構成モデルを前例のない規模でトレーニングするため、動的シーンを処理する高品質なデータアノテーションパイプライン、自己監督学習プロトコル、メモリ要件を大幅に削減するアーキテクチャの変更を導入します。VGGTの複数の密な予測ヘッドを損失駆動型マルチタスク学習で置き換え、不安定なDPTブロックを削除し、シーントークンによる効率的なグローバルアテンションを導入することで、VGGTのアーキテクチャを大幅に簡素化します。これらの変更により、VGGT-Ωは監督データを20倍、非監督データを100倍増やしてトレーニングできる一方で、VGGTのメモリ要件の30%しか必要とせず、推論時には1.6倍速く動作します。その結果、VGGT-Ωは静的および動的シーンの両方で広範なベンチマークを通じて新たな3D再構成のステート・オブ・ザ・アートを確立し、例えばSintelデータセットにおけるカメラ推定精度を77%向上させました。モデルとコードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

We present VGGT-Ω, a feed-forward model for 3D reconstruction that substantially advances the state of the art in accuracy, efficiency, and capability for both static and dynamic scenes. Prior models such as VGGT have shown that feed-forward 3D reconstruction can already be competitive with traditional optimization-based methods. Here, we further demonstrate that the accuracy and robustness of these models scale predictably with model capacity and data size. To enable training 3D reconstruction models at an unprecedented scale, we introduce a high-quality data annotation pipeline that handles dynamic scenes, a self-supervised learning protocol, and architectural changes that greatly reduce memory requirements. We significantly simplify VGGT’s architecture by replacing multiple dense prediction heads with loss-driven multitask learning, removing unstable DPT blocks, and introducing more efficient global attention via scene tokens. These changes allow us to efficiently train VGGT-Ω with 20$\times$ more supervised data and 100$\times$ more unsupervised data than prior work, while requiring only 30% of VGGT’s memory and running 1.6$\times$ faster at inference. As a result, VGGT-Ω establishes a new state of the art for 3D reconstruction on both static and dynamic scenes across a wide range of benchmarks, e.g., improving the camera estimation accuracy by 77% on the Sintel dataset. Models and code will be publicly released.
</details>

---

### EmoTaG: Emotion-Aware Talking Head Synthesis on Gaussian Splatting with Few-Shot Personalization
著者: Haolan Xu, Keli Cheng, Lei Wang, Ning Bi, Xiaoming Liu

<details>
<summary> 日本語要旨 </summary>

音声駆動型3Dアニメーションの顔面合成は、Neural Radiance Fields（NeRF）や3D Gaussian Splatting（3DGS）を用いて急速に進化しています。フィーチャー・ショット法では、数秒間の動画から高精度なアバターを再構築することで即時の個別カスタマイズが可能です。しかし、自然な話す顔の生成には強力な感情認識運動モデリングが必要であり、既存のフィーチャー・ショット手法では表現豊かな顔面運動下で幾何学的不安定性や音声と感情の不一致が生じます。本研究では、Pretrain-and-Adaptパラダイムに基づくフィーチャー・ショット感情認識型3Dアニメーション合成フレームワークであるEmoTaGを提案します。我々の重要な洞察は、3Dガウス分布を直接変形するのではなく、構造化されたFLAMEパラメータ空間において運動予測を再定式化することであり、これにより安定かつ解釈可能な運動に強力な幾何学的事前知識が導入されます。この基盤の上で、感情的なリズムを音声から捉えつつ、音声に欠ける頭部姿勢や上顔面の手掛かりを補完することで表現力豊かで安定した運動生成が可能となるGated Residual Motion Network（GRMN）を提案します。広範囲にわたる実験により、EmoTaGは感情的表現力、唇の同期性、視覚的リアリズム、運動安定性において最先端のパフォーマンスを達成することが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

Audio-driven 3D talking head synthesis has advanced rapidly with Neural Radiance Fields (NeRF) and 3D Gaussian Splatting (3DGS). Few-shot methods enable instant personalization by reconstructing high-fidelity avatars from only a few seconds of video. However, achieving natural talking-head generation further requires strong emotion-aware motion modeling, and existing few-shot approaches exhibit geometric instability and audio-emotion mismatch under expressive facial motion. In this work, we present EmoTaG, a few-shot emotion-aware 3D talking head synthesis framework built on the Pretrain-and-Adapt paradigm. Our key insight is to reformulate motion prediction in a structured FLAME parameter space rather than directly deforming 3D Gaussians, which introduces strong geometric priors for stable and interpretable motion. Building upon this, we propose a Gated Residual Motion Network (GRMN), which can capture emotional prosody from audio while supplementing head pose and upper-face cues absent in audio to enable expressive yet stable motion generation. Extensive experiments demonstrate that EmoTaG achieves state-of-the-art performance in emotional expressiveness, lip synchronization, visual realism, and motion stability.
</details>

---

### Any4D: Unified Feed-Forward Metric 4D Reconstruction
著者: Jay Karhade, Nikhil Keetha, Yuchen Zhang, Tanisha Gupta, Akash Sharma, Sebastian Scherer, Deva Ramanan

<details>
<summary> 日本語要旨 </summary>

私たちは、メトリックスケールで密なフィードフォワード4D再構成を可能にするスケーラブルなマルチビュートランスフォーマー「Any4D」を提案します。Any4Dは、Nフレームの各ピクセルごとに運動と幾何学的予測を直接生成し、これまでの研究が通常2ビュー密なシーンフローやスパース3Dポイントトラッキングに焦点を当てるのとは対照的です。さらに、最近の単眼RGB動画からの4D再構成方法と異なり、Any4Dは利用可能であれば追加のモダリティやセンサー（例えば、RGB-Dフレーム、IMUに基づくエゴムーブメント、レーダードップラー測定）を処理することができます。このような柔軟なフレームワークを可能にする重要な革新の一つは、4Dシーンのモジュール化された表現です。具体的には、各ビューの4D予測はローカルカメラ座標で表されるエゴセントリックな要因（深度マップとカメラ内部パラメータ）を用いて符号化され、グローバルワールド座標で表されるアロケンティックな要因（カメラ外部パラメータとシーンフロー）が使用されます。私たちは多様なセットアップにおいて優れた性能を達成しました - 正確さ（2〜3倍の低誤差）と計算効率（15倍速い）の両方で、複数の下流応用への道を開きます。
</details>

<details>
<summary> 英語要旨 </summary>

We present Any4D, a scalable multi-view transformer for metric-scale, dense feed-forward 4D reconstruction. Any4D directly generates per-pixel motion and geometry predictions for N frames, in contrast to prior work that typically focuses on either 2-view dense scene flow or sparse 3D point tracking. Moreover, unlike other recent methods for 4D reconstruction from monocular RGB videos, Any4D can process additional modalities and sensors such as RGB-D frames, IMU-based egomotion, and Radar Doppler measurements, when available. One of the key innovations that allows for such a flexible framework is a modular representation of a 4D scene; specifically, per-view 4D predictions are encoded using a variety of egocentric factors (depthmaps and camera intrinsics) represented in local camera coordinates, and allocentric factors (camera extrinsics and scene flow) represented in global world coordinates. We achieve superior performance across diverse setups - both in terms of accuracy (2-3X lower error) and compute efficiency (15X faster) - opening avenues for multiple downstream applications.
</details>

---

### Spatial Retrieval Augmented Autonomous Driving
著者: Xiaosong Jia, Chenhe Zhang, Yule Jiang, Songbur Wong, Zhiyuan Zhang, chen chen, Shaofeng Zhang, Xuanhe Zhou, Xue Yang, Junchi Yan, Yu-Gang Jiang

<details>
<summary> 日本語要旨 </summary>

既存の自律走行システムは、環境認識にカメラやLiDAR、IMUなどのオンボードセンサーを依存しています。しかし、このパラダイムはドライブタイムの認識範囲が限られており、視野が狭い場合や遮蔽物がある場合、または暗闇や雨などの極端な条件下ではしばしば失敗します。対照的に、人間のドライバーは視界が悪くても道路構造を思い出すことができます。モデルにこの「記憶」能力を与えるために、「空間取得パラダイム」を提案します。これは、オフラインで取得した地理画像を追加入力として導入するものです。これらの画像は、Googleマップや保存された自律走行データセットなどのオフラインキャッシュから容易に取得できるため、追加センサーを必要とせず、既存のADスタックに簡単に統合可能です。実験では、まずGoogleマップAPIを使用してnuScenesデータセットに地理画像を追加し、新たなデータをエゴ車両の軌跡と整列させます。自律走行の5つのコアタスク（物体検出、オンラインマッピング、占有予測、エンドツーエンド計画、生成的世界モデリング）にわたってベースラインを確立します。広範な実験では、拡張されたモダリティが特定のタスクのパフォーマンス向上に寄与することが示されました。この新しい自律走行パラダイムのさらなる研究のため、データセットカリキュレーションコード、データ、ベンチマークをオープンソース化します。
</details>

<details>
<summary> 英語要旨 </summary>

Existing autonomous driving systems rely on onboard sensors (cameras, LiDAR, IMU, etc) for environmental perception. However, this paradigm is limited by the drive-time perception horizon and often fails under limited view scope, occlusion or extreme conditions such as darkness and rain. In contrast, human drivers are able to recall road structure even under poor visibility. To endow models with this "recall" ability, we propose the spatial retrieval paradigm, introducing offline retrieved geographic images as an additional input. These images are easy to obtain from offline caches (e.g, Google Maps or stored autonomous driving datasets) without requiring additional sensors, making it a plug-and-play extension for existing AD stacks. For experiments, we first extend the nuScenes dataset with geographic images retrieved via Google Maps APIs and align the new data with ego-vehicle trajectories. We establish baselines across five core autonomous driving tasks: object detection, online mapping, occupancy prediction, end-to-end planning, and generative world modeling. Extensive experiments show that the extended modality could enhance the performance of certain tasks. We will open-source dataset curation code, data, and benchmarks for further study of this new autonomous driving paradigm.
</details>

---

### Fast-ThinkAct: Efficient Vision-Language-Action Reasoning Via Verbalizable Latent Planning
著者: Chi-Pin Huang, Yunze Man, Zhiding Yu, Min-Hung Chen, Jan Kautz, Yu-Chiang Frank Wang, Fu-En Yang

<details>
<summary> 日本語要旨 </summary>

ビジョン言語行動（VLA）タスクは、複雑な視覚シーンを理解し、ダイナミックな環境で適応的にアクションを実行することを要求します。最近のVLAsに関する推論研究では、明示的なチェーン・オブ・サウザンド（CoT）が一般化能力を向上させることが示されていますが、長い推論トレースにより高いインフェリエンス遅延が発生します。我々はFast-ThinkActという効率的な推論フレームワークを提案し、これは言語化可能な潜在的推論によってコンパクトでありながらも優れた計画を実現します。Fast-ThinkActは教師からの知識伝達と、操作経路を調整することで言語的および視覚的計画能力を移転させることにより、潜在的CoTを用いて効率的な推論を学習します。これにより、コンパクトな推論とアクション実行を有効に結びつける推論強化ポリシー学習が可能になります。多様なエンボディド操作および推論ベンチマークでの広範囲な実験では、Fast-ThinkActは最先端の推論VLAsと比較してインフェリエンス遅延を89.3％削減しながらも、効果的な長期計画、少数ショット適応、および障害復旧能力を維持する強力なパフォーマンスを示しました。
</details>

<details>
<summary> 英語要旨 </summary>

Vision-Language-Action (VLA) tasks require reasoning over complex visual scenes and executing adaptive actions in dynamic environments. While recent studies on reasoning VLAs show that explicit chain-of-thought (CoT) can improve generalization, they suffer from high inference latency due to lengthy reasoning traces. We propose Fast-ThinkAct, an efficient reasoning framework that achieves compact yet performant planning through verbalizable latent reasoning. Fast-ThinkAct learns to reason efficiently with latent CoTs by distilling from a teacher, driven by a preference-guided objective to align manipulation trajectories that transfers both linguistic and visual planning capabilities for embodied control. This enables reasoning-enhanced policy learning that effectively connects compact reasoning to action execution. Extensive experiments across diverse embodied manipulation and reasoning benchmarks demonstrate that Fast-ThinkAct achieves strong performance with up to 89.3\% reduced inference latency over state-of-the-art reasoning VLAs, while maintaining effective long-horizon planning, few-shot adaptation, and failure recovery.
</details>

---

### XR-Poser: Accurate Egocentric Human Motion Estimation for AR/VR
著者: Zhenyu Li, Sai Kumar Dwivedi, Filip Maric, Carlos Chacón, Nadine Bertsch, Filippo Arcadu, Tomas Hodan, Michael Ramamonjisoa, Peter Wonka, Amy Zhao, Robin Kips, Cem Keskin, Anastasia Tkach, Chenhongyi Yang

<details>
<summary> 日本語要旨 </summary>

拡張現実（AR）/仮想現実（VR）体験において、自己中心的な3D人間の動作推定は不可欠ですが、限られた身体カバレッジ、頻繁な遮蔽、そしてラベル付きデータの希少性により困難を極めています。本稿では、これらの課題に対処するためのXR-Poserという方法を提案します。その主な貢献は以下の2点です：（1）時間的一貫性と空間的根拠付けが可能な姿勢推定用トランスフォーマーに基づくモデル、および（2）大規模なラベルのないデータセットを利用した訓練を可能にする自動ラベリングシステムです。提案されたモデルは完全に微分可能であり、アイデンティティ条件付きクエリ、マルチビュー空間補正、因果的時間注意、および計算量を一定に保ちながらキーポイントとパラメトリックボディ表現の両方をサポートします。提案された自動ラベリングシステムは、不確実性意識型半教師あり学習により、数百万フレームのラベルなしデータを用いて学習を拡張します。このシステムは教師-生徒スキーマに基づき、不確実性蒸留を通じて仮ラベルを生成し、トレーニングをガイドすることで、モデルがさまざまな環境に一般化することを可能にします。EgoBody3Mベンチマークにおける実験では、XR-Poserは2つの最先端手法よりも精度で12.2%と19.4%向上し、それぞれ時間的ジッタを22.2%と51.7%削減しています。さらに、私たちの自動ラベリングシステムは手首のMPJPEを13.1%改善します。
</details>

<details>
<summary> 英語要旨 </summary>

Egocentric 3D human motion estimation is essential for AR/VR experiences, yet remains challenging due to limited body coverage from the egocentric viewpoint, frequent occlusions, and scarce labeled data. We present XR-Poser, a method that addresses these challenges through two key contributions: (1) a transformer-based model for temporally consistent and spatially grounded body pose estimation, and (2) an auto-labeling system that enables the use of large unlabeled datasets for training. The proposed model is fully differentiable, introduces identity-conditioned queries, multi-view spatial refinement, causal temporal attention, and supports both keypoints and parametric body representations under a constant compute budget. The proposed auto-labeling system scales learning to tens of millions of unlabeled frames via uncertainty-aware semi-supervised training. The system follows a teacher–student schema to generate pseudo-labels and guide training with uncertainty distillation, enabling the model to generalize to different environments. In experiments on the EgoBody3M benchmark, XR-Poser outperforms two state-of-the-art methods by 12.2% and 19.4% in accuracy, and reduces temporal jitter by 22.2% and 51.7%, respectively. Furthermore, our auto-labeling system additionally improves the wrist MPJPE by 13.1%.
</details>

---

### CubeComposer: Spatio-Temporal Autoregressive 4K 360° Video Generation from Perspective Video
著者: Lingen Li, Guangzhi Wang, Xiaoyu Li, Zhaoyang Zhang, Qi Dou, Jinwei Gu, Tianfan Xue, Ying Shan

<details>
<summary> 日本語要旨 </summary>

仮想現実（VR）における重要な応用の一つとして、視点入力から高品質な360°パノラマ動画を生成することがあります。特に没入感のある体験には高解像度のビデオが不可欠です。既存の方法は、通常の拡散モデルの計算上の制約により、最大1K解像度での原生生成しかサポートせず、解像度を向上させるために非効率な後処理スーパーリゾリューションに依存しています。私たちは、CubeComposerという新しい空間時間自己回帰拡散モデルを導入します。これは4K解像度の360°動画を原生で生成することが可能です。ビデオを6つの面からなるキューブマップ表現に分解し、CubeComposerは計画的な空間時間順序でコンテンツを自己回帰的に合成します。これによりメモリ要求が削減されつつ高解像度の出力が可能となります。具体的には、多次元自己回帰の課題に対処するために以下を提案します：（1）360°動画生成をキューブ面および時間ウィンドウ全体で組織化し、一貫した合成を可能にする空間時間自己回帰戦略；（2）効率を向上させるためのスパースコンテキスト注意設計を備えたキューブ面コンテキスト管理メカニズム；および（3）境界縫い目を排除するための連続性に配慮した技術、具体的にはキューブ認識位置エンコーディング、パディング、ブレンド。ベンチマークデータセットを用いた広範な実験では、CubeComposerが原生解像度および視覚品質の両方で最先端手法を上回り、現実的なVRアプリケーションシナリオに対応することを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Generating high-quality 360° panoramic videos from perspective input is one of the crucial applications for virtual reality (VR), whereby high-resolution videos are especially important for immersive experience. Existing methods are constrained by computational limitations of vanilla diffusion models, only supporting $\leq$ 1K resolution native generation and relying on suboptimal post super-resolution to increase resolution. We introduce CubeComposer, a novel spatio-temporal autoregressive diffusion model that natively generates 4K-resolution 360° videos. By decomposing videos into cubemap representations with six faces, CubeComposer autoregressively synthesizes content in a well-planned spatio-temporal order, reducing memory demands while enabling high-resolution output. Specifically, to address challenges in multi-dimensional autoregression, we propose: (1) a spatio-temporal autoregressive strategy that orchestrates 360° video generation across cube faces and time windows for coherent synthesis; (2) a cube face context management mechanism, equipped with a sparse context attention design to improve efficiency; and (3) continuity-aware techniques, including cube-aware positional encoding, padding, and blending to eliminate boundary seams. Extensive experiments on benchmark datasets demonstrate that CubeComposer outperforms state-of-the-art methods in native resolution and visual quality, supporting practical VR application scenarios.
</details>

---

### When Token Pruning Is Worse Than Random: Understanding Visual Token Information in VLLMs
著者: Yahong Wang, Juncheng Wu, Zhangkai Ni, Longzhen Yang, Yihang Liu, Chengmei Yang, Ying Wen, Lianghua He, Xianfeng Tang, Hui Liu, Yuyin Zhou

<details>
<summary> 日本語要旨 </summary>

ビジョン大規模言語モデル（VLLMs）は、画像を表現するために数百の視覚トークンに依存しており、その結果として高い計算コストがかかります。トークンプルーニングは推論加速の有望な解決策を提供しますが、本研究では重要な観察を特定しました：より深い層（例えば20層を超える場合）において、既存のトレーニングフリーなプルーニング手法はランダムプルーニングと同等以上の性能を発揮しません。この劣化が「消失するトークン情報」によって引き起こされると仮定します。これは、視覚トークンがネットワーク深度が増すにつれて徐々にその重要性を失う現象です。この仮説を検証するために、トークンの情報内容をモデル出力確率の変化量で測定し、トークンの削除時の影響を評価します。この提案された指標を用いて視覚トークンの情報内容を層ごとに分析した結果、以下の3つの重要な発見があります：（1）層が深くなるにつれて、視覚トークンの情報は徐々に均一化し、最終的に「情報地平線」と呼ばれる中間層で消失します。この地平線を超えると、視覚トークンは冗長になります；（2）この地平線の位置は静的ではありません。光学文字認識（OCR）のような視覚的に集中したタスクでは、一般的なタスクであるビジュアルクエスチョンアンサー（VQA）と比較して、地平線がより深く延びます；（3）この地平線はモデル容量とも強い相関を持ち、より強力なVLLMs（例えばQwen2.5-VL）は、より弱いモデル（例えばLLaVA-1.5）に比べて深層の視覚トークンを使用します。これらの発見に基づき、深層での単純なランダムプルーニングがパフォーマンスと効率のバランスを効果的に取ることを示しました。さらに、ランダムプルーニングを組み込むことで既存手法の性能が一貫して向上します。DARTにランダムプルーニングを統合することで、視覚トークンを50％削減しながらもQwen-2.5-VL-7Bのパフォーマンスの93.9%を維持し、最先端の成果を達成します。
</details>

<details>
<summary> 英語要旨 </summary>

Vision Large Language Models (VLLMs) incur high computational costs due to their reliance on hundreds of visual tokens to represent images. While token pruning offers a promising solution for accelerating inference, this paper, however, identifies a key observation: in deeper layers (e.g., beyond the 20th), existing training-free pruning methods perform no better than random pruning. We hypothesize that this degradation is caused by **"vanishing token information''**, where visual tokens progressively lose their salience with increasing network depth. To validate this hypothesis, we quantify a token's information content by measuring the change in the model output probabilities upon its removal. Using this proposed metric, our analysis of the information of visual tokens across layers reveals three key findings: (1) As layers deepen, the information of visual tokens gradually becomes uniform and eventually vanishes at an intermediate layer, which we term as ``information horizon", beyond which the visual tokens become redundant;(2) The position of this horizon is not static; it extends deeper for visually intensive tasks, such as Optical Character Recognition (OCR), compared to more general tasks like Visual Question Answering (VQA);(3) This horizon is also strongly correlated with model capacity, as stronger VLLMs (e.g., Qwen2.5-VL) employ deeper visual tokens than weaker models (e.g., LLaVA-1.5).Based on our findings, we show that simple random pruning in deep layers efficiently balances performance and efficiency. Moreover, integrating random pruning consistently enhances existing methods. Using DART with random pruning achieves state-of-the-art results, maintaining 93.9\% of Qwen-2.5-VL-7B performance while pruning 50\% of visual tokens.
</details>

---

### BAgger: Backwards Aggregation for Mitigating Drift in Autoregressive Video Diffusion Models
著者: Ryan Po, Eric Ryan Chan, Changan Chen, Gordon Wetzstein

<details>
<summary> 日本語要旨 </summary>

自己回帰型ビデオモデルは次フレーム予測による世界モデリングの有望な手法ですが、露出バイアスという問題を抱えています。これは、クリーンなコンテキストでのトレーニングと自己生成フレームでの推論の不一致により、エラーが積み重なり品質が時間と共に低下することを指します。私たちはBackwards Aggregation（BAgger）という教師なしスキームを導入しました。これはモデル自身のロールアウトから修正的な軌道を構築し、エラーから回復する方法を学習させます。BAggerは、品質や多様性に影響を与える可能性がある少数ステップの蒸留と分布マッチング損失に依存する従来のアプローチとは異なり、標準的なスコアまたはフロー一致目的でトレーニングを行い、大規模な教師や長鎖のバックプロパゲーション・スルー・タイムを避けます。私たちはBAggerを因果的拡散変換器に実装し、テキストからビデオ生成、ビデオ延長、マルチプロンプト生成の評価を行いました。これにより、安定した長期間の動きと減少したドリフトでの優れた視覚的一貫性が観察されました。
</details>

<details>
<summary> 英語要旨 </summary>

Autoregressive video models are promising for world modeling via next-frame prediction, but they suffer from exposure bias: a mismatch between training on clean contexts and inference on self-generated frames, causing errors to compound and quality to drift over time. We introduce Backwards Aggregation (BAgger), a self-supervised scheme that constructs corrective trajectories from the model’s own rollouts, teaching it to recover from its mistakes. Unlike prior approaches that rely on few-step distillation and distribution-matching losses --which can hurt quality and diversity -- BAgger trains with standard score or flow matching objectives, avoiding large teachers and long-chain backpropagation through time. We instantiate BAgger on causal diffusion transformers and evaluate on text-to-video, video extension, and multi-prompt generation, observing more stable long-horizon motion and better visual consistency with reduced drift.
</details>

---

### Stabilizing Streaming Video Geometry Via Dynamic Feature Normalization
著者: Xiaoyang Lyu, Muxin Liu, Xiaoshan Wu, Ruicheng Wang, Yihua Huang, Yangtian Sun, Shaoshuai Shi, Xiaojuan Qi

<details>
<summary> 日本語要旨 </summary>

リアルワールドの応用、例えば自動運転、エンバディッドAI、大規模再構築においては、ストリーミングRGB入力から一貫した3D幾何学的推定が重要です。現代のモノクロジオメトリー基礎モデルは、シングルイメージで強い精度を達成していますが、連続入力においては深刻な時間的不一致を示し、特にスケール・シフトドリフティングによって支配されます。ターゲットとした実験分析を通じて、この不安定性の根本原因を追跡します：予測深度のスケールとシフトを直接決定する潜在的特徴統計の変動です。この洞察に基づき、私たちはDynamic Feature Normalization（DyFN）を導入します。これは軽量で因果的な再帰モジュールであり、時間とともに安定した幾何学を維持するために特徴統計を動的かつ堅牢に調整します。DyFNのみ（追加パラメーターがわずか2％）を微調整し、バックボーンを凍結したままで強力な事前学習されたモノクロジオメトリーモデルをストリーミングに適応させます。これにより、時間的一貫性を実現しつつシングルイメージの精度を損なうことなく済みます。四つのベンチマークで広範囲にわたる実験は、DyFNが不連続な層化や位置ジッターなどの時間的アーティファクトを効果的に排除し、最先端の時間的安定性を達成していることを示します。これは以前のストリーミング方法よりも最大14％改善し、さらに重い非因果的ビデオベースラインを上回っています。
</details>

<details>
<summary> 英語要旨 </summary>

Consistent 3D geometry estimation from streaming RGB input is crucial for real-world applications such as autonomous driving, embodied AI, and large-scale reconstruction. While modern monocular geometry foundation models achieve strong single-image accuracy, they exhibit severe temporal inconsistency on continuous input, notably dominated by scale–shift drifting. Through targeted empirical analysis, we trace this instability to its root cause: fluctuations in latent feature statistics, whose mean and variance directly determine the predicted depth’s scale and shift. Building on this insight, we introduce Dynamic Feature Normalization (DyFN), a lightweight, causal recurrent module that dynamically and robustly modulates feature statistics to maintain stable geometry over time. We adapt powerful pretrained monocular geometry models for streaming by finetuning only DyFN-- a mere 2\% additional parameters-- while keeping the backbone frozen, thereby achieving temporal consistency without compromising single-image accuracy. Extensive experiments across four benchmarks show that DyFN effectively eliminates temporal artifacts such as disjointed layering and positional jitter, and achieves state-of-the-art temporal stability, improving over prior streaming methods by up to 14\% and even outperforming heavier non-causal video baselines.
</details>

---

### ZINA: Multimodal Fine-grained Hallucination Detection and Editing
著者: Yuiga Wada, Kazuki Matsuda, Komei Sugiura, Graham Neubig

<details>
<summary> 日本語要旨 </summary>

多モーダル大規模言語モデル（MLLMs）はしばしば幻覚を生成し、出力が視覚コンテンツから逸脱することがあります。これらの幻覚は多様な形で現れるため、詳細レベルでの幻覚の検出は包括的な評価と分析に不可欠です。この目的を達成するために、私たちはMLLMs向けの多モーダル微細レベルの幻覚検出および編集の新しいタスクを提案します。さらに、ZINAという新しい方法を提案します。これは、詳細なレベルで幻覚されたスパンを特定し、そのエラータイプを6つのカテゴリーに分類し、適切な改善策を提案します。このタスク用のモデルをトレーニングおよび評価するために、私たちはVisionHallというデータセットを構築しました。これは12のMLLMsから得られた6,900件の出力と211人のアノテーターによって手動で注釈されたもの、およびエラータイプ間の依存関係を捉えるグラフベースの方法を用いて生成された20,000件の合成サンプルから構成されています。私たちはZINAが、GPT-4oやLlama-3.2などの既存手法を両方の検出および編集タスクで上回ることを示しました。
</details>

<details>
<summary> 英語要旨 </summary>

Multimodal Large Language Models (MLLMs) often generate hallucinations, where the output deviates from the visual content. Given that these hallucinations can take diverse forms, detecting hallucinations at a fine-grained level is essential for comprehensive evaluation and analysis. To this end, we propose a novel task of multimodal fine-grained hallucination detection and editing for MLLMs. Moreover, we propose ZINA, a novel method that identifies hallucinated spans at a fine-grained level, classifies their error types into six categories, and suggests appropriate refinements. To train and evaluate models for this task, we constructed VisionHall, a dataset comprising 6.9k outputs from twelve MLLMs manually annotated by 211 annotators, and 20k synthetic samples generated using a graph-based method that captures dependencies among error types. We demonstrated that ZINA outperformed existing methods, including GPT-4o and Llama-3.2, in both detection and editing tasks.
</details>

---

### DriveLaW: Unifying Planning and Video Generation in A Latent Driving World
著者: Tianze Xia, Yongkang Li, Lijun Zhou, Jingfeng Yao, Kaixin Xiong, Haiyang Sun, Bing Wang, Kun Ma, Guang Chen, Hangjun Ye, Wenyu Liu, Xinggang Wang

<details>
<summary> 日本語要旨 </summary>

自動運転において、世界モデルはシナリオの進化を学習し、現実世界の長尾課題に対処するために重要な役割を果たしています。しかし、現在のアプローチでは、世界モデルが限定的な役割にとどまっており、統一されたように見えるアーキテクチャ内であっても、世界予測と運動計画を分離したプロセスとして扱われています。このギャップを埋めるために、私たちはDriveLaWという新しいパラダイムを提案します。これはビデオ生成と運動計画を統一するものです。そのビデオジェネレーターから得られた潜在表現を直接プランナーに注入することで、DriveLaWは高品質な将来予測と信頼性のある軌道計画の間の固有の一貫性を保証します。具体的には、DriveLaWは二つのコアコンポーネントから構成されています：強力な世界モデルであるDriveLaW-Videoは、表現豊かな潜在表現を用いた高品質な予測生成を行い、DriveLaW-Actという拡散プランナーは、DriveLaW-Videoの潜在表現から一貫性があり信頼性のある軌道を生成します。これらのコンポーネントは三段階の進行的なトレーニング戦略によって最適化されます。私たちの統一パラダイムの力強さは、両タスクで新しい最先端の成果を示すことにより証明されています。DriveLaWはビデオ予測を大幅に進化させ、FIDで最高パフォーマンス作品を33.3%上回り、FVDでは1.8%向上しましたが、同時にNAVSIM計画ベンチマークで新記録を達成しています。
</details>

<details>
<summary> 英語要旨 </summary>

World models have become crucial for autonomous driving, as they learn how scenarios evolve over time to address the long-tail challenges of the real world. However, current approaches relegate world models to limited roles: they operate within ostensibly unified architectures that still keep world prediction and motion planning as decoupled processes. To bridge this gap, we propose DriveLaW, a novel paradigm that unifies video generation and motion planning. By directly injecting the latent representation from its video generator into the planner, DriveLaW ensures inherent consistency between high-fidelity future generation and reliable trajectory planning. Specifically, DriveLaW consists of two core components: DriveLaW-Video, our powerful world model that generates high-fidelity forecasting with expressive latent representations, and DriveLaW-Act, a diffusion planner that generates consistent and reliable trajectories from the latent of DriveLaW-Video, with both components optimized by a three-stage progressive training strategy. The power of our unified paradigm is demonstrated by new state-of-the-art results across both tasks. DriveLaW not only advances video prediction significantly, surpassing best-performing work by 33.3% in FID and 1.8% in FVD, but also achieves a new record on the NAVSIM planning benchmark.
</details>

---

### VibeToken: Scaling 1D Image Tokenizers and Autoregressive Models for Dynamic Resolution Generations
著者: Maitreya Patel, Jingtao Li, Weiming Zhuang, Yezhou Yang, Lingjuan Lyu

<details>
<summary> 日本語要旨 </summary>

我々は、任意の解像度やアスペクト比に対応する効率的で解像度非依存な自己回帰（AR）画像合成手法を導入し、大規模な場面でディフュージョンモデルとのギャップを縮めます。その核心には、VibeTokenという新たな解像度非依存な1Dトランスフォーマーに基づく画像トークナイザがあり、ユーザーの制御可能な動的な32～256トークンのシーケンスに画像をエンコードし、最先端の効率と性能のトレードオフを達成します。VibeTokenを基に、我々は任意の解像度に対応する出荷時からのサポートが可能なクラス条件付きARジェネレータであるVibeToken-Genを提示します。これにより、計算資源を大幅に削減しつつも任意の解像度への対応が可能となります。特筆すべきは、VibeToken-Genがわずか64トークンで1024×1024画像を合成し、3.94 gFIDを達成する点です。これに対して、ディフュージョンベースの最先端代替手法は1,024トークンを必要とし、5.87 gFIDを達成します。一方で、固定解像度のARモデルであるLlamaGenのように、推論FLOPsが解像度の二乗に比例して増加する（1024×1024では約11T FLOPs）のとは対照的に、VibeToken-Genは解像度に依存せず179G FLOPs（63.4倍効率的）を一定に保ちます。我々は、VibeTokenがAR視覚ジェネレーティブモデルの広範な生産用途での普及を解放する手助けとなることを期待しています。
</details>

<details>
<summary> 英語要旨 </summary>

We introduce an efficient, resolution-agnostic autoregressive (AR) image synthesis approach that generalizes to arbitrary resolutions and aspect ratios, narrowing the gap to diffusion models at scale. At its core is VibeToken, a novel resolution-agnostic 1D Transformer-based image tokenizer that encodes images into a dynamic, user-controllable sequence of 32–256 tokens, achieving a state-of-the-art efficiency and performance trade-off. Building on VibeToken, we present VibeToken-Gen, a class-conditioned AR generator with out-of-the-box support for arbitrary resolutions while requiring significantly fewer compute resources. Notably, VibeToken-Gen synthesizes 1024$\times$1024 images using only 64 tokens and achieves 3.94 gFID; by comparison, a diffusion-based state-of-the-art alternative requires 1,024 tokens and attains 5.87 gFID. In contrast to fixed-resolution AR models such as LlamaGen—whose inference FLOPs grow quadratically with resolution ($\approx$11T FLOPs at 1024$\times$1024)—VibeToken-Gen maintains a constant 179G FLOPs (63.4$\times$ efficient) independent of resolution. We hope VibeToken can help unlock the wide adoption of AR visual generative models in production use cases.
</details>

---

### MMBench-GUI: A Unified Hierarchical Evaluation Framework for Multi-Platform GUI Agents
著者: Xuehui Wang, Zhenyu Wu, JingJing Xie, Zichen Ding, Bowen Yang, Zehao Li, Zhaoyang Liu, Qingyun Li, Xuan Dong, Zhe Chen, Weiyun Wang, Xiangyu Zhao, Jixuan Chen, Haodong Duan, Tianbao Xie, Chenyu Yang, Shiqian Su, Yue Yu, Yanting Zhang, Xiangyu Yue, Weijie Su, Xizhou Zhu, Wei Shen, Jifeng Dai, Wenhai Wang

<details>
<summary> 日本語要旨 </summary>

私たちは、Windows、macOS、Linux、iOS、Android、Webを含む複数のプラットフォームにわたるGUI自動化エージェントの評価のための階層的ベンチマークであるMMBench-GUIを紹介します。このベンチマークは、GUIエージェントが必要とする4つのレベルにわたります：コンテンツ理解、要素固定、タスク自動化、タスク協調です。効果性と効率性を評価するために、さらにEfficiency–Quality-Aware（EQA）メトリックを提案します。これは、タスク成功のみならずアクション冗長性も測定します。広範囲な評価から、正確な視覚的固定がパフォーマンスにおける重要な決定因子であることが明らかになりました。これはモジュール化設計の特化した固定モジュールを持つ利点を強調しています。また、すべてのエージェントが大きな非効率性に苦しんでおり、多くのステップを経て最終的に成功するものの、タスクを完了します。パフォーマンスはまた、複雑またはクロスアプリケーションのタスクで低下し、メモリ、計画、適応的推論における弱点を露呈します。広範なカバレッジ、標準化されたプロトコル、新規のメトリックを提供することで、MMBench-GUIはGUIエージェント研究の進展に向けて初めて包括的な基盤を確立します。
</details>

<details>
<summary> 英語要旨 </summary>

We introduce MMBench-GUI, a hierarchical benchmark for evaluating GUI automation agents across Windows, macOS, Linux, iOS, Android, and Web. The benchmark spans four levels: Content Understanding, Element Grounding, Task Automation, and Task Collaboration, covering essential skills for GUI agents. To assess both effectiveness and efficiency, we further propose the Efficiency–Quality-Aware (EQA) metric, which measures task success alongside action redundancy. Extensive evaluations reveal that precise visual grounding is the critical determinant of performance, underscoring the advantages of modular designs with specialized grounding modules. Moreover, all agents suffer from substantial inefficiencies, frequently completing tasks with excessive steps despite eventual success. Performance also degrades on complex or cross-application tasks, exposing weaknesses in memory, planning, and adaptive reasoning. By providing broad coverage, standardized protocols, and novel metrics, MMBench-GUI establishes the first comprehensive foundation for advancing GUI agent research.
</details>

---

### VULCAN: Tool-Augmented Multi Agents for Iterative 3D Object Arrangement
著者: Zhengfei Kuang, Rui Lin, Long Zhao, Gordon Wetzstein, Saining Xie, Sanghyun Woo

<details>
<summary> 日本語要旨 </summary>

多様な2Dビジョン言語タスクにおける顕著な進歩にもかかわらず、マルチモーダル大規模言語モデル（MLLMs）の複雑な3Dシーン操作への応用は未だ十分に探求されていません。本研究では、この重要なギャップを埋めるために、MLLMsを使用した3Dオブジェクト配置タスクにおける三つの主要な課題に取り組みます。まず、MLLMsの弱い視覚的根拠を解決するために、プログラム編集と正確な3D結果をリンクさせることが難しい問題に対処します。これには、MCPベースのAPIを導入しています。このAPIは、壊れやすい原始コード操作からより堅牢な関数レベルの更新へとインタラクションを移行させます。次に、MLLMsの3Dシーン理解を強化するために、専門的な視覚ツール群を用いてシーン状態の分析、空間情報の収集、およびアクション結果の検証を行います。この知覚フィードバックループは、言語ベースの更新と正確な3D意識操作のギャップを埋めるために重要です。第三に、反復的でエラーが発生しやすい更新を管理するために、計画、実行、検証という指定された役割を持つ協調型マルチエージェントフレームワークを提案します。この分解により、システムは多段階の指示を堅牢に処理し、中間で発生するエラーから回復することが可能になります。私たちは、25種類の複雑なオブジェクト配置タスクの多様なセットで、既存のベースラインを大幅に上回るアプローチの有効性を示します。
</details>

<details>
<summary> 英語要旨 </summary>

Despite the remarkable progress of Multimodal Large Language Models (MLLMs) in 2D vision-language tasks, their application to complex 3D scene manipulation remains underexplored. In this paper, we bridge this critical gap by tackling three key challenges in 3D object arrangement task using MLLMs. First, to address the weak visual grounding of MLLMs, which struggle to link programmatic edits with precise 3D outcomes, we introduce an MCP-based API. This shifts the interaction from brittle raw code manipulation to more robust, function-level updates. Second, we augment the MLLM's 3D scene understanding with a suite of specialized visual tools to analyze scene state, gather spatial information, and validate action outcomes. This perceptual feedback loop is critical for closing the gap between language-based updates and precise 3D-aware manipulation. Third, to manage the iterative, error-prone updates, we propose a collaborative multi-agent framework with designated roles for planning, execution, and verification. This decomposition allows the system to robustly handle multi-step instructions and recover from intermediate errors. We demonstrate the effectiveness of our approach on a diverse set of 25 complex object arrangement tasks, where it significantly outperforms existing baselines.
</details>

---

### AMB3R: Accurate Feed-forward Metric-scale 3D Reconstruction with Backend
著者: Hengyi Wang, Lourdes Agapito

<details>
<summary> 日本語要旨 </summary>

私たちは、多視点フィードフォワードモデルであるAMB3Rを紹介します。これは、様々な3Dビジョンタスクに対応するメトリックスケールの密度3D再構築を行うものです。主要なアイディアとして、幾何学的推論における空間的コンパクト性を可能にするために、スパースでありながらコンパクトなボリュメトリックシーン表現をバックエンドとして利用します。AMB3Rは多視点再構築のみに訓練されていますが、非カルマチャライズドビジュアルオドメトリ（オンライン）や大規模な構造から運動推定への拡張を容易に行うことができることを示します。これは、タスク固有の微調整やテスト時最適化を必要としません。以前のポイントマップベースのモデルと比較して、私たちのアプローチはカメラ姿勢、深度、メトリックスケール推定、3D再構築において最先端の性能を達成し、さらに密な再構築事前情報を持つ典型的なベンチマークで最適化ベースのSLAMやSfM手法を超える結果を示します。
</details>

<details>
<summary> 英語要旨 </summary>

We present AMB3R, a multi-view feed-forward model for dense 3D reconstruction on a metric-scale that addresses diverse 3D vision tasks. The key idea is to leverage a sparse, yet compact, volumetric scene representation as our backend, enabling geometric reasoning with spatial compactness. Although trained solely for multi-view reconstruction, we demonstrate that AMB3R can be seamlessly extended to uncalibrated visual odometry (online) or large-scale structure from motion without the need for task-specific fine-tuning or test-time optimization. Compared to prior pointmap-based models, our approach achieves state-of-the-art performance in camera pose, depth, and metric-scale estimation, 3D reconstruction, and even surpasses optimization-based SLAM and SfM methods with dense reconstruction priors on common benchmarks.
</details>

---

### A Frame Is Worth One Token: Efficient Generative World Modeling with Delta Tokens
著者: Tommie Kerssies, Gabriele Berton, Ju He, Qihang Yu, Wufei Ma, Daan de Geus, Gijs Dubbelman, Liang-Chieh Chen

<details>
<summary> 日本語要旨 </summary>

ビデオ世界モデリングにおける多様な将来の状態を予測することは中心的な課題です。既存の世界モデルでは、複数の可能性のある未来を生成する計算コストが主要な制約となっています。最近の研究により、ビジョンファウンデーションモデル（VFM）の潜在空間で将来を予測することは、原画像空間で行うよりも効率が大幅に向上することが示されました。しかし、この進歩にもかかわらず、効率的なVFMベースの世界モデルは依然として主に識別的であり、多くの可能性のある未来を暗黙的に平均化した予測を生成します。明示的かつ効率的に多様な可能性のある未来をモデル化するために、我々はDeltaWorldを導入しました。これは、単一の前方通過で複数の可能性のある未来を生成する能力へとシフトした初めてのVFMベースの世界モデルです。DeltaWorldの中核には、連続するフレーム間の特徴差を単一のコンパクトな「delta」トークンにエンコードするDeltaTokというトークナイザーがあります。これにより、時間的に隣接する特徴マップ間の冗長性を効果的に削減します。未来をdeltaトークンで表現することで、DeltaWorldは並列で複数の多様な予測を効率的に生成します。密集した予測タスクにおける実験では、DeltaWorldが既存の生成型世界モデルよりも桁違いに効率的でありながら、現実世界の結果とより密接に一致する未来を予測可能であることが示されました。コードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

Anticipating diverse future states is a central challenge in video world modeling. A key limitation lies in the computational cost of generating multiple plausible futures with existing world models. Recent work demonstrates that predicting the future in the latent space of a vision foundation model (VFM), rather than in raw pixel space, greatly improves efficiency. Despite this progress, efficient VFM-based world models are still predominantly discriminative, producing predictions that implicitly average over many possible futures. To explicitly and efficiently model diverse plausible futures, we introduce DeltaWorld, the first VFM-based world model which shifts from deterministic prediction to the ability to generate multiple plausible futures in a single forward pass. At the core of DeltaWorld is DeltaTok, a tokenizer that encodes feature differences between consecutive frames into a single compact “delta” token, effectively reducing redundancy among temporally adjacent feature maps. By representing futures as delta tokens, DeltaWorld efficiently generates multiple diverse predictions in parallel. Experiments on dense forecasting tasks demonstrate that DeltaWorld is capable of predicting futures that more closely align with real-world outcomes, while being orders of magnitude more efficient than existing generative world models. Code will be made publicly available.
</details>

---

### Scaling View Synthesis Transformers
著者: Evan Kim, Hyunwoo Ryu, Thomas W. Mitchel, Vincent Sitzmann

<details>
<summary> 日本語要旨 </summary>

最近、幾何モデルを必要としないビュー合成トランスフォーマーが新規ビュー合成（NVS）において従来のアプローチを上回る結果を達成しています。これらは明示的な幾何モデリングに依存するものです。しかし、そのパフォーマンスが計算量とどのようにスケールするかについてはまだ十分に理解されていません。本研究では、ビュー合成トランスフォーマーのスケーリング法則を徹底的に分析し、計算量最適化されたNVSモデルの設計選択肢を明らかにします。特に重要なことに、以前はスケーラビリティが低いと考えられていたエンコーダー–デコーダーアーキテクチャが実際に計算量最適であることを発見しました。以前のエンコーダー–デコーダーメソッドの性能が劣っていた理由は、特定のアーキテクチャ設計と比較におけるトレーニング計算量の不一致にあったことを明らかにします。さまざまな計算量レベルで、私たちがスケーラブルビュー合成モデル（SVSM）と呼ぶエンコーダー–デコーダーアーキテクチャは、デコーダーのみのモデルと同様に効果的にスケールし、優れた性能–計算量パレートフロンティアを達成し、大幅に削減されたトレーニング計算量で実世界のNVSベンチマークにおいて従来の最先端技術を上回ることを示します。
</details>

<details>
<summary> 英語要旨 </summary>

Recently, geometry-free view synthesis transformers have achieved state-of-the-art results in Novel View Synthesis (NVS), outperforming traditional approaches that rely on explicit geometry modeling. However, the specific factors that govern how their performance scales with compute remain poorly understood. In this work, we conduct a rigorous analysis of the scaling laws for view synthesis transformers and elucidate a series of design choices for training compute-optimal NVS models. Most significantly, we find that an encoder–decoder architecture, which was previously found to be less scalable, can in fact be compute-optimal. We attribute the previously inferior performance of previous encoder–decoder methods to certain architectural choices and inconsistent training compute across comparisons. Across several compute levels, we demonstrate that our encoder–decoder architecture, which we call the Scalable View Synthesis Model (SVSM), scales as effectively as decoder-only models, achieves a superior performance–compute Pareto frontier, and outperforms the previous state-of-the-art on real-world NVS benchmarks with substantially reduced training compute.
</details>

---

### Thinking With Videos: Multimodal Tool-Augmented Reinforcement Learning for Long Video Reasoning
著者: Haoji Zhang, Xin Gu, Jiawen Li, Chixiang Ma, Sule Bai, Chubin Zhang, bowen zhang, zhichao zhou, Dongliang He, Yansong Tang

<details>
<summary> 日本語要旨 </summary>

マルチモーダル大規模言語モデル（MLLMs）のビデオ推論能力は、動画質問応答や時間的アンカリングなどの下流タスクにとって重要です。最近の手法では、テキストベースのチェーン・オブ・シンク（CoT）推論をMLLMsで探求していますが、これらの方法は特に長い動画や推論チェーンにおいて、限定的なクロスモーダル相互作用と増加する幻覚傾向を示すことが多いです。これらの課題に対処するため、私たちはビデオインテリジェンスをツール強化学習（VITAL）という新しいエンド・トゥ・エンド型エージェント動画推論フレームワークを提案します。視覚的なツールボックスにより、モデルは必要に応じて新しい動画フレームを密集サンプリングし、正確な長時間動画推論のためのマルチモーダルCoTを生成できます。私たちは、時間的アンカリングと質問応答が互いに利益をもたらすことを観察しました。したがって、監督学習用の高品質なマルチタスク動画推論データセットMTVR-CoT-72kおよび強化学習用のMTVR-RL-110kを構築しました。さらに、多タスク強化学習における難易度不均衡を軽減するために、難易度認識グループ相対ポリシーオプティマイゼーションアルゴリズム（DGRPO）を提案します。11の挑戦的な動画理解ベンチマークにおける広範な実験は、VITALが特に長時間動画シナリオで既存手法を上回り、動画質問応答と時間的アンカリングタスクの高度な推論能力を示しています。
</details>

<details>
<summary> 英語要旨 </summary>

The video reasoning ability of multimodal large language models (MLLMs) is crucial for downstream tasks like video question answering and temporal grounding. While recent approaches have explored text-based chain-of-thought (CoT) reasoning for MLLMs, these methods often suffer from limited cross-modal interaction and increased hallucination, especially with longer videos or reasoning chains. To address these challenges, we propose Video Intelligence via Tool-Augmented Learning (VITAL), a novel end-to-end agentic video reasoning framework. With a visual toolbox, the model can densely sample new video frames on demand and generate multimodal CoT for precise long video reasoning. We observe that temporal grounding and question answering are mutually beneficial for video understanding tasks. Therefore, we construct two high-quality multi-task video reasoning datasets MTVR-CoT-72k for supervised fine-tuning and MTVR-RL-110k for reinforcement learning. Moreover, we propose a Difficulty-aware Group Relative Policy Optimization algorithm (DGRPO) to mitigate difficulty imbalance in multi-task reinforcement learning. Extensive experiments on eleven challenging video understanding benchmarks demonstrate the advanced reasoning ability of VITAL, outperforming existing methods in video question answering and temporal grounding tasks, especially in long video scenarios.
</details>

---

### Hyperbolic Gramian Volumes for Multimodal Alignment
著者: Saiyang Na, Feng Jiang, Qifeng Zhou, Wenliang Zhong, Thao Dang, Yuzhi Guo, Hehuan Ma, Chunyuan Li, Weizhi An, Junzhou Huang

<details>
<summary> 日本語要旨 </summary>

多様なモダリティの対比的学習は通常、ペアワイズの類似性に依存して整列を行いますが、最近の研究ではグラミアン体積が異なるモダリティ間で高次の相関を捉えられることが示されています。しかし、L2正規化によりユークリッド空間のグラミアン体積は体積崩壊を起こし、単位近くに集中して差別的な分散が最小限になってしまいます。超球面幾何学の指数関数的な体積増加は自然とこの問題を解決するため、変動性を保持することでグラミアン整列を超球面空間に拡張する動機付けとなります。しかし、予備実験では純粋な超球面幾何学だけでは不十分であることが示されました：変動性を保持しつつも、クロスカテゴリーの差別化においてユークリッド基準線を下回っています。私たちは、ハイパーグラム（HyperGRAM）と呼ばれる混合幾何学フレームワークを導入します。これは、数値的に安定したローレンツモデルを用いて、ユークリッドの差別力と超球面の意味的変動性を学習可能な混合によって結びつけます。この体積は二重の役割を果たします：一致したトリプレットと不一致なトリプレットを差別化すると同時に、解釈空間（有効な多様モダリティ実現の集合）内での意味的感度を保持します。四つのビデオ・テキスト評価基準にわたる評価では、混合幾何学が純粋なユークリッドおよび純粋な超球面バリアントを一貫して上回り、ゼロショット改善を達成しました。また、異なるデータセット間の意味的感度は対照的な相関パターンを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Multimodal contrastive learning typically relies on pairwise similarities for alignment, but recent work has shown that Gramian volumes can capture higher-order correlations across modalities. However, Euclidean Gramian volumes suffer from volume collapse under L2 normalization, concentrating near unity with minimal discriminative variance. Hyperbolic geometry's exponential volume growth naturally addresses this via variance preservation, motivating us to extend Gramian alignment to hyperbolic space. Yet preliminary experiments reveal that pure hyperbolic geometry alone is insufficient: while it preserves variance, it underperforms Euclidean baselines on cross-category discrimination. We introduce HyperGRAM, a hybrid geometry framework that combines Euclidean discriminative stability with hyperbolic semantic variance through learnable mixing. Using the numerically stable Lorentz model, HyperGRAM enables volumes to serve dual roles: discriminating matched from mismatched triplets while preservingsemantic sensitivity within matched pairs that reflects interpretation spaces (the set of valid multimodal realizations). Evaluation across four video-text benchmarks demonstrates that hybrid geometry consistently outperforms both pure Euclidean and pure hyperbolic variants, achievingsignificant zero-shot improvements with cross-dataset semantic sensitivity exhibiting contrasting correlation patterns.
</details>

---

### MoVieS: Motion-Aware 4D Dynamic View Synthesis in One Second
著者: Chenguo Lin, Yuchen Lin, Panwang Pan, Yifan Yu, Tao Hu, Honglei Yan, Katerina Fragkiadaki, Yadong Mu

<details>
<summary> 日本語要旨 </summary>

私たちは、モーションに配慮したビュー合成モデルであるMoVieSを紹介します。これは、単眼動画から4Dダイナミックシーンを1秒以内に再構築するものです。MoVieSはピクセルアラインドなガウス原始体で動的3Dシーンを表現し、その時間変化する運動を明示的に監督します。これにより、単眼動画から初めて統一された外観、幾何学、および運動のモデリングが可能となり、再構築、ビュー合成、3Dポイント追跡を単一の学習ベースフレームワーク内で実現します。ビュー合成と幾何学的再構築を結びつけることにより、MoVieSはタスク固有の監督に依存することなく多様なデータセットで大規模なトレーニングが可能となります。その結果、シーンフロー推定や動くオブジェクト分割のようなゼロショットアプリケーションを自然にサポートします。広範囲にわたる実験がMoVieSの効果と効率を複数のタスクで検証し、競争力のあるパフォーマンスを達成しながらいくつかの桁にわたる高速化を提供しています。
</details>

<details>
<summary> 英語要旨 </summary>

We present MoVieS, a motion-aware view synthesis model that reconstruct 4D dynamic scenes from monocular videos in one second. It represents dynamic 3D scenes with pixel-aligned Gaussian primitives and explicitly supervises their time-varying motions. This allows, for the first time, the unified modeling of appearance, geometry and motion from monocular videos, and enables reconstruction, view synthesis and 3D point tracking within a single learning-based framework. By bridging view synthesis with geometry reconstruction, MoVieS enables large-scale training on diverse datasets with minimal dependence on task-specific supervision. As a result, it also naturally supports a wide range of zero-shot applications, such as scene flow estimation and moving object segmentation. Extensive experiments validate the effectiveness and efficiency of MoVieS across multiple tasks, achieving competitive performance while offering several orders of magnitude speedups.
</details>

---

### One Model, Many Budgets: Elastic Latent Interfaces for Diffusion Transformers
著者: Moayed Haji Ali, Willi Menapace, Ivan Skorokhodov, Dogyun Park, Anil Kag, Michael Vasilkovsky, Sergey Tulyakov, Vicente Ordonez, Aliaksandr Siarohin

<details>
<summary> 日本語要旨 </summary>

拡散変換器（DiTs）は高品質な生成を実現しますが、画像解像度にFLOPsを固定し、原則的な遅延と品質のトレードオフを制限し、入力空間トークン全体で計算リソースを均等に配分するため、重要でない領域へのリソースが無駄になります。私たちは、DiTと互換性のある入力画像サイズと計算を切り離すElastic Latent Interface Transformer（ELIT）というメカニズムを導入します。このアプローチでは、標準的なトランスフォーマーブロックが操作できる可変長の学習可能なトークンシーケンスとしてラテントインターフェースを挿入します。軽量なReadおよびWriteクロスアテンション層が空間トークンとラテント間で情報を移動し、重要な入力領域を優先します。尾部のラテントをランダムに落としてELITを訓練することで、初期のラテントが全体的な構造を捉える一方で、後半のラテントは詳細を洗練する情報を含む重要度順に並んだ表現を学ぶことができます。推論時には、計算制約に合わせてラテントの数を動的に調整できます。ELITは意図的に最小限に設計されており、2つのクロスアテンション層を追加するだけで、矯正流目標とDiTスタックを変更しません。さまざまなデータセットやアーキテクチャ（DiT、U-ViT、HDiT、MM-DiT）においてELITは一貫した向上をもたらします。ImageNet-1K 512pxでは、ELITはFIDスコアで平均35.3％、FDDスコアで39.6％の向上を達成しています。
</details>

<details>
<summary> 英語要旨 </summary>

Diffusion transformers (DiTs) achieve high generative quality but lock FLOPs to image resolution, limiting principled latency-quality trade-offs, and allocate computation uniformly across input spatial tokens, wasting resource allocation to unimportant regions. We introduce Elastic Latent Interface Transformer (ELIT), a drop-in, DiT-compatible mechanism that decouples input image size from compute. Our approach inserts a latent interface, a learnable variable-length token sequence on which standard transformer blocks can operate. Lightweight Read and Write cross-attention layers move information between spatial tokens and latents and prioritize important input regions. By training with random dropping of tail latents, ELIT learns to produce importance-ordered representations with earlier latents capturing global structure while later ones contain information to refine details. At inference, the number of latents can be dynamically adjusted to match compute constraints. ELIT is deliberately minimal, adding two cross-attention layers while leaving the rectified flow objective and the DiT stack unchanged. Across datasets and architectures (DiT, U-ViT, HDiT, MM-DiT), ELIT delivers consistent gains. On ImageNet-1K 512px, ELIT delivers an average gain of $35.3\%$ and $39.6\%$ in FID and FDD scores.
</details>

---

### Structural–Semantic Perception for Diffusion-Guided Temporal Forgery Localization
著者: Ligong Cao, Yeting Guo, Haoang Chi

<details>
<summary> 日本語要旨 </summary>

ディープフェイクフォレンジックの解釈性と責任を向上させるために、Temporal Forgery Localization（TFL）は正確に操作されたセグメントを特定することが重要です。しかし、既存の方法は二つの制約に直面しています：(1) ローカライゼーション精度で、一発予測モデルが固有の初期予測バイアスを修正できず、時間的強調がモダリティ内部の意味論的な偽造手掛かりを見逃し、ノイズに敏感なローカライゼーションを引き起こすこと、および(2) クロスデータセットの一般化で、固定スケールの時間的受容野が実際のシナリオにおける変動する操作期間を適応させることに苦労しています。これらの課題に対処するため、構造的・意味論的知覚と拡散ガイド付き精緻化に基づく統一フレームワークを提案します。構造的・意味論的知覚は二つの補完的なコンポーネントから成ります：(1) 構造的知覚、設計されたスケール重み割り当てネットワークを用いて変動する時間的範囲における操作期間を適応的にモデル化し、(2) 意味論的知覚、各モダリティ内の意味論的一貫性を分析するためのインターモーダル散乱。このようにして、まず低品質な偽造ローカライゼーション提案を抑制し、構造的かつ意味論的に信頼性のある候補セットを得ます。その後、拡散ベースの回帰ヘッドが候補を反復的に精緻化し、正確で時間的に一貫した境界軌道にします。複数のTFLベンチマークにおける広範な実験は、我々の方法が最先端の性能を達成していることを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

Temporal Forgery Localization (TFL) is crucial for enhancing the interpretability and accountability of deepfake forensics by precisely pinpointing the manipulated segments. However, existing methods face two limitations: (1) localization precision, where one-shot boundary prediction models fail to rectify inherent initial prediction biases, and temporal emphasis overlooks modality-internal semantic forgery cues, resulting in noise-sensitive localization, and (2) cross-dataset generalization, where fixed-scale temporal receptive fields struggle to accommodate varying manipulation durations across real-world scenarios. To address these challenges, we propose a unified framework based on structural–semantic perception and diffusion-guided refinement. The structural–semantic perception comprises two complementary components: (1) structural perception, which adaptively models manipulation durations across varying temporal spans using a designed scale weight allocation network, and (2) semantic perception, which analyzes the semantic consistency within each modality through intra-modal distillation. In this way, it first suppresses low-quality forgery localization proposals, yielding a structurally and semantically reliable candidate set. Then a diffusion-based regression head further iteratively refines the candidates into precise and temporally coherent boundary trajectories. Extensive experiments on multiple TFL benchmarks demonstrate that our method achieves state-of-the-art performance.
</details>

---

### AToken: A Unified Tokenizer for Vision
著者: Jiasen Lu, Liangchen Song, Mingze Xu, Byeongjoo Ahn, Yanjun Wang, Chen Chen, Afshin Dehghan, Yinfei Yang

<details>
<summary> 日本語要旨 </summary>

私たちは、画像、動画、および3Dアセットにわたる高品質の再構成と意味理解を実現する初めての統一視覚トークナイザーであるATokenを紹介します。既存のトークナイザーは、単一モダリティにおいて再構成または理解のどちらかに特化していますが、ATokenはこれら多様な視覚入力を共有4Dラテンスペースにエンコードし、タスクとモダリティを単一フレームワークで統合します。具体的には、任意の解像度および時間長さの視覚入力を処理するために4D回転位置埋め込みを持つピュアトランスフォーマーアーキテクチャを導入します。安定した訓練を確保するため、我々は敵対的な要素のない新しい訓練目標を提案し、知覚およびグラム行列損失を組み合わせて最先端の再構成品質を達成します。進化的な訓練カリキュラムを用いることで、ATokenは単一画像、動画、3Dから始まり、連続および離散ラテントークンの両方をサポートします。ATokenは、画像に対して0.21 rFIDと82.2%のImageNet精度、動画に対して3.01 rFVDと40.2%のMSRVTT検索精度、3Dに対して28.28 PSNRと90.9%の分類精度を達成します。下流アプリケーションでは、ATokenは視覚生成タスク（例：連続および離散トークンによる画像生成、テキストから動画の生成、画像から3D合成）と理解タスク（例：マルチモーダルLLMs）を可能にし、すべてのベンチマークで競争力のある性能を達成します。これらの結果は、統一視覚トークナイゼーションに基づく次世代マルチモーダルAIシステムの構築に向けた示唆を提供します。
</details>

<details>
<summary> 英語要旨 </summary>

We present AToken, the first unified visual tokenizer that achieves both high-fidelity reconstruction and semantic understanding across images, videos, and 3D assets. Unlike existing tokenizers that specialize in either reconstruction or understanding for single modalities, AToken encodes these diverse visual inputs into a shared 4D latent space, unifying both tasks and modalities in a single framework. Specifically, we introduce a pure transformer architecture with 4D rotary position embeddings to process visual inputs of arbitrary resolutions and temporal durations. To ensure stable training, we introduce an adversarial-free training objective that combines perceptual and Gram matrix losses, achieving state-of-the-art reconstruction quality. By employing a progressive training curriculum, AToken gradually expands from single images, videos, and 3D, and supports both continuous and discrete latent tokens. AToken achieves 0.21 rFID with 82.2% ImageNet accuracy for images, 3.01 rFVD with 40.2% MSRVTT retrieval for videos, and 28.28 PSNR with 90.9% classification accuracy for 3D.. In downstream applications, AToken enables both visual generation tasks (e.g., image generation with continuous and discrete tokens, text-to-video generation, image-to-3D synthesis) and understanding tasks (e.g., multimodal LLMs), achieving competitive performance across all benchmarks. These results shed light on the next-generation multimodal AI systems built upon unified visual tokenization.
</details>

---

### VSRELL: A Simple Baseline for Video Super-Resolution and Enhancement in Low-Light Environment
著者: Yanming hui, Fanhua Shang, Hongying Liu, Ben Wang, Zhenwei Zhang, Liang Wan, Wei Feng, Tong Xue, Bingqin Lv

<details>
<summary> 日本語要旨 </summary>

私たちは、低照度環境におけるビデオスーパー解像度と強化の統合学習スキームを提案します。このシステムはVSRELL（Video Super-Resolution and Enhancement in Low-Light environment）と名付けられ、低光量・低解像度（LLLR）の対応物からよく照明された高解像度（WIHR）シーケンスを回復することを目的としています。複数の劣化が複雑に結びついているため、この共同タスクは比較的少ない注目を受けてきました。私たちのアプローチでは、照明強調と空間時間超解像度を組み合わせてモデル化し、絡み合った劣化を分離します。具体的には、物理的な照明変動や個々のフレーム内でのノイズ分布を明示的にモデリングするダイナミックウィンドウパーティション戦略を採用した、Illumination-Noise Co-Optimization（INCO）ネットワークを導入します。これにより、フレーム間のノイズ蓄積や照明のチラつきを効果的に抑制し、動作補償と明るさ修正の同時最適化を実現します。また、Illumination-Sensitive Feature Propagation（ISFP）メカニズムも導入されており、階層的な照明感知ゲートユニットを使用して特徴チャンネル応答を適応的に調整します。特徴伝播の強度を調整し、メモリー特徴減衰戦略を用いることで、高品質な特徴の重み付けを強化し、エラー蓄積の伝播を抑制し、伝送効率を向上させます。実験結果は、VSRELLが明るさの連続性とテクスチャ忠実度を強化し、復元された出力における時間的一貫性を保持することを示しています。
</details>

<details>
<summary> 英語要旨 </summary>

We propose an integrated learning scheme of Video Super-Resolution and Enhancement in Low-Light environment, named VSRELL, which aims to recover Well-Illuminated High-Resolution (WIHR) sequence from Low-Light Low-Resolution (LLLR) counterparts. Due to the complex coupling of multiple degradations, this joint task has received relatively little attention. Our approach jointly models illumination enhancement and spatial-temporal super-resolution to disentangle intertwined degradations. Specifically, we introduce an Illumination-Noise Co-Optimization (INCO) network that employs a dynamic window partitioning strategy to explicitly model physical priors of illumination variations and noise distributions within individual frames of a long-term sequence. This effectively suppresses cross-frame noise accumulation and illumination flickering, achieving simultaneous optimization of motion compensation and brightness correction. Additionally, an Illumination-Sensitive Feature Propagation (ISFP) mechanism is introduced, which utilizes hierarchical illumination-sensing gating unit to adaptively modulate feature channel responses. By adjusting feature propagation intensity and using memory feature attenuation strategy, it can enhance the weighting of high-quality features and suppress error accumulation propagation and strengthen transmission efficiency. The experiments show that VSRELL can explicitly strengthen the brightness continuity and texture fidelity of the restored output, maintaining temporal consistency across the video.
</details>

---

### VisionLeaf: Entropy-Guided Leaf-First Reasoning for Efficient and Accurate Think-with-Image
著者: Haokun GUI, Senqiao Yang, Mingkang Zhu, Meng Chu, WU Sitong, Changsheng Lu, Zihao Wang, Zhuotao Tian, Jiaya Jia

<details>
<summary> 日本語要旨 </summary>

最近、「思考による画像」パラダイムが複雑な視覚的推論タスクで注目を集めています。しかし、既存のアプローチは固定された冗長な推論ステップによる推論効率の低さやトレーニングの不安定性に直面しています。この課題は主に標準的な強化学習ポリシーを直接使用することから生じ、これらは「思考による画像」マルチターン会話シナリオの改善を取り入れていません。この課題に対処するために、我々はエントロピー指導型木構造ベースの推論フレームワークであるVisionLeafを提案します。従来のGRPOではすべてのノードがルートから拡張され、各リーフには単一の枝しかありませんが、我々の方法はリーフノードから推論木を成長させ、エントロピーに基づいて最も価値のあるノードを選択して徹底的な展開探索を行います。このリーフファースト拡張は自然にマルチステップ画像分析の階層的性質と一致します。モデルやトレーニングデータを変更することなく、我々のVisionLeafはVSTARやHRBenchなどのベンチマークで4.2%のパフォーマンス向上を達成し、推論ラウンド数をほぼ半分に削減しています。これにより、精度と速度の両方で顕著な改善が示されています。すべてのコードは公開されます。
</details>

<details>
<summary> 英語要旨 </summary>

The "think-with-image” paradigm has recently gained traction for complex visual reasoning tasks. However, existing approaches often struggle with inference inefficiency due to a fixed number of redundant reasoning steps, as well as training instability. This challenge primarily arises from the direct use of standard reinforcement learning policies, which do not incorporate improvements for the think-with-image multi-turn conversational scenario. To address this challenge, we propose VisionLeaf, an entropy-guided, tree-based reasoning framework. Unlike conventional GRPO, where all nodes expand from the root and each leaf has only a single branch, our method grows the reasoning tree from the leaf nodes and selects the most valuable nodes based on entropy for thorough rollout exploration. This leaf-first expansion naturally aligns with the hierarchical nature of multi-step image analysis. Without modifying any model or training data, our VisionLeaf achieves a 4.2\% performance improvement on benchmarks such as VSTAR and HRBench, while reducing the number of inference rounds by nearly half—demonstrating significant gains in both accuracy and speed. All our code will be released.
</details>

---

### Attend Before Attention: Efficient and Scalable Video Understanding Via Autoregressive Gazing
著者: Baifeng Shi, Stephanie Fu, Long Lian, Hanrong Ye, David Eigen, Aaron Reite, Jan Kautz, Boyi Li, David Chan, Trevor Darrell, Pavlo Molchanov, Danny Yin

<details>
<summary> 日本語要旨 </summary>

マルチモーダル大規模言語モデル（MLLMs）は一般的なビデオ理解を進化させましたが、長時間かつ高解像度のビデオに対しては苦戦しています。これらのモデルはそのビジョントランスフォーマー（ViTs）やLLMsで重要でない空間的・時間的冗長性を持つピクセルも同様に処理します。私たちは、ViTまたはMLLMの前処理として冗長なパッチを除去する軽量モジュールであるAutoGazeを導入しました。次トークン予測と強化学習によって訓練されたAutoGazeは、ユーザー指定の誤差閾値内でビデオを再構成する最小限のマルチスケールパッチセットを自動的に選択します。これにより冗長性が除去されながら情報が保持されます。実験結果として、AutoGazeは視覚トークンを4倍から100倍削減し、ViTsおよびMLLMsの処理速度を最大19倍に加速します。これにより、1,000フレーム・4K解像度のビデオに対してMLLMsをスケールすることが可能となり、ビデオベンチマーク（例えばVideoMMEで66.5%）で優れた結果を達成します。さらに、AutoGazeでスケーリングされたMLLMが最新のSOTA MLLMよりも6.3%高い性能を示す、初めての4K解像度・長尺ビデオQAベンチマークであるHLVidを紹介します。
</details>

<details>
<summary> 英語要旨 </summary>

Multi-modal large language models (MLLMs) have advanced general-purpose video understanding but struggle with long, high-resolution videos---they process every pixel equally in their vision transformers (ViTs) or LLMs despite significant spatiotemporal redundancy. We introduce AutoGaze, a lightweight module that removes redundant patches before processed by a ViT or an MLLM. Trained with next-token prediction and reinforcement learning, AutoGaze autoregressively selects a minimal set of multi-scale patches that reconstructs the video within a user-specified error threshold, eliminating redundancy while preserving information. Empirically, AutoGaze reduces visual tokens by 4x-100x and accelerates ViTs and MLLMs by up to 19x, enabling scaling MLLMs to 1K-frame 4K-resolution videos and achieving superior results on video benchmarks (e.g., 66.5% on VideoMME). Furthermore, we introduce HLVid: the first high-resolution, long-form video QA benchmark with multi-minute 4K videos, where an MLLM scaled with AutoGaze outperform the previous SOTA MLLM by 6.3%.
</details>

---

### BiEvLight: Bi-level Learning of Task-Aware Event Refinement for Low-Light Image Enhancement
著者: Zishu Yao, Xiang-Xiang Su, Shengning Zhou, Guang-Yong Chen, Guodong Fan, Xing Chen

<details>
<summary> 日本語要旨 </summary>

イベントカメラは、その高いダイナミックレンジにより、ローカイト画像強調（LLIE）に大きな可能性を秘めています。既存の研究は主に効果的なモーダル融合戦略の設計に焦点を当てていますが、イベント内部の固有のバックグラウンド活動（BA）ノイズと画像の低い信号対雑音比（SNR）から生じる二重劣化により、モーダル融合中に深刻なノイズ結合が発生し、パフォーマンスのボトルネックとなっています。したがって、私たちは正確なイベントノイズ除去がイベントベース融合の全ポテンシャルを解放するための前提条件であると考えます。この目的のために、私たちは強化とノイズ除去の固有の相互依存性を活用して共同最適化を行う階層的かつタスク認識型フレームワークであるBiEvLightを提案します。具体的には、BiEvLightは画像とイベントの強い勾配相関を利用して、重度にノイズが多い領域で不十分なノイズ除去を軽減する勾配ガイド付きイベントノイズ除去事前条件を構築します。また、特定の強調目的に適応できず、必然的に過剰および不足したノイズ除去とのトレードオフが発生する静的な前処理段階として扱われることを回避し、強調タスクで制約された二重最適化問題として再定義します。クロストラック相互作用により、上位レベルのノイズ除去問題は下位レベルの強調目的に合わせたイベント表現を学習し、全体としての強調品質が大幅に向上します。リアルワールドノイズデータセットSEDでの広範な実験では、私たちの方法が最先端（SOTA）手法を大きく上回り、PSNRで平均1.30dB、PSNR*で2.03dB、SSIMで0.047の改善をそれぞれ達成しています。
</details>

<details>
<summary> 英語要旨 </summary>

Event cameras, with their high dynamic range, show great promise for Low-light Image Enhancement (LLIE). Existing works primarily focus on designing effective modal fusion strategies. However, a key challenge is the dual degradation from intrinsic background activity (BA) noise in events and low signal-to-noise ratio (SNR) in images, which causes severe noise coupling during modal fusion, creating a critical performance bottleneck. We therefore posit that precise event denoising is the prerequisite to unlocking the full potential of event-based fusion. To this end, we propose BiEvLight, a hierarchical and task-aware framework that collaboratively optimizes enhancement and denoising by exploiting their intrinsic interdependence. Specifically, BiEvLight exploits the strong gradient correlation between images and events to build a gradient-guided event denoising prior that alleviates insufficient denoising in heavily noisy regions. Moreover, instead of treating event denoising as a static pre-processing stage—which inevitably incurs a trade-off between over- and under-denoising and cannot adapt to the requirements of a specific enhancement objective—we recast it as a bilevel optimization problem constrained by the enhancement task. Through cross-task interaction, the upper-level denoising problem learns event representations tailored to the lower-level enhancement objective, thereby substantially improving overall enhancement quality. Extensive experiments on the Real-world noise Dataset SED demonstrate that our method significantly outperforms state-of-the-art (SOTA) approaches, with average improvements of 1.30dB in PSNR , 2.03dB in PSNR* and 0.047 in SSIM, respectively.
</details>

---

### SpatialTree: How Spatial Intelligence Branches Out in MLLMs
著者: Yuxi Xiao, longfei li, Shen Yan, Xinhang Liu, Sida Peng, Yunchao Wei, Xiaowei Zhou, Bingyi Kang

<details>
<summary> 日本語要旨 </summary>

多言語大規模言語モデル（MLLMs）において、空間知性（SI）は重要なフロンティアとして浮上し、基礎的な知覚から高度な空間推論までのスキル階層を包含しています。しかし、これらの能力がどのように獲得され、発達し、移行するかは未だ不明です。この問題を調査するために、私たちは空間知性を階層的な樹形図として整理する「SpatialTree」という階層分類法を提案します。これは低レベルの知覚（L1）から始まり、精神マッピング（L2）、精神シミュレーション（L3）、エージェント的能力（L4）へと続きます。この基盤の上で、私たちは提案する「Spatial Engine」を用いて階層・能力中心のベンチマークを構築し、各能力をそのレベルに応じて注釈付けします。ベンチマークの相関分析に基づき、重要な能力に対してターゲット指向の教師あり微調整（SFT）とプロンプティング実験を行います。結果は同レベルの能力の独立性を確認し、クロスレベル間の移行を明らかにし、さらにこれらの能力が共同で訓練された際の多能力シナジーを示します。私たちの研究はMLLMsにおけるSI分析のための新たなフレームワークを提供し、基礎的な能力がどのように発達し高次の能力を支えるかを総合的に研究する方法論を提示します。
</details>

<details>
<summary> 英語要旨 </summary>

Spatial Intelligence (SI) has emerged as a critical frontier for MLLMs, encompassing a hierarchy of skills from foundational perception to high level spatial reasoning. However, how these abilities are acquired, emerge, and transferred remains largely unknown. To investigate this, we propose SpatialTree a hierarchical taxonomy that organizes SI into a capability tree—from low level perception (L1), mental mapping (L2), mental simulation (L3), to agentic competence (L4). Building on this, we construct a hierarchical, capability-centric benchmark using our proposed Spatial Engine, annotating each ability according to its level. Guided by the benchmark's correlation analysis, we conduct targeted supervised fine-tuning (SFT) and prompting experiments on key abilities. The results confirm the independence of abilities at the same level, reveal cross-level transfer, and further demonstrate a multi-ability synergy when these abilities are trained jointly. Our work provides a novel framework for analyzing SI in MLLMs, offering a comprehensive methodology to study how foundational abilities emerge and support higher-level competencies.
</details>

---

### ForeHOI: Feed-forward 3D Object Reconstruction from Daily Hand-Object Interaction Videos
著者: Yuantao Chen, Jiahao Chang, Chongjie Ye, Chaoran Zhang, Zhaojie Fang, Chenghong Li, Xiaoguang Han

<details>
<summary> 日本語要旨 </summary>

日常の手と物体の相互作用を捉えたモノクル動画は、具現化された知性にとって貴重なリソースです。野生動画から3D手の再構築が大きく進展している一方で、関与する物体を再構築することは依然として困難であり、これは重度の遮蔽やカメラ、手、物体の複雑な結合動きによるものです。本論文では、モノクル手-物体相互作用ビデオから3D物体幾何を直接再構築する新しいフィードフォワードモデルであるForeHOIを紹介します。このモデルは、推論時間が1分以内に完了し、事前処理ステップの必要性を排除します。私たちの主な洞察は、フィードフォワードフレームワークで2Dマスクインパイントと3D形状補完の共同予測が、モノクル手持ち物体ビデオにおける重度の遮蔽問題を効果的に解決し、最適化ベースの方法よりも優れた結果を達成できるということです。2D形状補完と3D形状補完間の情報交換は全体的な再構築品質を向上させ、フレームワークが重度の手-物体遮蔽に効果的に対処できるようにします。また、私たちのモデルのトレーニングをサポートするために、手と物体の相互作用の最初の大規模かつ高精度な合成データセットを提供しました。このデータセットは包括的なアノテーションが付されています。広範な実験により、ForeHOIが物体再構築で最先端のパフォーマンスを達成し、約100倍の高速化と共に以前の方法を大幅に上回ることが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

The ubiquity of monocular videos capturing daily hand-object interactions presents a valuable resource for embodied intelligence. While 3D hand reconstruction from in-the-wild videos has seen significant progress, reconstructing the involved objects remains challenging due to severe occlusions and the complex, coupled motion of the camera, hands, and object. In this paper, we introduce ForeHOI, a novel feed-forward model that directly reconstructs 3D object geometry from monocular hand-object interaction videos within one minute of inference time, eliminating the need for any pre-processing steps. Our key insight is that, the joint prediction of 2D mask inpainting and 3D shape completion in a feed-forward framework can effectively address the problem of severe occlusion in monocular hand-held object videos, thereby achieving results that outperform the performance of optimization-based methods. The information exchanges between the 2D and 3D shape completion boosts the overall reconstruction quality, enabling the framework to effectively handle severe hand-object occlusion. Furthermore, to support the training of our model, we contribute the first large-scale, high-fidelity synthetic dataset of hand-object interactions with comprehensive annotations. Extensive experiments demonstrate that ForeHOI achieves state-of-the-art performance in object reconstruction, significantly outperforming previous methods with around a 100x speedup.
</details>

---

### Unified Customized Generation By Disentangled Reward Modeling
著者: Shaojin Wu, Mengqi Huang, Yufeng Cheng, wenxu wu, Jiahe Tian, Yiming Luo, Fei Ding, Qian HE

<details>
<summary> 日本語要旨 </summary>

既存の文献では、さまざまなカスタマイズ生成タスク（例えば、対象カスタマイズ生成、スタイルカスタマイズ生成）をそれぞれ異なる問題として扱い、各タスクが参照画像の特定の側面に焦点を当てています。しかし、これらの異なるカスタマイズタスクの目的は本質的に補完的であり、それらを統一されたフレームワーク内で相互に強化することが可能です。これらのタスクは基本的に参照画像から複数の特徴要素を分離することを含んでいるためです。この目的のため、私たちは**USO**（**U**nified **S**imultaneous **O**ptimizationフレームワーク）を導入しました。これは異なるカスタマイズタスク（すなわち、対象とスタイル）を同時に統一するものです。具体的に、USOはこれら二つのタスクを接続するサイクリックデータモデルフレームワークを導入しました。このフレームワークには、対象-スタイルデータキュレーションパイプラインとスタイル-対象モデルトレーニングパイプラインが含まれています。対象-スタイルデータキュレーションパイプラインは、最先端の対象カスタマイズモデルを利用して、コンテンツ画像、スタイル画像、およびそれに対応するスタイリッシュなコンテンツ画像から成る高品質のトリプレットデータを生成します。この基盤の上で、スタイル-対象モデルトレーニングパイプラインは、スタイルとコンテンツ特徴を同時に整合させるための補助的なスタイルリワードを導入し、これによりモデルが参照画像から望ましいスタイルまたはコンテンツ特徴を抽出する能力を強化します。広範な実験によって、USOがオープンソースモデルの中で最先端の性能を達成し、対象一貫性とスタイル類似度の両方で優れていることが示されました。
</details>

<details>
<summary> 英語要旨 </summary>

Existing literature typically treats various customized generation tasks (e.g., subject-customized generation, style-customized generation) as distinct and disjoint problems, with each task focusing solely on customizing a specific aspect of the reference image. However, we argue that the objectives of these different customization tasks are inherently complementary and can be mutually enhanced within a unified framework, as they fundamentally involve the disentanglement of multiple feature aspects from the reference image. To this end, we introduce **USO**, a **U**nified **S**imultaneous **O**ptimization framework to simultaneously unify different customized tasks (i.e., subject and style). Specifically, USO introduces a cyclical data-model framework that connects these two tasks by a subject-for-style data curation pipeline and a style-for-subject model training pipeline. The subject-for-style data curation pipeline leverages a state-of-the-art subject-customized model to generate high-quality triplet data comprising content images, style images, and their corresponding stylized content images. Building on this foundation, the style-for-subject model training pipeline introduces an auxiliary style reward to simultaneously align style and content features, thereby reinforcing the model’s ability to extract the desired style or content features from the reference image. Extensive experiments demonstrate that USO achieves state-of-the-art performance among open-source models, excelling in both subject consistency and style similarity.
</details>

---

