# Personal-Deep-Learning-Paper-Record
# Under Construction
# Table of Contents
- [Network](#network)
- [General](#general)
- [Optimization](#optimization)
- [Theory](#theory)
# Rank
- Network <Br>
  - ★★★ <Br>
  - ★★ <Br>
  **[ResNeXt]**, **[DenseNet]** <Br>
  - ★ <Br>
  **[Residual Attention Network]**, **[SENet]**, **[GENet]** <Br>
  
- General <Br>
  - ★★★ <Br>
  - ★★ <Br>
  **[Deformable-ConvNets]** <Br>
  - ★ <Br>
  **[OctaveConv]**
- Theory <Br>
  - ★★★ <Br>
  - ★★ <Br>
    **[ERF]**, **[Convolution Arithmetic]** <Br>
  - ★ <Br>
  
# Network
### **RAM**
**[Paper]** Recurrent models of visual attention <Br>
**[Year]** NIPS 2014 <Br>
**[Authors]** [Volodymyr Mnih](https://www.cs.toronto.edu/~vmnih/), [Nicolas Heess](http://homepages.inf.ed.ac.uk/s0677090/), [Alex Graves](https://www.cs.toronto.edu/~graves/), [Koray Kavukcuoglu](http://koray.kavukcuoglu.org/)<Br>
 **[Pages]** <Br>
  https://github.com/kevinzakka/recurrent-visual-attention (Unofficial) <Br>
  https://github.com/jlindsey15/RAM (Unofficial) <Br>
  https://github.com/zhongwen/RAM  (Unofficial) <Br>
 **[Description]**<Br>

### **ResNeXt ★★**
**[Paper]** Aggregated Residual Transformations for Deep Neural Networks <Br>
**[Year]** arXiv 1611 <Br>
**[Authors]** [Saining Xie](http://vcl.ucsd.edu/~sxie/), [Ross Girshick](http://www.rossgirshick.info/), [Piotr Dollár](https://pdollar.github.io/), [Zhuowen Tu](http://pages.ucsd.edu/~ztu/), [Kaiming He](http://kaiminghe.com/) <Br>
 **[Pages]** https://github.com/facebookresearch/ResNeXt <Br>
 **[Description]**<Br>
1) ResNet的改进版, 复杂度不变的情况下提升了精度. 只看了其它blog的解析, 自己没读 

### **DenseNet ★★**
**[Paper]** Densely Connected Convolutional Networkss <Br>
**[Year]** CVPR 2017 Best Paper<Br>
**[Authors]** [Gao Huang](http://www.cs.cornell.edu/~gaohuang/), [Zhuang Liu](https://liuzhuang13.github.io/), [Laurens van der Maaten](https://lvdmaaten.github.io/), [Kilian Q. Weinberger](http://www.cs.cornell.edu/~kilian/)	<Br>
**[Pages]** https://github.com/liuzhuang13/DenseNet <Br>
**[Description]**<Br>
1) 核心思路是每一层都与之前的层直接相连, 实现特征的重复利用, 并使得每层的feature map数可以设置的很小. <Br>
2) 实际设计中, 采用dense block + transition layer的结构. 每个dense block中进行feature的密集连接(将前面得到feature直接concat到后面的feature map上), 并用1*1的conv降维, transition layer的作用也是降低前一block的输出维度. <Br>
3) 优点: 性能好, 相对而言参数较少. 缺点: 很耗内存. 以caffe为例, concat层会为需要concat的feature另外分配一份新的内存空间, 这样第L层的feature实际需要L(L+1)/2个feature的空间. 作者团队给出了优化策略, 还没看. <Br>
  
### ***Residual Attention Network* ★**
**[Paper]** Residual Attention Network <Br>
**[Year]** CVPR 2017 Spotlight <Br>
**[Authors]** Fei Wang, [Mengqing Jiang](https://github.com/Jmq14), Chen Qian, [Shuo Yang](http://shuoyang1213.me/), Chen Li, Honggang Zhang, [Xiaogang Wang](http://www.ee.cuhk.edu.hk/~xgwang/), [Xiaoou Tang](https://www.ie.cuhk.edu.hk/people/xotang.shtml) <Br>
 **[Pages]** https://github.com/fwang91/residual-attention-network <Br>
 **[Description]**<Br>
1) 提出了一个形式上与resnet很相似的结构: resudual attention net, 将attention机制结合进前馈深度神经网络中. <Br>
2) 所谓residual attention network, 即采用类似residual block的(1+M(x))*F(x)的形式, 而不是直接将attention map M(x)直接与feature map相乘, 避免了使feature数值越来越小的问题. Attention mask branch采用了encoder-decoder的结构. <Br>
3) 虽然本文看上去就是将resnet中的high way一支改成encoder-decoder结构的mask branch, 但其思路和论述的角度比较独特, 值得学习. 从结果上看attention mask branch的确能起到抑制背景, 增强前景feature的效果, 感觉挺神奇. 不过, 这一机制能否用到如语义分割等其他任务上存疑.<Br>
  
### **SENet ★☆**
**[Paper]** Squeeze-and-Excitation Networks <Br>
**[Year]** CVPR 2018 <Br>
**[Authors]**  Jie Hu, Li Shen, Gang Sun<Br>
**[Pages]** https://github.com/hujie-frank/SENet <Br>
**[Description]** <Br>
1) 粗读, 提出了一个修正channel间feature的模块, 该模块可以嵌入到任意网络模型中. <Br>
2) 方法很简单, squeeze部分将每个channel的feature求和(C*H*W -> C*1), excitation部分用两个全连接层计算每个channel的权重, 最后用这个权重对feature加权. <Br>
3) 主要用于分类中, 实验细节没看. <Br>
  
### **GENet ★☆**
**[Paper]** Gather-Excite: Exploiting Feature Context in Convolutional Neural Networks <Br>
**[Year]** NIPS 2018 <Br>
**[Authors]**  Jie Hu, Li Shen, [Samuel Albanie](http://www.robots.ox.ac.uk/~albanie/), Gang Sun, [Andrea Vedaldi](http://www.robots.ox.ac.uk/~vedaldi/)<Br>
**[Pages]**https://github.com/hujie-frank/GENet <Br>
**[Description]** <Br>
1) 在SENet的基础上, 提出了gather-excite操作. Gather就是收集long-range空间信息的操作, excite就是将gather的信息分配给local feature的操作. 作者认为GE操作可以更有效地挖掘context信息, 并增加feature的可复用性. <Br>
2) Gather操作可以有多种形式, 如无参数的average pooling(GE-), 有参数的多级depth-wise卷积(GE), 全局depth-wise卷积(GE+)等. 其中无参数的策略对性能有轻微提升, GE+性能最好, 所需参数最多. Excite操作就是把gather的结果经过scale后与原feature的过程. <Br>
3) 方法主要在分类任务上进行验证. 思路和做法很简单, 论述方法值得学习. <Br>

# General

### **Deformable-ConvNets ★★**
**[Paper]** Deformable Convolutional Networks <Br>
**[Year]** ICCV 2017 Oral<Br>
**[Authors]**	[Jifeng Dai](http://www.jifengdai.org/), [Haozhi Qi](http://haozhi.io/), [Yuwen Xiong](http://www.cs.toronto.edu/~yuwen/), [Yi Li](https://liyi14.github.io/), [Guodong Zhang](http://www.cs.toronto.edu/~gdzhang/), [Han Hu](https://sites.google.com/site/hanhushomepage/), [Yichen Wei](https://www.microsoft.com/en-us/research/people/yichenw/) <Br>
 **[Pages]** https://github.com/msracver/Deformable-ConvNets <Br>
 **[Description]**<Br>
1) 传统CNN对几何形变的适应力差, 这是标准卷积中的规则格点采样造成的. 为此论文提出了deformable convolution和deformable ROI pooling
2) 具体做法很简洁, 即用卷积层从前一层的feature map中学习到每个位置的offsets, 整个过程是完全可微的.
3) 实验效果很好. 论文可以之后精读

### **OctaveConv ★**
**[Paper]** Drop an Octave: Reducing Spatial Redundancy in Convolutional Neural Networks with Octave Convolution <Br>
**[Year]** arXiv 1904<Br>
**[Authors]**	[Yunpeng Chen](https://cypw.github.io/), Haoqi Fan, Bing Xu, [Zhicheng Yan](https://sites.google.com/view/zhicheng-yan), [Yannis Kalantidis](http://www.skamalas.com/), [Marcus Rohrbach](http://rohrbach.vision/), [Shuicheng Yan](https://www.ece.nus.edu.sg/stfpage/eleyans/), [Jiashi Feng](https://sites.google.com/site/jshfeng/) <Br>
 **[Pages]** https://github.com/facebookresearch/OctConv <Br>
 **[Description]**<Br>
  1) 提出一种新的卷积形式, 试图将特征图的高低频分类分解, 并在不同尺度上处理, 以节省内存和计算成本的效果. <Br>
  2) 以为会真正提出分解特征图高频低频分类的算法, 其实只是做了个avg pool把原feature降采样两倍作为低频组. 所谓的高低频组分别卷积, 并且两组之间也有信息传递. 至于这种方案到底是不是真的能提取出高低频的特征图, 文中并未给出任何理论证明和实验验证. <Br>
  3) 实验做得非常多, 写作也值得学习. 但是看完之后还是有点


# Optimization
### **Uncertainty Weighting ★★**
**[Paper]** Multi-Task Learning Using Uncertainty to Weigh Losses for Scene Geometry and Semantics <Br>
**[Year]** CVPR 2018 <Br>
**[Authors]**  [Alex Kendall](https://alexgkendall.com/), [Yarin Gal](http://www.cs.ox.ac.uk/people/yarin.gal/website/), [Roberto Cipolla](https://mi.eng.cam.ac.uk/~cipolla/)<Br>
**[Pages]** https://github.com/alexgkendall/multitaskvision<Br>
**[Description]** <Br>
1) 提出了一种用不确定度为多任务学习中每个loss赋权重的方法. 作者证从多任务的最大似然估计出发, 证明了在多任务学习中, 分类和回归问题的loss应该用1/sigma^2来对其进行加权, 其中sigma表示该任务的不确定度. 实际应用中, 作者通过为每个任务分别学习其log sigma来自适应地得到每个loss的weight. <Br>
2) 分类任务加入一1/sigma^2作为scale factor的原理没有搞清楚. <Br>

# Theory
### **ERF ★★**
**[Paper]** Understanding the Effective Receptive Field in Deep Convolutional Neural Networks <Br>
**[Year]** NIPS 2016 <Br>
**[Authors]**  [Wenjie Luo](http://www.cs.toronto.edu/~wenjie/), [Yujia Li](http://www.cs.toronto.edu/~yujiali/), [Raquel Urtasun](http://www.cs.toronto.edu/~urtasun/), [Richard Zemel](http://www.cs.toronto.edu/~zemel/inquiry/home.php)<Br>
**[Pages]** <Br>
**[Description]** <Br>
1) 从理论上分析了CNN中的有效感受野其实比理论感受野小很多, 且呈现高斯分布的现象. <Br>
2) 很多数学没读懂, 有去复习概率和组合数学的冲动>_<. <Br>
  
 ### **Convolution Arithmetic ★★**
**[Paper]** A guide to convolution arithmetic for deep learning <Br>
**[Year]** technical report, arXiv 1603 <Br>
**[Authors]**  [Vincent Dumoulin](https://vdumoulin.github.io/), Francesco Visin <Br>
**[Pages]** https://github.com/vdumoulin/conv_arithmetic <Br>
**[Description]** <Br>
  1) 讨论了卷积, 池化, 转置卷积的输入输出关系, 供需要时查阅 <Br>
