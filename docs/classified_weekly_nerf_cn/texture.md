
每周分类神经辐射场 - texture ![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)
====================================================================================================================================
## 按类别筛选: 
 [全部](../weekly_nerf_cn.md) | [动态](./dynamic.md) | [编辑](./editing.md) | [快速](./fast.md) | [泛化](./generalization.md) | [人体](./human.md) | [视频](./video.md) | [光照](./lighting.md) | [重建](./reconstruction.md) | [纹理](./texture.md) | [语义](./semantic.md) | [姿态-SLAM](./pose-slam.md) | [其他](./others.md) 
## Nov13 - Nov19, 2022
## Nov6 - Nov12, 2022
## Oct30 - Nov5, 2022
  - [深度外观预过滤, ToG2022](https://dl.acm.org/doi/abs/10.1145/3570327) | [code]
    > 复杂场景的基于物理的渲染可能成本高得令人望而却步，并且复杂性在渲染图像上的分布可能是无限且不均匀的。理想的细节层次 (LoD) 方法的目标是使渲染成本独立于 3D 场景的复杂性，同时保持场景的外观。然而，由于依赖近似模型和其他启发式方法，当前的预过滤 LoD 方法在它们可以支持的外观方面受到限制。我们提出了第一个全面的多尺度 LoD 框架，用于预过滤具有复杂几何形状和材料（例如 Disney BRDF）的 3D 环境，同时保持与光线追踪参考相关的外观。使用场景的多尺度层次结构，我们执行数据驱动的预过滤步骤以获得每个尺度的外观相位函数和方向覆盖掩码。我们方法的核心是一种新颖的神经表示，它将这些信息编码成一种紧凑的潜在形式，这种形式很容易在基于物理的渲染器中解码。一旦场景被烘焙出来，我们的方法在渲染时不需要原始几何体、材质或纹理。我们证明我们的方法与最先进的预过滤方法相比具有优势，并且可以为复杂场景节省大量内存。
## Oct23 - Oct29, 2022
## Oct16 - Oct22, 2022
## Oct9 - Oct15, 2022
  - [IBL-NeRF：基于图像的神经辐射场照明公式](https://arxiv.org/abs/2210.08202) | [code]
    > 我们提出了 IBL-NeRF，它将大规模室内场景的神经辐射场 (NeRF) 分解为内在成分。以前的 NeRF 逆向渲染方法转换隐式体积以适应显式几何的渲染管道，并使用环境照明近似分割、孤立对象的视图。相比之下，我们的逆渲染扩展了原始的 NeRF 公式，以捕捉场景体积内照明的空间变化，以及表面属性。具体来说，将不同材质的场景分解为基于图像的渲染的内在组件，即反照率、粗糙度、表面法线、辐照度和预过滤辐射度。所有组件都被推断为来自 MLP 的神经图像，可以对大规模的一般场景进行建模。通过采用基于图像的 NeRF 公式，我们的方法继承了合成图像的卓越视觉质量和多视图一致性。我们展示了在具有复杂对象布局和灯光配置的场景上的性能，这些在以前的任何作品中都无法处理。
  - [NeuralRoom：用于室内场景重建的几何约束神经隐式表面](https://arxiv.org/abs/2210.06853) | [code]
    > 我们提出了一种称为 NeuralRoom 的新型神经表面重建方法，用于直接从一组 2D 图像重建房间大小的室内场景。最近，由于其高质量的结果和简单性，隐式神经表示已成为从多视图图像重建表面的有前途的方法。然而，隐式神经表示通常不能很好地重建室内场景，因为它们存在严重的形状-辐射度模糊性。我们假设室内场景由纹理丰富和平坦的无纹理区域组成。在纹理丰富的区域，多视图立体可以获得准确的结果。在平坦区域，正态估计网络通常能获得较好的正态估计。基于上述观察，我们通过可靠的几何先验来减少隐式神经表面可能的空间变化范围，以减轻形状-辐射度的模糊性。具体来说，我们使用多视图立体结果来限制 NeuralRoom 优化空间，然后使用可靠的几何先验来指导 NeuralRoom 训练。然后，NeuralRoom 将生成一个神经场景表示，该表示可以渲染与输入训练图像一致的图像。此外，我们提出了一种称为扰动残差限制的平滑方法来提高平坦区域的准确性和完整性，该方法假设局部表面中的采样点应该与观测中心具有相同的法线和相似的距离。在 ScanNet 数据集上的实验表明，我们的方法可以重建室内场景的无纹理区域，同时保持细节的准确性。我们还将 NeuralRoom 应用于更高级的多视图重建算法，并显着提高了它们的重建质量。
## Oct2 - Oct8, 2022
## Sep25 - Oct1, 2022
## Sep18 - Sep24, 2022
  - [SG-SRNs：超像素引导的场景表示网络, SignalProcessingLetters](https://ieeexplore.ieee.org/abstract/document/9900405) | [code]
    > 最近，场景表示网络（SRNs）由于其连续且轻量级的场景表示能力，在计算机视觉领域引起了越来越多的关注。然而，SRN 通常在低纹理图像区域上表现不佳。为了解决这个问题，我们在本文中提出了超像素引导的场景表示网络，称为 SG-SRN，由主干模块 (SRN)、超像素分割模块和超像素正则化模块组成。在所提出的方法中，除了新颖的视图合成任务外，表示感知的超像素分割掩码生成任务由所提出的超像素分割模块实现。然后，超像素正则化模块利用超像素分割掩码以局部平滑的方式引导要学习的主干，并优化局部区域的场景表示，以自监督的方式间接缓解低纹理区域的结构失真.在我们构建的数据集和公共 Synthetic-NeRF 数据集上的广泛实验结果表明，所提出的 SG-SRN 实现了显着更好的 3D 结构表示性能。
  - [通过神经动画网格进行人体性能建模和渲染](https://arxiv.org/abs/2209.08468) | [code]
    > 我们最近看到了照片真实人体建模和渲染的神经进步的巨大进步。但是，将它们集成到现有的基于网格的管道中以用于下游应用程序仍然具有挑战性。在本文中，我们提出了一种综合神经方法，用于从密集的多视图视频中对人类表演进行高质量的重建、压缩和渲染。我们的核心直觉是将传统的动画网格工作流程与新型高效神经技术联系起来。我们首先介绍了一种用于在几分钟内生成高质量表面的神经表面重建器。它将截断有符号距离场 (TSDF) 的隐式体积渲染与多分辨率哈希编码结合在一起。我们进一步提出了一种混合神经跟踪器来生成动画网格，它将显式非刚性跟踪与自监督框架中的隐式动态变形相结合。前者将粗略的变形提供回规范空间，而后者隐含的进一步使用我们的重构器中的 4D 哈希编码来预测位移。然后，我们讨论使用获得的动画网格的渲染方案，范围从动态纹理到各种带宽设置下的流明图渲染。为了在质量和带宽之间取得复杂的平衡，我们提出了一种分层解决方案，首先渲染覆盖表演者的 6 个虚拟视图，然后进行遮挡感知神经纹理混合。我们展示了我们的方法在各种基于网格的应用程序和各种平台上逼真的自由视图体验中的有效性，即通过移动 AR 将虚拟人类表演插入真实环境或使用 VR 耳机沉浸式观看才艺表演。
## Sep11 - Sep17, 2022
  - [StructNeRF：具有结构提示的室内场景的神经辐射场](https://arxiv.org/abs/2209.05277) | [code]
    > 神经辐射场 (NeRF) 使用密集捕获的输入图像实现照片般逼真的视图合成。然而，在给定稀疏视图的情况下，NeRF 的几何形状受到极大限制，导致新视图合成质量显着下降。受自监督深度估计方法的启发，我们提出了 StructNeRF，这是一种针对具有稀疏输入的室内场景的新颖视图合成的解决方案。 StructNeRF 利用自然嵌入在多视图输入中的结构提示来处理 NeRF 中的无约束几何问题。具体来说，它分别处理纹理和非纹理区域：提出了一种基于块的多视图一致光度损失来约束纹理区域的几何形状；对于非纹理平面，我们明确将它们限制为 3D 一致平面。通过密集的自监督深度约束，我们的方法提高了 NeRF 的几何和视图合成性能，而无需对外部数据进行任何额外的训练。对几个真实世界数据集的广泛实验表明，StructNeRF 在数量和质量上都超过了用于室内场景的最先进的方法。
## Sep4 - Sep10, 2022
  - [具有学习几何先验的 3D 纹理形状恢复](https://arxiv.org/abs/2209.03254) | [code]
    > 从部分扫描中恢复 3D 纹理形状对于许多实际应用至关重要。现有方法已经证明了隐式函数表示的有效性，但它们存在严重遮挡和不同对象类型的部分输入，这极大地阻碍了它们在现实世界中的应用价值。本技术报告介绍了我们通过结合学习几何先验来解决这些限制的方法。为此，我们从学习的姿势预测中生成一个 SMPL 模型，并将其融合到部分输入中，以添加人体的先验知识。我们还提出了一种新颖的完整性感知边界框自适应，用于处理不同级别的尺度和部分扫描的局部性。
## Aug28 - Sep3, 2022
## Aug21 - Aug27, 2022
## Aug14 - Aug20, 2022
## Aug7 - Aug13, 2022
## Jul31 - Aug6, 2022
## Jul24 - Jul30, 2022
  - [ShAPO：多对象形状、外观和姿势优化的隐式表示, ECCV2022](https://arxiv.org/abs/2207.13691) | [***``[code]``***](https://zubair-irshad.github.io/projects/ShAPO.html)
    > 我们的方法从单个 RGB-D 观察中研究以对象为中心的 3D 理解的复杂任务。由于这是一个不适定问题，现有方法在具有遮挡的复杂多对象场景中的 3D 形状和 6D 姿势和尺寸估计性能低下。我们提出了 ShaAPO，一种用于联合多对象检测、3D 纹理重建、6D 对象姿态和大小估计的方法。 ShAPO 的关键是一个单次管道，用于回归形状、外观和姿势潜在代码以及每个对象实例的掩码，然后以稀疏到密集的方式进一步细化。首先学习了一种新的解开的先验形状和外观数据库，以将对象嵌入到它们各自的形状和外观空间中。我们还提出了一种新颖的、基于八叉树的可微优化步骤，使我们能够以综合分析的方式在学习的潜在空间下同时进一步改进对象形状、姿势和外观。我们新颖的联合隐式纹理对象表示使我们能够准确地识别和重建新的看不见的对象，而无需访问它们的 3D 网格。通过广泛的实验，我们证明了我们的方法在模拟室内场景上进行训练，能够以最少的微调准确地回归现实世界中新物体的形状、外观和姿势。我们的方法显着优于 NOCS 数据集上的所有基线，6D 姿态估计的 mAP 绝对提高了 8%。
  - [NeuMesh：学习基于解缠结神经网格的隐式场，用于几何和纹理编辑, ECCV2022(oral)](https://arxiv.org/abs/2207.11911) | [code]
    > 最近，神经隐式渲染技术得到了迅速发展，并在新颖的视图合成和 3D 场景重建中显示出巨大的优势。然而，现有的用于编辑目的的神经渲染方法提供的功能有限，例如，刚性变换，或者不适用于日常生活中一般对象的细粒度编辑。在本文中，我们提出了一种新颖的基于网格的表示，通过在网格顶点上使用解开几何和纹理代码对神经隐场进行编码，这促进了一组编辑功能，包括网格引导的几何编辑、带有纹理交换的指定纹理编辑、填充和绘画操作。为此，我们开发了几种技术包括可学习的符号指标以放大基于网格的表示的空间可区分性，蒸馏和微调机制以实现稳定收敛，以及空间感知优化策略以实现精确的纹理编辑。对真实数据和合成数据的大量实验和编辑示例证明了我们的方法在表示质量和编辑能力方面的优越性。代码可在项目网页上找到：此 https URL。
## Previous weeks
  - [CodeNeRF：对象类别的解开神经辐射场, ICCV2021(oral)](https://www.google.com/url?q=https%3A%2F%2Farxiv.org%2Fpdf%2F2109.01750.pdf&sa=D&sntz=1&usg=AOvVaw1Fnir0e4aRa22Nt0HoXDWh) | [***``[code]``***](https://www.google.com/url?q=https%3A%2F%2Fgithub.com%2Fwbjang%2Fcode-nerf&sa=D&sntz=1&usg=AOvVaw2eD5ZoRbk2aWFuwUSHlh5_)
    > CodeNeRF 是一种隐式 3D 神经表示，它学习对象形状和纹理在一个类别中的变化，并且可以从一组姿势图像中进行训练，以合成看不见的对象的新视图。与特定场景的原始 NeRF 不同，CodeNeRF 通过学习单独的嵌入来学习解开形状和纹理。在测试时，给定一个看不见的物体的单个未定位图像，CodeNeRF 通过优化联合估计相机视点、形状和外观代码。看不见的物体可以从单个图像中重建，然后从新的视点渲染，或者通过改变潜在代码编辑它们的形状和纹理。我们在 SRN 基准上进行了实验，结果表明 CodeNeRF 可以很好地泛化到看不见的对象，并且在测试时需要已知相机姿态的方法达到同等性能。我们在真实世界图像上的结果表明，CodeNeRF 可以弥合模拟到真实的差距。
  - [物体辐射场的无监督发现, ICLR2022](https://arxiv.org/abs/2107.07905) | [code]
    > 我们研究从单个图像推断以对象为中心的场景表示的问题，旨在推导出解释图像形成过程的表示，捕捉场景的 3D 性质，并且在没有监督的情况下学习。由于将复杂的 3D 到 2D 图像形成过程集成到强大的推理方案（如深度网络）中存在根本性挑战，大多数现有的场景分解方法都缺乏这些特征中的一个或多个。在本文中，我们提出了对象辐射场 (uORF) 的无监督发现，将神经 3D 场景表示和渲染的最新进展与深度推理网络相结合，用于无监督 3D 场景分解。在没有注释的多视图 RGB 图像上进行训练，uORF 学习从单个图像分解具有不同纹理背景的复杂场景。我们展示了 uORF 在无监督 3D 场景分割、新视图合成和三个数据集上的场景编辑方面表现良好。
  - [NeRF-Tex：神经反射场纹理, EGSR2021](https://developer.nvidia.com/blog/nvidia-research-nerf-tex-neural-reflectance-field-textures/) | [***``[code]``***](https://github.com/hbaatz/nerf-tex)
    > 我们研究使用神经场来模拟不同的中尺度结构，例如毛皮、织物和草。我们建议使用由神经反射场 (NeRF-Tex) 表示的多功能体积基元，而不是使用经典的图形基元来建模结构，它联合建模材料的几何形状及其对照明的响应。 NeRF-Tex 原语可以在基础网格上实例化，以使用所需的细观和微尺度外观对其进行“纹理化”。我们根据控制外观的用户定义参数来调节反射率场。因此，单个 NeRF 纹理捕获了反射场的整个空间，而不是一个特定的结构。这增加了可以建模的外观范围，并提供了一种解决重复纹理伪影的解决方案。我们还证明了 NeRF 纹理自然地促进了连续的细节层次渲染。我们的方法将神经网络的多功能性和建模能力与虚拟场景精确建模所需的艺术控制相结合。虽然我们所有的训练数据目前都是合成的，但我们的工作提供了一个方法，可以进一步扩展以从真实图像中提取复杂、难以建模的外观。
