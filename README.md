网络设计, 理论, GAN等方向的论文

# Table of Contents
- <a href='GAN.md'> GAN </a>
- [Network](#network)
- [Training Tricks](#training-tricks)
- [General](#general)
- [Optimization](#optimization)
- [Theory](#theory)
- [Pruning](#pruning)
  
# Network
- **ResNeSt: Split-Attention Networks** <Br>
[Hang Zhang](https://hangzhang.org/), Chongruo Wu, [Zhongyue Zhang](http://zhongyuezhang.com/), [Yi Zhu](https://sites.google.com/view/yizhu/home), Zhi Zhang, [Haibin Lin](https://sites.google.com/view/haibinlin/), [Yue Sun](https://aptsunny.github.io/), [Tong He](https://hetong007.github.io/), [Jonas Muller](https://people.csail.mit.edu/jonasmueller/), R. Manmatha, [Mu Li](https://www.cs.cmu.edu/~muli/), [Alex Smola](http://alex.smola.org/) <Br>
[arXiv 2004] [[Pytorch-Code](https://github.com/zhanghang1989/ResNeSt)] <Br>
[★★] 类似于将ResNeXt中的每个cardinal再分成成并行的切片, 并对这些split做attention. 性能在分类, 检测, 分割任务上都提升了不少

- **Gather-Excite: Exploiting Feature Context in Convolutional Neural Networks** <Br>
Jie Hu, Li Shen, [Samuel Albanie](http://www.robots.ox.ac.uk/~albanie/), Gang Sun, [Andrea Vedaldi](http://www.robots.ox.ac.uk/~vedaldi/) <Br>
[NIPS 2018] [[https://github.com/hujie-frank/GENet)] <Br>
[**GENet**] [★☆] 1) 在SENet的基础上, 提出了gather-excite操作. Gather就是收集long-range空间信息的操作, excite就是将gather的信息分配给local feature的操作. 作者认为GE操作可以更有效地挖掘context信息, 并增加feature的可复用性; 
2) Gather操作可以有多种形式, 如无参数的average pooling(GE-), 有参数的多级depth-wise卷积(GE), 全局depth-wise卷积(GE+)等. 其中无参数的策略对性能有轻微提升, GE+性能最好, 所需参数最多. Excite操作就是把gather的结果经过scale后与原feature的过程; 
3) 方法主要在分类任务上进行验证. 思路和做法很简单, 论述方法值得学习. <Br>

- **Squeeze-and-Excitation Networks** <Br>
Jie Hu, Li Shen, [Samuel Albanie](http://www.robots.ox.ac.uk/~albanie/), Gang Sun, [Andrea Vedaldi](http://www.robots.ox.ac.uk/~vedaldi/) <Br>
[CVPR 2018] [[Caffe-Code](https://github.com/hujie-frank/SENet)] <Br>
[**SENet**] [★★★] 经典的空间attention

- **Densely Connected Convolutional Networks** <Br>
[Gao Huang](http://www.cs.cornell.edu/~gaohuang/), [Zhuang Liu](https://liuzhuang13.github.io/), [Laurens van der Maaten](https://lvdmaaten.github.io/), [Kilian Q. Weinberger](http://www.cs.cornell.edu/~kilian/) <Br>
[CVPR 2017 Best Paper] [[Pytorch-Code](https://github.com/liuzhuang13/DenseNet)] <Br>
[**DenseNet**] [★★★] 1) 核心思路是每一层都与之前的层直接相连, 实现特征的重复利用, 并使得每层的feature map数可以设置的很小; 
2) 实际设计中, 采用dense block + transition layer的结构. 每个dense block中进行feature的密集连接(将前面得到feature直接concat到后面的feature map上), 并用1*1的conv降维, transition layer的作用也是降低前一block的输出维度; 
3) 优点: 性能好, 相对而言参数较少. 缺点: 很耗内存. 以caffe为例, concat层会为需要concat的feature另外分配一份新的内存空间, 这样第L层的feature实际需要L(L+1)/2个feature的空间. 作者团队给出了优化策略, 还没看. <Br>

- **Residual Attention Network** <Br>
Fei Wang, [Mengqing Jiang](https://github.com/Jmq14), Chen Qian, [Shuo Yang](http://shuoyang1213.me/), Chen Li, Honggang Zhang, [Xiaogang Wang](http://www.ee.cuhk.edu.hk/~xgwang/), [Xiaoou Tang](https://www.ie.cuhk.edu.hk/people/xotang.shtml) <Br>
[CVPR 2017 Spotlight] [[Caffe-Code](https://github.com/fwang91/residual-attention-network)] <Br>
[★] 提出了一个形式上与resnet很相似的结构: resudual attention net, 将attention机制结合进前馈深度神经网络中.

- **Aggregated Residual Transformations for Deep Neural Networks** <Br>
[Saining Xie](http://vcl.ucsd.edu/~sxie/), [Ross Girshick](http://www.rossgirshick.info/), [Piotr Dollár](https://pdollar.github.io/), [Zhuowen Tu](http://pages.ucsd.edu/~ztu/), [Kaiming He](http://kaiminghe.com/)  <Br>
[CVPR 2017] [[Torch-Code](https://github.com/facebookresearch/ResNeXt)] <Br>
[**ResNeXt**] [★★] ResNet的改进版, 复杂度不变的情况下提升了精度

- **Recurrent models of visual attention** <Br>
[Volodymyr Mnih](https://www.cs.toronto.edu/~vmnih/), [Nicolas Heess](http://homepages.inf.ed.ac.uk/s0677090/), [Alex Graves](https://www.cs.toronto.edu/~graves/), [Koray Kavukcuoglu](http://koray.kavukcuoglu.org/) <Br>
[NIPS 2014] <Br>
[**RAM**]




# Training Tricks	
- **CutMix: Regularization Strategy to Train Strong Classifiers with Localizable Features** <Br>
[Sangdoo Yun](https://sangdooyun.github.io/), [Dongyoon Han](https://sites.google.com/site/dyhan0920/), [Seong Joon Oh](https://coallaoh.github.io//), [Sanghyuk Chun](https://sanghyukchun.github.io/home/), [Junsuk Choe](https://sites.google.com/site/junsukchoe/), [Youngjoon Yoo](https://yjyoo3312.github.io/) <Br>
[ICCV 2019 Oral] [[Pytorch-Code](https://github.com/clovaai/CutMix-PyTorch)] <Br>
[★★] 随机将一块区域替换成另一个类别的图像, label也做相应mix


# General
- **Pixel-Adaptive Convolutional Neural Networks** <Br>
[Hang Su](https://suhangpro.github.io/), [Varun Jampani](https://varunjampani.github.io/), [Deqing Sun](https://deqings.github.io/), [Orazio Gallo](https://research.nvidia.com/person/orazio-gallo), [Erik Learned-Miller](https://people.cs.umass.edu/~elm/), [Jan Kautz](https://jankautz.com/) <Br>
[CVPR 2019] [[Project](https://suhangpro.github.io/pac/)] [[Pytorch-Code](https://github.com/NVlabs/pacnet)] <Br>
[**PAC**] [★] 采用类似双边滤波的思想, 对卷积核乘上一个根据某些特征计算出来的weight

- **LIP: Local Importance-based Pooling** <Br>
[Ziteng Gao](https://sebgao.github.io/), [Limin Wang](http://wanglimin.github.io/), Gangshan Wu <Br>
[ICCV 2019] [[Pytorch-Code](https://github.com/sebgao/LIP)] <Br>
[★]  用一个分支预测pooling的权重


- **Drop an Octave: Reducing Spatial Redundancy in Convolutional Neural Networks with Octave Convolution** <Br>
[Yunpeng Chen](https://cypw.github.io/), Haoqi Fan, Bing Xu, [Zhicheng Yan](https://sites.google.com/view/zhicheng-yan), [Yannis Kalantidis](http://www.skamalas.com/), [Marcus Rohrbach](http://rohrbach.vision/), [Shuicheng Yan](https://www.ece.nus.edu.sg/stfpage/eleyans/), [Jiashi Feng](https://sites.google.com/site/jshfeng/) <Br>
[ICCV 2019] [[MXNet-Code](https://github.com/facebookresearch/OctConv)] <Br>
[**OctaveConv**] [★]   1) 提出一种新的卷积形式, 试图将特征图的高低频分类分解, 并在不同尺度上处理, 以节省内存和计算成本的效果;
  2) 以为会真正提出分解特征图高频低频分类的算法, 其实只是做了个avg pool把原feature降采样两倍作为低频组. 所谓的高低频组分别卷积, 并且两组之间也有信息传递.

- **ShuffleNet V2: Practical Guidelines for Efficient CNN Architecture Design** <Br>
[Ningning Ma](https://nmaac.github.io/home/), Xiangyu Zhang, Hai-Tao Zheng, Jian Sun <Br>
[ECCV 2018]  <Br>
[★★★] 从FLOPs, 访存的角度, 讨论了模型设计的一些原则

- **Deformable Convolutional Networks** <Br>
[Jifeng Dai](http://www.jifengdai.org/), [Haozhi Qi](http://haozhi.io/), [Yuwen Xiong](http://www.cs.toronto.edu/~yuwen/), [Yi Li](https://liyi14.github.io/), [Guodong Zhang](http://www.cs.toronto.edu/~gdzhang/), [Han Hu](https://sites.google.com/site/hanhushomepage/), [Yichen Wei](https://www.microsoft.com/en-us/research/people/yichenw/) <Br>
[ICCV 2017 Oral] [[Pytorch-Code](https://github.com/msracver/Deformable-ConvNets)] <Br>
[★★★]  传统CNN对几何形变的适应力差, 这是标准卷积中的规则格点采样造成的. 为此论文提出了deformable convolution和deformable ROI pooling



# Optimization
- **Multi-Task Learning Using Uncertainty to Weigh Losses for Scene Geometry and Semantics** <Br>
[Alex Kendall](https://alexgkendall.com/), [Yarin Gal](http://www.cs.ox.ac.uk/people/yarin.gal/website/), [Roberto Cipolla](https://mi.eng.cam.ac.uk/~cipolla/) <Br>
[CVPR 2018] [[Unofficial-PyTorch-Code](https://github.com/ranandalon/mtl)] <Br>
[★★] 1) 提出了一种用不确定度为多任务学习中每个loss赋权重的方法. 作者证从多任务的最大似然估计出发, 证明了在多任务学习中, 分类和回归问题的loss应该用1/sigma^2来对其进行加权, 其中sigma表示该任务的不确定度. 实际应用中, 作者通过为每个任务分别学习其log sigma来自适应地得到每个loss的weight; 2) 分类任务加入一1/sigma^2作为scale factor的原理没有搞清楚. <Br>
	


# Theory
- **Understanding the Effective Receptive Field in Deep Convolutional Neural Networks** <Br>
[Wenjie Luo](http://www.cs.toronto.edu/~wenjie/), [Yujia Li](http://www.cs.toronto.edu/~yujiali/), [Raquel Urtasun](http://www.cs.toronto.edu/~urtasun/), [Richard Zemel](http://www.cs.toronto.edu/~zemel/inquiry/home.php) <Br>
[NIPS 2016] <Br>
[**ERF**] [★★] 从理论上分析了CNN中的有效感受野其实比理论感受野小很多, 且呈现高斯分布的现象.
	
- **A guide to convolution arithmetic for deep learning** <Br>
[Vincent Dumoulin](https://vdumoulin.github.io/), Francesco Visin  <Br>
[arXiv 1603] [[PyTorch-Code](https://github.com/vdumoulin/conv_arithmetic)] <Br>
[★★] 讨论了卷积, 池化, 转置卷积的输入输出关系, 供需要时查阅
	
	

# Pruning
- **Filter Pruning via Geometric Median for Deep Convolutional Neural Network Acceleration** <Br>
[Yang He](https://he-y.github.io/), [Ping Liu](https://sites.google.com/site/pingliu264/), Ziwei Wang, Zhilan Hu, [Yi Yang](https://www.uts.edu.au/staff/yi.yang) <Br>
[CVPR 2019 Oral] [[PyTorch-Code](https://github.com/he-y/filter-pruning-geometric-median)] <Br>
[**FPGM**] [★★]