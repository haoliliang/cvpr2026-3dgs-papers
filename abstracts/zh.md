# CVPR 2026 3DGS 论文中文摘要

本页为 [README](../README.md) 中所列论文的**中文摘要**合集（由英文 arXiv 摘要翻译）。

> 翻译仅供阅读参考；如有出入请以原文为准。

---

<a id="paper-1"></a>
### [1] Bundle Adjusted Gaussian Avatars Deblurring
- **arXiv:** [2411.16758](https://arxiv.org/abs/2411.16758)

从多视角视频创建三维人体化身是计算机视觉中一项重要但极具挑战性的任务。然而，现有方法依赖高质量、清晰的图像作为输入，这在真实场景中往往难以获得，因为人体运动的速度和强度存在差异。本文提出一种新方法，可直接从模糊视频重建清晰的三维人体高斯化身。所提方法融合了面向三维、基于物理的人体运动模糊形成模型，以及用于消除运动诱导模糊歧义的三维人体运动模型。该框架支持从粗略初始化出发，联合优化化身表示与运动参数。我们在合成数据集以及使用360度同步混合曝光相机系统采集的真实世界数据集上建立了全面的基准。大量评估表明，该模型在多种条件下均有效。代码见：https://github.com/MyNiuuu/MAD-Avatar

---

<a id="paper-2"></a>
### [2] Turbo-GS: Accelerating 3D Gaussian Fitting for High-Quality Radiance Fields
- **arXiv:** [2412.13547](https://arxiv.org/abs/2412.13547)

新视角合成在计算机视觉中至关重要，可应用于三维重建、混合现实和机器人等领域。近年来，3D Gaussian Splatting（3DGS）等方法已成为最先进方案，可在实时条件下实现高质量的新视角合成。然而，训练 3DGS 模型仍然较慢，尤其在高分辨率图像上，对包含200个视角的场景往往需要数小时才能完成拟合。本工作旨在通过降低计算开销并提升学习效率来加速拟合过程。具体而言，我们引入膨胀渲染（dilated rendering）技术，仅渲染像素子集而非整幅图像，从而显著降低计算成本。为提升学习效率，我们设计了收敛感知的预算控制机制，在新高斯的添加与已有高斯的优化之间取得平衡。此外，为改善致密化效率并防止梯度消失，我们同时利用位置误差与外观误差来提升致密化的有效性。借助这些改进，我们实现了快速的4K分辨率拟合，同时保持甚至提升了新视角渲染质量。大量实验表明，本方法在显著加快优化的同时，仍能保持高渲染保真度。

---

<a id="paper-3"></a>
### [3] TT-GaussOcc: Test-Time Compute for Self-Supervised Occupancy Prediction via Spatio-Temporal Gaussian Splatting
- **arXiv:** [2503.08485](https://arxiv.org/abs/2503.08485)

自监督三维占用预测为理解复杂驾驶场景提供了一种有前景的方案，且无需代价高昂的三维标注。然而，训练稠密占用解码器以捕获细粒度几何与语义信息可能需要数百 GPU 小时；一旦训练完成，这类模型又难以在不进行大量重训练的情况下适应不同的体素分辨率或新物体类别。为克服这些局限，我们提出一种实用且灵活的测试时占用预测框架，称为 TT-Occ。该方法通过整合视觉基础模型（VFM），在运行时从原始传感器流中增量构建、优化并体素化时序感知的三维高斯。三维高斯的灵活表示支持在任意用户指定分辨率下进行体素化，而 VFM 的强泛化能力则支持准确感知与开放词汇识别，且无需任何网络训练或微调。为验证框架的通用性与有效性，我们给出两个变体：基于 LiDAR 的版本与以视觉为中心的版本，并在 Occ3D-nuScenes 与 nuCraft 基准上、于不同体素分辨率下进行了大量实验。实验结果表明，TT-Occ 显著优于现有计算代价高昂的自监督预训练方法。代码见：https://github.com/Xian-Bei/TT-Occ

---

<a id="paper-4"></a>
### [4] Let it Snow! Animating Static Gaussian Scenes With Dynamic Weather Effects
- **arXiv:** [2504.05296](https://arxiv.org/abs/2504.05296)

3D Gaussian Splatting 近期使静态三维场景的快速、照片级真实重建成为可能。然而，对此类场景进行动态编辑仍是一项重大挑战。我们提出一种新颖框架 Physics-Guided Score Distillation，以解决一个根本冲突：物理仿真提供了强运动先验，但不足以实现照片级真实感；而仅依赖基于视频的 Score Distillation Sampling（SDS）又无法为复杂的多粒子场景生成连贯运动。我们通过统一优化框架解决该问题：物理仿真引导 Score Distillation，在联合优化外观的同时共同精修运动先验以实现照片级真实感。具体而言，我们学习一个预测粒子运动与外观的神经动力学模型，并通过整合 Video-SDS（用于照片级真实感）与我们物理引导先验的联合损失进行端到端优化。这使得动力学保持合理的同时，仍可进行照片级真实感精修。该框架支持场景级动态天气效果，包括降雪、降雨、雾和沙尘暴，并具有物理上合理的运动。实验表明，我们的物理引导方法显著优于基线，消融实验进一步证实这种联合精修对于生成连贯、高保真动力学至关重要。

---

<a id="paper-5"></a>
### [5] Speedy Deformable 3D Gaussian Splatting: Fast Rendering and Compression of Dynamic Scenes
- **arXiv:** [2506.07917](https://arxiv.org/abs/2506.07917)

3D Gaussian Splatting（3DGS）的动态扩展通过神经运动场实现了高质量重建，但逐高斯的神经推理使这些模型计算代价高昂。在 DeformableGS 基础上，我们提出 Speedy Deformable 3D Gaussian Splatting（SpeeDe3DGS），通过三个互补模块弥合效率与保真度之间的差距：Temporal Sensitivity Pruning（TSP）通过时序聚合的敏感度分析移除低影响高斯；Temporal Sensitivity Sampling（TSS）扰动时间戳以抑制浮点伪影并改善时序一致性；GroupFlow 将学习到的形变场蒸馏为共享的 SE(3) 变换，以实现高效的组级运动。在 MonoDyGauBench 的50个动态场景上，将 TSP 与 TSS 集成到 DeformableGS 中，可在平均加速渲染 6.78 倍的同时保持神经场保真度，并使用 10 倍更少的基元。进一步加入 GroupFlow 后，渲染速度提升 13.71 倍，训练时间缩短 2.53 倍，在速度上超越所有基线，同时保持更优的图像质量。

---

<a id="paper-6"></a>
### [6] BulletGen: Improving 4D Reconstruction with Bullet-Time Generation
- **arXiv:** [2506.18601](https://arxiv.org/abs/2506.18601)

将随意拍摄的单目视频转换为完全沉浸式的动态体验是一项高度不适定任务，并伴随显著挑战，例如重建未见区域，以及处理单目深度估计中的歧义。本工作提出 BulletGen，利用生成模型来修正误差并补全基于高斯的动态场景表示中的缺失信息。具体做法是在单个冻结的“子弹时间”（bullet-time）步上，将基于扩散的视频生成模型输出与四维重建对齐，随后用生成帧监督四维高斯模型的优化。我们的方法将生成内容与静态及动态场景组件无缝融合，在新视角合成以及二维/三维跟踪任务上均达到最先进结果。

---

<a id="paper-7"></a>
### [7] HyperGaussians: High-Dimensional Gaussian Splatting for High-Fidelity Animatable Face Avatars
- **arXiv:** [2507.02803](https://arxiv.org/abs/2507.02803)

我们提出 HyperGaussians，这是 3D Gaussian Splatting 的一种新颖扩展，用于高质量可动画人脸化身。从视频创建此类精细人脸化身是一项具有挑战性的问题，在增强现实与虚拟现实中应用广泛。尽管静态人脸已取得巨大成功，但由单目视频得到的可动画化身仍落入恐怖谷。事实标准 3D Gaussian Splatting（3DGS）通过一组三维高斯基元表示人脸。3DGS 在渲染静态人脸上表现优异，但最先进方法仍难以应对非线性形变、复杂光照效应与精细细节。多数相关工作聚焦于从表情编码预测更优的高斯参数，而我们重新思考三维高斯表示本身以及如何使其更具表达力。我们的洞察将三维高斯扩展为高维多变量高斯，称为“HyperGaussians”。更高维度通过以可学习的局部嵌入为条件而增强表达力。然而，对 HyperGaussians 进行 splatting 计算代价高昂，因为需要求逆高维协方差矩阵。我们通过重参数化协方差矩阵——称为“inverse covariance trick”——解决该问题。该技巧显著提升了效率，使 HyperGaussians 可无缝集成到现有模型中。为展示这一点，我们将 HyperGaussians 接入快速单目人脸化身领域的最先进方法 FlashAvatar。在来自4个人脸数据集的19名受试者上的评估表明，HyperGaussians 在数值与视觉上均优于 3DGS，尤其在高频细节（如眼镜框、牙齿、复杂面部运动与镜面反射）方面表现突出。

---

<a id="paper-8"></a>
### [8] MoVieS: Motion-Aware 4D Dynamic View Synthesis in One Second
- **arXiv:** [2507.10065](https://arxiv.org/abs/2507.10065)

我们提出 MoVieS，一种 Motion-aware View Synthesis 模型，可在约一秒内从单目视频重建四维动态场景。它用与像素对齐的高斯基元表示动态三维场景，并显式监督其时变运动。这使得首次能够从单目视频统一建模外观、几何与运动，并在单一学习框架内同时支持重建、视角合成与三维点跟踪。通过将视角合成与几何重建桥接，MoVieS 可在多样化数据集上进行大规模训练，且对任务特定监督的依赖最小。因此，它也能自然支持多种零样本应用，如场景流估计与运动物体分割。大量实验验证了 MoVieS 在多项任务上的有效性与效率，在保持竞争力的同时实现数个数量级的加速。

---

<a id="paper-9"></a>
### [9] iLRM: An Iterative Large 3D Reconstruction Model
- **arXiv:** [2507.23277](https://arxiv.org/abs/2507.23277)

前馈式三维建模已成为快速、高质量三维重建的一种有前景方法。其中，直接生成显式三维表示（如 3D Gaussian Splatting）因其快速且高质量的渲染而备受关注。然而，许多基于 Transformer 架构的最先进方法存在严重可扩展性问题：它们依赖跨多输入视角图像 token 的全局注意力，导致随着视角数量或图像分辨率增加，计算成本变得不可承受。为迈向可扩展且高效的前馈三维重建，我们提出迭代式 Large 3D Reconstruction Model（iLRM），通过迭代精修机制生成三维高斯表示，并遵循三项核心原则：（1）将场景表示与输入图像解耦，以实现紧凑的三维表示；（2）将全局多视角交互分解为两阶段注意力方案以降低计算成本；（3）在每一层注入高分辨率信息以实现高保真重建。在 RE10K、DL3DV 等广泛使用的数据集上的实验结果表明，iLRM 在重建质量与速度上均优于现有方法。

---

<a id="paper-10"></a>
### [10] Uni3R: Unified 3D Reconstruction and Semantic Understanding via Generalizable Gaussian Splatting from Unposed Multi-View Images
- **arXiv:** [2508.03643](https://arxiv.org/abs/2508.03643)

从稀疏二维视角重建并语义理解三维场景仍是计算机视觉中的基本挑战。传统方法往往将语义理解与重建解耦，或需要代价高昂的逐场景优化，从而限制其可扩展性与泛化能力。本文提出 Uni3R，一种新颖的前馈框架，可从未标定的多视角图像直接联合重建统一的三维场景表示，并 丰富 开放词汇语义信息。我们的方法利用 Cross-View Transformer 在任意多视角输入间稳健融合信息，随后回归一组带有语义特征场的三维高斯基元。该统一表示可在单次前馈中支持高保真新视角合成、开放词汇三维语义分割与深度预测。大量实验表明，Uni3R 在多个基准上建立了新的最先进结果，包括在 RE10K 上达到 25.07 PSNR、在 ScanNet 上达到 55.84 mIoU。本工作标志着迈向可泛化、统一的三维场景重建与理解的新范式。代码见：https://github.com/HorizonRobotics/Uni3R

---

<a id="paper-11"></a>
### [11] PhysGM: Large Physical Gaussian Model for Feed-Forward 4D Synthesis
- **arXiv:** [2508.13911](https://arxiv.org/abs/2508.13911)

尽管基于物理的三维运动合成已有进展，现有方法仍面临关键局限：依赖由稠密多视角图像构建、且需耗时逐场景优化的预重建 3D Gaussian Splatting（3DGS）；物理集成要么通过不灵活的手工指定属性，要么通过使用 Score Distillation Sampling（SDS）的视频模型进行不稳定、优化代价高的引导；以及将预构建 3DGS 与物理模块简单拼接，忽略嵌入在外观中的物理信息，导致次优性能。为应对这些问题，我们提出 PhysGM，一种前馈框架，可从单张图像联合预测三维高斯表示与物理属性，从而立即进行仿真并实现高保真四维渲染。与缓慢且与外观无关的优化方法不同，我们首先预训练一个物理感知重建模型，直接推断高斯参数与物理参数。我们进一步用 Direct Preference Optimization（DPO）精修模型，使仿真与物理合理的参考视频对齐，并避免高代价的 SDS 优化。针对该任务缺乏支撑数据集的问题，我们提出 PhysAssets，包含 5 万+ 带有物理属性及对应参考视频的三维资产。实验表明，PhysGM 可在约一分钟内从单张图像生成高保真四维仿真，相较先前工作显著加速，同时提供真实感渲染。项目页：https://hihixiaolv.github.io/PhysGM.github.io/

---

<a id="paper-12"></a>
### [12] Polysemous Language Gaussian Splatting via Matching-based Mask Lifting
- **arXiv:** [2509.22225](https://arxiv.org/abs/2509.22225)

将二维开放词汇理解提升到 3D Gaussian Splatting（3DGS）场景是一项关键挑战。主流基于嵌入范式的方法存在三个核心缺陷：（i）几何-语义不一致，以点而非物体作为语义基础，限制语义保真度；（ii）向几何中注入 gigabytes 级特征数据导致语义膨胀；（iii）语义僵化，每个高斯单一特征难以捕获丰富的多义性（polysemy）。为克服这些局限，我们提出 ExtrinSplat，一种基于外在（extrinsic）范式、将几何与语义解耦的框架。ExtrinSplat 不嵌入特征，而是将高斯聚类为多粒度、重叠的三维物体组。随后由 Vision-Language Model（VLM）解释这些组以生成轻量级文本假设，构建原生支持复杂多义性的外在索引层。通过以轻量索引替代代价高昂的特征嵌入，ExtrinSplat 将场景适配时间从数小时降至数分钟，并将存储开销降低数个数量级。在开放词汇三维物体选择与语义分割基准任务上，ExtrinSplat 优于既有嵌入框架，验证了所提外在范式的有效性与效率。

---

<a id="paper-13"></a>
### [13] LTGS: Long-Term Gaussian Scene Chronology From Sparse View Updates
- **arXiv:** [2510.09881](https://arxiv.org/abs/2510.09881)

新视角合成的最新进展可从常规相机采集创建真实世界环境的照片级真实可视化。然而，日常环境频繁发生场景变化，需要普通设置难以覆盖的空间与时间稠密观测。我们提出基于稀疏视角更新的长期高斯场景时序建模方法，简称 LTGS，一种高效场景表示，可从高度欠约束的随意采集中适应日常变化。给定由初始输入图像得到的不完整、非结构化的 3D Gaussian Splatting（3DGS）表示，我们可稳健建模场景的长期时序演化，尽管存在突发移动与细微环境变化。我们将物体构建为 template Gaussians，作为共享物体轨迹的结构化、可复用先验。随后，物体模板经历进一步精修流程，在少样本观测下调制先验以适应时变环境。训练完成后，我们的框架可通过简单变换泛化到多个时间步，显著增强三维环境时序演化的可扩展性。由于现有数据集未显式表示稀疏采集设置下的长期真实世界变化，我们采集真实世界数据集以评估流程的实用性。实验表明，相较其他基线，我们的框架取得更优重建质量，同时支持快速、轻量更新。项目页：https://mkjjang3598.github.io/LTGS

---

<a id="paper-14"></a>
### [14] REALM: An MLLM-Agent Framework for Open World 3D Reasoning Segmentation and Editing on Gaussian Splatting
- **arXiv:** [2510.16410](https://arxiv.org/abs/2510.16410)

弥合复杂人类指令与精确三维物体定位之间的差距，仍是视觉与机器人领域的重大挑战。现有三维分割方法往往难以解释含糊、需推理的指令，而擅长此类推理的二维视觉-语言模型又缺乏内在三维空间理解。本文提出 REALM，一种创新的 MLLM-agent 框架，可在无需大量三维特定后训练的情况下实现开放世界推理式分割。我们直接在 3D Gaussian Splatting 表示上执行分割，利用其渲染适合 MLLM 理解的照片级真实新视角的能力。若直接将一个或多个渲染视角输入 MLLM，会对视角选择高度敏感；为此我们提出新颖的 Global-to-Local Spatial Grounding 策略。具体而言，多个全局视角首先并行输入 MLLM agent 进行粗粒度定位，聚合响应以稳健识别目标物体；随后合成若干目标物体的近景新视角以执行细粒度局部分割，得到准确且一致的三维掩码。大量实验表明，REALM 在 LERF、3D-OVS 以及我们新引入的 REALM3D 基准上，在解释显式与隐式指令方面均表现突出。此外，我们的 agent 框架无缝支持多种三维交互任务，包括物体移除、替换与风格迁移，展示了其实用性与通用性。项目页：https://ChangyueShi.github.io/REALM

---

<a id="paper-15"></a>
### [15] Diff4Splat: Controllable 4D Scene Generation with Latent Dynamic Reconstruction Models
- **arXiv:** [2511.00503](https://arxiv.org/abs/2511.00503)

我们提出 Diff4Splat，一种前馈方法，可从单张图像合成可控且显式的四维场景。我们的方法将视频扩散模型的生成先验与从大规模四维数据集学到的几何与运动约束统一起来。给定单张输入图像、相机轨迹以及可选文本提示，Diff4Splat 在单次前向传播中直接预测可形变的三维高斯场，编码外观、几何与运动，无需测试时优化或后处理精修。框架核心是一个 video latent transformer，扩展视频扩散模型以联合捕获时空依赖并预测时变三维高斯基元。训练由外观保真度、几何准确性与运动一致性目标引导，使 Diff4Splat 可在 30 秒内合成高质量四维场景。我们在视频生成、新视角合成与几何提取上验证了 Diff4Splat 的有效性，在动态场景合成上匹配或超越基于优化的方法，同时显著更高效。

---

<a id="paper-16"></a>
### [16] FastGS: Training 3D Gaussian Splatting in 100 Seconds
- **arXiv:** [2511.04283](https://arxiv.org/abs/2511.04283)

主流的 3D Gaussian Splatting（3DGS）加速方法未能在训练过程中恰当调节高斯数量，导致冗余的计算时间开销。本文提出 FastGS，一种新颖、简单且通用的加速框架，基于多视角一致性充分考虑每个高斯的重要性，高效解决训练时间与渲染质量之间的权衡。我们创新性地设计了基于多视角一致性的致密化与剪枝策略，无需预算机制。在 Mip-NeRF 360、Tanks & Temples 与 Deep Blending 数据集上的大量实验表明，我们的方法在训练速度上显著优于最先进方法：在 Mip-NeRF 360 上相较 DashGaussian 实现 3.32 倍训练加速且渲染质量相当，在 Deep Blending 上相较 vanilla 3DGS 实现 15.45 倍加速。我们证明 FastGS 具有强通用性，在动态场景重建、表面重建、稀疏视角重建、大规模重建以及 simultaneous localization and mapping（SLAM）等多种任务上均可带来 2–7 倍训练加速。项目页：https://fastgs.github.io/

---

<a id="paper-17"></a>
### [17] Changes in Real Time: Online Scene Change Detection with Multi-View Fusion
- **arXiv:** [2511.12370](https://arxiv.org/abs/2511.12370)

在线场景变化检测（Online Scene Change Detection, SCD）是一项极具挑战的问题，要求智能体在从任意视角观察场景时实时检测相关变化。现有在线 SCD 方法的准确度显著低于离线方法。我们提出首个在线 SCD 方法，具有与位姿无关、无需标注的特性，并保证多视角一致性，同时以超过 10 FPS 运行，达到新的最先进性能，甚至超越最佳离线方法。我们的方法引入新的自监督融合损失，从多种线索与观测推断场景变化；采用基于 PnP 的快速位姿估计相对参考场景；以及对 3D Gaussian Splatting 场景表示采用快速变化引导更新策略。在复杂真实世界数据集上的大量实验表明，我们的方法优于在线与离线基线。

---

<a id="paper-18"></a>
### [18] NeAR: Coupled Neural Asset-Renderer Stack
- **arXiv:** [2511.18600](https://arxiv.org/abs/2511.18600)

神经资产创作与神经渲染传统上作为相互独立的范式各自演进：前者为固定图形管线生成数字资产，后者将常规资产映射到图像。然而，将它们视为独立实体限制了端到端优化在保真度与一致性上的潜力。本文用 NeAR——Coupled Neural Asset–Renderer Stack——弥合这一差距。我们认为，协同设计资产表示与渲染器可形成更优生成的稳健“契约”。在资产侧，我们引入 Lighting-Homogenized SLAT（LH-SLAT）。借助 rectified-flow 模型，NeAR 将随意光照下的单张图像提升到规范、光照不变的 latent 空间，有效抑制烘焙阴影与高光。在渲染侧，我们设计面向光照的神经解码器，专门解释这些归一化 latent。以 HDR 环境贴图与相机视角为条件，它可在无需逐物体优化的情况下实时合成可重光照的 3D Gaussian splats。我们在四项任务上验证 NeAR：（1）基于 G-buffer 的前向渲染；（2）随机光照重建；（3）未知光照重光照；（4）新视角重光照。大量实验表明，我们的耦合栈在定量指标与感知质量上均优于最先进基线。我们希望这种耦合资产-渲染器视角能启发未来将神经资产与渲染器视为协同设计组件而非独立实体的图形栈。

---

<a id="paper-19"></a>
### [19] MetroGS: Efficient and Stable Reconstruction of Geometrically Accurate High-Fidelity Large-Scale Scenes
- **arXiv:** [2511.19172](https://arxiv.org/abs/2511.19172)

近期，3D Gaussian Splatting 及其衍生方法在大规模场景重建上取得重大突破。然而，如何高效且稳定地实现高质量几何保真度仍是核心挑战。为此，我们提出 MetroGS，一种用于复杂城市环境中高效、稳健重建的新颖 Gaussian Splatting 框架。我们的方法以分布式 2D Gaussian Splatting 表示为核心基础，作为后续模块的统一骨干。为处理复杂场景中可能的稀疏区域，我们提出结构化稠密增强方案：利用 SfM 先验与 pointmap 模型实现更稠密的初始化，并引入稀疏补偿机制以提升重建完整性。此外，我们设计渐进式混合几何优化策略，有机整合单目与多视角优化，实现高效且准确的几何精修。最后，针对大规模场景中常见的外观不一致，我们引入深度引导的外观建模，学习具有三维一致性的空间特征，促进几何与外观的有效解耦，并进一步提升重建稳定性。在大规模城市数据集上的实验表明，MetroGS 在几何精度与渲染质量上均表现优异，为高保真大规模场景重建提供统一解决方案。

---

<a id="paper-20"></a>
### [20] STAvatar: Soft Binding and Temporal Density Control for Monocular 3D Head Avatars Reconstruction
- **arXiv:** [2511.19854](https://arxiv.org/abs/2511.19854)

从单目视频重建高保真且可动画化的三维头部虚拟形象仍是一项具有挑战性但至关重要的任务。现有基于三维高斯溅射（3D Gaussian Splatting）的方法通常将高斯绑定到网格三角形上，并仅通过线性混合蒙皮（Linear Blend Skinning）建模形变，这导致运动刚性且表现力有限。此外，它们缺乏专门策略来处理频繁被遮挡的区域（例如口腔内部、眼睑）。为应对这些局限，我们提出 STAvatar，其包含两个关键组件：（1）UV 自适应软绑定（UV-Adaptive Soft Binding）框架，利用基于图像和几何的先验，在 UV 空间中学习每个高斯对应的特征偏移。该 UV 表示支持动态重采样，确保与自适应密度控制（Adaptive Density Control, ADC）完全兼容，并增强对形状与纹理变化的适应能力。（2）时序 ADC 策略，首先对结构相似的帧进行聚类，以便更有针对性地计算致密化准则；进一步引入一种新颖的融合感知误差作为克隆准则，联合捕捉几何与纹理差异，鼓励在需要更精细细节的区域进行致密化。在四个基准数据集上的大量实验表明，STAvatar 达到了最先进的重建性能，尤其在捕捉细粒度细节和重建频繁遮挡区域方面表现突出。

---

<a id="paper-21"></a>
### [21] Splatent: Splatting Diffusion Latents for Novel View Synthesis
- **arXiv:** [2512.09923](https://arxiv.org/abs/2512.09923)

辐射场表示方法近期已在扩散模型常用的 VAE 潜空间中受到探索。这一方向提供了高效渲染，并能与基于扩散的流程无缝集成。然而，这些方法面临一个根本性局限：VAE 潜空间缺乏多视图一致性，导致三维重建过程中纹理模糊且细节缺失。现有方法试图通过微调 VAE 来解决该问题，但会牺牲重建质量；或依赖预训练扩散模型恢复细粒度细节，但存在一定程度的幻觉风险。我们提出 Splatent，一种基于扩散的增强框架，旨在 VAE 潜空间中运行于三维高斯溅射（3D Gaussian Splatting, 3DGS）之上。我们的关键洞见偏离了传统的以三维为中心的视角：与其在三维空间中重建细粒度细节，我们通过多视图注意力机制从输入视图中在二维空间恢复细节。该方法在保持预训练 VAE 重建质量的同时，实现了忠实的细节恢复。在多个基准上的评估表明，Splatent 为 VAE 潜空间辐射场重建树立了新的最先进水平。我们进一步证明，将本方法与现有前馈框架集成后，能够一致地提升细节保留能力，为高质量稀疏视图三维重建开辟了新的可能性。代码可在项目页面获取：https://orhir.github.io/Splatent/

---

<a id="paper-22"></a>
### [22] Long-LRM++: Preserving Fine Details in Feed-Forward Wide-Coverage Reconstruction
- **arXiv:** [2512.10267](https://arxiv.org/abs/2512.10267)

可泛化高斯溅射（Gaussian Splatting, GS）的最新进展使从数十张输入视图进行前馈式场景重建成为可能。Long-LRM 显著将这一范式扩展至 32 张 $950\times540$ 分辨率的输入图像，在单次前向传播中实现 360° 场景级重建。然而，一次性直接预测数百万个高斯参数仍然高度误差敏感：位置或其他属性的微小偏差会导致明显模糊，尤其在文字等精细结构上。与此同时，隐式表示方法如 LVSM 和 LaCT 通过将场景信息压缩到模型权重而非显式高斯中，并使用完整的 transformer 或 TTT 骨干网络解码 RGB 帧，展示了显著更高的渲染保真度。然而，对每个渲染帧进行这种计算密集的解压过程，使实时渲染不可行。这些观察引出了关键问题：深度、顺序的"解压"过程是否必要？能否在保留隐式表示优势的同时实现实时性能？我们以 Long-LRM++ 回答这些问题，该模型采用半显式场景表示并结合轻量级解码器。Long-LRM++ 在 DL3DV 上达到与 LaCT 相当的渲染质量，同时在 A100 GPU 上实现 14 FPS 的实时渲染，克服了先前隐式方法的速度局限。我们的设计还可扩展至 64 张 $950\times540$ 分辨率的输入视图，展现了对更长输入序列的强泛化能力。此外，与直接从高斯渲染深度相比，Long-LRM++ 在 ScanNetv2 上提供了更优的新视角深度预测。大量消融实验验证了所提框架各组件的有效性。

---

<a id="paper-23"></a>
### [23] Off The Grid: Detection of Primitives for Feed-Forward 3D Gaussian Splatting
- **arXiv:** [2512.15508](https://arxiv.org/abs/2512.15508)

前馈式三维高斯溅射（3D Gaussian Splatting, 3DGS）模型能够实现实时场景生成，但受限于次优的像素对齐基元放置——其依赖稠密、刚性的网格，限制了质量与效率。我们引入一种新的前馈架构，在亚像素级别检测三维高斯基元，以自适应的"Off-The-Grid"分布替代像素网格。受关键点检测启发，我们的解码器学习在图像块上局部分布基元。我们还通过基于 Shannon 熵为每个块分配不同数量的基元，提供自适应密度机制。我们将所提解码器与预训练的三维重建骨干网络结合，在无三维标注的情况下，仅使用光度监督进行端到端训练。所得的无位姿模型可在数秒内生成照片级真实的三维高斯溅射场景，在前馈模型的新视角合成方面达到最先进水平。它在基元数量远少于竞争对手的同时超越现有方法，展示了更准确、更高效的分配策略，能够捕捉精细细节并减少伪影。项目页面：https://arthurmoreau.github.io/OffTheGrid/。

---

<a id="paper-24"></a>
### [24] Geometric-Photometric Event-based 3D Gaussian Ray Tracing
- **arXiv:** [2512.18640](https://arxiv.org/abs/2512.18640)

事件相机相比传统帧式相机具有更高的时间分辨率，使其适用于运动与结构估计。然而，基于事件的三维高斯溅射（3D Gaussian Splatting, 3DGS）方法如何利用稀疏事件的细粒度时间信息仍不明确。本工作提出 GPERT，一个框架，用于解决基于事件的三维高斯溅射在精度与时间分辨率之间的权衡。我们的核心思想是将渲染解耦为两个分支：逐事件的几何（深度）渲染与基于快照的辐射（强度）渲染，分别使用光线追踪与事件扭曲图像。大量评估表明，我们的方法在真实世界数据集上达到最先进水平，在合成数据集上具有竞争力。此外，所提方法无需先验信息（例如预训练图像重建模型）或基于 COLMAP 的初始化，在事件选择数量上更加灵活，并能在场景边缘实现清晰重建且训练速度快。我们希望本工作能加深对事件稀疏性在三维重建中作用的理解。https://github.com/e3ai/gpert

---

<a id="paper-25"></a>
### [25] EcoSplat: Efficiency-controllable Feed-forward 3D Gaussian Splatting from Multi-view Images
- **arXiv:** [2512.18692](https://arxiv.org/abs/2512.18692)

前馈式三维高斯溅射（3D Gaussian Splatting, 3DGS）能够实现高效的一次性场景重建，为新颖视角合成提供无需逐场景优化的三维表示。然而，现有方法通常为每个视图预测像素对齐的基元，在稠密视图设置下产生过量基元，且无法显式控制预测高斯的数量。为此，我们提出 EcoSplat，首个效率可控的前馈式 3DGS 框架，能够在推理时针对任意给定的目标基元数量自适应预测三维表示。EcoSplat 采用两阶段优化流程：第一阶段为像素对齐高斯训练（Pixel-aligned Gaussian Training, PGT），模型学习初始基元预测；第二阶段为重要性感知高斯微调（Importance-aware Gaussian Finetuning, IGF），模型学习对基元排序，并根据目标基元数量自适应调整其参数。在多种稠密视图设置上的大量实验表明，EcoSplat 在严格的基元数量约束下表现稳健，并超越最先进水平，非常适合灵活的下游渲染任务。

---

<a id="paper-26"></a>
### [26] GaussianDWM: 3D Gaussian Driving World Model for Unified Scene Understanding and Multi-Modal Generation
- **arXiv:** [2512.23180](https://arxiv.org/abs/2512.23180)

驾驶世界模型（Driving World Models, DWMs）随着生成模型的进展而快速发展。然而，现有 DWM 缺乏三维场景理解能力，只能基于输入数据生成内容，无法解释或推理驾驶环境。此外，当前方法用点云或 BEV 特征表示三维空间信息，无法将文本信息与底层三维场景精确对齐。为应对这些局限，我们提出一种基于三维高斯场景表示的新型统一 DWM 框架，同时支持三维场景理解与多模态场景生成，并能为理解与生成任务提供上下文增强。我们的方法通过将丰富的语言特征嵌入每个高斯基元，直接将文本信息与三维场景对齐，从而实现早期模态对齐。此外，我们设计了一种新颖的任务感知语言引导采样策略，去除冗余的三维高斯，并向 LLM 注入准确且紧凑的三维 token。进一步地，我们设计了双条件多模态生成模型，其中视觉-语言模型捕获的信息作为高级语言条件，与低级图像条件相结合，共同引导多模态生成过程。我们在 nuScenes 和 NuInteract 数据集上进行了全面研究以验证框架有效性。我们的方法达到最先进水平。代码将在 GitHub 公开发布：https://github.com/dtc111111/GaussianDWM。

---

<a id="paper-27"></a>
### [27] ParkGaussian: Surround-view 3D Gaussian Splatting for Autonomous Parking
- **arXiv:** [2601.01386](https://arxiv.org/abs/2601.01386)

泊车是自动驾驶系统（Autonomous Driving Systems, ADS）的关键任务，在拥挤车位和 GPS 拒止环境中面临独特挑战。然而，现有工作主要关注二维车位感知、建图与定位，三维重建仍探索不足，而这对捕捉泊车场景中的复杂空间几何至关重要。单纯提升重建泊车场景的视觉质量并不能直接惠及自动泊车，因为泊车的关键入口是车位感知模块。为应对这些局限，我们构建了首个专为泊车场景重建设计的基准 ParkRecon3D，包含来自四个环视鱼眼相机的传感器数据（含标定外参）及稠密车位标注。随后我们提出 ParkGaussian，首个将三维高斯溅射（3D Gaussian Splatting, 3DGS）用于泊车场景重建的框架。为进一步改善重建与下游车位检测之间的对齐，我们引入车位感知重建策略，利用现有泊车感知方法增强车位区域的合成质量。ParkRecon3D 上的实验表明，ParkGaussian 达到最先进的重建质量，并更好地保持下游任务的感知一致性。代码与数据集将发布于：https://github.com/wm-research/ParkGaussian

---

<a id="paper-28"></a>
### [28] Faster-GS: Analyzing and Improving Gaussian Splatting Optimization
- **arXiv:** [2602.09999](https://arxiv.org/abs/2602.09999)

三维高斯溅射（3D Gaussian Splatting, 3DGS）的最新进展聚焦于在保持重建质量的同时加速优化。然而，许多方法将实现层面的改进与根本性算法修改纠缠在一起，或以保真度换取性能，导致研究格局碎片化，使公平比较变得复杂。在本工作中，我们整合并评估了先前 3DGS 研究中最有效且广泛适用的策略，并补充若干新颖优化。我们进一步探究框架中探索不足的方面，包括数值稳定性、高斯截断与梯度近似。所得系统 Faster-GS 提供了一个严格优化的算法，我们在全面的基准套件上对其进行评估。实验表明，Faster-GS 在保持视觉质量的同时实现最高 5$\times$ 的训练加速，为 3DGS 优化建立了新的高性价比、资源高效基线。此外，我们证明这些优化可应用于四维高斯重建，实现高效的非刚性场景优化。

---

<a id="paper-29"></a>
### [29] B³-Seg: Camera-Free, Training-Free 3DGS Segmentation via Analytic EIG and Beta-Bernoulli Bayesian Updates
- **arXiv:** [2602.17134](https://arxiv.org/abs/2602.17134)

交互式三维高斯溅射（3D Gaussian Splatting, 3DGS）分割对于影视与游戏制作中预重建资产的实时编辑至关重要。然而，现有方法依赖预定义相机视角、真值标签或代价高昂的重训练，难以满足低延迟使用需求。我们提出 B$^3$-Seg（Beta-Bernoulli Bayesian Segmentation for 3DGS），一种在无需相机与无需训练条件下进行开放词汇 3DGS 分割的快速且理论有据的方法。我们将分割重新表述为序列 Beta-Bernoulli 贝叶斯更新，并通过解析期望信息增益（Expected Information Gain, EIG）主动选择下一视角。该贝叶斯形式保证了 EIG 的自适应单调性与次模性，从而对最优视角采样策略产生 $(1{-}1/e)$ 的贪心近似。在多个数据集上的实验表明，B$^3$-Seg 在数秒内完成端到端分割，达到与高开销监督方法相当的竞争力结果。实验结果证明，B$^3$-Seg 以可证明的信息效率实现了实用的交互式 3DGS 分割。

---

<a id="paper-30"></a>
### [30] RAP: Fast Feedforward Rendering-Free Attribute-Guided Primitive Importance Score Prediction for Efficient 3D Gaussian Splatting Processing
- **arXiv:** [2602.19753](https://arxiv.org/abs/2602.19753)

三维高斯溅射（3D Gaussian Splatting, 3DGS）已成为高质量三维场景重建的领先技术。然而，迭代细化与致密化过程会产生大量基元，每个基元对重建的贡献程度差异显著。因此，估计基元重要性对于重建过程中去除冗余以及实现高效压缩与传输至关重要。现有方法通常依赖基于渲染的分析，通过基元在多个相机视角下的贡献来评估其重要性。然而，这类方法对视角数量与选择敏感，依赖专用可微光栅化器，且计算时间随视角数量线性增长，难以作为即插即用模块集成，限制了可扩展性与泛化能力。为解决这些问题，我们提出 RAP，一种快速前馈、无需渲染、属性引导的 3DGS 高效重要性分数预测方法。RAP 直接从高斯内在属性与局部邻域统计推断基元重要性，避免基于渲染或依赖可见性的计算。紧凑的 MLP 使用渲染损失、剪枝感知损失与重要性分布正则化预测每个基元的重要性分数。在少量场景上训练后，RAP 能有效泛化至未见数据，并可无缝集成到重建、压缩与传输流程中。我们的代码公开发布于：https://github.com/yyyykf/RAP。

---

<a id="paper-31"></a>
### [31] tttLRM: Test-Time Training for Long Context and Autoregressive 3D Reconstruction
- **arXiv:** [2602.20160](https://arxiv.org/abs/2602.20160)

我们提出 tttLRM，一种新型大型三维重建模型，利用测试时训练（Test-Time Training, TTT）层实现长上下文、自回归三维重建，且具有线性计算复杂度，进一步扩展模型能力。我们的框架高效地将多幅图像观测压缩到 TTT 层的快速权重中，在潜空间形成隐式三维表示，可解码为多种显式格式（如 Gaussian Splats, GS）以供下游应用。我们模型的在线学习变体支持从流式观测中进行渐进式三维重建与细化。我们证明，在新视角合成任务上的预训练能有效迁移至显式三维建模，从而提升重建质量并加快收敛。大量实验表明，在物体与场景的前馈式三维高斯重建方面，我们的方法相比最先进水平取得更优性能。

---

<a id="paper-32"></a>
### [32] RU4D-SLAM: Reweighting Uncertainty in Gaussian Splatting SLAM for 4D Scene Reconstruction
- **arXiv:** [2602.20807](https://arxiv.org/abs/2602.20807)

将三维高斯溅射与同时定位与建图（Simultaneous Localization and Mapping, SLAM）结合已日益流行，因为它能在运动过程中实现连续的三维环境重建。然而，现有方法在动态环境中表现困难，尤其是运动物体会使三维重建复杂化，进而阻碍可靠跟踪。四维重建的兴起，尤其是四维高斯溅射，为应对这些挑战提供了有前景的方向，但其在四维感知 SLAM 中的潜力在很大程度上仍未被充分探索。沿此方向，我们提出一个鲁棒且高效的框架，即高斯溅射 SLAM 中的不确定性重加权（Reweighting Uncertainty in Gaussian Splatting SLAM, RU4D-SLAM），用于四维场景重建，将时间因子引入空间三维表示，同时融合对场景变化、模糊图像合成与动态场景重建的不确定性感知。我们通过集成运动模糊渲染增强动态场景表示，并通过扩展原本为静态场景设计的逐像素不确定性建模来处理模糊图像，从而改进不确定性感知跟踪。此外，我们提出语义引导的动态场景逐像素不确定性估计重加权机制，并引入可学习的不透明度权重以支持自适应四维建图。在标准基准上的大量实验表明，我们的方法在轨迹精度与四维场景重建方面大幅超越最先进水平，尤其在含运动物体与低质量输入的动态环境中表现突出。代码可用：https://ru4d-slam.github.io

---

<a id="paper-33"></a>
### [33] Dropping Anchor and Spherical Harmonics for Sparse-view Gaussian Splatting
- **arXiv:** [2602.20933](https://arxiv.org/abs/2602.20933)

近期的三维高斯溅射（3D Gaussian Splatting, 3DGS）Dropout 方法通过随机置零高斯不透明度来缓解稀疏视图条件下的过拟合。然而，我们发现这些方法存在邻域补偿效应：被丢弃的高斯往往被其邻居补偿，削弱了预期的正则化效果。此外，这些方法忽视了高阶球谐系数（Spherical Harmonics, SH）对过拟合的贡献。为解决这些问题，我们提出 DropAnSH-GS，一种新颖的基于锚点的 Dropout 策略。我们的方法并非独立丢弃高斯，而是随机选择某些高斯作为锚点并同时移除其空间邻居，从而有效破坏锚点附近的局部冗余，鼓励模型学习更鲁棒、全局信息更丰富的表示。进一步地，我们将 Dropout 扩展至颜色属性，随机丢弃高阶 SH，将外观信息集中于低阶 SH，进一步缓解过拟合，并支持训练后通过 SH 截断进行灵活的模型压缩。实验结果表明，DropAnSH-GS 在几乎不增加计算开销的情况下大幅超越现有 Dropout 方法，并可轻松集成到多种 3DGS 变体中以增强其性能。项目网站：https://sk-fun.fun/DropAnSH-GS

---

<a id="paper-34"></a>
### [34] BrepGaussian: CAD reconstruction from Multi-View Images with Gaussian Splatting
- **arXiv:** [2602.21105](https://arxiv.org/abs/2602.21105)

边界表示（Boundary Representation, B-Rep）将三维实体建模为其显式边界：修剪后的角、边和面。从无结构数据中恢复 B-Rep 表示是计算机视觉与图形学中具有挑战性且极具价值的任务。深度学习的最新进展大幅提升了三维形状几何的恢复，但仍依赖稠密且干净的点云，且难以泛化到新形状。我们提出 B-Rep Gaussian Splatting（BrepGaussian），一种从二维图像学习三维参数化表示的新型框架。我们采用带可学习特征的高斯溅射渲染器，并配合特定的拟合策略。为解耦几何重建与特征学习，我们引入两阶段学习框架：首先捕获几何与边，再细化面片特征以实现干净几何与连贯的实例表示。大量实验表明，我们的方法优于最先进水平。

---

<a id="paper-35"></a>
### [35] AeroDGS: Physically Consistent Dynamic Gaussian Splatting for Single-Sequence Aerial 4D Reconstruction
- **arXiv:** [2602.22376](https://arxiv.org/abs/2602.22376)

四维场景重建的最新进展显著改进了各领域的动态建模。然而，现有方法在单视图采集、宽空间范围以及空间占比有限且运动差异较大的动态物体的航空条件下仍然受限。这些挑战导致严重的深度歧义与不稳定运动估计，使单目航空重建本质上不适定。为此，我们提出 AeroDGS，一种面向单目 UAV 视频的物理引导四维高斯溅射框架。AeroDGS 引入单目几何提升（Monocular Geometry Lifting）模块，从单条航空序列重建可靠的静态与动态几何，为动态估计提供鲁棒基础。为进一步解决单目歧义，我们提出物理引导优化（Physics-Guided Optimization）模块，融入可微的地面支撑、直立稳定与轨迹平滑先验，将歧义图像线索转化为物理一致的运动。该框架联合细化静态背景与动态实体，实现稳定几何与连贯时序演化。我们还构建了涵盖多种高度与运动条件的真实 UAV 数据集，用于评估动态航空重建。在合成与真实 UAV 场景上的实验表明，AeroDGS 超越最先进水平，在动态航空环境中实现更优重建保真度。

---

<a id="paper-36"></a>
### [36] No Calibration, No Depth, No Problem: Cross-Sensor View Synthesis with 3D Consistency
- **arXiv:** [2602.23559](https://arxiv.org/abs/2602.23559)

我们呈现首个跨不同模态的跨传感器新视角合成研究。我们考察一个实用、基础但广泛被忽视的问题：获取对齐的 RGB-X 数据。多数 RGB-X 先前工作假设此类配对存在并聚焦模态融合，但实证上这需要大量标定工程投入。我们提出 match-densify-consolidate 方法：首先进行 RGB-X 图像匹配，随后进行引导点致密化；利用所提的置信度感知致密化与自匹配过滤，我们获得更好的视角合成，并将其整合到三维高斯溅射（3D Gaussian Splatting, 3DGS）中。我们的方法对 X 传感器不使用三维先验，且仅假设对 RGB 使用几乎零成本的 COLMAP。我们旨在消除各类 RGB-X 传感器的繁琐标定，通过可扩展方案突破大规模真实世界 RGB-X 数据采集的瓶颈，推动跨传感器学习的普及。

---

<a id="paper-37"></a>
### [37] SR3R: Rethinking Super-Resolution 3D Reconstruction With Feed-Forward Gaussian Splatting
- **arXiv:** [2602.24020](https://arxiv.org/abs/2602.24020)

三维超分辨率（3D Super-Resolution, 3DSR）旨在从低分辨率（Low-Resolution, LR）多视图图像重建高分辨率（High-Resolution, HR）三维场景。现有方法依赖稠密 LR 输入与逐场景优化，限制用于构建 HR 三维高斯溅射（3D Gaussian Splatting, 3DGS）的高频先验只能继承自预训练二维超分辨率（2D Super-Resolution, 2DSR）模型，严重制约重建保真度、跨场景泛化与实时可用性。我们将 3DSR 重新表述为从稀疏 LR 视图到 HR 3DGS 表示的直接前馈映射，使模型能够从大规模多场景数据中自主学习三维特定的高频几何与外观。这从根本上改变了 3DSR 获取高频知识的方式，并实现对未见场景的鲁棒泛化。具体而言，我们引入 SR3R，一种前馈框架，通过学习的映射网络直接从稀疏 LR 视图预测 HR 3DGS 表示。为进一步提升重建保真度，我们引入高斯偏移学习与特征细化，稳定重建并锐化高频细节。SR3R 即插即用，可与任意前馈 3DGS 重建骨干配对：骨干提供 LR 3DGS 骨架，SR3R 将其上采样为 HR 3DGS。在三个三维基准上的大量实验表明，SR3R 超越最先进（State-of-the-Art, SOTA）3DSR 方法，并实现强零样本泛化，甚至在未见场景上超越 SOTA 逐场景优化方法。

---

<a id="paper-38"></a>
### [38] Prune Wisely, Reconstruct Sharply: Compact 3D Gaussian Splatting via Adaptive Pruning and Difference-of-Gaussian Primitives
- **arXiv:** [2602.24136](https://arxiv.org/abs/2602.24136)

三维高斯溅射（3D Gaussian Splatting, 3DGS）的最新重大进展推动了实时照片级真实渲染的三维场景表示。3DGS 通常需要大量基元以实现高保真，导致冗余表示与高资源消耗，从而限制其在复杂或大规模场景中的可扩展性。因此，能够在减少冗余的同时保持视觉质量的有效剪枝策略与更具表达力的基元，对实际部署至关重要。我们提出一种高效、集成的重建感知剪枝策略，根据重建质量自适应确定剪枝时机与细化间隔，在减小模型规模的同时提升渲染质量。此外，我们引入三维 Difference-of-Gaussians 基元，在单个基元中联合建模正密度与负密度，提升紧凑配置下高斯的表达力。我们的方法显著改善模型紧凑性，在高斯数量上实现最高 90\% 的削减，同时提供与最先进水平相当、某些情况下更优的视觉质量。代码将公开发布。

---

<a id="paper-39"></a>
### [39] OnlineX: Unified Online 3D Reconstruction and Understanding with Active-to-Stable State Evolution
- **arXiv:** [2603.02134](https://arxiv.org/abs/2603.02134)

可泛化的 3D Gaussian Splatting（3DGS）近期进展已使 3D 场景重建在数秒内完成，无需逐场景优化。然而，现有方法主要遵循离线重建范式，缺乏持续重建能力，限制了其在机器人、VR/AR 等在线场景中的应用。本文提出 OnlineX，一种前馈框架，仅利用流式图像即可在线重建 3D 视觉外观场与语言场。在线设定的一个关键挑战是累积漂移问题，其根源在于记忆状态两种对立角色之间的根本冲突：主动角色需不断刷新以捕获高频局部几何，稳定角色则需保守地累积并保留长期全局结构。为此，我们引入解耦的 active-to-stable 状态演化范式：将记忆状态解耦为专用的 active state 与持久的 stable state，并协同地将前者信息融合进后者，以同时实现高保真与稳定性。此外，我们联合建模视觉外观场与语言场，并引入隐式 Gaussian 融合模块以提升重建质量。在主流数据集上的实验表明，本方法在新视角合成与语义理解上始终优于先前工作，在不同长度输入序列上均展现稳健性能，且具备实时推理速度。

---

<a id="paper-40"></a>
### [40] EmbodiedSplat: Online Feed-Forward Semantic 3DGS for Open-Vocabulary 3D Scene Understanding
- **arXiv:** [2603.04254](https://arxiv.org/abs/2603.04254)

在具身任务中，智能体需在线、近乎实时地构建并理解 3D 场景，因此在探索过程中即时理解 3D 场景至关重要。本研究提出 EmbodiedSplat，一种用于开放词汇场景理解的在线前馈 3DGS，可从流式图像同时完成在线 3D 重建与 3D 语义理解。与现有开放词汇 3DGS 方法通常局限于离线或逐场景优化设定不同，我们的目标有二：1）以在线方式从 300 余张流式图像重建整个场景的语义嵌入 3DGS；2）以前馈设计高度泛化至新场景，并结合实时 2D 模型支持近乎实时的 3D 语义重建。为实现上述目标，我们提出 Online Sparse Coefficients Field 与 CLIP Global Codebook，将 2D CLIP 嵌入绑定至各 3D Gaussian，同时最小化内存消耗并保留 CLIP 的完整语义泛化能力。此外，我们通过 3D U-Net 聚合 3DGS 的部分点云，生成 3D 几何感知 CLIP 特征，以弥补 2D 导向语言嵌入所缺失的 3D 几何先验。在 ScanNet、ScanNet++ 与 Replica 等多样化室内数据集上的大量实验验证了本方法的有效性与效率。项目页面：https://0nandon.github.io/EmbodiedSplat/。

---

<a id="paper-41"></a>
### [41] Where, What, Why: Toward Explainable 3D-GS Watermarking
- **arXiv:** [2603.08809](https://arxiv.org/abs/2603.08809)

随着 3D Gaussian Splatting 成为交互式 3D 资产的事实标准表示，鲁棒且不可察觉的水印技术至关重要。我们提出一种面向表示的原生框架，将"写入位置"与"质量保持方式"解耦。Trio-Experts 模块直接作用于 Gaussian 基元以推导载体选择先验，Safety and Budget Aware Gate（SBAG）将 Gaussian 分配至水印载体（针对扰动与码率预算优化比特鲁棒性）及视觉补偿器（与水印损失隔离）。为保持保真度，我们引入 channel-wise group mask 控制载体与补偿器的梯度传播，从而限制 Gaussian 参数更新、修复局部伪影，并在不增加运行时开销的前提下保留高频细节。该设计实现视角一致的水印持久性，并对压缩、噪声等常见图像失真具有强鲁棒性，在鲁棒性-质量权衡上优于先前方法。此外，解耦微调提供逐 Gaussian 归因，揭示消息承载位置及载体选择原因，实现可审计的可解释性。与最先进方法相比，本方法 PSNR 提升 +0.83 dB，比特准确率提升 +1.24%。

---

<a id="paper-42"></a>
### [42] Speeding Up the Learning of 3D Gaussians with Much Shorter Gaussian Lists
- **arXiv:** [2603.09277](https://arxiv.org/abs/2603.09277)

3D Gaussian Splatting（3DGS）已成为从多视角位姿图像学习辐射场的重要工具。尽管 3DGS 在渲染质量与效率上相较 NeRF 具有显著优势，进一步提升 3D Gaussian 学习效率仍是研究挑战。为应对此挑战，我们提出新颖训练策略与损失，以缩短渲染像素所用的各 Gaussian 列表，通过沿射线参与 splatting 的 Gaussian 数量更少来加速 splatting。具体而言，我们定期重置各 Gaussian 尺度以缩小其尺寸，鼓励较小 Gaussian 覆盖更少邻近像素，从而缩短像素的 Gaussian 列表。此外，我们对 alpha blending 过程引入熵约束，锐化沿各射线的 Gaussian 权重分布，使主导权重更大、次要权重更小。结果上，各 Gaussian 更聚焦于其主导像素，减少对邻近像素的影响，进一步缩短 Gaussian 列表。最终，我们将方法集成至渲染分辨率调度器，通过渐进式分辨率提升进一步改善效率。在广泛使用的 benchmark 上与最先进方法对比评估，结果显示本方法在效率上具有显著优势，且未牺牲渲染质量。

---

<a id="paper-43"></a>
### [43] VarSplat: Uncertainty-aware 3D Gaussian Splatting for Robust RGB-D SLAM
- **arXiv:** [2603.09673](https://arxiv.org/abs/2603.09673)

基于 3D Gaussian Splatting（3DGS）的 Simultaneous Localization and Mapping（SLAM）可实现快速、可微渲染及跨多样化真实场景的高保真重建。然而，现有 3DGS-SLAM 方法隐式处理测量可靠性，使位姿估计与全局对齐在低纹理区域、透明表面或复杂反射特性区域易受漂移影响。为此，我们提出 VarSplat，一种不确定性感知的 3DGS-SLAM 系统，显式学习 per-splat 外观方差。通过 total variance 法则与 alpha compositing，我们以高效单次光栅化渲染可微 per-pixel 不确定性图。该图引导 tracking、子图配准与 loop detection 聚焦可靠区域，有助于更稳定的优化。在 Replica（合成）及 TUM-RGBD、ScanNet、ScanNet++（真实世界）上的实验表明，VarSplat 提升了鲁棒性，在 tracking、mapping 与新视角合成渲染上相较现有稠密 RGB-D SLAM 研究达到具有竞争力或更优的表现。

---

<a id="paper-44"></a>
### [44] 4DEquine: Disentangling Motion and Appearance for 4D Equine Reconstruction from Monocular Video
- **arXiv:** [2603.10125](https://arxiv.org/abs/2603.10125)

从单目视频进行马科动物（如马）4D 重建对动物福利具有重要意义。先前主流 4D 动物重建方法需对整个视频联合优化运动与外观，耗时且对不完整观测敏感。本工作提出 4DEquine，通过将 4D 重建问题解耦为两个子问题：动态运动重建与静态外观重建。对于运动，我们引入简洁有效的 spatio-temporal transformer 及后优化阶段，从视频回归平滑且像素对齐的 pose 与 shape 序列。对于外观，我们设计新颖前馈网络，从少至单张图像重建高保真、可动画的 3D Gaussian avatar。为辅助训练，我们构建大规模合成运动数据集 VarenPoser（含高质量表面运动与多样化相机轨迹）及合成外观数据集 VarenTex（通过 multi-view diffusion 生成的真实多视角图像）。仅在合成数据上训练，4DEquine 在真实世界 APT36K 与 AiM 数据集上达到 state-of-the-art 性能，展现了 4DEquine 与新数据集在几何与外观重建上的优越性。全面消融实验验证了运动与外观重建网络的有效性。项目页面：https://luoxue-star.github.io/4DEquine_Project_Page/。

---

<a id="paper-45"></a>
### [45] RetimeGS: Continuous-Time Reconstruction of 4D Gaussian Splatting
- **arXiv:** [2603.13783](https://arxiv.org/abs/2603.13783)

时间重定时（temporal retiming）——在任意时间戳重建并渲染动态场景——对慢动作播放、时间编辑与后期制作等应用至关重要。然而，多数现有 4D Gaussian Splatting（4DGS）方法在离散帧索引上过拟合，难以表示连续时间帧，在时间戳间插值时产生 ghosting 伪影。我们将此局限识别为一种 temporal aliasing，并提出 RetimeGS，一种简洁有效的 4DGS 表示，显式定义 3D Gaussian 的时间行为并缓解 temporal aliasing。为实现平滑一致的插值，我们结合 optical flow 引导的初始化与监督、triple-rendering 监督及其他针对性策略。这些组件共同实现大运动下无 ghost、时间连贯的渲染。在含快速运动、非刚性形变与严重遮挡的数据集上，RetimeGS 在质量与连贯性上优于 state-of-the-art 方法。

---

<a id="paper-46"></a>
### [46] PhyGaP: Physically-Grounded Gaussians with Polarization Cues
- **arXiv:** [2603.14001](https://arxiv.org/abs/2603.14001)

3D Gaussian Splatting（3DGS）近期进展通过 deferred rendering（DR）在建模反射 3D 物体及其与环境交互方面取得巨大成功。然而，现有方法常难以正确重建 albedo、reflectance 等物理属性，因而无法支持高保真 relighting。我们观察到，该局限源于 RGB 图像缺乏形状与材质信息，遂提出 PhyGaP，一种 physically-grounded 3DGS 方法，利用 polarization cues 促进精确反射分解及重建物体的视觉一致 relighting。具体而言，我们设计 polarimetric deferred rendering（PolarDR）过程以建模偏振反射，以及 self-occlusion-aware environment map 构建技术（GridMap）以解析非凸物体的间接光照。在多个合成与真实场景（含仅含部分 polarization cues 的场景）上的验证表明，PhyGaP 不仅在反射 3D 物体外观与表面法线重建上表现优异（相较现有 RGB 方法平均 PSNR 约高 2 dB、Cosine Distance 约优 45.7%），且达到 state-of-the-art 的 inverse rendering 与 relighting 能力。代码即将发布。

---

<a id="paper-47"></a>
### [47] E2EGS: Event-to-Edge Gaussian Splatting for Pose-Free 3D Reconstruction
- **arXiv:** [2603.14684](https://arxiv.org/abs/2603.14684)

Neural Radiance Fields（NeRF）与 3D Gaussian Splatting（3DGS）的出现推动了 novel view synthesis（NVS）的发展。然而，这些方法需要高质量 RGB 输入及准确对应位姿，限制了在快速相机运动或不利光照等真实条件下的鲁棒性。Event camera 以高时间分辨率与宽动态范围捕获各像素亮度变化，可精确感知动态场景，提供有前景的解决方案。但现有 event-based NVS 方法要么假设已知位姿，要么依赖受初始观测约束的深度估计模型，在相机穿越此前未见区域时无法泛化。我们提出 E2EGS，一种仅基于 event stream 的无位姿框架。关键洞察是：边缘信息提供准确轨迹估计与高质量 NVS 所需的丰富结构线索。为从含噪 event stream 提取边缘，我们利用边缘与非边缘区域在时空上的显著差异：event camera 运动在边缘处引发一致 event，非边缘区域产生稀疏噪声。我们通过基于 patch 的 temporal coherence 分析测量局部方差以提取边缘并鲁棒抑制噪声。提取的边缘引导 structure-aware Gaussian 初始化，并在初始化、tracking 与 bundle adjustment 全程启用 edge-weighted 损失。在合成与真实数据集上的大量实验表明，E2EGS 在重建质量与轨迹精度上达到更优表现，确立了 event-based 3D 重建的完全无位姿范式。

---

<a id="paper-48"></a>
### [48] Zero-Shot Reconstruction of Animatable 3D Avatars with Cloth Dynamics from a Single Image
- **arXiv:** [2603.14772](https://arxiv.org/abs/2603.14772)

现有单图像 3D 人体 avatar 方法主要依赖刚性关节变换，限制了其建模真实 cloth dynamics 的能力。我们提出 DynaAvatar，一种 zero-shot 框架，从单张图像重建具有 motion-dependent cloth dynamics 的可动画 3D 人体 avatar。在大规模多人运动数据集上训练，DynaAvatar 采用基于 Transformer 的前馈架构，直接预测动态 3D Gaussian 形变，无需 subject-specific 优化。为克服动态捕获数据稀缺，我们引入 static-to-dynamic 知识迁移策略：在大规模静态捕获上预训练的 Transformer 提供强几何与外观先验，通过轻量 LoRA fine-tuning 在动态捕获上高效适配至 motion-dependent 形变。我们进一步提出 DynaFlow loss，一种 optical flow 引导目标，在渲染空间为 cloth dynamics 提供可靠的运动方向几何线索。最后，我们重新标注现有动态捕获数据集中缺失或含噪的 SMPL-X fittings，因多数公开动态捕获数据集含不完整或不可靠 fittings，不适合训练高质量 3D avatar 重建模型。实验表明，DynaAvatar 产生视觉丰富且可泛化的动画，优于先前方法。

---

<a id="paper-49"></a>
### [49] ProgressiveAvatars: Progressive Animatable 3D Gaussian Avatars
- **arXiv:** [2603.16447](https://arxiv.org/abs/2603.16447)

在实际实时 XR 与远程呈现应用中，网络与计算资源频繁波动，因此需要渐进式 3D 表示。为此，我们提出 ProgressiveAvatars，一种渐进式 avatar 表示，基于在模板网格上通过 adaptive implicit subdivision 生长的 3D Gaussian 层次结构构建。3D Gaussian 定义在 face-local 坐标中，以在不同细节层级下于不同表情与头部运动中保持可动画性。当屏幕空间信号表明细节不足时，层次结构扩展，向重要区域分配资源。利用 importance ranking，ProgressiveAvatars 支持增量加载与渲染，在新 Gaussian 到达时添加并保留先前内容，从而在不同带宽下实现平滑质量提升。ProgressiveAvatars 在波动网络带宽及变化的计算与内存资源下实现渐进式传输与渐进式渲染。

---

<a id="paper-50"></a>
### [50] Rethinking Pose Refinement in 3D Gaussian Splatting under Pose Prior and Geometric Uncertainty
- **arXiv:** [2603.16538](https://arxiv.org/abs/2603.16538)

3D Gaussian Splatting（3DGS）近期成为强大的场景表示，并日益用于视觉定位与位姿精化。然而，尽管其高质量可微渲染，基于 3DGS 的位姿精化鲁棒性对初始相机位姿与重建几何均高度敏感。本工作深入审视这些局限，识别两大不确定性来源：（i）位姿先验不确定性，常源于回归或检索模型输出单一确定性估计；（ii）几何不确定性，由 3DGS 重建缺陷引起，将误差传播至 PnP 求解器。此类不确定性可扭曲重投影几何并使优化失稳，即使渲染外观仍看似合理。为应对这些不确定性，我们引入重定位框架，结合 Monte Carlo 位姿采样与基于 Fisher Information 的 PnP 优化，显式考虑位姿与几何不确定性，无需重新训练或额外监督。在多样化室内外 benchmark 上，本方法持续提升定位精度，并在位姿与深度噪声下显著增强稳定性。

---

<a id="paper-51"></a>
### [51] CrowdGaussian: Reconstructing High-Fidelity 3D Gaussians for Human Crowd from a Single Image
- **arXiv:** [2603.17779](https://arxiv.org/abs/2603.17779)

单视角 3D 人体重建近年来备受关注。尽管进展众多，先前研究集中于从清晰、近距离的单人图像重建 3D 模型，在更常见的多人场景中常效果欠佳。重建 3D 人体人群模型是高度复杂的任务，面临诸多挑战：1）严重遮挡，2）低清晰度，3）数量众多且外观各异。为应对此任务，我们提出 CrowdGaussian，一种统一框架，直接从单图像输入重建多人 3D Gaussian Splatting（3DGS）表示。为处理遮挡，我们设计自监督适配流程，使预训练 large human model 能从严重遮挡输入重建具有合理几何与外观的完整 3D 人体。此外，我们引入 Self-Calibrated Learning（SCL），该训练策略使单步 diffusion model 通过融合身份保持样本与干净/损坏图像对，自适应地将粗糙渲染精化至最优质量，输出可蒸馏回以提升多人 3DGS 表示质量。大量实验表明，CrowdGaussian 生成照片级真实、几何一致的多人场景重建。

---

<a id="paper-52"></a>
### [52] OnlinePG: Online Open-Vocabulary Panoptic Mapping with 3D Gaussian Splatting
- **arXiv:** [2603.18510](https://arxiv.org/abs/2603.18510)

具身应用需感知并与环境交互，因此具有在线全景映射的开放词汇场景理解至关重要。然而，现有方法主要为离线或缺乏实例级理解，限制了其在真实机器人任务中的适用性。本文提出 OnlinePG，一种新颖有效的系统，在在线设定下利用 3D Gaussian Splatting 集成几何重建与开放词汇感知。技术上，为实现在线全景映射，我们采用带滑动窗口的高效 local-to-global 范式。为构建局部一致性地图，我们构建 3D segment clustering graph，联合利用几何与语义线索，将滑动窗口内不一致片段融合为完整实例。随后，为更新全局地图，我们为局部 3D Gaussian 地图构建带空间属性的显式网格，并通过鲁棒双向二分 3D Gaussian 实例匹配融合至全局地图。最后，我们利用 3D 空间属性网格内融合的 VLM 特征实现开放词汇场景理解。在广泛使用的数据集上的大量实验表明，本方法在在线方法中达到更优性能，同时保持实时效率。

---

<a id="paper-53"></a>
### [53] 3D Gaussian Splatting with Self-Constrained Priors for High Fidelity Surface Reconstruction
- **arXiv:** [2603.19682](https://arxiv.org/abs/2603.19682)

3D 表面渲染在辐射场建模中因 3DGS 或 NeRF 而革新。尽管 3DGS 在渲染质量或速度上相较 NeRF 具有优势，通过 3DGS 恢复高保真表面仍有改进空间。为解决此问题，我们提出 self-constrained prior 以约束 3D Gaussian 学习，目标为更准确的深度渲染。该先验源自 TSDF 网格，通过融合当前 3D Gaussian 渲染的深度图获得。先验在估计表面周围度量距离场，提供以表面为中心的带状区域，对 3D Gaussian 施加更具体的约束，如移除带外 Gaussian、将 Gaussian 移近表面，以及以几何感知方式鼓励更大或更小不透明度。更重要的是，先验可定期由通常更准确、更完整的最新深度图更新。此外，先验可逐步收窄带状区域以收紧约束。我们在广泛使用的 benchmark 上验证思路并报告相较最先进方法的优越性。

---

<a id="paper-54"></a>
### [54] GaussianPile: A Unified Sparse Gaussian Splatting Framework for Slice-based Volumetric Reconstruction
- **arXiv:** [2603.20611](https://arxiv.org/abs/2603.20611)

基于切片的体数据成像应用广泛，需要既能高效压缩又保留内部分析所需内部结构的表示。我们提出 GaussianPile，将 3D Gaussian splatting 与成像系统感知的 focus model 统一以应对此挑战。所提方法引入三项关键创新：（i）slice-aware piling 策略，定位各向异性 3D Gaussian 以建模跨切片贡献；（ii）可微投影算子，编码成像采集系统的有限厚度点扩散函数；（iii）紧凑编码与联合优化 pipeline，同时重建并压缩 Gaussian 集合。基于 CUDA 的设计保留 Gaussian 基元的压缩与实时渲染效率，同时保留高频内部体数据细节。在显微镜与超声数据集上的实验表明，本方法降低存储与重建成本，维持诊断保真度，并支持快速 2D 可视化及 3D 体素化。实践中，可在少至 3 分钟内交付高质量结果，较基于 NeRF 的方法快达 11 倍，相对体素网格实现一致 16 倍压缩，为基于切片的体数据集的部署级压缩与探索提供实用路径。

---

<a id="paper-55"></a>
### [55] Glove2Hand: Synthesizing Natural Hand-Object Interaction from Multi-Modal Sensing Gloves
- **arXiv:** [2603.20850](https://arxiv.org/abs/2603.20850)

理解 hand-object interaction（HOI）对计算机视觉、机器人与 AR/VR 至关重要。然而，常规手部视频常缺乏接触力、运动信号等关键物理信息，且易受频繁遮挡影响。为应对这些挑战，我们提出 Glove2Hand，一种框架，将多模态传感手套 HOI 视频翻译为照片级真实的裸手，同时忠实保留底层物理交互动力学。我们引入新颖 3D Gaussian 手部模型以确保时序渲染一致性。渲染手部通过基于 diffusion 的手部修复器无缝集成至场景，有效处理复杂手-物交互与非刚性形变。利用 Glove2Hand，我们创建 HandSense，首个多模态 HOI 数据集，含手套到裸手视频及同步触觉与 IMU 信号。我们证明 HandSense 显著增强下游裸手应用，包括基于视频的接触估计及严重遮挡下的手部跟踪。

---

<a id="paper-56"></a>
### [56] SGAD-SLAM: Splatting Gaussians at Adjusted Depth for Better Radiance Fields in RGBD SLAM
- **arXiv:** [2603.21055](https://arxiv.org/abs/2603.21055)

3D Gaussian Splatting（3DGS）在 RGBD SLAM 中取得显著进展。当前方法通常使用 3D Gaussian 或 view-tied 3D Gaussian 表示 tracking 与 mapping 中的辐射场。然而，这些 Gaussian 要么过于灵活要么运动受限，导致收敛缓慢或渲染质量受限。为解决此问题，我们采用 pixel-aligned Gaussian，但允许各 Gaussian 沿其射线调整位置以最大化渲染质量，即使为提升系统可扩展性而简化 Gaussian 亦然。为加速 tracking，我们将各像素周围深度分布建模为高斯分布，并利用这些分布快速将各帧对齐至 3D 场景。我们在广泛使用的 benchmark 上报告评估，论证设计并展示在视角渲染、相机跟踪、运行时间与存储复杂度上相较最新方法的优势。代码与视频见项目页面：https://machineperceptionlab.github.io/SGAD-SLAM-Project。

---

<a id="paper-57"></a>
### [57] EmoTaG: Emotion-Aware Talking Head Synthesis on Gaussian Splatting with Few-Shot Personalization
- **arXiv:** [2603.21332](https://arxiv.org/abs/2603.21332)

音频驱动的 3D talking head 合成随 Neural Radiance Fields（NeRF）与 3D Gaussian Splatting（3DGS）快速进展。借助丰富预训练先验，few-shot 方法可从仅数秒视频实现即时个性化。然而，在富有表现力的面部运动下，现有 few-shot 方法常受几何不稳定与音频-情感不匹配困扰，凸显更有效情感感知运动建模的需求。本工作提出 EmoTaG，一种基于 Pretrain-and-Adapt 范式的 few-shot 情感感知 3D talking head 合成框架。关键洞察是：在结构化 FLAME 参数空间而非直接形变 3D Gaussian 中重新表述运动预测，从而引入显式几何先验以改善运动稳定性。在此基础上，我们提出 Gated Residual Motion Network（GRMN），从音频捕获情感韵律，同时补充音频中缺失的头部姿态与上半脸线索，实现富有表现力且连贯的运动生成。大量实验表明，EmoTaG 在情感表现力、唇形同步、视觉真实感与运动稳定性上达到 state-of-the-art 性能。

---

<a id="paper-58"></a>
### [58] Cross-Instance Gaussian Splatting Registration via Geometry-Aware Feature-Guided Alignment
- **arXiv:** [2603.21936](https://arxiv.org/abs/2603.21936)

我们提出了 Gaussian Splatting Alignment（GSA），一种通过对相似变换（旋转、平移与缩放）对齐两个独立 3D Gaussian Splatting（3DGS）模型的新方法，即使它们属于同一类别中的不同物体（例如不同的汽车）也能完成对齐。相比之下，现有方法只能对齐同一物体的 3DGS 模型（例如同一辆汽车），且通常需要给定真实尺度作为输入，而 GSA 能够成功估计该尺度。GSA 利用视角引导的球面映射特征获得鲁棒对应关系，并引入两步优化框架，在对 3DGS 模型保持固定的同时进行对齐。首先，我们采用迭代式特征引导的绝对定向求解器作为粗配准步骤，对较差初始化（例如 180 度错位或 10 倍尺度差异）具有鲁棒性。随后，我们采用受逆辐射场公式启发的细配准步骤，以强化多视图特征一致性。第一步已可达到 state-of-the-art 性能，第二步可进一步提升结果。在相同物体情形下，GSA 优于先前工作，且往往具有显著优势，即使其他方法被给予真实尺度。在更困难的同类别不同物体情形下，GSA 大幅超越它们，为类别级 3DGS 配准提供了首个有效方案，并解锁了新的应用场景。项目网页：https://bgu-cs-vil.github.io/GSA-project/

---

<a id="paper-59"></a>
### [59] FreeArtGS: Articulated Gaussian Splatting Under Free-moving Scenario
- **arXiv:** [2603.22102](https://arxiv.org/abs/2603.22102)

增强现实与机器人领域日益增长的需求，推动了对可扩展关节物体重建的研究。然而，现有基于离散关节状态或随意单目视频进行重建的设置，要么需要非平凡的轴对齐，要么面临覆盖不足的问题，限制了其适用性。本文提出 FreeArtGS，一种在自由运动场景下重建关节物体的新方法；该设置具有简单采集配置且具备高可扩展性。FreeArtGS 将自由运动部件分割与关节估计及端到端优化相结合，仅以单目 RGB-D 视频作为输入。通过利用现成点跟踪与特征模型提供的先验进行优化，自由运动部件分割模块可在无约束采集条件下，从相对运动中识别刚性部件。关节估计模块校准统一的物体到相机位姿，并从部件分割中鲁棒恢复关节类型与轴。最后，采用基于 3DGS 的端到端优化，联合重建关节物体的视觉纹理、几何与关节角。我们在两个基准数据集及真实世界自由运动关节物体上开展实验。结果表明，FreeArtGS 在自由运动关节物体重建中 consistently 表现优异，并在先前重建设置中保持高度竞争力，证明其是面向真实资产生成的实用有效方案。项目页面：https://freeartgs.github.io/

---

<a id="paper-60"></a>
### [60] GaussFusion: Improving 3D Reconstruction in the Wild with A Geometry-Informed Video Generator
- **arXiv:** [2603.25053](https://arxiv.org/abs/2603.25053)

我们提出 GaussFusion，一种通过几何感知视频生成改进野外 3D Gaussian Splatting（3DGS）重建的新方法。GaussFusion 可缓解 3DGS 常见伪影，包括由相机位姿误差、覆盖不完整及噪声几何初始化引起的浮点、闪烁与模糊。与局限于单一重建管线的先前 RGB 方法不同，本文引入几何感知 video-to-video 生成器，对基于优化与 feed-forward 两类方法的 3DGS 渲染结果进行 refinement。给定已有重建结果，我们渲染编码深度、法线、不透明度与协方差的 Gaussian 基元视频缓冲，生成器对其进行 refinement 以产生时序一致、无伪影的帧。我们进一步引入伪影合成管线，模拟多样化退化模式，以确保鲁棒性与泛化能力。GaussFusion 在新视角合成 benchmark 上达到 state-of-the-art 性能；其高效变体以 15 FPS 实时运行且保持相近性能，从而支持交互式 3D 应用。

---

<a id="paper-61"></a>
### [61] Learning Explicit Continuous Motion Representation for Dynamic Gaussian Splatting from Monocular Videos
- **arXiv:** [2603.25058](https://arxiv.org/abs/2603.25058)

我们提出一种从单目视频实现高质量 dynamic Gaussian Splatting 的方法。为此，本文在先前方法基础上进一步显式建模动态 Gaussian 的连续位置与朝向形变，采用带紧凑控制点集的 SE(3) B-spline motion bases。为在提升复杂运动建模能力的同时提高计算效率，我们设计自适应控制机制，动态调整 motion bases 与控制点数量。此外，我们开发 soft segment reconstruction 策略以缓解长间隔运动干扰，并采用 multi-view diffusion model 提供多视图线索，避免对训练视角过拟合。大量实验表明，本文方法在新视角合成上优于 state-of-the-art 方法。代码见 https://github.com/hhhddddddd/se3bsplinegs。

---

<a id="paper-62"></a>
### [62] GLINT: Modeling Scene-Scale Transparency via Gaussian Radiance Transport
- **arXiv:** [2603.26181](https://arxiv.org/abs/2603.26181)

尽管 3D Gaussian Splatting 已成为强大范式，其本质上无法建模玻璃面板等透明体。核心挑战在于解耦透明界面与透过玻璃观察到的透射几何所交织的辐射贡献。我们提出 GLINT，一种通过显式分解 Gaussian 表示建模场景级透明性的框架。GLINT 重建主界面并分别建模反射与透射辐射，从而实现一致的 radiance transport。在优化过程中，GLINT 结合分解所诱导的几何分离线索，以及来自预训练 video relighting model 的几何与材质先验，引导透明区域定位。大量实验表明，GLINT 在复杂透明场景重建上 consistently 优于先前方法。

---

<a id="paper-63"></a>
### [63] Scene Grounding In the Wild
- **arXiv:** [2603.26584](https://arxiv.org/abs/2603.26584)

从无结构、野外采集 imagery 重建大规模真实场景准确 3D 模型，仍是计算机视觉核心挑战，尤其当输入视角几乎无重叠时更是如此。在此类情况下，现有重建管线常产生多个互不连接的局部重建，或错误地将非重叠区域合并为重叠几何。本文提出一种框架，将每个局部重建锚定（ground）到完整场景参考模型，从而在无视觉重叠时仍实现全局一致对齐。参考模型来自 Google Earth Studio 导出的稠密、地理空间准确的伪合成渲染，这些渲染提供完整场景覆盖，但外观与真实照片差异显著。我们的关键洞察是：尽管存在显著 domain gap，两域共享相同底层场景语义。我们以 3D Gaussian Splatting 表示参考模型，为每个 Gaussian 增强语义特征，并将对齐表述为基于特征的逆优化方案，在固定参考模型条件下估计全局 6DoF 位姿与尺度。此外，我们引入 WikiEarth 数据集，将现有局部 3D 重建与伪合成参考模型配准。实验表明，当以多种经典与学习式管线初始化时，本文方法 consistently 改善全局对齐，并缓解 state-of-the-art 端到端模型的失败模式。

---

<a id="paper-64"></a>
### [64] Unblur-SLAM: Dense Neural SLAM for Blurry Inputs
- **arXiv:** [2603.26810](https://arxiv.org/abs/2603.26810)

我们提出 Unblur-SLAM，一种面向模糊图像输入、实现清晰 3D 重建的新型 RGB SLAM 管线。与先前工作不同，本文方法可处理不同类型模糊，并在 motion blur 与 defocus blur 同时存在时展现 state-of-the-art 性能。此外，我们根据输入图像模糊程度自适应调整计算开销。第一阶段，方法采用 feed-forward 图像去模糊模型；我们提出合适训练方案，可同时提升 tracking 与 mapping 模块。经 feed-forward 网络成功去模糊的帧，通过 local-global multi-view optimization 与 loop closure 获得 refined 位姿与深度。第一阶段去模糊失败的帧，则直接通过全局 3DGS 表示及额外 blur network 建模，该网络建模多个模糊子帧并在 3D 空间中模拟 blur formation 过程，从而学习清晰细节并 refined 子帧位姿。在多个真实数据集上的实验表明，本文方法在位姿估计以及几何与纹理的清晰重建结果上 consistently 取得改进。

---

<a id="paper-65"></a>
### [65] NimbusGS: Unified 3D Scene Reconstruction under Hybrid Weather
- **arXiv:** [2603.27228](https://arxiv.org/abs/2603.27228)

我们提出 NimbusGS，一种统一框架，用于从在多样且混合恶劣天气条件下采集的退化多视图输入重建高质量 3D 场景。与针对特定天气类型的现有方法不同，NimbusGS 通过建模天气的双重性质来应对更广泛的泛化挑战：其一是连续、视角一致、衰减光线的介质；其二是动态、视角相关、引起散射与遮挡的粒子。为刻画该结构，我们将退化分解为全局 transmission field 与逐视图 particulate residuals。transmission field 表示跨视图共享的静态大气效应，residuals 则建模各输入独有的瞬态扰动。为在严重可见性退化下实现稳定几何学习，我们引入 geometry-guided gradient scaling 机制，缓解 3D Gaussian 表示自监督优化中的梯度失衡。该物理 grounded 公式使 NimbusGS 能够解耦复杂退化并保留场景结构，在几何重建上取得 superior 结果，并在多样且具有挑战性的天气条件下 outperform 任务特定方法。代码见 https://github.com/lyy-ovo/NimbusGS。

---

<a id="paper-66"></a>
### [66] SGS-Intrinsic: Semantic-Invariant Gaussian Splatting for Sparse-View Indoor Inverse Rendering
- **arXiv:** [2603.27516](https://arxiv.org/abs/2603.27516)

我们提出 SGS-Intrinsic，一种适用于稀疏视角室内图像的 inverse rendering 框架。与聚焦 object-centric 重建且在稀疏视角设置下失效的现有 3D Gaussian Splatting（3DGS）方法不同，本文方法可实现高质量几何重建及材质与光照的准确解耦。核心思想是：在语义与几何先验引导下构建稠密且几何一致的 Gaussian semantic field，为后续 inverse rendering 提供可靠基础。在此基础上，我们结合 hybrid illumination model 与 material prior 执行材质-光照解耦，有效捕获光照-材质交互。为缓解 cast shadows 影响并增强材质恢复鲁棒性，我们引入 illumination-invariant material constraint 及 deshadowing model。在 benchmark 数据集上的大量实验表明，本文方法 consistently 在重建保真度与 inverse rendering 质量上优于现有 3DGS-based inverse rendering 方法。代码见 https://github.com/GrumpySloths/SGS_Intrinsic.github.io。

---

<a id="paper-67"></a>
### [67] Physically Inspired Gaussian Splatting for HDR Novel View Synthesis
- **arXiv:** [2603.28020](https://arxiv.org/abs/2603.28020)

High dynamic range novel view synthesis（HDR-NVS）通过融合多曝光 low dynamic range（LDR）视图重建具有动态细节的场景，但难以捕获依赖 ambient illumination 的外观。通过约束 tone-mapped 结果隐式监督 HDR 内容，无法纠正异常 HDR 值，并导致 under/over-exposed 区域中 Gaussian 梯度受限。为此，我们引入 PhysHDR-GS，一种 physically inspired 的 HDR-NVS 框架，通过 intrinsic reflectance 与可调 ambient illumination 建模场景外观。PhysHDR-GS 采用互补的 image-exposure（IE）分支与 Gaussian-illumination（GI）分支，分别忠实复现标准相机观测并捕获依赖光照的外观变化。训练过程中，提出的 cross-branch HDR consistency loss 为 HDR 内容提供显式监督，而 illumination-guided gradient scaling 策略缓解 exposure-biased gradient starvation 并减少 under-densified 表示。在真实与合成数据集上的实验结果表明，本文方法在重建 HDR 细节方面具有 superior 性能（例如相较 HDR-GS 的 PSNR 提升 2.04 dB），同时保持实时渲染速度（最高 76 FPS）。代码与模型见 https://huimin-zeng.github.io/PhysHDR-GS/。

---

<a id="paper-68"></a>
### [68] 4DSurf: High-Fidelity Dynamic Scene Surface Reconstruction
- **arXiv:** [2603.28064](https://arxiv.org/abs/2603.28064)

本文研究基于 Gaussian Splatting（GS）的动态场景 surface reconstruction 问题，旨在恢复时序一致几何。现有 GS-based 动态 surface reconstruction 方法虽可取得 superior 重建，但通常局限于单个物体或仅小幅形变物体，难以在长时间跨度内维持大幅形变 surface 的时序一致重建。我们提出 *4DSurf*，一种用于通用动态 surface reconstruction 的新颖统一框架：无需指定场景中物体数量或类型，可处理大幅 surface 形变及重建中的时序不一致。框架的关键创新是引入 Gaussian deformations induced Signed Distance Function Flow Regularization，约束 Gaussian 运动与演化 surface 对齐。为处理大幅形变，我们引入 Overlapping Segment Partitioning 策略，将序列划分为具有小幅形变的重叠片段，并通过共享重叠时间步在片段间增量传递几何信息。在 Hi4D 与 CMU Panoptic 两个具有挑战性的动态场景数据集上的实验表明，本文方法在 Chamfer distance 上分别优于 state-of-the-art surface reconstruction 方法 49% 与 19%，并在 sparse-view 设置下实现 superior 时序一致性。

---

<a id="paper-69"></a>
### [69] Hierarchical Visual Relocalization with Nearest View Synthesis from Feature Gaussian Splatting
- **arXiv:** [2603.29185](https://arxiv.org/abs/2603.29185)

Visual relocalization 是 3D 计算机视觉基础任务，用于在相机重访已知场景时估计其位姿。尽管基于点的 hierarchical relocalization 方法展现出强可扩展性与高效率，但常受限于稀疏图像观测与弱 feature matching。本文提出 SplatHLoc，一种以 Feature Gaussian Splatting 作为场景表示的 hierarchical visual relocalization 框架。为应对 database 图像稀疏性，我们提出 adaptive viewpoint retrieval 方法，合成与 query 视角更对齐的 virtual candidates，从而提升初始位姿估计精度。对于 feature matching，我们观察到 Gaussian-rendered features 与直接从图像提取的特征在两阶段匹配过程中各有优势：前者在 coarse 阶段表现更好，后者在 fine 阶段更有效。因此，我们引入 hybrid feature matching 策略，实现更准确且高效的位姿估计。在室内与室外数据集上的大量实验表明，SplatHLoc 增强 visual relocalization 鲁棒性，并建立新的 state-of-the-art。

---

<a id="paper-70"></a>
### [70] MotionScale: Reconstructing Appearance, Geometry, and Motion of Dynamic Scenes with Scalable 4D Gaussian Splatting
- **arXiv:** [2603.29296](https://arxiv.org/abs/2603.29296)

从单目视频真实重建动态 4D 场景，对理解物理世界至关重要。尽管 neural rendering 近期取得进展，现有方法仍常难以在复杂环境中恢复准确 3D 几何与时序一致运动。为应对这些挑战，我们提出 MotionScale，一种 4D Gaussian Splatting 框架，可高效扩展至大场景与长序列，同时保持高保真结构与运动一致性。方法核心是可扩展 motion field，由 cluster-centric basis transformations 参数化，可自适应扩展以捕获多样且演化的运动模式。为确保长时长鲁棒重建，我们引入 progressive optimization 策略，包含两个解耦传播阶段：1）background extension 阶段，适应新可见区域、refined 相机位姿，并显式建模 transient shadows；2）foreground propagation 阶段，通过 specialized three-stage refinement 过程强化 motion consistency。在具有挑战性的真实 benchmark 上的大量实验表明，MotionScale 在重建质量与时序稳定性上显著优于 state-of-the-art 方法。项目页面：https://hrzhou2.github.io/motion-scale-web/。

---

<a id="paper-71"></a>
### [71] GRVS: a Generalizable and Recurrent Approach to Monocular Dynamic View Synthesis
- **arXiv:** [2603.29734](https://arxiv.org/abs/2603.29734)

从动态场景单目视频合成新视角仍是具有挑战性的问题。采用显式 motion priors 优化 4D 表示的 scene-specific 方法，常在高度动态区域失效，因为难以利用 multi-view 信息。将 camera control 集成到大型预训练模型中的 diffusion-based 方法可产生视觉 plausible 视频，但常在静态与动态区域均出现几何不一致。两类方法亦需大量计算资源。基于 static novel view synthesis 中 generalizable models 的成功，我们将该框架适配至动态输入，并提出包含两个关键组件的新模型：（1）recurrent loop，实现 input 与 target 视频之间无界且异步的 mapping；（2）对动态输入高效使用 plane sweeps，以解耦 camera 与 scene motion，并实现细粒度 six-degrees-of-freedom camera controls。我们在 UCSD 数据集及 Kubric-4D-dyn 上训练与评估模型；后者是新的 monocular dynamic 数据集，具有更长、更高分辨率序列及比现有替代方案更复杂的 scene dynamics。我们的模型在静态与动态区域 fine-grained 几何细节重建上，优于四种 Gaussian Splatting-based scene-specific 方法及两种 diffusion-based 方法。

---

<a id="paper-72"></a>
### [72] DirectFisheye-GS: Enabling Native Fisheye Input in Gaussian Splatting with Cross-View Joint Optimization
- **arXiv:** [2604.00648](https://arxiv.org/abs/2604.00648)

3D Gaussian Splatting（3DGS）已支持从日常图像高效重建 3D 场景并实现实时高保真渲染，极大推进 VR/AR 应用。Fisheye 相机凭借更宽 field of view（FOV），有望以更少输入实现高质量重建，近期受到广泛关注。然而，由于 3DGS 依赖 rasterization，多数涉及 fisheye 输入的后续工作会先 undistort 图像再训练，这带来两个问题：1）图像边缘 black borders 导致信息丢失，抵消 fisheye 大 FOV 优势；2）undistortion 的 stretch-and-interpolate 重采样将每个像素值扩散至更大区域，稀释 detail density——导致 3DGS 过拟合这些 low-frequency 区域，产生 blur 与 floating artifacts。本文将 fisheye camera model 集成至原始 3DGS 框架，支持 native fisheye 图像输入训练而无需预处理。尽管建模正确，我们仍观察到重建场景在图像边缘出现 floaters：畸变向 periphery 增大，而 3DGS 原始 per-iteration random-selecting-view 优化忽略 Gaussian 的 cross-view correlations，导致极端形状（如 oversized 或 elongated），降低重建质量。为此，我们引入 feature-overlap-driven cross-view joint optimization 策略，在跨视图间建立一致几何与 photometric constraints——该技术同样适用于现有 pinhole-camera-based 管线。DirectFisheye-GS 在公开数据集上达到或超越 state-of-the-art 性能。项目页面：https://yzxqh.github.io/DirectFisheye-GS/。

---

<a id="paper-73"></a>
### [73] DLWM: Dual Latent World Models enable Holistic Gaussian-centric Pre-training in Autonomous Driving
- **arXiv:** [2604.00969](https://arxiv.org/abs/2604.00969)

基于视觉的 autonomous driving 因低成本与优异性能受到广泛关注。与稠密 BEV（Bird's Eye View）或 sparse query 模型相比，Gaussian-centric 方法通过 3D semantic Gaussians 描述场景，是一种 comprehensive 且 sparse 的表示。本文提出 DLWM，一种专为 autonomous driving 中 holistic gaussian-centric pre-training 设计的 Dual Latent World Models 新范式，包含两个阶段。第一阶段，DLWM 通过 self-supervised 重建 multi-view semantic 与 depth 图像，从 queries 预测 3D Gaussians。第二阶段在 fine-grained contextual features 支持下，分别训练两个 latent world models 进行 temporal feature learning：包括 Gaussian-flow-guided latent prediction（用于下游 occupancy perception 与 forecasting 任务），以及 ego-planning-guided latent prediction（用于 motion planning）。在 SurroundOcc 与 nuScenes benchmark 上的大量实验表明，DLWM 在 Gaussian-centric 3D occupancy perception、4D occupancy forecasting 与 motion planning 任务上均取得显著性能提升。

---

<a id="paper-74"></a>
### [74] F3DGS: Federated 3D Gaussian Splatting for Decentralized Multi-Agent World Modeling
- **arXiv:** [2604.01605](https://arxiv.org/abs/2604.01605)

我们提出 F3DGS，一种面向 decentralized multi-agent 3D 重建的 federated 3D Gaussian Splatting 框架。现有 3DGS 管线假设可 centralized 访问全部观测，限制了其在 distributed robotic 设置中的适用性——各 agent 独立运行，且 centralized 数据聚合可能受限。将 centralized 训练直接扩展至多 agent 系统会引入通信开销与几何不一致。F3DGS 首先通过将多个 client 局部合并的 LiDAR 点云配准，构建 shared geometric scaffold 以初始化 global 3DGS 模型。在 federated optimization 过程中，Gaussian positions 被固定以 preserve 几何对齐，各 client 仅更新 appearance-related attributes，包括 covariance、opacity 与 spherical harmonic coefficients。server 采用 visibility-aware aggregation 聚合这些更新，按各 client 观测每个 Gaussian 的频率加权其贡献，从而解决 multi-agent exploration 固有的 partial-observability 挑战。为评估 decentralized reconstruction，我们采集包含同步 LiDAR、RGB 与 IMU 测量的 multi-sequence indoor 数据集。实验表明，F3DGS 在重建质量上 comparable 于 centralized training，同时支持跨 agent 的 distributed optimization。数据集、development kit 与源代码将公开发布。

---

<a id="paper-75"></a>
### [75] ProDiG: Progressive Diffusion-Guided Gaussian Splatting for Aerial to Ground Reconstruction
- **arXiv:** [2604.02003](https://arxiv.org/abs/2604.02003)

从仅含 aerial imagery 生成 ground-level 视图与 coherent 3D site models 具有挑战性，原因包括极端 viewpoint 变化、缺失 intermediate observations 及大尺度变化。现有方法要么 post-hoc refined 渲染结果，常产生几何不一致；要么依赖 multi-altitude ground-truth，而这类数据 rarely 可得。Gaussian Splatting 与 diffusion-based refinements 在小变化下可提升 fidelity，但在 wide aerial-to-ground gaps 下失效。为应对这些局限，我们引入 ProDiG（Progressive Diffusion-Guided Gaussian Splatting for Aerial to Ground Reconstruction），一种 diffusion-guided 框架，将 aerial 3D 表示 progressive 变换至 ground-level fidelity。ProDiG 合成 intermediate-altitude 视图，并在各阶段利用 geometry-aware causal attention module refined Gaussian 表示；该模块将 epipolar structure 注入 reference-view diffusion。distance-adaptive Gaussian module 根据 camera distance 动态调整 Gaussian scale 与 opacity，确保在大 viewpoint gaps 下稳定重建。这些组件共同实现 progressive、几何 grounded 的 refinement，而无需额外 ground-truth viewpoints。在 synthetic 与 real-world 数据集上的大量实验表明，ProDiG 产生视觉 realistic 的 ground-level 渲染与 coherent 3D 几何，在 visual quality、geometric consistency 及对 extreme viewpoint changes 的鲁棒性上显著优于现有方法。项目页面：https://sirsh07.github.io/research/prodig

---

<a id="paper-76"></a>
### [76] GP-4DGS: Probabilistic 4D Gaussian Splatting from Monocular Video via Variational Gaussian Processes
- **arXiv:** [2604.02915](https://arxiv.org/abs/2604.02915)

我们提出 GP-4DGS，一种将 Gaussian Processes（GPs）集成至 4D Gaussian Splatting（4DGS）的新框架，用于动态场景的 principled probabilistic modeling。现有 4DGS 方法聚焦 deterministic reconstruction，本质上难以捕获 motion ambiguity，且缺乏评估 prediction reliability 的机制。通过利用 GPs 基于 kernel 的 probabilistic 性质，本文方法引入三项关键能力：（i）对 motion predictions 的 uncertainty quantification；（ii）对 unobserved 或 sparsely sampled 区域的 motion estimation；（iii）超出已观测训练帧的 temporal extrapolation。为将 GPs 扩展至 4DGS 中大量 Gaussian primitives，我们设计 spatio-temporal kernels 以捕获 deformation fields 的相关结构，并采用带 inducing points 的 variational Gaussian Processes 实现 tractable inference。实验表明，GP-4DGS 在提升 reconstruction quality 的同时，提供可靠 uncertainty estimates，可有效识别高 motion ambiguity 区域。通过应对这些挑战，本文工作向 bridging probabilistic modeling 与 neural graphics 迈出有意义一步。

---

<a id="paper-77"></a>
### [77] SparseSplat: Towards Applicable Feed-Forward 3D Gaussian Splatting with Pixel-Unaligned Prediction
- **arXiv:** [2604.03069](https://arxiv.org/abs/2604.03069)

前馈式 3D Gaussian Splatting（3DGS）的最新进展显著提升了渲染质量。然而，先前前馈式 3DGS 方法生成的空间均匀且高度冗余的 3DGS 地图限制了其在下游重建任务中的集成应用。我们提出 SparseSplat，这是首个能够根据场景结构和局部区域信息丰富程度自适应调整 Gaussian 密度的前馈式 3DGS 模型，从而生成高度紧凑的 3DGS 地图。为实现这一目标，我们提出基于熵的概率采样策略，在无纹理区域生成大型稀疏 Gaussians，并将小型密集 Gaussians 分配至信息丰富的区域。此外，我们设计了一种专用点云网络，能够高效编码局部上下文并将其解码为 3DGS 属性，从而解决通用 3DGS 优化流程与前馈模型之间的感受野不匹配问题。大量实验结果表明，SparseSplat 仅使用 22% 的 Gaussians 即可达到最先进的渲染质量，且仅使用 1.5% 的 Gaussians 仍能维持合理的渲染质量。项目主页：https://victkk.github.io/SparseSplat-page/。

---

<a id="paper-78"></a>
### [78] CGHair: Compact Gaussian Hair Reconstruction with Card Clustering
- **arXiv:** [2604.03716](https://arxiv.org/abs/2604.03716)

我们提出一种紧凑的流水线，用于从多视角图像进行高保真头发重建。尽管近期的 3D Gaussian Splatting（3DGS）方法能够取得逼真的效果，但它们通常需要数百万个基元，导致存储和渲染成本高昂。我们观察到，同一发型中的发丝在结构和视觉上具有相似性，因此将发丝聚类为代表性头发卡片（hair cards），并将这些卡片分组到共享纹理码本中。我们的方法将这一结构与 3DGS 渲染相结合，在保持相当视觉质量的同时，显著降低了重建时间和存储开销。此外，我们提出一种生成式先验加速方法，从一组图像重建初始发丝几何。实验表明，该方法将发丝重建时间降低了 4 倍，并以超过 200 倍的更低内存占用实现了可比的渲染性能。

---

<a id="paper-79"></a>
### [79] 4C4D: 4 Camera 4D Gaussian Splatting
- **arXiv:** [2604.04063](https://arxiv.org/abs/2604.04063)

本文解决从仅四台便携相机拍摄的视频中恢复 4D 动态场景的挑战。学习场景动态以实现时间一致的新视角渲染是计算机图形学中的一项基础任务，而先前工作通常需要借助数十甚至上百个视角的密集多视角采集。我们提出 4C4D，一种新颖框架，能够从极度稀疏相机拍摄的视频中实现高保真 4D Gaussian Splatting。我们的核心洞察在于：在稀疏设置下，几何学习远比外观建模困难。基于这一观察，我们在 Gaussian 不透明度上引入 Neural Decaying Function，以增强 4D Gaussians 的几何建模能力。该设计通过促使 4DGS 梯度更多聚焦于几何学习，缓解了 4DGS 中几何与外观建模之间的固有失衡。在具有不同相机重叠度的稀疏视角数据集上的大量实验表明，4C4D 优于现有方法。项目主页：https://junshengzhou.github.io/4C4D。

---

<a id="paper-80"></a>
### [80] PR-IQA: Partial-Reference Image Quality Assessment for Diffusion-Based Novel View Synthesis
- **arXiv:** [2604.04576](https://arxiv.org/abs/2604.04576)

扩散模型在稀疏视角新视角合成（NVS）中展现出良好前景，因其能够生成伪真值视角以辅助 3D Gaussian Splatting（3DGS）等 3D 重建流水线。然而，这些合成图像常包含光度与几何不一致性，直接用于监督会损害重建效果。为此，我们提出 Partial-Reference Image Quality Assessment（PR-IQA），一种利用不同姿态参考图像评估扩散生成视角的框架，无需真值标注。PR-IQA 首先在重叠区域计算几何一致的部分质量图，随后通过质量补全将该部分图修复为稠密的全图质量图。该补全过程通过交叉注意力机制融入参考视角上下文，确保跨视角一致性并实现全面质量评估。当集成至扩散增强的 3DGS 流水线时，PR-IQA 将监督限制在其质量图识别的高置信度区域。实验表明，PR-IQA 优于现有 IQA 方法，在无真值监督的情况下达到全参考级别的精度。因此，我们的质量感知 3DGS 方法能更有效地过滤不一致性，产生更优的 3D 重建与 NVS 结果。项目主页：https://kakaomacao.github.io/pr-iqa-project-page/。

---

<a id="paper-81"></a>
### [81] AvatarPointillist: AutoRegressive 4D Gaussian Avatarization
- **arXiv:** [2604.04787](https://arxiv.org/abs/2604.04787)

我们提出 AvatarPointillist，一种从单张肖像图像生成动态 4D Gaussian 化身的新颖框架。该方法的核心是一个仅解码器 Transformer，以自回归方式生成用于 3D Gaussian Splatting 的点云。这种序列化方法支持精确、自适应的构建，根据主体复杂度动态调整点密度和总点数。在点生成过程中，AR 模型还联合预测逐点绑定信息，以实现逼真的动画。生成完成后，专用 Gaussian 解码器将点转换为完整、可渲染的 Gaussian 属性。我们证明，在解码器上以 AR 生成器的潜在特征为条件，可实现阶段间有效交互并显著提升保真度。大量实验验证了 AvatarPointillist 能够生成高质量、照片级真实且可控的化身。我们认为这种自回归建模方式代表了化身生成的新范式，并将发布代码以启发后续研究。

---

<a id="paper-82"></a>
### [82] Indoor Asset Detection in Large Scale 360° Drone-Captured Imagery via 3D Gaussian Splatting
- **arXiv:** [2604.05316](https://arxiv.org/abs/2604.05316)

我们提出一种方法，用于在由 360° 无人机采集图像重建的 3D Gaussian Splatting（3DGS）场景中进行目标级室内资产检测与分割。我们引入 3D 物体码本，联合利用掩码语义及其对应 Gaussian 基元的空间信息，以指导多视角掩码关联和室内资产检测。通过将 2D 物体检测与分割模型与语义及空间约束的合并流程相结合，我们的方法将多视角掩码聚合为连贯的 3D 物体实例。在两个大型室内场景上的实验表明，该方法实现了可靠的多视角掩码一致性，F1 分数较最先进基线提升 65%，并在物体级 3D 室内资产检测上取得 11% 的 mAP 增益。

---

<a id="paper-83"></a>
### [83] In Depth We Trust: Reliable Monocular Depth Supervision for Gaussian Splatting
- **arXiv:** [2604.05715](https://arxiv.org/abs/2604.05715)

在 3D Gaussian Splatting 中使用准确的深度先验有助于缓解稀疏训练数据和无纹理表面引起的伪影。然而，获取准确深度图需要专用采集系统。基础单目深度估计模型提供了更具成本效益的替代方案，但存在尺度歧义、多视角不一致和局部几何不准确等问题，若直接使用会损害渲染性能。本文解决如何可靠地利用单目深度先验增强 Gaussian Splatting（GS）渲染的问题。为此，我们引入一种训练框架，将尺度歧义和含噪深度先验整合进几何监督。我们强调从弱对齐深度变化中学习的重要性，并提出一种方法隔离不适定几何以进行选择性单目深度正则化，限制深度不准确向已良好重建的 3D 结构传播。在多种数据集上的大量实验显示，几何精度持续提升，在不同 GS 变体和单目深度骨干网络上均实现了更忠实的深度估计和更高的渲染质量。

---

<a id="paper-84"></a>
### [84] GaussianGrow: Geometry-aware Gaussian Growing from 3D Point Clouds with Text Guidance
- **arXiv:** [2604.05721](https://arxiv.org/abs/2604.05721)

3D Gaussian Splatting 在渲染效率和质量上表现优异，但在缺乏合适几何先验的情况下，3D Gaussians 的生成仍具挑战。现有方法探索将点图预测作为推断 Gaussian 基元的几何参考，但不可靠的估计几何可能导致生成质量不佳。本文提出 GaussianGrow，一种通过学习从易于获取的 3D 点云生长 3D Gaussians 的新方法，自然地在 Gaussian 生成中强制几何精度。具体而言，我们设计文本引导的 Gaussian 生长方案，利用多视角扩散模型从输入点云合成一致外观以进行监督。为缓解融合相邻视角引起的伪影，我们在不同视角重叠区域中识别出的非预设相机姿态处约束生成的新视角。对于难以观测区域的补全，我们提出迭代检测相机姿态——通过观察点云中最大未生长区域，并使用预训练 2D 扩散模型修复渲染视角——直至生成完整的 Gaussians。我们在合成乃至真实扫描点云的文本引导 Gaussian 生成任务上对 GaussianGrow 进行了广泛评估。项目主页：https://weiqi-zhang.github.io/GaussianGrow。

---

<a id="paper-85"></a>
### [85] PhysHead: Simulation-Ready Gaussian Head Avatars
- **arXiv:** [2604.06467](https://arxiv.org/abs/2604.06467)

逼真的数字化身需要富有表现力且动态的头发运动；然而，大多数现有头部化身方法假设头发为刚性运动。这些方法往往难以将头发与头部解耦，将其表示为简单外壳，无法捕捉其自然体积行为。本文通过引入 PhysHead 解决上述局限，这是一种混合表示，用于从多视角视频学习具有逼真头发动力学的可动画头部化身。其核心是基于 3D Gaussian 的分层头部表示。我们的方法将 3D 参数化网格用于头部，将基于发丝的头发与物理引擎直接仿真相结合。在外观模型方面，我们将 Gaussian 基元附着于头部网格和发丝段。该表示能够创建具有动态头发行为（如风吹效果）的照片级真实头部化身，克服现有方法中头发刚性的限制。然而，这些动画能力也需要新的训练方案。特别是，我们提出使用基于 VLM 的模型生成动态训练序列中被遮挡区域的外观。在定量与定性研究中，我们展示了所提模型的能力并与现有基线进行比较。我们证明，除表情和相机控制外，该方法还能合成物理上合理的头发运动。

---

<a id="paper-86"></a>
### [86] AnchorSplat: Feed-Forward 3D Gaussian Splatting with 3D Geometric Priors
- **arXiv:** [2604.07053](https://arxiv.org/abs/2604.07053)

近期前馈式 Gaussian 重建模型采用像素对齐建模方式，将每个 2D 像素映射到一个 3D Gaussian，使 Gaussian 表示与输入图像紧密耦合。本文提出 AnchorSplat，一种用于场景级重建的新型前馈 3DGS 框架，直接在 3D 空间中表示场景。AnchorSplat 引入由 3D 几何先验（如稀疏点云、体素或 RGB-D 点云）引导的锚点对齐 Gaussian 表示，实现更几何感知的可渲染 3D Gaussians，且独立于图像分辨率和视角数量。该设计显著减少所需 Gaussians 数量，在提升重建保真度的同时提高计算效率。除锚点对齐设计外，我们利用 Gaussian Refiner 通过少量前向传播调整中间 Gaussians。在 ScanNet++ v2 NVS 基准上的实验展示了 SOTA 性能，以更少 Gaussian 基元实现了更视角一致的结果，优于先前方法。

---

<a id="paper-87"></a>
### [87] GEAR: GEometry-motion Alternating Refinement for Articulated Object Modeling with Gaussian Splatting
- **arXiv:** [2604.07728](https://arxiv.org/abs/2604.07728)

高保真交互式数字资产对具身智能和机器人交互至关重要，但关节物体因其复杂结构和几何-运动耦合关系而难以重建。现有方法在几何-运动联合优化中不稳定，且在复杂多关节或分布外物体上泛化能力有限。为应对这些挑战，我们提出 GEAR，一种 EM 风格的交替优化框架，在 Gaussian Splatting 表示内将几何与运动作为相互依赖的组件进行联合建模。GEAR 将部件分割视为隐变量、关节运动参数视为显式变量，交替优化以提升收敛性和几何-运动一致性。为在不牺牲泛化能力的前提下提升部件分割质量，我们利用 vanilla 2D 分割模型提供多视角部件先验，并采用弱监督约束正则化隐变量。在多个基准和我们新构建的数据集 GEAR-Multi 上的实验表明，GEAR 在几何重建和运动参数估计上达到 SOTA 结果，尤其在具有多个可动部件的复杂关节物体上表现突出。

---

<a id="paper-88"></a>
### [88] F3G-Avatar : Face Focused Full-body Gaussian Avatar
- **arXiv:** [2604.09835](https://arxiv.org/abs/2604.09835)

现有全身 Gaussian 化身方法主要优化全局重建质量，往往难以保留细粒度面部几何和表情细节。这一挑战源于有限的面部表示能力，导致难以建模高频姿态相关形变。为此，我们提出 F3G-Avatar，一种全身、面部感知的化身合成方法，从多视角 RGB 视频和回归的姿态/形状参数重建可动画人体表示。该方法从穿衣 Momentum Human Rig（MHR）模板出发，渲染前/后位置图并通过双分支架构解码为 3D Gaussians：身体分支捕获姿态相关非刚性形变，面部聚焦形变分支细化头部几何和外观。预测的 Gaussians 经融合后，通过线性混合蒙皮（LBS）进行姿态变换，并使用可微 Gaussian splatting 渲染。训练结合重建与感知目标以及面部特定对抗损失，以提升特写视角的真实感。实验展示了强渲染质量，在 AvatarReX 数据集上面部视角达到 PSNR/SSIM/LPIPS 为 26.243/0.964/0.084。消融实验进一步突出了 MHR 模板和面部聚焦形变的贡献。F3G-Avatar 为逼真、可动画的全身化身合成提供了实用且高质量的流水线。

---

<a id="paper-89"></a>
### [89] PointSplat: Efficient Geometry-Driven Pruning and Transformer Refinement for 3D Gaussian Splatting
- **arXiv:** [2604.09903](https://arxiv.org/abs/2604.09903)

3D Gaussian Splatting（3DGS）近期通过显式 3D 基元表示场景，实现了实时、高保真的新视角合成。然而，传统方法往往需要数百万 Gaussians 才能捕捉复杂场景，导致显著的内存和存储需求。近期方法通过剪枝和逐场景 Gaussian 参数微调来解决该问题，在保持视觉质量的同时减小模型规模。这些策略通常依赖 2D 图像计算重要性分数，随后进行场景特定优化。本文提出 PointSplat，一种 3D 几何驱动的剪枝-精炼框架，桥接了先前相互独立的 Gaussian 剪枝与 Transformer 精炼方向。我们的方法包含两个关键组件：（1）高效几何驱动策略，仅基于 3D 属性对 Gaussians 排序，剪枝阶段不再依赖 2D 图像；（2）双分支编码器，分离并重加权几何与外观特征，避免特征失衡。在 ScanNet++ 和 Replica 上不同稀疏度级别的广泛实验表明，PointSplat 在不进行额外逐场景优化的情况下，始终取得有竞争力的渲染质量和更优效率。

---

<a id="paper-90"></a>
### [90] FreeScale: Scaling 3D Scenes via Certainty-Aware Free-View Generation
- **arXiv:** [2604.10512](https://arxiv.org/abs/2604.10512)

可泛化新视角合成（NVS）模型的发展受到大规模训练数据稀缺的严重制约，这类数据需具备多样且精确的相机轨迹。真实世界采集虽照片级真实，但通常稀疏且离散；合成数据虽可扩展，却存在域差距且常缺乏真实语义。我们提出 FreeScale，一种新颖框架，利用场景重建的力量将有限的真实世界图像序列转化为可扩展的高质量训练数据源。我们的核心洞察是：不完美的重建场景可作为丰富的几何代理，但朴素采样会放大伪影。为此，我们提出确定性感知的自由视角采样策略，识别既语义有意义又受重建误差影响最小的新视角。我们证明 FreeScale 的有效性：通过扩展前馈 NVS 模型训练，在具有挑战性的分布外基准上 PSNR 提升 2.7 dB。此外，生成的数据还能主动增强逐场景 3D Gaussian Splatting 优化，在多个数据集上带来一致改进。我们的工作提供了一种实用且强大的数据生成引擎，以克服 3D 视觉中的根本性瓶颈。项目主页：https://mvp-ai-lab.github.io/FreeScale。

---

<a id="paper-91"></a>
### [91] Learning 3D Representations for Spatial Intelligence from Unposed Multi-View Images
- **arXiv:** [2604.10573](https://arxiv.org/abs/2604.10573)

鲁棒的 3D 表示学习构成空间智能的感知基础，支撑场景理解和具身 AI 等下游任务。然而，直接从无姿态多视角图像学习此类表示仍具挑战。近期自监督方法尝试以前馈方式统一几何、外观和语义，但常受弱几何归纳、有限外观细节以及几何与语义不一致等问题困扰。我们提出 UniSplat，一种前馈框架，通过三个互补组件解决上述局限。首先，我们提出双掩码策略以加强编码器中的几何归纳：通过同时掩码编码器和解码器 token，并将解码器掩码定向于几何丰富区域，迫使模型从不完整视觉线索推断结构信息，即使在无姿态输入下也能获得几何感知表示。其次，我们开发由粗到细的 Gaussian splatting 策略，通过渐进精炼辐射场以减少外观-语义不一致。最后，为强制几何-语义一致性，我们引入姿态条件重校准机制，利用估计的相机参数将预测的 3D 点图和语义图重投影至图像平面，并与对应 RGB 和语义预测对齐，通过多头输出互相关联确保跨任务一致性，从而解决几何-语义错配。这些组件共同产生对无姿态、稀疏视角输入鲁棒且可泛化至多样任务的统一 3D 表示，为空间智能奠定感知基础。

---

<a id="paper-92"></a>
### [92] LumiMotion: Improving Gaussian Relighting with Scene Dynamics
- **arXiv:** [2604.10994](https://arxiv.org/abs/2604.10994)

在 3D 重建中，逆渲染——即恢复场景光照和材质属性——是一项基础问题。现有基于 Gaussian Splatting 的方法主要针对静态场景，常假设简化或中等光照以避免阴影与表面外观纠缠，这限制了其准确分离光照效应与材质属性的能力，尤其在真实世界条件下。我们通过利用动态元素——场景中发生运动的区域——作为逆渲染的监督信号来解决这一局限。运动使同一表面在不同光照条件下呈现，为解耦材质与光照提供更强线索。我们的实验结果支持这一论点：相比次优基线，反照率估计 LPIPS 提升 23%，场景重光照提升 15%。为此，我们提出 LumiMotion，首个利用动态信息进行逆渲染、可在任意动态场景运行的 Gaussian 方法。该方法学习动态 2D Gaussian Splatting 表示，采用一组新颖约束鼓励场景动态区域形变，同时保持静态区域稳定。我们证明，这种分离对反照率的正确优化至关重要。最后，我们发布包含五个场景、四种光照条件（各含静态与动态变体）的新合成基准，首次支持在动态环境和挑战性光照下对逆渲染方法的系统评估。项目主页：https://joaxkal.github.io/LumiMotion/。

---

<a id="paper-93"></a>
### [93] PDF-GS: Progressive Distractor Filtering for Robust 3D Gaussian Splatting
- **arXiv:** [2604.12580](https://arxiv.org/abs/2604.12580)

3D Gaussian Splatting（3DGS）的最新进展实现了令人印象深刻的实时照片级真实渲染。然而，传统训练流水线固有地假设输入图像间完全多视角一致，使其对违反该假设的干扰物敏感并导致视觉伪影。本文重新审视 3DGS 中一个尚未充分探索的方面：其抑制不一致信号的固有能力。基于这一洞察，我们提出 PDF-GS（Progressive Distractor Filtering for Robust 3D Gaussian Splatting），一种通过渐进式多阶段优化放大这一自过滤特性的框架。渐进过滤阶段利用差异线索逐步移除干扰物，随后的重建阶段从净化的 Gaussian 表示中恢复细粒度、视角一致的细节。通过这种迭代精炼，PDF-GS 实现鲁棒、高保真且无干扰物的重建，在多样数据集和具有挑战性的真实世界条件下一致优于基线。此外，我们的方法轻量且易于适配现有 3DGS 框架，无需架构改动或额外推理开销，达到新的 SOTA 性能。代码公开于：https://github.com/kangrnin/PDF-GS。

---

<a id="paper-94"></a>
### [94] PatchPoison: Poisoning Multi-View Datasets to Degrade 3D Reconstruction
- **arXiv:** [2604.13153](https://arxiv.org/abs/2604.13153)

3D Gaussian Splatting（3DGS）近期实现了从随意采集的多视角图像进行高度照片级真实的 3D 重建。然而，这种可及性引发了隐私担忧：公开可用的图像或视频可在未经所有者同意的情况下被利用以重建场景或物体的详细 3D 模型。我们提出 PatchPoison，一种轻量级数据集投毒方法，用于阻止未经授权的 3D 重建。与全局扰动不同，PatchPoison 在多视角数据集中每张图像的外围注入一个小型高频对抗补丁——结构化棋盘格。该补丁旨在通过引入虚假对应关系系统性错位估计的相机姿态，破坏 Structure-from-Motion（SfM）流水线（如 COLMAP）的特征匹配阶段，从而使下游 3DGS 优化偏离正确场景几何。在 NeRF-Synthetic 基准上，插入 12×12 像素补丁使重建误差（LPIPS）增加 6.8 倍，而投毒图像对人类观察者仍不显眼。PatchPoison 无需修改流水线，为内容创作者保护其多视角数据提供了实用的"即插即用"预处理步骤。

---

<a id="paper-95"></a>
### [95] ClipGStream: Clip-Stream Gaussian Splatting for Any Length and Any Motion Multi-View Dynamic Scene Reconstruction
- **arXiv:** [2604.13746](https://arxiv.org/abs/2604.13746)

动态 3D 场景重建对 VR、MR 和 XR 等沉浸式媒体至关重要，但对于具有大规模运动的长多视角序列仍具挑战。现有动态 Gaussian 方法要么是 Frame-Stream，可扩展但时间稳定性差；要么是 Clip，局部一致但以高内存和有限序列长度为代价。我们提出 ClipGStream，一种混合重建框架，在 clip 级别而非 frame 级别执行 stream 优化。序列被划分为短 clip，其中动态运动通过 clip 独立的时空场和残差 anchor 补偿建模以高效捕捉局部变化，而 clip 间继承的 anchor 和解码器维持跨 clip 的结构一致性。这种 Clip-Stream 设计实现了可扩展、无闪烁的长动态视频重建，具有高时间连贯性和更低内存开销。大量实验表明，ClipGStream 达到 SOTA 重建质量和效率。项目主页：https://liangjie1999.github.io/ClipGStreamWeb/。

---

<a id="paper-96"></a>
### [96] NG-GS: NeRF-Guided 3D Gaussian Splatting Segmentation
- **arXiv:** [2604.14706](https://arxiv.org/abs/2604.14706)

3D Gaussian Splatting（3DGS）的最新进展使得高效且照片级真实感的新视角合成成为可能。然而，由于高斯表示的离散性，在 3DGS 中准确分割物体仍然具有挑战性，这往往会在物体边界处导致混叠和伪影。本文提出 NG-GS，一种面向 3DGS 高质量物体分割的新框架，显式地解决边界离散化问题。我们的方法首先通过掩码方差分析自动识别物体边界处存在歧义的高斯。随后，我们应用径向基函数（RBF）插值构建空间连续的特征场，并通过多分辨率哈希编码增强以实现高效的多尺度表示。一种联合优化策略通过对齐损失与空间连续性损失，将 3DGS 与轻量级 NeRF 模块对齐，从而确保分割边界平滑且一致。在 NVOS、LERF-OVS 和 ScanNet 基准上的大量实验表明，我们的方法取得了最先进的性能，在边界 mIoU 上获得了显著提升。代码见 https://github.com/BJTU-KD3D/NG-GS。

---

<a id="paper-97"></a>
### [97] TokenGS: Decoupling 3D Gaussian Prediction from Pixels with Learnable Tokens
- **arXiv:** [2604.15239](https://arxiv.org/abs/2604.15239)

本文重新审视了基于 Transformer 的前馈式 3D Gaussian Splatting（3DGS）预测中的若干关键设计选择。我们认为，将高斯均值回归为沿相机射线的深度这一常见做法并非最优，并提出仅使用自监督渲染损失直接回归三维均值坐标。该表述使我们能够从标准的仅编码器设计转向带有可学习高斯 token 的编码器-解码器架构，从而将预测基元的数量与输入图像分辨率及视角数量解耦。我们提出的方法 TokenGS 在姿态噪声和多视角不一致性方面展现出更强的鲁棒性，同时能够自然地在 token 空间中进行高效的测试时优化，且不会削弱已学习的先验。TokenGS 在静态与动态场景上均取得了最先进的前馈重建性能，产生更规则的几何与更均衡的 3DGS 分布，并能无缝恢复诸如静动态分解与场景流等涌现的场景属性。

---

<a id="paper-98"></a>
### [98] Neural Gabor Splatting: Enhanced Gaussian Splatting with Neural Gabor for High-frequency Surface Reconstruction
- **arXiv:** [2604.15941](https://arxiv.org/abs/2604.15941)

近年来，3D Gaussian Splatting（3DGS）作为三维重建与新视角合成的强大方法迅速兴起。其基于高斯基元的显式表示支持快速训练、实时渲染，以及编辑与表面重建等便捷的后处理。然而，3DGS 存在一个关键缺陷：对于具有高频外观细节的场景，基元数量会急剧增长，因为每个基元只能表示单一颜色，每个尖锐的颜色过渡都需要多个基元。为克服这一局限，我们提出 Neural Gabor Splatting，为每个高斯基元配备轻量级多层感知机，以在单个基元内建模广泛的颜色变化。为进一步控制基元数量，我们引入频率感知的致密化策略，依据频率能量选择不匹配基元进行剪枝与克隆。我们的方法能够准确重建具有挑战性的高频表面。我们在 Mip-NeRF360 与 High-Frequency 数据集（如棋盘格图案）等标准基准上通过大量实验及全面的消融研究验证了其有效性。

---

<a id="paper-99"></a>
### [99] A Survey of Spatial Memory Representations for Efficient Robot Navigation
- **arXiv:** [2604.16482](https://arxiv.org/abs/2604.16482)

随着基于视觉的机器人在更大规模环境中导航，其空间记忆会无界增长，最终耗尽计算资源，尤其是在嵌入式平台（8–16GB 共享内存、<$30W）上，增加硬件往往并不可行。本综述考察了空间记忆效率问题，涵盖 88 篇参考文献、52 个系统（1989–2025），从占据栅格到神经隐式表示。我们引入 $α= M_{\text{peak}} / M_{\text{map}}$，即峰值运行时内存（运行期间消耗的总 RAM 或 GPU 内存）与保存地图大小（写入磁盘的持久化检查点）之比，从而揭示已发表地图规模与实际部署成本之间的差距。在 NVIDIA A100 GPU 上的独立性能分析表明，仅神经方法内部 $α$ 就跨越两个数量级，从 2.3（Point-SLAM）到 215（NICE-SLAM，其 47 MB 地图在运行时需要 10GB），说明决定部署可行性的因素是内存架构，而非范式标签。我们提出一套标准化评估协议，包括记忆增长率、查询延迟、记忆-完整度曲线和吞吐量退化，而现有基准均未涵盖这些指标。通过带有显式基准分离的 Pareto 前沿分析，我们表明在其各自评估范围内没有单一范式占据绝对优势：3DGS 方法在 Replica 上以 90–254 MB 地图规模取得最佳绝对精度，而场景图以可预测的成本提供语义抽象。我们提供了首批独立测得的 $α$ 参考值，以及一种 $α$ 感知的预算算法，使从业者能够在实现之前评估目标硬件上的部署可行性。

---

<a id="paper-100"></a>
### [100] PoInit-of-View: Poisoning Initialization of Views Transfers Across Multiple 3D Reconstruction Systems
- **arXiv:** [2604.16540](https://arxiv.org/abs/2604.16540)

对三维重建系统输入视角进行投毒攻击已受到近期研究关注。然而，我们发现现有研究只是将对抗梯度整体反向传播通过三维重建流水线，并未揭示根植于重建流水线特定模块的新漏洞。本文认为，作为许多广泛使用的重建系统几何核心的 Structure-from-Motion（SfM）初始化，可以被针对性地利用，从而在多种三维重建系统之间实现可迁移的投毒效果。为此，我们提出 PoInit-of-View，优化对抗扰动以在对应三维点的投影处故意引入跨视角梯度不一致。这些不一致性破坏关键点检测与特征匹配，从而破坏 SfM 内的位姿估计与三角化，最终导致低质量的渲染视角。我们还提供了将跨视角不一致性与对应关系崩溃联系起来的理论分析。实验结果表明，PoInit-of-View 在多种三维重建系统与数据集上有效，在 3DGS 到 NeRF 等黑盒迁移设置中，相比单视角基线 PSNR 提升 25.1%、SSIM 提升 16.5%。

---

<a id="paper-101"></a>
### [101] D-Prism: Differentiable Primitives for Structured Dynamic Modeling
- **arXiv:** [2604.17082](https://arxiv.org/abs/2604.17082)

对结构化动态物体（如多部件装配体或关节机构）同时捕获几何与刚体运动仍是一项关键挑战。现有动态方法（如可变形网格或 3DGS）依赖非结构化表示，无法联合建模合适的几何与关节运动。基于基元的方法在结构化静态场景中表现优异，但其动态潜力尚未被探索。我们提出 D-Prism，首个通过将可微基元扩展到动态域以实现高保真结构化动态建模的框架。具体而言，我们将 3DGS 绑定到基元表面，分别利用二者在外观与几何方面的优势。我们引入变形网络控制基元运动，确保其准确匹配物体的运动。此外，我们设计了一种新颖的自适应控制策略，动态调整基元数量，以更好地匹配物体的真实空间占用。实验证实，我们的方法在结构化动态建模上表现优异，同时提供结构化几何与精确的运动跟踪。

---

<a id="paper-102"></a>
### [102] SketchFaceGS: Real-Time Sketch-Driven Face Editing and Generation with Gaussian Splatting
- **arXiv:** [2604.19202](https://arxiv.org/abs/2604.19202)

三维高斯表示已成为数字人头建模的强大范式，在实现照片级真实感质量的同时支持实时渲染。然而，直观且交互式地创建或编辑三维高斯人头模型仍然具有挑战性。尽管二维草图为快速、直观的概念设计提供了理想的交互方式，但其稀疏、深度歧义且缺乏高频外观线索，使得从笔画推断稠密且几何一致的三维高斯结构十分困难——尤其是在实时约束下。为应对这些挑战，我们提出 SketchFaceGS，首个用于从二维草图实时生成与编辑照片级真实感三维高斯人头模型的草图驱动框架。我们的方法采用前馈式由粗到精架构：基于 Transformer 的 UV 特征预测模块首先从输入草图重建粗略但几何一致的 UV 特征图，随后三维 UV 特征增强模块以高频、照片级真实感细节对其进行精炼，生成高保真人头。对于编辑，我们引入 UV Mask Fusion 技术并结合逐层特征融合策略，实现精确、实时、自由视角的修改。大量实验表明，SketchFaceGS 在生成保真度与编辑灵活性上均优于现有方法，可在单次前向传播中从草图生成高质量、可编辑的三维人头。

---

<a id="paper-103"></a>
### [103] DualSplat: Robust 3D Gaussian Splatting via Pseudo-Mask Bootstrapping from Reconstruction Failures
- **arXiv:** [2604.21631](https://arxiv.org/abs/2604.21631)

尽管 3D Gaussian Splatting（3DGS）实现了实时照片级真实感渲染，当训练图像包含违反多视角一致性的瞬态物体时，其性能会显著下降。现有方法面临循环依赖：准确的瞬态检测需要良好重建的静态场景，而干净的重建本身又依赖可靠的瞬态掩码。我们通过 DualSplat 应对这一挑战，这是一种 Failure-to-Prior 框架，将第一遍重建失败转化为第二遍重建阶段的显式先验。我们观察到，仅出现在部分视角中的瞬态物体，在保守的初始训练中往往表现为不完整的碎片。我们利用这些失败，结合光度残差、特征不匹配与 SAM2 实例边界构建物体级伪掩码。这些伪掩码随后引导第二遍干净的 3DGS 优化，同时轻量级 MLP 在线精炼它们，逐渐从先验监督转向自一致性。在 RobustNeRF 与 NeRF On-the-go 上的实验表明，DualSplat 优于现有基线，在瞬态密集场景与瞬态区域中优势尤为明显。

---

<a id="paper-104"></a>
### [104] Bringing a Personal Point of View: Evaluating Dynamic 3D Gaussian Splatting for Egocentric Scene Reconstruction
- **arXiv:** [2604.23803](https://arxiv.org/abs/2604.23803)

以自我为中心的视频为人类感知与交互提供了独特视角，在增强现实、机器人与辅助技术中日益重要。然而，快速的相机运动与复杂的场景动态给从该视角进行三维重建带来重大挑战。尽管 3D Gaussian Splatting（3DGS）已成为高效、高质量新视角合成的最先进方法，专注于从单目视频重建动态场景的变体很少在自我中心视频上得到评估。现有模型是否能泛化到该设置，抑或需要自我中心专用方案，仍不明确。本文使用 EgoExo4D 数据集的配对 ego-exo 录制，在自我中心与外中心视频上评估动态单目 3DGS 模型。我们发现，自我中心视角的重建质量始终较低。分析表明，以峰值信噪比（PSNR）衡量的重建质量差异源于静态内容而非动态内容的重建。我们的发现凸显了当前方法的局限，并推动自我中心专用方法的发展，同时强调了分别评估视频中静态与动态区域的价值。

---

<a id="paper-105"></a>
### [105] Generalizable Human Gaussian Splatting via Multi-view Semantic Consistency
- **arXiv:** [2604.25466](https://arxiv.org/abs/2604.25466)

近年来，从稀疏视角输入实现可泛化的人体 Gaussian Splatting 以用于照片级真实感人体渲染受到积极研究。大多数现有方法依赖显式几何约束或预定义的结构化表示来准确定位三维高斯。尽管这些方法在该领域取得了显著进展，但由于人体复杂的关节运动以及不同视角间有限的重叠，它们仍受多视角输入间特征表示不一致问题的困扰。为解决该问题，我们提出一种新方法，以准确定位三维高斯并最终提升人体渲染质量。核心思想是将各视角编码的 latent embedding 通过预测的深度图反投影到共享三维空间，并基于跨视角注意力对属于同一身体部位的 embedding 进行重新校准。这有助于模型解决高度纹理区域以及被遮挡身体部位中的空间歧义，从而实现三维高斯的准确定位。在基准数据集上的实验结果表明，所提方法有效提升了从稀疏视角输入进行可泛化人体 Gaussian Splatting 的性能。

---

<a id="paper-106"></a>
### [106] Semantic Foam: Unifying Spatial and Semantic Scene Decomposition
- **arXiv:** [2604.26262](https://arxiv.org/abs/2604.26262)

现代场景重建方法（如 3D Gaussian Splatting）以实时速度提供照片级真实感的新视角合成，但其在交互式图形应用中的采用仍有限。主要瓶颈在于与人工制作的传统三维资产相比，与这些表示进行交互的难度较大。尽管已有研究尝试为这些模型施加语义分解，但在分割质量与一致性方面仍存在重大挑战。为此，我们提出 Semantic Foam，将近期提出的 Radiant Foam 表示扩展到语义分解任务。我们的方法将 Radiant Foam 的 Voronoi 网格所固有的空间体积分解与在单元级别参数化的显式语义特征场相结合。该显式结构支持直接的空间正则化，从而避免由遮挡或跨视角不一致监督引起的伪影——这是其他基于点的表示常见的陷阱。实验结果表明，我们的方法在物体级分割性能上达到与 Gaussian Grouping、SAGA 等最先进方法相当或更优的水平。

---

<a id="paper-107"></a>
### [107] Color-Encoded Illumination for High-Speed Volumetric Scene Reconstruction
- **arXiv:** [2604.26920](https://arxiv.org/abs/2604.26920)

从二维图像捕获并渲染三维动态场景的任务近年来日益流行。然而，大多数常规相机的带宽限制在 30–60 FPS，使这些方法局限于静态或缓慢演化的场景。虽然对一般场景克服带宽限制较为困难，近年来出现了一系列利用常规相机为特定应用（如动作捕捉与粒子图像测速）生成高速视频的计算成像方法。然而，这些方法大多需要修改相机光学系统或增加机械运动部件，因而局限于单视角高速捕获，无法直接用于捕获快速场景运动的三维表示。本文提出一种新方法，仅使用未改动的低速相机捕获并重建高速场景的体积表示。我们不修改各相机的硬件或光学系统，而是通过以快速、顺序的颜色编码序列照亮场景来编码高速场景动态。这实现了场景的同时多视角捕获，其中高速时间信息编码于捕获图像的空间强度与颜色变化中。为构建动态场景的高速体积表示，我们开发了一种基于动态 Gaussian Splatting 的新方法，从图像中解码时间信息。我们在模拟场景与真实多相机成像实验上评估了该方法，展示了首批同类高速体积场景重建。

---

<a id="paper-108"></a>
### [108] Softmax-GS: Generalized Gaussians Learning When to Blend or Bound
- **arXiv:** [2604.27437](https://arxiv.org/abs/2604.27437)

3D Gaussian Splatting（3D GS）因其高训练与渲染效率而被广泛采用于新视角合成。然而，其效率依赖于高斯在三维空间中不重叠的关键假设，这会导致明显的伪影与视角不一致。此外，高斯固有的弥散边界阻碍了对尖锐物体边缘的准确重建。我们提出 Softmax-GS，一种统一解决方案，通过在两个重叠高斯之间的重叠区域施加基于 softmax 的竞争机制，同时解决视角不一致与弥散边界问题。通过可学习参数控制竞争强度，它实现了从平滑颜色混合到清晰、明确边界的连续谱。我们的公式显式保持任意两个重叠高斯的顺序不变性，并确保输出透射率与重叠程度无关而保持不变，从而避免渲染输出中的不期望不连续。在简单几何上的消融实验验证了 Softmax-GS 各分量的有效性，在真实世界基准上的评估表明其取得了最先进的性能，同时提升了重建质量与参数效率。

---

<a id="paper-109"></a>
### [109] Generalizable Sparse-View 3D Reconstruction from Unconstrained Images
- **arXiv:** [2604.28193](https://arxiv.org/abs/2604.28193)

在光照变化与瞬态遮挡等真实世界条件下，从稀疏、无位姿图像重建三维场景仍然具有挑战性。现有方法依赖外观 embedding 或动态掩码进行逐场景优化，需要大量逐场景训练且在稀疏视角下失效。此外，在有限场景上的评估也引发了对泛化能力的质疑。我们提出 GenWildSplat，一种用于稀疏视角室外重建的前馈框架，无需逐场景优化。给定无位姿的互联网图像，GenWildSplat 利用学习的几何先验在规范空间中预测深度、相机参数与三维高斯。外观适配器调制目标光照条件下的外观，语义分割处理瞬态物体。通过在合成与真实数据上的课程学习，GenWildSplat 可泛化到多样化的光照与遮挡模式。在 PhotoTourism 与 MegaScenes 基准上的评估表明，其取得了最先进的前馈渲染质量，在无需测试时优化的情况下实现实时推理。

---

<a id="paper-110"></a>
### [110] GOR-IS: 3D Gaussian Object Removal in the Intrinsic Space
- **arXiv:** [2605.00498](https://arxiv.org/abs/2605.00498)

Neural Radiance Fields（NeRF）与 3D Gaussian Splatting（3DGS）的最新进展使从多视角图像重建三维场景成为标准做法。从这类三维表示中移除物体是一项基础编辑任务，需要对被遮挡区域进行完整且无缝的 inpainting，并确保几何与外观一致。尽管现有方法在提升 inpainting 一致性方面取得了显著进展，它们往往忽略全局光照效应，导致物理上不可信的结果。此外，这些方法难以处理视角相关的非 Lambertian 表面，其外观随视角变化，导致 inpainting 不可靠。本文提出 3D Gaussian Object Removal in the Intrinsic Space（GOR-IS），一种用于物理一致且视觉连贯的三维物体移除的新框架。我们的方法将场景分解为 intrinsic 分量，并显式建模光传输以保持全局光照效应的一致性。此外，我们引入 intrinsic 空间 inpainting 模块，直接在材质与光照域中操作，有效应对非 Lambertian 表面带来的挑战。在合成与真实世界数据集上的大量实验表明，我们的框架显著提升了物体移除的物理一致性与视觉连贯性，在感知相似度（LPIPS）上优于现有方法 13%，在峰值信噪比（PSNR）上优于 2dB。代码公开见 https://applezyh.github.io/GOR-IS-project-page/。

---

<a id="paper-111"></a>
### [111] Multi-Scale Gaussian-Language Map for Zero-shot Embodied Navigation and Reasoning
- **arXiv:** [2605.01736](https://arxiv.org/abs/2605.01736)

理解环境的几何与语义结构对具身导航与推理至关重要。现有语义建图方法在显式几何与多尺度语义之间权衡，且缺乏面向大模型的原生接口，因而需要额外训练特征投影以实现语义对齐。为此，我们提出 multi-scale Gaussian-Language Map（GLMap），引入三项关键设计：（1）显式几何；（2）涵盖实例与区域概念的多尺度语义；（3）双模态接口，其中每个语义单元联合存储自然语言描述与三维高斯表示。三维高斯通过 Gaussian Splatting 实现紧凑存储与任务相关图像的快速渲染。为实现高效的增量构建，我们进一步提出 Gaussian Estimator，从稠密点云解析推导高斯参数，无需基于梯度的优化。在 ObjectNav、InstNav 与 SQA 任务上的实验表明，GLMap 有效增强目标导航与上下文推理，同时以零样本方式与大模型方法兼容。代码见 https://github.com/sx-zhang/GLMap。

---

<a id="paper-112"></a>
### [112] Velox: Learning Representations of 4D Geometry and Appearance
- **arXiv:** [2605.04527](https://arxiv.org/abs/2605.04527)

我们引入一种学习四维物体 latent 表示的框架，该表示具有描述性，忠实捕获物体几何与外观；具有压缩性，有助于下游效率；且易于获取，仅需非结构化动态点云作为输入即可构建。具体而言，Velox 训练编码器将时空彩色点云压缩为一组动态 shape token。这些 token 通过两个互补解码器进行监督：四维表面解码器建模时变表面分布以捕获几何；高斯解码器将 token 映射为三维高斯，辅助学习外观。为展示我们表示的实用性，我们在三个下游任务——video-to-4D 生成、三维跟踪以及通过 image-to-4D 生成的布料模拟——上进行评估，在所有设置中均观察到强劲表现。

---

<a id="paper-113"></a>
### [113] ULF-Loc: Unbiased Landmark Feature for Robust Visual Localization with 3D Gaussian Splatting
- **arXiv:** [2605.04730](https://arxiv.org/abs/2605.04730)

视觉定位是增强现实与自主导航的核心技术。近期方法将 3D Gaussian Splatting（3DGS）的高效渲染与基于特征的定位相结合。这些方法依赖二维查询特征与三维高斯特征场之间的直接匹配，但由于学习得到的高斯特征中固有的偏差，往往导致匹配错误。我们从理论上分析了 3DGS 中的特征学习过程，揭示广泛采用的 $α$-blending 优化会固有地向三维点特征引入偏差。该偏差源于单个高斯与其邻域高斯之间的纠缠，使学习到的特征不适合精确匹配任务。基于这些发现，我们提出 ULF-Loc，一种 unbiased landmark feature 框架，以几何加权特征融合替代有偏的特征优化。我们进一步引入 keypoint-consensus landmark sampling 以选择可靠高斯，以及局部几何一致性验证以拒绝由渲染伪影引起的误匹配。在 Cambridge Landmarks 数据集上，ULF-Loc 相比最先进方法将平均中位平移误差降低 17%，同时以仅 1/10 的训练时间与 1/6 的 GPU 内存实现更优效率，优于 STDLoc。

---

<a id="paper-114"></a>
### [114] BEA-GS: BEyond RAdiance Supervision in 3DGS for Precise Object Extraction
- **arXiv:** [2605.09662](https://arxiv.org/abs/2605.09662)

大多数提供场景三维语义表示的 Gaussian Splatting 技术并不优化底层三维几何，使得物体级编辑或资产提取具有挑战性。COBGS、Trace3D、ObjectGS 等近期方法认识到这一局限，提出修改场景几何以表示底层语义。我们进一步推进这一概念，提出一种新颖的解决方案，在物体提取中提供近乎完美的边界。为此，我们在优化中引入两项新损失：（1）修改可见高斯几何以尊重语义边界的损失；（2）调整物体提取后才出现之不可见高斯几何的损失。第一项损失直接通过光栅化传播梯度，可无缝集成到高斯参数的优化中。第二项损失同样向高斯参数传播梯度，但不经过光栅化，从而即使到达某高斯的透射率很低（部分可见或不可见）时也能修改场景几何。与 12 种最先进方法在 4 个数据集上、使用 6 项指标的全面对比表明，我们的方法迄今产生了整体最佳的边界分割效果。

---
