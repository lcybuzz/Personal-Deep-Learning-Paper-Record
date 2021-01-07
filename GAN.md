记录使用GAN相关影响力较大的论文. 对于GAN在各领域的应用, 如使用GAN进行图像恢复, inpainting等, 只记录较重要的一些论文.

可能与其它方向的论文记录有重叠.

### improved-gan ★★
**[Paper]** (arXiv 2016) Improved Techniques for Training GANs <Br>
**[Author]** Tim Salimans, [Ian Goodfellow](https://www.iangoodfellow.com/), [Wojciech Zaremba](http://wojzaremba.com/), Vicki Cheung, Alec Radford, Xi Chen  <Br>
**[[TF-Code](https://github.com/openai/improved-gan)]** <Br>
提出了更好训练GAN的几个技巧

### CycleGAN 
**[Paper]**  (ICCV 2017) Unpaired Image-to-Image Translation using Cycle-Consistent Adversarial Networks<Br>
**[Author]** [RJun-Yan Zhu](https://www.cs.cmu.edu/~junyanz/), [Taesung Park](https://taesung.me/), [Phillip Isola](http://web.mit.edu/phillipi/), [Alexei A. Efros](https://people.eecs.berkeley.edu/~efros/) <Br>
**[[Project](https://junyanz.github.io/CycleGAN/)]**  <Br>

### Progressive Growing of GANs ★★☆
**[Paper]** (ICLR 2018) Progressive Growing of GANs for Improved Quality, Stability, and Variation <Br>
**[Author]** [Tero Karras](https://research.nvidia.com/person/tero-karras), [Timo Aila](https://research.nvidia.com/person/timo-aila), [Samuli Laine](https://users.aalto.fi/~laines9/), [Jaakko Lehtinen](https://users.aalto.fi/~lehtinj7/)   <Br>
**[[Pytorch-Code](https://github.com/tkarras/progressive_growing_of_gans)]** <Br>
提出了一个渐进式训练GAN的方案, 可以实现大分辨率图像的生成(1024x1024人脸), 并提出了一些训练的技巧. 代码Star非常多, 可以学习一下 <Br>

### StarGAN 
**[Paper]**  (CVPR 2018 Oral) StarGAN: Unified Generative Adversarial Networks for Multi-Domain Image-to-Image Translation <Br>
**[Author]** [Yunjey Choi](https://yunjey.github.io/), [Minje Choi](http://www.minjechoi.com/), Munyoung Kim, Jung-Woo Ha, [Sunghun Kim](http://home.cse.ust.hk/~hunkim/), [Jaegul Choo](https://sites.google.com/site/jaegulchoo/) <Br>
**[[Pytorch-Code](https://github.com/yunjey/stargan)]**   <Br>

### StarGAN v2
**[Paper]** (CVPR 2020) StarGAN v2: Diverse Image Synthesis for Multiple Domains <Br>
**[Author]** [Yunjey Choi](https://yunjey.github.io/), [Youngjung Uh](https://sites.google.com/site/youngjunguh), Jaejun Yoo, Jung-Woo Ha<Br>
**[[Pytorch-Code](https://github.com/clovaai/stargan-v2)]**<Br>

### BigGAN 
**[Paper]**  (arXiv 1809) Large Scale GAN Training for High Fidelity Natural Image Synthesis <Br>
**[Author]** Andrew Brock, [Jeff Donahue](https://jeffdonahue.com/), Karen Simonyan <Br>
**[[Pytorch-Code](https://github.com/ajbrock/BigGAN-PyTorch)]**  <Br>

### StyleGAN 
**[Paper]**  (CVPR 2019) A Style-Based Generator Architecture for Generative Adversarial Networks <Br>
**[Author]** Tero Karras, [Samuli Laine](https://users.aalto.fi/~laines9/), [Timo Aila](https://users.aalto.fi/~ailat1/) <Br>
**[[TF-Code](https://github.com/NVlabs/stylegan)]**  <Br>

### Image2StyleGAN 
**[Paper]**  (ICCV 2019) Image2StyleGAN: How to Embed Images Into the StyleGAN Latent Space? <Br>
**[Author]** Rameen Abdal, Yipeng Qin, Peter Wonka <Br>
**[[TF-Code](https://github.com/NVlabs/stylegan)]**  <Br>

### GANSeeing 
**[Paper]**  (ICCV 2019) Seeing What a GAN Cannot Generate <Br>
**[Author]** [David Bau](https://people.csail.mit.edu/davidbau/home/), [Jun-Yan Zhu](https://www.cs.cmu.edu/~junyanz/), Jonas Wulff, [William Peebles](https://www.wpeebles.com/), [Hendrik Strobelt](http://hendrik.strobelt.com/), [Bolei Zhou](http://bzhou.ie.cuhk.edu.hk/), [Antonio Torralba](https://groups.csail.mit.edu/vision/torralbalab/) <Br>
**[[Project](https://ganseeing.csail.mit.edu/)]**  **[[Pytorch-Code](https://github.com/davidbau/ganseeing)]**  <Br>

### SinGAN 
**[Paper]**  (ICCV 2019 Best Paper) SinGAN：Learning a generative Model from a Single Natural Image <Br>
**[Author]** [Tamar Rott Shaham](https://tamarott.github.io/), [Tali Dekel](http://people.csail.mit.edu/talidekel/), [Tomer Michaeli](https://tomer.net.technion.ac.il/) <Br>
**[[Pytorch-Code](https://github.com/tamarott/SinGAN)]**  <Br>

### RAGAN ★☆
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


