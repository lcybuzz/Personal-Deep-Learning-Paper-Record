记录使用GAN相关影响力较大的论文. 对于GAN在各领域的应用, 如使用GAN进行图像恢复, inpainting等, 只记录较重要的一些论文.

可能与其它方向的论文记录有重叠.



- **Exploiting Deep Generative Prior for Versatile Image Restoration and Manipulation** <Br>
[Xingang Pan](https://xingangpan.github.io/), [Xiaohang Zhan](https://xiaohangzhan.github.io/), [Bo Dai](http://daibo.info/), [Dahua Lin](http://dahua.site/), [Chen Change Loy](http://personal.ie.cuhk.edu.hk/~ccloy/), [Ping Luo](http://luoping.me/) <Br>
[ECCV 2020 Oral] [[Pytorch-Code](https://github.com/XingangPan/deep-generative-prior)] <Br>
[**DGP**] [★★] **(online finetune, 无需训练样本对)**  提出用预训练的GAN作为先验, 无需在特定任务上finetune, 即可实现超分, 上色等图像恢复任务和图像变形，类别转换等图像编辑功能. 论文主要是在一般GAN inversion的基础上, 提出同时优化隐向量z和生成网络参数, 达到了更好更自然的效果.

- **Seeing What a GAN Cannot Generate** <Br>
[David Bau](https://people.csail.mit.edu/davidbau/home/), [Jun-Yan Zhu](https://www.cs.cmu.edu/~junyanz/), Jonas Wulff, [William Peebles](https://www.wpeebles.com/), [Hendrik Strobelt](http://hendrik.strobelt.com/), [Bolei Zhou](http://bzhou.ie.cuhk.edu.hk/), [Antonio Torralba](https://groups.csail.mit.edu/vision/torralbalab/) <Br>
[ICCV 2019] [[Project](https://ganseeing.csail.mit.edu/)] [[Pytorch-Code](https://github.com/davidbau/ganseeing)] <Br>
[**GANSeeing**]

- **SinGAN：Learning a generative Model from a Single Natural Image** <Br>
[Tamar Rott Shaham](https://tamarott.github.io/), [Tali Dekel](http://people.csail.mit.edu/talidekel/), [Tomer Michaeli](https://tomer.net.technion.ac.il/) <Br>
[ICCV 2019 Best Paper] [[Pytorch-Code](https://github.com/tamarott/SinGAN)] <Br>
[**SinGAN**]

- **Self-Attention Generative Adversarial Networks** <Br>
[Han Zhang](https://sites.google.com/view/hanzhang), [Ian Goodfellow](https://www.iangoodfellow.com/), [Dimitris Metaxas](https://www.cs.rutgers.edu/~dnm/), [Augustus Odena](http://www.augustusodena.com/) <Br>
[ICML 2019] [[Pytorch-Code](https://github.com/heykeetae/Self-Attention-GAN)] [[TF-Code1](https://github.com/brain-research/self-attention-gan)] [[TF-Code2](https://github.com/taki0112/Self-Attention-GAN-Tensorflow)] <Br>
[**SAGAN**]

- **The relativistic discriminator: a key element missing from standard GAN** <Br>
Alexia Jolicoeur-Martineau <Br>
[ICLR 2019] [[Code](https://github.com/AlexiaJM/RelativisticGAN)] <Br>
[**RAGAN**] [★★☆] 提出使用真假样本直接的相对距离作为衡量discriminator的准则

- **Blind Super-Resolution Kernel Estimation using an Internal-GAN** <Br>
Sefi Bell-Kligler, [Assaf Shocher](http://www.wisdom.weizmann.ac.il/~/assafsho/), [Michal Irani](https://www.weizmann.ac.il/math/irani/) <Br>
[NIPS 2019 Oral] [[Project](http://www.wisdom.weizmann.ac.il/~vision/kernelgan/)] [[Pytorch-Code](https://github.com/sefibk/KernelGAN)] <Br>
[**KernelGAN**] [★★☆] **(zero-shot, 降质核估计)**  无监督预测降质核并进行超分的方法. 使用若干个现象卷积层的GAN预测降质kernel, 训练的的GAN可以合成一个kernel, 作为该图形的降质核, 网络训练采用LSGAN和若干正则项构成. 预测的模糊核作为ZSSR的降质核, 再无监督地预测炒粉结果

- **Spectral Normalization for Generative Adversarial Networks** <Br>
[Takeru Miyato](http://takerum.github.io/), Toshiki Kataoka, Masanori Koyama, [Yuichi Yoshida](http://research.nii.ac.jp/~yyoshida/ <Br>
[ICLR 2018 Oral] [[Chainer-Code](https://github.com/pfnet-research/sngan_projection)] [[Blog1](https://christiancosgrove.com/blog/2018/01/04/spectral-normalization-explained.html)]  [[Blog2](http://kaizhao.net/posts/spectral-norm)] <Br>
[★★☆]  **(提升GAN稳定性)** 非常常用的一种对判别器的正则化方法, 注意不能与BN同时使用

- **Progressive Growing of GANs** <Br>
[Tero Karras](https://research.nvidia.com/person/tero-karras), [Timo Aila](https://research.nvidia.com/person/timo-aila), [Samuli Laine](https://users.aalto.fi/~laines9/), [Jaakko Lehtinen](https://users.aalto.fi/~lehtinj7/) <Br>
[ICLR 2018] [[Pytorch-Code](https://github.com/tkarras/progressive_growing_of_gans)] <Br>
[★★☆]

- **Least Squares Generative Adversarial Networks** <Br>
[Xudong Mao](https://xudongmao.github.io/), [Qing Li](https://www4.comp.polyu.edu.hk/~csqli/), [Haoran Xie](http://home.eduhk.hk/~hxie/), Raymond Y.K. Lau, Zhen Wang, Stephen Paul Smolley <Br>
[ICCV 2017] [[TF-Code](https://github.com/xudonmao/LSGAN)] <Br>
[**LSGAN**] [★★☆]

- **Wasserstein generative adversarial networks** <Br>
** Towards Principled Methods for Training Generative Adversarial Networks** <Br>
** Improved training of wasserstein gans <Br>
Tim Salimans, [Ian Goodfellow](https://www.iangoodfellow.com/), [Wojciech Zaremba](http://wojzaremba.com/), Vicki Cheung, Alec Radford, Xi Chen <Br>
[ICLR 2017] [[TF-Code](https://github.com/igul222/improved_wgan_training)] [[Blog](https://zhuanlan.zhihu.com/p/25071913)] <Br>
[**WGAN**] [★★★] 提出了一种改进的GAN训练方式

- **Conditional Image Synthesis with Auxiliary Classifier GANs** <Br>
[Augustus Odena](http://www.augustusodena.com/), [Christopher Olah](http://colah.github.io/), [Jonathon Shlens](https://shlens.github.io/)  <Br>
[ICML 2017]  [[Unofficial-TF-Code](https://github.com/lukedeo/keras-acgan)] [[Unofficial-Pytorch-Code](https://github.com/clvrai/ACGAN-PyTorch)] <Br>
输入包括噪声和label, 判别器输出真假和label. 可用于生成分类数据.

- **Improved Techniques for Training GANs** <Br>
Tim Salimans, [Ian Goodfellow](https://www.iangoodfellow.com/), [Wojciech Zaremba](http://wojzaremba.com/), Vicki Cheung, Alec Radford, Xi Chen <Br>
[arXiv 2016] [[TF-Code](https://github.com/openai/improved-gan)] <Br>
[★★] 提出了更好训练GAN的几个技巧

- **InfoGAN: Interpretable Representation Learning by Information Maximizing Generative Adversarial Nets** <Br>
[Xi Chen](https://peterchen.us/), [Yan Duan](http://rockyduan.com/), [Rein Houthooft](http://rockyduan.com/), [John Schulman](http://joschu.net/), [Ilya Sutskever](http://www.cs.utoronto.ca/~ilya/), [Pieter Abbeel](https://people.eecs.berkeley.edu/~pabbeel/) <Br>
[arXiv 1606] [[TF-Code](https://github.com/carpedm20/DCGAN-tensorflow)]<Br>

- **f-GAN: Training Generative Neural Samplers using Variational Divergence Minimization** <Br>
[Sebastian Nowozin](http://nowozin.net/sebastian/), Botond Cseke, [Ryota Tomioka](http://tomioka.dk/) <Br>
[NIPS 2016] [[TF-Code](https://github.com/carpedm20/DCGAN-tensorflow)]<Br>
[**f-GAN**] [★] 经典生成网络

- **Unsupervised Representation Learning with Deep Convolutional Generative Adversarial Networks** <Br>
Alec Radford, [Luke Metz](http://lukemetz.com/), [Soumith Chintala](https://soumith.ch/) <Br>
[arXiv 1511] [[TF-Code](https://github.com/carpedm20/DCGAN-tensorflow)]<Br>
[★★] 经典生成网络

- **Conditional Generative Adversarial Nets** <Br>
Mehdi Mirza, Simon Osindero <Br>
[arXiv 1411] <Br>
[★★] 给定类别的图像生成, 把label分别加入G和D的输入中

