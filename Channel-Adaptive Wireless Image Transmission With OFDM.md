---
tags:
  - research/read
title: Channel-Adaptive Wireless Image Transmission With OFDM
author: Haotian Wu , Graduate Student Member, IEEE, Yulin Shao, Member, IEEE, Krystian Mikolajczyk, Senior Member, IEEE, and Deniz Gündüz , Fellow, IEEE
date: 2020-5-1
journal: " IEEE JOURNAL ON SELECTED AREAS IN INFORMATION THEORY"
paper_class: Semantic Communication; Feedback channel
rdate: 2024-12-01
---

## Intruction


**_Background_**



**_Motivation_**


## MainWork

**_technical route_**


**_result_**


**_contuibution_**


**_deficiency_**



**_Innovation_**


**_method_**




## Discussion

**_doubt_**



**_direction_**



## Enlightment

#### Writing

**_Logic_**

**_Good Picture_**

**_Analysis_**


#### Method::VQ; 

## Conclusion:: 




## Reference

## Chat

一、对摘要Abstract进行详细介绍和总结，格式：1、逐句分析：英文原句+汉语翻译；2、摘要总结：对整段的总结

**1、逐句分析**
- “We present a learning-based ==channel-adaptive joint source and channel coding (CA-JSCC) scheme== for wireless image transmission ==over multipath fading channels.==”：我们提出了一种基于学习的信道自适应联合信源信道编码（CA-JSCC）方案，用于多径衰落信道上的无线图像传输。 - “The proposed method is an ==end-to-end autoencoder== architecture with a dualattention mechanism employing ==orthogonal frequency division multiplexing (OFDM)== transmission.”：所提出的方法是一种端到端的自动编码器架构，具有采用正交频分复用（OFDM）传输的双注意力机制。 - “Unlike the previous works, our approach is ==adaptive to channel-gain and noise-power variations by exploiting the estimated channel state information (CSI)==.”：与先前的工作不同，我们的方法通过利用估计的信道状态信息（CSI）来适应信道增益和噪声功率的变化。 - “Specifically, with the proposed ==dual-attention mechanism==, our model can learn to map the features and ==allocate transmission  power resources== judiciously to the available subchannels based on the estimated CSI.”：具体而言，借助所提出的双注意力机制，我们的模型可以根据估计的CSI学习映射特征，并明智地将传输功率资源分配到可用的子信道。 - “Extensive numerical experiments verify that CA-JSCC achieves state-of-the-art performance among existing JSCC schemes.”：大量的数值实验验证了CA-JSCC在现有JSCC方案中达到了最先进的性能。 - “In addition, CA-JSCC is robust to varying channel conditions and can better exploit the limited channel resources by transmitting critical features over better subchannels.”：此外，CA-JSCC对变化的信道条件具有鲁棒性，并且可以通过在更好的子信道上传输关键特征来更好地利用有限的信道资源。 
**2、摘要总结** 本文提出一种基于学习的CA-JSCC方案用于多径衰落信道上的无线图像传输。该方案是端到端自动编码器架构，利用双注意力机制和OFDM传输，能根据估计的CSI自适应调整特征映射与功率分配，适应信道变化。实验表明，CA-JSCC性能领先，对不同信道条件鲁棒，可有效利用信道资源。

二、对I. INTRODUCTION章节进行详细介绍和总结，格式：1、逐段分析：对英文每段的原文段落+汉语翻译+段落总结；2、章节提到的参考文献总结（参考文献序号，相关内容）；3、整个I. INTRODUCTION章节的总结

 **1、逐段分析**
	  - **第一段** 
		  - 英文原文：“SHANNON’s separation theorem states that it is optimal to design source and channel codes separately for an to design source and channel codes separately for an infinite block-length [1]. However, an increasing number of wireless applications, such as Internet-of-Things and edge intelligence [2], [3], [4], require the efficient transmission of large volumes of data under strict delay constraints, resulting in an increasing interest in joint source channel coding (JSCC) in recent years. Recently, inspired by the success of deep learning techniques, researchers have started to exploit deep neural networks to design novel and competitive JSCC schemes to transmit high information content signals, such as images or videos, over wireless channels [5], [6], [7], [8], [9], [10], [11], [12], [13].” - 中文翻译：香农分离定理指出，对于无限长的码块长度，分别设计信源编码和信道编码是最优的[1]。然而，越来越多的无线应用，如物联网和边缘智能[2]、[3]、[4]，需要在严格的延迟约束下高效传输大量数据，这导致近年来对联合信源信道编码（JSCC）的兴趣日益增加。最近，受深度学习技术成功的启发，研究人员开始利用深度神经网络设计新颖且有竞争力的JSCC方案，以通过无线信道传输高信息含量的信号，如图像或视频[5]、[6]、[7]、[8]、[9]、[10]、[11]、[12]、[13]。
		  - 段落总结：介绍香农分离定理及当前无线应用需求促使对JSCC兴趣增加，深度学习技术被用于设计JSCC方案。 
	  - **第二段** 
		  - 英文原文：“This was later extended to feedback channels in [6] and to bandwidth-adaptive transmission in [7]. In [8], authors consider JSCC over orthogonal frequency division multiplexing (OFDM) channels. An alternative generative architecture is considered in [9], [10], [11].” - 中文翻译：这后来在[6]中扩展到反馈信道，在[7]中扩展到带宽自适应传输。==在[8]中，作者考虑了正交频分复用（OFDM）信道上的JSCC。在[9]、[10]、[11]中考虑了另一种生成式架构==。 - 段落总结：阐述了前人对JSCC研究的扩展方向，包括反馈信道、带宽自适应传输以及不同的架构。 
		- **第三段** 
			- 英文原文：“However, adaptability to various channel conditions is still a challenge for deep-learning-based JSCC. Methods in [5], [6], [7] are either trained for a specific signal-to-noise ratio (SNR), or for a range of channel SNRs. The former requires significant storage memory to store different network parameters for different channel conditions, while the latter sacrifices performance and does not exploit the channel state information (CSI). In conventional digital communication systems, CSI at the transmitter can allow power allocation to boost the communication rate. In [8], [12], [13], CSI is used in a similar manner in the context of learning-aided design, mainly to adjust the feature weights according to the CSI; however, in the case of OFDM, CSI will be instrumental not only for power control, but also to decide the mapping of the features to different subcarriers according to their relative qualities. For example, more critical features of the input image can be mapped to more reliable subcarriers.” 
			- 中文翻译：然而，对于基于深度学习的JSCC来说，对各种信道条件的适应性仍然是一个挑战。[5]、[6]、[7]中的方法要么针对特定的信噪比（SNR）进行训练，要么针对一系列信道SNR进行训练。前者需要大量的存储空间来存储不同信道条件下的不同网络参数，而后者牺牲了性能且未利用信道状态信息（CSI）。在传统数字通信系统中，发射机处的CSI可用于功率分配以提高通信速率。在[8]、[12]、[13]中，CSI在学习辅助设计的背景下以类似的方式被使用，主要是根据CSI调整特征权重；然而，在OFDM情况下，CSI不仅对功率控制有用，还可根据子载波的相对质量决定特征到不同子载波的映射。例如，输入图像的更关键特征可以映射到更可靠的子载波。 
			- 段落总结：指出基于深度学习的JSCC在信道适应性方面存在问题，前人方法的不足，==强调在OFDM中CSI对特征映射和功率控制的重要性==。 
	- **第四段** 
		- 英文原文：“We introduce a channel-adaptive JSCC (CA-JSCC) scheme, which employs a dual-attention mechanism to adjust its features in the multi-scale intermediate layers according to the estimated CSI at the encoder and decoder. Our dual-attention mechanism employs both channel-wise attention and spatial attention, and jointly learns to map the features to the subcarriers and to allocate power judiciously. Our method achieves state-of-the-art performance and can adapt to different channel conditions.” 
		- 中文翻译：我们引入一种信道自适应JSCC（CA-JSCC）方案，该方案采用双注意力机制，根据编码器和解码器处估计的CSI在多尺度中间层调整其特征。我们的双注意力机制同时采用信道注意力和空间注意力，并共同学习将特征映射到子载波并明智地分配功率。我们的方法实现了最先进的性能并能适应不同的信道条件。 
		- 段落总结：介绍本文提出的CA-JSCC方案，包括双注意力机制及其功能，以及该方案的性能优势。 
	1. 据我们所知，之前尚未研究过==基于 OFDM 的 JSCC 的信道适应性==。所有先前的方法都要求训练和测试信噪比相匹配，且没有充分利用 CSI。
	2. 我们提出了一种 CA-JSCC 方案，该方案在==各种信噪比和带宽场景下==都具有最先进的性能。我们==提出一种双注意力机制==，同时利用估计的 CSI 来辅助特征和功率资源的分配，以适应时变信道条件。
**2、章节提到的参考文献总结** 
- **参考文献[1]**：与香农分离定理相关，该定理指出在无限长码块长度下分别设计信源和信道编码是最优的。
- **参考文献[2] - [4]**：涉及物联网和边缘智能等无线应用，这些应用对数据传输有严格延迟约束，促使了对联合信源信道编码（JSCC）的研究。 
- **参考文献[5] - [13]**：展示了前人在JSCC方案设计方面的工作，包括不同的研究方向如反馈信道、带宽自适应传输、不同架构以及在OFDM信道上的考虑等，还涉及深度学习技术在JSCC中的应用及存在的问题，如信道适应性挑战、CSI的利用方式等。 

**3、整个I. INTRODUCTION章节的总结**
本章节首先介绍香农分离定理，指出在实际无线应用中由于严格延迟约束促使对联合信源信道编码（JSCC）兴趣增加，深度学习技术开始用于设计JSCC方案。接着阐述前人对JSCC研究的扩展方向，然后分析基于深度学习的JSCC在信道适应性方面面临的挑战，包括前人方法的局限。最后引出本文提出的信道自适应JSCC（CA-JSCC）方案，采用双注意力机制，能根据估计的CSI调整特征映射和功率分配，实现先进性能并适应不同信道条件。

