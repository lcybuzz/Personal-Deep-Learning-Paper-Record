记录使用GAN相关影响力较大的论文. 对于GAN在各领域的应用, 如使用GAN进行图像恢复, inpainting等, 只记录较重要的一些论文.

可能与其它方向的论文记录有重叠.


### Conditional GAN ★★
**[Paper]** (arXiv 1411) Conditional Generative Adversarial Nets <Br>
**[Author]** Mehdi Mirza, Simon Osindero  <Br>
给定类别的图像生成, 把label分别加入G和D的输入中
 
### DCGAN ★★★
**[Paper]** (arXiv 1511) Unsupervised Representation Learning with Deep Convolutional Generative Adversarial Networks <Br>
**[Author]** Alec Radford, [Luke Metz](http://lukemetz.com/), [Soumith Chintala](https://soumith.ch/)  <Br>
**[[TF-Code](https://github.com/carpedm20/DCGAN-tensorflow)]** <Br>
经典生成网络
 
### f-GAN ★
**[Paper]** (NIPS 2016) f-GAN: Training Generative Neural Samplers using Variational Divergence Minimization <Br>
**[Author]** [Sebastian Nowozin](http://nowozin.net/sebastian/), Botond Cseke, [Ryota Tomioka](http://tomioka.dk/)  <Br>
 
### InfoGAN
**[Paper]** (arXiv 1606) InfoGAN: Interpretable Representation Learning by Information Maximizing Generative Adversarial Nets <Br>
**[Author]** [Xi Chen](https://peterchen.us/), [Yan Duan](http://rockyduan.com/), [Rein Houthooft](http://rockyduan.com/), [John Schulman](http://joschu.net/), [Ilya Sutskever](http://www.cs.utoronto.ca/~ilya/), [Pieter Abbeel](https://people.eecs.berkeley.edu/~pabbeel/) <Br>
**[[TF-Code](https://github.com/openai/InfoGAN)]** <Br>
 
### improved-gan ★★
**[Paper]** (arXiv 2016) Improved Techniques for Training GANs <Br>
**[Author]** Tim Salimans, [Ian Goodfellow](https://www.iangoodfellow.com/), [Wojciech Zaremba](http://wojzaremba.com/), Vicki Cheung, Alec Radford, Xi Chen  <Br>
**[[TF-Code](https://github.com/openai/improved-gan)]** <Br>
提出了更好训练GAN的几个技巧

### ACGAN ★
**[Paper]** (ICML 2017) Conditional Image Synthesis with Auxiliary Classifier GANs <Br>
**[Author]** [Augustus Odena](http://www.augustusodena.com/), [Christopher Olah](http://colah.github.io/), [Jonathon Shlens](https://shlens.github.io/)  <Br>
 **[[Unofficial-TF-Code](https://github.com/lukedeo/keras-acgan)]** **[[Unofficial-Pytorch-Code](https://github.com/clvrai/ACGAN-PyTorch)]** <Br>
 输入包括噪声和label, 判别器输出真假和label. 可用于生成分类数据.

### WGAN ★★★
**[Paper]** (ICLR 2017) Towards Principled Methods for Training Generative Adversarial Networks <Br>
**[Author]** Martin Arjovsky, [Léon Bottou](https://leon.bottou.org/)  <Br>
**[Paper]** (ICML 2017) Wasserstein generative adversarial networks <Br>
**[Author]** Martin Arjovsky, [Soumith Chintala](https://soumith.ch/), [Léon Bottou](https://leon.bottou.org/)  <Br>
**[Paper]** (NIPS 2017) Improved training of wasserstein gans <Br>
**[Author]** [Ishaan Gulrajani](https://ishaan.io/), Faruk Ahmed, Martin Arjovsky, [Vincent Dumoulin](https://vdumoulin.github.io/), Aaron C Courville  <Br>
**[[TF-Code](https://github.com/igul222/improved_wgan_training)]** **[[Blog](https://zhuanlan.zhihu.com/p/25071913)]**<Br>
**(GAN的改进)**  提出了一种改进的GAN训练方式
 
### LSGAN ★★☆
**[Paper]** (ICCV 2017) Least Squares Generative Adversarial Networks <Br>
**[Author]** [Xudong Mao](https://xudongmao.github.io/), [Qing Li](https://www4.comp.polyu.edu.hk/~csqli/), [Haoran Xie](http://home.eduhk.hk/~hxie/), Raymond Y.K. Lau, Zhen Wang, Stephen Paul Smolley <Br>
**[[TF-Code](https://github.com/xudonmao/LSGAN)]** **[[Unofficial-TF-Code](https://github.com/GunhoChoi/LSGAN-TF)]** <Br>
**(GAN loss)**  常用的一种GAN loss
 
### Progressive Growing of GANs ★★☆
**[Paper]** (ICLR 2018) Progressive Growing of GANs for Improved Quality, Stability, and Variation <Br>
**[Author]** [Tero Karras](https://research.nvidia.com/person/tero-karras), [Timo Aila](https://research.nvidia.com/person/timo-aila), [Samuli Laine](https://users.aalto.fi/~laines9/), [Jaakko Lehtinen](https://users.aalto.fi/~lehtinj7/)   <Br>
**[[Pytorch-Code](https://github.com/tkarras/progressive_growing_of_gans)]** <Br>
提出了一个渐进式训练GAN的方案, 可以实现大分辨率图像的生成(1024x1024人脸), 并提出了一些训练的技巧. 代码Star非常多, 可以学习一下 <Br>

### Spectral Norm ★★☆
**[Paper]**  (ICLR 2018 Oral) Spectral Normalization for Generative Adversarial Networks <Br>
**[Author]** [Takeru Miyato](http://takerum.github.io/), Toshiki Kataoka, Masanori Koyama, [Yuichi Yoshida](http://research.nii.ac.jp/~yyoshida/) <Br>
**[[Chainer-Code](https://github.com/pfnet-research/sngan_projection)]** **[[TF-Code](**[[Chainer-Code](https://github.com/pfnet-research/sngan_projection)]**)]** **[[Blog1](https://christiancosgrove.com/blog/2018/01/04/spectral-normalization-explained.html)]**  **[[Blog2](http://kaizhao.net/posts/spectral-norm)]** <Br>
 **(提升GAN稳定性)** 非常常用的一种对判别器的正则化方法, 注意不能与BN同时使用

### GANSeeing 
**[Paper]**  (ICCV 2019) Seeing What a GAN Cannot Generate <Br>
**[Author]** [David Bau](https://people.csail.mit.edu/davidbau/home/), [Jun-Yan Zhu](https://www.cs.cmu.edu/~junyanz/), Jonas Wulff, [William Peebles](https://www.wpeebles.com/), [Hendrik Strobelt](http://hendrik.strobelt.com/), [Bolei Zhou](http://bzhou.ie.cuhk.edu.hk/), [Antonio Torralba](https://groups.csail.mit.edu/vision/torralbalab/) <Br>
**[[Project](https://ganseeing.csail.mit.edu/)]**  **[[Pytorch-Code](https://github.com/davidbau/ganseeing)]**  <Br>

### SinGAN 
**[Paper]**  (ICCV 2019 Best Paper) SinGAN：Learning a generative Model from a Single Natural Image <Br>
**[Author]** [Tamar Rott Shaham](https://tamarott.github.io/), [Tali Dekel](http://people.csail.mit.edu/talidekel/), [Tomer Michaeli](https://tomer.net.technion.ac.il/) <Br>
**[[Pytorch-Code](https://github.com/tamarott/SinGAN)]**  <Br>

### SAGAN
**[Paper]**  (ICML 2019) Self-Attention Generative Adversarial Networks <Br>
**[Author]** [Han Zhang](https://sites.google.com/view/hanzhang), [Ian Goodfellow](https://www.iangoodfellow.com/), [Dimitris Metaxas](https://www.cs.rutgers.edu/~dnm/), [Augustus Odena](http://www.augustusodena.com/) <Br>
**[[Pytorch-Code](https://github.com/heykeetae/Self-Attention-GAN)]**  **[[TF-Code1](https://github.com/brain-research/self-attention-gan)]** **[[TF-Code2](https://github.com/taki0112/Self-Attention-GAN-Tensorflow)]**<Br>
 
### RAGAN ★★☆
**[Paper]**  (ICLR 2019) The relativistic discriminator: a key element missing from standard GAN <Br>
**[Author]** Alexia Jolicoeur-Martineau <Br>
**[[Code](https://github.com/AlexiaJM/RelativisticGAN)]**  <Br>
提出使用真假样本直接的相对距离作为衡量discriminator的准则
  
### KernelGAN ★★
**[Paper]**  (NIPS 2019 Oral) Blind Super-Resolution Kernel Estimation using an Internal-GAN <Br>
**[Author]** Sefi Bell-Kligler, [Assaf Shocher](http://www.wisdom.weizmann.ac.il/~/assafsho/), [Michal Irani](https://www.weizmann.ac.il/math/irani/) <Br>
**[[Project](http://www.wisdom.weizmann.ac.il/~vision/kernelgan/)]** **[[Pytorch-Code](https://github.com/sefibk/KernelGAN)]**  <Br>
**(zero-shot, 降质核估计)**  无监督预测降质核并进行超分的方法. 使用若干个现象卷积层的GAN预测降质kernel, 训练的的GAN可以合成一个kernel, 作为该图形的降质核, 网络训练采用LSGAN和若干正则项构成. 预测的模糊核作为ZSSR的降质核, 再无监督地预测炒粉结果

### DGP ★★
**[Paper]** (ECCV 2020 Oral) Exploiting Deep Generative Prior for Versatile Image Restoration and Manipulation <Br>
**[Author]** [Xingang Pan](https://xingangpan.github.io/), [Xiaohang Zhan](https://xiaohangzhan.github.io/), [Bo Dai](http://daibo.info/), [Dahua Lin](http://dahua.site/), [Chen Change Loy](http://personal.ie.cuhk.edu.hk/~ccloy/), [Ping Luo](http://luoping.me/) <Br>
**[[Pytorch-Code](https://github.com/XingangPan/deep-generative-prior)]** <Br>
**(online finetune, 无需训练样本对)**  提出用预训练的GAN作为先验, 无需在特定任务上finetune, 即可实现超分, 上色等图像恢复任务和图像变形，类别转换等图像编辑功能. 论文主要是在一般GAN inversion的基础上, 提出同时优化隐向量z和生成网络参数, 达到了更好更自然的效果.


