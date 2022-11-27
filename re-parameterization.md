# Table of Contents
- [Re-parameterization Papers](#re-parameterization-papers)
- [Articles](#articles)


# Re-parameterization Papers
- **RepGhost: A Hardware-Efficient Ghost Module via Re-parameterization** <Br>
Chengpeng Chen, Zichao Guo, Haien Zeng, Pengfei Xiong, Jian Dong <Br>
[arXiv 2211] [[Pytorch-Code](https://github.com/ChengpengChen/RepGhost)] <Br>
[★] 修改ghost block, 将concat替换为add, 加速推理.

- **Re-parameterizing Your Optimizers rather than Architectures** <Br>
[Xiaohan Ding](https://dingxiaohan.xyz/), Honghao Chen, Xiangyu Zhang, Kaiqi Huang, [Jungong Han](https://jungonghan.github.io/), Guiguang Ding <Br>
[arXiv 2205] [[Pytorch-Code](https://github.com/DingXiaoH/RepOptimizers)] <Br>
[**RepOpt**]

- **RepSR: Training Efficient VGG-style Super-Resolution Networks with Structural Re-Parameterization and Batch Normalization** <Br>
[Xintao Wang](https://xinntao.github.io/), [Chao Dong](http://xpixel.group/), Ying Shan <Br>
[MM 2022] [[Pytorch-Code](https://github.com/TencentARC/RepSR)] <Br>

- **DyRep: Bootstrapping Training with Dynamic Re-parameterization** <Br>
Tao Huang, [Shan You](https://shanyou92.github.io/), Bohan Zhang, [Yuxuan Du](https://yuxuan-du.github.io/), [Fei Wang](http://wangfei.info/), Chen Qian, Chang Xu <Br>
[CVPR 2022] [[Pytorch-Code](https://github.com/hunto/DyRep)] <Br>

- **OREPA: Online Convolutional Re-parameterization** <Br>
Mu Hu, Junyi Feng, Jiashen Hua, Baisheng Lai, Jianqiang Huang, [Xiaojin Gong](https://person.zju.edu.cn/en/gongxj), Xiansheng Hua <Br>
[CVPR 2022] [[Pytorch-Code](https://github.com/JUGGHM/OREPA_CVPR2022)] <Br>

- **Scaling Up Your Kernels to 31x31: Revisiting Large Kernel Design in CNNs** <Br>
[Xiaohan Ding](https://dingxiaohan.xyz/), Xiangyu Zhang, Yizhuang Zhou, [Jungong Han](https://jungonghan.github.io/), Guiguang Ding, [Jian Sun](http://www.jiansun.org/) <Br>
[CVPR 2022] [[Pytorch-Code](https://github.com/DingXiaoH/RepLKNet-pytorch)] <Br>

- **About Edge-oriented Convolution Block for Real-time Super Resolution on Mobile Devices** <Br>
Xindong Zhang, [Hui Zeng](https://huizeng.github.io/), [Lei Zhang](http://www4.comp.polyu.edu.hk/~cslzhang/) <Br>
[MM 2021 Oral] [[Pytorch-Code](https://github.com/xindongzhang/ECBSR)]  <Br>
[**ECBSR**] [★★] Low Level任务重参数化, 并行卷积模块+sobel/laplacian算子

- **ResRep: Lossless CNN Pruning via Decoupling Remembering and Forgetting** <Br>
[Xiaohan Ding](https://dingxiaohan.xyz/), Tianxiang Hao, [Jianchao Tan](https://jianchaotan.github.io/), [Ji Liu](https://jiliu-ml.org/), [Jungong Han](https://jungonghan.github.io/), [Yuchen Guo](http://ise.thss.tsinghua.edu.cn/MIG/gyc.html), Guiguang Ding <Br>
[ICCV 2021] [[Pytorch-Code](https://github.com/DingXiaoH/RepVGG)] <Br>
[★] 利用重参数化做剪枝

- **Repvgg: Making vgg-style convnets great again** <Br>
[Xiaohan Ding](https://dingxiaohan.xyz/), Xiangyu Zhang, [Ningning Ma](https://www.cse.ust.hk/~nmaac/), [Jungong Han](https://sites.google.com/site/jungonghan77/), Guiguang Ding, [Jian Sun](http://www.jiansun.org/) <Br>
[CVPR 2021] [[Pytorch-Code](https://github.com/DingXiaoH/RepVGG)] <Br>
[★★] 训练时加入并行1x1 conv和shortcut, 推理时间其合并成一个conv

- **Diverse Branch Block: Building a Convolution as an Inception-like Unit** <Br>
[Xiaohan Ding](https://dingxiaohan.xyz/), Xiangyu Zhang, [Jungong Han](https://sites.google.com/site/jungonghan77/), Guiguang Ding <Br>
[CVPR 2021] [[Pytorch-Code](https://github.com/DingXiaoH/DiverseBranchBlock)] <Br>
[★]

- **ACNet: Strengthening the Kernel Skeletons for Powerful CNN via Asymmetric Convolution Blocks** <Br>
[Xiaohan Ding](https://dingxiaohan.xyz/), [Yuchen Guo](http://ise.thss.tsinghua.edu.cn/MIG/gyc.html), Guiguang Ding, [Jungong Han](https://jungonghan.github.io/)  <Br>
[ICCV 2019] [[Pytorch-Code](https://github.com/DingXiaoH/ACNet)] <Br>
[★★] 3x3, 1x3, 3x1并行



# Articles
- [YOLOv6量化部署实战指南](https://zhuanlan.zhihu.com/p/568521540)